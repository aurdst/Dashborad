<template>
  <!-- stats -->
  <div id="HomePage">
    <b-row class="w-50 mx-auto py-5">
      <b-col>
        <company-data></company-data>
      </b-col>
    </b-row>
    <b-row class="w-60">
      <b-col cols="10" class="mx-auto">
        <onglet-data></onglet-data>
      </b-col>
    </b-row>
  </div>
</template>

<script>
import ongletData from '../components/ongletData.vue'
import companyData from '../components/companyData.vue'

  export default {
  components: { ongletData, companyData },
    data() {
      return {
        name: 'HomeView',
        components: {ongletData}
      }
    }
  }
</script>