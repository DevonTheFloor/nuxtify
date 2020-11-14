<template>
  <v-row justify="center" align="center">
    <v-col cols="12" sm="8" md="6">
      <v-card>
        <v-card-title>
          <h1 class="display-1">
            Login
          </h1>
          <v-card-text>
            <v-form>
              <v-text-field
                label="Username"
                prepend-icon="mdi-account-circle"
              />
              <v-text-field
                label="Password"
                :type="showPassWord ? 'text':'password'"
                prepend-icon="mdi-lock"
                :append-icon="showPassWord ? 'mdi-eye' : 'mdi-eye-off'"
                @click:append="showPassWord = !showPassWord"
              />
              <v-divider />
              <v-card-actions>
                <v-btn color="success">
                  Register
                </v-btn>
                <v-spacer />
                <v-btn color="info">
                  Login
                </v-btn>
              </v-card-actions>
            </v-form>
          </v-card-text>
        </v-card-title>
      </v-card>
    </v-col>
  </v-row>
</template>

<script>

export default {
  data () {
    return {
      showPassWord: false
    }
  }
}
</script>
