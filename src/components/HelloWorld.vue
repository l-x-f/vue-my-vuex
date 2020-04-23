<template>
  <div class="hello">
    <h1>HelloWorld 组件</h1>
    {{ $store.state.count }}
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  }
}
</script>
