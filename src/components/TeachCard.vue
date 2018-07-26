<template>
  <!--<div class="hello container-fluid">-->
    <!--<div class="row mt-3">-->
      <!--<div class="col-xs-12 col-sm-12 col-md-6 col-lg-4 col-xl-4">-->
        <div class="card">
          <div class="header">
            <h4 class="title mb-2">
              {{title}}
            </h4>

            <p class="category">
               {{year}}, {{loc}}
            </p>
          </div>
          <div class="content">
            <p>{{desc}}</p>

            <p class="category mb-3" v-if="lesson">
              <i class="ti-ruler-pencil m-3" v-if="type=='teach'"></i>
              <i class="ti-layout-slider m-3" v-else-if="type=='talk'"></i>
              <i class="ti-basketball m-3" v-else-if="type=='leadership'"></i>
              <span class="text-primary">
                  <a v-if="type=='teach'" :href="lesson">Lesson</a>
                  <a v-else-if="type=='talk'" :href="lesson">Slides</a>
                  <a v-else-if="type=='leadership'" :href="lesson">Website</a>
              </span>
            </p>

            <p v-if="tags" class="text-secondary"><i class="ti-bookmark-alt mr-3"></i> tags: {{tags}} </p>
          </div>
        </div>
      <!--</div>-->
    <!--</div>-->

  <!--</div>-->
</template>
<script>
export default {
  name: 'teachCard',
  props: ['title', 'year', 'desc', 'loc', 'tags', 'lesson', 'type']
}
</script>
