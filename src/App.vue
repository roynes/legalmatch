<template>
  <div id="app" class="bg-white">
    <div class="content">
      <div class="top">
        <div class="logo">
          <img :src="require('./assets/img/logo.png')" alt="">
          <p class="">Find the Right Lawyer now</p>
        </div>
        <div class="options" style="">
          <div class="option-value">
            <div class="check-mark"></div>
            <p>
              No fee to present your case
            </p>
          </div>

          <div class="option-value">
            <div class="check-mark"></div>
            <p>
              Choose from lawyers in your area
            </p>
          </div>

          <div class="option-value">
            <div class="check-mark"></div>
            <p>
              A 100% confidential service
            </p>
          </div>
        </div>
      </div>
      <div class="center">
        <div class="top-header">
          <h1>Find a Lawyer for your Legal Issue</h1>
          <h3>Fast, Free and Confidential</h3>
        </div>

        <div class="main">
          <div class="left">
            <div class="form-input">
              <label for="zipcode">Enter Zip Code or City:</label>
              <div class="inputs">
                <div class="number-badge">
                  <div class="input-number">1</div>
                </div>
                <input 
                  type="text" 
                  name="zipcode" 
                  id="zipcode"
                  placeholder="Does not have to be where you live."
                >
                <div class="input-end"></div>
              </div>
            </div>

            <div class="form-input">
              <label for="category">Choose a category:</label>
              <div class="inputs">
                <div class="number-badge">
                  <div class="input-number">2</div>
                </div>
                <input 
                  type="text" 
                  name="category" 
                  id="category"
                  placeholder="Click to choose a legal category"
                >
                <div class="input-end"></div>
              </div>
            </div>

            <div class="category-not-found">
              <p>Can't find your category? Click here.</p>
            </div>
          </div>

          <div class="right">
            <h3 class="review-header">
              Clients review LegalMatch lawyers
            </h3>

            <div class="review-contents">
              <!-- lawyer 1 -->
              <div class="lawyer">
                <div class="details">
                  <div class="image">
                    <img :src="require('./assets/img/mitchell.jpg')">
                  </div>
                  <div class="name">Mitchell M.</div>
                  <div class="location">Cherry Hill. NJ</div>
                </div>

                <div class="review">
                  <div class="header">
                    <p>Family Law</p>
                    <img :src="require('./assets/img/favorite-star.png')">
                  </div>

                  <div class="content">
                    <p>
                      "Lorem ipsum dolor sit amet consectetur adipisicing elit. Aspernatur, non quibusdam nemo accusantium quos repellat
                    </p>
                  </div>

                  <div class="read-review">
                    <p>Read Review</p> 
                    <img :src="require('./assets/img/shape-1.png')" alt="" srcset="">
                  </div>
                </div>
              </div>

              <div class="separator w-full pt-1 mt-4 mb-8" style="background: #4978a6"></div>

              <!-- lawyer 2 -->
              <div class="lawyer">
                <div class="details">
                  <div class="image">
                    <img :src="require('./assets/img/richard.jpg')">
                  </div>
                  <div class="name">Richard V.</div>
                  <div class="location">San Francisco, CA</div>
                </div>

                <div class="review">
                  <div class="header">
                    <p>Job & Employment Law</p>
                    <img :src="require('./assets/img/favorite-star.png')">
                  </div>

                  <div class="content">
                    <p>
                      "Lorem ipsum dolor sit amet consectetur adipisicing elit. Aspernatur, non quibusdam nemo accusantium quos repellat
                    </p>
                  </div>

                  <div class="read-review">
                    <p>Read Review</p> 
                    <img :src="require('./assets/img/shape-1.png')" alt="" srcset="">
                  </div>
                </div>
              </div>

              <div class="separator w-full pt-1 mt-4 mb-8" style="background: #4978a6"></div>

              <!-- lawyer 3 -->
              <div class="lawyer">
                <div class="details">
                  <div class="image">
                    <img :src="require('./assets/img/brigida.jpg')">
                  </div>
                  <div class="name">Brigida R.</div>
                  <div class="location">Dallas, TX</div>
                </div>

                <div class="review">
                  <div class="header">
                    <p>Family Law</p>
                    <img :src="require('./assets/img/favorite-star.png')">
                  </div>

                  <div class="content">
                    <p>
                      "Lorem ipsum dolor sit amet consectetur adipisicing elit. Aspernatur, non quibusdam nemo accusantium quos repellat
                    </p>
                  </div>

                  <div class="read-review">
                    <p>Read Review</p> 
                    <img :src="require('./assets/img/shape-1.png')" alt="" srcset="">
                  </div>
                </div>
              </div>  
            </div>
          </div>
        </div>
      </div>
      <div class="bottom">
        <div class="left">
          <div class="logo-bottom">
            <div class="logo">
              <img :src="require('./assets/img/logo.png')">
            </div>
            <div>
              <p>
                find the right lawyer now
              </p>
            </div>
          </div>
        </div>
        <div class="middle">
          <div class="agreements">
            <div>User Agreement</div>
            <div class="privacy-policy">Privacy Policy</div>
            <div>Site Map</div>
          </div>
          <div class="copyrights">
            <div>Copyright 1999-2016 LegalMatch. All rights reserved. LegalMatch , the LegalMatch Logo and</div>
            <div>the traded address are trademarks of LegalMatch. Patents Pending</div>
          </div>
        </div>
        <div class="right">
          <div class="trust-e">
            <img :src="require('./assets/img/truste.png')" alt="">
          </div>
          <div>
            <img :src="require('./assets/img/bbb.png')" alt="">
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'app',
  components: {
    HelloWorld
  }
}
</script>

<style>
@tailwind utilities;


#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

input {
  @apply outline-none;
}

/* top */
.top {
  @apply w-full flex items-center justify-between px-16 mb-1;
  min-height: 60px;
}

.logo {
  @apply flex items-center;
}

.top .logo p {
  font-family: 'gotham-bold'; 
  color: #032d6c;
  @apply uppercase mt-3;
}

.top .options {
  @apply flex justify-center w-64 flex-col text-xs leading-normal;
  font-family: 'gotham-medium';
}

.top .options .option-value {
  @apply text-left flex items-center;
}

.top .options .option-value .check-mark {
  background: url('./assets/img/check-solid.svg')  no-repeat;
  padding: 5px;
  @apply mr-1 p-1;
}


/* center */
.center {
  background: radial-gradient(circle farthest-side at 50% 300%, #1478b6, #032d6c);
  @apply w-full flex flex-col;
}

.center .top-header {
  @apply px-16 text-left pt-6 text-grey-light;
}

.center .top-header h1 {
  font-family: 'gotham-xlight';
  @apply text-5xl;
}

.center .top-header h3 {
  font-family: 'gotham-book';
  @apply mt-2;
}

.center .main {
  @apply px-16 flex mb-5;
}

.center .main .left {
  @apply w-1/2 text-left text-grey-light pt-10;
}

.center .main .left .category-not-found {
  @apply text-left ml-24;
  font-family:'gotham-light';
}

.center .main .left .form-input {
  @apply flex flex-col mb-8;
  font-family: 'gotham-bold';
}

.center .main .left .form-input label {
  @apply pb-4;
}

.center .main .right {
  @apply w-1/2 flex flex-col justify-start text-grey-light pl-32;
}

.main .right .review-header {
  @apply text-left pt-1 pb-6;
  font-family: 'gotham-thin';
}

.main .right .review-contents {
  @apply flex flex-col;
}

.main .right .review-contents .lawyer {
  @apply flex text-xs;
}

.lawyer .details {
  @apply flex flex-col w-1/3 leading-normal;
}

.lawyer .details img {
  @apply w-16 h-16 rounded-full border border-grey-dark;
}

.lawyer .details .name {
  font-family: 'gotham-medium';
}

.lawyer .details .location {
  font-family: 'gotham-light';
}

.lawyer .review {
  @apply  flex flex-col pl-1 w-2/3;
}

.lawyer .review .header {
  @apply flex items-center mb-3;
  font-family: 'gotham-bold';
}

.lawyer .review .content {
  @apply w-full;
  font-family: 'gotham-xlight-ita';
}

.lawyer .review .content p {
  @apply text-left;
}

.lawyer .review .read-review {
  @apply mt-4 flex items-center justify-end w-full;
  font-family: 'gotham-medium';
}

.lawyer .review .read-review p {
  @apply mr-1; 
  color: #dec24c;
}

.review .header img {
  @apply ml-6 w-24 h-4;
}

.separator {
  @apply w-full pt-1 mt-4 mb-8; 
  background: #4978a6;
}

.number-badge {
  @apply flex items-center border p-1 pl-3 rounded-l-full bg-white border-r-0;
}

.input-number {
  background: #d68d00;
  @apply rounded-full py-2 px-3 h-8;
}

.form-input .inputs {
  @apply flex;
}

.form-input .inputs input {
  @apply p-6 w-4/5;
}

.form-input .inputs .input-end {
  @apply p-4 rounded-r-full bg-white;
}

.privacy-policy::before, .privacy-policy::after {
  content: "";
  background: url('./assets/img/circle-solid.svg')  no-repeat;
  position:relative;
  top: 8px;
  margin: 0px 35px;
  padding: 3px;
}

.bottom {
  @apply w-full flex justify-between items-center px-16 pb-16;
}

.bottom .left {
  @apply flex flex-col w-1/5;
}

.bottom .middle {
  @apply flex flex-col w-3/5 text-sm text-grey;
}

.bottom .right {
  @apply flex flex-col w-1/5;
}

.bottom .left .logo-bottom {
  @apply flex flex-col items-center justify-center;
}

.left .logo-bottom p {
  @apply uppercase text-sm;
  font-family: 'gotham-bold'; 
  color: #032d6c;
}

.bottom .middle .agreements {
  @apply flex items-center justify-center mt-16; 
  font-family:'gotham-light';
}

.bottom .middle .copyrights {
  @apply flex flex-col items-center justify-center mt-16; font-family:'gotham-light';
}

.bottom .right trust-e {
  
}
</style>