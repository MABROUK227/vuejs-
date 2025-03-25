<template>
  <v-card width="100%" max-width="400" elevation="0" class="pl-8">
    <div class="text-h5 font-weight-black text-uppercase text-center">Connexion</div>
    <v-divider class="my-5"></v-divider>

    <div class="text-subtitle-1 text-medium-emphasis mt-8">Adresse e-mail</div>
    <v-text-field prepend-inner-icon="mdi-email" class="mt-3"></v-text-field>

    <div
      class="text-subtitle-1 text-medium-emphasis d-flex align-center justify-space-between"
    >
      Mot de passe

      <a
        class="text-caption text-subtitle-2 font-weight-medium text-decoration-none primary-color"
        href="#"
      >
        Mot de passe oublié ?</a
      >
    </div>
    <v-text-field
      type="password"
      prepend-inner-icon="mdi-lock"
      class="mt-3"
    ></v-text-field>
    <v-card-text class="d-none text-medium-emphasis text-caption pa-2 assh-bg-color">
      Attention : Après 3 tentatives de connexion échouées consécutives,
    </v-card-text>

    <v-btn color="primary" class="mt-5" size="large" variant="tonal" block>
      Se connecter
    </v-btn>
    <div
      class="text-subtitle-2 mt-5 text-center font-weight-medium text-decoration-none"
      href="#"
    >
      <span class="cursor-pointer" @click="$router.push('/authentication/signup')"
        >Vous n'avez pas de compte ? INSCRIVEZ-VOUS maintenant</span
      >
    </div>
  </v-card>
</template>

<script setup></script>

<style scoped lang="scss"></style>
