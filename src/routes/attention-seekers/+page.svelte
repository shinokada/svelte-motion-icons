<script lang="ts">
	import {
		AtSign,
		BadgeCheck,
		Bell,
		AcademicCap,
		Wrapper,
		ArrowDownLeft,
		Animate,
		ArrowBigUp,
		ArrowDownLeft2,
		ArrowDownOnSquare
	} from '$lib';
</script>

<div class="container">
	<h1>Svelte Animate for Svelte 5</h1>
	<h2>Click to see animation</h2>

	<AtSign size={50} color="purple" />
	<BadgeCheck size={50} color="green" />
	<Bell size={50} color="red" />
	<AcademicCap size={50} color="blue" />
	<Wrapper
		event="onclick"
		params={{
			duration: 500,
			delay: 300
		}}
	>
		<ArrowDownOnSquare size={50} color="green" />
	</Wrapper>
	<Wrapper event="onclick">
		<ArrowDownLeft2
			size={50}
			color="skyblue"
			params={{
				duration: 500,
				delay: 300
			}}
			params2={{
				duration: 500,
				delay: 800
			}}
		/>
	</Wrapper>
	<Wrapper
		event="onclick"
		params={{
			duration: 500,
			delay: 300
		}}
	>
		<ArrowDownLeft size={50} color="orange" />
	</Wrapper>
	<Animate animation="backInLeft" trigger="click" duration="0.5s">
		<ArrowBigUp size="50" color="#FF0000" ariaLabel="Upward arrow" />
	</Animate>

	<Animate animation="zoomIn" trigger="click" duration="0.5s">
		<h1>Hello World!</h1>
	</Animate>

	<Animate animation="zoomOutRight" trigger="click" duration="0.5s" hideAfter={true}>
		<div style="height: 200px; width: 200px; background: #0055f0"></div>
	</Animate>

	<div class="animation-container">
		<Animate animation="backInUp" trigger="click" duration="0.5s">
			<ArrowBigUp size="50" color="#FF0000" ariaLabel="Upward arrow" />
		</Animate>
	</div>
</div>

<style>
	.container {
		margin: 40px;
		display: flex;
		flex-direction: column;
		align-items: center;
		/* justify-content: center; */
		min-height: 100vh;
	}
	.animation-container {
		position: relative;
		width: 300px;
		height: 200px;
		overflow: hidden;
		background: #f0f0f0;
	}
</style>
