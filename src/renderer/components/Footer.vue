<template>
    <footer>
        <ul class="items">
            <li class="item">
                Путь: <span>{{path}}</span></li>
            <li class="item">Имя пути: <span>{{name}}</span></li>
            <li class="item">Платформа: <span>{{platform}}</span></li>
        </ul>
    </footer>
</template>

<script>
  export default {
    data () {
      return {
        electron: process.versions.electron,
        name: this.$route.name,
        path: this.$route.path,
        platform: require('os').platform(),
        vue: require('vue/package.json').version
      }
    }
  }
</script>

<style scoped lang="scss">
    footer {
        position: fixed;
        bottom: 0;
        width: 100%;
        height: 50px;
        padding-top:10px;
        border-top: 1px solid #888;
    }


    ul.items {
        list-style-type: none;
        display: flex;
        .item{
            margin-left: 15px;
            font-weight: normal;
            font-size: 0.7em;
            &:first-child{
                margin-left: 0;
            }
            span{
                font-weight: bold;
            }
        }
    }

</style>
