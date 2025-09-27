# Compremos-Penoles
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Bono Verde Peñoles: Inversión a 10 Años</title>
    <style>
        /* Estilos Generales */
        body {
            font-family: 'Arial', sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f4f7f6;
            color: #333;
            text-align: center;
        }
        .container {
            max-width: 800px;
            margin: 50px auto;
            padding: 40px;
            background-color: #fff;
            border-radius: 12px;
            box-shadow: 0 4px 20px rgba(0, 0, 0, 0.1);
        }

        /* Estilos para el Encabezado y Marca */
        header {
            background-color: #006040; /* Verde oscuro (sostenibilidad) */
            color: #ffffff;
            padding: 20px 0;
            border-top-left-radius: 12px;
            border-top-right-radius: 12px;
            margin: -40px -40px 30px -40px;
        }
        header h1 {
            margin: 0;
            font-size: 2.2em;
            letter-spacing: 1px;
        }
        header p {
            font-size: 1.1em;
            margin-top: 5px;
            font-style: italic;
        }

        /* Estilos para la Imagen (Minería Ecológica) */
        .hero-image {
            margin-bottom: 30px;
            border-radius: 8px;
            overflow: hidden;
        }
        .hero-image img {
            max-width: 100%;
            height: auto;
            display: block;
            margin: 0 auto;
        }

        /* Estilos de la Sección de Bonos */
        .details h2 {
            color: #1a4a87;
            font-size: 1.8em;
            margin-bottom: 20px;
        }
        .key-feature {
            font-size: 1.2em;
            margin: 15px 0;
            line-height: 1.5;
            padding: 5px 0;
            border-bottom: 1px dashed #eee;
        }
        .key-feature:last-child {
             border-bottom: none;
        }
        .key-feature strong {
            color: #006040;
            font-weight: bold;
        }
        
        /* Estilo para la Tasa Final Calculada */
        .final-rate {
            font-size: 2.0em;
            font-weight: bold;
            color: #ffaa00; /* Dorado para destacar la tasa */
            margin: 20px 0;
            padding: 10px;
            border: 2px solid #ffaa00;
            display: inline-block;
            border-radius: 5px;
        }

        .disclaimer {
            font-size: 0.85em;
            color: #777;
            margin-top: 30px;
        }

        /* Estilos del Botón de Acción (Comprar) */
        .buy-button {
            display: inline-block;
            padding: 15px 35px;
            margin-top: 30px;
            background-color: #ffaa00;
            color: #333;
            text-decoration: none;
            font-size: 1.4em;
            font-weight: bold;
            border-radius: 8px;
            transition: background-color 0.3s ease, transform 0.1s ease;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
            cursor: pointer;
        }
        .buy-button:hover:not(.disabled) {
            background-color: #e09500;
            transform: translateY(-2px);
        }
        .buy-button.disabled {
            background-color: #ccc;
            cursor: not-allowed;
            box-shadow: none;
        }

        /* Estilos para el mensaje de confirmación */
        #confirmation-message {
            margin-top: 20px;
            font-size: 1.5em;
            color: #006040;
            font-weight: bold;
            opacity: 0;
            transition: opacity 0.5s ease-in-out;
        }
        #confirmation-message.show {
            opacity: 1;
        }
    </style>
    <script>
        function handleBuyClick(event) {
            event.preventDefault(); 
            
            const buyButton = document.getElementById('buyButton');
            const confirmationMessage = document.getElementById('confirmation-message');
            
            if (buyButton.classList.contains('disabled')) return;

            buyButton.classList.add('disabled');
            buyButton.style.pointerEvents = 'none'; 
            buyButton.textContent = 'Registrando interés...';

            setTimeout(() => {
                confirmationMessage.textContent = '¡Gracias! Ya eres parte del futuro.';
                confirmationMessage.classList.add('show');
            }, 1000); 
        }
    </script>
</head>
<body>

    <div class="container">
        <header>
            <h1>Bono Verde Peñoles</h1>
            <p>Financiamiento para la Sustentabilidad Minera en México</p>
        </header>

        <div class="hero-image">
             <img src="https://storage.googleapis.com/haxd-green-bond-image/green_mining_concept.jpg" alt="Ilustración de minería sostenible con turbinas eólicas y paneles solares sobre un entorno natural.">
        </div>

        <section class="details">
            <h2>Detalles Financieros (Estimados)</h2>
            
            <div class="key-feature">
                **Plazo:** **10 años** con pagos de cupón semestrales.
            </div>

            <div class="key-feature">
                **Tasa de Referencia:** TIIE de Fondeo (7.8%)
            </div>
            
            <div class="key-feature">
                **Spread por Riesgo (Corporativo):** + 0.90%
            </div>
            
            <div class="key-feature">
                **Greenium (Ahorro por Etiqueta Verde):** - 0.05%
            </div>
            
            <div class="key-feature">
                **Cálculo (Yield/Tasa Final):** 7.8% (TIIE) + 0.90% (Spread) - 0.05% (Greenium)
            </div>

            <div class="final-rate">
                Tasa Flotante Estimada: **8.65%**
            </div>
            
            <div class="key-feature">
                **Destino del Capital:** Proyectos de **eficiencia energética**, **gestión hídrica** y **reducción de emisiones** en nuestras operaciones.
            </div>

            <a href="#" id="buyButton" class="buy-button" onclick="handleBuyClick(event)">
                ¡Comprar Ahora!
            </a>

            <div id="confirmation-message"></div>

            <p class="disclaimer">
                *Esta página es informativa y no constituye una oferta pública de valores. La tasa final es estimada y variable, referenciada a la TIIE de Fondeo. El rendimiento final estará sujeto a las condiciones del mercado al momento de la colocación y al prospecto definitivo.*
            </p>
        </section>
    </div>

</body>
</html>
