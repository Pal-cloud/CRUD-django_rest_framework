# Librería - API REST con Django REST Framework

Una aplicación web desarrollada con Django y Django REST Framework para gestionar una librería con libros y categorías.

## 🚀 Características

- **API REST completa** para gestión de libros y categorías
- **Django REST Framework** para serialización y vistas API
- **Base de datos SQLite** (configurable para PostgreSQL)
- **Variables de entorno** para configuraciones sensibles
- **Estructura modular** con aplicaciones separadas

## 📋 Requisitos

- Python 3.8+
- pip (gestor de paquetes de Python)

## 🛠️ Instalación

### 1. Clonar el repositorio
```bash
git clone <url-del-repositorio>
cd CRUD-django_rest_framework/libreria
```

### 2. Crear entorno virtual
```bash
python -m venv .venv
```

### 3. Activar entorno virtual
- **Windows:**
  ```bash
  .venv\Scripts\activate
  ```
- **macOS/Linux:**
  ```bash
  source .venv/bin/activate
  ```

### 4. Instalar dependencias
```bash
pip install -r requirements.txt
```

### 5. Configurar variables de entorno
Copia el archivo de ejemplo y configura tus variables:
```bash
cp .env.example .env
```

Edita el archivo `.env` con tus configuraciones:
```env
SECRET_KEY=tu-secret-key-aqui
DEBUG=True
DATABASE_NAME=db.sqlite3
DATABASE_ENGINE=django.db.backends.sqlite3
```

### 6. Realizar migraciones
```bash
python manage.py makemigrations
python manage.py migrate
```

### 7. Crear superusuario (opcional)
```bash
python manage.py createsuperuser
```

### 8. Ejecutar el servidor
```bash
python manage.py runserver
```

La aplicación estará disponible en `http://127.0.0.1:8000/`

## 📁 Estructura del Proyecto

```
libreria/
├── manage.py                 # Script de gestión de Django
├── requirements.txt          # Dependencias del proyecto
├── .env                     # Variables de entorno (no incluido en git)
├── .env.example             # Ejemplo de variables de entorno
├── .gitignore              # Archivos ignorados por git
├── libreria/               # Configuración principal del proyecto
│   ├── __init__.py
│   ├── settings.py         # Configuraciones del proyecto
│   ├── urls.py            # URLs principales
│   ├── wsgi.py            # Configuración WSGI
│   └── asgi.py            # Configuración ASGI
├── libros/                # Aplicación para gestión de libros
│   ├── __init__.py
│   ├── admin.py           # Configuración del admin
│   ├── apps.py            # Configuración de la app
│   ├── models.py          # Modelos de datos
│   ├── views.py           # Vistas de la API
│   ├── tests.py           # Pruebas unitarias
│   └── migrations/        # Migraciones de base de datos
└── categorias/            # Aplicación para gestión de categorías
    ├── __init__.py
    ├── admin.py           # Configuración del admin
    ├── apps.py            # Configuración de la app
    ├── models.py          # Modelos de datos
    ├── views.py           # Vistas de la API
    ├── tests.py           # Pruebas unitarias
    └── migrations/        # Migraciones de base de datos
```

## 🔧 Configuración

### Variables de Entorno

El proyecto utiliza variables de entorno para configuraciones sensibles. Las principales variables son:

- `SECRET_KEY`: Clave secreta de Django
- `DEBUG`: Modo de depuración (True/False)
- `DATABASE_ENGINE`: Motor de base de datos
- `DATABASE_NAME`: Nombre de la base de datos
- `DATABASE_USER`: Usuario de la base de datos (para PostgreSQL)
- `DATABASE_PASSWORD`: Contraseña de la base de datos (para PostgreSQL)
- `DATABASE_HOST`: Host de la base de datos (para PostgreSQL)
- `DATABASE_PORT`: Puerto de la base de datos (para PostgreSQL)

### Base de Datos

Por defecto, el proyecto usa SQLite. Para usar PostgreSQL:

1. Instala psycopg2:
   ```bash
   pip install psycopg2-binary
   ```

2. Actualiza tu archivo `.env`:
   ```env
   DATABASE_ENGINE=django.db.backends.postgresql
   DATABASE_NAME=nombre_de_tu_bd
   DATABASE_USER=tu_usuario
   DATABASE_PASSWORD=tu_contraseña
   DATABASE_HOST=localhost
   DATABASE_PORT=5432
   ```

## 🏗️ Aplicaciones

### Libros
Gestiona la información de los libros de la librería.

### Categorías
Gestiona las categorías para clasificar los libros.

## 🔌 API Endpoints

Una vez que configures los modelos y serializers, la API proporcionará endpoints para:

- `GET /api/libros/` - Listar todos los libros
- `POST /api/libros/` - Crear un nuevo libro
- `GET /api/libros/{id}/` - Obtener un libro específico
- `PUT /api/libros/{id}/` - Actualizar un libro
- `DELETE /api/libros/{id}/` - Eliminar un libro

- `GET /api/categorias/` - Listar todas las categorías
- `POST /api/categorias/` - Crear una nueva categoría
- `GET /api/categorias/{id}/` - Obtener una categoría específica
- `PUT /api/categorias/{id}/` - Actualizar una categoría
- `DELETE /api/categorias/{id}/` - Eliminar una categoría

## 🧪 Pruebas

Ejecutar las pruebas unitarias:
```bash
python manage.py test
```

## 📚 Tecnologías Utilizadas

- **Django 6.0.1**: Framework web de Python
- **Django REST Framework**: Toolkit para crear APIs REST
- **SQLite**: Base de datos por defecto
- **python-decouple**: Gestión de variables de entorno

## 🤝 Contribuir

1. Fork el proyecto
2. Crea una rama para tu feature (`git checkout -b feature/AmazingFeature`)
3. Commit tus cambios (`git commit -m 'Add some AmazingFeature'`)
4. Push a la rama (`git push origin feature/AmazingFeature`)
5. Abre un Pull Request

## 👨‍💻 Autor

Pal - paloma.gom.sal@gmail.com

## 🔗 Enlaces

- [Documentación de Django](https://docs.djangoproject.com/)
- [Documentación de Django REST Framework](https://www.django-rest-framework.org/)

---

⌨️ con ❤️ por [Pal-cloud](https://github.com/Pal-cloud)