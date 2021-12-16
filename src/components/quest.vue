<template> 
<section class="title">
        <div class="vertical-center">
            <div class="container">
              <div class="d-flex justify-content-center name-title">                    
                        <div>
                            <h1 > {{this.name_at}} </h1>
                        </div>
                        <div>
                            <span > {{this.name}} </span>
                        </div>                        
              </div>
            </div>        
        <div class="deac-q">
          <p>{{this.text_desc}} </p>
        </div>
      </div>
   </section>
</template>

<script>
export default {
  name: "Quest",
  props: ['quests'],
    data() {
    return {
      id: null,
      name_at:null,
      name:null,
      text_desc:null
    }
  },
  created() {
    this.id = this.$route.params.id,
    this.name_at = this.$route.params.name_at,
    this.name = this.$route.params.name,
    this.text_desc= this.$route.params.text_desc
  }
}
</script>