<svelte:options tag="tag-hurb" />

<script>
	/**
	 * Title of the Tag component
	 */
	export let title = 'Tag Title';
	/**
	 * Whats the color you want?
	 */
	export let color = 'purple';

	export let align = 'start';

	export let icon = 'shield';
</script>

<div class="{color} {align} tag-hurb">
	<span class="title">
		{title}
	</span>
</div>

<style>
	.tag-hurb {
		color: #fff;
		display: flex;
		align-items: center;
		border-radius: 4px;
		padding: 6px 8px;
	}

	.title {
		margin-left: 8px;
		font-weight: 500;
	}

	.start {
		justify-content: start;
	}
	.center {
		justify-content: center;
	}
	.end {
		justify-content: end;
	}
	.primary {
		background-color: #3468fc;
	}

	.freeze {
		background: #8caafd;
	}
	.purple {
		background-color: #9747ff;
	}

	.orange {
		background-color: #fc7821;
	}
</style>
