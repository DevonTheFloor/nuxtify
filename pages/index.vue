<template>
  <div>
    <v-row>
      <v-col cols="12" sm="12">
        <Navbar />
      </v-col>
    </v-row>
    <v-row justify="center" align="center">
      <v-col cols="12" sm="8" md="6">
        <v-card-actions>
          <v-btn color="success" @click="seeFormLogin">
            Se Connecter
          </v-btn>
          <v-spacer />
          <v-btn color="info" @click="seeFormSignup">
            S'Enregistrer
          </v-btn>
        </v-card-actions>
        <v-card v-show="seeLogin">
          <v-card-title>
            <h1 class="display-1">
              Se Connecter
            </h1>
            <v-card-text>
              <v-form>
                <v-text-field
                  label="Username"
                  prepend-icon="mdi-account-circle"
                  :rules="[rules.username.regex]"
                />
                <v-text-field
                  label="Password"
                  :type="showPassWord ? 'text':'password'"
                  prepend-icon="mdi-lock"
                  :rules="[rules.password.regex]"
                  :append-icon="showPassWord ? 'mdi-eye' : 'mdi-eye-off'"
                  @click:append="showPassWord = !showPassWord"
                />
                <v-text-field
                  label="Email"
                  prepend-icon="mdi-at"
                  :rules="[rules.email.regex]"
                />
                <v-divider />
                <v-card-actions>
                  <v-btn color="success">
                    Envoyer
                  </v-btn>
                  <v-spacer />
                  <v-btn
                    type="reset"
                    color="danger"
                  >
                    Annuler
                  </v-btn>
                </v-card-actions>
              </v-form>
            </v-card-text>
          </v-card-title>
        </v-card>
        <v-card v-show="seeSignup">
          <v-card-title>
            <h1 class="display-1">
              S'Enregistrer
            </h1>
            <v-card-text>
              <v-form>
                <v-text-field
                  label="Username"
                  prepend-icon="mdi-account-circle"
                  :rules="[rules.username.regex]"
                />
                <v-text-field
                  label="Password"
                  :type="showPassWord ? 'text':'password'"
                  prepend-icon="mdi-lock"
                  :rules="[rules.password.regex]"
                  :append-icon="showPassWord ? 'mdi-eye' : 'mdi-eye-off'"
                  @click:append="showPassWord = !showPassWord"
                />
                <v-text-field
                  label="Email"
                  prepend-icon="mdi-at"
                  :rules="[rules.email.regex]"
                />
                <v-divider />
                <v-card-actions>
                  <v-btn color="success">
                    Envoyer
                  </v-btn>
                  <v-spacer />
                  <v-btn
                    type="reset"
                    color="danger"
                  >
                    Annuler
                  </v-btn>
                </v-card-actions>
              </v-form>
            </v-card-text>
          </v-card-title>
        </v-card>
      </v-col>
    </v-row>
  </div>
</template>

<script>

export default {
  data () {
    return {
      seeLogin: true,
      seeSignup: false,
      showPassWord: false,
      rules: {
        username: {
          regex: v => /^[aA-Zz]\d{5,25}$/.test(v) || 'Doit contenir entre 5 et 20 caractères'
        },
        email: {
          required: v => !!v || 'Obligatoire',
          regex: v => /^\w+([.-]?\w+)*@\w+([.-]?\w+)*(\.\w{2,3})+$/.test(v) || 'E-mail must be valid'
        },
        password: {
          require: v => !!v || 'Obligatoire',
          regex: v => /^(?=.*[A-Z])(?=.*[a-z])(?=.*\d)(?=.*[-+!*$@%_])([-+!*$@%_\w]{12,20})$/.test(v) || 'Entre 12 et 20 caractères,au moins une majuscule, un chiffre, un caractère spécial'
        }
      }
    }
  },
  methods: {
    seeFormSignup () {
      this.seeLogin = false
      this.seeSignup = true
    },
    seeFormLogin () {
      this.seeSignup = false
      this.seeLogin = true
    }
  }
}
</script>
