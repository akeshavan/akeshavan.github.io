<template>
  <!--<div class="hello container-fluid">-->
    <!--<div class="row mt-3">-->
      <!--<div class="col-xs-12 col-sm-12 col-md-6 col-lg-4 col-xl-4">-->
        <div class="card">
          <div class="header">
            <h4 class="title mb-2">
              <a :href="link">{{title}}</a>
            </h4>

            <p class="category">
              {{authors}} ({{year}}) {{journal}}
            </p>
          </div>
          <div class="content">

            <p v-if="tags" class="text-secondary"><i class="ti-bookmark-alt mr-3"></i> tags: {{tags}} </p>

          </div>
        </div>
      <!--</div>-->
    <!--</div>-->

  <!--</div>-->
</template>
<script>
export default {
  name: 'pubCard',
  props: ['title', 'authors', 'year', 'link', 'journal', 'tags']
}
</script>
