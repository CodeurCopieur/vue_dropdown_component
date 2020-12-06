<template>
  <nav>
    <ul class="menu-list-item">
      <li class="menu-item">
        <a href="#">Home</a>
      </li>
      <li class="menu-item">
        <a href="#">About</a>
      </li>
      <li class="menu-item">
        <a href="#">Contact</a>
      </li>
    </ul>
  </nav>
</template>

<script>
 export default {
   name: 'Navbar',
   data: () => {
     return {}
   }
  }
</script>

<style lang="scss" scoped>
  nav {

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