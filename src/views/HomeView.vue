<template>
  <v-app>
    
    <v-main style="background-color: #f0f0f0;"> 
      <v-container>
      <div class="ma-5 pa-5 align-center">
        <v-row>
          <v-col md="4" style="margin-top: 4%;">
            <p class="my-1" style="color: #0048D0; font: 35px Roboto,sans-serif;"> Our Services</p>
            <p>Unlock the value in every dimension of your real estate.
              A one stop solution for all your real estate needs. Using effective data driven insights and decades of
              experience, we curate personalised real estate strategies to maximise your investments.</p>
          </v-col>
          <v-row>
            <v-col class="pl-md-5" cols="12" md="5" justify="end" style="margin-top: 4%;">
              <v-responsive :aspect-ratio="682 / 1">
                <v-img src="https://agprop.in/img/service.1396b0dd.svg" alt="Service Image" cover></v-img>
              </v-responsive>
            </v-col>
          </v-row>
        </v-row>
      </div>
     
          <v-row no-gutters>
            <v-col cols="12">
              <v-card class="pa-2" outlined tile
                style="padding: 24px; font: 16px Roboto,sans-serif; border-radius: 16px !important; padding-top: 2% !important;">
                <p>We offer a broad palette of services that help both, small and large organisations, achieve their
                  vision for their working spaces and optimise their <br>productivity.
                </p>
              </v-card>
            </v-col>
            <v-col cols="12">
            </v-col>
          </v-row>
          <v-row class="my-10" justify="center">
            <v-col v-for="(item, index) in services" :key="index" cols="12" sm="6" md="6">
              <v-card class="pa-3 px-md-5" :style="{ backgroundColor: 'rgb(255, 255, 255)', borderRadius: '20px' }">
                <div class="container container--fluid role aria-haspopup aria-expanded"
                  @click="navigateToService(item.link)" style="cursor: pointer;">
                  <v-row class="align-center justify-center">
                    <v-col class="col-md-8 col-7">
                      <p class="mb-1" style="font-size: 110%;">
                        <strong>{{ item.title }}</strong>
                      </p>
                      <p class="mb-0">{{ item.description }}</p>
                      <v-btn class="mt-4" text
                        :style="{ color: 'rgb(0, 72, 208)', caretColor: 'rgb(0, 72, 208)', borderRadius: '8px', textTransform: 'capitalize' }">
                        <span class="v-btn__content">Learn More</span>
                      </v-btn>
                    </v-col>
                    <v-col class="col-md-4 col-5" style="text-align: right;">
                      <p class="mb-0" style="font-size: 500%; color: rgb(0, 72, 208);">
                        {{ item.number }}
                      </p>
                    </v-col>
                  </v-row>
                </div>
              </v-card>
            </v-col>
          </v-row>
        </v-container>
      
    </v-main>
  </v-app>
</template>

<script>
export default {
  name: 'HomeView',
  data() {
    return {
      services: [
        {
          title: 'Investment Advisory',
          description: 'Get specialized advice and find investment opportunities to fuel your future.',
          link: '/investment-advisory',
          number: '01',
        },
        {
          title: 'Asset Development & Built To Suit',
          description: 'Greatness is in the details.',
          link: '/asset-development',
          number: '02',
        },
        {
          title: 'Leasing',
          description: 'Make real estate your competitive advantage.',
          link: '/leasing',
          number: '03',
        },
        {
          title: 'Legal',
          description: 'Our In-house legal team provides comprehensive services in all aspects of property & real estate transactions.',
          link: '/legal',
          number: '04',
        },
      ],
    };
  },
  methods: {
    navigateToService(link) {
      // Add your navigation logic here
      // For example: this.$router.push(link);
      link
    },
  },
};
</script>
