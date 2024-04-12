<script lang="ts">
  let emailInput = "";
  let passwordInput = "";
  let error = "";
  let message = "";

  //import { signInWithEmail } from "../../db/auth";

  async function signIn() {
    //await signInWithEmail(emailInput, passwordInput);
  }
</script>

<div class="form">
  <div class="title">
    <p>Inicia Sesión</p>
  </div>

  <form on:submit|preventDefault={signIn}>
    <div class="item-input">
      <label for="email">Correo:</label>
      <input type="email" id="email" bind:value={emailInput} />
    </div>
    <div class="item-input">
      <label for="password">Contraseña:</label>
      <input type="password" id="password" bind:value={passwordInput} />
    </div>
    <a href="/" class="small-text underline-hover">¿Olvidaste tu contraseña?</a>
    <input class="btn" type="submit" value="Login" />
  </form>

  {#if error}
    <div class="error">{error}</div>
  {/if}
  {#if message}
    <div class="message">{message}</div>
  {/if}

  <div class="footer-form">
    <div class="flex-row-text">
      <p>¿Aún no tiene una cuenta?</p>
      <a href="/register" class="underline-hover">Regístrese</a>
    </div>
  </div>
</div>

<style>
  /* Estilos para pantallas más pequeñas (menor de 650px) */
  @media screen and (max-width: 650px) {
    .form {
      min-width: 15rem;
    }
  }

  @media screen and (max-width: 650px) {
    .form {
      min-width: 15rem;
      padding: 2rem;
    }
  }
</style>
