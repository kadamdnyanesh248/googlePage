<template>
  <GooglePage msg="Welcome to my page" />
</template>

<script>
import '@fortawesome/fontawesome-free/css/all.css';
import GooglePage from '@/components/GooglePage.vue';

export default {
  name: 'MainPage',
  components: {
    GooglePage,
  },
};

</script>
<style src="@/styles/tailwind.css" />
<style src="@/styles/app.css" />
