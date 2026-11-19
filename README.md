# MyPetsFriends - ERP Veterinario

## Descripción del proyecto

MyPetsFriends es un sistema ERP desarrollado para gestionar las operaciones principales de una clínica veterinaria.

El proyecto utiliza Odoo Community, PostgreSQL y Docker para proporcionar un entorno centralizado de gestión de clientes, productos, servicios, inventario, ventas y facturación.

## Tecnologías utilizadas

- **Odoo Community 20.0:** plataforma ERP.
- **PostgreSQL 16:** sistema de gestión de bases de datos.
- **Docker:** ejecución de los servicios mediante contenedores.
- **Docker Compose:** administración de los contenedores.
- **Git y GitHub:** control de versiones y almacenamiento del código.

## Módulos instalados

- Contactos.
- Ventas.
- Inventario.
- Facturación.
- Calendario.

## Información registrada

Se realizó la carga inicial de información mediante archivos CSV:

| Archivo | Registros |
|---|---:|
| propietarios.csv | 15 |
| proveedores.csv | 5 |
| productos.csv | 30 |
| **Total** | **50** |

También se configuraron cinco servicios veterinarios:

- Consulta veterinaria.
- Vacunación.
- Baño para mascotas.
- Desparasitación.
- Cirugía veterinaria.

## Flujo de venta comprobado

Se realizó una prueba de venta utilizando los siguientes datos:

- Cliente: Carlos Mendoza.
- Producto: Alimento para perro adulto 3 kg.
- Cantidad: 2 unidades.
- Precio unitario: S/45.00.
- Subtotal: S/90.00.
- IGV: S/16.20.
- Total: S/106.20.

Se comprobó la entrega del producto, la actualización del inventario, la generación de la factura y el registro del pago de prueba.

## Inventario

Se registraron cantidades iniciales para cinco productos.

Después de validar la entrega de dos unidades de alimento para perro adulto de 3 kg, el inventario pasó de 20 a 18 unidades.

## Instalación y ejecución

### Requisitos

- Windows.
- Docker Desktop.
- Docker Compose.
- Git.
- Visual Studio Code.

### Iniciar el proyecto

Clonar el repositorio:

```bash
git clone https://github.com/nikoTM02/MyPetsFriends-ERP.git
```

Ingresar a la carpeta:

```bash
cd MyPetsFriends-ERP
```

Configurar el archivo `.env` con las variables requeridas por `docker-compose.yml`.

Descargar las imágenes:

```bash
docker compose pull
```

Iniciar los servicios:

```bash
docker compose up -d
```

Comprobar los contenedores:

```bash
docker compose ps
```

Acceder a Odoo desde el navegador:

```text
http://localhost:8069
```

## Copias de seguridad

Se realizó una copia de seguridad de PostgreSQL utilizando `pg_dump` en formato personalizado.

También se verificó la integridad de lectura del archivo y se realizó una restauración en una base de datos temporal para comprobar la recuperación de los registros.

El respaldo se almacena localmente en la carpeta `backups/`.

## Estructura del proyecto

```text
MyPetsFriends/
│
├── addons/
├── backups/
├── config/
├── csv/
├── screenshots/
│
├── .env
├── .gitignore
├── docker-compose.yml
└── README.md
```

## Evidencias

La carpeta `screenshots/` contiene las capturas de:

- Contactos.
- Productos.
- Servicios veterinarios.
- Inventario.
- Orden de venta.
- Entrega de productos.
- Factura.
- Pago.
- Reporte de ventas.
- Reporte de inventario.

## Consideraciones

Este proyecto utiliza los módulos estándar de Odoo Community adaptados al contexto de una clínica veterinaria. Las funcionalidades veterinarias especializadas, como historias clínicas de mascotas y registros de vacunación, pueden requerir módulos adicionales o desarrollo personalizado.

## Autor

Proyecto académico: **MyPetsFriends - ERP Veterinario**.