<template>
    <div>
        <button @click="toggleModal">Modal ON</button>
        <teleport to='body'>
            <div v-show="showed" class="modal">
                <h2>Title Of Modal</h2>
                <p>Lorem ipsum dolor sit amet  prov id aliqolor, ex nobis iusto.</p>
                <button @click="toggleModal">Close Modal</button>
            </div>
        </teleport>
    </div>
</template>

<script>
export default {
    data() {
        return {
            showed: false
        }
    },
    methods: {
        toggleModal() {
            this.showed = !this.showed;
        }
    }
}
</script>