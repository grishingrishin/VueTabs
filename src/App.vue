<template>
	<div id="app">
		<AppTabs v-model="activeTab">
			<AppTabNav>
				<AppTab tabId="tab-1">
					Tab-1
				</AppTab>
				<AppTab tabId="tab-2">
					Tab-2
				</AppTab>
			</AppTabNav>
			<AppTabItems>
				<AppTabItem tabId="tab-1">
					<p>
						Donec rutrum congue leo eget malesuada. Mauris blandit aliquet elit, eget tincidunt nibh pulvinar a. Mauris blandit aliquet elit,
						eget tincidunt nibh pulvinar a. Praesent sapien massa, convallis a pellentesque nec,
						egestas non nisi. Donec sollicitudin molestie malesuada.
					</p>
					<p>
						Lorem ipsum dolor sit amet consectetur adipisicing elit. Ipsum ea, labore non laudantium quibusdam dolor animi
						accusantium numquam fugit odit enim dolorem corrupti. Temporibus adipisci,
						sunt repellat voluptates velit fuga!
					</p>
					<p>
						Lorem ipsum dolor sit amet consectetur adipisicing elit. Ipsum ea, labore non laudantium quibusdam dolor animi
						accusantium numquam fugit odit enim dolorem corrupti. Temporibus adipisci,
						sunt repellat voluptates velit fuga!
					</p>
				</AppTabItem>
				<AppTabItem tabId="tab-2">
					<p>
						Lorem ipsum dolor sit amet consectetur adipisicing elit. Ipsum ea, labore non laudantium quibusdam dolor animi
						accusantium numquam fugit odit enim dolorem corrupti. Temporibus adipisci,
						sunt repellat voluptates velit fuga!
					</p>
					<p>
						Lorem ipsum dolor sit amet consectetur adipisicing elit. Ipsum ea, labore non laudantium quibusdam dolor animi
						accusantium numquam fugit odit enim dolorem corrupti. Temporibus adipisci,
						sunt repellat voluptates velit fuga!
					</p>
					<p>
						Donec rutrum congue leo eget malesuada. Mauris blandit aliquet elit, eget tincidunt nibh pulvinar a. Mauris blandit aliquet elit,
						eget tincidunt nibh pulvinar a. Praesent sapien massa, convallis a pellentesque nec,
						egestas non nisi. Donec sollicitudin molestie malesuada.
					</p>
				</AppTabItem>
			</AppTabItems>
		</AppTabs>
	</div>
</template>

<script>
import AppTabs from './components/AppTabs.vue';
import AppTabNav from './components/AppTabNav.vue';
import AppTab from './components/AppTab.vue';
import AppTabItems from './components/AppTabItems.vue';
import AppTabItem from './components/AppTabItem.vue';

export default {
	name: 'App',
	components: {
		AppTabs,
		AppTab,
		AppTabNav,
		AppTabItems,
		AppTabItem,
	},
	data() {
		return {
			activeTab: 'tab-1',
		};
	},
};
</script>

<style>
#app {
	max-width: 480px;
	margin: 0 auto;
	font-family: Avenir, Helvetica, Arial, sans-serif;
	-webkit-font-smoothing: antialiased;
	-moz-osx-font-smoothing: grayscale;
	color: #2c3e50;
	margin-top: 60px;
}
</style>
