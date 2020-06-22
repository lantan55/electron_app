<template>
    <ul class="menu">
        <li class="menu-item">
            <a href="#">Калькулятор</a>
        </li>
        <li class="menu-item">
            <a href="#">Техзадание</a>
        </li>
        <li class="menu-item">
            <a href="#">Проверка макета</a>
        </li>
    </ul>
</template>

<script>
  export default {
    name: 'MainMenu'
  }
</script>

<style scoped lang="scss">
    .menu{
        margin-top: 30px;
        list-style-type: none;
        &-item{
            margin-top: 15px;
            font-size: 1.5em;
            a{
                text-decoration: none;
                color: darkred;
            }
        }
    }

</style>
