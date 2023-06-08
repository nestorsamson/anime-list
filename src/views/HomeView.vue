<template>
  <div>
    <RecommendationView/>
    <ScheduleView/>
  </div>
</template>

<script>
// @ is an alias to /src

import RecommendationView from './Components/RecommendationView.vue'
import ScheduleView from './Components/ScheduleView.vue'

export default ({
  name: 'HomeView',
  components: {
    RecommendationView,
    ScheduleView
  },
  

})
</script>
