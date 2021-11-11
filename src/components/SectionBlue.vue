<template>
  <section class="sectionBlue">
    <div class="containerBlue">
    <ul class="containerBlue_list">
      <li
        class="containerBlue_list_item"
        v-for="(item, i) in blueList"
        :key="i"
      >
        <img src='../assets/buy-comics-digital-comics.png' :alt="item.text">
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
          icon: '../assets/buy-comics-digital-comics.png',
          text: 'DIGITAL COMICS',
        },
        {
          icon: '../assets/buy-comics-merchandise.png',
          text: 'DC MERCHANDISE',
        },
        {
          icon: '../assets/buy-comics-subscriptions.png',
          text: 'SUBSCRIPTIONS',
        },
        {
          icon: '../assets/buy-comics-shop-locator.png',
          text: 'COMIC SHOP LOCATOR',
        },
        {
          icon: '../assets/buy-dc-power-visa.svg',
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

  .containerBlue{
    max-width: $container_width;
    padding: $padding-Y;
    margin: auto;

    .containerBlue_list{
      display: flex;
      justify-content: space-evenly;
      list-style: none;

      .containerBlue_list_item{
        display: flex;
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