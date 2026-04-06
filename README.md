# LorHels-Auth

### 1. Arquitectura y Diseño (Frontend)
* **Single Page Application (SPA):** La aplicación funciona en una sola pantalla. Se siente súper rápida porque cambia entre vistas (Login, Panel, Escáner, Perfil) ocultando y mostrando secciones sin tener que recargar la página web.
* **Diseño 100% Responsivo:** Construido con **Tailwind CSS**, se adapta a cualquier pantalla. En teléfonos móviles la navegación se simplifica a iconos y las tarjetas se ajustan para que todo sea táctil y cómodo.
* **Búsqueda en tiempo real:** Una barra de búsqueda en el panel que filtra al instante a los empleados por nombre, cargo o departamento.

### 2. Base de Datos y Almacenamiento de Fotos (Backend)
* **Google Firebase:** Maneja la seguridad y los datos.
    * **Authentication:** Un sistema de login real donde solo los administradores con correo y contraseña pueden entrar al panel. Los usuarios externos entran de forma "anónima" solo para escanear.
    * **Firestore:** Guarda la información de los empleados en tiempo real.
* **Cloudinary:** Integrado directamente en el formulario. Permite subir la foto del empleado desde el celular o computadora y la guarda en la nube automáticamente, devolviendo una URL segura.

### 3. Panel de Administración (Control Total)
* **CRUD Completo:** Puedes Crear, Leer, Actualizar (Editar) y Eliminar empleados.
* **Generación Automática de QR:** Cada vez que guardas a alguien, el sistema genera automáticamente un código QR único que contiene la URL exacta hacia su perfil público.
* **Controles de Privacidad:** Agregamos casillas de verificación para que el administrador decida si el teléfono, el correo o el departamento deben ser públicos o mantenerse privados.
* **Gestión de Roles y Estados:** Puedes desactivar temporalmente a un empleado (cambiar de Activo a Inactivo) o darle permisos de Administrador a otros compañeros.

### 4. Perfil Público (El Carnet Digital)
* **Acceso por URL:** Si alguien escanea el código QR con la cámara de su celular nativa, la URL lo lleva directamente a la vista del perfil de ese empleado sin pasar por el login.
* **Indicadores de Seguridad:** Muestra un banner llamativo de "VERIFICACIÓN OFICIAL" y colores dinámicos (Verde si el empleado está Activo, Rojo si está Inactivo).
* **Acciones Rápidas Inteligentes:** Botones para llamar, enviar un WhatsApp o escribir un correo con un solo toque (solo si el administrador permitió mostrar esos datos).
* **Firma Corporativa:** Al pie del carnet, se muestran los datos oficiales de tu empresa (LorHels Auth) junto con un mapa interactivo de Google Maps para dar total legitimidad a la credencial.
* **Simulador de Escáner:** Por ahora, incluye una vista manual donde puedes pegar el ID único del empleado para simular el escaneo y probar que el perfil se vea bien.

---
