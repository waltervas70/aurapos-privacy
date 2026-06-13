# Política de Privacidad — AuraPOS

**Última actualización:** 13 de junio de 2026

Esta política de privacidad describe cómo la aplicación móvil **AuraPOS** (en adelante, "la Aplicación") recopila, utiliza y protege la información de los usuarios. La Aplicación está desarrollada como una solución de punto de venta (POS) empresarial (B2B) orientada a la gestión comercial local de tiendas y comercios.

---

## 1. Información que Recopilamos

### A. Datos de uso local e inventario

La Aplicación opera de manera local en el dispositivo utilizando una base de datos SQLite encapsulada (`Drift`). Se almacenan localmente:

- Catálogo de productos (nombres, precios, código de barras, existencias).
- Registro de transacciones de venta (fecha, total, método de pago).
- Datos de clientes locales asignados por el propio comercio (nombre, teléfono, correo, puntos de fidelidad acumulados).

### B. Datos de ubicación y red

- **Ubicación:** La Aplicación **no** recopila, rastrea ni comparte datos de ubicación geográfica (GPS) del usuario.
- **Acceso a red:** Se utiliza la conexión a Internet únicamente para validar la licencia de uso y sincronizar los datos locales con el servidor central en la red local de la tienda.

---

## 2. Permisos del dispositivo requeridos y justificación

Para su correcto funcionamiento, la Aplicación solicita acceso a los siguientes recursos del dispositivo:

1. **Cámara** (`android.permission.CAMERA`):
   Utilizada exclusivamente para el lector de código de barras incorporado, que permite escanear productos y agregarlos al carrito de compras o buscarlos en el inventario.

2. **Bluetooth** (`android.permission.BLUETOOTH`, `android.permission.BLUETOOTH_CONNECT`):
   Requerido para buscar y conectar impresoras térmicas de tickets (ESC/POS de 58mm u 80mm) con el fin de imprimir recibos de venta de forma física.

3. **Internet** (`android.permission.INTERNET`):
   Requerido para verificar el estado de la licencia de uso y sincronizar datos del catálogo con el servidor local de la tienda.

---

## 3. Intercambio de datos con terceros

AuraPOS es una aplicación orientada a la privacidad local:

- **No vendemos, comercializamos ni transferimos** datos de transacciones, inventarios ni de clientes a terceros.
- Las consultas externas se limitan a:
  - **Firebase (Google LLC):** utilizado como infraestructura de backend para la verificación y gestión de licencias, y para el envío de notificaciones administrativas del servicio. Firebase puede recopilar datos técnicos de diagnóstico del dispositivo conforme a su propia [política de privacidad](https://policies.google.com/privacy).
  - **Servidor local del comercio:** sincronización de datos vía red local (mDNS), configurado por el propio usuario. Ningún dato sale de la red local del establecimiento.

---

## 4. Almacenamiento y seguridad

Toda la información de ventas se guarda localmente en el dispositivo. Las credenciales críticas de licencia se resguardan en el almacenamiento seguro nativo del sistema operativo (`FlutterSecureStorage`). El usuario es responsable de la custodia física del dispositivo móvil.

La Aplicación no cuenta con cuentas de usuario propias ni contraseñas almacenadas en servidores externos.

---

## 5. Retención y eliminación de datos

Los datos almacenados localmente (productos, ventas, clientes) permanecen en el dispositivo hasta que el usuario los elimine manualmente o desinstale la Aplicación. No se realizan copias de seguridad automáticas en servidores externos.

---

## 6. Cambios a esta política

Nos reservamos el derecho de actualizar esta política de privacidad cuando sea necesario. La fecha de "Última actualización" al inicio del documento refleja siempre la versión vigente. El uso continuado de la Aplicación tras una actualización implica la aceptación de los cambios.

---

## 7. Contacto del desarrollador

Para dudas, soporte o comentarios sobre esta política de privacidad, puede contactar al equipo de AuraPOS:

- **Correo electrónico:** soporte@aurapos.xyz
