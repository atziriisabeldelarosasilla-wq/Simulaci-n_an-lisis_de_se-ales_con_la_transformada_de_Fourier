# Simulación y análisis de señales con la Transformada de Fourier

Script en Python que genera señales elementales en el dominio del tiempo, calcula su Transformada de Fourier con la FFT y verifica tres de sus propiedades fundamentales.

## Propósito

Este repositorio corresponde a la actividad **"Simulación y análisis de señales con la transformada de Fourier"**. El objetivo es analizar señales en el dominio del tiempo y de la frecuencia, aplicando la Transformada de Fourier (mediante la FFT) para visualizar y comparar ambas representaciones.

## Contenido

```
fourier_signals.py      # Script principal
figures/                # Gráficas generadas al ejecutar el script
    01_rect_tiempo.png
    02_step_tiempo.png
    03_sinusoid_tiempo.png
    04_rect_espectro.png
    05_step_espectro.png
    06_sinusoid_espectro.png
    07_propiedad_linealidad.png
    08_propiedad_desplazamiento_tiempo.png
    09_propiedad_escalamiento_frecuencia.png
```

## Señales analizadas

1. **Pulso rectangular**: amplitud 1 entre t = 0.05 s y t = 0.15 s.
2. **Función escalón unitario**: salta de 0 a 1 en t = 0.1 s.
3. **Función senoidal**: frecuencia de 5 Hz.

## Qué calcula el script

- Representación de cada señal en el dominio del tiempo (`matplotlib`).
- Transformada de Fourier de cada señal con `np.fft.fft()`.
- Magnitud y fase del espectro de frecuencia de cada señal.
- Verificación de tres propiedades de la Transformada de Fourier:
  - **Linealidad**: `F{a·x1(t) + b·x2(t)} = a·F{x1(t)} + b·F{x2(t)}`.
  - **Desplazamiento en el tiempo**: un retraso en el tiempo no cambia la magnitud del espectro, pero sí su fase.
  - **Escalamiento en frecuencia**: comprimir una señal en el tiempo expande su espectro en frecuencia (dualidad tiempo-frecuencia).

## Requisitos

- Python 3.8+
- `numpy`
- `scipy`
- `matplotlib`

Instalación rápida:

```bash
pip install numpy scipy matplotlib
```

## Cómo ejecutarlo

```bash
python fourier_signals.py
```

Al terminar, todas las gráficas quedan guardadas en la carpeta `figures/` y en la consola se imprime el error numérico de la verificación de linealidad (debe ser cercano a cero).

## Parámetros de muestreo

- Frecuencia de muestreo: `Fs = 1000 Hz`
- Número de muestras: `N = 2048`
- Resolución en frecuencia: `Fs / N ≈ 0.49 Hz`

## Autora

Atziri Isabel de la Rosa Silla — Universidad Ciudadana de Nuevo León
