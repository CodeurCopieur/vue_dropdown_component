<template>
  <nav>
    <ul class="menu-list-item">
      <li class="menu-item">
        <a href="#">Home</a>
      </li>
      <li class="menu-item">
        <a href="#">About</a>
      </li>
      <dropdown title="Services" :items="Services" />
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
          title: 'SCSS',
          link: '#'
         },
         {
          title: 'JS',
          link: '#'
         },
         {
          title: 'VUE JS',
          link: '#'
         }
       ]
     }
   }
  }
</script>

<style lang="scss">
  nav {
    background-color: #000;
    padding: 15px;

    .menu-list-item {
      display: flex;
      justify-content: center;
      align-items: center;

      .menu-item {
        
        position: relative;
        color: #fff;
        padding: 10px 20px;
        border-bottom: 3px solid transparent;
        cursor: pointer;
        transition: all .5s ease-out;

        &.active,
        &:hover{
          background-color: #444;
          border-bottom-color: #FF5858;
        }

        a {
          color: inherit;
        }

        
        .sub-menu {
          position: absolute;
          background-color: #222;
          top: calc(100% + 18px);
          left: 50%;
          transform: translateX(-50%);
          width: max-content;
        }
      }
    }
  }
</style>