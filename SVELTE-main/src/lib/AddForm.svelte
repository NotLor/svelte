<script>
    import {todos} from "./store"

    let nuovoTodo

    function AddTodo() {
        todos.update((old) =>{
            old.push({
                title : nuovoTodo, 
                done : false 
            }) 
            return old
        })
    }

</script>

<div class="flex flex-col items-center">
<input type ="text" bind:value={nuovoTodo} class="input my-2 input-primary w-80"/>
<button on:click={AddTodo} class="btn btn-outline btn-primary w-1/3"> Aggiungi </button>
</div>

