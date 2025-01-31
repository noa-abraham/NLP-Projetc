# NLP-Projetc
Un emocionante proceso de transformación profesional hacia la Ciencia de Datos y Procesamiento del Lenguaje Natural (NLP), un campo que une mi pasión por las palabras con la potencia de la tecnología.

## *Introducción y Fundamentos de NLP*

    00:00 - Introducción
    06:12 - Todo sobre los Vectores
    12:25 - Bolsa de Palabras (Bag of Words)
    17:41 - Método de Conteo
    23:40 - Tokenización
    34:58 - Stop words o Palabras de Parada
    42:52 - Stemming y Lemmatization

00:00 - Introducción

    Propósito del tutorial: Introducir el procesamiento de lenguaje natural (PLN) desde conceptos básicos hasta herramientas prácticas.
    ¿Qué es NLP?:
        Campo que combina lingüística y computación para analizar, entender y generar texto.
        Aplicaciones comunes: análisis de sentimiento, clasificación de textos, chatbots, traducción automática, etc.

06:12 - Todo sobre los Vectores

    Representación numérica del texto: Los modelos de Machine Learning y Deep Learning no procesan texto directamente, necesitan convertir palabras o frases en números.
    Tipos básicos de representaciones vectoriales:
        One-hot encoding: Representa palabras como vectores binarios donde cada palabra ocupa una posición única. Ejemplo:

        ["gato", "perro", "ratón"] → [1, 0, 0], [0, 1, 0], [0, 0, 1]

            Problemas: Alta dimensionalidad, poca información sobre relaciones semánticas entre palabras.
        Contar frecuencias: Representar palabras según cuántas veces aparecen en un documento.

12:25 - Bolsa de Palabras (Bag of Words)

    Definición: Modelo que representa un texto como un conjunto de palabras (ignorando el orden) y cuenta su frecuencia.
    Ventajas: Simple y efectivo para tareas básicas como clasificación de textos.
    Limitaciones:
        Ignora el contexto y la posición de las palabras.
        No considera relaciones entre palabras (por ejemplo, "no feliz" y "triste" serían tratados por separado).

17:41 - Método de Conteo

    Construcción de matrices de frecuencia:
        Cada fila representa un documento y cada columna una palabra única del vocabulario.
        Ejemplo:

        Documento 1: "Me gusta NLP"
        Documento 2: "No me gusta"
        Matriz:
            gusta   NLP   me   No
        D1    1      1    1    0
        D2    1      0    1    1

    TF (Frecuencia de término): Número de veces que una palabra aparece en un documento.
    IDF (Frecuencia inversa de documento): Da más peso a palabras menos comunes.

23:40 - Tokenización

    Definición: Proceso de dividir un texto en unidades más pequeñas, como palabras, oraciones o caracteres.
    Métodos comunes:
        Tokenización por palabras: Divide en palabras individuales.
        Tokenización por caracteres: Divide en letras individuales (útil en tareas como corrección ortográfica).
        Tokenización por oraciones: Divide el texto en frases completas.
    Herramientas populares:
        nltk.word_tokenize (NLTK)
        spacy para tokenización avanzada.

34:58 - Stop Words o Palabras de Parada

    Definición: Palabras comunes y de poca relevancia para el análisis, como "el", "y", "un", "de".
    Razón para eliminarlas: Reducir ruido y mejorar la eficiencia de los modelos.
    Herramientas para manejar stop words:
        nltk.corpus.stopwords para eliminar palabras de parada en múltiples idiomas.
        Crea listas personalizadas según el dominio del texto.

42:52 - Stemming y Lemmatization

    Stemming:
        Proceso de reducir palabras a su raíz (stem), eliminando prefijos y sufijos.
        Ejemplo:

    amando → am
    amar → am
    amado → am

    Herramientas comunes:
        PorterStemmer (nltk.stem).
        SnowballStemmer (para múltiples idiomas).

Lemmatization:

    Reduce palabras a su forma base o lemma, considerando su contexto gramatical.
    Ejemplo:

amando → amar
fue → ser

Ventajas: Más preciso que stemming, pero más lento.
Herramientas comunes:

    WordNetLemmatizer (NLTK).
    spaCy (incluye modelos preentrenados).
