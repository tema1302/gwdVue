<template>
  <div class="wrapper">
    <Header />
    <content id="content">
      <MaintenancePopup />
      <main id="main" class="container login">
        <LoginForm />
        <About />
        <LoginTopics />
      </main>
    </content>
    <Footer />
  </div>
</template>

<script setup>
import Header from './components/Header.vue';
import LoginForm from './components/LoginForm.vue';
import About from './components/About.vue';
import LoginTopics from './components/LoginTopics.vue';
import Footer from './components/Footer.vue';
import MaintenancePopup from './components/MaintenancePopup.vue';
</script>
