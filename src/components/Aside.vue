<template>
  <v-card
        flat
        class="transparent mx-0"
        max-width="500"
  >
    <v-card-title>
      <h2>{{ aside.header }}</h2>
    </v-card-title>
    <v-card-text>
      <p>
        {{ aside.text }}
      </p>
    </v-card-text>
    <v-card-text>
      <!-- <p style="margin-left: 0!important"><b>Exactly what’s on offer:</b></p> -->
      <h5>{{ aside.offer[0].blackText }} <span class="red--text">{{ aside.offer[0].redText }}</span></h5>
      <h5>{{ aside.offer[1].blackText }} <span class="red--text">{{ aside.offer[1].redText }}</span></h5>
    </v-card-text>
    <v-card-text>
      <p class="small">
        {{ aside.smallText[0] }}
      </p>
      <p class="small">
        {{ aside.smallText[1] }}
      </p>
    </v-card-text>
  </v-card>
</template>

<style scoped>

h2 {
  color: #1A1A1A;
  letter-spacing: 0.1rem;
}
h4 {
  color: #665566;
}
.red--text {
  color: #F54436;
}
p {
  color: #665566;
}
.small {
  font-size: 14px;
}

</style>

<script>
import { mapState } from 'vuex'

export default {
  name: 'Aside',
  props: ['page'],
  data () {
    return {
      // contact: false
    }
  },
  computed: {
    ...mapState('content', ['aside'])
  },
  watch: {
    // contact (val) {
    //   if (!val) return
    //   this.$emit('update:page', 'contact')
    //   this.contact = false
    // }
  },
  mounted () {
    console.log(this.aside)
  }
}
</script>
