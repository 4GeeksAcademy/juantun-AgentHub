# Especificaciones 

# Descripcion
- El AgentHub es un panel de control de administración de agentes de IA, donde aquí se presenta un dashboard en el que se visualiza la gestion de usuarios, gestion de agentes, skills de cada agente, contratacion de agentes, un log de errores para poder corregirlos luego 

# Especificación visual
- cuatro tarjetas de métricas en una cuadrícula responsive 2×2, cada una con un icono, una etiqueta y un valor hardcodeado; (2) las tarjetas usan colores de acento distintos por tipo de métrica e incluyen una sombra sutil; (3) debajo de las tarjetas, un div de ancho completo con borde discontinuo y una etiqueta centrada representa el gráfico de actividad semanal
- Un inventario de componentes: una lista de los componentes de UI reutilizables que aparecen en varias secciones (sidebar, tarjeta de métrica, dropdown de acciones, modal, badge, lista de skills colapsable, toggle de modo oscuro).

- una lista numerada de condiciones verificables que deben cumplirse para que el prototipo se considere completo — incluye al menos un criterio por comportamiento interactivo (dropdown, modal, colapsable, modo oscuro).

# Requisitos 
-  Usa HTML
- TailWind Via CDN
- Solo JS Vanilla

# Restricciones
- Sin frameworks
- Sin Backend
#
# Admin Panel
- De un vistazo, el administrador debe poder ver: ingresos totales generados (este mes), pérdida total por descuentos y cupones, número de agentes activos en todos los clientes, y número de agentes actualmente marcados como fallando. Cada uno de estos debe ser una tarjeta de métrica visible. Debajo de las tarjetas, incluye un área de marcador de posición para un gráfico de actividad semanal.
    ## Gestion de usuarios
    - Una tabla que lista todos los usuarios registrados (nombre, email, plan, estado). Cada fila debe tener un dropdown de acciones — un pequeño menú activado con un botón ⋮ — con al menos dos opciones: "Ver detalle" y "Eliminar". Al elegir "Ver detalle" se abre un modal overlay con el registro completo del usuario. El modal debe cerrarse mediante un botón y haciendo clic en el backdrop.

    ## Gestion de Agentes
    
    - Un listado de todos los agentes registrados en la plataforma, mostrando nombre del agente, propietario, estado actual (activo / inactivo / fallando) y una lista de skills colapsada. Las skills asociadas a cada agente están ocultas por defecto; hacer clic en un control expandible las revela con una transición suave. Cada agente también tiene un dropdown de acciones con las opciones "Configurar" — que abre un modal con el prompt de sistema del agente — y "Eliminar".

    ## Skills

    - Una sección dedicada al catálogo de skills disponibles  las capacidades que se pueden adjuntar a los agentes. Cada skill tiene un nombre, una descripción breve, y un indicador de cuántos agentes la tienen habilitada actualmente. Incluye una breve explicación dentro del panel sobre qué significa una "skill" en el contexto de AgentHub. Las skills también tienen un dropdown de acciones con "Ver detalle" y "Eliminar".

    ## Contrataciones de agentes
    - Una tabla que muestra todos los contratos de alquiler activos y pasados. 
    Cada fila debe mostrar el cliente, el agente alquilado, las skills contratadas, las fechas del contrato y el importe total pagado.
    - Cada fila tiene un dropdown de acciones. Al elegir "Ver detalle" se abre un modal con el desglose completo del contrato, incluyendo la lista desglosada de skills contratadas y sus precios individuales.
    ## Log de errores
    -  Un registro de errores de ejecución de los agentes — mostrando timestamp, nombre del agente, tipo de error y una descripción breve. Los errores deben categorizarse visualmente por tipo o gravedad usando badges con código de color. Cada entrada tiene un dropdown de acciones con "Ver detalle" (abre un modal con la traza completa del error) y "Marcar como resuelto".
