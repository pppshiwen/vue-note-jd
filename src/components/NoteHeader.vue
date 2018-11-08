<template>
    <div class="noteheader">
        <div class="note_headerlist">
            <ul>
                <li v-for="item in list"><span>{{item}}</span></li>
            </ul>
        </div>
    </div>
</template>
<script>
    export default {
        data(){
			return{
				list:[
                    '推荐',
                    '育儿',
                    '哺乳',
                    '分娩',
                    '生病',
                    '奶粉',
                    '尿布'
                ]
			}
		}

    }
</script>
<style>

</style>
