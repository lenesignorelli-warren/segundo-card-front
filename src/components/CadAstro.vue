<template>
<head>
    <meta name="viewport" content="width=device-width, initial-scale=1">
<link href="https://fonts.googleapis.com/icon?family=Material+Icons" rel="stylesheet">
</head>
  
  <div class="container">
      <div class="header">
          <h2>Criar uma conta</h2>
      </div>

      <form id="form" class="form">
          <div class="form-control error">
              <label for="username">Nome de Usuário</label>
              <input type="text" id="username" placeholder="Digite seu nome de usuário..."/>
              <i class="material-icons exclamation">&#xe000;</i>
              <i class="material-icons check">&#xe86c;</i>
              <small>Mensagem de Erro</small>
          </div>

          <div class="form-control error">
              <label for="email">E-mail</label>
              <input type="text" id="email" placeholder="Digite seu e-mail..."/>
              <i class="material-icons exclamation">&#xe000;</i>
              <i class="material-icons check">&#xe86c;</i>
              <i class="material-icons">&#xe0be;</i>
              <small>Mensagem de Erro</small>
          </div>

           <div class="form-control success">
              <label for="password">Senha</label>
              <input type="text" id="password" placeholder="Digite sua senha..."/>
              <i class="material-icons exclamation">&#xe000;</i>
              <i class="material-icons check">&#xe86c;</i>
              <small>Mensagem de Erro</small>
          </div>

          <div class="form-control">
              <label for="password-confirmation">Confirmação de Senha</label>
              <input type="text" id="password-confirmation" placeholder="Digite sua senha novamente..."/>
              <i class="material-icons exclamation">&#xe000;</i>
              <i class="material-icons check">&#xe86c;</i>
              <small>Mensagem de Erro</small>
          </div>

          <button type="submit">Enviar</button>
      </form>
  </div>
</template>

<script>
export default {
    name: "CadAstro"
};
</script>

<style scoped>
* {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
}

.container {
    width: 100%;
    min-height: 100vh;
    display: center;
    justify-content: center;
    align-items: center;
    width: 400px;
    max-width: 100%;
}

.form {
    padding: 20px;
}

.form-control {
    margin-bottom: 10px;
    padding-bottom: 20px;
}

.form-control label {
    display: inline-block;
    margin-bottom: 5px;
}

.form-control input {
    border: 2px solid;
    display: block;
    border-radius: 10px;
    font-size: 14px;
    width: 100%;
    padding: 10px;
}

.form-control i {
   position: initial; 
   visibility: hidden;
}

.form-control small {
    position: relative;
    bottom: 0;
    left: 0;
    visibility: hidden;
}

.form button {
  background-color: #e02b57;
  border: none;
  border-radius: 50px;
  color: white;
  padding: 10px;
  font-weight: bold;
}

/* Error and Success */
.form-control.success input {
  border-color: #2ecc71;
}

.form-control.error input {
  border-color: #e74c3c;
}

.form-control.success i.check {
  color: #2ecc71;
  visibility: visible;
}

.form-control.error i.exclamation {
  color: #e74c3c;
  visibility: visible;
}

.form-control.error small {
  color: #e74c3c;
  visibility: visible;
}
</style>