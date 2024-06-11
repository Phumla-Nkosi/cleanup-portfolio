<template>
  <div class="home">
    <h1>Hello, I'm Phumla Nkosi</h1>
    <h2>iOS Up coming Software Developer {{ experienceYear }} year of experience in </h2>
  </div>
</template>

<script>
import { ref, onMounted } from 'vue'
export default {
  name: 'Home',
  setup() {
    const experienceYear = ref(0)
    const calculateExperienceYearFrom = (date) => {
      const today = new Date()
      const year = today.getFullYear() - date.getFullYear()
      return year
    }

    onMounted(() => {
      experienceYear.value = calculateExperienceYearsFrom(new Date("2024-06-11"))
    })

    return {
      experienceYear,
      calculateExperienceYearFrom
    }
  },
  components: {
    
  },
}
</script>
