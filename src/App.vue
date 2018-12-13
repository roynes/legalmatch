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
        <div class="main-container">
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
                    ref="inputZip"
                    type="text" 
                    name="zipcode" 
                    id="zipcode"
                    placeholder="Does not have to be where you live."
                  >
                  <!-- <div class="input-end"></div> -->
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
                  <div class="input-end category" @click="toggleDropDownCategoryClicked =!toggleDropDownCategoryClicked"></div>

                  <DropDown
                    :toggle="toggleDropDownCategoryClicked"
                    :contents="[
                      'Family', 'Criminal Defense', 'Business', 'Personal Injury', 'Bankcruptcy & Finances',
                      'Products & Services', 'Employment', 'Real Estate', 'Immigration', 'Wills, Trusts & Estates',
                      'Government', 'Intellectual Property'
                    ]"
                    @content-click='showCategoryModal($event)'
                  ></DropDown>
                </div>
              </div>

              <div class="category-not-found">
                <p>Can't find your category? <a href="#" @click="toggleModal =!toggleModal">Click here</a></p>
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

                    <div class="read-review" @click="toggleLawyer1 = !toggleLawyer1">
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

                    <div class="read-review" @click="toggleLawyer2 = !toggleLawyer2">
                      <p>Read Review</p> 
                      <img :src="require('./assets/img/shape-1.png')" alt="" srcset="">
                    </div>
                  </div>
                </div>

                <div class="separator w-full pt-1 mt-4 mb-8" style="background: #4978a6"></div>

                <!-- lawyer 3 -->
                <div class="lawyer" >
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

                    <div class="read-review" @click="toggleLawyer3 = !toggleLawyer3">
                      <p>Read Review</p> 
                      <img :src="require('./assets/img/shape-1.png')" alt="" srcset="">
                    </div>
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

    <Modals :toggle="toggleModal" @close="toggleModal=false">
      <template slot="header-contents">
        <div class="flex flex-wrap flex-col text-left items-start justify-center text-black" style="font-family: 'gotham-medium'">
          <h2 class="uppercase font-bold">Other Categories</h2>
          <h5 class="text-xs">Choose the category that best fits your case</h5>
        </div>
      </template>
      <template slot="content-slot">
        <div class="h-92 w-144 flex text-left text-xs leading-loose cursor-pointer" style="font-family: 'gotham-medium'; color: #1478b6;">
          <div class="w-1/2 h-full">
            <div>Abuse ( Child, Domestic, Sexual )</div>
            <div>Agencies & Administration</div>
            <div>Automobiles ( DUI, Crimes, Overspeeding )</div>
            <div>Automobiles ( Accidents, Insurance )</div>
            <div>Banking ( Business, Consumer )</div>
            <div>Bars & Restaurants</div>
            <div>Business Formation & Dissolution</div>
            <div>Children ( Adoption, Custody, Support )</div>
            <div>Class Actions ( Bad Drugs, Products )</div>
            <div>Commercial Law & Contracts</div>

            <div>Commercial Real Estate</div>
            <div>Constitutional Law</div>
            <div>Construction ( Dispute, Liens )</div>
            <div>Categories Item Here</div>
            <div>Some Other Category</div>
          </div>
          <div class="w-1/2 h-full">
            <div>Abuse ( Child, Domestic, Sexual )</div>
            <div>Agencies & Administration</div>
            <div>Automobiles ( DUI, Crimes, Overspeeding )</div>
            <div>Automobiles ( Accidents, Insurance )</div>
            <div>Banking ( Business, Consumer )</div>
            <div>Bars & Restaurants</div>
            <div>Business Formation & Dissolution</div>
            <div>Children ( Adoption, Custody, Support )</div>
            <div>Class Actions ( Bad Drugs, Products )</div>
            <div>Commercial Law & Contracts</div>

            <div>Commercial Real Estate</div>
            <div>Constitutional Law</div>
            <div>Construction ( Dispute, Liens )</div>
            <div>Categories Item Here</div>
            <div>Some Other Category</div>
          </div>
        </div>
      </template>
    </Modals>

    <Modals :toggle="toggleCategoryModal" @close="toggleCategoryModal=false">
      <template slot="header-contents">
        <div class="flex text-left text-grey-darker items-center" style="font-family: 'gotham-medium'">
          <div class="number-badge border-none pl-1 text-white">
            <div class="input-number">3</div>
          </div>
          <p>Which <span class="font-bold text-black">{{ categoryChosen }} Law</span> issue(s) apply to your case?</p>
        </div>
      </template>
      <template slot="content-slot">
        <div class="h-48 w-144 flex text-left flex-wrap text-grey-darker leading-loose cursor-pointer pb-4" style="font-family: 'gotham-medium';">
          <div class="w-1/2 h-full pl-2">
            <CheckBox class="mb-4">Adoptions</CheckBox>
            <CheckBox class="mb-4">Guardianship</CheckBox>
            <CheckBox class="mb-4">Child Custody & Visitation</CheckBox>
            <CheckBox class="mb-4">Paternity</CheckBox>
          </div>
          <div class="w-1/2 h-full">
            <CheckBox class="mb-4">Child Support</CheckBox>
            <CheckBox class="mb-4">Separations</CheckBox>
            <CheckBox class="mb-4">Divorce</CheckBox>
            <CheckBox class="mb-4">Spousal Support & Alimony</CheckBox>
          </div>
        </div>
        <div style="font-family: 'gotham-medium';" class="flex items-center justify-center uppercase text-white my-4 cursor-pointer">
          <div class="p-4 rounded-full" style="background: #032d6c;">Find a lawyer now</div>
        </div>
      </template>
    </Modals>

    <Modals :toggle="toggleLawyer1" @close="toggleLawyer1=false">
      <template slot="header-contents">
        <div class="flex flex-col text-left text-grey-darker justify-center w-full" style="font-family: 'gotham-medium'">
          <h2 class="uppercase">Client reviews</h2>
          <div class="separator mt-2 mb-0"></div>
        </div>
      </template>
      <template slot="content-slot">
        <div class="h-128 w-128 flex text-left flex-wrap text-grey-darker cursor-pointer pb-4" style="font-family: 'gotham-medium';">
          <div class="w-full h-full flex flex-col">
            <div class="mt-2 details flex items-start">
              <div class="image">
                <img :src="require('./assets/img/mitchell.jpg')" class="w-16 h-16 rounded-full border-grey-dark">
              </div>
              <div class="ml-4 flex flex-col justify-start">
                <h2 class="name">Mitchell M.</h2>
                <p class="font-thin text-grey text-sm">Cherry Hill. NJ</p>
                <p class="font-thin text-sm">Family Law</p>
              </div>
            </div>
            <div class="flex mt-6 items-center">
              <h2>Rating ( 30 users )</h2>
              <img :src="require('./assets/img/favorite-star.png')" class="w-24 h-4 ml-4">
            </div>
            <div>
              <div class="separator mt-2 mb-2"></div>
            </div>
            <div class="flex flex-col w-full mt-4 text-sm" style="font-family: 'gotham-light';">
              <div class="w-full flex items-center mb-2">
                <div class="text-left w-1/2 font-bold" style="font-family: 'gotham-medium';">Overall</div>
                <div class="flex items-center justify-center w-1/2"><img :src="require('./assets/img/favorite-star.png')" class="w-24 h-4"></div>
              </div>
              <div class="w-full flex items-center mb-2">
                <div class="text-left w-1/2 text-xs">Responded in a timely manner</div>
                <div class="flex items-center justify-center w-1/2"><img :src="require('./assets/img/favorite-star.png')" class="w-24 h-4"></div>
              </div>
              <div class="w-full flex items-center mb-2">
                <div class="text-left w-1/2 text-xs">Answered questions clearly</div>
                <div class="flex items-center justify-center w-1/2"><img :src="require('./assets/img/favorite-star.png')" class="w-24 h-4"></div>
              </div>
              <div class="w-full flex items-center mb-2">
                <div class="text-left w-1/2 text-xs">Understands Needs</div>
                <div class="flex items-center justify-center w-1/2"><img :src="require('./assets/img/favorite-star.png')" class="w-24 h-4"></div>
              </div>
              <div class="w-full flex items-center mb-2">
                <div class="text-left w-1/2 text-xs">Gave complete and clear information</div>
                <div class="flex items-center justify-center w-1/2"><img :src="require('./assets/img/favorite-star.png')" class="w-24 h-4"></div>
              </div>
              <div class="w-full flex items-center mb-2">
                <div class="text-left w-1/2 text-xs">Knowledgeable in legal area</div>
                <div class="flex items-center justify-center w-1/2"><img :src="require('./assets/img/favorite-star.png')" class="w-24 h-4"></div>
              </div>
              <div class="w-full flex items-center mb-2">
                <div class="text-left w-1/2 text-xs">Good value for money</div>
                <div class="flex items-center justify-center w-1/2"><img :src="require('./assets/img/favorite-star.png')" class="w-24 h-4"></div>
              </div>
              <div class="w-full flex items-center mb-2">
                <div class="text-left w-1/2 text-xs">Would hire again</div>
                <div class="flex items-center justify-center w-1/2"><img :src="require('./assets/img/favorite-star.png')" class="w-24 h-4"></div>
              </div>
              <div class="w-full flex items-center mb-2">
                <div class="text-left w-1/2 text-xs">Would recommend to a friend</div>
                <div class="flex items-center justify-center w-1/2"><img :src="require('./assets/img/favorite-star.png')" class="w-24 h-4"></div>
              </div>
            </div>
            <div>
              <div class="separator mb-4 mt-6"></div>
            </div>
            <div class="flex flex-col text-xs">
              <div class="flex flex-col">
                <div class="flex items-center" style="font-family: 'gotham-medium';">
                  <img :src="require('./assets/img/favorite-star.png')" class="w-24 h-4">
                  <p class="ml-4">by Dexter Marchel 07/04/2018</p>
                </div>
                <div style="font-family: 'gotham-light';" class="w-full mt-4">
                  Lorem ipsum dolor sit amet consectetur, adipisicing elit. Odio ad sint atque facere minima vitae repellendus, natus magni. Ex quisquam optio aperiam porro illum hic, cupiditate asperiores nihil dignissimos error.
                </div>
              </div>
            </div>
          </div>
        </div>
      </template>
    </Modals>

    <Modals :toggle="toggleLawyer2" @close="toggleLawyer2=false">
      <template slot="header-contents">
        <div class="flex flex-col text-left text-grey-darker justify-center w-full" style="font-family: 'gotham-medium'">
          <h2 class="uppercase">Client reviews</h2>
          <div class="separator mt-2 mb-0"></div>
        </div>
      </template>
      <template slot="content-slot">
        <div class="h-128 w-128 flex text-left flex-wrap text-grey-darker cursor-pointer pb-4" style="font-family: 'gotham-medium';">
          <div class="w-full h-full flex flex-col">
            <div class="mt-2 details flex items-start">
              <div class="image">
                <img :src="require('./assets/img/richard.jpg')" class="w-16 h-16 rounded-full border-grey-dark">
              </div>
              <div class="ml-4 flex flex-col justify-start">
                <h2 class="name">Richard V.</h2>
                <p class="font-thin text-grey text-sm">San Francisco, CA</p>
                <p class="font-thin text-sm">Job & Employment Law</p>
              </div>
            </div>
            <div class="flex mt-6 items-center">
              <h2>Rating ( 40 users )</h2>
              <img :src="require('./assets/img/favorite-star.png')" class="w-24 h-4 ml-4">
            </div>
            <div>
              <div class="separator mt-2 mb-2"></div>
            </div>
            <div class="flex flex-col w-full mt-4 text-sm" style="font-family: 'gotham-light';">
              <div class="w-full flex items-center mb-2">
                <div class="text-left w-1/2 font-bold" style="font-family: 'gotham-medium';">Overall</div>
                <div class="flex items-center justify-center w-1/2"><img :src="require('./assets/img/favorite-star.png')" class="w-24 h-4"></div>
              </div>
              <div class="w-full flex items-center mb-2">
                <div class="text-left w-1/2 text-xs">Responded in a timely manner</div>
                <div class="flex items-center justify-center w-1/2"><img :src="require('./assets/img/favorite-star.png')" class="w-24 h-4"></div>
              </div>
              <div class="w-full flex items-center mb-2">
                <div class="text-left w-1/2 text-xs">Answered questions clearly</div>
                <div class="flex items-center justify-center w-1/2"><img :src="require('./assets/img/favorite-star.png')" class="w-24 h-4"></div>
              </div>
              <div class="w-full flex items-center mb-2">
                <div class="text-left w-1/2 text-xs">Understands Needs</div>
                <div class="flex items-center justify-center w-1/2"><img :src="require('./assets/img/favorite-star.png')" class="w-24 h-4"></div>
              </div>
              <div class="w-full flex items-center mb-2">
                <div class="text-left w-1/2 text-xs">Gave complete and clear information</div>
                <div class="flex items-center justify-center w-1/2"><img :src="require('./assets/img/favorite-star.png')" class="w-24 h-4"></div>
              </div>
              <div class="w-full flex items-center mb-2">
                <div class="text-left w-1/2 text-xs">Knowledgeable in legal area</div>
                <div class="flex items-center justify-center w-1/2"><img :src="require('./assets/img/favorite-star.png')" class="w-24 h-4"></div>
              </div>
              <div class="w-full flex items-center mb-2">
                <div class="text-left w-1/2 text-xs">Good value for money</div>
                <div class="flex items-center justify-center w-1/2"><img :src="require('./assets/img/favorite-star.png')" class="w-24 h-4"></div>
              </div>
              <div class="w-full flex items-center mb-2">
                <div class="text-left w-1/2 text-xs">Would hire again</div>
                <div class="flex items-center justify-center w-1/2"><img :src="require('./assets/img/favorite-star.png')" class="w-24 h-4"></div>
              </div>
              <div class="w-full flex items-center mb-2">
                <div class="text-left w-1/2 text-xs">Would recommend to a friend</div>
                <div class="flex items-center justify-center w-1/2"><img :src="require('./assets/img/favorite-star.png')" class="w-24 h-4"></div>
              </div>
            </div>
            <div>
              <div class="separator mb-4 mt-6"></div>
            </div>
            <div class="flex flex-col text-xs">
              <div class="flex flex-col">
                <div class="flex items-center" style="font-family: 'gotham-medium';">
                  <img :src="require('./assets/img/favorite-star.png')" class="w-24 h-4">
                  <p class="ml-4">by Dexter Marchel 07/04/2018</p>
                </div>
                <div style="font-family: 'gotham-light';" class="w-full mt-4">
                  Lorem ipsum dolor sit amet consectetur, adipisicing elit. Odio ad sint atque facere minima vitae repellendus, natus magni. Ex quisquam optio aperiam porro illum hic, cupiditate asperiores nihil dignissimos error.
                </div>
              </div>
            </div>
          </div>
        </div>
      </template>
    </Modals>

    <Modals :toggle="toggleLawyer3" @close="toggleLawyer3=false">
      <template slot="header-contents">
        <div class="flex flex-col text-left text-grey-darker justify-center w-full" style="font-family: 'gotham-medium'">
          <h2 class="uppercase">Client reviews</h2>
          <div class="separator mt-2 mb-0"></div>
        </div>
      </template>
      <template slot="content-slot">
        <div class="h-128 w-128 flex text-left flex-wrap text-grey-darker cursor-pointer pb-4" style="font-family: 'gotham-medium';">
          <div class="w-full h-full flex flex-col">
            <div class="mt-2 details flex items-start">
              <div class="image">
                <img :src="require('./assets/img/brigida.jpg')" class="w-16 h-16 rounded-full border-grey-dark">
              </div>
              <div class="ml-4 flex flex-col justify-start">
                <h2 class="name">Mitchell M.</h2>
                <p class="font-thin text-grey text-sm">Dallas, TX</p>
                <p class="font-thin text-sm">Family Law</p>
              </div>
            </div>
            <div class="flex mt-6 items-center">
              <h2>Rating ( 26 users )</h2>
              <img :src="require('./assets/img/favorite-star.png')" class="w-24 h-4 ml-4">
            </div>
            <div>
              <div class="separator mt-2 mb-2"></div>
            </div>
            <div class="flex flex-col w-full mt-4 text-sm" style="font-family: 'gotham-light';">
              <div class="w-full flex items-center mb-2">
                <div class="text-left w-1/2 font-bold" style="font-family: 'gotham-medium';">Overall</div>
                <div class="flex items-center justify-center w-1/2"><img :src="require('./assets/img/favorite-star.png')" class="w-24 h-4"></div>
              </div>
              <div class="w-full flex items-center mb-2">
                <div class="text-left w-1/2 text-xs">Responded in a timely manner</div>
                <div class="flex items-center justify-center w-1/2"><img :src="require('./assets/img/favorite-star.png')" class="w-24 h-4"></div>
              </div>
              <div class="w-full flex items-center mb-2">
                <div class="text-left w-1/2 text-xs">Answered questions clearly</div>
                <div class="flex items-center justify-center w-1/2"><img :src="require('./assets/img/favorite-star.png')" class="w-24 h-4"></div>
              </div>
              <div class="w-full flex items-center mb-2">
                <div class="text-left w-1/2 text-xs">Understands Needs</div>
                <div class="flex items-center justify-center w-1/2"><img :src="require('./assets/img/favorite-star.png')" class="w-24 h-4"></div>
              </div>
              <div class="w-full flex items-center mb-2">
                <div class="text-left w-1/2 text-xs">Gave complete and clear information</div>
                <div class="flex items-center justify-center w-1/2"><img :src="require('./assets/img/favorite-star.png')" class="w-24 h-4"></div>
              </div>
              <div class="w-full flex items-center mb-2">
                <div class="text-left w-1/2 text-xs">Knowledgeable in legal area</div>
                <div class="flex items-center justify-center w-1/2"><img :src="require('./assets/img/favorite-star.png')" class="w-24 h-4"></div>
              </div>
              <div class="w-full flex items-center mb-2">
                <div class="text-left w-1/2 text-xs">Good value for money</div>
                <div class="flex items-center justify-center w-1/2"><img :src="require('./assets/img/favorite-star.png')" class="w-24 h-4"></div>
              </div>
              <div class="w-full flex items-center mb-2">
                <div class="text-left w-1/2 text-xs">Would hire again</div>
                <div class="flex items-center justify-center w-1/2"><img :src="require('./assets/img/favorite-star.png')" class="w-24 h-4"></div>
              </div>
              <div class="w-full flex items-center mb-2">
                <div class="text-left w-1/2 text-xs">Would recommend to a friend</div>
                <div class="flex items-center justify-center w-1/2"><img :src="require('./assets/img/favorite-star.png')" class="w-24 h-4"></div>
              </div>
            </div>
            <div>
              <div class="separator mb-4 mt-6"></div>
            </div>
            <div class="flex flex-col text-xs">
              <div class="flex flex-col">
                <div class="flex items-center" style="font-family: 'gotham-medium';">
                  <img :src="require('./assets/img/favorite-star.png')" class="w-24 h-4">
                  <p class="ml-4">by Dexter Marchel 07/04/2018</p>
                </div>
                <div style="font-family: 'gotham-light';" class="w-full mt-4">
                  Lorem ipsum dolor sit amet consectetur, adipisicing elit. Odio ad sint atque facere minima vitae repellendus, natus magni. Ex quisquam optio aperiam porro illum hic, cupiditate asperiores nihil dignissimos error.
                </div>
              </div>
            </div>
          </div>
        </div>
      </template>
    </Modals>
  </div>
</template>

<script>
import Modals from '@/components/Modals.vue';
import DropDown from '@/components/DropDown.vue';
import CheckBox from '@/components/CheckBox.vue';
import places from 'places.js';

export default {
  name: 'app',

  components: { Modals, DropDown, CheckBox },

  data() {
    return {
      toggleDropDownCategoryClicked: false,
      toggleModal: false,
      toggleCategoryModal: false,

      toggleLawyer1: false,
      toggleLawyer2: false,
      toggleLawyer3: false,

      categoryChosen: ''
    }
  },

  methods: {
    showCategoryModal(value) {
      this.toggleDropDownCategoryClicked = false;
      this.toggleCategoryModal = value.tog;
      this.categoryChosen = value.v;
    }
  },

  mounted() {
    places({
      appId: 'plYV192WO6AY',
      apiKey: 'e1cb0436529d7c91975c43220e00868f',
      container: this.$refs.inputZip
    }).configure({
      countries: ['us', 'ph'],
    })
  }
}
</script>

<style>

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

/* global fonts */
.top .options,
.lawyer .details .name, 
.lawyer .review .read-review {
  font-family: 'gotham-medium';
}

.top .logo p,
.center .main .left .form-input,
.lawyer .review .header,
.left .logo-bottom p {
  font-family: 'gotham-bold';
}

.center .main .left .category-not-found,
.lawyer .details .location,
.bottom .middle .agreements,
.bottom .middle .copyrights {
  font-family:'gotham-light';
}

/* top */
.top {
  @apply w-full flex items-center justify-between px-16 mb-1 max-w-4xl mx-auto;
  min-height: 60px;
}

.logo {
  @apply flex items-center;
}

.top .logo p {
  color: #032d6c;
  @apply uppercase mt-3;
}

.top .options {
  @apply flex justify-center w-64 flex-col text-xs leading-normal;
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
  @apply w-full;
}

.center .main-container {
  @apply flex flex-col w-full max-w-4xl mx-auto;
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
  
}

.category-not-found a {
  @apply text-white;
}

.center .main .left .form-input {
  @apply flex flex-col mb-8;
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
  @apply flex flex-col w-1/5 leading-normal;
}

.lawyer .details img {
  @apply w-16 h-16 rounded-full border border-grey-dark;
}

.lawyer .review {
  @apply  flex flex-col pl-1 w-4/5;
}

.lawyer .review .header {
  @apply flex items-center mb-3;
}

.lawyer .review .content {
  @apply w-full;
  font-family: 'gotham-xlight-ita';
}

.lawyer .review .content p {
  @apply text-left;
}

.lawyer .review .read-review {
  @apply mt-4 flex items-center justify-end w-full cursor-pointer;
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
  width: 31px;
  padding-top: 7px;
  text-align: center;
  @apply rounded-full h-8;
}

.form-input .inputs {
  @apply flex;
}

.form-input .inputs input {
  width: 28rem;
  @apply p-6;
}

.form-input .inputs .input-end {
  @apply p-4 rounded-r-full bg-white;
}

.inputs .input-end.category::before {
  background: url('./assets/img/chevron-down-solid.svg') left no-repeat;
}

.inputs .input-end::before {
  content: "";
  position: relative;
  padding: 0 6px;
  top: 7px;
  right: 10px;
}

.privacy-policy::before, .privacy-policy::after {
  content: "";
  background: url('./assets/img/circle-solid.svg')  no-repeat;
  position:relative;
  top: 8px;
  margin: 0px 35px;
  padding: 3px;
}

/* bottom */
.bottom {
  @apply w-full flex justify-between items-start px-16 pb-16 max-w-4xl mx-auto;
}

.bottom .left {
  @apply flex flex-col w-1/5;
}

.bottom .middle {
  @apply flex flex-col w-3/5 text-sm text-grey-darkest;
}

.bottom .right {
  @apply flex flex-col w-1/5;
}

.bottom .left .logo-bottom {
  @apply flex flex-col items-center justify-center m-6;
}

.left .logo-bottom p {
  @apply uppercase text-sm; 
  color: #032d6c;
}

.bottom .middle .agreements {
  @apply flex items-center justify-center mt-6 ;
}

.bottom .middle .copyrights {
  margin-top: 4.3rem;
  @apply flex flex-col items-center justify-center;
}

.bottom .right .trust-e {
  @apply mb-4 mt-6;
}

/* algolia */
span.algolia-places {
  @apply bg-white rounded-full rounded-l-none;
  width: 30.75rem;
}

span.algolia-places input.ap-input {
  border: none;
  margin: 0.5rem;
  margin-left: 0px;
  width: 90%;
}

span.ap-dropdown-menu.ap-with-places {
  left: -44px !important;
  width: 33.1rem;
  @apply rounded-lg mt-3;
}
</style>