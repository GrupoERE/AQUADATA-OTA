# AQUADATA-OTA 🌊

Repositorio para gestión de actualizaciones Over-The-Air (OTA) del sistema AQUADATA.

## 📁 Estructura del Repositorio

AQUADATA-OTA/
├── firmware/
│   ├── v1.0.0/           # Primera versión
│   ├── v1.1.0/           # Versiones futuras
│   └── latest/           # Última versión estable
├── version.json          # Control de versiones
└── README.md            # Este archivo

## 🚀 Cómo usar este repositorio

### Para desarrolladores:
1. Compilar el código Arduino y generar el archivo .bin
2. Subir el archivo .bin a la carpeta de versión correspondiente
3. Actualizar el archivo `version.json`
4. Copiar el archivo .bin también a la carpeta `latest/`

### Para el sistema OTA:
El dispositivo consultará automáticamente:
- `version.json` para verificar nuevas versiones
- `firmware/latest/` para descargar la actualización

## 📋 Formato del archivo version.json
```json
{
  "latest_version": "1.0.0",
  "firmware_url": "URL_del_archivo_bin",
  "changelog": "Descripción de cambios",
  "mandatory": false,
  "release_date": "YYYY-MM-DD",
  "file_size_kb": 0,
  "checksum": "hash_del_archivo"
}


## 🚀 Cómo usar este repositorio

### Para desarrolladores:
1. Compilar el código Arduino y generar el archivo .bin
2. Subir el archivo .bin a la carpeta de versión correspondiente
3. Actualizar el archivo `version.json`
4. Copiar el archivo .bin también a la carpeta `latest/`

### Para el sistema OTA:
El dispositivo consultará automáticamente:
- `version.json` para verificar nuevas versiones
- `firmware/latest/` para descargar la actualización

## 📋 Formato del archivo version.json
```json
{
  "latest_version": "1.0.0",
  "firmware_url": "URL_del_archivo_bin",
  "changelog": "Descripción de cambios",
  "mandatory": false,
  "release_date": "YYYY-MM-DD",
  "file_size_kb": 0,
  "checksum": "hash_del_archivo"
}
🔄 Flujo de actualización OTA

Arduino consulta version.json
Compara versión local vs remota
Si hay nueva versión → descarga desde latest/
Instala automáticamente
Reinicia con nuevo firmware

⚠️ Importante

✅ Siempre actualizar latest/ con la versión estable más reciente
✅ Mantener version.json actualizado
✅ Usar nombres descriptivos para los archivos .bin
✅ Probar el firmware antes de subirlo a latest/

📊 Estado actual

Versión actual: 1.0.0 (Pendiente de subir)
Última actualización: 2024-09-14
Repositorio: Configurado y listo para usar
