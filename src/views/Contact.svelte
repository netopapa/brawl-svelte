<script>
  function check(input) {
    if (input.value != document.getElementById("email_addr").value) {
      input.setCustomValidity("The two email addresses must match.");
    } else {
      // input is valid -- reset the error message
      input.setCustomValidity("");
    }
  }
</script>

<style>
  :invalid {
    -moz-box-shadow: 0 0 5px rbba(255, 0, 0, 0.8);
    -o-box-shadow: 0 0 5px rbba(255, 0, 0, 0.8);
    -ms-box-shadow: 0 0 5px rbba(255, 0, 0, 0.8);
  }

  :required {
    border-color: #88a;
  }

  section {
    background-image: url("assets/brawl-stars.jpg");
    background-size: cover;
    background-repeat: no-repeat;
    background-position: 50% 100%;
    height: calc(100vh - 70px);
  }

  section h1 {
    margin: 0;
    padding-top: 15px;
  }

  form {
    background-color: #fff;
    width: 310px;
    height: auto;
    border-radius: 10px;
    padding: 30px 40px 30px 40px;
  }

  input {
    font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
    border: 1px solid #ccc;
    font-size: 20px;
    width: 310px;
    min-height: 30px;
    display: block;
    margin-bottom: 15px;
    margin-top: 10px;
    outline: none;

    -webkit-border-radius: 5px;
    -moz-border-radius: 5px;
    -o-border-radius: 5px;
    -ms-border-radius: 5px;
    border-radius: 5px;
  }

  textarea {
    font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
    border: 1px solid #ccc;
    font-size: 20px;
    width: 313px;
    margin-bottom: 15px;
    margin-top: 10px;
    resize: none;
  }

  input[type="submit"] {
    background: none;
    padding: 10px;
  }
</style>

<section class="centralizado">
  <form
    oninput="total.value = (nights.valueAsNumber * 99) + ((guests.valueAsNumber
    - 1) * 10)">

    <label>Nome Completo: *</label>
    <input
      type="text"
      id="full_name"
      name="full_name"
      placeholder="Nome"
      required />

    <label>E-mail: *</label>
    <input type="email" id="email_addr" name="email_addr" required />

    <label>Confirmação de e-mail: *</label>
    <input
      type="email"
      id="email_addr_repeat"
      name="email_addr_repeat"
      required
      oninput="check(this)" />

    <label>Data de nasciemnto: *</label>
    <input type="date" id="arrival_dt" name="arrival_dt" required />

    <label>Comentário: *</label>
    <textarea id="coment" name="coment" rows="5" maxlength="250" />

    <input type="submit" value="Enviar Comentário" />
  </form>
</section>
