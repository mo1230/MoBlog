<template>
  <div class="nav">
      <el-menu class="nav-menu" :default-active="active" mode="horizontal" @select="selected">
		<el-menu-item class="nav-menu-item">
			<h1>
				<router-link to="/" class="nav-link">MoBlog</router-link>
			</h1>
		</el-menu-item>
        <el-menu-item class="nav-menu-item" index="1">
			<router-link to="/" class="nav-link">主页</router-link>
		</el-menu-item>
        <el-menu-item class="nav-menu-item" index="2">
            <el-submenu class="nav-menu-item" >
                <template slot="title" class="nav-menu-item-title">前端</template>
                <el-menu-item class="nav-menu-item nav-submenu-item" index="2.1">vue</el-menu-item>
            </el-submenu>
        </el-menu-item>
      </el-menu>
      
  </div>
</template>

<script>
export default {
    data() {
        return {
            active: "1"
        }
    },
    methods: {
        selected: function (key, key_path) {
            this.active = key
        }
    }
}
</script>

<style>
	.nav {
		width: 100%;
		display: flex;
		align-items: center;
		justify-content: center;
		background-image: linear-gradient(141deg,#9fb8ad 0%,#1fc8db 51%,#2cb5e8 75%);
	}
	.nav-menu {
		border-bottom: none !important;
		background-color: transparent !important;
		margin: 0;
		width: 80%;
		height: 100%;
	}
	.nav-menu-item:hover {
		background-image: linear-gradient(141deg,#9fb8ad 0%,#1fc8db 51%,#2cb5e8 75%);
	}
	.el-submenu__title:focus, .el-submenu__title:hover, .is-active  {
		background-color: transparent !important;
		/* background-image: linear-gradient(141deg,#9fb8ad 0%,#1fc8db 51%,#2cb5e8 75%); */
	}
	.nav-submenu-item:hover {
		background-image: none;
		/* background-color: rgb(254, 254, 254) !important; */
	}
	.nav-link {
		text-decoration: none;
		color: #000 !important;
	}

</style>