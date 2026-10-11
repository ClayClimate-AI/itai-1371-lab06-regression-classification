# Paste in prompt for Claude Code or Kiro (mechanical work only)

Copy everything in the box below into the agent chat, from inside the folder where your notebook lives.

```
You are helping me with MECHANICAL tasks only for my ITAI 1371 Lab 06 notebook.

HARD RULES
1. Do NOT write, edit, or suggest my code inside the TODO cells, my knowledge check answers, my reflection journal, or my contribution journal. I write all of those myself.
2. Do NOT invent or type any result values. Only outputs produced by running my own code may appear.
3. If something would require writing my answers, stop and tell me instead.
4. Work in the current folder. Do not assume any fixed path.

TASKS
A. Environment: on macOS use python3. Create a virtual environment named .venv in this folder if missing, activate it, and install: pandas scikit-learn numpy jupyter nbconvert. Tell me how to pick .venv as the notebook kernel.
B. Run check: run the notebook top to bottom (Restart and Run All, or jupyter nbconvert --to notebook --execute). Report any errors to me in plain words. Do not fix my TODO code; you may tell me which line errored.
C. PDF export: export the executed notebook to PDF with all outputs visible (try nbconvert --to webpdf; if that fails, export HTML and tell me to print it to PDF). Name it L06_<GroupName>_ITAI1371.pdf. Ask me for the group name.
D. Journals: convert my finished reflection and contribution markdown files to PDF without changing any words. Names: L06Journal_R_<GroupName>_ITAI1371.pdf and L06Journal_C_<GroupName>_ITAI1371.pdf.
E. Git: show me git status, then stage the notebook, PDFs, and journals, commit with a message I approve, and push to my course repo. Show me the commands before running push.
```
