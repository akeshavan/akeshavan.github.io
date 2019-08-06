<template>
  <div class="awards container-fluid">
    <div class="row mt-3">
      <div class="col-12">
        <teach-card v-for="t in filteredTeaching"
         :title="t.title"
         :year="t.year"
         :desc="t.desc"
         :tags="t.tags"
         :loc="t.location"
         :lesson="t.lesson"
         type="awards"
        >
        </teach-card>
      </div>
    </div>
  </div>
</template>

<script>
import teachCard from './TeachCard';

export default {
  name: 'Awards',
  components: { teachCard },
  props: ['filter'],
  computed: {
    filteredTeaching() {
      return this.teaching.filter(def =>
        def.title.toLowerCase().includes(this.filter.toLowerCase()) ||
        def.tags.toLowerCase().includes(this.filter.toLowerCase()) ||
        def.desc.toLowerCase().includes(this.filter.toLowerCase())
      );
    },
  },
  data() {
    return {
      teaching: [
        {
          title: 'Sage Young Investigator',
          year: 2019,
          desc: 'Young investigator award for the Sage Assembly',
          tags: 'open science, deep learning, citizen science, medical imaging',
          location: 'Seattle, WA',
          lesson: null,
        },
        {
          title: 'Amazon Web Services Cloud Credits for Research',
          year: 2018,
          desc: 'Awarded 15,000$ from AWS for research in human in the loop deep learning for crowdsourced image segmentation.',
          tags: 'deep learning, citizen science, medical imaging',
          location: 'Seattle, WA',
          lesson: null,
        },
        {
          title: 'Open Bioinformatics Foundation Travel Grant',
          year: 2018,
          desc: 'Awarded a travel grant to attend the eLife Innovation Sprint in Cambridge, England, May 10-11.',
          tags: 'travel award, web technology',
          location: 'Cambridge, UK',
          lesson: null,
        },
        {
          title: 'NVIDIA Corporation GPU Seed Grant',
          year: 2017,
          desc: 'Awarded a TitanXP NVIDIA GPU for research in deep learning for medical images.',
          tags: 'deep learning',
          location: 'Seattle, WA',
          lesson: null,
        },
        {
          title: 'Postdoctoral Fellowship in Neuroengineering and Data Science',
          year: 2017,
          desc: `Joint WRF Innovation Postdoctoral Fellowship in
          Neuroengineering and Data Science at the University of
          Washington eScience Institute and the Institute of Neuroengineering
          (UWIN) `,
          tags: 'fellowship, data science',
          location: 'Seattle, WA',
          lesson: null,
        },
        {
          title: 'Precision Health Science TL1 Postdoctoral Fellowship Training Program (PRESCIENT)',
          year: 2017,
          desc: 'Sadly, I had to decline this fellowship because I chose to take the WRF Innovation Postdoctoral Fellowship',
          tags: 'fellowship, precision medicine',
          location: 'San Francisco, CA',
          lesson: null,
        },
        {
          title: 'Brainhack Travel Award',
          year: 2016,
          desc: `Awarded a travel award from the Organization
          for Human Brain Mapping Open Science Special Interest Group to
          attend the annual Hackathon`,
          tags: 'travel award, hackathon',
          location: 'Lausanne, Switzerland',
          lesson: null,
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
