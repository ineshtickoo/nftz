<template>
	<div id="app">
		<div class="container">
			<div id="nav">
				<div class="logo">
					<router-link to="/">
						<img src="@/assets/logo.svg" alt="Cura" class="cura" />
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
		<!-- <df-messenger
			chat-icon="f8dd78d6-1704-4697-a88d-e1f04ce67a54_x.png"
			intent="WELCOME"
			chat-title="Cura"
			agent-id="df5e4bfc-1fb5-45eb-aebd-5c0148aa95e1"
			language-code="en"
		></df-messenger> -->
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
