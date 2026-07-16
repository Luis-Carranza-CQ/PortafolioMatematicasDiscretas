<p align="center">
  <img src="https://img.shields.io/badge/UNIDAD%203-SISTEMAS%20NO%20LINEALES-7928ca?style=for-the-badge&logo=gitbook&logoColor=white" alt="Banner Unidad 3" />
</p>

<p align="center">
  <a href="./CONTENIDOS.md">
    <img src="https://img.shields.io/badge/⬅️_Volver_a_Contenidos-1f2328?style=for-the-badge&logo=github&logoColor=white" alt="Regresar" />
  </a>
</p>

# 🌳 Estructuras de Datos No Lineales: Grafos y Árboles

> [!NOTE]
> ### 📖 Introducción Detallada
> El propósito de este módulo es consolidar y exponer el diseño de algoritmos eficientes capaces de resolver problemas complejos en el desarrollo de software.
> 
> Mientras que las estructuras lineales (arreglos, listas, pilas) limitan la representación de datos a una sola dimensión secuencial, las **estructuras no lineales** rompen este esquema para modelar relaciones multidimensionales y jerárquicas del mundo real. En este espacio abordamos los fundamentos teóricos, propiedades matemáticas, clasificaciones y aplicaciones de las dos estructuras de datos más icónicas de las Ciencias de la Computación: **Grafos** y **Árboles**.

---

## 🕸️ 1. Estructura y Tipología de Grafos

Un **grafo** es una estructura matemática abstracta diseñada para modelar relaciones de red bidimensionales entre múltiples elementos que interactúan entre sí.

> ### 🧮 Definición Formal
> $$G = (V, E)$$
> Donde:
> * **$V$** representa el conjunto de vértices o nodos.
> * **$E$** representa el conjunto de aristas o conexiones.

<p align="center">
  <img width="500" alt="Concepto de Grafo" src="https://github.com/user-attachments/assets/ac3927a8-958b-4b15-b31b-6b229791f6ec" />
</p>

### ⚙️ Componentes Fundamentales

| Componente | Símbolo | Definición y Comportamiento | Representación Visual |
| :--- | :---: | :--- | :---: |
| **Vértices (Nodos)** | $V$ | Conjunto no vacío de elementos que representan objetos, entidades o puntos de información dentro del sistema. | `( A )`, `( B )` |
| **Aristas (Conexiones)** | $E$ | Conjunto de líneas o uniones físicas/lógicas que establecen una relación de adyacencia entre los vértices. | `A ── B` |

---

### 📌 Clasificación y Propiedades de los Grafos

#### 1. Grafos Dirigidos (Dígrafos)
Representan sistemas de flujo donde las relaciones tienen un sentido único y asimétrico de origen a destino.

> [!TIP]
> **Propiedades Técnicas:**
> * **Representación formal:** La arista se define como un par ordenado $(u, v)$ donde el camino va estrictamente de $u$ hacia $v$.
> * **Comportamiento:** Unidireccional $(u \to v \neq v \to u)$.
> * **Casos de Uso:** Redes de transporte de sentido único, jerarquías de herencia, mapas de dependencias de software o transiciones de estados.

<p align="center">
  <img width="320" alt="Grafo Dirigido" src="https://github.com/user-attachments/assets/c1f92558-f627-4fdd-88b1-51d8cccbe4dd" />
</p>

#### 2. Grafos No Dirigidos
Modelan conexiones simétricas donde la relación es recíproca por naturaleza.

> [!TIP]
> **Propiedades Técnicas:**
> * **Representación formal:** La arista se define como un conjunto no ordenado $\{u, v\}$ lo que implica adyacencia mutua.
> * **Comportamiento:** Bidireccional. Si existe una conexión entre $u$ y $v$, se puede transitar en ambos sentidos libremente.
> * **Casos de Uso:** Redes sociales de amistad (conexión mutua), topologías de redes físicas (cables de red bidireccionales), o conexiones de transporte de doble sentido.

<p align="center">
  <img width="260" alt="Grafo No Dirigido" src="https://github.com/user-attachments/assets/d4026878-41bb-493e-a8ec-f8ebfa678111" />
</p>

#### 3. Grafos Ponderados (Valorados)
Cada arista posee un peso o etiqueta con un valor numérico asociado. Este valor cuantifica la "dificultad" o "costo" de transitar por esa conexión (como la distancia en kilómetros, el tiempo o el costo económico).

> [!IMPORTANT]
> ### 🧭 Algoritmos de Optimización de Rutas
> * **Algoritmo de Dijkstra:** Encuentra el camino más corto desde un nodo origen a todos los demás nodos en grafos con pesos no negativos.
> * **Algoritmos de Prim y Kruskal:** Determinan el Árbol de Expansión Mínima (MST), es decir, el conjunto de aristas que conecta todos los vértices con el menor peso total posible sin generar ciclos.
> * **Algoritmo de Floyd-Warshall:** Resuelve el problema de encontrar los caminos más cortos entre todos los pares de vértices del grafo de una sola vez.

---

## 🌲 2. Arquitectura de Árboles

Desde la teoría de grafos, un **árbol** es un **grafo conexo y acíclico**. Esto significa que existe un único camino simple para llegar de cualquier nodo a otro y que es imposible formar bucles cerrados o ciclos dentro de su estructura.

Desde la perspectiva del desarrollo de software, representa la organización **jerárquica** por excelencia.

<p align="center">
  <img width="220" alt="Componentes del Árbol" src="https://github.com/user-attachments/assets/88935394-54d2-4ce3-92de-031ca6cee993" />
</p>

### 🌿 Elementos Constituyentes de la Jerarquía
* 🌱 **Raíz (Root):** El nodo origen de jerarquía superior del cual descienden todos los demás nodos del árbol. No posee nodos padres.
* 🌿 **Nodos Internos (Padres/Hijos):** Elementos intermedios del árbol que actúan como bifurcación. Tienen un nodo padre y al menos un nodo hijo.
* 🍃 **Hojas (Leafs):** Nodos terminales o extremos del árbol que no tienen descendencia (cero hijos).

---

### 📌 Taxonomía y Tipos de Árboles

#### 1. Árboles Generales ($N$-arios)
Cada nodo del árbol tiene la libertad de ramificarse en un número ilimitado y variable de nodos hijos.
* **Usos Comunes:** Sistemas de archivos de sistemas operativos (directorios), organigramas empresariales estructurados y análisis de código HTML/XML (DOM).

#### 2. Árboles Binarios
Estructura restringida donde cada nodo puede tener como máximo **dos nodos hijos**, denominados tradicionalmente como subárbol izquierdo y subárbol derecho.
* **Usos Comunes:** Compresión de datos (Árbol de Huffman) y árboles de decisiones binarias.

#### 3. Árboles Binarios de Búsqueda (BST)
Es un árbol binario que implementa una estricta propiedad de ordenamiento para optimizar las consultas y búsquedas de elementos.

> ### ⚖️ Propiedad de Ordenamiento
> $$\text{Subárbol Izquierdo} < \text{Nodo Padre} < \text{Subárbol Derecho}$$

* **Ventaja:** Permite realizar búsquedas de elementos en tiempo logarítmico $O(\log n)$ en lugar del tiempo lineal $O(n)$ requerido en listas enlazadas tradicionales.

#### 4. Árboles AVL (Adelson-Velsky y Landis)
Son árboles binarios de búsqueda **auto-balanceados**. Un problema con los BST de tipo convencional es que pueden deformarse en una lista enlazada si los datos se insertan ordenados. El árbol AVL soluciona esto obligándose a mantener equilibrada la altura de sus subárboles.

> [!WARNING]
> ### ⚖️ Reglas de Autobalanceo (AVL)
> * **Factor de Equilibrio:** Para cada nodo del árbol, la diferencia de altura entre el subárbol izquierdo y el derecho nunca puede ser mayor que **1**.
> * **Rotaciones:** Si una inserción o eliminación rompe esta regla, el árbol ejecuta rotaciones automáticas (simples o dobles) para reestructurarse, asegurando siempre un rendimiento de búsqueda óptimo.

---

<p align="center">
  <a href="./CONTENIDOS.md">
    <img src="https://img.shields.io/badge/⬅️_Volver_a_Contenidos-1f2328?style=for-the-badge&logo=github&logoColor=white" alt="Regresar" />
  </a>
</p>

# 🎯 Objetivo del Portafolio

> [!NOTE]
> ### 💡 Enfoque del Proyecto
> El análisis, diseño e implementación de las estructuras de datos no lineales constituye un pilar fundamental en la formación de futuros profesionales de la ingeniería.
> 
> Los ejercicios y casos prácticos desarrollados en este portafolio tienen como finalidad demostrar la aplicación de los conceptos teóricos mediante la resolución de problemas reales, fortaleciendo la comprensión de algoritmos y promoviendo el diseño de sistemas de información eficientes y escalables.

---

# 📂 Actividades del Curso

En esta sección se encuentran organizadas las actividades desarrolladas durante el curso. Cada apartado contiene un enlace al repositorio correspondiente en Google Drive, donde se almacenan los archivos elaborados en grupo.

<br />

## 📘 Actividad Autónoma (AA) N.º 1
> [!TIP]
> ### 👥 Aprendizaje Cooperativo
> **Descripción:**  
> Actividad desarrollada de forma colaborativa como parte del aprendizaje autónomo.
> 
> <table width="100%">
>   <tr>
>     <td><b>Estado:</b> <code>ENTREGADO</code></td>
>     <td align="right">
>       <a href="https://drive.google.com/drive/folders/141aLS6RH6c24ANHnOIiZmLh7Z129pgoO?usp=sharing">
>         <img src="https://img.shields.io/badge/🔗_Acceder_a_la_actividad-Drive-34A853?style=for-the-badge&logo=googledrive&logoColor=white" alt="Drive AA1" />
>       </a>
>     </td>
>   </tr>
> </table>

---

## 👨‍🏫 Actividad en Contacto con el Docente (ACD) N.º 1
> [!IMPORTANT]
> ### 🏫 Mentoría Sincrónica
> **Descripción:**  
> Actividad desarrollada en conjunto bajo la orientación del docente.
> 
> <table width="100%">
>   <tr>
>     <td><b>Estado:</b> <code>ENTREGADO</code></td>
>     <td align="right">
>       <a href="https://drive.google.com/drive/folders/1WkWPefM13L0VUdmtz3_LdLer6mThym6C?usp=drive_link">
>         <img src="https://img.shields.io/badge/🔗_Acceder_a_la_actividad-Drive-34A853?style=for-the-badge&logo=googledrive&logoColor=white" alt="Drive ACD1" />
>       </a>
>     </td>
>   </tr>
> </table>

---

## 📘 Actividad Autónoma (AA) N.º 2
> [!TIP]
> ### 👥 Aprendizaje Cooperativo
> **Descripción:**  
> Actividad colaborativa correspondiente al segundo bloque de aprendizaje autónomo.
> 
> <table width="100%">
>   <tr>
>     <td><b>Estado:</b> <code>ENTREGADO</code></td>
>     <td align="right">
>       <a href="https://drive.google.com/drive/folders/1D6X6DXJbhCl9fTPWNPmDqGPP6csqv6NW?usp=sharing">
>         <img src="https://img.shields.io/badge/🔗_Acceder_a_la_actividad-Drive-34A853?style=for-the-badge&logo=googledrive&logoColor=white" alt="Drive AA2" />
>       </a>
>     </td>
>   </tr>
> </table>

---

## 👨‍🏫 Actividad en Contacto con el Docente (ACD) N.º 2
> [!IMPORTANT]
> ### 🏫 Mentoría Sincrónica
> **Descripción:**  
> Actividad desarrollada con el acompañamiento del docente durante el segundo bloque.
> 
> <table width="100%">
>   <tr>
>     <td><b>Estado:</b> <code>ENTREGADO</code></td>
>     <td align="right">
>       <a href="https://drive.google.com/drive/folders/1gPo8fWeAXHPXHzljmdlEmS_hvvhGpcSP?usp=sharing">
>         <img src="https://img.shields.io/badge/🔗_Acceder_a_la_actividad-Drive-34A853?style=for-the-badge&logo=googledrive&logoColor=white" alt="Drive ACD2" />
>       </a>
>     </td>
>   </tr>
> </table>

---

## 🧩 Aprendizaje Practico Experimental (APE) – Fases 1 a 5
> [!WARNING]
> ### 🚀 Aprendizaje Basado en Problemas (ABP)
> **Descripción:**  
> Compilación de todas las fases correspondientes al Aprendizaje Basado en Problemas (ABP), desarrolladas de manera grupal.
> 
> <table width="100%">
>   <tr>
>     <td><b>Estado:</b> <code>COMPLETADO</code></td>
>     <td align="right">
>       <a href="https://drive.google.com/drive/folders/1C9iO0sYRAyfCKzEn0cXHgVuM-QCLw1Iw?usp=sharing">
>         <img src="https://img.shields.io/badge/🔗_Acceder_a_las_actividades-Drive-34A853?style=for-the-badge&logo=googledrive&logoColor=white" alt="Drive APE" />
>       </a>
>     </td>
>   </tr>
> </table>

---

> [!NOTE]
> **Nota:** Todos los enlaces dirigen a carpetas de Google Drive donde se encuentran almacenados los documentos, informes y demás evidencias correspondientes a cada actividad académica.
