<template>
  <div class="teaching container-fluid">
    <div class="row mt-3">
      <div class="col-12">
        <div class="card">
          <div class="header">
            <h4 class="title">Overview</h4>
            <p class="category">
              I have many projects and many collaborators
            </p>
          </div>
          <div class="content">
            <p>I have many projects, and many collaborators</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data() {
    return {
      msg: 'Teaching',
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
