<template>
  <div class="hello">
    <div class="row m-3">
      <div class="card-columns">
        <card-title v-for="p in projects"
         :title="p.name"
         :subtitle="p.tags"
         :github_link="p.code"
         :demo_link="p.demo"
         :image="p.image"
         :publication="p.publication"
         :demo="p.demo"
         :content="p.description">
        </card-title>
      </div>
    </div>
  </div>
</template>

<script>
import cardTitle from './ProjectCard';
import roygbiv from '../assets/img/roygbiv.png';
import medulina from '../assets/img/Medulina.gif'

export default {
  name: 'Projects',
  components: {cardTitle},
  data() {
    return {
      projects: [
        {'name': 'braindr',
         'tags': 'Citizen Science, Deep Learning, Medical Imaging',
         'code': 'https://github.com/OpenNeuroLab/braindr',
         'demo': 'https://braindr.us',
         'publication': 'http://results.braindr.us',
         'image': 'https://braindr.us/static/img/mainGIF.dee1125.gif',
         'description': `A mobile optimized web application for binary image classification.
         The current application is to quality control the Healthy Brain Network imaging dataset.`,
        },
        {'name': 'appstract',
         'tags': 'Citizen Science',
         'code': 'https://github.com/akeshavan/appstract',
         'demo': 'https://appstract.pub',
         'publication': null,
         'description': `A mobile-optimized web application to crowdsource
         metadata annotation of scientific publications.
         The current application is to annotate sample sizes in
         neuroimaging studies of autism.`,
         'image': 'https://media.giphy.com/media/fxR1CmdpkHMVVarKlp/giphy.gif'},
        {'name': 'metacurious',
         'tags': 'Citizen Science',
         'code': 'https://github.com/akeshavan/brainspell-neo-frontend',
         'demo': 'https://metacurious.org',
         'publication': null,
         'description': `A web application to annotate fMRI publications
         for a coordinate-based meta analysis.`,
         'image': 'https://metacurious.org/static/img/metacurious.cb8117a.svg'},
        {'name': 'braindrles',
        'tags': 'Citizen Science, Deep Learning, Medical Imaging',
        'code': 'https://github.com/npnl/braindrles',
        'demo': 'https://braindrles.us',
        'publication': null,
        'description': 'A mobile optimized citizen science application for classifying stroke lesion segmentations',
        'image': 'https://s3-us-west-1.amazonaws.com/braindrles/c0008s0029t01_slice_4.png'},
        {'name': 'whaledr',
         'tags': 'Citizen Science, Deep Learning, Oceanography',
         'code': 'https://github.com/akeshavan/whaledr',
         'demo': 'https://whale-dr.firebaseapp.com',
         'publication': null,
         'description': 'A citizen science app for classifying ocean sounds as "whale" or "not whale"',
         'image': 'https://whale-dr.firebaseapp.com/static/img/whaldrStatic.e7be1c6.png'},
        {'name': 'Mindcontrol',
         'tags': 'Citizen Science, Medical Imaging',
         'code': 'https://github.com/akeshavan/mindcontrol',
         'demo': 'https://mindcontrol-hbn.herokuapp.com',
         'publication': 'https://www.sciencedirect.com/science/article/pii/S1053811917302707?via%3Dihub',
         'description': `A web-based dashboard to organize, quality control,
         annotate, edit, and collaborate on neuroimaging processing results.
         The current application is to quality control the Healthy Brain Network
         imaging dataset.`,
         'image': 'https://camo.githubusercontent.com/ce2fe83bb999b8ed492bc5c83c7af7db0044d1b5/687474703a2f2f64787567786a6d3239303138352e636c6f756466726f6e742e6e65742f64656d6f5f676966732f6c6f67436f6e746f75722e676966'},
        {'name': 'Mindboggle',
         'tags': 'Data Visualization, Medical Imaging',
         'code': 'https://github.com/OpenNeuroLab/braindr',
         'demo': 'https://braindr.us',
         'publication': 'http://results.braindr.us',
         'description': 'A mobile optimized app for brain MRI quality control',
         'image': roygbiv},
         {'name': 'Medulina',
          'tags': 'Data Visualization, Medical Imaging, Citizen Science, Deep Learning',
          'code': 'https://github.com/akeshavan/medulina_v2',
          'demo': 'https://test.medulina.com',
          'publication': null,
          'description': `A lightweight web application for crowdsourcing biomedical image segmentation.
          Current applications include segmenting: meningiomas, stroke lesions, the dentate gyrus,
          and prostate cancer tissue images. `,
          'image': medulina},

      ],
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
