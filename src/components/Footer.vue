<template>
  <footer>
    <div class="containerFooterTop">
      <div class="containerFooterLinks">
        <div class="containerFooterLinks_Lists">
          <ul class="containerFooterLinks_list"
          v-for="(list, i) in footerLinksList"
          :key="i"
          >
          <li
            v-for="(links, j) in list"
            :key="j"
            :class="(j === 0) ? 'list_link_title' : '' "
          >
            {{links}}
          </li>
          </ul>
        </div>

        <div class="containerFooterLinks_img">
          <img src="../assets/dc-logo-bg.png" alt="">
        </div>
      </div>
    </div>
    <div class="containerFooterBottom">
      
      <div class="containerFooterSocials">
      
      <button class="containerFooterSocials_btn">SIGN-UP NOW!</button>

      <ul class="containerFooterSocials_list">
        <li class="containerFooterSocials_list_item">FOLLOW US</li>
        <li class="containerFooterSocials_list_item"
          v-for="(icon, i) in socialsIconsList"
          :key="i"
        >
          <a href="#"><img :src="require('@/assets/footer-' + icon + '.png')" :alt="icon"></a>
        </li>
      </ul>

      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: 'Footer',
  props: { },
  data() {
    return {
      footerLinksList:[
        [
          "DC COMICS",
          "Characters",
          "Movies",
          "TV",
          "Games",
          "Video",
          "News"
        ],
        [
          "SHOP",
          "Shop DC",
          "Shop DC Collectibles"
        ],
        [
          "DC",
          "Terms Of Use",
          "Privacy policy (New)",
          "Ad Choices",
          "Advertising",
          "Jobs",
          "Subscriptions",
          "Talent Workshops",
          "CPSC Certificates",
          "Ratings",
          "Shop Help",
          "Contact Us"
        ],
        [
          "SITES",
          "DC",
          "MAD Magazine",
          "DC Kids",
          "DC Universe",
          "DC Power Visa"
        ],
      ],
      socialsIconsList: [
        "facebook",
        "twitter",
        "youtube",
        "pinterest",
        "periscope",
      ],
    };
  },
}
</script>

<style lang='scss'>
@import "../styles/variables.scss";

footer{
  
  .containerFooterTop{
    background-image: url('../assets/footer-bg.jpg');

    .containerFooterLinks{
      max-width: $container_width;
      max-height: 335px;
      margin: auto;
      display: $display_flex;
      justify-content: space-between;

      .containerFooterLinks_Lists{
        display: $display_flex;
        flex-direction: column;
        flex-wrap: wrap;
        padding: $padding-Y;
      
        .containerFooterLinks_list{
          list-style: none;
          color: rgb(149, 149, 149);
          font-size: 15px;
          padding: 0;
          padding-right: 25px;
          margin: 0;
          
          .list_link_title{
            color: white;
            font-size: 18px;
            font-weight: bold;
            padding: 10px 0;
          }
        }
      }

      .containerFooterLinks_img{
        overflow: hidden;
        text-align: end;

        img{
          position: relative;
          width: 95%;
          top: -100px;
        }
      }
    }


  }

  .containerFooterBottom{
    background: rgb(48, 48, 48);
    padding: $padding-Y;

    .containerFooterSocials{
      max-width: $container_width;
      margin: auto;
      display: $display_flex;
      justify-content: $flex_space_between;

      .containerFooterSocials_btn{
        font-size: 16px;
        font-weight: bold;
        padding: 10px;
        background-color: transparent;
        color: white;
        border: 2px solid $color_primary;
      }

      .containerFooterSocials_list{
        list-style: none;
        display: $display_flex;
        align-items: center;

        .containerFooterSocials_list_item{
          padding-left: 15px;
          color: $color_primary;
          font-weight: bold;
        }
      }

    }
  }
}

</style>