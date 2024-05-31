<!-- En este ejemplo, doubled se actualiza automáticamente cuando count cambia gracias a la declaración reactiva $: doubled = count * 2. -->
<script>
  // Declaramos dos variables
  let count = 0;
  let doubled;

  // Declaración reactiva que actualiza `doubled` cuando `count` cambia
  $: doubled = count * 2;

  // Función para incrementar el contador
  function increment() {
    count += 1;
  }
</script>

<!-- Mostramos los valores de las variables en el HTML -->
<p>Count: {count}</p>
<p>Doubled: {doubled}</p>
<button on:click={increment}>Increment</button>
