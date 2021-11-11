<template>
  <footer>
    <div class="containerFooter">
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
      <div class="containerFooterSocials">
        
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
  background-image: url('../assets/footer-bg.jpg');

  .containerFooter{
    max-width: $container_width;
    padding: $padding-Y;
    margin: auto;

    .containerFooterLinks{
      display: flex;
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
          
          .list_link_title{
            color: white;
            font-size: 18px;
            font-weight: bold;
          }
        }
      }


      .containerFooterLinks_img{
        overflow: hidden;
        max-height: 300px;

        img{
          position: relative;
          width: 80%;
          top: -75px;
        }
      }
    }


  }
}

</style>