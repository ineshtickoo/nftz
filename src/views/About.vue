<template>
	<div class="container">
		<br class="nvm" />
		<br />
		<h2 class="center zero">NFTZ</h2>
		<h5 class="center">NFTs Made Easy.</h5>
		<br />
		<!-- <div class="flex-center">
			<div class="flexbruhh center">
				<div class="boxcard">
					<h4 class="zero" style="margin-top: 0.6em">Vaccines</h4>
					<p>
						Helping you manage the distribution of vaccines throughout the
						country, so that you stay safe.
					</p>
				</div>
				<div class="boxcard">
					<h4>
						<img src="@/assets/curapass.png" alt draggable="false" />
					</h4>
					<p>
						A new way to
						<b>explore</b>
						during these difficult times.
					</p>
				</div>
			</div>
		</div> -->
		<br />
		<br />
		<br />
		<br />
		<h2>What is NFTZ?</h2>
		<div class="row" id="whatisnft">
			<div class="seven columns text">
				<p>
					NFTs are all the rage now, Everyone has heard of NFTs and wants in on
					the action. However the process of creating and deploying an NFT can
					be still a daunting and technically challenging task.
				</p>
				<p>
					To tackle both these problems, we present
					<span><b>NFTZ</b></span>
					<span>.</span>
					NFTZ is a multi-currency multi-model wallet with abilities to create
					NFTs on demand using images or other media.
					<span>
						<a href="https://cura.arhaanb.co/present" target="_blank">
							<span>this page</span>
						</a>
					</span>
					<span>.</span>
				</p>
			</div>
			<div class="five columns">
				<img
					src="@/assets/appui-learnmore-1.png"
					alt="MOCKUP"
					class="mock"
					id="firstmock"
				/>
			</div>
		</div>
		<div class="u-cf"></div>

		<div class="row" id="mobile-app">
			<div class="five columns pages">
				<p class="center">
					<img
						src="@/assets/appui-learnmore-2.png"
						alt="MOCKUP"
						id="secondmock"
					/>
				</p>
			</div>
			<div class="seven columns">
				<h3>Mobile app</h3>
				<p>
					We have a mobile app interface which allows a user to generate an NFT
					or sell an existing one. This is then uploaded to our backend which
					generates an NFT on the openSea marketplace using Chainlink.
				</p>
				<p>
					We currently use LINK on the rinkeby Testnet for deploying our NFTs.
				</p>
			</div>
		</div>

		<div class="row" id="mobile-app">
			<div class="seven columns">
				<h3>Physical Hardware</h3>

				<p>
					We have used an RFID reader to implement a multi currency wallet,
					which can be used to access the cryptocurrencies linked to the NFTs.
					We can also approve pending NFT deployments using wearable NFT
					devices. All this will be happening while the cards are integrated
					with our app NFTZ.
				</p>
				<p>
					A multi currency wallet has been put in place which uses RFID
					technology for accessing your cryptocurrencies linked to your account.
					This is also applicable for wearable devices using which we can
					approve pending deployments.
				</p>
			</div>
			<div class="five columns pages">
				<p class="center">
					<img id="hardimg" src="@/assets/hardwaer.png" alt="MOCKUP" />
				</p>
			</div>
		</div>

		<br />
		<br class="nvm" />
		<br />

		<div class="vidpen">
			<div>
				<iframe
					width="100%"
					src="https://www.youtube.com/embed/mf5JssMr3Mw"
					frameborder="0"
					allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture"
					allowfullscreen
					class="video"
				></iframe>
			</div>
		</div>
		<br />
		<br />
		<br />
		<h2>The team</h2>
		<div class="team">
			<div class="box six columns">
				<img
					src="@/assets/muntaser.png"
					alt="Arhaan Bahadur"
					draggable="false"
				/>
				<div class="info">
					<h4>Muntaser Syed</h4>
					<p>Co-founder</p>
				</div>
			</div>

			<div class="box six columns">
				<img src="@/assets/ebtesam.png" alt="Aditya Pramar" draggable="false" />
				<div class="info">
					<h4>Ebtesam Haque</h4>
					<p>Co-founder</p>
				</div>
			</div>

			<div class="u-cf"></div>
		</div>
		<div class="team">
			<div class="box six columns">
				<img src="@/assets/kk.png" alt="Aditya Pramar" draggable="false" />
				<div class="info">
					<h4>Kartikay Sharma</h4>
					<p>Co-Founder</p>
				</div>
			</div>
			<div class="box six columns">
				<img src="@/assets/inesh.png" alt="Aditya Pramar" draggable="false" />
				<div class="info">
					<h4>Inesh Tickoo</h4>
					<p>Co-Founder</p>
				</div>
			</div>
		</div>
	</div>
</template>

<script>
import axios from 'axios'
export default {
	data() {
		return {
			info: null,
			loading: true,
			date: false,
			months: [
				'january',
				'february',
				'march',
				'april',
				'may',
				'june',
				'july',
				'august',
				'september',
				'october',
				'november',
				'december',
			],
		}
	},
	methods: {
		cap(string) {
			return string.charAt(0).toUpperCase() + string.slice(1)
		},
		commas(x) {
			return x.toString().replace(/\B(?=(\d{3})+(?!\d))/g, ',')
		},
		superscr(x) {
			const num = x.slice(-1)
			var scr = ''
			if (num == 1) {
				scr = 'st'
			} else if (num == 2) {
				scr = 'nd'
			} else if (num == 3) {
				scr = 'rd'
			} else {
				scr = 'th'
			}
			return scr
		},
	},
	async mounted() {
		await axios.get('https://covid19.mathdro.id/api/').then((response) => {
			this.info = response.data
			console.log(response)
		})
		this.date = new Date(this.info.lastUpdate)
		this.loading = false
	},
}
</script>

<style scoped>
.pages img {
	width: 50%;
	margin-top: 2em;
}
.mock {
	width: 100%;
	margin-top: -3em;
}
#firstmock {
	transform: translateY(-30%);
}
#secondmock {
	width: 100%;
	transform: translateY(-30%);
}
#hardimg {
	border-radius: 25px;
	transform: translateY(-20%);
}
.flexbruhh {
	display: flex;
	justify-content: center;
}
.boxcard {
	width: 40%;
	border-style: solid;
	border-color: #7599e6;
	border-radius: 1em;
	margin: 1em;
	padding: 1em;
}
.boxcard img {
	width: 60%;
	margin-bottom: -1em;
}
.flex-center {
	display: flex;
	justify-content: center;
}

.vidpen {
	position: relative;
	width: 100%;
	height: 0;
	padding-bottom: 56.25%;
}

.video {
	position: absolute;
	top: 0;
	left: 0;
	width: 100%;
	height: 100%;
}
#whatisnft {
	padding-bottom: 0;
	margin-bottom: 0;
}
#mobile-app {
	transform: translateY(-10%);
}
div.row {
	padding-bottom: 0;
}
.box {
	display: flex;
	align-items: center;
	margin-bottom: 2em;
}

.box img {
	width: 10em;
	/* border-radius: 100%; */
	margin-right: 2em;
}

.box .info {
	margin-bottom: 1em;
}
.box .info .p {
	color: #6494d2;
}

.box h4,
.box p {
	margin: 0;
}

.zero {
	margin: 0;
}
.top {
	margin-top: 1.5em;
}
.data {
	display: flex;
	justify-content: center;
}
.card {
	text-align: center;
	padding: 2em;
	background: rgba(255, 255, 255, 0.3);
	border-radius: 1em;
	border-style: solid;
	border-width: 0.1em;
}

.confirmed {
	border-color: #7599e6;
}

a {
	color: #7599e6;
}

.deaths {
	border-color: red;
}

.recovered {
	border-color: rgb(79, 161, 110);
}

.minte {
	width: 10em;
}

@media (max-width: 550px) {
	.data,
	.flexbruhh {
		flex-direction: column;
	}
	.boxcard {
		width: 90%;
		margin: 0;
		margin-bottom: 1em;
	}
	.card {
		width: 100%;
		margin: 0.5em 0;
	}
	.nvm {
		display: none;
	}
	.mock {
		margin: 0;
		margin-top: 2em;
	}
	.pages img {
		display: none;
	}
}

@media (max-width: 750px) {
	#firstmock {
		transform: translateY(0);
		margin-top: -2em;
	}
	#mobile-app {
		transform: translateY(0);
		margin-bottom: 2em;
	}
}
</style>
