# Paso 2: Selección de Tecnologías y Diseño de Arquitectura

## 2.1 Selección de Lenguaje y Bibliotecas
- Lenguaje principal: Python
- Bibliotecas de edición de video:
  - MoviePy (edición y manipulación de video)
  - OpenCV (procesamiento de video e imágenes)
  - (Opcional) PyDub o librosa para procesamiento de audio

## 2.2 Diseño de la Arquitectura Modular
- Estructura de carpetas sugerida:
  - src/
    - core/ (lógica de edición)
    - ui/ (interfaz de usuario)
    - utils/ (utilidades y helpers)
    - tests/ (pruebas unitarias)
- Separar claramente la lógica de edición, la interfaz y las utilidades

## 2.3 Definición de la Interfaz de Usuario (UI)
- Interfaz gráfica recomendada: Tkinter (incluida en Python, fácil de usar)
- Alternativas: PyQt5, Kivy (para futuras versiones o mayor personalización)
- Elementos básicos de la UI:
  - Cargar video
  - Seleccionar segmento para cortar/pegar
  - Agregar imagen en el timeline
  - Botón para reducción de ruido
  - Exportar video

## 2.4 Consideraciones de Compatibilidad y Dependencias
- Documentar las dependencias en requirements.txt
- Asegurar compatibilidad inicial con Windows
- Planificar estructura para facilitar portabilidad a otros sistemas operativos

---

Este documento define las tecnologías y la arquitectura base para el desarrollo, asegurando un enfoque modular y escalable.