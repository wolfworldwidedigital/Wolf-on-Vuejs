<template>
  <section class="block-sec">
    <div class="background bg-img pt-100 pb-0 parallaxie" style="background-image: url('/img/bg-vid.jpg')"
      data-overlay-dark="5">
      <div class="container">
        <div class="row">
          <div class="col-lg-6">
            <div class="vid-area">
              <span class="text">Watch Video</span>
              <ModalVideo :channel="videoChannel" :videoId="videoId" :isOpen.sync="videoIsOpen" />
              <div class="vid-icon cursor-pointer" @click="openVideo">
                <a class="vid">
                  <div class="vid-butn">
                    <span class="icon">
                      <i class="fas fa-play"></i>
                    </span>
                  </div>
                </a>
              </div>
            </div>
          </div>
          <div class="col-lg-5 offset-lg-1">
            <div class="testim-box">
              <div class="head-box">
                <h6 class="wow fadeIn" data-wow-delay=".5s">Our Clients</h6>
                <h4 class="wow fadeInLeft" data-wow-delay=".5s">
                  What Client&apos;s Say?
                </h4>
              </div>
              <Swiper v-bind="settings" class="slic-item wow fadeInUp" data-wow-delay=".5s">
                <SwiperSlide class="item">
                  <p>
                    Nulla metus metus ullamcorper vel tincidunt sed euismod nibh
                    volutpat velit class aptent taciti sociosqu ad litora.
                  </p>
                  <div class="info">
                    <div class="img">
                      <div class="img-box">
                        <img src="/img/clients/1.jpg" alt="" />
                      </div>
                    </div>
                    <div class="cont">
                      <div class="author">
                        <h6 class="author-name">Alex Regelman</h6>
                        <span class="author-details">
                          Co-founder, Colabrio
                        </span>
                      </div>
                    </div>
                  </div>
                </SwiperSlide>
                <SwiperSlide class="item">
                  <p>
                    Nulla metus metus ullamcorper vel tincidunt sed euismod nibh
                    volutpat velit class aptent taciti sociosqu ad litora.
                  </p>
                  <div class="info">
                    <div class="img">
                      <div class="img-box">
                        <img src="/img/clients/2.jpg" alt="" />
                      </div>
                    </div>
                    <div class="cont">
                      <div class="author">
                        <h6 class="author-name">Alex Regelman</h6>
                        <span class="author-details">
                          Co-founder, Colabrio
                        </span>
                      </div>
                    </div>
                  </div>
                </SwiperSlide>
                <SwiperSlide class="item">
                  <p>
                    Nulla metus metus ullamcorper vel tincidunt sed euismod nibh
                    volutpat velit class aptent taciti sociosqu ad litora.
                  </p>
                  <div class="info">
                    <div class="img">
                      <div class="img-box">
                        <img src="/img/clients/3.jpg" alt="" />
                      </div>
                    </div>
                    <div class="cont">
                      <div class="author">
                        <h6 class="author-name">Alex Regelman</h6>
                        <span class="author-details">
                          Co-founder, Colabrio
                        </span>
                      </div>
                    </div>
                  </div>
                </SwiperSlide>
              </Swiper>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { Swiper, SwiperSlide } from 'swiper/vue';
import ModalVideo from '../Common/ModalVideo.vue';

const videoIsOpen = ref(false);

const settings = {
  loop: true,
  speed: 500,
  slidesPerView: 1,
}

const videoChannel = 'vimeo';
const videoId = '127203262';

function openVideo() {
  videoIsOpen.value = !videoIsOpen.value;
}
</script>