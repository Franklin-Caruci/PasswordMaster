🔐 Password Master V1.2 - Pro Editor Edition
Password Master es una aplicación web ligera y segura diseñada para gestionar credenciales de dispositivos, cuentas de acceso y contraseñas personales. Combina la comodidad de la sincronización en la nube con la seguridad de la encriptación local de grado militar.

🚀 Características Principales
🔒 Cifrado AES-256: Todas tus contraseñas se encriptan localmente en tu navegador mediante una Llave Maestra. Tus datos nunca viajan por internet en texto plano.

☁️ Sincronización con Google Drive: Guarda y recupera tu bóveda cifrada automáticamente en tu cuenta personal de Google Drive.

📱 Multiplataforma: Accede a tus claves desde tu PC (Localhost) o desde tu celular Android (GitHub Pages).

✏️ Editor Integrado: Corrige errores fácilmente mediante el icono de edición (lápiz) sin duplicar registros.

📂 Importación/Exportación: Realiza respaldos manuales en formato JSON para mayor seguridad.

🔍 Buscador Inteligente: Filtra rápidamente por nombre de dispositivo, usuario o categoría.

🏷️ Organización por Niveles: Clasifica tus datos en Personal, Trabajo, Dispositivos/Red o Bancos.

🛡️ Arquitectura de Seguridad (Zero-Knowledge)
La aplicación utiliza un modelo de Conocimiento Cero:

Ingresas tu Llave Maestra (no se almacena en ningún lugar).

La aplicación usa esa llave para descifrar el archivo .enc descargado de Drive.

Si pierdes tu Llave Maestra, los datos en Drive son técnicamente imposibles de recuperar, ya que Google solo aloja el archivo cifrado.

🛠️ Configuración e Instalación
Para habilitar la sincronización en la nube en tu propio repositorio:

1. Google Cloud Console
Crea un proyecto en Google Cloud Console.

Habilita la Google Drive API.

Configura la Pantalla de Consentimiento OAuth (Modo Producción).

Crea las credenciales:

API Key.

ID de Cliente OAuth 2.0 (Tipo: Aplicación Web).

IMPORTANTE: En "Orígenes de JavaScript autorizados", añade:

http://localhost (para pruebas locales).

https://tu-usuario.github.io (URL de GitHub Pages).

2. Integración en el Código
Pega tus credenciales en las constantes al inicio del script en index.html:

JavaScript

const CLIENT_ID = 'TU_ID_CLIENTE';
const API_KEY = 'TU_API_KEY';
📖 Guía de Uso
Inicio por primera vez
Abre la aplicación y define una Llave Maestra robusta.

Presiona el icono de Google Drive para conectar tu cuenta.

Comienza a añadir tus credenciales mediante el botón + Nueva.

Corregir datos
Haz clic en el icono verde (✎) de cualquier tarjeta.

Modifica los campos necesarios en el modal.

Pulsa Actualizar Bóveda. El sistema guardará los cambios localmente y los subirá a la nube de forma invisible.

Sincronización entre PC y Android
En PC: Carga tus datos y asegúrate de que el punto de estado esté en verde.

En Android: Abre tu URL de GitHub Pages, ingresa la misma Llave Maestra y presiona conectar a Drive. Tus datos aparecerán instantáneamente.

🛠️ Tecnologías Utilizadas
HTML5 / JavaScript (ES6+)

Tailwind CSS: Para una interfaz moderna y responsiva con efectos de Glassmorphism.

CryptoJS: Motor de encriptación AES-256.

Google Drive API v3: Para almacenamiento persistente en la nube.

GSI (Google Identity Services): Para una autenticación segura.

⚠️ Notas de Seguridad
Nunca compartas tu archivo index.html si contiene tus credenciales de API en un repositorio público. Se recomienda mantener el repositorio de GitHub como Privado.

Realiza exportaciones periódicas mediante el botón Exportar y guárdalas en un lugar seguro.

Desarrollado por Franklin Caruci - 2026