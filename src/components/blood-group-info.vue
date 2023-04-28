<template>
        <table >
            <tbody>
                <tr>
                    <th class="heading">BLOOD TYPE</th>
                    <th class="heading">DONOR</th>
                    <th class="heading">RECIPIENT</th>
                    <th class="heading">PERSONALITY</th>
                    <th class="heading">% IN WORLD </th>
                </tr>
                <tr v-for="bloodGroup in bloodGroups" :key="bloodGroup.blood_type" >
                    <td>{{bloodGroup.blood_group}}</td>
                    <td>{{bloodGroup.donor}}</td>
                    <td>{{bloodGroup.recipient}}</td>
                    <td>{{bloodGroup.personality}}</td>
                    <td>{{bloodGroup.percentage_people_in_world}}</td>
                </tr>
            </tbody>
        </table>
</template>

<script>
    export default {
        props: {
            bloodGroups: Array
        }
    }
</script>
<style>
table{
    margin: auto;
    border-collapse: separate;
    border-spacing: 0;
    white-space: normal;
    overflow: hidden;
    border: 1px solid darkgrey;
}
tr, th, td{
    padding: 10px 15px;
    text-align: left;
    border: 1px solid darkgrey;
    font-weight: 500;
}
tr:nth-child(1) {
    background-color: black !important;
    color: #fff;
}
tr:nth-child(odd) {
    background-color: bisque;
}
.heading{
    min-width: 100px;
    font-weight: bold;
}
</style>