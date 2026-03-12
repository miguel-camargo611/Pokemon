# Ideas de Proyecto: Ecosistema Pokémon 🎮

Para tu proyecto de Bases de Datos, usar Pokémon permite crear escenarios muy ricos que cumplen con todos los puntos de la rúbrica. Aquí tienes algunas ideas de "Industria o Caso" basadas en los datos descargados:

## 1. Centro de Investigación y Salud Pokémon (Pokémon Healthcare)
**Contexto**: Una red de Centros Pokémon que gestiona la salud y el historial médico de los Pokémon capturados.
- **Relacional (SQL)**: Tablas para `Pacientes` (Pokémon), `Médicos` (Enfermera Joy), `Tratamientos` y `Estadísticas de Salud`.
- **NoSQL**: Documentos JSON con el `Historial Genético` de cada Pokémon (esquema flexible para diferentes genes/IVs).
- **Problema**: Riesgo de datos duplicados o lentitud en emergencias cuando un Pokémon herido llega a recepción.

## 2. Plataforma Competitiva de Combates (E-Sports Analytics)
**Contexto**: Una liga oficial de torneos donde se analizan las estadísticas para balancear el juego.
- **Relacional (SQL)**: Tablas de `Torneos`, `Jugadores`, `Equipos` y `Resultados de Partidas`.
- **NoSQL**: Logs de batallas en tiempo real (JSON) que guardan cada movimiento realizado paso a paso.
- **Mejora**: Un sistema que prediga qué movimientos son más efectivos basándose en datos históricos.

## 3. Mercado Global de Criadores (Breeding Market & Logistics)
**Contexto**: Una empresa dedicada a la crianza selectiva y distribución de Pokémon a entrenadores de todo el mundo.
- **Relacional (SQL)**: Gestión de `Inventario`, `Genealogía` (padres/hijos), y `Logística de Envío`.
- **NoSQL**: Catálogo dinámico con fotos y descripciones de Pokémon "raros" o "Variocolor" (Shiny).
- **Problema**: Falta de trazabilidad en la cadena de frío para el transporte de huevos Pokémon.

---

## Sugerencias Técnicas para la Rúbrica:

### SQL (Mejora y Optimización)
- **Procedimiento**: `sp_CalcularDañoBase(pokemon_id, movimiento_id)` -> Devuelve el daño potencial.
- **Función**: `fn_EsEfectivo(tipo_ataca, tipo_defiende)` -> Retorna el multiplicador (0x, 0.5x, 1x, 2x).
- **Vista**: `vw_TopAmenazas` -> Clasifica Pokémon por la suma total de sus estadísticas base (BST).

### NoSQL (Integración)
- Podrían usar archivos JSON para guardar las "Estrategias Sugeridas" o "Comentarios de Usuarios" sobre cada Pokémon, ya que el texto y las etiquetas cambian mucho.

### Nube (Arquitectura)
- **Supabase (PostgreSQL)** para los datos relacionales.
- **MongoDB Atlas** para los documentos JSON.
- **AWS S3 / Azure Blob** para guardar las imágenes de los Pokémon.

### Legal y Ética
- **Protección de Datos**: Los nombres de los entrenadores son datos personales (PII).
- **Ética**: ¿Es ético usar algoritmos para decidir qué Pokémon "liberar" basándose solo en sus estadísticas bajas? (Sesgo algorítmico).
