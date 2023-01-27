<template>
    <div :class="{backdrop:navOpen}"  @click.self="navOpen=!navOpen">
        <div id="side-menu">
            <button class="side-menu-btn" @click="navOpen=!navOpen" :class="{active:navOpen}">
                <span class="top"></span>
                <span class="mid"></span>
                <span class="bottom"></span>
            </button>
            <transition name="translateX">
                <nav v-show="navOpen" @close="navOpen=!navOpen">
                    <div class="side-menu-wrapper">
                        <ul class="side-menu-list">
                            <li class="side-menu-item">
                                <RouterLink @click="navOpen=!navOpen" :to="{name: 'Home'}">Home</RouterLink>
                            </li>
                            <li class="side-menu-item">
                                <RouterLink @click="navOpen=!navOpen" :to="{name: 'About'}">About</RouterLink>
                            </li>
                            <li class="side-menu-item">
                                <RouterLink @click="navOpen=!navOpen" :to="{name: 'Projects'}">Projects</RouterLink>
                            </li>
                            <li class="side-menu-item">
                                <RouterLink @click="navOpen=!navOpen" :to="{name: 'Contact'}">Contact</RouterLink>
                            </li>
                        </ul>
                    </div>
                </nav>
            </transition>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            navOpen: false
        }
    }

}
</script>

<style scoped>
.backdrop {
    top: 0;
    position: fixed;
    background: rgba(0, 0, 0, 0.5);
    width: 100%;
    height: 100%;
}

nav {
    width: 200px;
    /* height: calc(100% - #{$headerHeight} - #{$footerHeight}); */
    background: var(--background-color-secondary);
    position: fixed;
    top: 0;
    right: 0;
    z-index: 99;
    /* box-shadow: 2px 0 3px$grey-6; */
    /* overflow-y: scroll; */
}

.side-menu-btn {
    display: block;
    width: 50px;
    height: 50px;
    background: var(--background-color-secondary);
    border: none;
    position: fixed;
    top: 0;
    right: 0;
    z-index: 100;
    appearance: none;
    cursor: pointer;
    outline: none;
}

.side-menu-btn span {
    display: block;
    width: 20px;
    height: 2px;
    margin: auto;
    background: var(--text-primary-color);
    position: absolute;
    top: 0;
    bottom: 0;
    left: 0;
    right: 0;
    transition: all .4s ease;
}

.side-menu-btn span.top {
    transform: translateY(8px);
}

.side-menu-btn span.bottom {
    transform: translateY(-8px);
}

.side-menu-btn.active .top {
    transform: rotate(45deg);
}

.side-menu-btn.active .mid {
    transform: translateX(20px) rotate(360deg);
    opacity: 0;
}

.side-menu-btn.active .bottom {
    transform: rotate(-45deg);
}

.side-menu-wrapper {
    padding-top: 50px;
}

.side-menu-list {
    padding-top: 50px;
    list-style:none;
    padding: 0;
    margin: 0;
}

.side-menu-item a {
    text-decoration: none;
    line-height: 1.6em;
    font-size: 1.6em;
    padding: .5em;
    display: block;
    color: var(--text-primary-color);
    transition: .4s ease;
}

.side-menu-item a:hover {
    background: var(--accent-bright);
    color: var(--background-color-primary);
}

.translateX-enter{
	transform:translateX(200px);
	opacity: 0;
}

.translateX-enter-active,.translateX-leave-active{
	transform-origin: top right 0;
	transition:.2s ease;
}

.translateX-leave-to{
	transform: translateX(200px);
	opacity: 0;
}
</style>