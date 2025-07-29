# 💻 GesTec – Sistema Web de Inventario

**GesTec** es un sistema web desarrollado como parte de un proyecto de prácticas preprofesionales en la **Red de Salud Trujillo – UTES N.º 06**.
El objetivo principal es mejorar la gestión, trazabilidad y control de equipos y componentes informáticos, reemplazando procesos manuales con una herramienta digital moderna, intuitiva y eficiente.

---

## 📊 Comparativo de Resultados

| Aspecto Evaluado                 | Antes del Sistema      | Después del Sistema             | % de Mejora Estimada |
| -------------------------------- | ---------------------- | ------------------------------- | -------------------- |
| Uso de registros manuales        | 100 % en Excel         | 20 % (uso mínimo para respaldo) | 🔻 80 %              |
| Tiempo por registro              | \~5 min por equipo     | \~1.5 min por equipo            | ⏱️ 70 %              |
| Trazabilidad de equipos          | 30 % seguimiento claro | 95 % seguimiento actualizado    | 🔺 65 %              |
| Atención de requerimientos       | \~1 día                | \~3 horas                       | ⏱️ 75 %              |
| Errores en registros             | 4 de cada 10           | 1 de cada 10                    | 🔻 75 %              |
| Satisfacción del usuario técnico | 40 %                   | 85 %                            | 🔺 45 %              |

> 🔍 Estos datos se obtuvieron a partir de observación directa, validaciones de usuario y comparación de tiempos de operación antes y después del sistema implementado.

---

## ⚙️ Tecnologías utilizadas

* **Frontend**: HTML, CSS, JavaScript
* **Backend**: Python 3.10.12, Django
* **Base de datos**: PostgreSQL 17
* **Librerías**:

  * Pillow
  * psycopg2-binary

---

## 📦 Instalación del entorno

### 🔧 Requisitos previos

* Python 3.10.12
* PostgreSQL 17
* Git (opcional para clonar el repositorio)

---

### 🛠️ Pasos de instalación

1. **(Opcional) Clonar el repositorio:**

```bash
git clone https://github.com/gussanx1/GesTec.git
cd GesTec
```

2. **Eliminar cualquier entorno virtual anterior si lo hubiera.**

3. **Crear un nuevo entorno virtual:**

```bash
python -m venv venv
```

4. **Activar el entorno virtual:**

```bash
.\venv\Scripts\activate
```

5. **Instalar las dependencias necesarias:**

```bash
pip install django
pip install pillow
pip install psycopg2-binary
pip install -r requirements.txt
```

6. **Configurar base de datos en `settings.py`:**

```python
'NAME': 'nombre_de_tu_db',
'USER': 'postgres',
'PASSWORD': '12345',
'HOST': 'localhost',
'PORT': '5432',
```

---

## 🗃️ Configuración de la base de datos

### 🔄 Opción 1: Importar base de datos ya creada

Si ya tienes un archivo `.backup` con los datos de prueba, importa directamente desde PostgreSQL.

> No necesitas migrar.

### ⚙️ Opción 2: Crear estructura desde cero

```bash
python manage.py makemigrations
python manage.py migrate
```

### 👤 Crear superusuario para acceder al sistema

```bash
cd gestion_utes
python manage.py createsuperuser
```

> Se solicitará nombre de usuario, correo y contraseña para acceso como administrador.

---

## ▶️ Ejecución del sistema

Con todo configurado, ejecuta:

```bash
python manage.py runserver
```

---

## 🚀 Apertura rápida del proyecto (modo diario)

Cada vez que desees abrir el sistema en modo local:

```bash
.venv\Scripts\activate
cd gestion_utes
python manage.py runserver
```

> No es necesario tener PostgreSQL abierto manualmente si ya está configurado como servicio.

---

## 🧠 Funcionalidades clave de GesTec

* Registro digital de equipos y componentes informáticos.
* Seguimiento y trazabilidad por ubicación, estado y tipo.
* Validación y edición de datos desde formularios web.
* Filtrado dinámico de equipos por estado, sede y características.
* Interfaz intuitiva validada por usuarios técnicos de la OGI.

---

## 📈 Potencial de escalabilidad

* Integración futura con plataformas SIGA/SIAF.
* Implementación de módulos de reportes interactivos.
* Control de usuarios por rol (administrador, técnico, auditor).
* Soporte para más tipos de activos (mobiliario, redes, etc).

---

## 👨‍💻 Autor

**Luis Gustavo Sánchez Villalva**
Estudiante de Ingeniería de Sistemas – IX ciclo
Universidad César Vallejo
Proyecto desarrollado en la Red de Salud Trujillo – UTES N.° 06
Nombre del sistema: **GesTec**

---
