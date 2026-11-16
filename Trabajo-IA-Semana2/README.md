# Semana 2: Tres cupos, ocho estudiantes
 
Actividad hecha con IA, como lo pedía el entregable. Consiste en decidir quiénes de ocho estudiantes ficticios deberían recibir uno de los tres cupos de un programa de acompañamiento, y ver cómo cambia la respuesta de la IA según el contexto que se le da.
 
El registro completo de la actividad (datos, consultas, respuestas y observaciones) está en [`tres-cupos.txt`](tres-cupos.txt).
 
## El caso
 
Ocho estudiantes de un curso de programación (Ana, Bruno, Camila, Diego, Elena, Felipe, Gabriela y Hugo), con nota actual (0 a 5, se aprueba con 3), porcentaje de asistencia y una breve descripción de su situación.
 
## Mi elección individual (sin IA)
 
**Camila, Elena y Hugo.**
 
Criterio: quise dejar dentro a quienes necesitan el acompañamiento por tener una nota baja y cuya situación muestra que intentan aprender pero no terminan de entender. También que asistan siempre o casi siempre, porque un programa de apoyo no sirve si no se asiste, sea cual sea la circunstancia.
 
## Consulta 1: solo con los datos de la tabla
 
- **Instrucción:** seleccionar a los tres estudiantes que más necesitan el acompañamiento, justificar cada elección y explicar por qué se dejó fuera a los demás.
- **Respuesta de la IA:** Diego, Gabriela y Ana.
- **Criterios que usó:** necesidad académica, barreras de aprendizaje y beneficio esperado.
**Observaciones:**
- Se apoyó más en las notas que en la asistencia y la situación de cada estudiante.
- Supuso cosas que los datos no dicen. Por ejemplo, dijo que las ausencias de Bruno se deben al trabajo, cuando solo se dice que sus turnos coinciden con algunas clases. Puede haber otras causas.
- No pidió información adicional, aunque sí reconoció que habría que conversar con los ocho estudiantes.
## Consulta 2: con información del programa
 
Se agregó el contexto del **Programa B: Continuidad en el curso**: ocho semanas de acompañamiento para favorecer la continuidad y evitar el abandono, con tutorías semanales de horario flexible y seis horas adicionales de computador por semana. Los ocho estudiantes pueden asistir al menos a un horario. No incluye apoyo económico ni préstamo de computadores. El repaso para el examen está abierto a todos y es independiente de los cupos.
 
- **Respuesta de la IA:** Diego, Gabriela y Ana (los mismos).
- **Criterios que usó:** riesgo académico, barreras para continuar y utilidad del programa.
## Comparación
 
La selección no cambió. Con más contexto sí tuvo en cuenta más factores de la tabla (diría que todos) y cambió un poco sus criterios de decisión, pero llegó a los mismos tres estudiantes.
 
## Conclusión
 
Necesitábamos darle a la IA el objetivo del programa y un contexto más amplio: qué se hace en él, a quién va dirigido, cuántos horarios tiene, si exige asistencia, etc. Entre más contexto **relevante** se le dé (no conviene llenarla de información irrelevante), más fácil es que la respuesta se ajuste a lo que realmente necesitamos.
 
También ayuda decirle qué esperamos de salida. Por ejemplo: "escoge a los estudiantes que tengan más posibilidades de asistir y que más necesiten el apoyo por tener una nota baja". Con una petición así la respuesta podría ser totalmente distinta. Igual que una persona puede interpretar el ejercicio de otra manera según cómo lo lea.
