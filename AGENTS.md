# Instrucciones para la adaptación de la presentación de Despliegue DAW (presentacion.html)

## 🎯 Objetivo Principal
Modificar el contenido textual, la estructura de las diapositivas y el flujo interactivo (JavaScript) del archivo `presentacion.html`. El objetivo es alinear la presentación con una nueva estructura narrativa de 4 bloques, diseñada para estudiantes de farmacia, demostrando la criticidad del Despliegue de Aplicaciones Web (DAW) en su sector.

## 🎭 Tono y Estilo
* **Narrativa:** "Golpe de realidad" respetuoso pero contundente. El objetivo NO es decir literalmente "los informáticos somos mejores", sino transmitir la idea de: *"Vuestra labor salva vidas y es vital, pero sin nuestra infraestructura informática detrás (Despliegue), volvéis a la Edad Media y la farmacia se paraliza"*.
* **Estilo Visual:** Mantener el tema oscuro, los colores neón (azul, verde, rojo) y las animaciones CSS existentes. Solo se debe modificar el contenido (HTML) y la lógica de la demo (JS).

## 📋 Tareas de Modificación por Secciones

### BLOQUE 1: El Choque de Realidades (Diapositivas Iniciales)
* **Modificar Slide 1 & 2:** Cambiar los textos para reflejar la premisa inicial. Reconocer la importancia del farmacéutico (salvan vidas).
* **Introducir un nuevo concepto:** Añadir una diapositiva o modificar una existente para explicar las bases de la informática crítica mediante el **Triángulo de la Seguridad**: Disponibilidad (Alta disponibilidad), Confidencialidad (Datos sensibles) e Integridad (Recetas exactas).

### BLOQUE 2: Las Herramientas del Día a Día (Contexto del Software)
* **Modificar Slide de "El Sector Farmacéutico":** Eliminar las referencias genéricas y añadir explícitamente que los farmacéuticos trabajarán con aplicaciones reales del sector: **Farmatic, Famanager, Nixfarma y Unycop Win**.
* **Explicar el "Under the hood":** Mostrar que estas aplicaciones no son simples interfaces bonitas, sino ecosistemas complejos conectados en tiempo real con:
    * Servidores del Gobierno/Ministerio (Receta electrónica).
    * Bases de datos de almacén y mayoristas (Stock).
    * Bases de datos con usuarios y medicamentos sensibles.

### BLOQUE 3: El Desastre y la Salvación (Demo Interactiva y Resiliencia)
* **Modificar el flujo del Mockup UI (Slide 5) y JS:** * Cambiar la lógica del botón `simulateValidationBtn` en JavaScript.
    * **Fase A (Fallo Estrepitoso):** La primera vez que se use la aplicación interactiva, debe fallar mostrando visualmente un **Error 404** o **Error 500** (pantalla roja, alertas). Explicar que "todo está mal" y el impacto real (el paciente no se lleva la medicación).
    * **Fase B (Explicación técnica):** Introducir el concepto de **Resiliencia** y cómo los contenedores (Docker) y el despliegue evitan que este fallo sea definitivo.

### BLOQUE 4: La Resurrección y Cierre (Resolución y Preguntas)
* **Resolución de la Demo:**
    * **Fase C (Arreglo):** Tras explicar la resiliencia, añadir un botón para "Aplicar Arquitectura DAW" (o similar). Al volver a utilizar la aplicación ficticia, esta vez el tráfico se deriva correctamente y funciona.
* **Modificar la sección de Quiz (Diapositivas finales):** Reemplazar las preguntas actuales por las siguientes (adaptando los botones de opciones correctas/incorrectas en el HTML):
    * *Pregunta 1:* ¿Cuál es el concepto que define la capacidad del sistema de resistir y recuperarse ante un fallo inminente? (Opciones: Balanceo de carga / Resiliencia (Correcta) / Cifrado de datos).
    * *Pregunta 2:* ¿Es importante mantener los datos de los clientes privados y cómo lo