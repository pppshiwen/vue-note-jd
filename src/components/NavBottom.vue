<template>
  <div class="footer">
  	<footer class="fixBottomBox">

    <tabbar>
        <tabbar-item link="/note" selected>
            <span slot="label">笔记</span>
        </tabbar-item>
        <tabbar-item link="/home">
            <span slot="label">商城</span>
        </tabbar-item>
        <tabbar-item link="/public">
            <span slot="label">
                <x-icon type="ios-plus" size="30">发布</x-icon>
            </span>
        </tabbar-item>
        <tabbar-item link="/cart">
            <span slot="label">购物车</span>
        </tabbar-item>
        <tabbar-item link="/mine">
            <span slot="label">我</span>
        </tabbar-item>
    </tabbar>

 
        <!-- <ul>
            <router-link tag="li" to="/note" class="tabItem">
            	<a href="javascript:;" class="tab-item-link">
                   
                    <span>笔记</span>
                </a>
            </router-link>
            <router-link tag="li" to="/home" class="tabItem">
                <a href="javascript:;" class="tab-item-link">
                   
                    <span>商城</span>
                </a>
            </router-link>
            <router-link tag="li" to="/cart" class="tabItem">
                <a href="javascript:;" class="tab-item-link">
                    
                    <span>购车</span>
                </a>
            </router-link>
            <router-link tag="li" to="/mine" class="tabItem">
                <a href="javascript:;" class="tab-item-link">
                    
                    <span>我</span>
                </a>
            </router-link>
        </ul> -->

    </footer>
  </div>
</template>
<script>
    import { Tabbar, TabbarItem, Group, Cell } from 'vux'

    export default {
    components: {
        Tabbar,
        TabbarItem,
        Group,
        Cell
    }
    }
</script>
<style >
.weui-tabbar__item.weui-bar__item_on .weui-tabbar__icon, .weui-tabbar__item.weui-bar__item_on .weui-tabbar__icon > i, .weui-tabbar__item.weui-bar__item_on .weui-tabbar__label{
    color:brown !important; 
    font-size: 16px;
}
.vux-x-icon {
    fill: rgb(199, 68, 68);

}
.vux-x-icon {
    width:50px;
    height: 50px;
}
   

</style>
