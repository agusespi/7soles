# 🍺 Distribuidora de Bebidas - Sistema de Pedidos Full-Stack

Sistema web interactivo para la gestión de pedidos y catálogo de una distribuidora de bebidas. Permite a los clientes navegar productos, armar carritos y seguir el estado de su pedido en tiempo real, mientras que brinda al administrador un panel integral para gestionar inventarios, precios y el flujo completo de entrega.

---

## 🚀 Características Principales

* **Vista Cliente (`index.html`)**:
  * Catálogo de productos interactivo.
  * Carrito de compras dinámico.
  * Formulario de datos de envío y método de pago.
  * **Seguimiento en vivo**: Polling automático cada 5 segundos para actualizar el estado del pedido (*Pendiente*, *Confirmado*, *Rechazado*, *Finalizado*).

* **Panel de Administración (`admin.html`)**:
  * Control del interruptor global de delivery (Habilitar/Deshabilitar).
  * Gestión de stock y precios con actualización inmediata.
  * Carga de nuevos productos con imágenes subidas localmente.
  * **Tablero Kanban de Pedidos**: Filtrado por estado con acciones rápidas para aceptar (abre notificación de WhatsApp con un clic), rechazar con motivo o finalizar.

* **Backend (`app.py`)**:
  * Servidor RESTful desarrollado en Flask.
  * Gestión de archivos estáticos y subida de imágenes seguras.
  * Almacenamiento en memoria para ejecución rápida y prototipado local.

---

## 📁 Descripción de los Archivos del Proyecto

```text
distribuidora_bebidas/
│
├── app.py                 # Servidor Flask principal y API REST
├── templates/
│   ├── index.html         # Interfaz pública para el cliente (Catálogo y Checkout)
│   └── admin.html         # Panel de control de administración y gestión de pedidos
├── static/
│   ├── css/
│   │   └── style.css      # Estilos visuales globales de la aplicación
│   └── uploads/           # Carpeta donde se guardan las imágenes cargadas por el admin
└── README.md              # Documentación del proyecto
