<template>
<!-- Every component must have only one parent element in thr tempalte file -->
<!--While exportin g defauilt we must give a name to the component-->
<!--before
 registering a compontn it must be registered in vue-->

  <div >
    <div class="alert-primary" :class="mode" role="alert">
     <slot></slot>
    </div>
  </div>
</template>

<script>
export default {
  name: "Alert",
  props:[
    'mode'
  ]

};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.alert-primary {
    color: #004085;
    background-color: #cce5ff;
    border-color: #b8daff;
    position: relative;
    padding: 50px;
    margin-bottom: 10px;
    border: 1px solid transparent;
        border-top-color: transparent;
        border-right-color: transparent;
        border-bottom-color: transparent;
        border-left-color: transparent;
    border-radius: 5px;
  
}

.danger{
  background-color:red;
}
.success{
  background-color:green;
}

</style>
