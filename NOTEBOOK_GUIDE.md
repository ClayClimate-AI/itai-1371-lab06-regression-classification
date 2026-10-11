# Lab 06 Notebook Guide

A walk through the starter notebook, cell by cell. This tells you what each part asks and which idea it uses. It does not give you the code or the answers. Concept numbers point to sections in BRIEF.md.

Before you start: Restart and Run All often. Run cells in order.

---

## Cell 1: Title and objective (markdown)
Nothing to do. Goal: understand regression vs classification and build one linear model of each type.

## Cell 2: Part 1, Regression vs Classification (markdown)
Read it. Concept: BRIEF 2.
* Ask yourself: for each example listed (house price, spam, flower type, churn), which kind is it and why?

## Cell 3: Part 2, Linear Regression (markdown)
Problem: predict `Fare` from `Age` and `Pclass`. Concepts: BRIEF 3, 6.

## Cell 4: Setup code for regression (already written, just run it)
What it does: loads Titanic from GitHub, drops rows missing Age, picks features and target, splits 80/20 with `random_state=42`.
* Compare with your midterm: you used 70/30 with seed 33. What does `random_state` buy you?
* Why might dropping missing Age rows be a choice with a cost? How many rows survive? (You can check with `df.shape`.)
* Needs internet for the CSV.

## Cell 5: Task 1 instructions (markdown)
Four steps: create the model, fit it, predict on test, compute MSE. Concepts: BRIEF 3, 4, 5.

## Cell 6: Task 1 code (YOUR TODO)
The comments show the shape of each line. You fill them in.
* **Create:** which class was imported at the top of Cell 4? An instance is that class name followed by `()`.
* **Train:** `.fit` needs two things. Which variables hold the training features and the training answers?
* **Predict:** `.predict` takes only features. Training or test features? Why?
* **Evaluate:** `mean_squared_error(actual, predicted)`. Which is which?
* **Heads up:** the printed line uses `np.sqrt`, but numpy is not imported anywhere. What one line fixes that?
* **Heads up:** the comment says "off by about $48." Replace that with what your own output shows, or remove the claim.
* Guiding question: is your RMSE big or small compared with a typical fare? What does that say about Age and Pclass as predictors?

## Cell 7: Part 3, Logistic Regression (markdown)
Problem: predict `Survived` from `Age`, `Pclass`, `Sex`. Concepts: BRIEF 10 to 14.

## Cell 8: Setup code for classification (already written, run once)
Maps Sex to numbers, picks features, splits 80/20.
* **Heads up:** running this cell twice turns `Sex` into blanks. If an error mentions NaN, Restart and Run All.
* Compare: here Sex is mapped to 0 and 1 by hand. In your midterm you used one hot encoding for categories. When is a simple 0/1 map fine, and when do you need one hot?

## Cell 9: Task 2 instructions (markdown)
Same four steps, with `LogisticRegression` and `accuracy_score`.

## Cell 10: Task 2 code (YOUR TODO)
Mirror your Task 1 structure with the classification variables (names end in `_cls`).
* If you see a convergence warning, read it. What does "converge" mean (BRIEF 4)? Look up the `max_iter` parameter in the scikit learn docs.
* Guiding questions: what share of passengers survived in the data? What accuracy would a model get by always guessing the most common answer? Is your model better than that baseline? (Midterm link: the 4.7% stroke lesson, BRIEF 15.)
* Optional curiosity (not required): `log_model.coef_` and `.predict_proba` show the sigmoid at work. The slides call this "quantify Women First."

## Cell 11: Knowledge Check (YOUR ANSWERS, in your own words)
Write in the markdown cell, replacing `[ENTER YOUR ANSWERS HERE]`.

1. **Difference between regression and classification.** Concept: BRIEF 2. Think about the "ruler vs buckets" test and give your own example, maybe from your stroke project.
2. **Print `lr_model.coef_`. What do the numbers represent?** Concept: BRIEF 7. Add a small code cell to print it. Questions to guide you: how many numbers are there and why? Which feature does each belong to? What does the sign mean? What does one unit of Pclass mean?
3. **Why MSE for regression, accuracy for classification? Why not accuracy for fare?** Concepts: BRIEF 5, 15. Think: how often would a predicted fare match the real fare to the exact cent?

Write these after you run the code, using what you saw.

---

## Finish line
1. Kernel: Restart and Run All. No red errors.
2. Export to PDF with all outputs visible.
3. Name the files (see CRITERIA_MAP.md).
4. Commit and push to GitHub.
