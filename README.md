# Text-to-Speech
Created by Anamika Kashyap
<html>
<head>
	<title>speak</title>
	<style>
		input{
			padding: 10px;
			width: 300px;
			border-radius: 5px;
			border: solid 2px #BBB;
		}
		div{
			margin: 10px 0px;
		}
		button{
			padding: 10px;
			background-color: #6a67ce;
			color: #FFFFFF;
			border: 0px;
			cursor: pointer;
			border-radius: 5px;
		}
	</style>
	
</head>
<body>

<div>
	<input type="text" id="text-to-speech" placeholder = "Enter text to speech..."/>
</div>
<div>
	<button type="button" onclick="textToAudio()">Speak</button>
</div>

<script>
	function textToAudio() {
		let msg = document.getElementById("text-to-speech").value;

		let speech = new SpeechSynthesisUtterance();
		speech.lang = "en-US";

		speech.text = msg;
		speech.volume = 1;
		speech.rate = 1;
		speech.pitch = 1;

		window.speechSynthesis.speak(speech);
	}
</script>
</body>
</html>
