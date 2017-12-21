<template>
    <div class="ft-nav">
        <div class="menu">
            <ul class="list">
                <li class="item">
                    <router-link to="/">
                        <i class="iconfont">&#xe604;</i>
                        <span class="txt">首页</span>
                    </router-link>
                </li>
                <li class="item">
                    <router-link to="/Invest">
                        <i class="iconfont">&#xe603;</i>
                        <span class="txt">投资</span>
                    </router-link>
                </li>
                <li class="item">
                    <router-link to="/Discover">
                        <i class="iconfont">&#xe75d;</i>
                        <span class="txt">发现</span>
                    </router-link>
                </li>
                <li class="item">
                    <router-link to="/My">
                        <i class="iconfont">&#xe668;</i>
                        <span class="txt">我的</span>
                    </router-link>
                </li>
            </ul>
        </div>
    </div>
</template>
<script>
export default {
    data() {
        return {
            isActive: false
        }
    }
}
</script>
<style lang="scss" scoped>
@import '../assets/scss/icon.scss';
.ft-nav {
    position: fixed;
    bottom: 0;
    left: 0;
    width: 100%;
    background-color: rgba(255, 255, 255, .9);
    border-top: 1px solid #E5E5E5;
}

.ft-nav ul {
    white-space: nowrap;
    overflow-x: auto;
    display: flex;
    display: -webkit-box;
    display: -webkit-flex;
    width: 100%;
    padding: 2px 0;
    -webkit-overflow-scrolling: touch;
}

.ft-nav ul li {
    display: inline-block;
    -webkit-flex: 1;
    -webkit-box-flex: 1;
    flex: 1;
    text-align: center;
    vertical-align: middle;
}

.ft-nav ul li span {
    color: #888887;
}

.router-link-exact-active {
    .txt {
        color: #119df8;
    }
    .iconfont {
        color: #119df8;
    }
}

.router-link-exact-active:hover {
    text-decoration: none;
}
</style>