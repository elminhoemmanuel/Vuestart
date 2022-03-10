<template>
    <div>
        {{firstName}} {{lastName}}
    </div>
</template>

<script>
    import { reactive, toRefs } from 'vue'

    export default {
        name:"Demo",
        setup(){
            const state = reactive({
                firstName: "James",
                lastName: "Amodu",
            })

            setTimeout(() => {
                state.firstName = "Jude"
                state.lastName = "Joshua"
            }, 2000);

            return toRefs(state)
        }
    }
</script>

<style scoped>

</style>