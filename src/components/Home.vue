<template>
   <v-app light>
    <v-toolbar class="white">
      <v-toolbar-title v-text="title">Xeno-Studios</v-toolbar-title>
    </v-toolbar>
    <main>
      <v-content>
        <section>
          <v-parallax src="https://cdn.stocksnap.io/img-thumbs/960w/CDFFE6C72E.jpg">
            <v-layout
              column
              align-center
              justify-center
              class="white--text"
            >
              <h1 class="white--text mb-2 display-1 text-xs-center">Xeno-Studios</h1>
              <div class="subheading mb-3 text-xs-center">Web Development and Design</div>
            </v-layout>
          </v-parallax>
        </section>

        <section>
          <v-layout
            column
            wrap
            class="my-5"
            align-center
          >
            <v-flex xs12 sm8 class="my-3">
              <div class="text-xs-center">
                <h2 class="headline">Custom built web solutions for all types of companies. </h2>
                <span class="subheading">
                  Let's build something together!    
                </span>
              </div>
            </v-flex>
            <v-flex xs12>
              <v-container grid-list-xl>
                <v-layout row wrap align-center>
                  <v-flex xs12 md4>
                    <v-card class="elevation-0 transparent" style="height: 400px;">
                      <v-card-text class="text-xs-center">
                        <v-icon x-large class="blue--text text--lighten-2">color_lens</v-icon>
                      </v-card-text>
                      <v-card-title primary-title class="layout justify-center">
                        <div class="headline text-xs-center">Custom Design</div>
                      </v-card-title>
                      <v-card-text>
                        Custom styling built with your company in mind. We have knowledge of many different types of design frameworks including Material Design, UIKit, Fluent Design, Bootstrap and others. Let us know what you need and we will put together the best possible design!  
                      </v-card-text>
                    </v-card>
                  </v-flex>
                  <v-flex xs12 md4>
                    <v-card class="elevation-0 transparent" style="height: 400px;">
                      <v-card-text class="text-xs-center">
                        <v-icon x-large class="blue--text text--lighten-2">flash_on</v-icon>
                      </v-card-text>
                      <v-card-title primary-title class="layout justify-center">
                        <div class="headline">Fast development</div>
                      </v-card-title>
                      <v-card-text>
                        We also have knowledge of many frontend frameworks which speeds up the process of building your website. With tools such as Vuejs, React, AngularJS 4 and others at our disposal building your website to match your business needs will be no problem! 
                      </v-card-text>
                    </v-card>
                  </v-flex>
                  <v-flex xs12 md4>
                    <v-card class="elevation-0 transparent" style="height: 400px;">
                      <v-card-text class="text-xs-center">
                        <v-icon x-large class="blue--text text--lighten-2">build</v-icon>
                      </v-card-text>
                      <v-card-title primary-title class="layout justify-center">
                        <div class="headline text-xs-center">Free Hosting<sup>*</sup></div>
                      </v-card-title>
                      <v-card-text>
                        Free hosting with static websites! Static websites include the ability to have a Contact Us form for users to contact you directly via e-mail. We also have other options for bigger websites! Contact us today and let us know what you need!<br /><br />
                        <div style="font-size:12px;"><sup>*</sup> Free hosting for static websites only. Websites that need to have users, blogs, news articles, etc... a server will be needed and we can discuss hosting options if it is needed.</div>
                      </v-card-text>
                    </v-card>
                  </v-flex>
                </v-layout>
              </v-container>
            </v-flex>
          </v-layout>
        </section>

        <section>
          <v-parallax src="https://cdn.stocksnap.io/img-thumbs/960w/0O6GE6M3GU.jpg" height="380">
            <v-layout column align-center justify-center>
              <div class="headline white--text mb-3 text-xs-center">Obtaining a Website has never been easier! Contact Us Today!</div>
            </v-layout>
          </v-parallax>
        </section>

        <section>
          <v-container grid-list-xl>
            <v-layout row wrap justify-center class="my-5">
              <v-flex xs12 sm4>
                <v-card class="elevation-0 transparent">
                  <v-card-title primary-title class="layout justify-center">
                    <div class="headline">About Xeno-Studios</div>
                  </v-card-title>
                  <v-card-text>
                    Xeno-Studios is a web development studio based in Boise, Idaho. We want to bring affordable website solutions to Idaho where overpricing for simple websites is rampant. We can provide cheap static websites for smaller companies wanting to get their name into the area. We can accomplish this through rapid development and free web hosting for static websites which will empower local businesses to get their name out there.
                  </v-card-text>
                </v-card>
              </v-flex>
              <v-flex xs12 sm4 offset-sm1>
                <v-card class="elevation-0 transparent">
                  <v-card-title primary-title class="layout justify-center">
                    <div class="headline">Contact Us Today!</div>
                  </v-card-title>
                  <v-card-text>
                    Let us know how we can help you and we can setup a schedule to achieve what you need!
                  </v-card-text>
                  <v-form v-model="valid" ref="form" method="POST" action="http://formspree.io/xeno.cmills@gmail.com" lazy-validation>
                    <v-text-field
                      label="Name"
                      type="text"
                      name="Full Name: "
                      v-model="name"
                      :rules="nameRules"
                      required
                    ></v-text-field>
                    <v-text-field
                      label="E-mail"
                      type="email"
                      name="E-mail Address: "
                      v-model="email"
                      :rules="emailRules"
                      required
                    ></v-text-field>  
                    <v-text-field
                      name="Message: "
                      label="Message"
                      textarea
                    ></v-text-field>

                    <v-text-field
                       type="hidden" 
                       name="_next" 
                       value="http://www.xeno-studios.com"
                    ></v-text-field>

                    <v-btn
                      @click="submit"
                      type="submit"
                      value="Send"
                    >
                      submit
                    </v-btn>
                </v-form>
                </v-card>
              </v-flex>
            </v-layout>
          </v-container>
        </section>

        <xeno-footer />
      </v-content>
    </main>
  </v-app>
</template>

<script>
import Footer from '@/components/Footer'

export default {
  name: 'Home',
  data () {
    return {
      title: 'Xeno-Studios'
    }
  },
  components: {
    'xeno-footer': Footer
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
