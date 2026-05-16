<div align="center">
  <h2>SIS-BIBLIO - Sistema de Gestión Bibliotecaria</h2>

[![PHP](https://img.shields.io/badge/PHP-8+-777BB4?logo=php&logoColor=white)](https://www.php.net/)
[![MySQL](https://img.shields.io/badge/MySQL-PDO-4479A1?logo=mysql&logoColor=white)](https://www.mysql.com/)
[![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)](https://developer.mozilla.org/es/docs/Web/HTML)
[![CSS3](https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=white)](https://developer.mozilla.org/es/docs/Web/CSS)
[![JavaScript](https://img.shields.io/badge/JavaScript-Vanilla-F7DF1E?logo=javascript&logoColor=black)](https://developer.mozilla.org/es/docs/Web/JavaScript)
[![PHPMailer](https://img.shields.io/badge/PHPMailer-SMTP-DD4B39?logo=gmail&logoColor=white)](https://github.com/PHPMailer/PHPMailer)

**SIS-BIBLIO** es una plataforma integral desarrollada para la administración eficiente de una biblioteca, con un avanzado **Módulo de Seguridad Web**. Construido estrictamente con **PHP puro**, HTML5, CSS3, JavaScript Vanilla y MySQL (PDO), enfatizando las mejores prácticas de **Clean Code** y **Principios SOLID**.

</div>

<br />

![448a24be-197c-4ca5-8f6f-0cf5e6452249](https://github.com/user-attachments/assets/49d68bce-f589-4d8f-8164-7885f29bdec8)

---

## Características Principales

#### 1. Módulo de Autenticación y Seguridad

- **Login Seguro**: Validación del lado del cliente y servidor. Regeneración de ID de sesión PHP (`session_regenerate_id`).
- **Antifuerza Bruta**: El sistema bloquea temporalmente las cuentas tras múltiples intentos fallidos.
- **Tokens CSRF**: Incorporados en todos los formularios y acciones críticas para evitar _Cross-Site Request Forgery_.
- **Contraseñas Hasheadas**: Uso del algoritmo seguro `PASSWORD_BCRYPT`.
- **Prevención de Inyección SQL y XSS**: Uso estricto de sentencias preparadas (PDO) y sanitización de salidas HTML (`htmlspecialchars`).
- **Arquitectura de Roles**: Diferenciación estricta entre `Administradores` y `Lectores`, con ocultación de UI y bloqueos de backend.
- **Interfaz Responsiva**: Diseño con modo oscuro adaptable a dispositivos móviles mediante cuadrículas flexibles, botones táctiles y menú de hamburguesa.

#### 2. Panel de Control (Dashboard)

- **Dashboard Estadístico**: Visualización en tiempo real de métricas e indicadores diferenciados por rol.
- **Estilos Modulares**: Cada página cuenta con su propio archivo `.css` encapsulado bajo `/assets/dashboard/`.
- **Catálogo de Libros**: CRUD completo para gestionar el acervo bibliográfico.
- **Mis Préstamos**: Historial y estado de los libros prestados por el lector.
- **Gestión de Cuentas**: Administración jerárquica para creación, edición y eliminación de cuentas de Staff y Lectores.

#### 3. Recuperación de Contraseña Segura

- Generación de un token aleatorio, único y de un solo uso, con vida útil limitada (1 hora).
- Integración al 100% con **PHPMailer** para el envío del enlace temporal al correo del usuario.

---

## Tecnologías Utilizadas

- **Backend**: PHP 8+ (Sin frameworks)
- **Base de Datos**: MySQL / MariaDB con driver PDO
- **Frontend**: HTML5, CSS3 Nativo, JavaScript Vanilla
- **Librerías**: PHPMailer (correo transaccional), FontAwesome (íconos)
- **Arquitectura**: Separación de responsabilidades funcionales (Configuración, Autenticación, Vistas)

---

## Estructura del Proyecto

```text
SIS-BIBLIO/
├── assets/                 # Estilos CSS públicos e imágenes
│   └── dashboard/          # CSS encapsulado por cada interfaz privada
├── config/                 # Lógica CORE (conexión PDO, autenticación y CSRF)
├── modules/                # Componentes del Dashboard y Formularios de CRUD
├── PHPMailer/              # Motor para envío transaccional de correos
├── base_de_datos.sql       # Script SQL (incluye usuarios de prueba bcrypted)
├── ca.pem                  # Certificado SSL para conexiones seguras en la nube
├── index.php               # Landing Page del sistema
├── login.php               # Validación de acceso
├── register.php            # Registro de nuevos lectores
├── recover.php             # Petición de recuperación (envío de email)
└── reset.php               # Cambio autorizado de contraseña (vía token)
```

---

## Configuración

1. Mueve esta carpeta a tu entorno de desarrollo (`htdocs` de Apache, XAMPP o `www` de WampServer).

2. **Configura la base de datos:**
   - Para uso **local**: Importa `base_de_datos.sql` en MySQL Workbench o phpMyAdmin.
   - Abre `config/database.php` y configura las variables de conexión.

3. **Configura PHPMailer (Recuperación de contraseña):**
   - Abre `recover.php` y localiza la configuración SMTP (aprox. línea 47).
   - En `$mail->Username`, coloca tu correo de Gmail.
   - En `$mail->Password`, genera una **Contraseña de Aplicación de 16 dígitos** desde [myaccount.google.com/apppasswords](https://myaccount.google.com/apppasswords) y pégala ahí.

4. Visita en tu navegador:

   ```bash
   http://localhost/CRUD-SIS-BIBLIO-Publico/index.php
   ```

---

## Casos de Prueba Incluidos

La base de datos se entrega pre-poblada con 2 cuentas maestras:

- **Administrador**: `admin@ejemplo.com` | Pass: `1234567`
- **Lector Estándar**: `lector@ejemplo.com` | Pass: `1234567`

---

## Desarrollador

**Emir Polito** - Desarrollador Fullstack & QA Tester.

- GitHub: [@EmirPolito](https://github.com/EmirPolito)
- LinkedIn: [Emir Polito](https://www.linkedin.com/in/emir-polito-g/)
