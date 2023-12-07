<script>
	import { themes } from "./config.js";
	import { getContext } from "svelte";

	export let theme = getContext("theme");
</script>

<footer
	style="--text: {themes[theme]['text']}; --muted: {themes[theme][
		'muted'
	]}; --pale: {themes[theme]['pale']};"
>
	<div class="col-wide" data-analytics="footer">
		{#if theme == "dark"}
			<img
				class="logo-img"
				src="https://github.com/erickoepcke/payEquity_scrollyPage/blob/master/public/img/DataTeamLogo.png?raw=true"
				alt="New York City Council Data Team"
			/>
		{:else}
			<img
				class="logo-img"
				src="https://github.com/erickoepcke/payEquity_scrollyPage/blob/master/public/img/DataTeamLogo.png?raw=true"
				alt="New York City Council Data Team"
			/>
		{/if}
		<ul>
			<li>
				<a href="mailto:datainfo@council.nyc.gov" class="list__link"
					>Contact us</a
				>
			</li>
		</ul>
		<hr />
		<div class="license">
			<p>
				Any opinion, findings, and conclusions or recommendations
				expressed in this material are those of the authors and do not
				necessarily reflect the views of the NYC Council. All errors are
				our own.
			</p>

			<p>
				Webpage adapted from the template available <a
					href="https://github.com/onsvisual/svelte-scrolly"
					target="_blank">here</a
				>. Title image borrowed from
				<a
					href="https://iwpr.org/quick-figure-pay-equity-still-decades-away/"
					target="_blank">here</a
				>.
			</p>
		</div>
	</div>
</footer>

<style>
	footer {
		color: var(--text);
		background-color: var(--pale);
		padding-bottom: 20px;
		padding-top: 20px;
		font-size: 18px;
	}
	footer a {
		-webkit-box-sizing: border-box;
		box-sizing: border-box;
		color: var(--muted);
		text-decoration: underline;
		display: inline-block;
	}
	footer a:hover {
		color: var(--text);
		text-decoration: none;
	}
	footer a:active {
		outline: 3px solid transparent;
		background-color: #fd0;
		-webkit-box-shadow:
			0 -2px #fd0,
			0 4px #222;
		box-shadow:
			0 -2px #fd0,
			0 4px #222;
		color: #222;
		text-decoration: none;
	}
	footer hr {
		margin-bottom: 27px;
		margin-top: 36px;
		border: 0;
		border-top: 1px solid var(--muted);
	}
	/*footer svg > path {
		fill: var(--muted);
	}*/
	ul {
		padding: 0;
		margin: 0;
	}
	li {
		margin-right: 18px;
		display: inline-block;
	}
	.logo-img {
		margin-bottom: 5px;
		width: 350px;
	}
	/*.ogl-img {
		margin: 0 0.5rem 0.2rem 0;
		width: 59px;
		vertical-align: middle;
	}*/
	.license {
		vertical-align: top;
		font-size: 0.8em;
	}
</style>
