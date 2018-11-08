<template>
  <div>
    <div class="handle">
      <a href="javascript:;" @click="removeComment">删除</a>
    </div>
    <p class="user">
      <div class="my_headerpic">
        <img :src="comment.user_photo" alt="">
      </div>
      
      <span class="comment_user">{{comment.username}}:</span>
    </p>
    <p class="centence">{{comment.content}}!</p>
  </div>
</template>

<script>
  export default {
    props: {
        index: Number,
        comment: Object,
        deleteComment: Function

    },
    methods: {
      removeComment () {
          const {username} = this.comment
          if (confirm(`确定要删除${username}的评论么？`)) {
              this.deleteComment(this.index)
          }
      }
    }
  }
</script>

<style scoped>
  li{
    transition: .5s;
    overflow: hidden;
  }
  .handle{
    width: 40px;
    border: 1px solid #ccc;
    background: #fff;
    position: absolute;
    right: 10px;
    top: 1px;
    text-align: center;
  }
  .handle a{
    display: block;
    text-decoration: none;
  }
  .list-group-item .centence {
    padding: 0px 50px;
  }
  .user{
    font-size: 22px;
  }
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
    /* float: left; */
}
.comment_user{
  display: block;
  margin-top: 20px;
  line-height: 20px;
}
</style>
