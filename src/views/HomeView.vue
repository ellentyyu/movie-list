<template>
    <main>
        <div class="container mx-auto p-4 bg-stone-100">
            <draggable 
            v-model="list" 
            group="people"
            animation="400"
            @start="drag=true;" 
            @end="drag=false"
            @move="onMove"
            item-key="id"
            class="flex flex-wrap justify-between gap-y-4">
                <template #item="{element}">
                    <div v-if="element.name" class="card flex-initial bg-indigo-200 p-5 rounded">
                        <p>{{element.name}}</p>
                    </div>
                    <div v-else class="card empty"></div>
                </template>
            </draggable>
        </div>
    </main>
</template>

<script setup>
import { ref } from 'vue'
import draggable from 'vuedraggable'
let drag = ref(false);
const chosen = ref(null);
const list = ref(
    [
      {id: 1, name: 'Item 1'},
      {id: 2, name: 'Item 2'},
      {id: 3, name: 'Item 3'},
      {id: 4, name: 'Item 4'},
      {id: 5, name: 'Item 5'},
      {id: 6, name: 'Item 6'},
      {},
      {}
    ]
)

function onMove(e) {
    console.log('move', e);
}

</script>