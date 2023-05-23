<template>
    <ContentField>
        My Bot
    </ContentField>
</template>

<script>
import ContentField from '../../../components/ContentField.vue'
import $ from 'jquery'
import { useStore } from 'vuex';

export default {
    components: {
        ContentField
    }, 
    setup() {
        const store = useStore();
        // $.ajax({
        //     url: "http://127.0.0.1:3000/user/bot/add/", 
        //     type: "POST", 
        //     data: {
        //         title: "Bot's Title", 
        //         description: "Bot's Description", 
        //         content: "Bot's Code",
        //     }, 
        //     headers: {
        //         Authorization: "Bearer " + store.state.user.token, 
        //     }, 
        //     success(resp) {
        //         console.log(resp);
        //     }, 
        //     error(resp) {
        //         console.log(resp);
        //     }
        // })

        // $.ajax({
        //     url: "http://127.0.0.1:3000/user/bot/remove/", 
        //     type: "POST", 
        //     data: {
        //         bot_id: 6, 
        //     }, 
        //     headers: {
        //         Authorization: "Bearer " + store.state.user.token, 
        //     }, 
        //     success(resp) {
        //         console.log(resp);
        //     }, 
        //     error(resp) {
        //         console.log(resp);
        //     }
        // })

        // $.ajax({
        //     url: "http://127.0.0.1:3000/user/bot/update/", 
        //     type: "POST", 
        //     data: {
        //         bot_id: 3, 
        //         title: "Bot's", 
        //         description: "Bot's Description", 
        //         content: "Bot's Code",
        //     },
        //     headers: {
        //         Authorization: "Bearer " + store.state.user.token, 
        //     }, 
        //     success(resp) {
        //         console.log(resp);
        //     }, 
        //     error(resp) {
        //         console.log(resp);
        //     }
        // })

        $.ajax({
            url: "http://127.0.0.1:3000/user/bot/getList/", 
            type: "get", 
            headers: {
                Authorization: "Bearer " + store.state.user.token, 
            }, 
            success(resp) {
                console.log(resp);
            }, 
            error(resp) {
                console.log(resp);
            }
        })
    }
}
</script>

<style scoped>
</style>