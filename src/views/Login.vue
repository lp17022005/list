 <template>
  <v-container fill-height fluid text-center>
    <v-container>
      <v-row>
        <v-col
          class="success--text text-center mx-auto pb-4"
          cols="1"
          sm="4"
          offset="4"
        >
          <h1 class="h1">Login</h1>
        </v-col>
      </v-row>
      <v-row class="elevation-3 mx-auto">
        <v-clo clos="auto">
          <v-img
            mx-height="150"
            max-width="250"
            src="@/assets/images/firebase_logo.png"
          ></v-img>
        </v-clo>
        <v-col>
          <v-form>
            <v-text-field label="Email" v-model="user.email"></v-text-field>
            <v-text-field
              label="Senha"
              v-model="user.password"
              :type="show ? 'text' : 'password'"
              :append-icon="show ? 'mdi-eye' : 'mdi-eye-off'"
              @click:append="show = !show"
            ></v-text-field>
            <v-btn color="success" @click="login">login</v-btn>
            <v-btn class="ml-2" color="warning" @click="reset">cancelar</v-btn>
          </v-form>
        </v-col>
      </v-row>
    </v-container>
    <v-snackbar color="red" v-model="errorLogin" danger multline timeout="2000">
      Usuário ou senha inválidos
    </v-snackbar>
  </v-container>
</template>
 
 <script>
export default {
  data() {
    return {
      user: {},
      show: false,
      errorLogin: false,
    };
  },
  methods: {
    reset() {
      this.user = {};
    },
    login() {
      if (this.user.email === "leticia" && this.user.password === "leticia") {
        this.$router.push({ name: "Home" });
      } else {
        this.errorLogin = true;
      }
    },
  },
};
</script>
 
 <style>
</style>