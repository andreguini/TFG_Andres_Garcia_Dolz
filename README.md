# TFG_Andres_Garcia_Dolz
Este repositorio contiene el código desarrollado para mi Trabajo de Fin de Grado (TFG), centrado en la modelización de leyes físicas mediante análisis dimensional y aprendizaje automático.

## Resumen de la metodología

1. **Análisis dimensional**: a partir de la matriz dimensional de las variables del problema, se obtienen mediante el teorema de Buckingham el prefactor dimensional y los invariantes adimensionales.
2. **Diccionario de funciones**: se construye una expansión de Fourier truncada sobre los invariantes adimensionales para aproximar la función Φ.
3. **Ajuste**: los coeficientes de la expansión se ajustan mediante regresión Ridge con validación cruzada, usando una partición del 80 % para entrenamiento y 20 % para test.
4. **Evaluación**: se calculan el coeficiente de determinación (R²) y el error cuadrático medio (RMSE) sobre el conjunto de test, y se compara la función aprendida con la ley física teórica conocida.

## Resultados principales

- **Péndulo simple**: el modelo recupera Φ(θ) ≈ 2π con R² = 0.9996 y RMSE = 0.0084 s.
- **Radiación de cuerpo negro**: el modelo reproduce la función de Planck con R² = 0.9796 globalmente, y R² = 0.9992 en la región donde la señal domina sobre el ruido (0.2 < π₁ < 1.75).

En ambos casos, el espectro de los coeficientes de Fourier ajustados muestra un decaimiento con el orden de la expansión, lo que indica que el modelo captura la estructura principal de la función adimensional sin ajustar de forma excesiva el ruido presente en los datos.

## Autor

Andrés García Dolz — Grado en Física, Universidad Europea de Valencia
Dirigido por: Dr. Héctor Gisbert Mullor
Curso académico 2025–2026
