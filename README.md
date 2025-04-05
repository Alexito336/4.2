# 4.1

implementacion 
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Formulario Principal - Cartelera Cine</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: #f4f4f4;
      margin: 0;
      padding: 20px;
    }

    .panel {
      background-color: #fff;
      border-radius: 12px;
      box-shadow: 0 4px 10px rgba(0,0,0,0.1);
      max-width: 700px;
      margin: auto;
      padding: 30px;
    }

    .panel h2 {
      margin-top: 0;
      color: #2c3e50;
      text-align: center;
    }

    .input-group {
      margin-bottom: 15px;
    }

    .input-group label {
      display: block;
      margin-bottom: 5px;
      font-weight: bold;
    }

    .input-group input[type="text"] {
      width: 100%;
      padding: 10px;
      border: 1px solid #ccc;
      border-radius: 8px;
    }

    .button-group {
      text-align: center;
      margin-top: 20px;
    }

    .button-group button {
      padding: 10px 20px;
      margin: 5px;
      border: none;
      background-color: #3498db;
      color: white;
      border-radius: 8px;
      cursor: pointer;
      font-weight: bold;
    }

    .tabs {
      display: flex;
      margin-top: 20px;
      border-bottom: 2px solid #ccc;
    }

    .tab-button {
      flex: 1;
      padding: 10px;
      text-align: center;
      cursor: pointer;
      font-weight: bold;
      background-color: #ecf0f1;
    }

    .tab-button.active {
      background-color: #3498db;
      color: white;
      border-bottom: 2px solid white;
    }

    .tab-content {
      display: none;
      padding: 20px;
    }

    .tab-content.active {
      display: block;
    }
  </style>
</head>
<body>

  <div class="panel">
    <h2>Formulario Principal</h2>

    <div class="input-group">
      <label for="nombre">Nombre</label>
      <input type="text" id="nombre" placeholder="Ingresa tu nombre">
    </div>

    <div class="input-group">
      <label for="email">Correo electrónico</label>
      <input type="text" id="email" placeholder="ejemplo@correo.com">
    </div>

    <div class="button-group">
      <button>Enviar</button>
      <button>Cancelar</button>
    </div>

    <div class="tabs">
      <div class="tab-button active" onclick="mostrarTab('tab1')">Cartelera</div>
      <div class="tab-button" onclick="mostrarTab('tab2')">Promociones</div>
    </div>

    <div id="tab1" class="tab-content active">
      <h3>Películas en Cartelera</h3>
      <p>Aquí puedes consultar los títulos en exhibición, horarios disponibles y clasificaciones.</p>
    </div>

    <div id="tab2" class="tab-content">
      <h3>Cupones y Promociones</h3>
      <p>Descubre los descuentos disponibles para entradas, combos de comida y promociones especiales.</p>
    </div>
  </div>

  <script>
    function mostrarTab(id) {
      // Ocultar todos los contenidos
      const tabs = document.querySelectorAll('.tab-content');
      tabs.forEach(tab => tab.classList.remove('active'));

      // Desactivar todos los botones
      const buttons = document.querySelectorAll('.tab-button');
      buttons.forEach(btn => btn.classList.remove('active'));

      // Mostrar contenido y activar botón correspondiente
      document.getElementById(id).classList.add('active');
      const index = id === 'tab1' ? 0 : 1;
      buttons[index].classList.add('active');
    }
  </script>

  <p style="max-width: 700px; margin: 30px auto; font-size: 16px; text-align: justify;">
    El uso de contenedores en el diseño web permite organizar los elementos de forma lógica y atractiva, mejorando tanto la estética como la experiencia del usuario. Un panel bien estructurado, como el mostrado, divide claramente las secciones, agrupa campos relacionados y permite integrar funcionalidades como pestañas sin desorden. Esta técnica proporciona una interfaz profesional y accesible, en comparación con estructuras básicas donde los controles están desordenados. Los contenedores también facilitan la adaptación a distintos dispositivos, permitiendo un diseño responsivo. En conjunto, aportan claridad visual, orden funcional y una navegación intuitiva.
  </p>

</body>
</html>
