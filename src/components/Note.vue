<template>
    <div class="note">
        <div class="note_layout">
            <HomeHeaderView></HomeHeaderView>
           
            <NoteHeaderView></NoteHeaderView>
            <NoteMainView></NoteMainView>
        </div>
    </div>
</template>
<script>
    import HomeHeaderView from './HomeHeader.vue';
    import NoteHeaderView from './NoteHeader.vue';
    import NoteMainView from './NoteMain.vue'
    export default {
        components: {
           HomeHeaderView,
           NoteHeaderView,
           NoteMainView
        }
    }
    
</script>
<style >
    @import '../assets/css/note.css';
   
</style>
