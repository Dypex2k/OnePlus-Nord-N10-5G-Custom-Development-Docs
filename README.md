# OnePlus-Nord-N10-5G-Custom-Development-Docs
Este repositorio contiene los archivos esenciales y la documentación técnica para la implementación de Kali NetHunter en el OnePlus Nord N10 5G (Codename: billie). El objetivo es proporcionar un entorno de auditoría de seguridad estable, superando las limitaciones de las particiones dinámicas y los bloqueos de solo lectura de Android 10/11.

ESPECIFICACIONES

Modelo: BE2026 / BE2029
Arquitectura: ARM64
SO Base: Android 10 / 11

INSTALACION DE TWRP

Desbloquear Bootloader (Obligatorio).
Entrar a modo Fastboot: adb reboot bootloader
Boot temporal: fastboot boot twrp_file.img
Nota: Si el touch no funciona, usar mouse por OTG o comandos ADB.

BOOT.IMG MODIFICADO (ROOT Y NETHUNTER)

Extraer boot.img original de la ROM.
Parchear con Magisk App para obtener Root.
Para NetHunter: Habilitar en el kernel soporte HID y Drivers Wi-Fi externos.
Flash: fastboot flash boot magisk_patched.img

SOLUCION DE ERRORES COMUNES

Error I/O o Read-only: Android 10 bloquea /system. Usar 'mount -o remount,rw /' en TWRP.
Bootanimation: Si no cambia en /system/media, buscar en /product/media.
