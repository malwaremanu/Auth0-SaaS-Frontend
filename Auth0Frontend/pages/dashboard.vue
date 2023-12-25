<template>
  <div>
    <!-- Dashboard component -->
  </div>
</template>

<script>
import Cookies from 'js-cookie';
import jwt_decode from 'jwt-decode';

export default {
  data() {
    return {
      tokenPayload: null,
    };
  },
  created() {
    const token = Cookies.get('token');
    this.tokenPayload = jwt_decode(token);
  },
};
</script>
