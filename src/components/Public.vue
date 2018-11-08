<template>
	<div class="public">
		<div class="top_bar">
			<a onclick="window.history.go(-1)" class="icon_back"></a>
			<h3>发布笔记</h3>
		</div>	
	<div class="p_content">
		<form method="post" enctype="multipart/form-data" action="http://localhost:3333/noteadd">
			<div class="p_text">
				<group >
					<x-textarea name="note_title" placeholder="标题" :rows="1" >
					</x-textarea>
					<x-textarea name="note_cont" title="笔记" placeholder="来说点什么吧~" :show-counter="false" :rows="4" autosize>	
					</x-textarea>
				</group>
			</div>
			<div class="p_pic">
				<divider>提交图片</divider>
				<input type="file" name="note_pic" id="">
			</div>
			<div class="p_but">
				<divider>.</divider>
				<x-button plain type="primary" action-type="submit" class="custom-primary-red">提交</x-button>
				<!-- <button type="submit"></button> -->
			</div>
		</form>



	</div>
	</div>
</template>
<script>

import { XTextarea, Group, XInput, XButton, Divider } from 'vux'

export default {
  components: {
    XTextarea,
    Group,
    XInput,
    XButton,
    Divider
  },
  methods: {
    onEvent (event) {
      console.log('on', event)
    }
  }
}
</script>
<style>
@import '../assets/css/public.css';

</style>