<!DOCTYPE html>
<html>
<body>
<head><div style= "font-size:30px;font-weight:bold"> Calculate Weighted Averages</div></head>
<form>
 <fieldset>
  <legend>Input your scores and weights here:</legend>
  <span style="color:red">Category A:</span> <input id="a" type="text""> <span style="color:red">Weight(%):</span> <input id="aweight" type="text""><br>
  <span style="color:blue">Category B:</span> <input id="b" type="text""> <span style="color:blue">Weight(%):</span> <input id="bweight" type="text""><br>
  <span style="color:green">Category C:</span> <input id="c" type="text""> <span style="color:green">Weight(%):</span> <input id="cweight" type="text""><br>
 </fieldset>
 <button type="button" onclick="inputfunc()">Calculate</button>
 <p id="score">Score: </p>
</form>
<script type="text/javascript">
	inputfunc = function() {
    	var a = parseFloat(document.getElementById("a").value);
    	var aweight = parseFloat(document.getElementById("aweight").value);
    	var b = parseFloat(document.getElementById("b").value);
    	var bweight = parseFloat(document.getElementById("bweight").value);
    	var c = parseFloat(document.getElementById("c").value);
    	var cweight = parseFloat(document.getElementById("cweight").value);
        
        if (isNaN(a)) a = 0;
        if (isNaN(aweight)) aweight = 0;
        if (isNaN(b)) b = 0;
        if (isNaN(bweight)) bweight = 0;
        if (isNaN(c)) c = 0;
        if (isNaN(cweight)) cweight = 0;
        
        var score = a*aweight/100 + b*bweight/100 + c*cweight/100;
        
        if (aweight + bweight + cweight != 100) {
         document.getElementById("score").innerHTML = "weights don't add up to 100"
        } else {
            document.getElementById("score").innerHTML = "Score: " + score.toString();
        }
    }
</script>
</body>
</html>

