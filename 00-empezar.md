# Proyecto ULISES - Bitácora de inicio

## Datos del equipo
- CPU: Intel i7-13700H (13th Gen)
- RAM: 16 GB (15.6 GB utilizable)
- GPU: NVIDIA RTX 4060 Laptop (8 GB VRAM)
- Almacenamiento: 954 GB (586 GB usados, 366 GB libres)
- Sistema: Windows 11
- Modelo IA local principal: Granite 4.1:8b (Ollama v0.40.4)
- Modelo de razonamiento profundo: DeepSeek-R1:8b (Ollama)
- Kernel ULISES: ulises_psicjung.py v2.5
- Entorno virtual: venv_ulises (Python)
- Ruta del proyecto: C:\Users\cesar\Documents\ULISES\

## Estado actual verificado (23/09/2026)
- [x] Repositorio creado en GitHub con licencia MIT
- [x] Ollama instalado (v0.40.4) con 12 modelos descargados
- [x] Granite 4.1:8b funcionando (prueba: "Responde exactamente: OK")
- [x] Kernel ULISES arranca correctamente
- [x] Pipeline de voz completo: Micrófono → Whisper (local) → Router de intención → IA (DeepSeek-R1) → Exportación a .docx
- [x] Dependencia `python-docx` instalada y funcionando
- [x] Generación de reportes en Word en C:\Users\cesar\Downloads\
- [x] Guardado de memoria al cerrar el kernel
- [x] Centinela operativo (snapshot y check)
- [x] Limpieza de backups viejos completada
- [ ] ulises.db limpia (pendiente de recrear)
- [ ] 3 casos anonimizados (pendiente)
- [ ] Script de agente secretario (pendiente)
- [ ] Integración de bitácora del investigador en el flujo de voz

## Comandos de emergencia
```powershell
# Activar entorno virtual
cd C:\Users\cesar\Documents\ULISES
.\venv_ulises\Scripts\Activate.ps1

# Verificar integridad
python modules\centinela.py check

# Snapshot de BD
python modules\centinela.py snapshot

# Arrancar ULISES (pipeline de voz)
python reconocimiento_voz.py

# Arrancar ULISES (kernel principal)
python ulises_psicjung.py

# Chat con Granite
ollama run granite4.1:8b

# Chat con DeepSeek-R1
ollama run deepseek-r1:8b

# Botón de emergencia
# Doble clic en RESCATE.bat
