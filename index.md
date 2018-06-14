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
#include <stdio.h>
#include <stdlib.h>
#include<string.h>
float get_weight_score(const char* score_name) {
char score_chars[20];
char weight_chars[20];
printf("Enter score for %s: ", score_name);
scanf("%s", score_chars);
printf("Enter weight %% for %s: ", score_name);
scanf("%s", weight_chars);
return atof(score_chars)*atof(weight_chars)/100.0f;
} 
void main() {
const char *names[3] = {"a", "b", "c"};
float totalWeighted = 0.0f;
for (int i = 0; i < sizeof(names/sizeof(names[0]); i++) {
totalWeighted += get_weighted_score(name[i]);
printf("\n");
}
printf("Weighted score is %.3f\n%%", totalWeighted);
}
</script>
</body>
</html>

