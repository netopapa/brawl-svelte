<style>
  section {
    height: calc(100vh - 70px);
    display: flex;
    justify-content: center;
    align-items: center;
  }

  .card {
    width: 700px;
    background-color: #fff;
    border-radius: 5px;
    box-shadow: 4px 4px 6px #8e8e8e;
  }

  form {
    width: 80%;
    padding: 10px 10%;
  }

  input {
    outline: 0;
    border: 0;
    border-bottom: 1px solid #8e8e8e;
    border-radius: 0;
    transition: border .2s linear;
  }

  input:focus {
    border-bottom: 2px solid #8e8e8e;
  }

  .half {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  .form-control {
    display: flex;
    flex-direction: column;
    justify-content: start;
    align-items: flex-start;
  }

  textarea {
    width: 100%;
    height: 100px;
    resize: none;
  }
</style>

<section>

  <div class="card">
    <form>
      <h1 class="center">Fale Conosco</h1>
      <div class="half">
        <div class="form-control">
          <label>Nome:</label>
          <input type="text" />
        </div>

        <div class="form-control">
          <label>Sobrenome:</label>
          <input type="text" />
        </div>
      </div>

      <div class="half">
        <div class="form-control">
          <label>E-mail:</label>
          <input type="email" />
        </div>

        <div class="form-control">
          <label>Telefone:</label>
          <input type="text" />
        </div>
      </div>

      <textarea placeholder="Conte sua história..." />
    </form>
  </div>
</section>
