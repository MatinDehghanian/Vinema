<template>
  <v-layout justify-end row class="mt-3 mr-4">
    <v-flex class="ml-5" align-self-center>
      <h1 class="font-sans font-weight-light">{{pageTitle}}</h1>
      <h5 class="font-weight-light">{{sortCriteria}}</h5>
    </v-flex>
    <v-spacer></v-spacer>

    <v-flex align-self-center class="my-3">
      <div class="text-sm-end">
        <v-tooltip top>
          <template v-slot:activator="{on}">
            <v-btn
              v-on="on"
              small
              color="primary"
              class="criteriaSelector mx-3 mt-3"
              @click="sortBy('popularity')"
            >
              <v-icon left>mdi-account-heart</v-icon>
              <span class="caption text-lowercase">بر اساس تاریخ محبوبیت</span>
            </v-btn>
          </template>
          <span>دسته بندی بر اساس محبوبیت</span>
        </v-tooltip>

        <v-tooltip top>
          <template v-slot:activator="{on}">
            <v-btn
              v-on="on"
              small
              color="primary"
              class="criteriaSelector mx-3 mt-3"
              @click="sortBy('vote_average')"
            >
              <v-icon left>mdi-star</v-icon>
              <span class="caption text-lowercase">بر اساس تاریخ  امتیاز</span>
            </v-btn>
          </template>
          <span>دسته بندی بر اساس امتیاز</span>
        </v-tooltip>
        <v-tooltip top>
          <template v-slot:activator="{on}">
            <v-btn
              v-on="on"
              small
              color="primary"
              class="criteriaSelector mx-3 mt-3"
              @click="sortBy('release_date')"
            >
              <v-icon left>mdi-calendar</v-icon>
              <span class="caption text-lowercase">بر اساس تاریخ انتشار</span>
            </v-btn>
          </template>
          <span>دسته بندی بر اساس تاریخ انتشار</span>
        </v-tooltip>
      </div>
    </v-flex>
  </v-layout>
</template>

<script>
  export default {
    props: ["pageTitle", "sortCriteria"],
    data() {
      return {};
    },
    methods: {
      sortBy(prop) {
        this.$emit(prop);
      }
    }
  };
</script>

<style scoped>
</style>
