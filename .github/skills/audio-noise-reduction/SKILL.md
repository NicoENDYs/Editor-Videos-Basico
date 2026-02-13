---
name: audio-noise-reduction
description: Implementar reducción de ruido de fondo en audio de videos
---

# Reducción de Ruido de Audio

## Método 1: noisereduce library (Recomendado)
```python
import noisereduce as nr
from moviepy.editor import VideoFileClip, AudioFileClip
import numpy as np

def reduce_noise(video_path, output_path):
    # Extraer audio
    video = VideoFileClip(video_path)
    audio = video.audio
    audio_array = audio.to_soundarray()
    
    # Reducir ruido (noise reduction)
    reduced_noise = nr.reduce_noise(
        y=audio_array, 
        sr=audio.fps,
        stationary=True,
        prop_decrease=0.8  # Ajustar según necesidad
    )
    
    # Crear nuevo audio clip
    from moviepy.audio.AudioClip import AudioArrayClip
    new_audio = AudioArrayClip(reduced_noise, fps=audio.fps)
    
    # Reemplazar audio en video
    final_video = video.set_audio(new_audio)
    final_video.write_videofile(output_path)
