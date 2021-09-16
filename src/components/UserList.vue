<template>
  <select>
    <option v-for="(member, index) in members" :value="member.id" :key="member.id">{{ member.name }}</option>
  </select>
</template>

<script>
import axios from 'axios'

export default {
  data () {
    return {
      users: [1, 2, 3, 4, 5],
      members: [],
      info: null
    }
  },

  mounted () {
    axios
      .get('https://wordpress-487479-2160705.cloudwaysapps.com/wp-json/wp/v2/members')
      .then(response => {
        response.data.forEach(member => {
          this.members.push({
            'id': member.slug,
            'name': member.title.rendered
          })
        })
      });
  }
}
</script>

<style>

</style>