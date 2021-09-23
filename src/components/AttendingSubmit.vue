<template>
  <form>
    <input type="text" name="phone" autocomplete="off" v-model="phone" />
    <input type="submit" />
  </form>
</template>

<script>
export default {
  data() {
    return {
      phone: null,
    };
  },

  methods: {
    onSubmit() {
      if (this.phone.length > 0) alert('Submitted - ' + this.phone);
      else alert('No phone number entered');
    },
  },
};
</script>

<style></style>
