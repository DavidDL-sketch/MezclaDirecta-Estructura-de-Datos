# Práctica: Ordenamiento Externo - Mezcla Directa (Straight Merge)

Implementación en Java de la fase de intercalación de bloques del algoritmo de ordenamiento externo **Mezcla Directa**. El programa lee dos archivos auxiliares previamente ordenados por bloques de tamaño L (`f1.txt` y `f2.txt`), compara sus elementos uno a uno y genera un archivo de salida (`f3.txt`) con los datos fusionados y ordenados de forma ascendente.

---

## 🎓 Información Académica

* **Instituto:** Instituto Tecnológico Superior de Xalapa
* **Materia:** Estructura de Datos
* **Alumno:** David Domínguez López

---

## 📋 Requisitos Previos

* **Java Development Kit (JDK):** Versión 8 o superior.
* **IDE o Editor de Texto:** IntelliJ IDEA, NetBeans, Eclipse o Visual Studio Code.

---

## 📂 Estructura del Proyecto

Para una correcta ejecución, los archivos de texto de entrada deben ubicarse en la **carpeta raíz** del proyecto (al mismo nivel que la carpeta `src`):

```text
MiProyectoMezcla/
├── src/
│   └── MezclaDirectaPractica.java   # Código fuente principal
├── f1.txt                           # Archivo auxiliar 1 (entrada)
├── f2.txt                           # Archivo auxiliar 2 (entrada)
└── f3.txt                           # Archivo resultante (generado automáticamente)
```

---

## 🚀 Instrucciones de Ejecución

1. **Clonar o descargar el repositorio:**
   ```bash
   git clone https://github.com
   ```

2. **Preparar los archivos de entrada:**
   Crea los archivos `f1.txt` y `f2.txt` en la raíz del proyecto e inserta números enteros (uno por renglón). Ejemplo para una prueba con bloques de tamaño L = 1:

   * **`f1.txt`**:
     ```text
     45
     ```
   * **`f2.txt`**:
     ```text
     12
     ```

3. **Compilar y ejecutar:**
   Ejecuta el método `main` de la clase `MezclaDirectaPractica`. Si todo sale bien, la consola mostrará:
   ```text
   Bloque intercalado con exito!
   ```

4. **Verificar el resultado:**
   Abre el archivo generado **`f3.txt`** en la raíz del proyecto. El contenido debe estar ordenado:
   ```text
   12
   45
   ```

---

## ⚙️ Funcionamiento del Algoritmo (`intercalarBloques`)

El método recibe las rutas de los dos archivos de entrada, la ruta del archivo de salida y el tamaño de bloque $L$. La lógica se divide en tres casos principales dentro del ciclo de lectura:

* **Caso 1 (Comparación directa):** Mientras ambos bloques tengan elementos disponibles (`elementosEscritos1 < L && elementosEscritos2 < L`), se convierten las líneas a enteros (`Integer.parseInt`) y se escribe el valor menor en `f3.txt`, avanzando únicamente el puntero y contador del archivo correspondiente.
* **Caso 2 (Vaciado de F1):** Si el bloque de `f2.txt` alcanza el límite $L$ primero, se vuelcan directamente los elementos restantes del bloque de `f1.txt`.
* **Caso 3 (Vaciado de F2):** Si el bloque de `f1.txt` alcanza el límite $L$ primero, se vuelcan directamente los elementos restantes del bloque de `f2.txt`.

---

## ✒️ Autor

* **David Domínguez López** - *Desarrollo de la práctica de Estructura de Datos (ITSX)*
