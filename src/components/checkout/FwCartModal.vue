<script setup lang="ts">
import {IonFooter,IonList, IonImg, IonButton, IonButtons} from "@ionic/vue";

const props = defineProps({
  show: {
    type: Boolean,
    default: false
  }
})

const emit = defineEmits(['closeModal'])
</script>

<template>
    <ion-modal style="max-width: 600px; margin: auto;" v-if="props.show" >
      <!-- product grid quick cart -->
      <div class="qcart-content-wrap hide">
        <ion-list class="qcart-content">
          <div class="position-wrap">
            <!-- top section -->
            <div class="qcart-top-info-wrap">
              <ion-img class="product-img" src="/assets/img/product-mock3.png"></ion-img>
              <ion-buttons class="qcart-closing-btn">
                <ion-button @click="emit('closeModal')">
                  <img src="/assets/icon/closing-icon.svg">
                </ion-button>
              </ion-buttons>
              <div class="qcart-info-right">
                <span class="qcart-title">Baam My Whey Protien one two sentences dfsdf dfsf</span>
                <p class="qcart-des">Short description two sentence Lorem ipsum Short description two</p>
                <div class="price-d">฿1,250 <span class="price-o">฿1,699</span></div>
                <!-- <div class="price-d">฿1,250</div> -->
                <div class="qcart-points">
                  <img src="/assets/icon/clear-point-icon.svg"/><span class="point">200</span>
                </div>
                <a href="#" class="qcart-lm">Learn More ></a>
              </div>
            </div>
            <!-- mid and bottom section wrap -->
            <div class="qcart-exp">EXP:20/2021</div>
            <div class="qcart-mid-wrap">
              <!-- mid section -->
              <div class="qcart-selector-wrap">
                <div class="qcart-selector">
                  <div class="qcart-heading"> Size <span class="select-num"> (Select 1)</span></div>
                  <ion-buttons class="selector-btn-wrap">
                    <ion-button class="selector-btn n-select">Sample <img class="flash" src="/assets/icon/mnf.svg">
                    </ion-button>
                    <ion-button class="selector-btn n-select">250g</ion-button>
                    <ion-button class="selector-btn select ">1lb <img class="flash" src="/assets/icon/mnf.svg">
                    </ion-button>
                    <ion-button class="selector-btn disable">3lb <img class="flash" src="/assets/icon/mnf.svg">
                    </ion-button>
                    <ion-button class="selector-btn n-select">5lb</ion-button>
                    <ion-button class="selector-btn n-select">10lb</ion-button>
                  </ion-buttons>
                </div>
                <div class="qcart-selector">
                  <div class="qcart-heading">Flavor / Selections <span class="select-num"> (Select 1)</span></div>
                  <ion-buttons class="selector-btn-wrap">
                    <ion-button class="selector-btn n-select">Chocolate</ion-button>
                    <ion-button class="selector-btn n-select">Matcha Green Tea</ion-button>
                    <ion-button class="selector-btn select">Vanilla</ion-button>
                    <ion-button class="selector-btn disable">Cafe Mocha</ion-button>
                    <ion-button class="selector-btn n-select">Orange Yuzu</ion-button>
                    <ion-button class="selector-btn select">Vanilla</ion-button>
                    <ion-button class="selector-btn disable">Cafe Mocha</ion-button>
                    <ion-button class="selector-btn n-select">Orange Yuzu</ion-button>
                  </ion-buttons>
                </div>
              </div>
              <!-- bottom section -->
              <ion-footer class="qcart-confirm-footer">
                <div class="scroll-arrow-wrap" id="scrollable-arrow">
                  <img src="/assets/icon/arrow-down-icon.svg">
                </div>
                <div class="qcart-confirm" lines="none">
                  <div class="qcart-qty-wrap">
                    <p class="qty-left">Quantity</p>
                    <div class="qty-right">
                      <ion-button class="qcart-btn-qty">
                        <img src="/assets/icon/subtract-icon.svg">
                      </ion-button>
                      <span class="quickcart-text-qty">1</span>
                      <ion-button class="qcart-btn-qty">
                        <img src="/assets/icon/add-icon.svg">
                      </ion-button>
                    </div>
                  </div>
                  <ion-buttons class="qcart-mix-btn-wrap">
                    <ion-button slot="start" class="qcart-btn add">Add to Cart</ion-button>
                    <ion-button class="qcart-btn buy">Buy Now</ion-button>
                  </ion-buttons>
                  <!-- for buttons use add,buy,remove,update,inactive for 50% width, add extension -f for width 100%, example: add-f -->
                  <!--
                  <ion-buttons class="qcart-mix-btn-wrap">
                      <ion-button slot="start" expand="block" class="qcart-btn update">Update Cart</ion-button>
                  </ion-buttons>
                  -->
                  <!--
                  <ion-buttons class="qcart-mix-btn-wrap">
                      <ion-button slot="start" expand="block" class="qcart-btn remove">Remove</ion-button>
                  </ion-buttons>
                  -->
                  <!--
                  <ion-buttons class="qcart-mix-btn-wrap">
                      <ion-button slot="start" class="qcart-btn inactive">Add to Cart</ion-button>
                      <ion-button class="qcart-btn inactive">Buy inactive</ion-button>
                  </ion-buttons>
                  -->
                </div>
              </ion-footer>
            </div>
          </div>
        </ion-list>
      </div>

      <!-- product detail quick cart-->
      <div class="qcart-content-wrap hide">
        <ion-list class="qcart-content">
          <div class="position-wrap">
            <!-- top section -->
            <div class="qcart-top-info-wrap">
              <ion-img class="product-img" src="/assets/img/product-mock3.png"></ion-img>
              <ion-buttons class="qcart-closing-btn">
                <ion-button @click="emit('closeModal')">
                  <img alt="" src="/assets/icon/closing-icon.svg">
                </ion-button>
              </ion-buttons>
              <div class="qcart-info-right">
                <span class="qcart-title">Baam My Whey Protien one two sentences dfsdf dfsf</span>
                <p class="qcart-des">Short description two sentence Lorem ipsum Short description two</p>
                <div class="price-d">฿1,250 <span class="price-o">฿1,699</span></div>
                <!-- <div class="price-d">฿1,250</div> -->
                <div class="qcart-points">
                  <img alt="" src="/assets/icon/clear-point-icon.svg"/><span class="point">200</span>
                </div>
              </div>
            </div>
            <!-- mid and bottom section wrap -->
            <div class="qcart-exp">EXP:20/2021</div>
            <div class="qcart-mid-wrap">
              <!-- mid section -->
              <div class="qcart-selector-wrap">
                <div class="qcart-selector">
                  <div class="qcart-heading"> Size <span class="select-num"> (Select 1)</span></div>
                  <ion-buttons class="selector-btn-wrap">
                    <ion-button class="selector-btn n-select">Sample</ion-button>
                    <ion-button class="selector-btn n-select">250g</ion-button>
                    <ion-button class="selector-btn select">1lb</ion-button>
                    <ion-button class="selector-btn disable">3lb</ion-button>
                    <ion-button class="selector-btn n-select">5lb</ion-button>
                    <ion-button class="selector-btn n-select">10lb</ion-button>
                  </ion-buttons>
                </div>
                <div class="qcart-selector">
                  <div class="qcart-heading">Flavor / Selections <span class="select-num"> (Select 1)</span></div>
                  <ion-buttons class="selector-btn-wrap">
                    <ion-button class="selector-btn n-select">Chocolate</ion-button>
                    <ion-button class="selector-btn n-select">Matcha Green Tea</ion-button>
                    <ion-button class="selector-btn select">Vanilla</ion-button>
                    <ion-button class="selector-btn disable">Cafe Mocha</ion-button>
                    <ion-button class="selector-btn n-select">Orange Yuzu</ion-button>
                    <ion-button class="selector-btn disable">Cafe Mocha</ion-button>
                    <ion-button class="selector-btn n-select">Orange Yuzu</ion-button>
                  </ion-buttons>
                </div>
              </div>
              <!-- bottom section -->
              <ion-footer class="qcart-confirm-footer">
                <div class="scroll-arrow-wrap" id="scrollable-arrow">
                  <img alt="" src="/assets/icon/arrow-down-icon.svg">
                </div>
                <div class="qcart-confirm" lines="none">
                  <div class="qcart-qty-wrap">
                    <p class="qty-left">Quantity</p>
                    <div class="qty-right">
                      <ion-button class="qcart-btn-qty">
                        <img src="/assets/icon/subtract-icon.svg">
                      </ion-button>
                      <span class="quickcart-text-qty">1</span>
                      <ion-button class="qcart-btn-qty">
                        <img src="/assets/icon/add-icon.svg">
                      </ion-button>
                    </div>
                  </div>
                  <ion-buttons class="qcart-mix-btn-wrap">
                    <ion-button slot="start" class="qcart-btn add">Add to Cart</ion-button>
                    <ion-button class="qcart-btn buy">Buy Now</ion-button>
                  </ion-buttons>
                  <!-- for buttons use add,buy,remove,update,inactive for 50% width, add extension -f for width 100%, example: add-f -->
                  <!--
                  <ion-buttons class="qcart-mix-btn-wrap">
                      <ion-button slot="start" expand="block" class="qcart-btn update">Update Cart</ion-button>
                  </ion-buttons>
                  -->
                  <!--
                  <ion-buttons class="qcart-mix-btn-wrap">
                      <ion-button slot="start" expand="block" class="qcart-btn remove">Remove</ion-button>
                  </ion-buttons>
                  -->
                  <!--
                  <ion-buttons class="qcart-mix-btn-wrap">
                      <ion-button slot="start" class="qcart-btn inactive">Add to Cart</ion-button>
                      <ion-button class="qcart-btn inactive">Buy inactive</ion-button>
                  </ion-buttons>
                  -->
                </div>
              </ion-footer>
            </div>
          </div>
        </ion-list>
      </div>

      <!-- promotion detail quick cart-->
      <div class="qcart-content-wrap hide">
        <ion-list class="qcart-content">
          <div class="position-wrap">
            <!-- top section -->
            <div class="qcart-top-info-wrap">
              <ion-img class="product-img" src="/assets/img/product-mock4.png"></ion-img>
              <ion-buttons class="qcart-closing-btn">
                <ion-button @click="emit('closeModal')">
                  <img src="/assets/icon/closing-icon.svg">
                </ion-button>
              </ion-buttons>
              <div class="qcart-info-right">
                <span class="qcart-title">Baam Mass V1</span>
                <p class="qcart-des">Short description two sentence Lorem ipsum Short description two</p>
                <div class="price-d">฿2,499 <span class="price-o">฿2,000</span></div>
                <!-- <div class="price-d">฿1,250</div> -->
                <div class="qcart-points">
                  <img src="/assets/icon/clear-point-icon.svg"/><span class="point">200</span>
                </div>
              </div>
            </div>
            <!-- mid and bottom section wrap -->
            <div class="qcart-mid-wrap hide">
              <!-- mid section -->
              <div class="qcart-selector-wrap">
                <div class="qcart-selector">
                  <div class="qcart-exp-promo">EXP:20/2021</div>
                  <div class="qcart-heading"> Mega Mass 5lb <span class="select-num"> (X1)</span></div>
                  <ion-buttons class="selector-btn-wrap">
                    <ion-button class="selector-btn n-select">Rich Chocolate</ion-button>
                    <ion-button class="selector-btn disable">Cookie & Cream</ion-button>
                    <ion-button class="selector-btn select">Vanilla</ion-button>
                    <ion-button class="selector-btn n-select">Banana</ion-button>
                  </ion-buttons>
                </div>
                <div class="qcart-selector">
                  <div class="qcart-exp-promo">EXP:20/2021</div>
                  <div class="qcart-heading">100% Creatine 5000 300g <span class="select-num"> (X1)</span></div>
                  <ion-buttons class="selector-btn-wrap">
                    <ion-button class="selector-btn select">Super Micronized 17x</ion-button>
                  </ion-buttons>
                </div>
                <div class="qcart-selector">
                  <div class="qcart-heading">Spider Bottle 500ml <span class="select-num"> (X1)</span></div>
                  <ion-buttons class="selector-btn-wrap">
                    <ion-button class="selector-btn n-select">Baam Red</ion-button>
                    <ion-button class="selector-btn n-select">Fitwhey Blue</ion-button>
                    <ion-button class="selector-btn select">VX Green</ion-button>
                    <ion-button class="selector-btn n-select">Fitwhey Purple</ion-button>
                    <ion-button class="selector-btn n-select">Fitwhey Gym Orange</ion-button>
                  </ion-buttons>
                </div>
                <div class="qcart-selector">
                  <div class="qcart-heading">E-Book Digital V1<span class="select-num"> (X1)</span></div>
                  <ion-buttons class="selector-btn-wrap">
                    <ion-button class="selector-btn select">-</ion-button>
                  </ion-buttons>
                </div>
              </div>
              <!-- bottom section -->
              <ion-footer class="qcart-confirm-footer">
                <div class="scroll-arrow-wrap" id="scrollable-arrow">
                  <img src="/assets/icon/arrow-down-icon.svg">
                </div>
                <div class="qcart-confirm" lines="none">
                  <div class="qcart-qty-wrap">
                    <p class="qty-left">Quantity</p>
                    <div class="qty-right">
                      <ion-button class="qcart-btn-qty">
                        <img src="/assets/icon/subtract-icon.svg">
                      </ion-button>
                      <span class="quickcart-text-qty">1</span>
                      <ion-button class="qcart-btn-qty">
                        <img src="/assets/icon/add-icon.svg">
                      </ion-button>
                    </div>
                  </div>
                  <ion-buttons class="qcart-mix-btn-wrap">
                    <ion-button slot="start" class="qcart-btn add">Add to Cart</ion-button>
                    <ion-button class="qcart-btn buy">Buy Now</ion-button>
                  </ion-buttons>
                  <!-- for buttons use add,buy,remove,update,inactive for 50% width, add extension -f for width 100%, example: add-f -->
                  <!--
                  <ion-buttons class="qcart-mix-btn-wrap">
                      <ion-button slot="start" expand="block" class="qcart-btn update">Update Cart</ion-button>
                  </ion-buttons>
                  -->
                  <!--
                  <ion-buttons class="qcart-mix-btn-wrap">
                      <ion-button slot="start" expand="block" class="qcart-btn remove">Remove</ion-button>
                  </ion-buttons>
                  -->
                  <!--
                  <ion-buttons class="qcart-mix-btn-wrap">
                      <ion-button slot="start" class="qcart-btn inactive">Add to Cart</ion-button>
                      <ion-button class="qcart-btn inactive">Buy Now</ion-button>
                  </ion-buttons>
                  -->
                </div>
              </ion-footer>
            </div>
          </div>
        </ion-list>
      </div>

      <!-- add on quick cart-->
      <div class="qcart-content-wrap hide">
        <ion-list class="qcart-content">
          <div class="position-wrap">
            <!-- top section -->
            <div class="qcart-top-info-wrap">
              <ion-img class="product-img" src="/assets/img/product-mock3.png"></ion-img>
              <ion-buttons class="qcart-closing-btn">
                <ion-button @click="emit('closeModal')" >
                  <img src="/assets/icon/closing-icon.svg">
                </ion-button>
              </ion-buttons>
              <div class="qcart-info-right">
                <span class="qcart-title">Baam My Whey Protien one two sentences dfsdf dfsf</span>
                <p class="qcart-des">Short description two sentence Lorem ipsum Short description two</p>
                <div class="price-d">฿1,250 <span class="price-o">฿1,699</span></div>
                <!-- <div class="price-d">฿1,250</div> -->
                <div class="qcart-points">
                  <img src="/assets/icon/clear-point-icon.svg"/><span class="point">200</span>
                </div>
              </div>
            </div>
            <!-- mid and bottom section wrap -->
            <div class="qcart-exp">EXP:20/2021</div>
            <div class="qcart-mid-wrap">
              <!-- mid section -->
              <div class="qcart-selector-wrap">
                <div class="qcart-selector">
                  <div class="qcart-heading">Flavor / Selections <span class="select-num"> (Select 1)</span></div>
                  <ion-buttons class="selector-btn-wrap">
                    <ion-button class="selector-btn n-select">Chocolate</ion-button>
                    <ion-button class="selector-btn n-select">Matcha Green Tea</ion-button>
                    <ion-button class="selector-btn select">Vanilla</ion-button>
                    <ion-button class="selector-btn disable">Cafe Mocha</ion-button>
                    <ion-button class="selector-btn n-select">Orange Yuzu</ion-button>
                  </ion-buttons>
                </div>
              </div>
              <!-- bottom section -->
              <ion-footer class="qcart-confirm-footer">
                <div class="scroll-arrow-wrap" id="scrollable-arrow">
                  <img src="/assets/icon/arrow-down-icon.svg">
                </div>
                <div class="qcart-confirm" lines="none">
                  <div class="qcart-qty-wrap">
                    <p class="qty-left">Quantity</p>
                    <div class="qty-right">
                      <ion-button class="qcart-btn-qty">
                        <img src="/assets/icon/subtract-icon.svg">
                      </ion-button>
                      <span class="quickcart-text-qty">1</span>
                      <ion-button class="qcart-btn-qty">
                        <img src="/assets/icon/add-icon.svg">
                      </ion-button>
                    </div>
                  </div>
                  <!-- for buttons use add,buy,remove,update,inactive for 50% width, add extension -f for width 100%, example: add-f -->
                  <!--
                  <ion-buttons class="qcart-mix-btn-wrap">
                      <ion-button slot="start" class="qcart-btn add">Add to Cart</ion-button>
                      <ion-button class="qcart-btn buy">Buy Now</ion-button>
                  </ion-buttons>
                  -->
                  <ion-buttons class="qcart-mix-btn-wrap">
                    <ion-button slot="start" expand="block" class="qcart-btn update">Update Cart</ion-button>
                  </ion-buttons>
                  <!--
                  <ion-buttons class="qcart-mix-btn-wrap">
                      <ion-button slot="start" expand="block" class="qcart-btn remove">Remove</ion-button>
                  </ion-buttons>
                  -->
                  <!--
                  <ion-buttons class="qcart-mix-btn-wrap">
                      <ion-button slot="start" class="qcart-btn inactive">Add to Cart</ion-button>
                      <ion-button class="qcart-btn inactive">Buy Now</ion-button>
                  </ion-buttons>
                  -->
                </div>
              </ion-footer>
            </div>
          </div>
        </ion-list>
      </div>

      <!-- none selected quick cart-->
      <div class="qcart-content-wrap ">
        <ion-list class="qcart-content">
          <div class="position-wrap">
            <!-- top section -->
            <div class="qcart-top-info-wrap">
              <ion-img class="product-img" src="/assets/img/product-mock3.png"></ion-img>
              <ion-buttons class="qcart-closing-btn">
                <ion-button @click="emit('closeModal')">
                  <img src="/assets/icon/closing-icon.svg">
                </ion-button>
              </ion-buttons>
              <div class="qcart-info-right">
                <span class="qcart-title">Baam My Whey Protien one two sentences dfsdf dfsf</span>
                <p class="qcart-des">Short description two sentence Lorem ipsum Short description two</p>
              </div>
            </div>
            <!-- mid and bottom section wrap -->
            <div class="qcart-select">Please select your options</div> <!-- กดตัวเลือกด้านล่าง เพื่อสั่งซื้อ -->
            <div class="qcart-exp">EXP:20/2021</div>
            <div class="qcart-mid-wrap">
              <!-- mid section -->
              <div class="qcart-selector-wrap">
                <div class="qcart-selector">
                  <div class="qcart-heading">Size <span class="select-num"> (Select 1)</span></div>
                  <ion-buttons class="selector-btn-wrap">
                    <ion-button class="selector-btn n-select">1lb</ion-button>
                  </ion-buttons>
                </div>
                <div class="qcart-selector">
                  <div class="qcart-heading">Flavor / Selections <span class="select-num"> (Select 1)</span></div>
                  <ion-buttons class="selector-btn-wrap">
                    <ion-button class="selector-btn n-select">Chocolate</ion-button>
                    <ion-button class="selector-btn n-select">Matcha Green Tea</ion-button>
                    <ion-button class="selector-btn select">Vanilla</ion-button>
                    <ion-button class="selector-btn disable">Cafe Mocha</ion-button>
                    <ion-button class="selector-btn n-select">Super Yummy Japanese Home Made Orange Yuzu</ion-button>
                  </ion-buttons>
                </div>
              </div>
              <!-- bottom section -->
              <ion-footer class="qcart-confirm-footer">
                <div class="scroll-arrow-wrap" id="scrollable-arrow">
                  <img src="/assets/icon/arrow-down-icon.svg">
                </div>
                <div class="qcart-confirm" lines="none">
                  <div class="qcart-qty-wrap">
                    <p class="qty-left">Quantity</p>
                    <div class="qty-right">
                      <ion-button class="qcart-btn-qty">
                        <img src="/assets/icon/subtract-icon.svg">
                      </ion-button>
                      <span class="quickcart-text-qty">1</span>
                      <ion-button class="qcart-btn-qty">
                        <img src="/assets/icon/add-icon.svg">
                      </ion-button>
                    </div>
                  </div>
                  <!-- for buttons use add,buy,remove,update,inactive for 50% width, add extension -f for width 100%, example: add-f -->
                  <!--
                  <ion-buttons class="qcart-mix-btn-wrap">
                      <ion-button slot="start" class="qcart-btn add">Add to Cart</ion-button>
                      <ion-button class="qcart-btn buy">Buy Now</ion-button>
                  </ion-buttons>
                  -->
                  <ion-buttons class="qcart-mix-btn-wrap">
                    <ion-button slot="start" expand="block" class="qcart-btn inactive-f">Add to Cart</ion-button>
                  </ion-buttons>
                  <!--
                  <ion-buttons class="qcart-mix-btn-wrap">
                      <ion-button slot="start" expand="block" class="qcart-btn remove">Remove</ion-button>
                  </ion-buttons>
                  -->
                  <!--
                  <ion-buttons class="qcart-mix-btn-wrap">
                      <ion-button slot="start" class="qcart-btn inactive">Add to Cart</ion-button>
                      <ion-button class="qcart-btn inactive">Buy Now</ion-button>
                  </ion-buttons>
                  -->
                </div>
              </ion-footer>
            </div>
          </div>
        </ion-list>
      </div>

      <!-- select freebies quick cart-->
      <div class="qcart-content-wrap hide">
        <ion-list class="qcart-content">
          <div class="position-wrap">
            <!-- top section -->
            <div class="qcart-top-info-wrap">
              <ion-img class="product-img" src="/assets/img/product-mock5.png"></ion-img>
              <ion-buttons class="qcart-closing-btn">
                <ion-button @click="emit('closeModal')">
                  <img src="/assets/icon/closing-icon.svg">
                </ion-button>
              </ion-buttons>
              <div class="qcart-info-right">
                <span class="qcart-title">Baam Mask Fitwhey</span>
                <p class="qcart-des">Short description two sentence Lorem ipsum Short description two</p>
                <div class="use-points">1000 Points</div>
              </div>
            </div>
            <!-- mid and bottom section wrap -->
            <div class="qcart-exp">EXP:20/2021</div>
            <div class="qcart-mid-wrap">
              <!-- mid section -->
              <div class="qcart-selector-wrap">
                <div class="qcart-selector">
                  <div class="qcart-heading">Flavor / Selections <span class="select-num"> (Select 1)</span></div>
                  <ion-buttons class="selector-btn-wrap">
                    <ion-button class="selector-btn n-select">Baam Red</ion-button>
                    <ion-button class="selector-btn n-select">Fitwhey Blue</ion-button>
                  </ion-buttons>
                </div>
              </div>
              <!-- bottom section -->
              <ion-footer class="qcart-confirm-footer">
                <div class="scroll-arrow-wrap" id="scrollable-arrow">
                  <img src="/assets/icon/arrow-down-icon.svg">
                </div>
                <div class="qcart-confirm" lines="none">
                  <div class="qcart-qty-wrap">
                    <p class="qty-left">Quantity</p>
                    <div class="qty-right">
                      <ion-button class="qcart-btn-qty">
                        <img src="/assets/icon/subtract-icon.svg">
                      </ion-button>
                      <span class="quickcart-text-qty">1</span>
                      <ion-button class="qcart-btn-qty">
                        <img src="/assets/icon/add-icon.svg">
                      </ion-button>
                    </div>
                  </div>
                  <!-- for buttons use add,buy,remove,update,inactive for 50% width, add extension -f for width 100%, example: add-f -->
                  <!--
                  <ion-buttons class="qcart-mix-btn-wrap">
                      <ion-button slot="start" class="qcart-btn add">Add to Cart</ion-button>
                      <ion-button class="qcart-btn buy">Buy Now</ion-button>
                  </ion-buttons>
                  -->
                  <ion-buttons class="qcart-mix-btn-wrap">
                    <ion-button slot="start" expand="block" class="qcart-btn add-f">Add to Cart</ion-button>
                  </ion-buttons>
                  <!--
                  <ion-buttons class="qcart-mix-btn-wrap">
                      <ion-button slot="start" expand="block" class="qcart-btn remove">Remove</ion-button>
                  </ion-buttons>
                  -->
                  <!--
                  <ion-buttons class="qcart-mix-btn-wrap">
                      <ion-button slot="start" class="qcart-btn inactive">Add to Cart</ion-button>
                      <ion-button class="qcart-btn inactive">Buy Now</ion-button>
                  </ion-buttons>
                  -->
                </div>
              </ion-footer>
            </div>
          </div>
        </ion-list>
      </div>

    </ion-modal>
</template>

<style scoped>

</style>