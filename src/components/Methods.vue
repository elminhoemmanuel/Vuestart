<template>
    <div>
        <!-- <h2>{{count}}</h2>
        <button @click="incrementCount">Increase Count</button>
        <h2>{{firstName}}</h2>
        <button @click="changeName">Change Name</button> -->
        <!-- <input type="text" v-model="fName">
        <input type="text" v-model="lName"> -->
        <input type="text" v-model="first">
        <input type="text" v-model="last">
        <input type="text" v-model="options.hero">
        <!-- <h2>{{fullName}}</h2> -->
    </div>
</template>

<script>
    import { reactive, toRefs, watch } from "vue"

    export default {
        name:"Methods",
        setup(){
            // const count = ref(0)

            // function incrementCount() {
            //     count.value += 1
            // } 

            // const state = reactive({
            //     firstName: "Jake",
            //     lastName: "jafe",
            // })

            // function changeName() {
            //     state.firstName = "Jamal"
            //     state.lastName = "Jones"
            // } 

            // const fName = ref("")
            // const lName = ref("")

            // const fullName = computed(function (){
            //     return `Full Name is ${fName.value} ${lName.value}`
            // })

            // watch([fName,lName], (oldValues, newValues)=>{
            //     console.log("fname old", oldValues[0])
            //     console.log("lname old", oldValues[1])
            //     console.log("fname new", newValues[0])
            //     console.log("lname new", newValues[1])
            // },{ immediate : true})

            const state = reactive({
                first:"",
                last:"",
                options:{
                    hero:""
                }
            })

            // watch(()=>{
            //     return { ...state}
            // }, (oldValue, newValue)=>{
            //     console.log("fname old", oldValue.first)
            //     console.log("lname old", oldValue.last)
            //     console.log("fname new", newValue.first)
            //     console.log("lname new", newValue.last)
            // })
            watch(()=>state.options.hero, (oldValue, newValue)=>{
                console.log("hero old", oldValue)
                console.log("hero new", newValue)
            })


            return{ 
                // count,
                // incrementCount,
                // ...toRefs(state),
                // changeName,  
                // fName,
                // lName,
                // fullName
                ...toRefs(state)                                                                                                                   
            }
        }
    }
</script>

<style scoped>

</style>