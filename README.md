# Army Operations Mastery Quiz

A free, browser-based practice aid for the *Introduction to Army Operations* lesson. Students enter a name, confirm the study warning, and take a 25-question Easy, Medium, or Hard examination at https://atticus-42.github.io/army-operations-scenario-quiz/. Questions are reshuffled on every attempt.

The 75 questions are fictional Philippine Army situations built only from the lesson notebook: the constitutional mandate and operational platforms, full spectrum operations, offensive and defensive tasks, support to civil governance, the tenets of Army operations, Army power and the warfighting functions, and the principles of Army operations. The lesson has no numbered slides, so questions carry no `sourceSlides` and the feedback shows no "Lesson reference" line (the field stays optional and is validated whenever a question includes it).

No login, payment, analytics, cookies, advertising, external fonts, images, scripts or runtime libraries. Answers stay in browser memory. Only the name, difficulty, score and finish time are sent to the class history Google Sheet (tab "Army Operations History", lesson key `armyops`) through `HISTORY_ENDPOINT` in `src/template.html`.

`src/questions/` holds the three banks, `src/template.html` is the page source, and `scripts/build.mjs` produces the self-contained `index.html`. `apps-script/Code.gs` is the shared history web app (one spreadsheet, one tab per lesson). Test gate:

```sh
node scripts/build.mjs && node scripts/verify.mjs
```
