<template>
  <v-footer app color="primary" dark>
    <v-container>
      <v-row justify="center">
        <!-- Sociale medier ikoner -->
        <v-col cols="12" class="text-center">
          <v-btn icon class="mx-2" href="https://github.com/Shahad1991" target="_blank">
            <v-img src="../images/github.svg.svg" alt="GitHub" max-width="30"></v-img>
          </v-btn>
          <v-btn icon class="mx-2" href="https://www.instagram.com/shahadnazaromhassoni/" target="_blank">
            <v-img src="../images/Vector.svg" alt="Instagram" max-width="30"></v-img>
          </v-btn>
          <v-btn icon class="mx-2" href="https://www.linkedin.com/in/shahad-al-jawashee-41502a24b/" target="_blank">
            <v-img src="../images/linkdin.svg" alt="LinkedIn" max-width="30"></v-img>
          </v-btn>
        </v-col>
      </v-row>

      <!-- Navigationsmenu -->
      <v-row justify="center">
        <v-col cols="12" class="text-center">
          <v-btn text color="white" href="#hero-image">Hjem</v-btn>
          <v-btn text color="white" href="#om-mig">Om</v-btn>
          <v-btn text color="white" href="#projekter">Projekter</v-btn>
          <v-btn text color="white" href="#contact">Kontakt</v-btn>
        </v-col>
      </v-row>

      <!-- Copyright tekst -->
      <v-row justify="center">
        <v-col cols="12" class="text-center">
          <p class="mb-0">&copy; 2024 Shahad. All rights reserved.</p>
        </v-col>
      </v-row>
    </v-container>
  </v-footer>
</template>

<script>
export default {
  name: 'Footer',
};
</script>

<style scoped>
.v-footer {
  padding: 20px;
}
</style>
