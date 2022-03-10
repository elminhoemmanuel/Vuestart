<template>
    <div>
        <!-- <h2>Options - {{ o_firstName }}</h2>
        <h2>Composition - {{ c_firstName }}</h2> -->
        <h2>Composition - {{ greet }}</h2>
        <h2>Reactive - {{ greetReactive }}</h2>
    </div>
</template>

<script>
    import { ref, reactive } from 'vue'

    export default {
        setup(){
            const c_firstName = ref("Omale");
            const c_lastName = ref("Abobo");
            const c_job = ref("dev");

            const greet = `Hello ${c_firstName.value} ${c_lastName.value}, ${c_job.value}`

            const state = reactive({
                firstName:"Omale",
                lastName:"Amodu",
                job:"code bushido",
            })

            const greetReactive = `Hello ${state.firstName} ${state.lastName}, ${state.job}`

            return{ 
                c_firstName,
                c_lastName,
                c_job,
                greet, 
                greetReactive
            }
        },
        data(){
            return{
                o_firstName:"Omale",
                o_lastName:"Amodu",
                o_job:"Coder",
            }
        }
    }
</script>

<style scoped>

</style>