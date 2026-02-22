# Plan Estratégico para Presentación: Despliegue en el Sector Farmacéutico

Este documento es el roadmap detallado para la generación del archivo `presentacion.html`. Está diseñado para que el próximo modelo técnico pueda ejecutar la creación íntegra del código basado en estas directrices.

## 1. Especificaciones Técnicas del Proyecto
*   **Formato de entrega:** Un único archivo `presentacion.html` (HTML Semántico, CSS y JS embebidos). No habrá dependencias externas locales (se permiten CDNs para fuentes o iconos).
*   **Estética y Diseño Web:**
    *   **Estilo Premium:** Interfaz de alto impacto orientada a captar y mantener la atención durante 30 minutos.
    *   **Colores y Tipografía:** Tema oscuro elegante (Dark Mode) con contrastes neón suaves (azules hospitalarios, verde esmeralda para éxito, rojo coral para alertas). Tipografía de Google Fonts (ej. *Inter* o *Outfit*) para dar un aspecto extremadamente limpio y moderno.
    *   **Efectos:** Uso de *Glassmorphism* (paneles translúcidos con desenfoque de fondo), animaciones CSS fluidas, transiciones suaves entre componentes, *hover effects* en todo elemento interactivo.
*   **Mecánica Base:** La web actuará como un "Slide Deck" (gestor de diapositivas) interactivo, pudiendo navegar con flechas del teclado o clics, pero con interactividad interna en cada vista (no serán imágenes estáticas, sino interfaces web operativas).

## 2. Organización del Tiempo y Oradores (6 Personas, 30 Minutos)
Cada miembro del equipo dispondrá de aproximadamente 5 minutos de tiempo de exposición.

*   **Persona 1 (Mins 0-5):** Introducción al Sector Farmacéutico y Contexto del Problema.
*   **Persona 2 (Mins 5-10):** La Solución (Aplicación Web Web para Gestión de Stock y Recetas).
*   **Persona 3 (Mins 10-15):** Arquitectura de Despliegue (Público no técnico, uso de analogías).
*   **Persona 4 (Mins 15-20):** La Importancia, Impacto Crítico (Salud) y Conceptos Clave DAW.
*   **Persona 5 (Mins 20-25):** Mini-Demo (Simulación visual e interactiva del sistema fallando y recuperándose).
*   **Persona 6 (Mins 25-30):** Dinámica Interactiva (Juego-Quiz en pantalla) y Ronda Q&A Final.

---

## 3. Estructura Exacta del Documento HTML (Detalle por "Slides")

El próximo LLM desarrollador del código deberá crear contenedores (ej: `<section class="slide" id="slide-X">`) para estructurar este contenido.

### Diapositiva 1: Portada (Persona 1)
*   **Visual:** Fondo con micro-animaciones (CSS particles o un gradiente animado lento). Título enorme: "Impacto del Despliegue en Sector Farmacéutico". Subtítulo: Tecnología que salva vidas.
*   **Interactivo:** Botón vibrante de "Iniciar Operación" que transiciona a la siguiente vista.

### Diapositiva 2: El Contexto y el Riesgo (Persona 1)
*   **Visual:** Tres paneles (Tarjetas interactivas 3D con *tilt effect*) representando: Control de Stock, Receta Electrónica y Datos de Paciente.
*   **Interactivo:** Al pasar el ratón (*hover*), cada tarjeta revela los datos sensibles y por qué requieren altísima disponibilidad.

### Diapositiva 3: La Aplicación Propuesta (Persona 2)
*   **Visual:** Un "Mockup" (Maqueta simulada en HTML/CSS) de la interfaz que usaría un farmacéutico. Panel de dispensación y validación.
*   **Interactivo:** Botones clicables simulando la validación ficticia de una receta, mostrando un indicador de "Conexión a Servidor Central...".

### Diapositiva 4: Arquitectura para Todos (Persona 3)
*   **Metodología:** Explicar conceptos complejos para público no ofimático.
*   **Visual:** Diagrama construido con divs y CSS (no imagen externa).
*   **Interactivo:**
    *   Clic en **Servidor Linux**: Se expande un tooltip explicando que "es el edificio blindado de la farmacia".
    *   Clic en **Nginx Proxy**: "El recepcionista de seguridad que distribuye las colas de las cajas".
    *   Clic en **Docker**: "Armarios estancos: si un medicamento explota, no afecta al resto".
    *   Clic en **HTTPS y Variables de Entorno**: "Cajas fuertes y pasillos cifrados".

### Diapositiva 5: Riesgo Real e Importancia (Persona 4)
*   **Visual:** Modo "Alerta" (luces rojas parpadeantes suaves CSS). Un gran titular: "¿Qué ocurre cuando la pantalla dice ERROR 500?".
*   **Texto Principal:** Si el despliegue falla, la señora María no tiene su tratamiento de insulina crónico. El despliegue no es "subir ficheros", es garantizar el servicio público de salud.
*   **Grid Explicativo:** Paneles pequeños para Alta Disponibilidad, Backups (copias de seguridad) y Entornos de Prueba vs Producción.

### Diapositiva 6: Mini-Demo de Resiliencia (Persona 5)
*   **Visual:** Un esquema con un Nube (Usuarios), un Proxy (Nginx) y 3 Contenedores Docker (Servicios).
*   **Mecánica Interactiva:** Habrá un botón rojo de "Derribar Servidor Principal" (Simulando un fallo).
    *   Al clicarlo, una animación CSS destruye contenedor 1.
    *   JavaScript captura el evento y lanza inmediatamente la simulación de Alta Disponibilidad / Balanceo de carga desviando el tráfico al Contenedor 2, manteniendo todo azul (estable). ¡Efecto "WoW" visual!

### Diapositiva 7: Dinámica Interactiva y Cierre (Persona 6)
*   **Mecánica Principal (Juego Integrado):** Interfaz tipo "Kahoot" rápido integrado en la web.
*   **Contenidos (3 Preguntas rápidas al público):**
    1.  *¿Qué herramienta de despliegue aísla los programas como si fueran cajas separadas?* (A: Nginx / B: Docker / C: Linux).
    2.  *En nuestra analogía, ¿qué elemento actúa como el "recepcionista o guardia de seguridad"?* (A: Nginx / B: El técnico / C: Variables de Entorno).
    3.  *El verdadero objetivo de un buen despliegue es...* (A: Ejecutar código / B: Evitar que el ciudadano se quede sin medicamentos / C: Usar HTTPS).
*   **Feedback Inmediato:** Al hacer clic en respuestas correctas, animaciones sonoras o destellos visuales (CSS Confetti/Marcas verdes). Respuestas incorrectas hacen *shake* (temblor rojo).
*   **Cierre final:** Panel elegante "Q&A" / ¿Preguntas? / Gracias por la atención.

---

## 4. Directrices para el Próximo Modelo (LLM/Agente Desarrollador)

Cuando leas este plan y procedas a generar el archivo `presentacion.html`, *CUMPLE LOS SIGUIENTES REQUISITOS ESTRICTAMENTE:*
1.  **NO usar dependencias de NPM o configuraciones complejas.** Solo HTML crudo, un inmenso bloque `<style>` con Vanilla CSS y un bloque `<script>` para la lógica.
2.  **Calidad Estética Crítica:** Usa degradados oscuros de fondo (`linear-gradient(135deg, #0f2027, #203a43, #2c5364)`), sombras profundas, bordes redondeados (`border-radius`), fuentes hermosas (importar de Google Fonts como `Inter` o `Poppins`). Que no parezca genérico, debe arrancar aplausos.
3.  **Javascript Modular:** Usa Vanilla JS. Implementa una clase o controlador simple para el estado de las diapositivas (`let currentSlide = 0;`), escucha al `keydown` de las flechas derecha/izquierda y clics de botones para añadir/quitar clases CSS de visualización (`.active`, `.hidden`, etc.).
4.  **Inclusión de Datos:** Escribe los textos proporcionados en esta planificación exactamente como se sugieren, adaptando las descripciones. No dejes "Lorem ipsum" en ninguna parte de la presentación final.
5.  **Interactividad:** Obligatoriamente la Diapositiva 4 (diagrama clickeable), la Diapositiva 6 (botón de fallo de servidor) y Diapositiva 7 (trivia) deben funcionar con JavaScript, sin errores en consola.
