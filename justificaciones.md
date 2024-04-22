# Justificaciones de Diseño

## Patron Strategy

Decidimos utilizar el patrón de diseño Strategy para representar las diversas formas de responder a posibles incidentes. Esto se debe a que, además de ofrecer una estructura organizada y cohesión a la clase ReaccionStrategy, nos permite adaptarnos fácilmente a futuros cambios en los requisitos. Al implementar este patrón, no solo obtenemos una solución robusta y flexible para el manejo de incidentes, sino que también facilitamos la incorporación de nuevas estrategias de reacción sin necesidad de modificar el código existente. Esto garantiza que podamos cambiar de estrategia durante la ejecución del programa sin afectar su funcionamiento general.
