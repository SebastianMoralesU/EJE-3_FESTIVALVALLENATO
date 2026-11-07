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
https://github.com/SebastianMoralesU/EJE_3_FESTIVALVALLENATO.git
```

---

## Instalación

### Clonar el repositorio

```powershell
git clone https://github.com/SebastianMoralesU/EJE_3_FESTIVALVALLENATO.git
```

### Ingresar al proyecto

```powershell
cd EJE_3_FESTIVALVALLENATO
```

### Crear entorno virtual

```powershell
python -m venv env_festival
```

### Activar entorno virtual

```powershell
env_festival\Scripts\activate
```

### Instalar dependencias

```powershell
pip install django
pip install mysqlclient
```

---

## Configuración de MySQL

Crear la base de datos:

```sql
CREATE DATABASE festival_db;
```

Configurar en:

```python
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

```powershell
python manage.py makemigrations
python manage.py migrate
```

---

## Datos de Prueba

### Edición

```text
Festival Vallenato 2026
```

### Categorías

```text
Acordeonero Profesional
Canción Inédita
Piquería
```

### Opciones

```text
Juan Pérez
Carlos Gómez
Primavera Eterna
Sebastian Morales Morales
```

---

## Ejecución

```powershell
python manage.py runserver
```

Abrir:

```text
http://127.0.0.1:8000/
```

---

## API Disponible

### Consultar categorías

```http
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
- Gestión de categorías.
- Gestión de opciones.
- Registro de votos.
- Validación de voto único.
- Consulta de votos realizados.
- Resultados de votación.
- API REST de categorías.
