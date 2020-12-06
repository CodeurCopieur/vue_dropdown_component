<template>
  <nav>
    <ul class="menu-list-item">
      <li class="menu-item">
        <a href="#">Home</a>
      </li>
      <li class="menu-item">
        <a href="#">About</a>
      </li>
      <dropdown title="Services" :items="services" />
      <li class="menu-item">
        <a href="#">Contact</a>
      </li>
    </ul>
  </nav>
</template>

<script>

import dropdown from './Dropdown.vue'

 export default {
   name: 'navbar',
   components: {
     dropdown
   },
   data: () => {
     return {
       Services: [ 
         {
          title: 'VUE JS',
          link: '#'
         },
         {
          title: 'SCSS',
          link: '#'
         },
         {
          title: 'JS',
          link: '#'
         }
       ]
     }
   }
  }
</script>

<style lang="scss">
  nav {
    border: 3px solid #fff;
    padding: 15px;

    .menu-list-item {
      display: flex;
      justify-content: center;
      align-items: center;

      .menu-item {
        
        position: relative;
        padding: 10px 20px;
        border-bottom: 3px solid transparent;
        cursor: pointer;
        transition: all .5s ease-out;

        &.active,
        &:hover{
          background-color: #fff;
          border-bottom-color: #FF5858;
        }

        &:hover a {
          color: #000;
        }

        a {
          color: #fff;
          background: transparent;
          transition: all .5s ease-out;
        }
      }
    }
  }
</style>