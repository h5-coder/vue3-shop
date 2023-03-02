<template>
    <h1>
        hello world
        {{ data.name }}
        {{ data.age }}
        {{ age }}
    </h1>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from '@/components/HelloWorld.vue'
import { reactive, toRefs } from 'vue'

export default {
    name: 'my-home',
    setup() {
        const data = reactive({
            name: '小梁',
            age: 18
        })
        console.log(toRefs(data));
        return { data, age: data.age }
    },
    components: {
        // HelloWorld
    }
}
</script>
