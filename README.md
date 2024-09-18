# Lección 1: Técnicas de análisis de textos

## Frecuencias de palabras en lenguaje y estadísticas de texto

El análisis de textos es una técnica que permite obtener información cuantitativa y cualitativa sobre un conjunto de palabras dentro de un corpus. En esta lección aprenderemos cómo se pueden extraer y analizar frecuencias de palabras, y cómo interpretar las estadísticas generadas por el análisis.

### Frecuencia de Palabras

La frecuencia de palabras es el número de veces que una palabra aparece en un texto o conjunto de textos. Este análisis nos permite observar las palabras más comunes, y a veces, identificar patrones importantes que pueden revelar información sobre el estilo o el tema del texto.

**Ejemplo**:
En un corpus de noticias deportivas, las palabras "equipo", "jugador" y "gol" pueden ser las más frecuentes, reflejando el tema central del texto.

### Pasos para realizar el análisis:
1. **Recopilación de texto**: Reúne el texto que deseas analizar. Puede ser un solo documento o varios.
2. **Preprocesamiento del texto**: 
   - Elimina caracteres especiales, números y puntuación.
   - Convierte todo el texto a minúsculas.
   - Elimina palabras vacías (palabras como "y", "el", "de" que no aportan mucho significado).
3. **Cálculo de frecuencias**: Utiliza herramientas como Python con la librería `nltk` o `collections.Counter` para contar las palabras.
4. **Análisis e interpretación**: Analiza las palabras más frecuentes y lo que podrían revelar sobre el texto.

### Ejemplo en Python
from collections import Counter
import re

# Texto de ejemplo
texto = "El jugador marcó un gol, y el equipo celebró. El partido fue emocionante."

# Preprocesamiento del texto
texto_procesado = re.sub(r'[^\w\s]', '', texto.lower())  # Eliminar puntuación y convertir a minúsculas
palabras = texto_procesado.split()

# Contar frecuencias de palabras
frecuencia_palabras = Counter(palabras)
print(frecuencia_palabras)
