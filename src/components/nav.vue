<template>
    <div>
        <header>
            <nav>
                <section class="logo">
                    <h1>GoBlog</h1>
                </section>
                <section class="logout">
                    <p @click="logout()">Logout</p>
                </section>
            </nav>
        </header>
    </div>
</template>

<script>
export default {
    name : "Nav",
    methods:{
        logout(){
            this.$router.push({name:'Login'})
        }
    }
}
</script>

<style scoped>
nav{
    display:flex;
}
header{
    padding-top:15px;
    padding-bottom:15px;
    width:100%;
    position:fixed;
    /* bottom:20px; */
    background:white;
}
nav{
    width:90%;
    margin:auto;
}
.logo,.logout{
    flex:1;
}
.logout{
    display: flex;
    justify-content: flex-end;
}
.logout p{
    color:red;
    cursor:pointer;
}
</style>