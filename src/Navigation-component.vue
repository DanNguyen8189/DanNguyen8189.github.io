<template>
    <div id = 'navigation'>
        <bar-menu id = 'bar-menu' :selected = selected :menuItems = menuItems></bar-menu>
        <drop-down-menu id = 'drop-down' :selected = selected :menuItems = menuItems></drop-down-menu>
    </div>
</template>

<script>
export default{
    data(){
        /*We're passing this data down to the bar menu and drop-down menu*/
        return{
            /*For styling the active button*/
            selected: 'HOME',
            /*Array of menu items to be rendered*/
            menuItems: [{id: 'HOME', route: '/'}, 
                        //{id: 'ABOUT', route: '/about' },   
                        {id: 'PROFILE', route: '/profile'}, 
                        {id: 'CONTACT', route: '/contact'}]
        }
    },
}
</script>
<style scoped>

#navigation{
    text-align: right;
    font-size: 200%;
    font-family: 'Actor', sans-serif;
    background-color: rgba(0,0,0,0.05);
    transition: color linear 0.15s;
}
@media screen and (min-aspect-ratio: 1/1) {
    #navigation{
        font-size: 150%;
    }
    #bar-menu {
        width:100%;
        box-shadow:0px 1px 1px rgba(255, 255, 255, 0.30);
        border-radius:3px;
    }
}
@media screen and (max-aspect-ratio: 1/1) {
    #bar-menu{
        display: none;
    }
}
</style>

