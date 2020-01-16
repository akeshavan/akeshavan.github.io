<template>
  <div class="about container">
    <div class="row mt-3">
      <div class="col-lg-6 col-md-12">
        <div class="card card-user">
            <div class="image">
                <img src="../assets/img/background.jpg" alt="...">
            </div>
            <div class="content">
                <div class="author">
                  <img class="avatar border-white" src="../assets/img/faces/anisha_pizza.jpg" alt="...">
                  <h4 class="title">Anisha Keshavan<br>
                     <a href="https://twitter.com/akeshavan_"><small>@akeshavan_</small></a>
                  </h4>
                </div>
                <p class="description text-center">
                    Senior Data Scientist
                    <br>
                    <a href="http://www.octavebio.com/">Octave Bioscience</a>
                    <br>
                </p>
            </div>
            <hr>
            <div class="text-center">
                <div class="row">
                    <div class="col-md-12">
                        <p class="description pl-2 pr-2">
                          <span class="text-info">Interests:</span>
                          Data Science,
                          Translational Medicine,
                          Citizen Science,
                          Machine Learning,
                          Medical Imaging,
                          Brain Imaging,
                          Pizza
                        </p>
                    </div>
                </div>
            </div>
        </div>

      </div>
      <div class="col-lg-6 col-md-12">
        <div class="card">
          <div class="header">
            <h4 class="title">Education</h4>
            <p class="category">
              Where I've Trained
            </p>
          </div>
          <div class="content">
            <div class="typo-line mt-3">
              <h6>
                <p class="category">Postdoc<br>2017-2018</p>
                Moore-Sloan Data Science Fellow
              </h6>
              <p class="text-muted">University of Washington</p>
              <p class="">
                <a href="https://escience.washington.edu/">eScience Institute</a> &
                <a href="http://uwin.washington.edu/">Institute for Neuroengineering</a>
              </p>
            </div>

            <div class="typo-line mt-3">
              <h6 class="mb-2">
                <p class="category">
                  PhD
                  <br>2013-2017
                </p>

                Bioengineering
              </h6>
              <p class="text-muted">University of California, Berkeley and University of California, San Francisco</p>

                <blockquote>
                  <p class="">
                    Thesis: A neuroinformatics framework for the collection, curation, and visualization of imaging biomarkers in multiple sclerosis
                  </p>
                  <small>Advisor: Roland Henry, PhD </small>
                </blockquote>


            </div>
            <div class="typo-line mt-3">
              <h6><p class="category">BS<br>2007-2011</p>Aerospace Engineering & Applied Math </h6>
              <p class="text-muted">University of California, Los Angeles</p>
              <p class="">Cum Laude, GPA: 3.7</p>
            </div>
          </div>
        </div>
      </div>
    </div>






  </div>
</template>

<script>
export default {
  name: 'About',
  data() {
    return {
      msg: 'I\'m Anisha',
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

blockquote {
    font-style: italic;
    border-left: 5px solid #eee;
    padding: 10px 20px;
    margin: 0 0 20px;
}
</style>
