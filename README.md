# Festival Vallenato - Sistema de Votaciones

## Descripción

Sistema web desarrollado en Django para la gestión de votaciones del Festival Vallenato.

Permite:

- Registro de usuarios.
- Inicio y cierre de sesión.
- Gestión de ediciones.
- Gestión de categorías.
- Gestión de opciones de votación.
- Registro de votos.
- Consulta de votos realizados.
- Visualización de resultados.
- Consulta de categorías mediante API JSON.

---

## Tecnologías Utilizadas

- Python 3.11.9
- Django 5.2.18
- MySQL
- HTML5
- CSS3
- Bootstrap
- Git
- GitHub

---

## Repositorio

```text
https://github.com/SebastianMoralesU/EJE-3_FESTIVALVALLENATO
```

---

## Instalación

### Clonar el repositorio


```

### Ingresar al proyecto

```
cd EJE-3_FESTIVALVALLENATO
```

### Crear entorno virtual

```
python -m venv env_festival
```

### Activar entorno virtual

```
env_festival\Scripts\activate
```

### Instalar dependencias

```
pip install -r requirements.txt
```

---



## Creación de Usuario Administrador

```
python manage.py createsuperuser
```

Acceso al panel administrativo:

```text
http://127.0.0.1:8000/admin/
```

---

## Configuración de MySQL

Crear la base de datos:

```
CREATE DATABASE festival_db;
```

Configurar la conexión en:

```
pr_festival/settings.py
```

Ejemplo:

```python
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.mysql',
        'NAME': 'festival_db',
        'USER': 'usuario_mysql',
        'PASSWORD': 'password_mysql',
        'HOST': 'localhost',
        'PORT': '3306',
    }
}
```

---

## Migraciones

Ejecutar las migraciones de la base de datos:

```
python manage.py makemigrations
python manage.py migrate
```

---

## Datos de Prueba

### Edición

```
Festival Vallenato 2026
```

### Categorías

```
Acordeonero Profesional
Canción Inédita
Piquería
```

### Opciones

```
Juan Pérez
Carlos Gómez
Primavera Eterna
Sebastian Morales Morales
```

---

## Ejecución del Proyecto

Iniciar el servidor de desarrollo:

```
python manage.py runserver
```

Abrir en el navegador:

```
http://127.0.0.1:8000/
```

---

## API Disponible

### Consultar Categorías

```
GET /api/categorias/
```

Ejemplo de respuesta:

```json
[
  {
    "categoria": "Acordeonero Profesional",
    "opciones": [
      "Juan Pérez",
      "Sebastian Morales Morales"
    ]
  }
]
```

---

## Funcionalidades

- Registro de usuarios.
- Inicio de sesión.
- Cierre de sesión.
- Gestión de ediciones.
- Gestión de categorías.
- Gestión de opciones.
- Registro de votos.
- Validación de voto único por categoría.
- Consulta de votos realizados.
- Visualización de resultados.
- API REST para consulta de categorías.

---