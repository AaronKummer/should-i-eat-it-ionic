
<template>
  <ion-app>
    <ion-grid v-if="!loggedIn">
      <ion-row class="ion-justify-content-center">
        <!-- <img class="grocs" src="./assets/groceries.jpg"> -->
        <ion-col size="12">
          <h1 style="text-align:center; font-size: 38px;">Grocery Helper</h1>
          <br><hr>
        </ion-col>
      </ion-row>
      <ion-row>
        <ion-col>
          <ion-item color="secondary">
            <ion-label>E-mail: </ion-label>
            <ion-input v-model="email"></ion-input>
          </ion-item>
        </ion-col>
        <ion-col>
          <ion-item color="secondary">
            <ion-label>Password: </ion-label>
            <ion-input v-model="password"></ion-input>
          </ion-item>
        </ion-col>
      </ion-row>
      <ion-row class="ion-justify-content-end">
        <ion-button color="secondary" @click="login"
          >Login</ion-button
        >
      </ion-row>
    </ion-grid>

    <ion-router-outlet v-if="loggedIn" />
  </ion-app>
</template>

<script lang="ts">
import { IonApp, IonRouterOutlet } from "@ionic/vue";
import { defineComponent } from "vue";

export default defineComponent({
  name: "App",
  components: {
    IonApp,
    IonRouterOutlet,
  },
  data: function () {
    return {
      loggedIn: false,
      email: "",
      password: "",
    };
  },
  methods: {
    login() {
      this.loggedIn = !this.loggedIn;
    },
  },
});
</script>

<style>
.grocs {
  width: 20% !important;
  margin-left: 40%;
}
@media (prefers-color-scheme: dark) {
  :root {
    /* dark mode variables go here */
  }
}
ion-input {
  /* background-color: white !important; */
}
</style>