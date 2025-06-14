<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>S3 Average Calculator</title>
  <style>
    body { font-family: Arial; max-width: 600px; margin: auto; padding: 20px; }
    input { margin: 5px 0; padding: 5px; width: 100%; }
    button { padding: 10px 15px; margin-top: 10px; }
    .result { margin-top: 20px; font-size: 1.2em; font-weight: bold; }
  </style>
</head>
<body>
  <h2>S3 Average Calculator</h2>
  <form id="notesForm">
    <label>Math appliquées exam:</label><input type="number" step="0.01" id="a" required />
    <label>Math appliquées TD:</label><input type="number" step="0.01" id="b" required />
    <label>Ondes et vibrations  exam:</label><input type="number" step="0.01" id="c" required />
    <label>Ondes et vibrations TD:</label><input type="number" step="0.01" id="d" required />
    <label>Ondes et vibrations TP:</label><input type="number" step="0.01" id="e" required />
    <label>ÉLECTROTECHNIQUE exam:</label><input type="number" step="0.01" id="f" required />
    <label>ÉLECTROTECHNIQUE TD:</label><input type="number" step="0.01" id="g" required />
    <label>ÉLECTROTECHNIQUE TP:</label><input type="number" step="0.01" id="h" required />
    <label>Électronique exam :</label><input type="number" step="0.01" id="i" required />
    <label>Électronique TD:</label><input type="number" step="0.01" id="j" required />
    <label>Électronique TP:</label><input type="number" step="0.01" id="k" required />
    <label>Informatique exam:</label><input type="number" step="0.01" id="l" required />
    <label>Informatique TD:</label><input type="number" step="0.01" id="m" required />
    <label>Etat de l'art génie électrique:</label><input type="number" step="0.01" id="n" required />
    <label>Logique combinatoires et séquentielle  TD:</label><input type="number" step="0.01" id="o" required />
    <label>Logique combinatoires et séquentielle  exam:</label><input type="number" step="0.01" id="p" required />
      <label>Anglais :</label><input type="number" step="0.01" id="q" required />
    <button type="submit">Calculate Average</button>
  </form>
  <div class="result" id="result"></div>

  <script>
    document.getElementById("notesForm").onsubmit = function(e) {
      e.preventDefault();
      const v = id => parseFloat(document.getElementById(id).value) || 0;
      const moyenne = (
        ((v("a")*0.6 + v("b")*0.4)*3 +
         (v("c")*0.6 + v("d")*0.2 + v("e")*0.2)*3 +
         (v("f")*0.6 + v("g")*0.4)*2  + 
         (v("i")*0.6 + v("j")*0.4 )*2 +
         (v("l")*0.6 + v("m")*0.4)*2  +
         (v("p")*0.6 + v("o")*0.4)*3  +
         v("q") + v("n") + v("h") + v("k")
        ) / 19
      ).toFixed(2);
      document.getElementById("result").innerText = "Your  average is: " + moyenne;
    };
  </script>
</body>
</html>
