<template>
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
    </v-col>
  </v-row>
</template>
