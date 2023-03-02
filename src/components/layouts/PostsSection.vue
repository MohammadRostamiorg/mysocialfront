<template>
<div class="post" v-bind:key="i" v-for="i in 7">
  <img src="https://www.calliaweb.co.uk/wp-content/uploads/2015/10/600x600.jpg" alt="" class="PostImg">
  <div class="actions">
    <i class="fa-regular fa-heart LikeIcon"></i>
    <i class="fa-sharp fa-regular fa-bookmark SaveIcon"></i>
  </div>
  <p class="caption">
    Lorem ipsum dolor sit amet, consectetur adipisicing elit. Beatae consequatur debitis dicta doloremque earum, eius, eos fugiat hic incidunt iste magni modi nobis, quasi quia rem rerum sit totam voluptates?
  </p>
</div>


</template>

<script>
export default {
  name: "PostsSection.vue"
}
</script>

<style scoped>
.post .actions{
  padding: 5px;
  display: flex;
  background: #dadada;

}
.post .actions i{
  font-size: 40px;
  margin-right: 5px;
  cursor: pointer;

}


@media only screen and (max-width: 980px) {
  .post{
    display: flex;
    flex-direction: column;
  }
  .PostImg{
    width: 100%;

  }
  .post .caption{
    text-align: justify;
    padding: 10px 20px;
    background: #e6e6e6;
  }
}
</style>