# Registro de uso de IA

| Fecha | Herramienta | Parte / tarea | Propósito | Qué verificó, adaptó o descartó el grupo |
| --- | --- | --- | --- | --- |
| 2026-10-15 | Claude (Anthropic) | Parte 1 / Ejercicio 1 | Guía paso a paso para crear la VM, preparar el disco de LFS y resolver errores de version-check.sh | Se verificó con lsblk -f que el disco de LFS no era el del ejemplo del enunciado. Se adaptó el campo fsck del fstab (1 2 en vez de 1 1). Se confirmó la versión estable del libro en linuxfromscratch.org. Cada comando se ejecutó y se revisó su salida antes de continuar |
| 2026-11-06 a 2026-11-08 | Claude (Anthropic) | Parte 1 / capítulos 3 a 7 | Guía de comandos por sección y diagnóstico de errores | Los comandos se contrastaron con el libro LFS 13.1-systemd en linuxfromscratch.org; se corrigieron opciones que la IA había propuesto de versiones anteriores (--enable-kernel=5.10, parche upstream_fixes de glibc, $LFS_TGT-readelf). El error de MPC se diagnosticó con make -j1 y se verificó en el árbol de GCC |
