# Hangman
PROJECT:- HANGMAN GAME (IN C LANGUAGE)
NAME:- Sanjith.S
REG.NO:- RA2111003011075
#include &lt;stdio.h&gt;
#include &lt;stdlib.h&gt;
#include &lt;stdbool.h&gt;
#include &lt;time.h&gt;
#include &lt;string.h&gt;
#define WORDS 10
#define WORDLEN 40
#define CHANCE 6
bool srand_called = false;
int i_rnd(int i) {
if (!srand_called) {
srand(time(NULL) &lt;&lt; 10);
srand_called = true;
}
return rand() % i;
}
char* decrypt(char* code) {
int hash = ((strlen(code) - 3) / 3) + 2;
char* decrypt = malloc(hash);
char* toFree = decrypt;
char* word = code;
for (int ch = *code; ch != &#39;\0&#39;; ch = *(++code))
{
if((code - word + 2) % 3 == 1){
*(decrypt++) = ch - (word - code + 1) - hash;
}
}
*decrypt = &#39;\0&#39;;
return toFree;
}
void printBody(int mistakes, char* body) {
printf(&quot;\tMistakes :%d\n&quot;, mistakes);
switch(mistakes) {
case 6: body[6] = &#39;\\&#39;; break;
case 5: body[5] = &#39;/&#39;; break;
case 4: body[4] = &#39;\\&#39;; break;
case 3: body[3] = &#39;|&#39;; break;
case 2: body[2] = &#39;/&#39;; break;
case 1: body[1] = &#39;)&#39;, body[0] = &#39;(&#39;; break;
default: break;
}
printf(&quot;\t _________\n&quot;
&quot;\t| |\n&quot;
&quot;\t| %c %c\n&quot;
&quot;\t| %c%c%c\n&quot;
&quot;\t| %c %c\n&quot;
&quot;\t| \n&quot;
&quot;\t| &quot;, body[0], body[1], body[2],
body[3], body[4], body[5], body[6]);

}
void printWord(char* guess, int len) {
printf(&quot;\t&quot;);
for (int i = 0; i &lt; len; ++i)
{
printf(&quot;%c &quot;, guess[i]);
}
printf(&quot;\n\n&quot;);
}
int main() {
printf(&quot;\n\t Be aware you can be hanged!!.&quot;);
printf(&quot;\n\n\t Rules : &quot;);
printf(&quot;\n\t - Maximum 6 mistakes are allowed.&quot;);
printf(&quot;\n\t - All alphabet are in lower case.&quot;);
printf(&quot;\n\t - All words are name of very popular Websites. eg.
Google&quot;);
printf(&quot;\n\t - If you enjoy continue, otherwise close it.&quot;);
printf(&quot;\n\t Syntax : Alphabet&quot;);
printf(&quot;\n\t Example : a \n\n&quot;);
char values[WORDS][WORDLEN] =
{&quot;N~mqOlJ^tZletXodeYgs&quot;,&quot;gCnDIfFQe^CdP^^B{hZpeLA^hv&quot;,&quot;7urtrtwQv{dt`&gt;^}FaR
]i]XUug^GI&quot;,
&quot;aSwfXsxOsWAlXScVQmjAWJG&quot;,&quot;cruD=idduvUdr=gmcauCmg]&quot;,&quot;BQt`zncypFVjvIaTl]u=
_?Aa}F&quot;,
&quot;iLvkKdT`yu~mWj[^gcO|&quot;,&quot;jSiLyzJ=vPmnv^`N]^&gt;ViAC^z_&quot;,&quot;xo|RqqhO|nNstjmzfiuo
iFfhwtdh~&quot;,
&quot;OHkttvxdp|[nnW]Drgaomdq&quot;};
char *body = malloc(CHANCE+1);
int id = i_rnd(WORDS);
char *word = decrypt(values[id]);
int len = strlen(word);
char *guessed = malloc(len);
char falseWord[CHANCE];
memset(body, &#39; &#39;, CHANCE+1);
memset(guessed, &#39;_&#39;, len);
char guess;
bool found;
char* win;
int mistakes = 0;
setvbuf(stdin, NULL, _IONBF, 0);
do {
found = false;
printf(&quot;\n\n&quot;);
printBody(mistakes, body);
printf(&quot;\n\n&quot;);
printf(&quot;\tFalse Letters : &quot;);
if(mistakes == 0) printf(&quot;None\n&quot;);
for (int i = 0; i &lt; mistakes; ++i)
{
printf(&quot;%c&quot;, falseWord[i]);
}
printf(&quot;\n\n&quot;);
printWord(guessed, len);
printf(&quot;\tGive me a alphabet in lower case : &quot;);

do {scanf(&quot;%c&quot;,&amp;guess);} while ( getchar() != &#39;\n&#39; );
for (int i = 0; i &lt; len; ++i)
{
if(word[i] == guess) {
found = true;
guessed[i] = guess;
}
}
if(!found) {
falseWord[mistakes] = guess;
mistakes += 1;
}
win = strchr(guessed, &#39;_&#39;);
}while(mistakes &lt; CHANCE &amp;&amp; win != NULL);
if(win == NULL) {
printf(&quot;\n&quot;);
printWord(guessed, len);
printf(&quot;\n\tCongrats! You have won : %s\n\n&quot;, word);
} else {
printf(&quot;\n&quot;);
printBody(mistakes, body);
printf(&quot;\n\n\tBetter try next time. Word was %s\n\n&quot;, word);
}
free(body);
free(word);
free(guessed);
return EXIT_SUCCESS;
}PROJECT:- HANGMAN GAME (IN C LANGUAGE)
NAME:- Sanjith.S
REG.NO:- RA2111003011075
#include &lt;stdio.h&gt;
#include &lt;stdlib.h&gt;
#include &lt;stdbool.h&gt;
#include &lt;time.h&gt;
#include &lt;string.h&gt;
#define WORDS 10
#define WORDLEN 40
#define CHANCE 6
bool srand_called = false;
int i_rnd(int i) {
if (!srand_called) {
srand(time(NULL) &lt;&lt; 10);
srand_called = true;
}
return rand() % i;
}
char* decrypt(char* code) {
int hash = ((strlen(code) - 3) / 3) + 2;
char* decrypt = malloc(hash);
char* toFree = decrypt;
char* word = code;
for (int ch = *code; ch != &#39;\0&#39;; ch = *(++code))
{
if((code - word + 2) % 3 == 1){
*(decrypt++) = ch - (word - code + 1) - hash;
}
}
*decrypt = &#39;\0&#39;;
return toFree;
}
void printBody(int mistakes, char* body) {
printf(&quot;\tMistakes :%d\n&quot;, mistakes);
switch(mistakes) {
case 6: body[6] = &#39;\\&#39;; break;
case 5: body[5] = &#39;/&#39;; break;
case 4: body[4] = &#39;\\&#39;; break;
case 3: body[3] = &#39;|&#39;; break;
case 2: body[2] = &#39;/&#39;; break;
case 1: body[1] = &#39;)&#39;, body[0] = &#39;(&#39;; break;
default: break;
}
printf(&quot;\t _________\n&quot;
&quot;\t| |\n&quot;
&quot;\t| %c %c\n&quot;
&quot;\t| %c%c%c\n&quot;
&quot;\t| %c %c\n&quot;
&quot;\t| \n&quot;
&quot;\t| &quot;, body[0], body[1], body[2],
body[3], body[4], body[5], body[6]);

}
void printWord(char* guess, int len) {
printf(&quot;\t&quot;);
for (int i = 0; i &lt; len; ++i)
{
printf(&quot;%c &quot;, guess[i]);
}
printf(&quot;\n\n&quot;);
}
int main() {
printf(&quot;\n\t Be aware you can be hanged!!.&quot;);
printf(&quot;\n\n\t Rules : &quot;);
printf(&quot;\n\t - Maximum 6 mistakes are allowed.&quot;);
printf(&quot;\n\t - All alphabet are in lower case.&quot;);
printf(&quot;\n\t - All words are name of very popular Websites. eg.
Google&quot;);
printf(&quot;\n\t - If you enjoy continue, otherwise close it.&quot;);
printf(&quot;\n\t Syntax : Alphabet&quot;);
printf(&quot;\n\t Example : a \n\n&quot;);
char values[WORDS][WORDLEN] =
{&quot;N~mqOlJ^tZletXodeYgs&quot;,&quot;gCnDIfFQe^CdP^^B{hZpeLA^hv&quot;,&quot;7urtrtwQv{dt`&gt;^}FaR
]i]XUug^GI&quot;,
&quot;aSwfXsxOsWAlXScVQmjAWJG&quot;,&quot;cruD=idduvUdr=gmcauCmg]&quot;,&quot;BQt`zncypFVjvIaTl]u=
_?Aa}F&quot;,
&quot;iLvkKdT`yu~mWj[^gcO|&quot;,&quot;jSiLyzJ=vPmnv^`N]^&gt;ViAC^z_&quot;,&quot;xo|RqqhO|nNstjmzfiuo
iFfhwtdh~&quot;,
&quot;OHkttvxdp|[nnW]Drgaomdq&quot;};
char *body = malloc(CHANCE+1);
int id = i_rnd(WORDS);
char *word = decrypt(values[id]);
int len = strlen(word);
char *guessed = malloc(len);
char falseWord[CHANCE];
memset(body, &#39; &#39;, CHANCE+1);
memset(guessed, &#39;_&#39;, len);
char guess;
bool found;
char* win;
int mistakes = 0;
setvbuf(stdin, NULL, _IONBF, 0);
do {
found = false;
printf(&quot;\n\n&quot;);
printBody(mistakes, body);
printf(&quot;\n\n&quot;);
printf(&quot;\tFalse Letters : &quot;);
if(mistakes == 0) printf(&quot;None\n&quot;);
for (int i = 0; i &lt; mistakes; ++i)
{
printf(&quot;%c&quot;, falseWord[i]);
}
printf(&quot;\n\n&quot;);
printWord(guessed, len);
printf(&quot;\tGive me a alphabet in lower case : &quot;);

do {scanf(&quot;%c&quot;,&amp;guess);} while ( getchar() != &#39;\n&#39; );
for (int i = 0; i &lt; len; ++i)
{
if(word[i] == guess) {
found = true;
guessed[i] = guess;
}
}
if(!found) {
falseWord[mistakes] = guess;
mistakes += 1;
}
win = strchr(guessed, &#39;_&#39;);
}while(mistakes &lt; CHANCE &amp;&amp; win != NULL);
if(win == NULL) {
printf(&quot;\n&quot;);
printWord(guessed, len);
printf(&quot;\n\tCongrats! You have won : %s\n\n&quot;, word);
} else {
printf(&quot;\n&quot;);
printBody(mistakes, body);
printf(&quot;\n\n\tBetter try next time. Word was %s\n\n&quot;, word);
}
free(body);
free(word);
free(guessed);
return EXIT_SUCCESS;
}
