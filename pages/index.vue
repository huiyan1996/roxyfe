<template>
  <!-- <Tutorial/> -->
  <div class="container-fluid">
    <!-- <h1 class="text-center">{{pageTitle}}</h1> -->
    <!-- <div class="row justify-content-center mt-3"> -->
    <!-- <div class="row">
      <div class="col-lg-12"> -->
        <!-- <About :aboutDesc="aboutDesc" title="About Us" /> -->
        <Banner />
        <About :desc="aboutDesc" />
        <Mission :desc="testimonialDesc" />
        <Forher :desc="missionDesc" />
        <Product :list="productList" />
        <Ingredient :list="ingredientList" />
        <Benefit :desc="benefitDesc" :list="benefitList" />
        <Testimonial :desc="testimonialDesc" :list="testimonialList" />
        <!-- <Accordion :list="list" title="ROSY" /> -->
      <!-- </div>
    </div> -->
  </div>
</template>

<script>
export default {
    name: "IndexPage",
    head() {
        return {
            title: "ROSY"
        };
    },
    data() {
        return {
            aboutDesc: "Lorem ipsum dolor sit amet, consectetuer adipiscing, elit, sed diam nonummy nibh euismod tincidunt ut laoreet dolore magna aliquam erat volutpat. Ut wisi enim ad minim veniam, quis nostrud exerci tation ullamcorper suscipit",
            testimonialDesc: "Lorem ipsum dolor sit amet, consectetuer adipiscing elit, sed diam nonummy nibh euismod tincidunt ut laoreet dolore magna aliquam erat volutpat. Ut wisi enim ",
            missionDesc: "Lorem ipsum dolor sit amet, consectetuer adipiscing elit",
            testimonialList: [
              { title: "Lorem ipsum dolor sit", content: "<p>consectetuer adipiscing</p>", src: "josue-michel-wtGp_v9VhqM-unsplash.jpg" },
              { title: "Lorem ipsum dolor sit", content: "<p>consectetuer adipiscing</p>", src: "wasa-crispbread-zy_TwITav9c-unsplash.jpg" },
              { title: "Lorem ipsum dolor sit", content: "<p>consectetuer adipiscing</p>", src: "marian-luzi-DBeaZsvTKIw-unsplash.jpg" },
              { title: "Lorem ipsum dolor sit", content: "<p>consectetuer adipiscing</p>", src: "zarina-iskarova-uPv_C0TRDhE-unsplash.jpg" },
              { title: "Lorem ipsum dolor sit", content: "<p>consectetuer adipiscing</p>", src: "keith-tanner-QIAOgZKwaxA-unsplash.jpg" },
            ],
            benefitDesc: "Lorem ipsum dolor sit amet, consectetuer adipiscing elit, sed diam nonummy nibh euismod tincidunt ut laoreet dolore magna aliquam erat volutpat. Ut wisi enim ad minim veniam, quis nostrud exerci tation ullamcorper suscipit",
            benefitList: [
              { title: "Lorem ipsum", src: "productDesc01.png" },
              { title: "Lorem ipsum", src: "productDesc02.png" },
              { title: "Lorem ipsum", src: "productDesc03.png" },
              { title: "Lorem ipsum", src: "productDesc04.png" },
            ],
            ingredientList: [
              { content: "Lorem ipsum dolor sit amet, consectetuer adipiscing elit, sed diam nonummy nibh euismod tincidunt ut laoreet dolore magna aliquam erat volutpat. Ut wisi enim ad minim veniam, quis nostrud exerci tation ullamcorper suscipit lobortis nisl ut aliquip ex ea commodo" },
              { content: "Lorem ipsum dolor sit amet, consectetuer adipiscing elit, sed diam nonummy nibh euismod tincidunt ut laoreet dolore magna aliquam erat volutpat. Ut wisi enim ad minim veniam, quis nostrud exerci tation" },
              { content: "Lorem ipsum dolor sit amet, consectetuer adipiscing elit, sed diam nonummy nibh euismod tincidunt ut laoreet dolore magna aliquam erat volutpat. Ut wisi enim ad minim veniam, quis nostrud exerci tation ullamcorper suscipit lobortis nisl ut aliquip ex ea commodo" },
            ],
            productList: [
              { title: "Serum", src: "keith-tanner-QIAOgZKwaxA-unsplash.jpg" },
              { title: "Collagen", src: "wasa-crispbread-zy_TwITav9c-unsplash.jpg" },
              { title: "Whitening", src: "zarina-iskarova-mfdcvEc0EMA-unsplash.jpg" },
            ],
            list: [
                { title: "USD/JPY????????????", content: "<p>???????????????????????????</p>" },
                { title: "?????????USD/JPY????????????", content: "<p>?????????????????????????????????????????????</p>" },
                { title: "??????????????????????????????USD/JPY???", content: "<p>EUR/USD???EUR/GBP???USD/JPY??????????????????????????????????????????????????????????????????????????????</p>" },
                { title: "???????????????USD/JPY?????????", content: "<p>USD/JPY?????????????????????????????????????????????GBP/JPY???EUR/JPY ???</p>" },
                { title: "USD/JPY???????????????????????????", content: "<p>??????????????????????????????17??????????????????????????????????????????17??????</p>" },
            ],
            pageTitle: "ROSY",
        };
    },
}
</script>

<style>
.container-fluid {
  padding: 0px;
}
</style>