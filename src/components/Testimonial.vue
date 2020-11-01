<template>
  <v-container>
    <v-row class="">
      <v-col class="col-md-9">
        <v-row>
          <v-col
              v-for="(item, idx) in testimonials"
              :key="idx"
              :class="item.class"
          >
            <v-card
              v-bind="item.attrs"
              class="pa-5 mb-8"
            >
              <div class="d-flex">
                <v-avatar>
                  <v-img
                    :src="require(`@/assets/${item.avatar}`)"
                    alt="Avatar"
                  ></v-img>
                </v-avatar>
                <div class="d-flex flex-column ml-2">
                  <span>{{ item.name }}</span>
                  <span class="user-type">{{ item.userType }}</span>
                </div>
              </div>
              <v-card-title> {{ item.primaryText }} </v-card-title>
              <v-card-text> {{ item.secondaryText }} </v-card-text>
            </v-card>
          </v-col>
        </v-row>
      </v-col>
      <v-col class="col-md-3">
        <v-row>
          <v-col>
            <v-card class="pa-5" >
              <div class="d-flex">
                <v-avatar>
                  <v-img
                    :src="require('@/assets/image-kira.jpg')"
                    alt="Avatar"
                  ></v-img>
                </v-avatar>
                <div class="d-flex flex-column ml-2">
                  <span>Kira Whittle</span>
                  <span class="user-type">Verified Graduate</span>
                </div>
              </div>
              <v-card-title>
                Such a life-changing experience. Highly recommended!
              </v-card-title>
              <v-card-text>“ Before joining the bootcamp, I’ve never written a line of code. I needed some structure from
                professionals who can help me learn programming step by step. I was encouraged to enroll by a former
                student of theirs who can only say wonderful things about the program. The entire curriculum and staff
                did not disappoint. They were very hands-on and I never had to wait long for assistance. The agile team
                project, in particular, was outstanding. It took my learning to the next level in a way that no tutorial
                could ever have. In fact, I’ve often referred to it during interviews as an example of my developent
                experience. It certainly helped me land a job as a full-stack developer after receiving multiple offers.
                100% recommend! ”
              </v-card-text>
            </v-card>
          </v-col>
        </v-row>
      </v-col>
    </v-row>

  </v-container>
</template>

<script>
export default {
  name: 'Testimonial',
  data () {
    return {
      testimonials: [
        {
          attrs: {
            dark: true,
            color: 'hsl(263, 55%, 52%)'
          },
          class: 'col-md-8',
          avatar: 'image-daniel.jpg',
          name: 'Daniel Clifford',
          userType: 'Verified Graduate',
          primaryText: `I received a job offer mid-course, and the subjects I learned were current, if not more so,
            in the company I joined. I honestly feel I got every penny’s worth.`,
          secondaryText: `“ I was an EMT for many years before I joined the bootcamp. I’ve been looking to make a
            transition and have heard some people who had an amazing experience here. I signed up
            for the free intro course and found it incredibly fun! I enrolled shortly thereafter.
            The next 12 weeks was the best - and most grueling - time of my life. Since completing
            the course, I’ve successfully switched careers, working as a Software Engineer at a VR startup. ”`
        },
        {
          attrs: {
            dark: true,
            color: 'hsl(219, 29%, 14%)'
          },
          class: 'col-md-4',
          avatar: 'image-jonathan.jpg',
          name: 'Jonathan Walters',
          userType: 'Verified Graduate',
          primaryText: 'The team was very supportive and kept me motivated',
          secondaryText: `“ I started as a total newbie with virtually no coding skills. I now work as a mobile engineer 
            for a big company. This was one of the best investments I’ve made in myself. ”`
        },
        {
          attrs: {},
          class: 'col-md-4',
          avatar: 'image-jeanette.jpg',
          name: 'Jeanette Harmon',
          userType: 'Verified Graduate',
          primaryText: 'An overall wonderful and rewarding experience',
          secondaryText: `“ Thank you for the wonderful experience! I now have a job I really enjoy, and make a good living 
            while doing something I love. ”`
        },
        {
          attrs: {
            dark: true,
            color: '(217, 19%, 35%)'
          },
          class: 'col-md-8',
          avatar: 'image-patrick.jpg',
          name: 'Patrick Abrams',
          userType: 'Verified Graduate',
          primaryText: `Awesome teaching support from TAs who did the bootcamp themselves. Getting guidance from them and 
            learning from their experiences was easy.`,
          secondaryText: `“ The staff seem genuinely concerned about my progress which I find really refreshing. The program 
            gave me the confidence necessary to be able to go out in the world and present myself as a capable 
            junior developer. The standard is above the rest. You will get the personal attention you need from 
            an incredible community of smart and amazing people. ”`
        }
      ]
    }
  }
}
</script>

<style>

.v-card__text {
  font-size: 13px !important;
}

.v-card__title {
  font-size: 20px !important;
}

.user-type {
  opacity: 50%;
}
</style>
