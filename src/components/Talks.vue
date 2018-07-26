<template>
  <div class="talks container-fluid">
    <div class="row mt-3">
      <div class="col-12">
        <teach-card v-for="t in teaching"
         :title="t.title"
         :year="t.year"
         :desc="t.desc"
         :tags="t.tags"
         :loc="t.location"
         :lesson="t.lesson"
         type="talk"
        >
        </teach-card>
      </div>
    </div>
  </div>
</template>

<script>
import teachCard from './TeachCard';

export default {
  name: 'Talks',
  components: { teachCard },
  data() {
    return {
      teaching: [
        {
          title: 'Organization for Human Brain Mapping: Symposium',
          year: 2018,
          desc: 'Reproducibility in fMRI: Web-based neuroimaging tools for reproducible and collaborative research',
          tags: 'reproducibility, fmri, neuroimaging',
          location: 'Singapore',
          lesson: 'https://docs.google.com/presentation/d/1LWWvbiycxBgl1n7KVpR-_XsA4wIbTPUXSRn0Xz-J2qk/edit?usp=sharing',
        },
        {
          title: 'Organization for Human Brain Mapping: Educational Course',
          year: 2018,
          desc: 'Hands on Deep Learning with Keras',
          tags: 'deep learning, neuroimaging',
          location: 'Singapore',
          lesson: 'http://nbviewer.jupyter.org/github/brainhack101/IntroDL/blob/master/IntroToKeras.ipynb',
        },
        {
          title: 'Seminar: Leveraging Web Technology to Address Challenges with Big Data in Neuroscience',
          year: 2018,
          desc: 'Hands on Deep Learning with Keras',
          tags: 'citizen science, deep learning, neuroimaging, data visualization',
          location: 'CRIUGM, University of Montreal',
          lesson: '',
        },
        {
          title: 'Interoperability of Cyberinfrastructure Workshop: Front-End Technologies',
          year: 2018,
          desc: 'Hands on Deep Learning with Keras',
          tags: 'web technology, data visualization',
          location: 'McGill University',
          lesson: '',
        },
        {
          title: 'Embracing Web Technology for more Open and Collaborative Science.',
          year: 2017,
          desc: 'Embracing Web Technology for more Open and Collaborative Science.',
          tags: 'web technology, data visualization, citizen science',
          location: 'National Institute of Health (NIH), Bethesda MD',
          lesson: '',
        },
        {
          title: 'Brain Imaging Analysis with Nipype.',
          year: 2017,
          desc: 'An interactive workshop on Nipype: a scalable Python-based workflow engine for neuroimaging.',
          tags: 'python, neuroimaging',
          location: 'University of Toronto, Toronto Canada',
          lesson: '',
        },
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
