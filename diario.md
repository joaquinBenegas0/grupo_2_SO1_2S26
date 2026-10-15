# Diario de trabajo

|Fecha|Tarea|Participantes|Decisiones|Problemas|Solución|Resultado|Evidencia|
|-|-|-|-|-|-|-|-|
|2026-10-15|Ej. 1: creación de la VM|Joaquín Benegas, Nicolás Rodríguez|VirtualBox, 6 vCPU, 12 GB RAM, BIOS/MBR (sin EFI). Disco 1 de 30 GB para Rocky y disco 2 de 40 GB dedicado a LFS. NAT + solo-anfitrión. Hostname grupo-2-lfs-host (los hostnames no admiten guion bajo)|—|—|VM operativa con acceso SSH|evidencias/parte1/anfitrion.txt|
|2026-10-15|Ej. 1: ISO de Rocky 10.2|Joaquín Benegas, Nicolás Rodríguez|Verificación SHA256 contra CHECKSUM oficial|—|—|Hash coincidente|Captura Get-FileHash|
|2026-10-15|Ej. 1: disco de LFS|Joaquín Benegas, Nicolás Rodríguez|MBR, una partición ext4 etiquetada LFS. fstab por UUID con campo fsck = 2 (1 se reserva para la raíz)|El disco de LFS apareció como sda y no sdb como en el enunciado; tras reiniciar los nombres se invirtieron|Verificar siempre con lsblk -f antes de tocar discos; montaje por UUID|/mnt/lfs se monta solo tras reiniciar|evidencias/parte1/disco-lfs.txt|
|2026-10-15|Ej. 1: version-check.sh|Joaquín Benegas, Nicolás Rodríguez|Libro LFS 13.1 systemd, fecha de inicio 2026-10-15|ERROR: yacc is NOT Bison (el grupo Development Tools instala byacc)|dnf remove byacc y wrapper /usr/bin/yacc que ejecuta bison -y, según el libro|Sin errores|evidencias/parte1/version-check.txt|
|2026-10-15|Ej. 1: erratas|Joaquín Benegas, Nicolás Rodríguez|Sin erratas generales registradas. Avisos de seguridad de Expat y Aspell revisados el 15/10/2026.|La página antigua de avisos de seguridad ya no se actualiza.|Se consultó la plataforma nueva, filtrando por LFS 13.1.|Sin erratas generales. Se identificaron avisos de Expat y Aspell.|https://www.linuxfromscratch.org/lfs/errata/13.1-systemd/ y https://www.linuxfromscratch.org/advisories/|
|2026-10-15|Ej. 1: snapshot inicial|Joaquín Benegas, Nicolás Rodríguez|Snapshot 00-host-listo-version-check-ok con la VM apagada, punto de retorno antes de compilar|—|—|Snapshot creado|evidencias/parte1/snapshot00.png|



