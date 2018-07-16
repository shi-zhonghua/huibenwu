<template>
	<div class="logo-main" >
		<div class="logo-opacity" @click="handleZhuceClick"></div>
		<div class="logo-form">
			<div class="logo-colse" @click="handleZhuceClick">X</div>
			<div>
				<table>
					<tr>
						<td>用户名：</td>
						<td><input type="text" class="text"></td>
					</tr>
					<tr>
						<td>密  码：</td>
						<td><input type="text" class="text"></td>
					</tr>
					<tr>
						<td colspan="2">
							<button class="submit">注册</button>
							<button class="submit">重置</button>
						</td>
					</tr>
				</table>
				
			</div>
		</div>

	</div>
</template>

<script >
export default {
	name: 'PublicDenglu',
	methods: {
		handleZhuceClick () {
			this.$emit('close')
		}
	}

}
</script>

<style lang="less" scoped>
.logo-opacity{
	position:fixed;
	top:0;
	left:0;
	bottom:0;
	background:#ccc;
	width:100%;
	z-index:100;
	opacity:.3;

}
.logo-form{
	width: 50%;
    position: fixed;
    max-height: 50%;
    overflow: auto;
    background: #fff;
    top: 20%;
    left: 50%;
    margin-left: -25%;
    z-index: 10;
    border: 2px solid #464068;
    padding: 2%;
    line-height: 1.6;
	z-index:103;
	
}
.logo-colse {
	position:absolute;
	right:10px;
	top:10px;
	color:#000;
	font-size:12px;
	cursor: pointer;
}
.text{
	 border:solid 1px #ccc;
	 padding-left:2px;
}
tr{
	line-height:30px;
}
.submit{
	padding:4px;
	background:#ff9228;
	border-radius: 3px;
	margin-left:60px;
	margin-top:20px;
	color:#fff;

}
</style>