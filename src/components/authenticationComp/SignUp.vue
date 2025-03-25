<template>
  <v-card width="100%" max-width="400" elevation="0" class="pl-8">
    <div class="text-h5 font-weight-black text-uppercase text-center">Inscription</div>
    <v-divider class="my-5"></v-divider>
    <div class="text-subtitle-1 text-medium-emphasis mt-8">Nom complet</div>
    <v-text-field prepend-inner-icon="mdi-account" class="mt-3"></v-text-field>

    <div class="text-subtitle-1 text-medium-emphasis">Adresse e-mail</div>
    <v-text-field type="email" prepend-inner-icon="mdi-email" class="mt-3"></v-text-field>

    <div
      class="text-subtitle-1 text-medium-emphasis d-flex align-center justify-space-between"
    >
      Mot de passe
    </div>
    <v-text-field
      type="password"
      prepend-inner-icon="mdi-lock"
      class="mt-3"
      placeholder="6+ caractères"
    ></v-text-field>

    <v-card-text class="d-none text-medium-emphasis text-caption pa-2 assh-bg-color">
      Attention : Après 3 tentatives de connexion échouées consécutives,
    </v-card-text>

    <div class="d-flex align-center">
      <v-checkbox
        class="shrink mr-0 mt-0"
        color="primary"
        hide-details
        density="compact"
        size="small"
      ></v-checkbox>
      <span class="text-subtitle-2 font-weight-regular text-medium-emphasis ml-4">
        J'accepte les conditions d'utilisation d'Auros.</span
      >
    </div>

    <v-btn color="primary" class="mt-5" size="large" variant="tonal" block>
      Créer un compte
    </v-btn>
    <div
      class="text-subtitle-2 mt-5 text-center font-weight-medium text-decoration-none"
      href="#"
    >
      <span class="cursor-pointer" @click="$router.push('/authentication/signin')"
        >Vous avez déjà un compte ? CONNECTEZ-VOUS</span
      >
    </div>
  </v-card>
</template>

<script setup></script>

<style scoped lang="scss"></style>
