<template>
  <footer>
    <div class="containerFooterTop">
      <div class="containerFooterLinks">
        <div class="containerFooterLinks_Lists">
          <ul class="containerFooterLinks_list"
          v-for="(list, i) in FooterLinksList"
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
        <li class="containerFooterSocials_list_item"><a href="#"><img src="../assets/footer-facebook.png" alt=""></a></li>
        <li class="containerFooterSocials_list_item"><a href="#"><img src="../assets/footer-twitter.png" alt=""></a></li>
        <li class="containerFooterSocials_list_item"><a href="#"><img src="../assets/footer-youtube.png" alt=""></a></li>
        <li class="containerFooterSocials_list_item"><a href="#"><img src="../assets/footer-pinterest.png" alt=""></a></li>
        <li class="containerFooterSocials_list_item"><a href="#"><img src="../assets/footer-periscope.png" alt=""></a></li>
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
      FooterLinksList:[
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
      padding: $padding-Y;
      margin: auto;
      display: $display_flex;
      justify-content: space-between;

      .containerFooterLinks_Lists{
        display: $display_flex;
        flex-direction: column;
        flex-wrap: wrap;
        max-height: 300px;
      
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
        max-height: 300px;
        text-align: end;

        img{
          position: relative;
          width: 80%;
          top: -75px;
        }
      }
    }


  }

  .containerFooterBottom{
    background: rgb(48, 48, 48);

    .containerFooterSocials{
      max-width: $container_width;
      padding: $padding-Y;
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