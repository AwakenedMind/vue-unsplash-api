<template>
	<div id="app">
		<div class="navbar">
			<span class="material-icons logo">
				party_mode
			</span>
			<form class="search-field" v-on:submit.prevent="onSubmit">
				<input type="text" placeholder="Search for an Image" v-model="text" />
				<button>
					<span>
						Search
					</span>
					<span class="material-icons">
						search
					</span>
				</button>
			</form>
			<nav>
				<span>Home</span>
				<span>Trending</span>
			</nav>
		</div>
	</div>
</template>

<script>
const accessToken = process.env.VUE_APP_ACCESS_KEY;

console.log(accessToken);

export default {
	name: 'App',
	components: {},
	data: () => {
		return {
			text: '',
		};
	},
	methods: {
		onSubmit: function() {},
	},
};
</script>

<style lang="scss">
* {
	box-sizing: border-box;
}

body {
	margin: 0;
	padding: 0;
	font-family: Lato;
}

.navbar {
	background: #262626;
	color: white;
	display: flex;
	align-items: center;
	padding-left: 2rem;
	padding-right: 2rem;
	height: 4rem;

	.logo {
		margin-right: 2rem;
		transform: scale(1.4);
	}

	.search-field {
		position: relative;
		margin: 0 auto;
		width: 70%;
		max-width: 40rem;
		height: 2rem;
		background: white;
		border-radius: 20px;
		overflow: hidden;

		button {
			font-size: 0.9em;
			position: absolute;
			right: 0;
			height: 100%;
			border: none;
			width: 6rem;
			color: white;
			background: #cc2b5e;
			background: -webkit-linear-gradient(to right, #753a88, #cc2b5e);
			background: linear-gradient(to right, #753a88, #cc2b5e);
			display: inline-flex;
			justify-content: center;
			align-items: center;
		}

		input {
			border: none;
			padding-left: 2rem;
			height: 100%;
			width: 100%;
			background: none;
		}

		.material-icons {
			height: 100%;
			color: white;
			transform: scale(0.8);
			line-height: 1.4;
			margin-left: 0.2rem;
		}
	}
	nav {
		span {
			margin-right: 1rem;
		}
	}
}
</style>
