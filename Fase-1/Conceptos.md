# Conceptos Clave

## Esquema (Schema)
El esquema define la estructura y el formato de los datos que se pasan al LLM. En esencia, son los "tipos de mensajes" que se utilizan para comunicarte con el modelo, cada uno con un propósito específico:

- **text**: Es la forma más simple. Simplemente pasa una cadena de texto sin una clasificación especial, como un mensaje genérico.
- **system**: Se utiliza para dar instrucciones generales o configurar el comportamiento del LLM.
- **human**: Representa la entrada del usuario, el mensaje o la pregunta que el humano le hace al modelo.
- **ai**: Captura la respuesta del LLM, es decir, el resultado del procesamiento de la entrada humana.
- **document**: Sirve para estructurar y pasar grandes bloques de texto o información externa que el modelo debe utilizar como contexto.

# Modelos
LangChain soporta diferentes tipos de modelos, cada uno optimizado para distintas tareas:

- **Modelo de Lenguaje (Language Model)**: Acepta una cadena de texto como entrada y devuelve otra cadena de texto. Útil para tareas básicas como generación de texto o resumen.
- **Modelo de Chat (Chat Model)**: Diseñados para conversaciones, entienden el "contexto" de la conversación usando un historial de mensajes.
- **Modelos de Llamada a Funciones (Function Calling Models)**: Reconocen cuándo una solicitud implica ejecutar una acción externa.
- **Modelo de Incrustación de Texto (Text Embedding Model)**: Convierte texto en vectores numéricos que capturan el significado semántico.

# Prompts

- **Prompt**: La instrucción que le das al LLM. Debe ser claro, específico y dar el contexto necesario.
- **Plantilla de Prompt (Prompt Template)**: Estructura dinámica que permite reutilizar el mismo formato de instrucción con variables.

# Flujos de Trabajo vs Agentes

## Flujos de Trabajo (Workflows)
Sistemas predecibles y controlados donde el camino de la información está predeterminado. El desarrollador define todos los pasos de antemano.

## Agentes (Agents)
Sistemas autónomos y dinámicos donde el agente decide por sí mismo qué hacer a continuación. El LLM actúa como un "cerebro" que toma decisiones en tiempo real.

**Consejo**: Prefiere flujos de trabajo determinísticos cuando sea posible. Introduce agentes solo para tareas complejas.

# Técnicas Clave

- **RAG (Recuperación Aumentada de Generación)**: Recupera información relevante de bases de datos externas y la usa para aumentar el prompt del LLM.
- **Encadenamiento de Prompts (Prompt Chaining)**: Divide tareas complejas en pasos más pequeños y manejables.
- **Enrutamiento (Routing)**: Dirige la pregunta del usuario al sub-agente o flujo de trabajo correcto.
- **Paralelización (Parallelization)**: Ejecuta múltiples tareas simultáneamente.
- **Orquestador (Orchestrator)**: LLM de "alto nivel" que coordina a otros LLMs especializados.
- **Evaluador-Optimizador (Evaluator-Optimizer)**: Sistema de retroalimentación que revisa y mejora las respuestas del LLM.
