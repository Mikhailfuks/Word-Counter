<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Word Counter</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 20px;
        }
        textarea {
            width: 100%;
            height: 200px;
        }
        #wordCount {
            margin-top: 20px;
            font-size: 18px;
        }
    </style>
</head>
<body>
    <h1>Word Counter</h1>
    <textarea id="textInput" placeholder="Type or paste your text here..."></textarea>
    <div id="wordCount">Word Count: 0</div>

    <script>
        // Function to count words
        function countWords(text) {
            // Use regex to match words
            const words = text.trim().split(/\s+/);
            // Check if the input is empty
            return text.trim() === '' ? 0 : words.length;
        }

        // Get the textarea and word count elements
        const textInput = document.getElementById('textInput');
        const wordCount = document.getElementById('wordCount');

        // Event listener for input change
        textInput.addEventListener('input', function() {
            const text = textInput.value;
            const count = countWords(text);
            wordCount.textContent = Word Count: ${count};
        });
    </script>
</body>
</html>
