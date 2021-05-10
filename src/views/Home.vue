<template>
	<div class="container">
		<div class="flexbabe">
			<div class="row section1">
				<div class="moreresp five columns text">
					<h1>NFTZ</h1>
					<p>
						NFTs made easy. A multi currency multi model wallet with abilities
						to create NFTs on demand using images as well as other media.
					</p>
					<div class="block noselect">
						<!-- <a href="/Cura.apk" download="Cura"> -->
						<button disabled>Download</button>
						<!-- </a> -->
						<router-link to="/about" class="more">
							Learn more &rarr;
						</router-link>
					</div>
				</div>
				<div class="one columns nvm">
					<br />
				</div>
				<div class="moreresp six columns">
					<div class="nvm">
						<br />
						<br />
					</div>
					<img
						src="@/assets/minmock-min.png"
						alt
						class="floating mockup"
						draggable="false"
					/>
				</div>
			</div>
		</div>
	</div>
</template>

<script>
export default {
	name: 'Home',
}
</script>

<style scoped>
.mockup {
	float: right;
	padding-right: 10%;
	width: 60%;
}

/* Animation */
.floating {
	animation-name: floating;
	animation-duration: 3s;
	animation-iteration-count: infinite;
	animation-timing-function: ease-in-out;
}

@keyframes floating {
	from {
		transform: translate(0, 0px);
	}
	50% {
		transform: translate(0, 10px);
	}
	to {
		transform: translate(0, -0px);
	}
}

.mock {
	width: 45%;
}
.flexbabe {
	height: 70vh;
	display: flex;
	flex-direction: column;
	justify-content: center;
	align-items: center;
}
.row {
	display: flex;
	align-items: center;
}
button {
	background: #0d6be7;
	color: #fff;
	border: none;
}
button:hover {
	background: #0553b9;
	color: #fff;
}
button:active {
	color: #fff;
}
a {
	color: #0d6be7;
	text-decoration: none;
}
a:hover {
	color: #0553b9;
}
.more {
	margin-left: 1.5em;
}
@media (max-width: 750px) {
	.moreresp.five.columns,
	.moreresp.six.columns {
		width: 100% !important;
	}
	.nvm {
		display: none;
	}
}
@media (max-width: 550px) {
	.row {
		flex-direction: column;
	}
	.text {
		margin-bottom: 2em;
	}
	.mockup {
		margin-left: 1em;
		overflow-x: hidden;
	}
	.flexbabe {
		height: auto;
		margin-top: 2em;
	}
}
</style>
