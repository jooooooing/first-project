<template lang="html5">
<div>
	<div id="title">
		<h1>후보별 득표 결과</h1>
	</div>
	<div id ="tableDiv">
		<table class="table">
			<tr>
				<td class="tableHeader">이름</td>
				<td class="tableHeader">득표</td>
			</tr>
				<tr v-for = "item in items" :key="item.name">
					<td class ="firstColumn">
						<div>{{item.name}}</div>
					</td>
					<td class = "secondColumn"> 
						<img :style = "{ width: `${item.rate*10}px`}" src="../assets/bar.png" alt="bar">
						<div id="contents">{{item.vote}} ({{item.rate}}%)</div>
					</td>
				</tr>				
		</table>	
	</div>
</div>

</template>
<script>
export default {
	data: function () {
		return {
			items: [
				{ name: "1번나연", vote: 31, rate: "15" },
				{ name: "2번정연", vote: 12, rate: "6" },
				{ name: "3번모모", vote: 25, rate: "12" },
				{ name: "4번사나", vote: 40, rate: "19" },
				{ name: "5번지효", vote: 21, rate: "10" },
				{ name: "6번미나", vote: 25, rate: "12" },
				{ name: "7번다현", vote: 15, rate: "7" },
				{ name: "8번채영", vote: 12, rate: "6" },
				{ name: "9번쯔위", vote: 32, rate: "15" },
			]
		}
	}
}
</script>
<style lang="scss" scoped>
#title {
	display: inline;
}

#tableDiv {
	display: flex;
	align-items: center;
	justify-content: center;
}

.table {
	width: 600px;
	border: 1px;
	border-color: black;
	border-style: solid;
	border-spacing: 0px;
}

.firstColumn {
	width: 75px;
	height: 40px;
	border: 1px;
	border-color: black;
	border-style: solid;
}

.secondColumn {
	width: 525px;
	height: 40px;
	border: 1px;
	border-color: black;
	border-style: solid;
	text-align: left;
}

.tableHeader {
	background-color: teal;
	height: 40px;
	border: 1px;
	border-color: black;
	border-style: solid;
	text-align: center;
	font-size: large;
	font-weight: bold;
}

img {
	width: 100px;
	height: 30px;
	display: inline-block;

}
#contents {
	display: inline-block;
}
</style>