<script setup>
import { VideoPlayer } from '@videojs-player/vue'
import guitarCoursePoster from 'assets/images/guitar-course.png'
import singingCoursePoster from 'assets/images/singing-course.png'
</script>

<template>
    <div class="text-center mt-6">
        <h1>This is demo test page</h1>
    </div>

    <VCard class="w-75 mx-auto mt-15 bg-grey-lighten-1">
      <VCardText>
        <VRow>
          <VCol
            cols="12"
            md="4"
          >
            <div class="d-flex flex-column align-center gap-y-4 h-100 justify-center">
              <VAvatar
                variant="tonal"
                size="52"
                rounded
                color="primary"
              >
                <VIcon
                  icon="mdi-gift"
                  size="36"
                />
              </VAvatar>
              <h4 class="mt-3">
                Today's Free Courses
              </h4>
              <p class="text-center my-5">
                We offers 284 Free Online courses from top tutors and companies to help you start or advance your career skills. Learn online for free and fast today!
              </p>
              <VBtn>Get Premium Courses</VBtn>
            </div>
          </VCol>
          <VCol
            cols="12"
            md="4"
            sm="6"
          >
            <VCard
              flat
              border
            >
              <div class="pa-2">
                <VideoPlayer
                  src="https://cdn.plyr.io/static/demo/View_From_A_Blue_Moon_Trailer-576p.mp4"
                  :poster="singingCoursePoster"
                  controls
                  plays-inline
                  :height="$vuetify.display.mdAndUp ? 200 : 150"
                  class="w-100 rounded"
                />
              </div>
              <VCardText class="pt-3">
                <h5 class="text-h5 mb-2">
                  Your First Singing Lesson
                </h5>
                <p class="text-body-1 mb-0">
                  In the same way as any other artistic domain, singing lends itself perfectly to self-teaching.
                </p>
              </VCardText>
            </VCard>
          </VCol>
          <VCol
            cols="12"
            md="4"
            sm="6"
          >
            <VCard
              flat
              border
            >
              <div class="pa-2">
                <VideoPlayer
                  src="https://cdn.plyr.io/static/demo/View_From_A_Blue_Moon_Trailer-576p.mp4"
                  :poster="guitarCoursePoster"
                  controls
                  plays-inline
                  :height="$vuetify.display.mdAndUp ? 200 : 150"
                  class="w-100 rounded"
                />
              </div>
              <VCardText class="pt-3">
                <h5 class="text-h5 mb-2">
                  Guitar for Beginners
                </h5>
                <p class="text-body-1 mb-0">
                  The Fender Acoustic Guitar is best choice for beginners and professionals.
                </p>
              </VCardText>
            </VCard>
          </VCol>
        </VRow>
      </VCardText>
    </VCard>
</template>

<style lang="scss">
@import "video.js/dist/video-js.css";
</style>