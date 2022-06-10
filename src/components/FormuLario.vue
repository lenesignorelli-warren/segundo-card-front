<template>
  <head>
    <meta name="viewport" content="width=device-width, initial-scale=1" />
    <link href="https://fonts.googleapis.com/icon?family=Material+Icons" rel="stylesheet"/>
  </head>
  <div class="bar">
    <h3>FORMULÁRIO</h3>
  </div>
  <section class="container">
    
    <div class="form">
      <h1>Seja Bem Vindo</h1>
      <p>Dados de Contato</p>
      <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
    <form action="index.php" method="post">
      <div class="input-box">
        <label for="name">Nome Completo</label>
        <input type="text" name="name" placeholder="Digite seu nome..." required />
      </div>
      <div class="input-box">
        <label for="email">E-mail</label>
        <i class="material-icons">&#xe0be;</i>
        <input type="email" id="email" placeholder="Digite seu e-mail" required />
        
        <small>Mensagem de erro</small>
      </div>
      <div class="input-box">
        <label for="confirmemail">Confirmar E-mail</label>
        <input type="email" id="confirmemail" placeholder="Digite seu e-mail" required />
        <small>Mensagem de erro</small>
      </div>
      <div class="input-box">
        <label for="cpf">Cpf</label>
        <input type="cpf" id="cpf" placeholder="Digite seu cpf (somente números)" autocomplete="off" maxlength="14" onkeypress="mascara_cpf ()" required />
        <small>Mensagem de erro</small>
      </div>
      <div class="input-box">
        <label for="phone">Celular</label>
        <input type="tel" id="phone" placeholder="Digite o n° celular" maxlength="14" required />
        <small>Mensagem de erro</small>
      </div>
      <div class="input-box">
        <label for="birthday">Data de Nascimento</label>
        <input type="date" id="birthday" required />
      </div>
      <div class="form">
        <br>
        <p><strong>Lorem ipsum dolor sit amet, consectetur adipiscing elit.</strong></p>
        <br>
        <p><strong>Sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</strong></p>
        <br />
      </div>
      <div class="form">
        <input type="checkbox" id="email" />
        <label for="email">E-mail e SMS</label>
        <br>
        <br>
        <input type="checkbox" id="whatsapp" />
        <label for="whatsapp">Whatsapp</label>
      </div>
      <div class="form">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
        <p>Sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>
        <p>Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris.</p>
      </div>
      <div class="button">
        <button type="submit">Continuar</button>
      </div>
    </form>
    </div>
      <div class="image">
        <img src="../assets/Fer.png" alt="Fernanda" />
      </div>
  </section>
</template>

<script>
export default {
  name: "FormuLario",
};
  
  function mascara_cpf () {
    var cpf = document.getElementById('cpf')
    if(cpf.value.length == 3 || cpf.value.length == 7) {
      cpf.value += "."
    } else if(cpf.value.length == 11) {
      cpf.value += "-"
    }
};
</script>

<style scoped>
.bar {
  background-color: #e02b57;
  padding: 10px;
  align-items: center;
}

h3 {
  font-weight: bold;
  color: white;
}

.container {
  display: flex;
  /* flex-direction: row-reverse; */
  justify-content: space-between;
}

img {
  width: 500px;
}

.image {
  border: solid black 2px;
}

.form {
  border: solid black 2px;
  text-align: left;
  /* margin-left: 100px; */
}

.input-box {
  margin-bottom: 10px;
  padding-bottom: 20px;
  position: relative;
}

.input-box label {
  margin-bottom: 5px;
}

.input-box input {
  border: 2px solid;
  display: block;
  border-radius: 5px;
  font-size: 15px;
  width: 50%;
  padding: 10px;
}

.material-icons {
  position: relative;
}

/* .input-box small {
  position: absolute;
  visibility: hidden;
} */

button {
  background-color: #e02b57;
  border: none;
  border-radius: 50px;
  color: white;
  padding: 10px;
  font-weight: bold;
}
</style>
