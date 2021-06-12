<script>
	import Timer from './Timer.svelte'
	import HowTo from './HowTo.svelte'

	let audio; 

	function timerEnds(e){
		console.log(e)
		console.log(e.detail) //e.detail is the data we pass from timer when timer is
		audio.play()
	}
</script>


<h1>Handwashing App</h1>
<Timer  on:end={timerEnds}/>
<HowTo />

<h3>
	<a href="https://www.google.com/imgres?imgurl=https%3A%2F%2Freader012.docslide.net%2Freader012%2Fhtml5%2F20180107%2F55cf92bc550346f57b99288e%2Fbg1.png&imgrefurl=https%3A%2F%2Fvdocuments.mx%2Fhow-do-i-wash-my-hands-properly.html&tbnid=HdUgNVZQ6KuCGM&vet=12ahUKEwj53OH6wo3xAhXYA6YKHTTwBRkQMygBegUIARCvAQ..i&docid=txhbVjCvYI29bM&w=906&h=1291&q=how%20do%20i%20wash%20my%20hands%20properly&ved=2ahUKEwj53OH6wo3xAhXYA6YKHTTwBRkQMygBegUIARCvAQ">Picture Source</a>
	<a href="https://www.google.com/imgres?imgurl=https%3A%2F%2Freader012.docslide.net%2Freader012%2Fhtml5%2F20180107%2F55cf92bc550346f57b99288e%2Fbg1.png&imgrefurl=https%3A%2F%2Fvdocuments.mx%2Fhow-do-i-wash-my-hands-properly.html&tbnid=HdUgNVZQ6KuCGM&vet=12ahUKEwj53OH6wo3xAhXYA6YKHTTwBRkQMygBegUIARCvAQ..i&docid=txhbVjCvYI29bM&w=906&h=1291&q=how%20do%20i%20wash%20my%20hands%20properly&ved=2ahUKEwj53OH6wo3xAhXYA6YKHTTwBRkQMygBegUIARCvAQ">Sound Source</a>
</h3>
<audio bind:this={audio} >
	<source  src="'https://interactive-examples.mdn.mozilla.net/media/cc0-audio/t-rex-roar.mp3'" />
</audio>
<style>
	h1, h3{
		text-align: center;
	}
</style>