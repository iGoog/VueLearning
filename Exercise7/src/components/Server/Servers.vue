<template>
    <div class="col-xs-12 col-sm-6">
        <ul class="list-group">
            <li
                    class="list-group-item"
                    v-for="server in servers"
                    @click="serverClicked(server)">
                Server #{{ server.id }} - {{server.status}}
            </li>
        </ul>
    </div>
</template>

<script>
    import { eventBus } from '../../main';

    export default {
        data: () => {
            return {
                servers : [
                    { id : 1, status: "Normal" },
                    { id : 2, status: "Critical" },
                    { id : 3, status: "Down" },
                    { id : 4, status: "Normal" },
                    { id : 5, status: "Maintenance" }
                    ]
            };
        },
        methods:  {
                serverClicked(server)  {
                    eventBus.$emit('serverClicked', server);
                }

        } //,
        // created() {
        //     eventBus.$on('fixServer', (server) => {
        //         this.server = server;
        //     })
        // }
    }

</script>

<style>

</style>
