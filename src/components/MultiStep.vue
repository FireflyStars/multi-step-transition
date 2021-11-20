<template>
  <div class="wrapper">
    <div class="step-container">
      <div class="step-panel bg-green" 
          :class="{
            'active': (currentStep == 1),
            'previous': (currentStep > 1),
            'next': (currentStep < 1),
          }" 
          >
          <div class="step-item bg-lightyellow">
            <div class="step-content bg-gray">
              <div class="logo-panel text-center">
                <div class="logo">

                </div>
                <p>Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod</p>
              </div>
            </div>
            <div class="step-nav">
              <img :src="rightChevron" class="arrow-right" alt="right arrow" @click="next">
            </div>
          </div>
      </div>
      <!-- step 2 -->
      <div class="step-panel bg-green" 
          :class="{
            'active': (currentStep == 2),
            'previous': (currentStep > 2),
            'next': (currentStep < 2),
          }" 
          >
          <div class="step-item bg-lightgreen">
            <div class="step-content bg-white">
              <div class="step-content-left bg-lightyellow">
                <div class="step-content-body">
                  <h2 class="w-100 text-center">BASIC INFORMATION</h2>
                  <p class="w-100 text-center">Let's get to know each other.</p>
                </div>
                <div class="step-content-footer">
                  <a href="javascript:;" class="text-black" @click="previous">&lt;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Back</a>
                </div>
              </div>
              <div class="step-content-right">

              </div>
            </div>
            <div class="step-nav">
              <img :src="rightChevron" class="arrow-right" alt="right arrow" @click="next">
            </div>
          </div>
      </div>
      <!-- step 2 end -->

      <!-- step 3 -->
      <div class="step-panel bg-green" 
          :class="{
            'active': (currentStep == 3),
            'previous': (currentStep > 3),
            'next': (currentStep < 3),
          }" 
          >
          <div class="step-item bg-lightbrown">
            <div class="step-content bg-white">
              <div class="step-content-left bg-lightgreen">
                <div class="step-content-body">
                  <h2 class="w-100 text-center title">tattoo basics</h2>
                  <p class="w-100 text-center description">This is permanent, you know...</p>
                </div>
                <div class="step-content-footer">
                  <a href="javascript:;" class="text-black" @click="previous">&lt;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Back</a>
                </div>
              </div>
              <div class="step-content-right">

              </div>
            </div>
            <div class="step-nav">
              <img :src="rightChevron" class="arrow-right" alt="right arrow" @click="next">
            </div>
          </div>
      </div>
      <!-- step 3 end -->

      <!-- step 4 -->
      <div class="step-panel bg-green" 
          :class="{
            'active': (currentStep == 4),
            'previous': (currentStep > 4),
            'next': (currentStep < 4),
          }" 
          >
          <div class="step-item bg-lightred">
            <div class="step-content bg-white">
              <div class="step-content-left bg-lightbrown">
                <div class="step-content-body">
                  <h2 class="w-100 text-center">Sizing & placement</h2>
                  <p class="w-100 text-center description">Draw on the model where you'd like your tattoo</p>
                </div>
                <div class="step-content-footer">
                  <a href="javascript:;" class="text-black" @click="previous">&lt;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Back</a>
                </div>
              </div>
              <div class="step-content-right">

              </div>
            </div>
            <div class="step-nav">
              <img :src="rightChevron" class="arrow-right" alt="right arrow" @click="next">
            </div>
          </div>
      </div>
      <!-- step 4 end -->

      <!-- step 5 -->
      <div class="step-panel bg-green" 
          :class="{
            'active': (currentStep == 5),
            'previous': (currentStep > 5),
            'next': (currentStep < 5),
          }" 
          >
          <div class="step-item bg-darkyellow">
            <div class="step-content bg-white">
              <div class="step-content-left bg-lightred">
                <div class="step-content-body">
                  <h2 class="w-100 text-center">Reference Images</h2>
                  <p class="w-100 text-center description">Upload up to six images</p>
                </div>
                <div class="step-content-footer">
                  <a href="javascript:;" class="text-black" @click="previous">&lt;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Back</a>
                </div>
              </div>
              <div class="step-content-right">

              </div>
            </div>
            <div class="step-nav">
              <img :src="rightChevron" class="arrow-right" alt="right arrow" @click="next">
            </div>
          </div>
      </div>
      <!-- step 5 end -->

      <!-- step 6 -->
      <div class="step-panel bg-green" 
          :class="{
            'active': (currentStep == 6),
            'previous': (currentStep > 6),
            'next': (currentStep < 6),
          }" 
          >
          <div class="step-item bg-lightblue">
            <div class="step-content bg-white">
              <div class="step-content-left bg-darkyellow">
                <div class="step-content-body">
                  <h2 class="w-100 text-center">Review & Submit</h2>
                  <p class="w-100 text-center description">Give it a quick once-over</p>
                </div>
                <div class="step-content-footer">
                  <a href="javascript:;" class="text-black" @click="previous">&lt;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Back</a>
                </div>
              </div>
              <div class="step-content-right">

              </div>
            </div>
            <div class="step-nav">
              <img :src="rightChevron" class="arrow-right" alt="right arrow">
            </div>
          </div>
      </div>
      <!-- step 6 end -->
    </div>
  </div>
</template>

<script>
import rightChevron from '../assets/imgs/right-chevron.svg';
export default {
  name: 'MultiStep',
  props: {
    msg: String
  },
  data() {
    return {
      currentStep: 1,
      totalStep: 3,
      rightChevron
    }
  },
  methods: {
    next(){
      this.currentStep++;
      this.direction = 1;
    },
    previous(){
      this.currentStep --;
      this.direction = 0;
    },

  }

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
