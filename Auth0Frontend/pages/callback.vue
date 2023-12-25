<template>
  <div>
    <!-- This page is used to handle the callback and store the token in a cookie. -->
  </div>
</template>

<script>
import Cookies from 'js-cookie';

export default {
  data() {
    return {
      token: null,
    };
  },
  created() {
    this.token = this.$route.query.token;
    Cookies.set('token', this.token);
    this.$router.push("/dashboard");
  },
};
</script>
