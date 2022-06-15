<template>
  <head>
    <meta name="viewport" content="width=device-width, initial-scale=1" />
    <link
      href="https://fonts.googleapis.com/icon?family=Material+Icons"
      rel="stylesheet"
    />
  </head>

  <form>
    <div class="count">
      <ul class="progressbar">
        <li class="active">Passo 1</li>
        <li>Passo 2</li>
        <li>Passo 3</li>
      </ul>
    </div>

    <h1>Seja Bem Vindo</h1>
    <p><strong>Dados de Contato</strong></p>
    <p>Abra sua conta em 2 minutos. É grátis!</p>

    <fieldset class="name">
      <legend>Nome Completo</legend>
      <input type="text" id="name" name="name" placeholder="Digite">
      <label for="name"></label>
    </fieldset><br>

    <fieldset class="email">
      <legend>E-mail</legend>
      <i class="material-icons">&#xe0be;</i>
      <input type="email" id="email" name="email" placeholder="Digite">
      <label for="email"></label>
    </fieldset>

    <fieldset class="email">
      <legend>Confirme E-mail</legend>
      <i class="material-icons">&#xe0be;</i>
      <input type="email" id="email" name="email" placeholder="Digite">
      <label for="email"></label>
    </fieldset><br/>

    <fieldset class="cpf">
      <legend>Cpf</legend>
      <input type="text" id="cpf" name="cpf" placeholder="000.000.000-00" maxlength="14">
      <label for="cpf"></label>
    </fieldset>

    <fieldset class="celular">
      <legend>Celular</legend>
      <input type="tel" id="tel" name="celular" placeholder="(00)00000-0000" maxlength="14">
      <label for="tel"></label>
    </fieldset>

    <!-- <div class="email">

      <label for="birthday">Data de Nascimento</label>
      <input type="date" id="birthday" /><br /><br />

      <p>
        <strong
          >Lorem ipsum dolor sit amet, consectetur adipiscing elit.</strong
        >
      </p>
      <p>
        <strong
          >Sed do eiusmod tempor incididunt ut labore et dolore magna
          aliqua.</strong
        >
      </p>
      <br />

      <input type="checkbox" id="email" />
      <label for="email">E-mail e SMS</label>
      <br />
      <br />
      <input type="checkbox" id="whatsapp" />
      <label for="whatsapp">Whatsapp</label><br />

      <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
      <p>Sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>
      <p>Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris.</p>

      <button type="submit">Continuar</button> -->
  </form>
</template>

<script>
export default {
  name: "FormuLario",
};

function mascara_cpf() {
  var cpf = document.getElementById("cpf");
  if (cpf.value.length == 3 || cpf.value.length == 7) {
    cpf.value += ".";
  } else if (cpf.value.length == 11) {
    cpf.value += "-";
  }
}
</script>

<style scoped>
form {
  border: solid black 1px;
  text-align: left;
  padding-right: 200px;
}

h1 {
  padding-top: 100px;
}

legend {
  font-size: 14px;
}

.name input {
  border: white;
  width: 500px;
  padding: 5px 10px 10px 50px;
}

fieldset.email {
  width: 250px;
}

.email input {
  border: white;
  width: 250px; 
  padding: 5px 10px 10px 50px;
}

.material-icons {
  position: absolute;
  display: flex;
  font-size: 20px;
  align-items: center;
  margin-left: 5px;
  margin-top: 5px;
}

.email {
  display: inline-block;
}

.cpf input {
  border: white;
  width: 250px; 
  padding: 5px 10px 10px 50px;
}

fieldset.cpf {
  width: 250px;
}

.celular input {
  border: white;
  width: 250px; 
  padding: 5px 10px 10px 50px;
}

fieldset.celular {
  width: 250px;
}

button {
  background-color: #e02b57;
  border: none;
  border-radius: 50px;
  color: white;
  padding: 10px;
  font-weight: bold;
}

.count {
  width: 100%;
}

.progressbar {
  counter-reset: step;
}

.progressbar li {
  list-style: none;
  float: left;
  width: 33.33%;
  position: relative;
  text-align: center;
}

.progressbar li:before {
  content: counter(step);
  counter-increment: step;
  width: 30px;
  height: 30px;
  line-height: 30px;
  border: 1px solid #ddd;
  display: block;
  text-align: center;
  margin: 0 auto 10px auto;
  border-radius: 50%;
  background-color: white;
}

.progressbar li:after {
  content: "";
  position: absolute;
  width: 100%;
  height: 1px;
  background-color: #ddd;
  top: 15px;
  left: -50%;
  z-index: -1;
}

.progressbar li:first-child:after {
  content: none;
}

.progressbar li.active {
  color: #e02b57;
}

.progressbar li.active:before {
  border-color: #e02b57;
}

.progressbar li.active + li:after {
  background-color: #e02b57;
}
</style>
