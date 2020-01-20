<template>
    <header class="header">
        <div class="container">
            <h1>Tk Portfolio</h1>

            <nav>
                <ul class="gnav">
                    <li>about</li>
                    <li>skill</li>
                    <li>work</li>
                </ul>
            </nav>
        </div>
    </header>
</template>



<style lang="scss" scoped>

.header {
    padding: 30px 20px;
    box-sizing: border-box;
    box-shadow: 0 0 2px #333;
    .container {
        display: flex;
        justify-content: space-between;
        align-items: flex-end;
        .gnav {
            display: flex;
            justify-content: space-between;
            & li:not(:last-of-type){
                margin-right: 10px;
            }
        }
    }
}
</style>