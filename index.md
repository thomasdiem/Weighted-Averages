#include <stdio.h>
#include <stdlib.h>
#include<string.h>
float get_weighted_score(const char* score_name) {
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
for (int i = 0; i < 3; i++) 
{
totalWeighted += get_weighted_score(names[i]);
printf("\n");}

printf("Weighted score is %.3f\n%%", totalWeighted); 
}


