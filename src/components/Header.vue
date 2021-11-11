<template>
  <header class="containerHeader">
    <img src="../assets/dc-logo.png" alt="dc-logo" class="logoHeader">
    <ul class="navHeader">
      <li 
      class="navHeader_item"
      v-for="(item, i) in navbarItem"
      :key="i"
      >
        <a :href="item.href" class="navHeader_item_link">{{item.title}}</a>
      </li>
    </ul>
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
    };
  },
}
</script>

<style lang="scss">
@import "../styles/variables.scss";

.containerHeader{
  display: $display_flex;
  justify-content: $flex_space_between;
  align-items: center;
  padding: $padding-Y;
  
  .logoHeader{
    width: 87px;
  }

  .navHeader{
    display: $display_flex;
    justify-content: space-evenly;
    list-style: none;

    .navHeader_item{
      
      .navHeader_item_link{
        text-decoration: none;
        color: black;
        font-size: 12px;
        font-weight: bold;
        margin: 0 15px;
      
        &:hover{
          color: $color_secondary;
        }
        
      }
      .navHeader_item_link-selected{
        border-bottom: 4px solid $color_secondary;
        padding-bottom: 45px;
      }
      
    }
  }
}

</style>