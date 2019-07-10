<template>
<div>

      <h1>{{ last_accumulators }}</h1>
</div>
</template>

<script>
import axios from 'axios'

export default {
  name: "LastAccumulators",
  created() {
    axios
      .get("http://ec2-34-239-60-25.compute-1.amazonaws.com/api/v1/accumulators_report", {
        headers: {
          Authorization: "eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjoiNDdmNjU2ZmItNTMxMS00ZmU5LWI4ZDktYzJjOWQ3OGE1NDJhIiwiZXhwIjoxNTYyNzk2NjUwfQ.MepgcGZk7KP-lYFDPNQ9jTz1NSh3mTCFo83PPksCAqM",
        },
        params: {
          query: "last_accumulators"
        }

      })
      .then(response => (this.last_accumulators = response.data));
  },
  data() {
    return {
      last_accumulators: []
    };
  }
};
</script>

<style scoped>
</style>
