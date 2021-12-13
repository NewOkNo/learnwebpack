<template>
<div>
  <!-- <todo-example></todo-example> -->
    <!--<button class="button is-primary" @click="active=true">Click me</button>
    <button class="button is-primary" @click="active2=true">Click me 2</button>
    <modal v-if="active" @close="active=false" img="http://placekitten.com/800/600"></modal>
    <modal v-show="active2" @close="active2=false" img="http://placebear.com/800/600"></modal>-->
    <tabs :tabArray="tabArray" @tabclick="changeTab($event, tabArray)"></tabs>
    <tabs :tabArray="tabArray2" @tabclick="changeTab($event, tabArray2)"></tabs>
</div>
</template>

<script>
import Modal from './components/Modal.vue'
import Tabs from './components/Tabs.vue'
import TodoExample from './components/TodoExample.vue'
export default {
    components: { TodoExample, Modal, Tabs },
    data() {
        return {
            active: false,
            active2: false,
            tabArray: [
                {
                    id: 0,
                    name: 'tab1',
                    active: true
                },
                {
                    id: 1,
                    name: 'tab2',
                    active: false
                }
            ],
            tabArray2: [
                {
                    id: 0,
                    name: 'tab1',
                    active: true
                },
                {
                    id: 1,
                    name: 'tab2',
                    active: false
                },
                {
                    id: 2,
                    name: 'tab3',
                    active: false
                }
            ]
        }
    },
    methods: {
        changeTab(id, tabArray) {
            tabArray.forEach(tab => tab.active = tab.id!==id ? false : true)
        }
    }
}
</script>

<style>

</style>