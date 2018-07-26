<template>
  <!--<div class="hello container-fluid">-->
    <!--<div class="row mt-3">-->
      <!--<div class="col-xs-12 col-sm-12 col-md-6 col-lg-4 col-xl-4">-->
        <div class="card">
          <div class="header">
            <h4 class="title mb-2">
              <img class="img-circle" style="max-height:50px;" :src="image" alt="Card image cap">
              {{title}}
            </h4>

            <p class="category">
              {{subtitle}}
            </p>
          </div>
          <div class="content">

                <p class="category" v-if="github_link">
                  <i class="ti-github m-3"></i>
                  <span class="text-primary">
                      <a :href="github_link">Code</a>
                  </span>
                </p>

                <p class="category" v-if="publication">
                  <i class="ti-book m-3"></i>
                  <span class="text-primary">
                      <a :href="publication">Publication</a>
                  </span>
                </p>

                <p class="category" v-if="demo">
                  <i class="ti-tablet m-3"></i>
                  <span class="text-primary">
                      <a :href="demo">Demo</a>
                  </span>
                </p>

                <p class="m-3">{{content}}</p>

            <p></p>
          </div>
        </div>
      <!--</div>-->
    <!--</div>-->

  <!--</div>-->
</template>
<script>
export default {
  name: 'cardTitle',
  props: ['title', 'subtitle', 'content', 'github_link', 'publication',
          'image', 'demo']
}
</script>
