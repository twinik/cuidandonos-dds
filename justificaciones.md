# Justificaciones de Diseño

## Patron Strategy

Decidimos utilizar el patrón de diseño Strategy para representar las diversas formas de responder a posibles incidentes. Esto se debe a que se requiere la capacidad de añadir nuevas formas de reaccionar antes estos en el futuro de manera sencilla. Esto proporciona una mayor cohesión a la clase ReaccionStrategy y además, permite cambiar de estretegia durante la ejecución.
