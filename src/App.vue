<template>
	<div id="app">
		<div class="container">
			<div id="nav">
				<div class="logo">
					<router-link to="/">
						<img src="@/assets/logo.svg" class="cura" />
					</router-link>
				</div>
				<div class="right">
					<router-link to="/about">About</router-link>
					<router-link to="/register">Register</router-link>
				</div>
			</div>
		</div>
		<main>
			<router-view v-slot="{ Component }">
				<transition name="fade" mode="out-in">
					<component :is="Component" />
				</transition>
			</router-view>
		</main>
		<footer class="footer noselect">
			<div class="container">
				<div class="flex">
					<div class="socialsy">
						<a href="" class="link" target="_blank">
							<span>Source</span>
						</a>
						<a
							href="https://github.com/ebtesam25/blockhacks2021"
							class="link"
							target="_blank"
						>
							<span>App Source</span>
						</a>
					</div>
				</div>
			</div>
		</footer>
	</div>
</template>

<style scoped>
.right a {
	padding: 1em;
}
</style>
