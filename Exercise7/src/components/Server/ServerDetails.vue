<template>
    <div class="col-xs-12 col-sm-6">
        <p>Server {{server.id}}</p>
        <p>{{ server.status }}</p>
        <p v-if="server.id!=null"><button value="Fix Server" @click="fixServer()">Fix Server</button></p>
    </div>

</template>

<script>
    import { eventBus } from '../../main';

    const EMPTY_SERVER = { id : null, status: "Please select a server" };

    export default {
        data: () => {
            return {
                server :  EMPTY_SERVER
            };
        },
        methods:  {
            fixServer()  {
                // the same object so we don't need to emit.
                this.server.status = 'Normal';
            }

        },
        created() {
            eventBus.$on('serverClicked', (server) => {
                this.server = server;
            })
        }
    }
</script>


<style>

</style>
