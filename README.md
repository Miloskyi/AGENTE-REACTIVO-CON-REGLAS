# 🏠 Agente Reactivo Simple: Hogar Inteligente

## 📌 Descripción
Este proyecto implementa un **agente reactivo simple** en Python para un entorno de hogar inteligente.  
El sistema utiliza sensores y reglas de producción del tipo **SI → ENTONCES** para tomar decisiones automáticas relacionadas con:

- Seguridad
- Emergencias
- Confort
- Ahorro energético

El agente analiza las percepciones del entorno y ejecuta acciones inmediatas sobre distintos actuadores del hogar.

---

# ⚙️ Características

## Sensores implementados
El sistema monitorea continuamente:

- 🌡️ Temperatura
- 💧 Humedad
- 🚶 Movimiento
- 💡 Nivel de luz
- 🔥 Detección de humo
- 🚪 Estado de la puerta

## Actuadores disponibles
El agente puede controlar:

- ❄️ Aire acondicionado
- 🔥 Calefacción
- 💡 Luces
- 🚨 Alarma
- 💦 Aspersores
- 🌬️ Ventilador
- 🔒 Cerradura

---

# 🧠 Arquitectura del Agente

El proyecto sigue el modelo clásico de un **Agente Reactivo Simple**, donde:

1. El agente recibe percepciones del entorno.
2. Actualiza el estado interno del hogar.
3. Evalúa reglas ordenadas por prioridad.
4. Ejecuta la primera regla válida.
5. Retorna la acción realizada.

## Pseudocódigo

```text
funcion agente_reactivo(percepcion):
    actualizar_estado(percepcion)

    para cada regla en reglas:
        si regla.condicion(estado):
            return regla.accion(estado)

    return "Sin acción"
