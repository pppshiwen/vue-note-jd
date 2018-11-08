<template>
    <div class="comment">
        <header class="">
            <div class="container">
                <div class="row">
                    <div class="">
                        <divider> <h1>请发表评论{{noteDetail.user_name}}</h1> </divider>
                    </div>
                </div>
            </div>
        </header>
        <div class="container">
            <add :add-comment="addComment"/>
            <list :comments="comments" :delete-comment="deleteComment"/>
        </div>
    </div>
</template>
<script>
    import { Divider } from 'vux'
    import add from './commentAdd.vue'
    import list from './commentList.vue'
  export default {
      props:[
          'noteDetail'
      ],
      data () {
          return {
              comments: []
          }
      },
      components: {
          add,
          list,
          Divider
      },
    methods: {
          addComment (comment) {
              this.comments.unshift(comment)
          },
          deleteComment (index) {
              this.comments.splice(index, 1)
          }
    },
    // 模拟Ajax发送请求
    created () {
          setTimeout(() => {
             const comments = [
                 {
               username: '明珠阿姨',
               user_photo:'https://p1.ssl.qhmsg.com/dr/220__/t0147dbf3700a1125a3.jpg',
               content: '我们格力都没有你优秀'
             },
             {
                 username: '建林伯伯',
                 user_photo:'https://gss1.bdstatic.com/-vo3dSag_xI4khGkpoWK1HF6hhy/baike/s%3D220/sign=ff2a3d6ff0d3572c62e29bdeba116352/2934349b033b5bb53c114a7834d3d539b700bc76.jpg',
                 content: '可以像吾儿一样红'
             }
             ]
            this.comments = comments
          }, 1000)
    }
 }
</script>
<style scoped>
.comment{
    margin-bottom: 50px;
}


</style>
