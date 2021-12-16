<template>
<div>
    <section class="title">
        <div class="vertical-center">
             <div class="container">
                <div class="d-flex justify-content-center name-title">                    
                        <div>
                            <h1 >Список тем</h1>
                        </div>                       
                </div>
            </div>
        </div>
   </section>

    <section >
    <div class="d-flex justify-content-center">
        <router-link :to="{name: 'Newquest'}">
            <button class = "btn btn-primary btn-lg">
                Новый вопрос
            </button>
        </router-link>
        <!--<a class="btn btn-primary btn-lg" href="new_quest.html" role="button">новый вопрос</a>-->
    </div>

        <div class="list-group">
            <h1>Gamming theme</h1>
            <div v-for="item in quests"  v-bind:key="item.id" class="row ansv-q answer-item">
                <router-link class="list-group-item list-group-item-action" :to="{name: 'Quest' , params: {id: item.id, name: item.name, name_at: item.name_at, text_desc: item.text_desc}}"> {{item.name}} </router-link>
            </div>                  
        </div>
        <div class="list-group">
            <h1>Virtual Reality</h1>
            <div v-for="item in quests"  v-bind:key="item.id" class="row ansv-q answer-item">
                <router-link class="list-group-item list-group-item-action" :to="{name: 'Quest' , params: {id: item.id, name: item.name, name_at: item.name_at, text_desc: item.text_desc}}"> {{item.name}} </router-link>
            </div>        
        </div>
        <div class="list-group">
            <h1>Hard settings</h1>
            <div v-for="item in quests"  v-bind:key="item.id" class="row ansv-q answer-item">
                <router-link class="list-group-item list-group-item-action" :to="{name: 'Quest' , params: {id: item.id, name: item.name, name_at: item.name_at, text_desc: item.text_desc}}"> {{item.name}} </router-link>
            </div>      
        </div>
    </section>
</div> 
</template>

<style>


</style>

<script>

import quests from "../components/quest.vue"


export default (
{
    name: "quest",
    components: {quests},
    data(){
      return{
        quests: [
        {
          id: 1,
          name_at: "name author 1",
          name: "вопрос 1",
          text_desc: "text of quest 1 glhjljdfghjlkdfjhlkj ",        
        },
        {
          id: 2,
          name_at: "name author 2",
          name: "вопрос 2",
          text_desc: "text of quest 2 hkgjugkgithjfnrfl ",        
        },
        {
          id: 3,
          name_at: "name author 1",
          name: "вопрос 3",
          text_desc: "text of quest 3 ;jytigsdhlasasdgnldfb ",        
        },
        ]
      }
    }
}



)
</script>