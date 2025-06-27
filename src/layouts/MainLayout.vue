<template>
  <q-layout view="lHh Lpr lFf" class="text-white">
    <q-header elevated class="bg-black text-white">
      <q-toolbar class="q-py-md q-px-lg">
        <!-- Name on the left -->
        <q-toolbar-title class="text-h6 text-sm-h5 text-md-h4 text-weight-bold font-poppins tracking-tight">
          Cong Ha
        </q-toolbar-title>


        <!-- Social media links on the right (email moved to Contact section) -->
        <div class="row q-gutter-md">
          <q-btn
            flat
            round
            icon="fab fa-linkedin"
            color="white"
            size="md"
            href="https://linkedin.com/in/congcha"
            target="_blank"
            class="social-btn"
          />
          <q-btn
            flat
            round
            icon="fab fa-github"
            color="white"
            size="md"
            href="https://github.com/Cong-Ha"
            target="_blank"
            class="social-btn"
          />
        </div>
      </q-toolbar>
    </q-header>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script setup>
</script>

<style scoped>
.social-btn {
  transition: all 0.3s ease;
}

.social-btn:hover {
  background-color: rgba(255, 255, 255, 0.1);
  transform: translateY(-2px);
}
</style>
