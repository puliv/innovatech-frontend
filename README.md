InnovaTech - Frontend (Rama Deploy)

Este repositorio contiene la interfaz de usuario para el ecosistema de aplicaciones de InnovaTech. La rama deploy aloja el código listo para ser compilado y distribuido en servidores de producción, integrando los módulos de ventas y despacho en una única experiencia de usuario.
Funcionamiento del Proyecto

El frontend sirve como el punto de interacción principal para administradores, personal de ventas y operadores logísticos. Está diseñado como una aplicación web moderna que consume las APIs de los servicios backend correspondientes para visualizar datos en tiempo real, gestionar pedidos y realizar el seguimiento de las entregas.

Capacidades principales:

    Visualización de catálogos y gestión de carritos de compra.

    Paneles de control (dashboards) para la supervisión de métricas de venta.

    Interfaz de seguimiento de rutas y estados de despacho.

    Gestión de usuarios y perfiles de empleados.

    Diseño adaptativo para su uso en computadoras de escritorio y dispositivos móviles.

Requisitos del Sistema

    Node.js (Versión LTS).

    Gestor de paquetes npm o yarn.

    Navegador web moderno compatible con estándares ES6+.

    Acceso a las URLs de los backends de ventas y despacho.

Instalación

    Descargar el código fuente:
    git clone https://github.com/puliv/innovatech-frontend

    Acceder al directorio y cambiar a la rama de producción:
    cd innovatech-frontend
    git checkout deploy

    Instalar las dependencias de desarrollo y producción:
    npm install

Configuración de Entorno

El proyecto requiere variables de entorno para apuntar a los servicios correctos. Cree un archivo .env o .env.production con los siguientes parámetros:

    VITE_API_VENTAS_URL: Dirección base de la API de ventas.

    VITE_API_DESPACHO_URL: Dirección base de la API de despacho.

    VITE_APP_TITLE: Nombre de la instancia de la aplicación.

Compilación y Despliegue

A diferencia del backend, el frontend debe ser compilado en archivos estáticos para ser servido por un servidor web (como Nginx o Apache):

    Construir el paquete de producción:
    npm run build

    Previsualización local (opcional):
    npm run preview

Los archivos resultantes en la carpeta dist (o build) son los que deben transferirse al servidor de hosting final.
Estructura de la Aplicación

    Components: Elementos de interfaz reutilizables.

    Views/Pages: Páginas principales (Ventas, Despacho, Login, Inventario).

    Services: Lógica de comunicación con las APIs backend.

    Store/State: Gestión del estado global de la aplicación.

Notas de la Rama

La rama deploy contiene las optimizaciones finales de rendimiento, como minificación de código y compresión de activos. Todo ajuste visual o de experiencia de usuario debe trabajarse en ramas de desarrollo antes de su integración final en esta rama.