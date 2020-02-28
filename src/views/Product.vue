<template>
  <div class="product">
    <!-- Header -->
    <HeaderShyna/>

    
    <!-- Breadcrumb Section Begin -->
    <div class="breacrumb-section">
        <div class="container">
            <div class="row">
                <div class="col-lg-12">
                    <div class="breadcrumb-text product-more">
                        <router-link to="/">
                            <i class="fa fa-home"></i> Home
                        </router-link>
                        <span>Detail</span>
                    </div>
                </div>
            </div>
        </div>
    </div>
    <!-- Breadcrumb Section Begin -->

    <!-- Product Shop Section Begin -->
    <section class="product-shop spad page-details">
        <div class="container">
            <div class="row">
                <div class="col-lg-12">
                    <div class="row">
                        <div class="col-lg-6">
                            <div class="product-pic-zoom">
                                <img class="product-big-img" :src="first_photo" alt="" />
                            </div>
                            <div class="product-thumbs">
                                <carousel class="product-thumbs-track ps-slider" :nav="false" :dots="false">
                                    <div class="pt" @click="changeImage(other_photo[0])" :class="other_photo[0] == first_photo ? 'active' : '' ">
                                        <img src="img/mickey1.jpg" alt="" />
                                    </div>

                                    <div class="pt" @click="changeImage(other_photo[1])" :class="other_photo[1] == first_photo ? 'active' : '' ">
                                        <img src="img/mickey2.jpg" alt="" />
                                    </div>

                                    <div class="pt" @click="changeImage(other_photo[2])" :class="other_photo[2] == first_photo ? 'active' : '' ">
                                        <img src="img/mickey3.jpg" alt="" />
                                    </div>

                                    <div class="pt" @click="changeImage(other_photo[3])" :class="other_photo[3] == first_photo ? 'active' : '' ">
                                        <img src="img/mickey4.jpg" alt="" />
                                    </div>
                                </carousel>
                            </div>
                        </div>
                        <div class="col-lg-6">
                            <div class="product-details">
                                <div class="pd-title">
                                    <span>oranges</span>
                                    <h3>Pure Pineapple</h3>
                                </div>
                                <div class="pd-desc">
                                    <p>
                                        Lorem ipsum dolor sit amet consectetur adipisicing elit. Corporis, error officia. Rem aperiam laborum voluptatum vel, pariatur modi hic provident eum iure natus quos non a sequi, id accusantium! Autem.
                                    </p>
                                    <p>
                                        Lorem ipsum dolor sit, amet consectetur adipisicing elit. Quam possimus quisquam animi, commodi, nihil voluptate nostrum neque architecto illo officiis doloremque et corrupti cupiditate voluptatibus error illum. Commodi expedita animi nulla aspernatur.
                                        Id asperiores blanditiis, omnis repudiandae iste inventore cum, quam sint molestiae accusamus voluptates ex tempora illum sit perspiciatis. Nostrum dolor tenetur amet, illo natus magni veniam quia sit nihil dolores.
                                        Commodi ratione distinctio harum voluptatum velit facilis voluptas animi non laudantium, id dolorem atque perferendis enim ducimus? A exercitationem recusandae aliquam quod. Itaque inventore obcaecati, unde quam
                                        impedit praesentium veritatis quis beatae ea atque perferendis voluptates velit architecto?
                                    </p>
                                    <h4>$495.00</h4>
                                </div>
                                <div class="quantity">
                                    <router-link to="/cart" class="primary-btn pd-cart">Add To Cart</router-link>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
    <!-- Product Shop Section End -->

    <!-- Related Products -->
    <RelatedProducts/>
    <!-- End Related Products -->

    <!-- Footer -->
    <FooterShyna/>
  </div>
</template>



<script>
// @ is an alias to /src
// import HelloWorld from '@/components/HelloWorld.vue'
import HeaderShyna from '@/components/HeaderShyna.vue';
import RelatedProducts from '@/components/RelatedProducts.vue';
import FooterShyna from '@/components/FooterShyna.vue';
import carousel from 'vue-owl-carousel';


export default {
  name: 'Product',
  components: {
    HeaderShyna,
    RelatedProducts,
    FooterShyna,
    carousel

  },
  data(){
      return{
          first_photo: "img/mickey1.jpg",
          other_photo: [
              "img/mickey1.jpg",
              "img/mickey2.jpg",
              "img/mickey3.jpg",
              "img/mickey4.jpg"
          ]
      }
  },
  methods: {
      changeImage(urlImage){
          this.first_photo = urlImage;
      }
  }
}
</script>

<style>
    .product-thumbs .pt{
        margin-right: 10px;
    }
</style>