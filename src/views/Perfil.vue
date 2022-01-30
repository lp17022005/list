<template>
  <v-containe class="pa-8" fluid>
    <h1 class="h1">Meu perfil</h1>
    <v-form>
      <v-container>
        <v-text-field label="Nome" v-model="nome"> </v-text-field>
        <v-text-field label="Sobrenome" v-model="sobrenome"> </v-text-field>
        <v-btn color="success">Salvar</v-btn>
      </v-container>
    </v-form>
  </v-containe>
</template>

<script>
export default {
  data() {
    return {
      nome: "",
      sobrenome: "",
    };
  },
};
</script>

<style>
</style>