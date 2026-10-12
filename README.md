<div align="center">

# CRIBA

**Un agente de diagnóstico que examina cómo opera una organización y le muestra,
con números en rango, dónde se le escapa el dinero y cómo la IA podría ayudar.**

Y, con el mismo peso, dónde **no** conviene automatizar todavía.

[![Java](https://img.shields.io/badge/Java-25-orange?logo=openjdk)](https://openjdk.org/)
[![Spring Boot](https://img.shields.io/badge/Spring%20Boot-4.1-6DB33F?logo=spring)](https://spring.io/projects/spring-boot)
[![SQLite](https://img.shields.io/badge/SQLite-local-003B57?logo=sqlite)](https://www.sqlite.org/)
[![Estado](https://img.shields.io/badge/estado-en%20desarrollo-2B57E0)](#estado)
[![Licencia](https://img.shields.io/badge/licencia-propietaria-9C83F7)](#licencia)

<br>

<img src="docs/capturas/01-lobby-en-espera.png" width="900"
     alt="El Lobby de CRIBA: el agente en el centro, en espera, con el botón Iniciar examen">

<sub>Diseño de la pantalla principal (mockup). El programa está en construcción.</sub>

</div>

> **In English.** CRIBA is a desktop diagnostic agent for small and mid-sized
> organizations that are afraid of AI, don't know where to start, or are out of date.
> It examines how the organization actually operates (roles, processes, demand) and
> reports where money is leaking, always as a range with visible assumptions, never as a
> promise. For each finding it builds an **AI plan**: what AI (or a simple rule, or just
> better order) could do, at what level of autonomy, which role owns it and the step by
> step to implement it, plus the cases where automating now would be a mistake. It runs
> entirely on the client's computer: nothing leaves the machine. Built with Java 25 and
> Spring Boot 4. Currently in development.

---

## El problema

Muchas empresas saben que "tienen que hacer algo con IA", pero no saben **dónde**, ni
**cuánto vale**, ni **por dónde empezar**. Los diagnósticos serios son caros y lentos;
los gratuitos son genéricos. Y el error más común es empezar por la herramienta en
lugar de por el proceso: automatizar el desorden solo lo acelera.

## Qué hace CRIBA

| | |
|---|---|
| **1 · Examina** | Reconoce cómo está armada la organización: sus roles (nunca personas), sus procesos y su volumen |
| **2 · Cuantifica** | Estima cuánto puede estar costando cada hueco, **en rango** y con sus supuestos a la vista, para que cualquiera pueda revisarlos |
| **3 · Dice "no"** | Señala dónde **no** conviene automatizar todavía, con el mismo peso que los hallazgos |
| **4 · Propone un plan de IA** | Por cada hallazgo: qué podría hacer la IA, con qué nivel de autonomía, qué rol lo lleva y el paso a paso, de lo más simple a lo más automático |
| **5 · Acompaña** | Lleva el plan en marcha, paso a paso, hasta el re-examen que compara el antes y el después |

## Las pantallas

El corazón es **el agente**: un tamiz con dos lentes por ojos que espera, escucha,
examina y avisa. Su estado refleja siempre el estado real del examen.

<table>
<tr>
<td width="50%"><img src="docs/capturas/02-lobby-primer-arranque.png" alt="Primer arranque: el agente se presenta en tres pasos"></td>
<td width="50%"><img src="docs/capturas/03-lobby-examen-en-curso.png" alt="Examen en curso: los anillos muestran el avance real de cada fase"></td>
</tr>
<tr>
<td><sub><b>Primer arranque.</b> El agente se presenta y dice qué no hace: no vigila, no promete, no saca datos del equipo.</sub></td>
<td><sub><b>Examen en curso.</b> Cada anillo es un dato real: las fases del recorrido, los conteos y la procedencia de cada número.</sub></td>
</tr>
<tr>
<td><img src="docs/capturas/04-lobby-examen-listo-ejemplo.png" alt="Examen listo con datos de ejemplo"></td>
<td><img src="docs/capturas/05-lobby-acompanamiento.png" alt="Acompañamiento del plan en marcha"></td>
</tr>
<tr>
<td><sub><b>Examen listo</b> (datos de EJEMPLO). La cifra siempre en rango, y las contraindicaciones al lado de los hallazgos.</sub></td>
<td><sub><b>Acompañamiento.</b> El siguiente paso del plan y la agenda hasta el re-examen.</sub></td>
</tr>
</table>

<sub>Todas las capturas son del diseño aprobado; los datos son de un caso de ejemplo
inventado, nunca de un cliente.</sub>

## Principios

- **Nunca promete un resultado.** Estima en rango, con supuestos visibles y su nivel de confianza.
- **Cada número dice de dónde sale:** medido, declarado o valor de referencia con su fuente.
- **Reproducible:** el mismo expediente produce el mismo examen, siempre.
- **Local:** funciona en el computador del cliente, sin conexión; nada sale de la máquina.
- **Sin vigilancia:** no captura pantallas, no lee mensajes, no registra a nadie. Roles, no personas.
- **Neutral:** recomienda patrones, no marcas, y no vende herramientas.
- **La IA no calcula:** las cifras las produce un motor determinista; la IA es opcional y llega después.

## Stack

Java 25 · Spring Boot 4 · Thymeleaf + HTMX · SQLite (un archivo por expediente) ·
Flyway · ventana local de escritorio con servidor en `127.0.0.1` · instalador propio.

## Estado

En desarrollo. Diseño de la pantalla principal aprobado; construcción de las
fundaciones en curso. Se busca una primera versión para probar en organizaciones de
tres tipos: profesionales independientes, consultorios y empresas con muchos roles.

## Licencia

Software propietario. Este repositorio publica **solo** una presentación (texto e
imágenes); no contiene código fuente y su visibilidad no concede ningún derecho de uso.
Ver [LICENSE](LICENSE).

© 2026 Rubén Agudelo Alzate.
