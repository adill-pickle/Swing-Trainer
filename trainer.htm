<!DOCTYPE html>
<html>
<head>
  <title>Baseball Reaction Trainer – Mobile</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <style>
    body {
      font-family: Arial, sans-serif;
      background: #eef5ff;
      text-align: center;
      padding: 20px;
      margin: 0;
    }
    h1 {
      font-size: 1.8em;
      margin-bottom: 0.2em;
    }
    #pitchInfo, #message, #result, #stats {
      font-size: 1.2em;
      margin: 15px;
    }
    button, select {
      font-size: 1.1em;
      padding: 12px 24px;
      margin: 10px;
      border-radius: 8px;
      border: none;
      cursor: pointer;
    }
    #startBtn {
      background-color: #007bff;
      color: white;
    }
    #difficulty {
      background-color: #d1eaff;
    }
    #tapHint {
      font-size: 0.9em;
      color: #666;
    }
  </style>
</head>
<body ontouchstart="">
  <h1>⚾ Swing Trainer PRO – Mobile</h1>

  <div>
    <label for="difficulty">Difficulty:</label>
    <select id="difficulty">
      <option value="beginner">Beginner</option>
      <option value="intermediate" selected>Intermediate</option>
      <option value="pro">MLB Mode</option>
    </select>
  </div>

  <div id="pitchInfo">Tap "Start" to begin</div>
  <div id="message"></div>
  <div id="result"></div>
  <div id="stats"></div>
  <button id="startBtn" onclick="startGame()">Start</button>
  <div id="tapHint">👆 Tap anywhere or press any key to swing</div>

  <script>
    let startTime, timeoutId, canSwing = false, pitchTime;
    let pitchSpeed, pitchType, difficulty = "intermediate";

    let stats = {
      totalPitches: 0,
      swings: 0,
      hits: 0,
      misses: 0,
      early: 0,
      late: 0
    };

    const pitchTypes = [
      { type: "Fastball", speedRange: [90, 95] },
      { type: "Curveball", speedRange: [75, 80] },
      { type: "Slider", speedRange: [82, 86] },
      { type: "Changeup", speedRange: [78, 83] }
    ];

    const difficultySettings = {
      beginner: { speedMin: 75, speedMax: 85, reactionBuffer: 150 },
      intermediate: { speedMin: 78, speedMax: 92, reactionBuffer: 100 },
      pro: { speedMin: 85, speedMax: 100, reactionBuffer: 60 }
    };

    document.getElementById("difficulty").addEventListener("change", function () {
      difficulty = this.value;
    });

    function getRandomFromRange(min, max) {
      return Math.floor(Math.random() * (max - min + 1)) + min;
    }

    function updateStatsDisplay() {
      const { totalPitches, swings, hits, misses, early, late } = stats;
      document.getElementById("stats").innerHTML =
        `📊 Pitches: ${totalPitches} | Swings: ${swings} | ✅ Hits: ${hits}<br>` +
        `❌ Misses: ${misses} | ⏱️ Early: ${early} | 🕒 Late: ${late}`;
    }

    function startGame() {
      document.getElementById("result").textContent = "";
      document.getElementById("message").textContent = "Get Ready...";
      canSwing = false;

      const level = difficultySettings[difficulty];
      const pitch = pitchTypes[Math.floor(Math.random() * pitchTypes.length)];
      pitchType = pitch.type;
      pitchSpeed = getRandomFromRange(level.speedMin, level.speedMax);

      const speedFtPerSec = pitchSpeed * 1.46667;
      pitchTime = (60.5 / speedFtPerSec) * 1000;

      document.getElementById("pitchInfo").textContent =
        `Pitch: ${pitchType} | ${pitchSpeed} mph (${difficulty.toUpperCase()})`;

      const delay = Math.random() * 2000 + 1000;
      stats.totalPitches++;
      updateStatsDisplay();

      timeoutId = setTimeout(() => {
        document.getElementById("message").textContent = "Pitch!";
        startTime = Date.now();
        canSwing = true;

        setTimeout(() => {
          if (canSwing) {
            document.getElementById("message").textContent = "Strike! No swing.";
            stats.misses++;
            canSwing = false;
            updateStatsDisplay();
          }
        }, pitchTime + level.reactionBuffer);
      }, delay);
    }

    function swing() {
      if (!startTime) return;
      const now = Date.now();

      if (canSwing) {
        const reaction = now - startTime;
        document.getElementById("result").textContent = `⏱️ Reaction Time: ${reaction} ms`;
        stats.swings++;

        const level = difficultySettings[difficulty];
        if (reaction <= pitchTime) {
          document.getElementById("message").textContent = "❌ Too Early!";
          stats.early++;
        } else if (reaction <= pitchTime + level.reactionBuffer) {
          document.getElementById("message").textContent = "✅ Contact!";
          stats.hits++;
        } else {
          document.getElementById("message").textContent = "❌ Too Late!";
          stats.late++;
        }

        canSwing = false;
        updateStatsDisplay();
      } else {
        clearTimeout(timeoutId);
        document.getElementById("message").textContent = "❌ Too early!";
        document.getElementById("result").textContent = "";
        stats.misses++;
        updateStatsDisplay();
      }
    }

    document.body.addEventListener("click", swing);
    document.body.addEventListener("touchstart", swing);
    document.body.addEventListener("keydown", swing);
  </script>
</body>
</html>