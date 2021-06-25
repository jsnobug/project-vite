<template>
  <n-button type="primary">{{ num }}</n-button>
  <n-button type="primary">{{ str }}</n-button>
  <n-button type="primary">{{ aa }}</n-button>
</template>

<script lang="ts">
import { ref, defineComponent } from 'vue'
import { num, str, aa } from '/@/hooks'
export default defineComponent({
  name: 'HelloWorld',
  props: {
    msg: {
      type: String,
      required: true
    }
  },
  components: {
  },
  setup: () => {
    const count = ref(0)
    return {
      count,
      num,
      str,
      aa
    }
  }
})
</script>

<style scoped>
a {
  color: #42b983;
}

label {
  margin: 0 0.5em;
  font-weight: bold;
}

code {
  background-color: #eee;
  padding: 2px 4px;
  border-radius: 4px;
  color: #304455;
}
</style>
