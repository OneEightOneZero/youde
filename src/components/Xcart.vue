<template>
  <div class="menu">
    <ul class="ind_navi clearfix">
      <li >
        <a>
          <i>
            <img src="">
          </i>{{item.name}}
        </a>
      </li>
    </ul>
  </div>
</template>
<script>
export default {
	// 购物车拿token的值进行渲染
	data() {
		return {
			data:[]
		}
	},
	created() {
		this.$axios.get('https://m.youde.com/youde/f/xcx/s_10020/advertising/list?type=4 ').then((res)=>{
			this.data=res.data.data;
		});
	},
};
</script>
<style scoped>
.menu{
	width:100%;
	margin-top:57px;
	background-color:#fff;
}
.menu ul{
	padding:3% 0;
	overflow:hidden;
	text-align:center;
}
.menu ul li{
	float:left;
	min-width:72px;
	width:25%;
	margin-bottom:10px;
}
.menu ul li img{
	width:45px;
	margin-bottom:6px;
}
.menu ul li a{
	display:flex;
	flex-direction:column;
	font-size:14px;
	color:#666;
}
</style>
