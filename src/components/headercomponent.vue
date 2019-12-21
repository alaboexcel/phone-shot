<template>
  <nav xs12 sm12 md12 app class>
    <v-app-bar class="grey white--text font-weight-bold">
      <span>Phone Shot</span>
      <v-spacer></v-spacer>
      <v-btn depressed class="pink lighten-4 white--text">
        <span>Contribute</span>
      </v-btn>

      <v-row justify="center">
        <v-dialog v-model="dialog1" persistent max-width="500">
          <template v-slot:activator="{ on }">
            <v-btn class="pink lighten-4 white--text" depressed v-on="on">Sign up</v-btn>
          </template>
          <v-card align="center">
            <v-col cols="12" sm="6" md="10">
              <v-text-field label="Name" outlined dense color="pink lighten-4"></v-text-field>
            </v-col>
            <v-col cols="12" sm="6" md="10">
              <v-text-field label="Email" outlined dense color="pink lighten-4"></v-text-field>
            </v-col>
            <v-col cols="12" sm="6" md="10">
              <v-text-field label="Phone Number" outlined dense color="pink lighten-4"></v-text-field>
            </v-col>
            <v-col cols="12" sm="6" md="10">
              <v-text-field label="Password" outlined dense color="pink lighten-4"></v-text-field>
            </v-col>
            <v-card-actions>
              <v-dialog v-model="dialog2" persistent max-width="350">
                <template v-slot:activator="{ on }">
                  <v-btn class="pink lighten-4 white--text" depressed v-on="on">Login</v-btn>
                </template>
                <v-card align="center">
                  <v-col cols="12" sm="6" md="10">
                    <v-text-field label="Name" outlined dense color="pink lighten-4"></v-text-field>
                  </v-col>
                  <v-col cols="12" sm="6" md="10">
                    <v-text-field label="Email" outlined dense color="pink lighten-4"></v-text-field>
                  </v-col>
                  <v-col cols="12" sm="6" md="10">
                    <v-text-field label="Password" outlined dense color="pink lighten-4"></v-text-field>
                  </v-col>
                   <span>Forgot password?</span><br>
                  <v-btn color="pink darken-1" text @click="dialog2 = false">Send</v-btn>
                </v-card>
              </v-dialog>
              <v-spacer></v-spacer>
              <v-btn color="pink darken-1" text @click="dialog1 = false">Close</v-btn>
              <v-btn color="pink darken-1" text @click="dialog1 = false">Send</v-btn>
            </v-card-actions>
          </v-card>
        </v-dialog>
      </v-row>
    </v-app-bar>
  </nav>
</template>

<script>
export default {
  name: "headercomponent",

  data: () => ({ dialog1: false, dialog2: false })
};
</script>

