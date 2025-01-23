<script>
    import { onMount } from "svelte";
  
    let nome = "";
    let usuario = "";
    let senha = "";
    let confirmSenha = "";
    let msgError = "";
    let msgSuccess = "";
  
    function cadastrar() {
      // Limpa mensagens anteriores
      msgError = "";
      msgSuccess = "";
  
      // Validação de campos
      if (!nome || !usuario || !senha || !confirmSenha) {
        msgError = "Todos os campos são obrigatórios!";
        return;
      }
  
      if (senha !== confirmSenha) {
        msgError = "As senhas não coincidem!";
        return;
      }
  
      // Simula sucesso no cadastro
      msgSuccess = "Cadastro realizado com sucesso!";
      function cadastrar() {
  // Limpa mensagens anteriores
  msgError = "";
  msgSuccess = "";
  
  // Limpa os campos após o sucesso
  nome = "";
  usuario = "";
  senha = "";
  confirmSenha = "";
}
    }
  
  </script>
  
  
  <div class="container">
    <h1>Cadastrar</h1>
  
    <div id="msgError">{msgError}</div>
    <div id="msgSuccess">{msgSuccess}</div>
  
    <div class="label-float">
      <input
        type="text"
        id="nome"
        bind:value={nome}
        placeholder=" "
        required
      />
      <label id="labelNome" for="nome">Nome</label>
    </div>
  
    <div class="label-float">
      <input
        type="text"
        id="usuario"
        bind:value={usuario}
        placeholder=" "
        required
      />
      <label id="labelUsuario" for="usuario">Usuário</label>
    </div>
  
    <div class="label-float">
      <input
        type="password"
        id="senha"
        bind:value={senha}
        placeholder=" "
        required
      />
      <label id="labelSenha" for="senha">Senha</label>
    </div>
  
    <div class="label-float">
      <input
        type="password"
        id="confirmSenha"
        bind:value={confirmSenha}
        placeholder=" "
        required
      />
      <label id="labelConfirmSenha" for="confirmSenha">Confirmar Senha</label>
    </div>
  
    <div class="justify-center">
      <button on:click={cadastrar}>Cadastrar</button>
    </div>
    <div class="justify-center">
      <a class ="btn" href="/DW2">Ir para outra página</a>
    </div>
  </div>

  
  <style>
    /* Estilo básico para centralizar o conteúdo e estilizar o formulário */
    .container {
      max-width: 400px;
      margin: auto;
      padding: 20px;
      border: 1px solid #ccc;
      border-radius: 8px;
      box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
      text-align: center;
    }
  
    .label-float {
      position: relative;
      margin: 20px 0;
    }
  
    .label-float input {
      width: 100%;
      padding: 10px;
      border: 1px solid #ccc;
      border-radius: 4px;
    }
  
    .label-float label {
      position: absolute;
      top: 10px;
      left: 12px;
      font-size: 12px;
      color: #666;
    }
  
    .justify-center {
      margin-top: 20px;
    }
  
    button {
      padding: 10px 20px;
      background-color: #007bff;
      color: white;
      border: none;
      border-radius: 4px;
      cursor: pointer;
    }
  
    button:hover {
      background-color: #0056b3;
    }
  
    #msgError {
      color: red;
      margin-bottom: 10px;
    }
  
    #msgSuccess {
      color: green;
      margin-bottom: 10px;
    }
  </style>
  