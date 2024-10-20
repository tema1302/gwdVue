<template>
  <header class="header">
    <div class="container">
      <div class="top-content">
        <div class="top-logo">
          <a href="https://lk.gwd.ru/" title="Личный кабинет  «ГУД ВУД»">
            <svg class="header__logo"></svg>
          </a>
        </div>
        <div class="header__aside" :class="{ 'show_aside': isAsideVisible }">
          <nav id="navbar-top-bg" class="navbar-top-bg">
            <ul id="menu_accordion" class="aside-mobile-menu">
              <li class="aside-mobile-menu__login">
                <a class="btn btn-orange" href="https://lk.gwd.ru/#login-app" id="show-form">Войти в личный кабинет</a>
              </li>
              <li class="login">
                <a href="https://lk.gwd.ru/#about">О работе ЛК</a>
              </li>
              <li class="login gwd_url" style="text-align: center;">
                <a href="https://www.gwd.ru/" class="menu__gwd-link" style="text-decoration: underline; border: none; color: white;">На сайт компании gwd.ru</a>
              </li>
            </ul>
          </nav>
        </div>
        <div class="top_menu_burger hidden-ms hidden-lg" @click="toggleMenu">
          <svg :class="{active: !isMenuOpen}" class="modal_burger" width="44" height="44" viewBox="0 0 44 44" fill="none" xmlns="http://www.w3.org/2000/svg">
            <path fill-rule="evenodd" clip-rule="evenodd" d="M36 13H8V11H36V13ZM36 23H8V21H36V23ZM36 33H8V31H36V33Z" fill="white"></path>
          </svg>
          <svg :class="{active: isMenuOpen}" class="modal_close" width="44" height="44" viewBox="0 0 44 44" fill="none" xmlns="http://www.w3.org/2000/svg">
            <path fill-rule="evenodd" clip-rule="evenodd" d="M23.4135 22L33 12.4135L31.5865 11L21.9999 20.5865L12.4135 11.0002L11 12.4137L20.5864 22L11 31.5863L12.4136 32.9998L21.9999 23.4136L31.5864 33L33 31.5865L23.4135 22Z" fill="white"></path>
          </svg>
        </div>
      </div>
    </div>
  </header>
</template>

<script setup>
import { ref } from 'vue';
const isMenuOpen = ref(false);
const isAsideVisible = ref(false);

const toggleMenu = () => {
  isMenuOpen.value = !isMenuOpen.value;
  isAsideVisible.value = !isAsideVisible.value;
};
</script>
