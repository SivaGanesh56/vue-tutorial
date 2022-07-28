<template>
  <h1>Hello {{ name }}</h1>
  <div v-text="role"></div>
  <div v-html="info"></div>

  <div :id="headingID">Heading</div>
  <button :disabled="isDisabled">Button</button>

  <h3 class="underline">Underlined Text</h3>
  <h3 class="underline" :class="status">Status</h3>

  <h2 :class="isPromoted && 'promoted'">Conditional Class</h2>
  <h2 :class="isSoldOut ? 'sold' : 'new'">SoldOut ? New</h2>

  <h2 :class="['promoted', 'new']">Array of classes</h2>
  <h2 :class="[isPromoted && 'promoted', isSoldOut ? 'sold' : 'new']">Array of Conditional classes</h2>
  <h2 :class="{
    promoted: isPromoted,
    new: !isSoldOut,
    sold: isSoldOut,
  }">Object Conditional classes</h2>

  <h2 :style="{
    color: highlightColor,
    fontSize: fontSize + 'px',
    padding: '20px'
  }">Inline Style</h2>
  <h2 :style="styleObject">Style Object</h2>
  <h2 :style="[basicStyleObject, successStyleObject]">Style Object</h2>

</template>

<script>

export default {
  name: 'Basic',
  data() {
    return {
      name: 'Siva',
      role: 'SDE-2',
      info: '<b>Hey, This is Siva</b>',
      headingID: 'heading',
      isDisabled: false,
      status: 'success',
      isPromoted: false,
      isSoldOut: true,
      highlightColor: 'orange',
      fontSize: 50,
      styleObject:{
        color: 'orange',
        fontSize: '50px',
        padding: '20px'
      },
      basicStyleObject: {
        color: 'blue',
        padding: '20px',
      },
      successStyleObject: {
        color: 'green',
        border: '1px solid #ccc'
      }
    }
  }
}
</script>

<style>

.underline {
  text-decoration: underline;
}

.success {
  color: green;
}

.promoted {
  font-style: italic;
}

.sold {
  color: red;
}

.new {
  color: green;
}
</style>
