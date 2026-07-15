# Conexión Remota Segura mediante SSH a Instancia AWS EC2

## Descripción del Proyecto
Este proyecto documenta el proceso completo de despliegue, configuración y establecimiento de una conexión remota segura a un servidor virtual en la nube utilizando **Amazon Web Services (AWS)**. Se implementó una instancia **AWS EC2** con el sistema operativo **Ubuntu Server**, gestionando el acceso mediante llaves criptográficas y políticas restrictivas de filtrado de tráfico.

El objetivo principal es demostrar habilidades en la administración remota de servidores en entornos Cloud y la aplicación de lineamientos básicos de seguridad perimetral.

---

## Arquitectura y Componentes Tecnológicos

*   **Proveedor Cloud:** Amazon Web Services (AWS Console).
*   **Servidor Virtual:** Instancia EC2 (Tipo `t3.micro`).
*   **Sistema Operativo:** Ubuntu Server (Distribución Linux).
*   **Protocolo de Red:** SSH (Secure Shell) sobre puerto 22/TCP.
*   **Autenticación:** Par de claves (Key Pair) con cifrado RSA (Archivo `.pem`).
*   **Herramientas de Conexión:** Termius / Terminal de comandos.

---

## Fases del Despliegue e Implementación

### 1. Inicialización de la Instancia Cloud
*   Configuración y lanzamiento de la máquina virtual utilizando una AMI oficial de Ubuntu Server.
*   Asignación automática de una dirección IP pública para permitir el enrutamiento y acceso externo desde redes públicas.

### 2. Gestión de Seguridad y Acceso Criptográfico
*   Generación de un par de llaves (`Llave de Acceso.pem`) para mitigar los riesgos de autenticación tradicional por contraseñas mediante el uso de llaves criptográficas.
*   Configuración de políticas de firewall mediante un **Security Group** de AWS, habilitando de forma exclusiva las conexiones entrantes dirigidas al puerto 22 (SSH) bajo el protocolo de transporte TCP.

### 3. Administración y Conectividad Remota
*   Configuración de perfiles de conexión segura (Hosts) dentro de la herramienta **Termius**.
*   Validación exitosa del handshake de SSH y acceso directo a la shell remota del servidor de AWS para su posterior gestión.

---

## Contenido del Repositorio

*   **`/docs/Reporte_Conexion_SSH_AWS.pdf`**: Documento de ingeniería detallado que contiene los objetivos de la práctica, los detalles conceptuales de la arquitectura, la evidencia fotográfica del aprovisionamiento en la consola de AWS y la captura de la conexión exitosa por consola.

---

## Conclusiones y Aprendizajes Técnicos
*   Comprensión del funcionamiento del protocolo SSH para establecer canales de comunicación completamente cifrados.
*   Experiencia práctica en el aprovisionamiento de infraestructura en la nube y el uso de consolas de administración Cloud de nivel empresarial.
*   Implementación de buenas prácticas en seguridad de redes mediante el principio de mínimo privilegio en reglas de Security Groups.
