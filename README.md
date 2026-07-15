# Despliegue de Infraestructura Cloud, Servidores Web y Resolución DNS en AWS

Este repositorio contiene la documentación técnica y de configuración de prácticas de ingeniería de redes y servidores aplicadas sobre la nube de **Amazon Web Services (AWS)**[cite: 1, 2].

---

## Proyecto 1: Conexión Remota Segura mediante SSH a AWS EC2

### Descripción
Despliegue y configuración de acceso remoto seguro a un servidor virtual utilizando **AWS EC2** con **Ubuntu Server**, gestionando el acceso mediante llaves criptográficas asimétricas y reglas restrictivas de firewall perimetral[cite: 1].

### Tecnologías y Componentes
*   **Instancia Cloud:** AWS EC2 (`t3.micro`)[cite: 1].
*   **Sistema Operativo:** Ubuntu Server[cite: 1].
*   **Seguridad:** Par de claves (Key Pair, archivo `.pem`)[cite: 1] y AWS Security Groups (Puerto 22/TCP)[cite: 1].
*   **Cliente SSH:** Termius[cite: 1].

---

## Proyecto 2: Configuración de Servidor Web Nginx y Enlace DNS Dinámico

### Descripción
Aprovisionamiento de un servidor web **Nginx** en la nube y configuración de un **DNS Dinámico (DDNS)** para asociar un Nombre de Dominio Completamente Calificado (FQDN) a la dirección IP pública del servidor virtual, permitiendo el enrutamiento lógico del tráfico HTTP[cite: 2].

### 🛠️ Tecnologías y Componentes
*   **Servidor Web:** Nginx (instalación, auditoría de estados mediante `systemctl` y configuración de bloques virtuales)[cite: 2].
*   **Servicio DNS:** DuckDNS para resolución dinámica de nombres (Dominio: `tonytnmnpr.duckdns.org` apuntando a la IP de AWS)[cite: 2].
*   **Configuración del Servidor (Nginx Host):** Edición del archivo `/etc/nginx/sites-available/default` para enlazar la directiva `server_name`[cite: 2].
*   **Seguridad y Puertos (AWS Security Group):** Apertura y filtrado perimetral de los siguientes puertos[cite: 2]:
    *   **Puerto 53 (UDP/TCP):** Para resolución estándar y transferencias de zonas DNS[cite: 2].
    *   **Puerto 3389 (TCP):** Habilitación para conexiones de interfaz gráfica remota (RDP)[cite: 2].
    *   **Puerto 123 (UDP):** Para sincronización horaria de red mediante protocolo NTP[cite: 2].

---

## Estructura de Documentos (`/docs`)

Los reportes detallados de ingeniería, con diagramas, comandos detallados y evidencias fotográficas de conectividad, se encuentran en la carpeta de documentación[cite: 1, 2]:

*    **`docs/Reporte_Conexion_SSH_AWS.pdf`**: Guía de despliegue de instancia EC2 y accesos por SSH[cite: 1].
*    **`docs/Implementacion_Servidor_Web_DNS.pdf`**: Guía paso a paso de instalación de Nginx, configuración de bloques virtuales, DDNS y reglas de puertos[cite: 2].

---

## Conclusiones y Habilidades Consolidadas
*   **Administración Cloud:** Experiencia en aprovisionamiento y gestión operativa de sistemas Linux sobre entornos empresariales AWS[cite: 1, 2].
*   **Seguridad Perimetral:** Implementación de políticas de cortafuegos restrictivas y del principio de mínimo privilegio en nubes públicas[cite: 1, 2].
*   **Infraestructura de Red:** Comprensión práctica de la resolución jerárquica de nombres de dominio DNS y el flujo de tráfico desde un navegador cliente hasta los recursos locales del servidor[cite: 2].
