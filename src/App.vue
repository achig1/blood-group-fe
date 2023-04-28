<template>
    <div class="main">
        <h1 class="text-center">Blood Group Information</h1>
        <BloodGroupList :bloodGroups="bloodGroups" />
    </div>
</template>
<script >
    import BloodGroupList from './components/blood-group-list.vue'
    export default {
        data(){
            return {
                bloodGroups: []
            }
        },
        components: { BloodGroupList  },
        methods: {
            async getDataFromAPI() {
                const res = await fetch('https://abhilash-final-project-be.onrender.com/api');
                return await res.json();
            }
        },
        mounted() {
            this.getDataFromAPI().then(res => {
                if(res){
                    this.bloodGroups = res.data;
                }
                
            })
        }
    }
</script>
<style>
h1{
    background-color: darkseagreen;
    padding: 10px
}
</style>