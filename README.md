<div align="center">

# SIS BIBLIO
[![PHP](https://img.shields.io/badge/PHP-8+-777BB4?logo=php&logoColor=white)](https://www.php.net/)
[![MySQL](https://img.shields.io/badge/MySQL-PDO-4479A1?logo=mysql&logoColor=white)](https://www.mysql.com/)
[![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)](https://developer.mozilla.org/es/docs/Web/HTML)
[![CSS3](https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=white)](https://developer.mozilla.org/es/docs/Web/CSS)
[![JavaScript](https://img.shields.io/badge/JavaScript-Vanilla-F7DF1E?logo=javascript&logoColor=black)](https://developer.mozilla.org/es/docs/Web/JavaScript)
[![PHPMailer](https://img.shields.io/badge/PHPMailer-SMTP-DD4B39?logo=gmail&logoColor=white)](https://github.com/PHPMailer/PHPMailer)

</div>

---

**SIS BIBLIO** es una plataforma desarrollada para la administración eficiente de bibliotecas, integrando un sistema de autenticación seguro, gestión de préstamos y control de usuarios mediante una arquitectura construida completamente con **PHP puro**, MySQL y JavaScript Vanilla.

<br>

<img width="1600" alt="SIS-BIBLIO Preview" src="https://github.com/user-attachments/assets/49d68bce-f589-4d8f-8164-7885f29bdec8"/>

---

## Características

- **Sistema Seguro**: Protección contra SQL Injection, XSS y ataques CSRF mediante PDO y validaciones seguras.
- **Gestión de Roles**: Paneles diferenciados para `Administradores` y `Lectores`.
- **Catálogo Bibliotecario**: CRUD completo para libros, préstamos y administración de cuentas.
- **Recuperación de Contraseña**: Integración con PHPMailer para envío seguro de correos.
- **Dashboard Responsivo**: Interfaz adaptable con soporte para modo oscuro y dispositivos móviles.

---

## Estructura del Proyecto

```text
SIS-BIBLIO/
├── assets/                 # Estilos CSS e imágenes
├── config/                 # Conexión PDO, autenticación y seguridad
├── modules/                # Componentes y módulos CRUD
├── PHPMailer/              # Librería de correos SMTP
├── base_de_datos.sql       # Script SQL principal
├── index.php               # Landing Page
├── login.php               # Inicio de sesión
├── register.php            # Registro de lectores
├── recover.php             # Recuperación de contraseña
└── reset.php               # Restablecimiento mediante token
```

---

## Tecnologías Utilizadas

- **Backend:** PHP 8+
- **Base de Datos:** MySQL / MariaDB con PDO
- **Frontend:** HTML5, CSS3 y JavaScript Vanilla
- **Librerías:** PHPMailer y FontAwesome

---

## Instalación

### 1. Clonar el repositorio

```bash
git clone https://github.com/EmirPolito/CRUD-SIS-BIBLIO-Publico.git
cd CRUD-SIS-BIBLIO-Publico
```

### 2. Configurar la base de datos

Importa el archivo:

```bash
base_de_datos.sql
```

en MySQL o MariaDB y configura las credenciales en:

```bash
config/database.php
```

### 3. Configurar PHPMailer

En `recover.php` agrega:

- Tu correo Gmail en `$mail->Username`
- Tu contraseña de aplicación en `$mail->Password`

### 4. Ejecutar proyecto

Coloca el proyecto en tu servidor local (`XAMPP`, `Laragon` o `WAMP`) y abre:

```bash
http://localhost/CRUD-SIS-BIBLIO-Publico/index.php
```

---

## Cuentas de Prueba

| Rol | Correo | Contraseña |
|------|---------|-------------|
| Administrador | `admin@ejemplo.com` | `1234567` |
| Lector | `lector@ejemplo.com` | `1234567` |


---

## Licencia

Este proyecto está bajo la licencia **MIT**. Consulta el archivo [LICENSE](LICENSE) para más detalles.

---

## Desarrollador

**Emir Polito** - Frontend & QA Tester

- X: https://x.com/emirpolitog
- GitHub: https://github.com/EmirPolito
- LinkedIn: https://www.linkedin.com/in/emirpolitog/
