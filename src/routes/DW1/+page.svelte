<script>
    import { onMount } from 'svelte';
  
    let email = '';
    let password = '';
    let errorMessage = '';
  
    // Função para validar o formulário
    function alidateForm() {
      if (!email || !password) {
        errorMessage = 'Por favor, preencha todos os campos.';
        return false;
      }
  
      if (!/^[^\s@]+@[^\s@]+\.[^\s@]+$/.test(email)) {
        errorMessage = 'Insira um e-mail válido.';
        return false;
      }
  
      errorMessage = '';
      return true;
    }
  
    // Função para lidar com o envio do formulário
    function handleSubmit(event) {
      event.preventDefault();
  
      if (validateForm()) {
        console.log('E-mail:', email);
        console.log('Senha:', password);
        alert('Login bem-sucedido!');
  
        // Resetar campos
        email = '';
        password = '';
      }
    }
  </script>
  
  <style>
    .login-container {
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      background-color: #f5f5f5;
    }
  
    .login-box {
      background: white;
      padding: 2rem;
      border-radius: 8px;
      box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
      max-width: 400px;
      width: 100%;
    }
  
    h2 {
      text-align: center;
      margin-bottom: 1.5rem;
    }
  
    form {
      display: flex;
      flex-direction: column;
    }
  
    label {
      margin-bottom: 0.5rem;
      font-weight: bold;
    }
  
    input {
      padding: 0.75rem;
      margin-bottom: 1rem;
      border: 1px solid #ddd;
      border-radius: 4px;
      font-size: 1rem;
    }
  
    .error {
      color: red;
      font-size: 0.9rem;
      margin-bottom: 1rem;
    }
  
    button {
      padding: 0.75rem;
      background-color: #007bff;
      color: white;
      border: none;
      border-radius: 4px;
      cursor: pointer;
      font-size: 1rem;
    }
  
    button:hover {
      background-color: #0056b3;
    }
  </style>
  
  <div class="login-container">
    <div class="login-box">
      <h2>Login</h2>
  
      {#if errorMessage}
        <div class="error">{errorMessage}</div>
      {/if}
  
      <form on:submit|preventDefault={handleSubmit}>
        <label for="email">E-mail</label>
        <input type="email" id="email" bind:value={email} placeholder="Digite seu e-mail" />
  
        <label for="password">Senha</label>
        <input type="password" id="password" bind:value={password} placeholder="Digite sua senha" />
  
        <button type="button" onclick="DW2';">Entrar</button>

      </form>
    </div> 
  </div>