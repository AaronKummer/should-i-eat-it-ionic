<template>
  <ion-page>
    <ion-header>
      <ion-toolbar>
        <ion-title>Grocery database</ion-title>
      </ion-toolbar>
    </ion-header>
    <ion-content :fullscreen="true">
      <ion-header collapse="condense">
        <ion-toolbar>
          <ion-title size="large">Grocery database</ion-title>
        </ion-toolbar>
      </ion-header>
      Carrots - 1 lb <br>
      Salted Codfish - 50lbs <br>
      Olive oil - none <br>
      Butter - none <br>
      Whale penises - 10lb  <br>
    </ion-content>
  </ion-page>
</template>

<script lang="ts">
import { IonPage, IonHeader, IonToolbar, IonTitle, IonContent } from '@ionic/vue';

export default  {
  name: 'Tab3',
  components: { IonHeader, IonToolbar, IonTitle, IonContent, IonPage }
}
</script>
