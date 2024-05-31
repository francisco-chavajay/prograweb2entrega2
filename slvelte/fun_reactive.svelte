<!-- En este ejemplo, area se actualiza automáticamente cuando width o height cambian gracias a la declaración reactiva $: area = calculateArea(width, height). -->

<script>
  // Declaramos dos variables
  let width = 100;
  let height = 100;
  let area;

  // Declaración reactiva que actualiza `area` cuando `width` o `height` cambian
  $: area = calculateArea(width, height);

  // Función para calcular el área
  function calculateArea(w, h) {
    return w * h;
  }

  // Funciones para cambiar las dimensiones
  function increaseWidth() {
    width += 10;
  }

  function increaseHeight() {
    height += 10;
  }
</script>

<!-- Mostramos los valores de las variables en el HTML -->
<p>Width: {width}</p>
<p>Height: {height}</p>
<p>Area: {area}</p>
<button on:click={increaseWidth}>Increase Width</button>
<button on:click={increaseHeight}>Increase Height</button>
