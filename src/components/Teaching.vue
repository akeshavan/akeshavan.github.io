<template>
  <div class="teaching container-fluid">
    <div class="row mt-3">
      <div class="col-12">
        <teach-card v-for="t in filteredTeaching"
         :title="t.title"
         :year="t.year"
         :desc="t.desc"
         :tags="t.tags"
         :loc="t.location"
         :lesson="t.lesson"
         type="teach"
        >
        </teach-card>
      </div>
    </div>
  </div>
</template>

<script>
import teachCard from './TeachCard';

export default {
  name: 'HelloWorld',
  components: { teachCard },
  props: ['filter'],
  computed: {
    filteredTeaching() {
      return this.teaching.filter(def =>
        def.title.toLowerCase().includes(this.filter.toLowerCase()) ||
        def.tags.toLowerCase().includes(this.filter.toLowerCase()) ||
        def.desc.toLowerCase().includes(this.filter.toLowerCase()) ||
        def.location.toLowerCase().includes(this.filter.toLowerCase())
      );
    },
  },
  data() {
    return {
      teaching: [
        {
          title: 'Neurohackademy',
          year: 2018,
          desc: 'Taught Introduction to D3 at neurohackweek, a summer school for neuroimaging',
          tags: 'javascript, data science',
          location: 'University of Washington, Seattle, WA',
          lesson: 'https://akeshavan.github.io/nhw2017_d3/'
        },
        {
          title: 'BrainHack School',
          year: 2018,
          desc: 'Taught Introduction to HTML, CSS, and Javascript (live coded), along with D3.',
          tags: 'javascript, data science',
          location: 'University of Montreal, Montreal, Canada',
        },
        {
          title: 'Neurohackweek',
          year: 2017,
          desc: 'Taught Introduction to D3 at neurohackweek, a summer school for neuroimaging',
          tags: 'javascript, data science',
          location: 'University of Washington, Seattle, WA',
          lesson: 'https://akeshavan.github.io/nhw2017_d3/'
        },
        {
          title: 'Hands-on Reproducible and Scalable Brain Imaging Analysis with Nipype',
          year: 2017,
          desc: 'Was an instructor at a week long course on Nipype',
          tags: 'python, neuroimaging',
          location: 'MIT, Cambridge, MA',
        },
        {
          title: 'Adjunt Professor',
          year: 2016,
          desc: 'Taught a Microsoft Excel class to first year undergraduates (3 1 unit courses).',
          tags: 'MS Excel',
          location: 'Hult Internation Business School, San Francisco, CA',
        },
        //{\sl UCSF Science and Health Education Partnership - Visiting Scientist} \hfill 2014-2015\\
        //
        {
          title: 'UCSF Science and Health Education Partnership - Visiting Scientist',
          year: 2015,
          desc: `Taught neuroscience to 3rd and 4th grade classes,
          which included lessons on the different parts of the brain
          and their functions, and included a dissection of a sheep brain.`,
          tags: 'neuroscience',
          location: 'University of California, San Francisco, San Francisco, CA',
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
