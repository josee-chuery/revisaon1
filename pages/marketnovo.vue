<template>
  <section class="section">
    <h1 class="title">Novo Classificado</h1>
    <div class="box">
      <p>Novo Produto</p>
      <br>
      <b-field>
        <b-input placeholder="Nome do produto"></b-input>
      </b-field>
    </div>
    <div class="box">
      <p>Valor</p>
      <br>
      <b-field>
        <b-input placeholder="ex. R$ 00,00"></b-input>
      </b-field>
    </div>
    <div class="box">
      <p>Descrição</p>
      <br>
      <b-field>
        <b-input maxlength="500" type="textarea"></b-input>
      </b-field>
    </div>
    <div class="columns">
      <div class="column is-6">
        <b-field label="Data de Publicação">
            <b-datepicker
                placeholder="Clique para selecionar..."
                :min-date="minDate"
                :max-date="maxDate">
            </b-datepicker>
        </b-field>
      </div>
      <div class="column is-6">
        <b-field label="Data de Validade">
            <b-datepicker
                placeholder="Clique para selecionar..."
                :min-date="minDate"
                :max-date="maxDate">
            </b-datepicker>
        </b-field>
      </div>
    </div>
    <button class="button is-success">Salvar</button>
    <button class="button is-danger">Cancelar</button>

  </section>
</template>
<script>
    export default {
        data() {
            const today = new Date()

            return {
                date: new Date(),
                minDate: new Date(today.getFullYear() - 80, today.getMonth(), today.getDate()),
                maxDate: new Date(today.getFullYear() + 18, today.getMonth(), today.getDate())
            }
        }
    }
</script>
