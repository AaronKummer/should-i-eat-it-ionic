
<template>
  <ion-app>
    <ion-grid class="app" v-if="!loggedIn">
      <ion-row>
        <img class="grocs" src="./assets/groceries.jpg">
      </ion-row>
      <ion-row>
        <ion-col>
          <ion-item color="secondary">
            <ion-label>E-mail: </ion-label> <ion-input v-model="email"></ion-input>
          </ion-item>
        </ion-col>
        <ion-col>
          <ion-item color="secondary">
            <ion-label>Password: </ion-label> <ion-input v-model="password"></ion-input>
          </ion-item>
        </ion-col>
      </ion-row>
      <ion-row>
        <ion-button style="margin-left:90%" color="secondary" @click="login">Login</ion-button>
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
      email: '',
      password: ''
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
.app {
  background-color: white;
}
.grocs {
  width: 20% !important;
  margin-left: 40%;
}
@media (prefers-color-scheme: light) {
  :root {
    /* dark mode variables go here */
  }
}
ion-input{
 /* background-color: white !important; */
}
</style>