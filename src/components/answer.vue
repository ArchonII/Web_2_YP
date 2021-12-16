<template>
    <div class="row ansv-q answer-item">
        <div class="col-md-2 nm_a cent">
            <p>{{answer.name_at }} </p>
        </div>
        <div class="col-md-2 t-ansv">
            <p>{{answer.text_ans }}</p>

        </div>
    </div>
</template> 



<script>
export default( 
{
  name: "Answer",
  data() {
    return {
      id: null,
      name_at:null,
      name:null,
      text_dans:null
    }
  },
  created() {
    this.id = this.$route.params.id,
    this.name_at = this.$route.params.name_at,
    this.name = this.$route.params.name,
    this.text_ans= this.$route.params.text_desc
  }
}
)
</script>