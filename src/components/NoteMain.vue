<template>
    <div class="notemain">
       <div class="notemain_l">
           <div class="box_big" v-for="item in noteList">
               <router-link :to="'/notedetail/'+item.note_id">
                    <div class="note_img">
                    <!-- <img :src="item.note_img" alt=""> -->
                    <img v-lazy="item.note_pic_url" alt="">  
                    </div>
                    <div class="note_title">
                        {{item.note_title}}
                    </div>
                    <div class="note_userpic"> 
                        <!-- <img :src="item.note_userpic" alt=""> -->
                        <img :src="item.user_photo" alt="">
                        <span>{{item.user_name}}</span> 
                    </div>
                    <div class="note_like">
                        <span>笔芯~{{item.note_like}}</span>   
                    </div>  
               </router-link>
                
           </div>
       </div>
       <div class="notemain_margin">
           
       </div>
    </div>
</template>
<script>
    export default {
        data(){
			return{
                noteList:[]
			}
        },
        mounted() {
            this.getDate();
            
        },
        methods:{
            getDate(){
                let _this = this;
                _this.$http.get('/note').then((res)=>{
                    //console.log(res.data);
                    _this.noteList=res.data;
                    console.log(_this.noteList);
                },(err)=>{
                    console.log(err);
                })
            }
        }
        
    }
</script>
<style>

</style>
