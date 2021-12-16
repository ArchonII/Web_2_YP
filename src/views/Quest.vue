<template>
    <div>     

        <section>
            <div class="container">
                <div v-for="item in answers"  v-bind:key="item.id" class="row ansv-q answer-item">
                    <div class="col-md-2 nm_a cent">
                        <p>{{item.name_at }} </p>
                    </div>
                    <div class="col-md-2 t-ansv">
                        <p>{{item.text_ans }} </p>

                    </div>
                </div>               
                <form>
                    <p><b>Введите ваш ответ:</b></p>
                    <p><textarea rows="10" cols="45" name="text"></textarea></p>
                    <p><input class="btn btn-primary " type="submit" value="Отправить"></p>
                </form>

            </div>
        </section> 
    </div>
</template>


<script>
import answers from "../components/quest.vue"
export default (
{
  name: "Quest",
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
},
{
    name: "Answer",
    components: {answers},
    data(){
      return{
        answers: [
        {
          id: 1,
          name_at: "name author 1",
          text_ans: "text of answer 1 author asgnbkdfnjdfglk ",        
        },
        {
          id: 2,
          name_at: "name author 2",
          text_ans: "text of answer 2 author agughnghghtkgh ",        
        },
        {
          id: 3,
          name_at: "name author 1",
          text_ans: "text of answer 1 author yiljhgjldfnglkdnhl ",        
        },
        ]
      }
    }
}
)
</script>