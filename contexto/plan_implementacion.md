# Plan de Implementación: Reestructuración del Libro y Parte II

Plan para ejecutarlo en sesiones futuras. Cada fase termina en **un commit propio** (commits convencionales, sin atribución de IA). Las fases son ordenadas; dentro de cada fase, los capítulos pueden hacerse uno por sesión.

**Para iniciar una sesión, decir:**
> "Implementa la Fase N de `contexto/plan_implementacion.md`."

---

## Fase 0: Lectura Obligatoria (antes de cualquier fase)

1. `contexto/vision_general.md`, en especial las premisas 14 a 17 (realismo latinoamericano, revelación en lugar de regaño, el costo de vivir en la carne, el tiempo como patrimonio).
2. `contexto/estructura_libro.md`: el índice destino y qué cambia en cada capítulo.
3. `contexto/ideas_clave_usuario.md`, secciones 11 a 17: el contenido base de la Parte II.
4. `contexto/ejercicios_practicos.md` y `contexto/finanzas_congregacion.md`.
5. Un capítulo ya escrito (por ejemplo `05_derribando_mitos.md`) para imitar la voz del autor: segunda persona, frases cortas, un versículo RVR1960 escrito completo después de cada idea, negritas para la idea clave.

**Reglas que aplican a todas las fases:**
- **Las "Palabras del autor" de las secciones 18 a 21 se conservan casi literales** (solo con la ortografía corregida), integradas en el texto y seguidas de su aplicación concreta. No se reemplazan por resúmenes.
- **Citas en RVR1960, escritas textualmente.** Las citas de los archivos de contexto se escribieron de memoria: **verificar cada una** contra una fuente RVR1960 antes de pasarla a un capítulo. Las versiones NVI y TLA no se usan.
- **No inventar cifras nuevas** si el contexto ya las trae. Si se cambia una cifra de los ejercicios, se recalculan los que dependen de ella (la familia Martínez es un solo caso continuo).
- **Toda advertencia va seguida de gracia y de una estrategia.**
- **Ningún consejo exclusivo de países desarrollados** (ver `ideas_clave_usuario.md`, sección 16.6).
- **Cierre estándar de cada capítulo:**
  1. "Lo que Dios nos revela aquí" (de 3 a 5 ideas clave).
  2. Palabra de esperanza.
  3. "Un paso esta semana".
  4. "Para reflexionar" (máximo 5 preguntas).

---

## Fase 1: Reorganizar Archivos y Corregir Errores

**Renombrar con `git mv`** según el índice de `estructura_libro.md`:

| Actual | Nuevo |
| --- | --- |
| `02_introduccion.md` | `00_introduccion.md` |
| `01_punto_cero.md` | `01_punto_cero.md` |
| `03_mayordomia.md` | `02_mayordomia.md` |
| `04_conceptos_basicos.md` | `03_conceptos_basicos.md` |
| `05_derribando_mitos.md` | `04_derribando_mitos.md` |
| — | `05_carne_o_espiritu.md` (Fase 2) |
| `06_finanzas_vida_diaria.md` | `06_finanzas_vida_diaria.md` |
| — | `07_deudas_ahorro_inversion.md` (Fase 2) |
| — | `08_tiempo_calidad_vida.md` (Fase 2) |
| `07_emprendimiento.md` | `09_trabajo_emprendimiento.md` |
| — | `10_plan_de_accion.md` (Fase 3) |
| `08_finanzas_mision.md` | `11_finanzas_mision.md` |
| — | `12_finanzas_congregacion.md` (Fase 3) |
| `09_ser_testigos.md` | `13_ser_testigos.md` |
| `10_conclusion.md` | `14_conclusion.md` |

**Corregir:**
- [ ] El encabezado `# Capítulo N:` de cada archivo según la nueva numeración. La Introducción va sin número.
- [ ] Mayordomía: quitar "Jesús y la Economía: No al Voto de Pobreza" (está duplicado en el Mito #2) y dejar una frase de referencia.
- [ ] Mateo 25:29 (Ley del Aumento) y Lucas 16:10: dejar la explicación completa solo en `09_trabajo_emprendimiento.md`; en los demás capítulos, una referencia breve.
- [ ] `04_derribando_mitos.md`, cita de "Juan 12:6": hoy mezcla varios pasajes. Reemplazarla por el texto real de Juan 12:6 en RVR1960.
- [ ] `00_introduccion.md`: quitar las versiones NVI y TLA (dejar solo RVR1960), o justificarlas como excepción si el autor lo decide.
- [ ] `06_finanzas_vida_diaria.md`:
  - Cambiar el ejemplo de "$5 al día" por montos de $1 a $2.
  - En la tabla de fijos, quitar hipoteca y seguros y agregar bombona de gas, agua (cisterna o camión), plan del teléfono y cuotas de apps.
  - Mover "La Fidelidad en lo Cotidiano" al capítulo 9.
- [ ] `11_finanzas_mision.md`: mover "Alzar la Mirada: El Cierre de Todo" al final del capítulo.
- [ ] `14_conclusion.md`: armonizar el ahorro ("empieza con el 5% y sube hasta el 10%") con el capítulo 6.
- [ ] `README.md`: nueva tabla de contenido con las rutas renombradas; marcar los capítulos pendientes como "(en construcción)".
- [ ] `predicaciones/01_.../01_...md`: actualizar la línea "Fuente: Capítulos 1 a 6, 8 y 9" con la nueva numeración. **No regenerar el PDF.**

**Commit:** `refactor: reorganize chapters into three parts and fix duplicates`

---

## Fase 2: Escribir los Capítulos Nuevos de la Parte II (uno por sesión)

| Archivo | Fuente | Contenido mínimo |
| --- | --- | --- |
| `05_carne_o_espiritu.md` | Secciones 11 y 18 | El hombre natural vs. el espiritual; la infidelidad con la tabla de $400 (del 87% al 117%); el embarazo no planificado con la aclaración de que el hijo es bendición; el cuidado pastoral; un camino para quien ya vive las consecuencias; vicios ($1.200 al año), gasto por impulso, el vicio del entretenimiento y la pornografía |
| `07_deudas_ahorro_inversion.md` | Secciones 12, 13, 13.1, 14 y 19 | Definición de deuda; criterios de deuda buena y mala; 7 pasos para salir; ahorro en divisas y por etapas; vista anual (tabla de $20/$30/$50); escalera de inversión y alerta de estafas; retener más en lugar de ganar más; vivienda (precio contra ubicación); alquilar una habitación con contrato |
| `08_tiempo_calidad_vida.md` | Sección 15 | El agua (madrugada, bomba, flotantes), la ropa (lavar, secar, planchar, guardar), 312 horas al año, lo que se pospone, soluciones por costo, cómo decidir; enlazar con 18.3 (el tiempo robado por las pantallas) |

- Ampliar `09_trabajo_emprendimiento.md` con las secciones 16.3 (incluye "Aprender, Perfeccionar y Especializar un Oficio Técnico"), 16.4, 16.5 (comprar donde es barato y llevar donde hace falta) y 20 (resolver problemas ajenos: transporte, carga, cocina, enseñanza, cuidado, oficios, la actitud que vende). Cambiar su cierre para que termine en esperanza.

**Commits:** uno por capítulo, por ejemplo `feat: add chapter 5 'Carne o Espíritu'`.

---

## Fase 3: Plan de Acción y Congregación

- `10_plan_de_accion.md`:
  - Secciones 16.1 y 16.2.
  - **Los 11 ejercicios** de `ejercicios_practicos.md`, cada uno con situación, datos, solución, "Lo que esto revela" y versículo.
  - La sección 21 (los imprevistos), ubicada junto a los Ejercicios 6 a 10, con el directorio de contingencia y el simulacro trimestral.
  - Las 12 plantillas en blanco al final, como tablas Markdown vacías.
- `12_finanzas_congregacion.md`: todo `finanzas_congregacion.md`, con el presupuesto de $600 y sus provisiones.
- **Antes de escribir:** resolver el PENDIENTE sobre qué es "el cuerpo que lleva espiritualmente a la iglesia" (preguntar al autor).

**Commits:** `feat: add action plan chapter with worked exercises` y `feat: add congregation finances chapter`.

---

## Fase 4: Cierres Estándar en Todos los Capítulos

- [ ] Agregar o ajustar el cierre de 4 partes en cada capítulo.
- [ ] Reducir los "Para reflexionar" de 10 preguntas (Mitos, Vida Diaria, Ser Testigos) a un máximo de 5. Las preguntas que se quiten pueden pasar a un apéndice de "Preguntas para grupos".
- [ ] **Capítulos que hoy no tienen cierre:** Punto Cero, Mayordomía y Conceptos.
- [ ] `09_trabajo_emprendimiento.md` no debe terminar en una advertencia.
- [ ] `13_ser_testigos.md`: agregar un párrafo de gracia (el Rey **provee** la ropa de boda).

**Commit:** `feat: add standard closing sections to all chapters`

---

## Fase 5: Conclusión y Verificación Final

- [ ] `14_conclusion.md`: el resumen de principios debe cubrir los 13 capítulos; los "Pasos concretos" deben enlazar a las plantillas del capítulo 10.
- [ ] Verificar con grep que no quedan referencias a la numeración vieja ("Capítulo 7" que antes era Emprendimiento, etc.).
- [ ] Verificar que las cifras de la familia Martínez sean coherentes entre los capítulos 7, 8, 9 y 10.
- [ ] Verificar todas las citas nuevas contra RVR1960.
- [ ] Actualizar `estructura_libro.md`: quitar las marcas "NUEVO" y "Archivo actual" de lo que ya se implementó.

**Commit:** `docs: update conclusion and verify cross-references`

---

## Preguntas Abiertas para el Autor

1. `ideas_clave_usuario.md` tiene una frase incompleta: "Ser testigos de que Jesus es el Cristo... Porque nosotros somos". ¿Cómo termina?
2. ¿"El cuerpo que lleva espiritualmente a la iglesia" es el equipo ministerial local, una organización o cobertura externa, o ambos?
3. ¿Se divide "Ser Testigos" (aprox. 10.000 palabras) en dos capítulos o se mueve parte a un apéndice?
4. ¿El capítulo 10 (Plan de Acción) va como capítulo o como apéndice al final del libro?
5. ¿Se mantienen las versiones NVI y TLA de la Introducción como excepción?
