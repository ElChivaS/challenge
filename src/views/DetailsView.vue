<template>
  <div>
    <MovieDetails />
  </div>
</template>

<!--
<style lang="scss">
.card {
  align-self: center;
  margin-top: 46px;
  width: 45%;

  .card-body {
    display: flex;
    justify-content: space-between;
    align-items: flex-end;
  }

  #plot {
    padding: 9px 23px;
    text-align: left;
  }
}
.rounded-start {
  border-bottom-left-radius: 0!important;
}
</style>-->
<style>
.card {
  align-self: center;
  margin-top: 46px;
  width: 50%;
} 
  .card-body {
    display: flex;
    align-items: flex-end;
    flex-direction: row;
    justify-content: space-between;
  }
  .card-title {
    font-size: 1.5em;
  }
  .card {
    border: none;
    border-radius: none;
  }
  #plot {
    text-align: left;
    padding: 9px 23px;
    /* width: 90%;
    font-size: 1.5em;
    font-weight: 200; */
  }
  .rounded-start {
    border-bottom-left-radius: 0!important;
  }
</style>


<script>
import MovieDetails from '@/components/MovieDetails.vue';

export default {
  name: "DetailsView",

  components: {
    MovieDetails
  }

}
</script>

