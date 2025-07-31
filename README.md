<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Simple AI Generator Demo</title>
  <style>
    body { font-family: Arial, sans-serif; max-width: 600px; margin: 2em auto; padding: 1em; }
    textarea { width: 100%; height: 100px; }
    button { padding: 10px 20px; margin-top: 10px; }
    .output { margin-top: 20px; padding: 10px; border: 1px solid #ccc; background: #f9f9f9; min-height: 50px; }
  </style>
</head>
<body>
  <h1>Simple AI Generator</h1>
  <textarea id="prompt" placeholder="Enter your prompt here..."></textarea>
  <br />
  <button onclick="generateResponse()">Generate</button>
  <div class="output" id="response"></div>

  <script>
    const fakeResponses = [
      "That's an interesting idea!",
      "Let me think about that...",
      "Here's something you might like.",
      "I can help with that!",
      "What about this approach?",
      "Sounds good to me.",
      "Let's explore this further.",
      "Here's a creative twist.",
      "Try this out!",
      "Hope this helps!"
    ];

    function generateResponse() {
      const prompt = document.getElementById('prompt').value.trim();
      const responseDiv = document.getElementById('response');

      if (!prompt) {
        responseDiv.textContent = "Please enter a prompt to generate a response.";
        return;
      }

      // Pick a random fake response
      const randomIndex = Math.floor(Math.random() * fakeResponses.length);
      const aiResponse = fakeResponses[randomIndex];

      responseDiv.textContent = aiResponse;
    }
  </script>
</body>
</html>
