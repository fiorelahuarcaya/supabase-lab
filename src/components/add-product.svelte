<script lang="ts">
  let id = "";
  let nombre = "";
  let categoria = "";
  let precio = 0;
  let stock = 0;
  let estado = "";

  function agregarProducto() {}
</script>

<form on:submit|preventDefault={agregarProducto}>
  <h3>Agregar nuevo Producto</h3>

  <div class="input">
    <label for="nombre">Nombre de Producto</label>
    <input type="text" id="nombre" bind:value={nombre} />
  </div>

  <div class="input">
    <label for="categoria">Categoria</label>
    <input type="text" id="categoria" bind:value={categoria} />
  </div>

  <div class="input">
    <label for="precio">Precio</label>
    <input type="number" id="precio" bind:value={precio} step="0.01" />
  </div>

  <div class="input">
    <label for="stock">Stock</label>
    <input type="number" id="stock" bind:value={stock} />
  </div>

  <div class="input">
    <label for="estado">Estado</label>
    <select id="estado" bind:value={estado}>
      <option value="true">Disponible</option>
      <option value="false">No Disponible</option>
    </select>
  </div>

  <div class="btns">
    <button type="submit">Añadir</button>
  </div>
</form>

<style>
  form {
    display: flex;
    flex-direction: column;
    gap: 1rem;
    width: 100%;
  }

  form .input {
    display: flex;
    flex-direction: column;
    gap: 0.5rem;
  }

  .btns {
    display: flex;
    flex-direction: row;
    width: 100%;
    justify-content: space-between;
  }
</style>
