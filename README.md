# **Car Manager - Django Application**

Car Manager es una aplicación web desarrollada con Django que permite a los usuarios gestionar información de vehículos, asignar permisos personalizados y proporcionar un flujo de registro, inicio y cierre de sesión con roles de usuario claramente definidos.

## **Características principales**
- **Gestión de Autos:** Los usuarios pueden ver y editar vehículos registrados en el sistema.
- **Sistema de Roles y Permisos:**
  - Roles disponibles: **Admin**, **Editor**, **Viewer**.
  - Permisos personalizados como `edit_car` para editar autos.
- **Dashboard:** Una interfaz intuitiva para gestionar autos.
- **Registro de usuarios:** Proporciona un formulario de registro que asigna roles dinámicamente.
- **Inicio/Cierre de sesión:** Integración con vistas predeterminadas y personalizadas de Django.
- **Interfaz moderna:** Estilo responsivo con Bootstrap 5.

---

## **Tecnologías utilizadas**
- **Backend:**
  - Python 3.x
  - Django 4.x
- **Frontend:**
  - HTML5, CSS3, Bootstrap 5
- **Base de datos:** SQLite (por defecto, fácil de reemplazar por PostgreSQL o MySQL)
- **Autenticación:** Sistema de autenticación de usuarios integrado de Django

---

## **Requisitos previos**
1. Python 3.x instalado en tu máquina.
2. Pipenv o virtualenv (recomendado).
3. Node.js (opcional, si necesitas trabajar con herramientas frontend adicionales).
4. Django instalado (ver instrucciones de instalación).

---

## **Instalación y configuración**

### 1. Clonar el repositorio
```bash
git clone https://github.com/tu-usuario/car-manager.git
cd car-manager
```

### 2. Crear y activar un entorno virtual
```bash
python -m venv env
source env/bin/activate  # Linux/Mac
env\Scripts\activate     # Windows
```

### 3. Instalar dependencias
```bash
pip install -r requirements.txt
```

### 4. Realizar migraciones
```bash
python manage.py makemigrations
python manage.py migrate
```

### 5. Crear un superusuario (opcional)
```bash
python manage.py createsuperuser
```

### 6. Iniciar el servidor de desarrollo
```bash
python manage.py runserver
```

### 7. Acceder a la aplicación
Abre tu navegador y visita: `http://127.0.0.1:8000/`

---

## **Uso de la aplicación**

### Roles y permisos
- **Admin:** Acceso completo a todos los módulos.
- **Editor:** Permiso para editar autos (`edit_car`).
- **Viewer:** Solo puede ver la información, sin acceso a ediciones.

### Flujo del usuario
1. Registra un nuevo usuario desde la página de registro (`/register/`).
2. Inicia sesión con las credenciales (`/login/`).
3. Gestiona tus autos desde el dashboard (`/dashboard/`).

---

## **Estructura del proyecto**

```
car-manager/
├── auth_app/
│   ├── migrations/
│   ├── templates/
│   │   ├── auth_app/
│   │   │   ├── dashboard.html
│   │   │   ├── login.html
│   │   │   └── register.html
│   ├── admin.py
│   ├── apps.py
│   ├── forms.py
│   ├── models.py
│   ├── urls.py
│   └── views.py
├── manage.py
├── requirements.txt
├── README.md
└── db.sqlite3
```

---

---

## **Contribuir**

1. Realiza un fork del repositorio.
2. Crea una nueva rama:
   ```bash
   git checkout -b feature/nueva-funcionalidad
   ```
3. Realiza tus cambios y sube los commits:
   ```bash
   git commit -m "Agregué nueva funcionalidad"
   git push origin feature/nueva-funcionalidad
   ```
4. Abre un Pull Request.

---

## **Licencia**
Este proyecto está licenciado bajo la [MIT License](LICENSE).

---
