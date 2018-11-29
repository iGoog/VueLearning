<template>
    <div class="container">
        <div class="row">
            <div class="col-xs-12">
                <pe-serverHeader></pe-serverHeader>
            </div>
        </div>
        <hr>
        <div class="row">
            <div class="col-xs-12 col-sm-6">
                <pe-serverStatus></pe-serverStatus>
            </div>
            <div class="col-xs-12 col-sm-6">
                <pe-serverDetails></pe-serverDetails>
            </div>
        </div>
        <hr>
        <div class="row">
            <div class="col-xs-12">
                <pe-serverFooter></pe-serverFooter>
            </div>
        </div>
    </div>
</template>

<script>
    import ServerDetails from './ServerDetails.vue';
    import ServerHeader from './ServerHeader.vue';
    import ServerStatus from './ServerStatus.vue';
    import ServerFooter from './ServerFooter.vue';
    export default {
        components: {
            'pe-serverHeader' : ServerHeader,
            'pe-serverStatus' : ServerStatus,
            'pe-serverDetails' : ServerDetails,
            'pe-serverFooter' : ServerFooter

        }
    }

</script>

<style>

</style>
