<template>
  <div class="commentadd">
    <form >
      <div class="comment-user">
        <div class="my_headerpic"><img :src="user_photo" alt=""> </div>
        <input type="text" class="form-control" placeholder="用户名" v-model="username">
      </div>
      <div class="comment-main">
        <!-- <textarea class="form-control" rows="6" placeholder="评论内容" v-model="content"></textarea> -->
        <x-textarea :max="200" placeholder="评论内容" v-model="content"></x-textarea>
      </div>
      <div class="comment-but">
        <div>
          <x-button mini plain type="warn" action-type='button' @click.native="submit">提交</x-button>
          <!-- <button type="button" class="btn btn-default pull-right" @click="submit">提交</button> -->
        </div>
      </div>
    </form>
  </div>
</template>

<script>
import { XTextarea} from 'vux'
import { XButton } from 'vux'

  export default {
      props: {
        addComment: {
            type: Function,
            required: true,
            username:String
        }
      },
      data () {
        return {
            uInfs:{},
            username:'',
            content:'',
            user_photo:''
        }
      },
      components:{
        XTextarea,
        XButton
      },
      mounted(){
        this.getUDatas();
      },
      methods:{
        getUDatas(){
          let _this = this;
          //console.log(window.sessionStorage.userInfo) 
//          {"user_id":28,"user_name":"3333","login_password":"6939d6564a2880feb56234b64d11280c","pay_password":null,"user_number":"3333","user_photo":"https://p1.ssl.qhmsg.com/dr/270_500_/t012a23393af202c19e.jpg","verification_code":null,"msg":"登录成功","status":1}
// index.js?9d48:79 最初 2
             let uInfs = JSON.parse(window.sessionStorage.userInfo);
             _this.username=uInfs.user_name;
            _this.user_photo=uInfs.user_photo;
            // console.log(_this.user_photo)
        },
        submit () {
              
                const {username, content, user_photo} = this
              // 检查用户输入
                if(!username.trim() || !content.trim()) {
                    alert('please check your WHRITE')
                  return
                }

              // 输入内容生成新的对象comment
                const comment = {username, content, user_photo}
              // 调用添加函数
                this.addComment(comment)
              // 重置清空输入框
              this.content = ''
            }
      }
      
  }
</script>

<style scoped>
.my_headerpic {
    height: 20px;
    margin-top: 5px;
    float: left;
    /* position: relative; */
}
.my_headerpic img{
    width: 30px;
    height:30px;
    border-radius: 15px;
    float: left;
}
</style>
