# RAPIDITO [Tiempo-Reacción]

Diseño de proyecto – Electiva (Mecatrónica)

RAPIDITO es un proyecto orientado a la enseñanza práctica de microcontroladores. El sistema genera estímulos **visuales (LED)** y **auditivos (buzzer)**, y mide con alta precisión el **tiempo de reacción** del usuario desde que se emite el estímulo hasta que presiona el botón de respuesta. La medición, en milisegundos o microsegundos, se envía por conexión inalámbrica a una **aplicación móvil** que la muestra y la analiza.

## Cómo funciona

1. El usuario elige en la app el tipo de estímulo (LED, buzzer o ambos).
2. El ESP32 espera un intervalo aleatorio y activa el estímulo. Al mismo tiempo inicia un **timer de hardware**.
3. Al presionar el botón, una **interrupción (ISR)** detiene el conteo de inmediato.
4. El ESP32 envía el tiempo medido a la app, que lo muestra y lo compara con rangos de referencia.

## Componentes

| Parte | Descripción |
|---|---|
| Microcontrolador | ESP32 (comunicación inalámbrica con la app) |
| Estímulo visual | LED ultrabrillante |
| Estímulo sonoro | Buzzer |
| Entrada | Pulsador con filtro antirrebote |
| App móvil | Configuración de la prueba, resultados y gráfico |

## Estructura del repositorio

```
├── doc/             Documentación (Especificación de requisitos IEEE-830)
├── hardware/kicad/  Esquemático y diseño del circuito (KiCad)
├── mecanica/        Diseño mecánico (boceto de la carcasa)
├── LICENSE          Licencia MIT
└── README.md
```

## Documentación

La especificación de requisitos de software y hardware, basada en el estándar **IEEE Std 830-1998**, está en la carpeta [`doc/`](doc/).

## Equipo

| Integrante | Rol |
|---|---|
| Juan Eduardo Vasquez Pilier | Fundador / representante del equipo |
| Dioni Markin Hernandez | Desarrollador de firmware y analista de cálculo |
| Josué Rafael Hiraldo Fajardo | Desarrollador de la app y encargado del repositorio |
| Rafael Ovalles | Ingeniero de electrónica |
| Luismel Pinales Santana | Diseñador gráfico y de interfaz (UI/UX) |

## Obtener el proyecto

```bash
git clone https://github.com/josuerafaelhiraldo-pixel/RAPIDITO-Tiempo-Reaccion.git
cd RAPIDITO-Tiempo-Reaccion
```

## Audiencia

- **Docente:** validación del cumplimiento funcional y educativo.
- **Estudiantes / usuarios finales:** comprender la interacción con el sistema.

## Licencia

Distribuido bajo licencia MIT. Ver el archivo [LICENSE](LICENSE).
