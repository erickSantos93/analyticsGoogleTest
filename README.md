# Página de Prueba para Google Analytics

Este archivo contiene el código HTML necesario para probar los flujos y eventos en Google Analytics 4 (GA4). Guarda el siguiente contenido como un archivo `.html`, por ejemplo `index.html`, y reemplaza tu ID de medición en el lugar correspondiente.

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Prueba de Flujos - Google Analytics</title>
    
    <!-- Google Analytics -->
    <script async src="https://www.googletagmanager.com/gtag/js?id=G-XXXXXXXXXX"></script>
    <script>
        window.dataLayer = window.dataLayer || [];
        function gtag(){dataLayer.push(arguments);}
        gtag('js', new Date());

        gtag('config', 'G-XXXXXXXXXX'); // Reemplaza con tu ID real
    </script>
    <!-- Fin Google Analytics -->

    <style>
        body {
            font-family: Arial, sans-serif;
            padding: 2rem;
            text-align: center;
        }
        button {
            padding: 1rem 2rem;
            font-size: 1rem;
            cursor: pointer;
        }
    </style>
</head>
<body>
    <h1>Página de Prueba de Google Analytics</h1>
    <p>Usa esta página para verificar si los eventos y visitas se están registrando correctamente en Google Analytics.</p>

    <button onclick="gtag('event', 'click_boton_prueba', {'event_category': 'Interacción', 'event_label': 'Botón de prueba'})">
        Enviar Evento de Prueba
    </button>
</body>
</html>
