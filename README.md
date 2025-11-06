# AgendaCita

AgendaCita es una aplicación para la gestión de citas, diseñada para facilitar el registro, consulta y respaldo de citas en formato digital. El sistema utiliza archivos JSON y CSV para el almacenamiento y respaldo de datos.

## Tabla de Contenidos

- [Características](#características)
- [Tecnologías Utilizadas](#tecnologías-utilizadas)
- [Estructura del Proyecto](#estructura-del-proyecto)
- [Instalación](#instalación)
- [Uso](#uso)
- [Respaldo y Recuperación](#respaldo-y-recuperación)
- [Validaciones](#validaciones)
- [Contribuciones](#contribuciones)
- [Licencia](#licencia)

---

## Características

- Registro, consulta y gestión de citas.
- Almacenamiento de datos en formato JSON.
- Respaldo automático en formatos CSV y JSON.
- Validación de datos de entrada.
- Modularidad para facilitar la extensión y el mantenimiento.

## Tecnologías Utilizadas

- **Python 3.x**: Lenguaje principal de desarrollo.
- **Módulos estándar**: `json`, `csv`, `os`, entre otros.
- No requiere dependencias externas.

## Estructura del Proyecto

```
app.py                # Punto de entrada principal de la aplicación
domain.py             # Definición de entidades y lógica de dominio
services.py           # Lógica de negocio y servicios de la aplicación
storage.py            # Gestión de almacenamiento y persistencia de datos
validators.py         # Validaciones de datos de entrada
backups/              # Carpeta de respaldos automáticos (CSV y JSON)
    2025-11-05-23-22-all.csv
    2025-11-05-23-22-all.json
data/                 # Carpeta de datos principales
    appointments.json
README.md             # Documentación del proyecto
```

## Instalación

1. **Clona el repositorio:**
   ```sh
   git clone <URL_DEL_REPOSITORIO>
   cd AgendaCita
   ```

2. **(Opcional) Crea un entorno virtual:**
   ```sh
   python -m venv venv
   source venv/bin/activate  # En Windows: venv\Scripts\activate
   ```

3. **No requiere instalación de dependencias externas.**

## Uso

1. **Ejecuta la aplicación:**
   ```sh
   python app.py
   ```

2. **Sigue las instrucciones en pantalla para:**
   - Registrar nuevas citas.
   - Consultar citas existentes.
   - Realizar respaldos manuales (si está implementado).
   - Restaurar datos desde un respaldo (si está implementado).

## Respaldo y Recuperación

- Los respaldos automáticos se almacenan en la carpeta `backups/` en formatos `.csv` y `.json`.
- Para restaurar datos, copia el archivo deseado desde `backups/` a `data/appointments.json` (previa copia de seguridad del archivo actual).

## Validaciones

- El módulo [`validators.py`](validators.py) contiene todas las validaciones necesarias para asegurar la integridad de los datos de entrada (fechas, horas, campos obligatorios, etc.).

## Contribuciones

¡Las contribuciones son bienvenidas! Por favor, abre un issue o un pull request para sugerencias, mejoras o correcciones.

## Licencia

Este proyecto está licenciado bajo la licencia MIT.

---

**Desarrollado por AgusMADEV**