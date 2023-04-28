
<template>
    <div>
        <h2>Blood Groups List</h2>
        <bloodGroupInfo :bloodGroups = "bloodGroups"  />
    </div>

</template>
<script>
    import bloodGroupInfo from './blood-group-info.vue';

    export default {
        components: {bloodGroupInfo},
        props: {
            bloodGroups: Array
        }
    }
</script>
<style>
h2{
margin: 10px 0;
text-align: center;;
}
</style>