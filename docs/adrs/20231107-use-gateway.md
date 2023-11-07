# ADR 1: Use API Gateway

# Context
Hay escenarios que consumen datos de microservicios diferentes y distribuidos.
Los microservicios necesitan encontrar los servicios adecuados con los que interactuar y contribuir a completar la funcionalidad en un plazo determinado y que cumpla con los SLA.

# Decision

Tener API Gateway como single point of contact para todo tipo de servicios con el fin de interactuar con servicios locales y remotos. 

# Consequences

## Pros
1. Disminuye la latencia cuando la funcionalidad requiere acceder a varios MS que se encuentran en la misma red local
2. Unico punto en donde se puede hacer enriquecimiento de mensajes, traducción de protocolos, agregar seguridad, etc. 
3. Abstrae detalles de implementación facilitando la evolución del sistema

## Cons
1. Aumenta la complejidad del sistema
2. Puede afectar el rendimiento al agregar un nodo a la infraestructura
