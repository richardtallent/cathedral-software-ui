<template>
	<div class="all cathedral-page">
		<div class="cathedral-side">
			<button>
				<span>Programs</span>
			</button>
			<button>
				<span>Systems</span>
			</button>
			<button>
				<span>Applications</span>
			</button>
			<button style="margin-top:0.4em;">
				<span>Command:</span>
				<input type="text">
			</button>
		</div>
		<div class="cathedral-center">
			<div class="cathedral-center-top">
				<div class="cathedral-center-top-square"/>
			</div>
			<div class="cathedral-header">
				<img src="../assets/cathedral-header.svg">
			</div>
			<h2>Programs Under
				<br>Development
			</h2>
			<ul>
				<li>Conference Moderator</li>
				<li>Internet Services</li>
				<li>Musical Notes</li>
				<li>TextEdit/Beta</li>
				<li>Mozart's Ghost.Net</li>
				<li>Run Like Hell!</li>
				<li>Internet Directory Services</li>
				<li>Language Translation</li>
				<li>Educational Packages</li>
				<li>Personal Banker</li>
				<li>InterNotes</li>
				<li>Bridge Challenge</li>
				<li>C++ Library Manager</li>
			</ul>
		</div>
		<div class="cathedral-side">&nbsp;</div>
		<div class="pi" @click="toggleOriginal">&pi;</div>
		<img class="original" v-show="showOriginal" src="../assets/original.jpg">
	</div>
</template>

<script>
export default {
	name: "CathedralMenuPage",
	data: () => ({ showOriginal: false }),
	methods: {
		toggleOriginal() {
			this.showOriginal = !this.showOriginal
		},
	},
}
</script>

<style scoped>
.cathedral-page {
	background-color: #a0aeeb;
	position: absolute;
	left: 0;
	top: 0;
	bottom: 0;
	right: 0;
	padding: 1em;
	overflow: scroll;
	display: flex;
	flex-direction: row;
	align-items: flex-start;
	font-size: 125%;
}
.cathedral-side {
	display: flex;
	flex: 1;
	flex-direction: column;
	margin-left: 0.5rem;
	width: 20rem;
}
.cathedral-center {
	flex: 1;
	flex-direction: column;
	background-color: #99ffff;
	border: 2px solid black;
	padding: 0;
	min-width: 24rem;
	max-width: 24rem;
}
.cathedral-center-top {
	background-color: #f7f7f7;
	border-bottom: 2px solid #000;
	padding: 0.1em 0.6em;
}
.cathedral-center-top-square {
	background-color: white;
	border: 1px solid black;
	height: 0.8em;
	width: 0.8em;
}
.cathedral-header,
h2 {
	background-color: #0000cc;
	text-align: center;
}
.cathedral-header {
	padding: 0.5rem 3.5rem 0 3.5rem;
}
h2 {
	padding-bottom: 0.2em;
	font-family: "Eurostile";
	font-weight: bold;
	font-size: 160%;
	line-height: 1.1;
	color: white;
}
button {
	width: 12rem;
	margin: 0.1em;
	padding: 0.3em 0.5em 0.2em 0.5em;
	border: 2px solid #000;
	border-radius: 0.4em;
	background-image: linear-gradient(#fff, #999);
	color: #00c;
	text-align: left;
	vertical-align: middle;
}
button span {
	display: block;
	margin-left: 0.2em;
	font-weight: bold;
	font-family: "Heiti SC";
	line-height: 1;
	transform: scale(1.1, 1);
	transform-origin: left center;
	text-transform: uppercase;
}
input {
	width: 100%;
	margin-top: 0.3em;
	padding: 0.2em 0.3em;
	border: 1px outset #fff;
	background-color: #000;
	color: white;
	font-family: "Courier New", Courier, monospace;
	font-size: 80%;
}
ul {
	margin: 0;
	padding: 0.3em 0;
	border-top: 2px solid #000;
	list-style: none;
	font-family: "Eurostile";
	font-size: 150%;
	font-style: italic;
	/* Faux bold */
	text-shadow: 1px 0 0 currentColor;
}
li {
	margin: 0;
	padding: 0 0.5em;
	line-height: 1.2;
	user-select: none;
}
li:hover {
	background-color: white;
	color: red;
}
.pi {
	position: absolute;
	right: 0.5em;
	bottom: 0.5em;
	font-family: "Eurostile";
	color: white;
}
.original {
	position: absolute;
	z-index: 1;
	right: 0;
	bottom: 0;
	top: 0;
	left: 0;
	margin: auto;
	height: 90%;
}
</style>
