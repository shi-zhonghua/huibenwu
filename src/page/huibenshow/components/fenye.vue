<template>
	<div class="pagev">
		<a href="">首页</a>
		<a href="">上一页</a>
		<a href="">下一页</a>
		<a href="">末页</a>
		<a href="" style="color: #df3033;font-weight: bold;">当前页</a>
		<a href="">共有页</a>
		<a href="">末页</a>
		<form  style="display: inline">
            跳转到：<input class="fy-input" name="pageNow" onkeyup="this.value=this.value.replace(/[^0-9]/g,'');" type="text">
            <input class="but_tiaozhuan" value="Go" type="submit">
        </form>
		

	</div>
</template>

<script>
export default {
	name:'PublicFenye'
}
</script>

<style lang="less" scoped>
.pagev {
    width: 100%;
    clear: both;
    color: #313131;
    font-weight: bold;
    margin-right: auto;
    margin-left: auto;
    text-align: center;
    margin-top: 20px;
    margin-bottom: 10px;
}
.pagev a {
    color: #333;
    font-size: 12px;
    font-weight: normal;
    background: #f7f7f7;
    border: solid 1px #ddd;
    padding: 8px;
}
.fy-input {
    width: 40px;
    height: 30px;
    border: solid 1px #ddd;
    padding-left: 2px;
}
.but_tiaozhuan {
    padding:4px 6px;
    color: #333;
    background: #f7f7f7;
    border: solid 1px #ddd;
}
</style>