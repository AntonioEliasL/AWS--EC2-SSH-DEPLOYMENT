# Suite de Infraestructura Cloud: Despliegue, DNS y Servidor Web en AWS

Este repositorio concentra un conjunto de prácticas de ingeniería de sistemas y redes aplicadas sobre entornos de nube de **Amazon Web Services (AWS)**, demostrando capacidades de administración remota, gestión de dominios y publicación de servicios web[cite: 1, 2, 3].

---

## Proyecto 1: Conexión Remota Segura mediante SSH a AWS EC2

### Descripción
Despliegue y configuración de acceso remoto seguro a un servidor virtual utilizando **AWS EC2** con **Ubuntu Server**, gestionando la autenticación mediante llaves criptográficas asimétricas y directivas de firewall perimetral[cite: 1].

### Tecnologías y Componentes
*   **Instancia Cloud:** AWS EC2 (`t3.micro`)[cite: 1].
*   **Sistema Operativo:** Ubuntu Server[cite: 1].
*   **Seguridad:** Par de claves (Key Pair, archivo `.pem`)[cite: 1] y AWS Security Groups (Puerto 22/TCP)[cite: 1].
*   **Cliente SSH:** Termius[cite: 1].

---

## Proyecto 2: Configuración de Servidor Web Nginx y Enlace DNS Dinámico

### Descripción
Aprovisionamiento de un servidor web **Nginx** en la nube y configuración de un **DNS Dinámico (DDNS)** para asociar un Nombre de Dominio Completamente Calificado (FQDN) a la dirección IP pública de la instancia, permitiendo el enrutamiento lógico de tráfico de red[cite: 2].

### Tecnologías y Componentes
*   **Servidor Web:** Nginx (administración de servicio con `systemctl` y configuración de Server Blocks)[cite: 2].
*   **Servicio DNS:** DuckDNS para resolución dinámica de nombres (Dominio: `tonytnmnpr.duckdns.org` enlazado a la IP de AWS)[cite: 2].
*   **Configuración del Servidor:** Vinculación de directivas en `/etc/nginx/sites-available/default`[cite: 2].
*   **Puertos y Firewall (AWS Security Group):**[cite: 2]
    *   **Puerto 53 (UDP/TCP):** Resolución y transferencia de zonas DNS[cite: 2].
    *   **Puerto 3389 (TCP):** Acceso remoto por interfaz gráfica (RDP)[cite: 2].
    *   **Puerto 123 (UDP):** Sincronización de hora mediante protocolo NTP[cite: 2].

---

## Proyecto 3: Despliegue de Aplicación Web Interactiva mediante HTTP/HTTPS

### Descripción
Habilitación y mapeo de los puertos de red web estándar para transformar la instancia cloud en un servidor público accesible universalmente. Se implementó una arquitectura de integración híbrida para desplegar un aplicativo interactivo (Pacman) optimizando el almacenamiento local de la máquina virtual[cite: 3].

### Tecnologías y Componentes
*   **Gestión de Archivos:** Limpieza segura de rutas del sistema (`/var/www/html`) utilizando la CLI mediante comandos como `rm -f` e hilado de código web con `nano`[cite: 3].
*   **Integración de Código:** Despliegue híbrido mediante el embebido de un elemento `<iframe>` a pantalla completa[cite: 3], llamando dinámicamente al código fuente alojado en un repositorio externo de **GitHub Gist**[cite: 3].
*   **Seguridad Perimetral (AWS Security Group):**[cite: 3]
    *   **HTTP (Puerto 80):** Tráfico web entrante estándar para la carga inicial del sitio web[cite: 3].
    *   **HTTPS (Puerto 443):** Habilitación y preparación de la infraestructura para el cifrado y seguridad del dominio[cite: 3].

---

## Estructura de Documentos (`/docs`)

La evidencia fotográfica, la salida de comandos en consola, el código HTML maquetado y los reportes de ingeniería detallados se organizan de la siguiente manera[cite: 1, 2, 3]:

*    **`docs/Reporte_Conexion_SSH_AWS.pdf`**: Guía de despliegue de instancia EC2 y accesos remotos[cite: 1].
*    **`docs/Implementacion_Servidor_Web_DNS.pdf`**: Bitácora de instalación de Nginx, vinculación DNS y configuración de zonas[cite: 2].
*    **`docs/Despliegue_Web_HTTP_HTTPS.pdf`**: Registro del despliegue del aplicativo web, integración con GitHub Gists y apertura de puertos de navegación[cite: 3].

---

## Conclusiones y Habilidades Consolidadas
*   **DevOps y Cloud:** Capacidad comprobada para aprovisionar, configurar, asegurar y mantener servicios vivos en entornos de producción en la nube[cite: 1, 2, 3].
*   **Networking Avanzado:** Dominio del flujo de datos en red, desde la resolución de nombres DNS hasta la negociación de solicitudes mediante los protocolos y puertos HTTP (80) y HTTPS (443)[cite: 2, 3].
*   **Soluciones Eficientes de Almacenamiento:** Uso de arquitecturas híbridas (embebidos desde Gists) para optimizar los recursos físicos de servidores virtuales en la nube[cite: 3].
