<template>
          <div>
              <label>
                  <input type="checkbox" :checked="!anyRemaining" @change="allCheked">
                 Check All
             </label>
           </div>
</template>
<script>
export default {
    name:'todo-remaining',
    props:{
        anyRemaining:{
            type:Boolean,
            required:true,
        }
    },
    methods:{
        allCheked(){
            eventBus.$emit("chekedAllChanged",this.anyRemaining);
        }
    }

}
</script>