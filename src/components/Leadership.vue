<template>
  <div class="leadership container-fluid">
    <div class="row mt-3">
      <div class="col-12">
        <teach-card v-for="t in teaching"
         :title="t.title"
         :year="t.year"
         :desc="t.desc"
         :tags="t.tags"
         :loc="t.location"
         :lesson="t.lesson"
         type="leadership"
        >
        </teach-card>
      </div>
    </div>
  </div>
</template>

<script>
import teachCard from './TeachCard';

export default {
  name: 'Leadership',
  components: { teachCard },
  data() {
    return {
      teaching: [
        {
          title: 'OHBM Open Science SIG Hackathon Organizer',
          year: 2018,
          desc: `Co-organizer for the OHBM Hackathon in Singapore, June 14-16.
                 This year we hosted a
                 training course in parallel to the hackathon, to teach
                 beginners the basics of data science
                for neuroimaging analysis`,
          tags: 'hackathon, neuroimaging, data science, teaching',
          location: 'Singapore',
          lesson: 'https://ohbm.github.io/hackathon2018',
        },
        {
          title: 'Brainhack San Francisco Organizer',
          year: 2017,
          desc: 'Helped organize a hackathon to study the brain, March 2-5.',
          tags: 'hackathon, neuroimaging',
          location: 'San Francisco',
          lesson: null,
        },
        {
          title: 'Bioengineering Association of Students (BEAST) Retreat Committee',
          year: '2014-2016',
          desc: 'Helped organize two annual bioengineering retreats for the UC Berkeley UCSF Joint Graduate Program in Bioengineering',
          tags: 'retreat',
          location: 'San Francisco',
          lesson: null,
        },
        {
          title: 'Bioengineering Association of Students (BEAST) Social Committee',
          year: '2014-2016',
          desc: 'Helped organize social events for the UC Berkeley UCSF Joint Graduate Program in Bioengineering',
          tags: 'retreat',
          location: 'San Francisco',
          lesson: null,
        },
        /*
        {\sl Brainhack San Francisco Organizer}: \hfill{March 2017}\\
        Helped organize a hackathon to study the brain, March 2-5.\\

        {\sl Bioengineering Association of Students (BEAST) Retreat Committee} \hfill{2014-2016}\\
        Helped organize two annual bioengineering retreats for the UC Berkeley UCSF Joint Graduate Program in Bioengineering\\

        {\sl Bioengineering Association of Students (BEAST) Social Committee} \hfill{2013-2014}\\
        Helped organize social events for the UC Berkeley UCSF Joint Graduate Program in Bioengineering\\
        */
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
