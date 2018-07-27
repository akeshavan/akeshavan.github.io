<template>
  <div class="hello container-fluid">
    <div class="row mt-3">
      <div class="col-12">
        <pub-card v-for="p in filteredPublications"
         :title="p.title"
         :authors="p.authors"
         :link="p.link"
         :year="p.year"
         :journal="p.journal"
         :tags="p.tags">
        </pub-card>
      </div>
    </div>
  </div>
</template>

<script>
import pubCard from './PubCard';

export default {
  name: 'Publications',
  components: {pubCard},
  props: ['filter'],
  computed: {
    filteredPublications() {
      return this.publications.filter(def =>
        def.title.toLowerCase().includes(this.filter.toLowerCase()) ||
        def.authors.toLowerCase().includes(this.filter.toLowerCase()) ||
        def.tags.toLowerCase().includes(this.filter.toLowerCase())
      );
    },
  },
  data() {
    return {
      publications: [
        {
          title: 'Combining citizen science and deep learning to amplify expertise in neuroimaging.',
          authors: 'Keshavan, A., Yeatman, J., and Rokem, A.,',
          link: 'http://results.braindr.us',
          year: '2018',
          journal: 'preprint (submitted)',
          tags: 'citizen science, deep learning, medical imaging, neuroimaging',
        },
        {
          title: 'A browser-based tool for visualization and analysis of diffusion MRI data.',
          authors: 'Yeatman, J.D., Richie-Halford, A., Smith, J.K., Keshavan, A. and Rokem, A.',
          link: 'https://www.nature.com/articles/s41467-018-03297-7',
          year: '2018',
          journal: 'Nature communications, 9(1), p.940.',
          tags: 'data visualization, medical imaging, neuroimaging',
        },
        {
          title: 'Human aging reduces the neurobehavioral influence of motivation on episodic memory.',
          authors: 'Geddes, M.R., Mattfeld, A.T., de los Angeles, C., Keshavan, A. and Gabrieli, J.D.',
          link: '',
          year: '2017',
          journal: 'NeuroImage.',
          tags: 'neuroimaging, mental health',
        },
        {
          title: 'Cluster Confidence Index: A Streamline‐Wise Pathway Reproducibility Metric for Diffusion‐Weighted MRI Tractography.',
          authors: 'Jordan, K.M., Amirbekian, B., Keshavan, A. and Henry, R.G.',
          link: '',
          year: '2017',
          journal: 'Journal of Neuroimaging.',
          tags: 'neuroimaging',
        },
        {
          title: 'Mindcontrol: A Web Application for Brain Segmentation Quality Control.',
          authors: 'Keshavan, A., Datta, E., McDonough, I., Madan, C., Henry, RG.',
          link: '',
          year: '2017',
          journal: 'Neuroimage.',
          tags: 'data visualization, citizen science, neuroimaging, medical imaging',
        },
        {
          title: 'Interactive Online Brain Shape Visualization.',
          authors: 'Keshavan, Anisha, Arno Klein, and Benjamin Cipollini.',
          link: '',
          year: '2017',
          journal: 'Research Ideas and Outcomes.',
          tags: 'data visualization, neuroimaging, hackathon',
        },
        {
          title: 'Mindcontrol: Organize, quality control, annotate, edit, and collaborate on neuroimaging processing results',
          authors: 'Keshavan, Anisha, Esha Datta, Ian McDonough, Chris Madan.',
          link: '',
          year: '2017',
          journal: 'Research Ideas and Outcomes.',
          tags: 'data visualization, neuroimaging, hackathon',
        },
        {
          title: 'Mindboggling Morphometry of Human Brains.',
          authors: 'Klein A, Ghosh SS., Bao F., Giard, J., Häme, Y., Stavsky E., Lee N., Rossa B., Reuter M., Chaibub Neto E., Keshavan A.',
          link: 'https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5322885/',
          year: '2017',
          journal: 'PLoS Comput Biol. 13(3): e1005350.',
          tags: 'data visualization, neuroimaging, brain morphometry',
        },
        {
          title: 'Power estimation for non-standardized multisite studies.',
          authors: 'Keshavan, A., et al. (50+ authors)',
          link: '',
          year: '2016',
          journal: 'Neuroimage.',
          tags: 'statistics, neuroimaging, brain morphometry',
        },
        {
          title: 'Association of HLA Genetic Risk Burden With Disease Phenotypes in Multiple Sclerosis',
          authors: 'Isobe, Noriko, Keshavan, Anisha, et al.',
          link: '',
          year: '2016',
          journal: 'JAMA Neurology.',
          tags: 'multiple sclerosis, neuroimaging, brain morphometry, genetics',
        },
        {
          title: 'Association Between Thoracic Spinal Cord Gray Matter Atrophy and Disability in Multiple Sclerosis.',
          authors: 'Schlaeger, R., Papinutto, N., Zhu, A. H., Lobach, I. V., Bevan, C. J., Bucci, M., ...  Keshavan, A. et al.',
          link: '',
          year: '2015',
          journal: 'JAMA Neurology.',
          tags: 'multiple sclerosis, spinal cord, medical imaging',
        },
        {
          title: 'Predicting Treatment Response from Resting State fMRI Data: Comparison of Parcellation Approaches',
          authors: 'Satrajit S. Ghosh, Anisha Keshavan, Georg Langs',
          link: '',
          year: '2013',
          journal: 'Pattern Recognition in Neuroimaging (PRNI), 2013 International Workshop on. 225-228.',
          tags: 'mental health, neuroimaging',
        },
        {
          title: 'Predicting Treatment Response in Social Anxiety Disorder From Functional Magnetic Resonance Imaging',
          authors: 'Oliver Doehrmann, PhD; Satrajit S. Ghosh, PhD; Frida E. Polli, PhD; Gretchen O. Reynolds, BA; Franziska Horn, BSc; Anisha Keshavan, BSc, et al.',
          link: '',
          year: '2012',
          journal: 'JAMA Psychiatry',
          tags: 'mental health, neuroimaging',
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
