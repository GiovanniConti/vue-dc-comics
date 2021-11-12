<template>
  <section class="sectionBlue">
    <div class="containerBlue">
    <ul class="containerBlue_list">
      <li
        class="containerBlue_list_item"
        v-for="(item, i) in blueList"
        :key="i"
      >
        <img :src='require( "@/assets/" + item.icon)' :alt="item.text">
        <h3>{{item.text}}</h3>
      </li>
    </ul>
    </div>
  </section>
</template>

<script>
export default {
  name: "SectionBlue",
  props: { },
  data() {
    return {
      blueList: [
        {
          icon: 'buy-comics-digital-comics.png',
          text: 'DIGITAL COMICS',
        },
        {
          icon: 'buy-comics-merchandise.png',
          text: 'DC MERCHANDISE',
        },
        {
          icon: 'buy-comics-subscriptions.png',
          text: 'SUBSCRIPTIONS',
        },
        {
          icon: 'buy-comics-shop-locator.png',
          text: 'COMIC SHOP LOCATOR',
        },
        {
          icon: 'buy-dc-power-visa.svg',
          text: 'DC POWER VISA',
        },
      ]
    };
  },
}
</script>

<style lang="scss">
@import "../styles/variables.scss";

.sectionBlue{
  background: $color_primary;
  padding: $padding-Y;

  .containerBlue{
    max-width: $container_width;
    margin: auto;

    .containerBlue_list{
      display: $display_flex;
      justify-content: space-evenly;
      list-style: none;

      .containerBlue_list_item{
        display: $display_flex;
        align-items: center;
        color: white;
        font-size: 12px;

        img {
          width: 50px;
        }
        h3 {
          padding: 0 10px;
        }

      }
    }
  }
}

</style>