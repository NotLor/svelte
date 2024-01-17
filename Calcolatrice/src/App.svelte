<script>
  let total = 0;
  let console = '';
  let state = null;

  function setOperation(operation){

  }

  function setValue(value){

  }

  function equal(){

  }
</script>

<style>
  .calcolatrice{
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    width: 50%;
    border: 1px solid #eee;
    box-shadow: 2px 2px 2px #eee;
    padding: 20px;
  }

  .calcolatrice input{
    width: 90%;
    padding: 20px;
    outline: none;
    text-align: right;
    font-size: 20px;
  }

  .calcolatrice .buttons{
    display: flex;
    flex-wrap: wrap;
    }
</style>

<div class="calcolatrice">
  <input type="text" bind:value={console} readonly/>
  <div class="buttons">
    <div class="operations">
      <button on:click={()=>{setOperation('add');}}>
        +
      </button>
      <button on:click={()=>{setOperation('substract');}}>
        -
      </button>
      <button on:click={()=>{setOperation('multiply');}}>
        &times;
      </button>
      <button on:click={()=>{setOperation('divide');}}>
        &divide;
      </button>
    </div>
    <div class="numbers">
      <div>
        <button on:click={()=>{setValue(7);}}>
          7
        </button>
        <button on:click={()=>{setValue(8);}}>
          8
        </button>
        <button on:click={()=>{setValue(9);}}>
          9
        </button>
      </div>
      <div>
        <button on:click={()=>{setValue(4);}}>
          4
        </button>
        <button on:click={()=>{setValue(5);}}>
          5
        </button>
        <button on:click={()=>{setValue(6);}}>
          6
        </button>
      </div>
      <div>
        <button on:click={()=>{setValue(1);}}>
          1
        </button>
        <button on:click={()=>{setValue(2);}}>
          2
        </button>
        <button on:click={()=>{setValue(3);}}>
          3
        </button>
      </div>
      <div>
        <button on:click={()=>{setValue(0);}}>
          0
        </button>
        <button on:click={()=>{setValue('.');}}>
          .
        </button>
        <button on:click={equal}>
          C
        </button>
      </div>
    </div>
    <div class="equal">
      <button on:click={equal}>
        =
      </button>
    </div>
  </div>
</div>