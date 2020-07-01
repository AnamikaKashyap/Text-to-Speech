<!DOCTYPE html><html>
<head>
	<title>speak</title>
	<style>
		body{
			background-color: Black;
			text-align: center;
			margin-top: 20%;
		}
		input{
			padding: 10px;
			width: 300px;
			border-radius: 5px;
			border: solid 2px #BBB;
			background-color: white;
		}
		input:hover {
		 box-shadow: 0 0 15px 5px #ccc;
            cursor: pointer;
            transition: 0.5s;
		}
		div{
			margin: 10px 0px;
		}
		h1,h3{
			color:white;
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

<h1>Welcome to Anamika's Text-to-speech Application</h1>
<h3>This app will speak the text which you will enter below ...</h3>>
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
