<template>
  <div id="app">
    <h1>YouTube Moments</h1>
    <SearchBar @search="search" />
    <ResultList :results="results"/>
  </div>
</template>

<script>
import SearchBar from './components/SearchBar.vue'
import ResultList from './components/ResultList.vue'

export default {
  name: 'App',
  components: {
    SearchBar,
    ResultList
  },
  data () {
    return {
      results: [
        {
          vid: 'j_MXSE3wUT4',
            title: 'Jordan Peterson\'s Critique of the Communist Manifesto',
            channel: 'Jordan B Peterson',
            excerpts: [
                {
                    text: 'Marx was a narcissist! So narcissistic... Good thing I\'m not a narcissistic thinker! I know I\'m not... Really these quotes should be longer, so I\'ll just manually make them so.',
                    timestamp: '1:23:44 – 1:24:35'
                },
                {
                    text: 'This is the second excerpt. Shorter than the previous, but still of a decent length. Realistically, these excerpts will be longer.',
                    timestamp: '1:23:44 – 1:24:35'
                },
            ],
        }, {
            vid: 'AcfeMxUs-xo',
            title: '(Drums) Parallel Processing "Drum Dirt" Bus | One Track Or Entire Kit',
            channel: 'pureMix',
            excerpts: [
                {
                    text: 'and there might as well be another quote from this video with yet again more of your search terms highlighted. This one actually does include more text. This is probably more of the size that the quotes will actually be, if not even longer',
                    timestamp: '1:23:44 – 1:24:35'
                },
            ],
        }, {
            vid: 'RennZ2vwY74',
            title: 'Everything You Need to Know About CRYPTO, & How to Gain WEALTH In the BITCOIN REVOLUTION | Raoul Pal',
            channel: 'Tom Bilyeu',
            excerpts: [
                {
                    text: 'A quote from this video with your search terms highlighted. Probably a lot more text too.',
                    timestamp: '1:23:44 – 1:24:35',
                },
                {
                    text: 'Another quote from this video with even more of your search terms highlighted. Also will include more text”',
                    timestamp: '1:23:44 – 1:24:35',
                },
                {
                    text: 'and there might as well be another quote from this video with yet again more of your search terms highlighted. This one actually does include more text. This is probably more of the size that the quotes will actually be, if not even longer',
                    timestamp: '1:23:44 – 1:24:35',
                }
            ],
        }
      ]
    }
  },
  methods: {
    search(query) {
      console.log('Searching: ' + query)
    }
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css?family=Roboto');
#app {
  /* font-family: Avenir, Helvetica, Arial, sans-serif; */
  font-family: 'Roboto';
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
