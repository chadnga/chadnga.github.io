<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Two Panel Live Update Demo</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <div class="container">
    <!-- Left: Preview Area -->
    <div class="preview-panel">
      <div id="live-preview" class="live-preview">
        <span id="preview-text">Type something →</span>
      </div>
    </div>
    <!-- Right: Controls -->
    <div class="controls-panel">
      <div class="control-group">
        <label for="input-text">Type here:</label>
        <input type="text" id="input-text" placeholder="Your text goes here">
      </div>
    </div>
  </div>
  <script>
    // Simple live update logic
    const input = document.getElementById('input-text');
    const preview = document.getElementById('preview-text');
    input.addEventListener('input', function() {
      preview.textContent = input.value || "Type something →";
    });
  </script>
</body>
</html>
