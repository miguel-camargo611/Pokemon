# Documentación de Datos Pokémon 🔎

Este repositorio contiene los datos base para el Proyecto Final Integrador de Bases de Datos. Los datos han sido extraídos de fuentes oficiales (PokéAPI) para cumplir con los requerimientos de modelado relacional y no relacional.

## Carpeta de Datos
Todos los archivos se encuentran en la carpeta [/data](./data).

### Archivos de Base de Datos Relacional (SQL)
Estos archivos CSV están listos para ser importados en un SGBD como SQL Server, PostgreSQL, MySQL o SQLite.

1.  **[pokemon.csv](./data/pokemon.csv)**: 
    - **Descripción**: Tabla maestra de Pokémon.
    - **Columnas**: `id`, `name`, `order`, `height`, `weight`, `base_experience`.
    - **Uso**: Entidad principal para el modelo ER.

2.  **[pokemon_stats.csv](./data/pokemon_stats.csv)**:
    - **Descripción**: Valores de las estadísticas base.
    - **Columnas**: `pokemon_id`, `stat_id`, `base_stat`, `effort`.
    - **Relación**: Llave foránea a `pokemon` (muchos a muchos con `stats`).

3.  **[stats.csv](./data/stats.csv)**:
    - **Descripción**: Catálogo de tipos de estadísticas.
    - **Columnas**: `id`, `damage_class_id`, `identifier`, `is_battle_only`, `game_index`.

4.  **[pokemon_types.csv](./data/pokemon_types.csv)**:
    - **Descripción**: Relación entre Pokémon y sus tipos.
    - **Columnas**: `pokemon_id`, `type_id`, `slot`.

5.  **[types.csv](./data/types.csv)**:
    - **Descripción**: Diccionario de tipos (Fuego, Agua, etc.).
    - **Columnas**: `id`, `identifier`, `generation_id`, `damage_class_id`.

### Archivos de Base de Datos NoSQL (Documental)
1.  **[pokemon_samples.json](./data/pokemon_samples.json)**:
    - **Descripción**: Ejemplo de estructura documental (JSON) para integrar con tecnologías NoSQL (MongoDB).
    - **Uso**: Ideal para el módulo NoSQL de la rúbrica, permitiendo almacenar datos anidados como habilidades y movimientos sin joins complejos.

---

## Instrucciones para el Equipo
- **Importación**: Pueden usar las herramientas de importación de su SGBD favorito para cargar los CSVs.
- **Modelo ER**: Se recomienda crear una tabla de `Generaciones` o `Habilidades` adicional si desean Normalizar a un nivel más alto (3NF).
- **Procesamiento**: Los datos están limpios, pero pueden requerir ajustes de tipos de datos (e.g., `height` y `weight` están en decímetros y hectogramos respectivamente).
