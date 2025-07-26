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
    <label>Math appliquées exam:</label><input type="number" step="0.01" id="a" onchange=live_calcule() />
    <label>Math appliquées TD:</label><input type="number" step="0.01" id="b"  />
    <label>Ondes et vibrations  exam:</label><input type="number" step="0.01" id="c"  />
    <label>Ondes et vibrations TD:</label><input type="number" step="0.01" id="d"  />
    <label>Ondes et vibrations TP:</label><input type="number" step="0.01" id="e"  />
    <label>ÉLECTROTECHNIQUE exam:</label><input type="number" step="0.01" id="f"  />
    <label>ÉLECTROTECHNIQUE TD:</label><input type="number" step="0.01" id="g"  />
    <label>ÉLECTROTECHNIQUE TP:</label><input type="number" step="0.01" id="h"  />
    <label>Électronique exam :</label><input type="number" step="0.01" id="i"  />
    <label>Électronique TD:</label><input type="number" step="0.01" id="j"  />
    <label>Électronique TP:</label><input type="number" step="0.01" id="k"  />
    <label>Informatique exam:</label><input type="number" step="0.01" id="l"  />
    <label>Informatique TD:</label><input type="number" step="0.01" id="m"  />
    <label>Etat de l'art génie électrique:</label><input type="number" step="0.01" id="n"  />
    <label>Logique combinatoires et séquentielle  TD:</label><input type="number" step="0.01" id="o"  />
    <label>Logique combinatoires et séquentielle  exam:</label><input type="number" step="0.01" id="p"  />
      <label>Anglais :</label><input type="number" step="0.01" id="q"  />
    <button type="submit">Calculate Average</button>
  </form>
  <div class="result" id="result"></div>

  <script>
    function live_calcule(){
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
