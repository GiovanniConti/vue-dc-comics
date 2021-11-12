<template>
  <header class="containerHeader">
    <div class="nav">
      <img src="../assets/dc-logo.png" alt="dc-logo" class="logoHeader">
      <ul class="navHeader">
        <li 
          class="navHeader_item"
          v-for="(item, i) in navbarItem"
          :key="i"
        >
          <a
            :href="item.href" class="navHeader_item_link" 
            :class="(i === activeItem) ? 'navHeader_item_link-selected' : '' "
          >
            {{item.title}}
          </a>
        </li>
      </ul>
    </div>

  </header>
</template>

<script>
export default {
  name: 'Header',
  props: { },
  data() {
    return {
      navbarItem: [
        {
          title: 'CHARACTERS',
          href: "#",
        },
        {
          title: 'COMICS',
          href: "#",
        },
        {
          title: 'MOVIES',
          href: "#",
        },
        {
          title: 'TV',
          href: "#",
        },
        {
          title: 'GAMES',
          href: "#",
        },
        {
          title: 'COLLECTIBLES',
          href: "#",
        },
        {
          title: 'VIDEOS',
          href: "#",
        },
        {
          title: 'FANS',
          href: "#",
        },
        {
          title: 'NEWS',
          href: "#",
        },
        {
          title: 'SHOP',
          href: "#",
        },
      ],
      activeItem: 0,
    };
  },
}
</script>

<style lang="scss">
@import "../styles/variables.scss";

.containerHeader{
  .nav{
    max-width: $container_width;
    margin: auto;
    display: $display_flex;
    justify-content: $flex_space_between;
    align-items: center;
    
    .logoHeader{
      width: 70px;
      padding: 10px 0;
    }
  
    .navHeader{
      display: $display_flex;
      justify-content: space-evenly;
      list-style: none;
      padding: $padding-Y;
  
      .navHeader_item{
        
        .navHeader_item_link{
          text-decoration: none;
          color: black;
          font-size: 12px;
          font-weight: bold;
          margin: 0 15px;
        
          &:hover{
            color: $color_primary;
          }
          
        }
        .navHeader_item_link-selected{
          color: $color_primary;
          border-bottom: 4px solid $color_primary;
          padding-bottom: 45px;
        }
        
      }
    }

  }

}

</style>