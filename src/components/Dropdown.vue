<template>
 <li class="menu-item" @click="isOpen = !isOpen">
  <a href="#">{{ title }}</a>
  <svg viewBox="0 0 1030 638" width="10">
    <path d="M1017 68L541 626q-11 12-26 12t-26-12L13 68Q-3 49 6 24.5T39 0h952q24 0 33 24.5t-7 43.5z" fill="#FFF"></path>
  </svg>
  <transition name="fade" appear>
    <div class="sub-menu" v-if="isOpen">
      <li class="menu-item" v-for="(item, i) in items" :key="i">
        <a :href="item.link">{{ item.title }}</a>
      </li>
    </div>
  </transition>
 </li>
</template>

<script>
 export default {
   name: 'dropdown',
   props: ['title', 'items'],
   data: () => {
     return {
       isOpen: false
     }
   }
  }
</script>

<style lang="scss">

  .menu-item {
    &:hover  {
      svg {
        width: 10px;
        color: #000;
      }
    }
    svg {
      width: 10px;
      margin-left: 10px;
    }
  }

  .fade-enter-active,
  .fade-leave-active {
    transition: all .5s ease-out;
  }

  .fade-enter,
  .fade-leave-to {
    opacity: 0;
  }
</style>