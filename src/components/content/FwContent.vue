<script setup lang="ts">
import {
  IonContent,
  IonIcon,
  IonButtons,
  IonButton,
  IonList,
  IonImg,
  IonItem,
  IonAvatar,
} from "@ionic/vue";
import { alertCircleOutline } from 'ionicons/icons';
import TopSlider from "@/components/content/TopSlider.vue";
import TopFlashSale from "@/components/content/TopFlashSale.vue";
import MidDetailSection from "@/components/content/MidDetailSection.vue";
import SizeSliderTab from "@/components/content/SizeSliderTab.vue";

</script>

<template>
  <ion-content class="main-content-pd" fullscreen>
    <!-- top detail section -->
    <div class="pd-top-sec-wrap">
      <top-slider/>
      <!-- flash -->
      <top-flash-sale/>
      <!-- product heading info -->
      <div class="product-heading-wrap">
        <div class="product-title">Baam 100% My Whey</div>
        <div class="rp-content">
          <ion-buttons class="rate">
            <label>★★★★★</label><span class="review-count">(200 Reviews)</span>
          </ion-buttons>
          <span class="points">500</span>
        </div>
        <div class="pricing-content">
          <div class="price-w">
            <div class="sub-text">Price</div>
            <div class="price-d">฿1,800<span class="price-o">฿2,000</span></div>
          </div>
          <div class="price-w border-left">
            <div class="sub-text">Your Price
              <ion-icon :icon="alertCircleOutline"></ion-icon>
            </div>
            <div class="price-d">฿1,600</div>
            <!--
            <div class="sub-text">Next Tier<ion-icon name="alert-circle-outline"></ion-icon></div>
            <div class="price-nt">฿1,600</div>
            -->
          </div>
        </div>
        <size-slider-tab />
        <ion-buttons class="supp-btn-wrap">
          <ion-button class="supp-btn">View Supplement Fact</ion-button>
        </ion-buttons>
      </div>
    </div>
    <div class="line-break"></div>
    <!-- mid detail section -->
    <mid-detail-section />

    <div class="line-break"></div>
    <!-- bottom detail section -->

    <!-- recommended promo set section -->
    <div class="p-title">Bundle Set</div>
    <div class="slider-item pd-product-slider">
      <div class="swiper-wrapper pd-product-slide">
        <div class="swiper-slide pd-product-container">
          <ion-img class="product-image" src="/assets/img/product-mock4.png"></ion-img>
          <div class="product-info">
            <div class="title">Baam Mass V1</div>
            <div class="price-d">฿1,000<span class="price-o">฿2,000</span></div>
            <ion-buttons class="cart">
              <ion-button>
                <img src="/assets/icon/cart-mini-icon.svg">
              </ion-button>
            </ion-buttons>
          </div>
        </div>
        <div class="swiper-slide pd-product-container">
          <ion-img class="product-image" src="/assets/img/product-mock4.png"></ion-img>
          <div class="product-info">
            <div class="title">Baam Mass V1</div>
            <div class="price-d">฿1,000<span class="price-o">฿2,000</span></div>
            <ion-buttons class="cart">
              <ion-button>
                <img src="/assets/icon/cart-mini-icon.svg">
              </ion-button>
            </ion-buttons>
          </div>
        </div>
        <div class="swiper-slide pd-product-container">
          <ion-img class="product-image" src="/assets/img/product-mock4.png"></ion-img>
          <div class="product-info">
            <div class="title">Baam Mass V1</div>
            <div class="price-d">฿1,000<span class="price-o">฿2,000</span></div>
            <ion-buttons class="cart">
              <ion-button>
                <img src="/assets/icon/cart-mini-icon.svg">
              </ion-button>
            </ion-buttons>
          </div>
        </div>
        <div class="swiper-slide pd-product-container">
          <ion-img class="product-image" src="/assets/img/product-mock4.png"></ion-img>
          <div class="product-info">
            <div class="title">Baam Mass V1</div>
            <div class="price-d">฿1,000<span class="price-o">฿2,000</span></div>
            <ion-buttons class="cart">
              <ion-button>
                <img src="/assets/icon/cart-mini-icon.svg">
              </ion-button>
            </ion-buttons>
          </div>
        </div>
      </div>
    </div>
    <div class="line-break"></div>
    <!-- review section -->
    <div class="pd-review">
      <div class="review-heading-wrap">
        <div class="re-flex">
          <div class="t-title">Customer Review</div>
          <div class="re-rate">
            <label>★★★★★</label><span class="re-rate-total">4/5</span><span class="re-count">(200 Reviews)</span>
          </div>
        </div>
        <ion-buttons class="re-write">
          <ion-button class="re-write-btn">Write Review</ion-button>
        </ion-buttons>
      </div>
      <!-- show max 4 reviews -->
      <ion-list>
        <ion-item>
          <ion-avatar class="img-content" slot="start">
            <img src="/assets/img/profile-placeholder.png">
          </ion-avatar>
          <div class="re-right-content">
            <ion-buttons>
              <ion-button class="like">0</ion-button>
            </ion-buttons>
            <div class="name">Barack Obama</div>
            <div class="rate">★★★★★</div>
            <div class="sub-info">
              <span>12 March 2022</span> |
              <span class="verify"><img src="/assets/icon/verify-icon.svg"> Verified Buyer</span>
            </div>
            <div class="flavor">Vanilla Milkshake</div>
            <p class="description">Lorem ipsum dolor sit met, consecterur adipiscing elit, ed Do eius
              mod tempor incididut ut labore te dfdf dfsdfdf
            </p>
            <div class="img-vdo-container">
              <ul>
                <li>
                  <ion-button class="play-btn">
                    <img src="/assets/icon/play-icon.svg">
                  </ion-button>
                  <img src="https://dummyimage.com/360x640/333/aaa">
                </li>
                <li>
                  <ion-button class="play-btn">
                    <img src="/assets/icon/play-icon.svg">
                  </ion-button>
                  <img src="/assets/img/place-holder3.png">
                </li>
                <li>
                  <img src="/assets/img/place-holder3.png">
                </li>
                <li>
                  <img src="/assets/img/place-holder3.png">
                </li>
                <li>
                  <img src="/assets/img/place-holder3.png">
                </li>
                <li>
                  <img src="/assets/img/place-holder3.png">
                </li>
              </ul>
            </div>
            <div class="bottom-sub-info">
              <span>Order ID: 0123456</span> |
              <span>Product 1 of 2</span><!-- ชิ้นที่ 1 จาก 2 -->
            </div>
          </div>
        </ion-item>
        <ion-item>
          <ion-avatar class="img-content" slot="start">
            <img src="/assets/img/profile-placeholder.png">
          </ion-avatar>
          <div class="re-right-content">
            <ion-buttons>
              <ion-button class="like">0</ion-button>
            </ion-buttons>
            <div class="name">Onitsuka Tiger</div>
            <div class="rate">★★★★★</div>
            <div class="sub-info">
              <span>12 March 2022</span>
            </div>
            <p class="description">Lorem ipsum dolor sit met, consecterur adipiscing elit, ed Do eius
              mod tempor incididut ut labore te dfdf dfsdfdf
            </p>
            <div class="bottom-sub-info">
            </div>
          </div>
        </ion-item>
        <ion-item>
          <ion-avatar class="img-content" slot="start">
            <img src="/assets/img/profile-placeholder.png">
          </ion-avatar>
          <div class="re-right-content">
            <ion-buttons>
              <ion-button class="like-active">3</ion-button>
            </ion-buttons>
            <div class="name">Steve Jobs</div>
            <div class="rate">★★★★★</div>
            <div class="sub-info">
              <span>12 March 2022</span>
              <span class="verify"><img src="/assets/icon/verify-icon.svg"> Verified Buyer</span>
            </div>
            <p class="description">Lorem ipsum dolor sit met, consecterur adipiscing elit, ed Do eius
              mod tempor incididut ut labore te dfdf dfsdfdf
            </p>
            <div class="bottom-sub-info">
              <span>Order ID: 0123456</span>
            </div>
          </div>
        </ion-item>
        <ion-item>
          <ion-avatar class="img-content" slot="start">
            <img src="/assets/img/profile-placeholder.png">
          </ion-avatar>
          <div class="re-right-content">
            <ion-buttons>
              <ion-button class="like-active">3</ion-button>
            </ion-buttons>
            <div class="name">Steve Jobs</div>
            <div class="rate">★★★★★</div>
            <div class="sub-info">
              <span>12 March 2022</span> |
              <span class="verify"><img src="/assets/icon/verify-icon.svg"> Verified Buyer</span>
            </div>
            <div class="flavor">Vanilla Milkshake</div>
            <p class="description">Lorem ipsum dolor sit met, consecterur adipiscing elit, ed Do eius
              mod tempor incididut ut labore te dfdf dfsdfdf
            </p>
            <div class="bottom-sub-info">
              <span>Order ID: 0123456</span> |
              <span>Product 1 of 2</span><!-- ชิ้นที่ 2 จาก 2 -->
            </div>
          </div>
        </ion-item>
      </ion-list>
      <ion-buttons class="sm-btn-wrap">
        <ion-button class="sm-btn">See More</ion-button>
      </ion-buttons>
    </div>
  </ion-content>
</template>

<style scoped>

</style>