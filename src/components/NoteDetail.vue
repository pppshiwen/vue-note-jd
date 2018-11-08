<template>
	<div class="note_detail">
		<header class="top_bar">
            <a onclick="window.history.go(-1)" class="icon_back"></a>
            <h3>笔记详情</h3>
        </header>
        <main class="detail_box">
            <section >
                <ul >
                    <li class="banner_item" >
                         <img :src="'http://localhost:8086/'+noteDetail.note_pic_url" alt=""> 
                    </li>
                
                </ul>
                <div class="banner_count">
                        <em id="slide-nub" class="fz18">1</em>
                        <em class="nub-bg">/</em>
                        <em id="slide-sum" class="fz12">5</em>
                </div>

            </section>
            <section class="notes_info clearfix">
                <div class="notes_left">
                    <div class="top_userpic"> 
                        <img :src="noteDetail.user_photo" alt="">
                        <div class="uname">{{noteDetail.user_name}}</div>  
                    </div>
                </div>
                <div class="notes_right">
                        +关注
                </div>
               
                <p class="p_name">标题：{{noteDetail.note_title}}</p>
            </section>
            <section class="notes_intro">
                <p class="pro_det">
                   {{noteDetail.note_detail}}
                   
                </p>
                <span class="note_create">{{noteDetail.note_create}}</span>
                <span class="note_like">点赞次数:{{noteDetail.note_like}}</span>
           </section>
           <section class="notes_intro">
              
           </section>
            <section class="notes_intro">
                <comment :noteDetail='noteDetail'></comment>
           </section>
          
        </main>
	</div>
</template>
<script>

import comment from './comment/Comment.vue'
   export default {
       data(){
           return{
               noteDetail:{}
           }
       },
       components:{
           comment
       },
        mounted() {
            this.getDate(this.$route.params.id);
            
            
        },
        methods:{
            getDate(id){
                let _this = this;
                _this.$http.get('/notedetail/',{
                    params:{
                        noteId: id
                    }
                }).then((res)=>{
                    //console.log(res.data);
                    _this.noteDetail=res.data[0];
                    _this.noteDetail.note_create=_this.noteDetail.note_create.slice(0, 10);
                     //console.log(_this.noteDetail);
                },(err)=>{
                    console.log(err);
                })
            }
        }
   }
</script>
<style>
    @import '../assets/css/notedetail.css'
</style>