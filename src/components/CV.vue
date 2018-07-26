<template>
  <div class="hello container-fluid">
    <div class="row mt-3">
      <div class="col-12">
        <iframe src="https://s3-us-west-2.amazonaws.com/akeshavan-mindcontrol/Anisha_CV_for_website.pdf"
        width="100%" style="height: calc(100vh - 100px);">
        </iframe>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data() {
    return {
      msg: 'Welcome to Your Vue.js App',
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
