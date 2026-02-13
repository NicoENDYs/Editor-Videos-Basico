---
name: video-processing-workflow
description: Flujo de trabajo completo para procesar y exportar videos. Úsalo cuando se pregunte sobre pipeline de procesamiento.
---

# Pipeline de Procesamiento de Video

## Paso 1: Validación de entrada
```python
def validate_video(filepath):
    from moviepy.editor import VideoFileClip
    try:
        clip = VideoFileClip(filepath)
        info = {
            'duration': clip.duration,
            'fps': clip.fps,
            'size': clip.size
        }
        clip.close()
        return True, info
    except Exception as e:
        return False, str(e)
