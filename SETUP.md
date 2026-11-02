# Set up your lab: Zero to AI-ML Systems Engineering

When you finish, you will have Python, the five lab packages and a 5,000-payment practice dataset ready, plus a quick test for each of Modules 1 to 3. Plan on about 10 to 15 minutes, once.

## What you need
- Any computer: Windows, Mac, Linux, or just a web browser (GitHub Codespaces).
- About 1 GB of free disk space for Python and the lab packages.
- A free GitHub account (only if you use Codespaces or `git clone`).
- Python 3.10 or newer, Git, and a terminal (the one inside VS Code is fine).
- Five Python packages, installed for you in Step 3: pandas, scikit-learn, joblib, flask, pytest.
- No GPU needed. No API keys or paid accounts needed.
- No coding experience needed.

## Step 1 · Pick where to run it

### Option A: GitHub Codespaces (easiest, any computer)
Everything is already installed. You only need a browser.
1. Sign in to GitHub and open this repo.
2. Click **Code > Codespaces > Create codespace**.
3. Wait for the editor to open. A terminal is at the bottom.
4. Check your tools:
```bash
python3 --version
git --version
```

### Option B: Windows (PowerShell)
1. Go to https://www.python.org/downloads/ and click the big download button.
2. On the very first installer screen, tick **Add Python to PATH**. This is the step people miss.
3. Install Git from https://git-scm.com/downloads.
4. Open a **new** PowerShell window and check:
```powershell
python --version
git --version
```
On Windows, type `python` wherever this guide says `python3`.

### Option C: Mac (Terminal)
1. Install Python from https://www.python.org/downloads/.
2. Open Terminal and check Git. If a box asks to install developer tools, click **Install**.
```bash
git --version
python3 --version
```

## Step 2 · Get the lab files
Download [zero-2-ai-foundations-lab.zip](downloads/zero-2-ai-foundations-lab.zip) from this repo. The zip has no top folder, so unzip it into a new folder and step into it.

Mac, Linux or Codespaces:
```bash
unzip zero-2-ai-foundations-lab.zip -d zero-2-ai-foundations
cd zero-2-ai-foundations
```
(In Codespaces the zip is already in `downloads/`, so use `unzip downloads/zero-2-ai-foundations-lab.zip -d zero-2-ai-foundations`.)

Windows PowerShell (run it in the folder where the zip was saved):
```powershell
Expand-Archive zero-2-ai-foundations-lab.zip -DestinationPath zero-2-ai-foundations
cd zero-2-ai-foundations
```

**Or** clone the public lab repo instead:
```bash
git clone https://github.com/Here2ServeU/zero-2-ai-foundations
cd zero-2-ai-foundations
```

## Step 3 · Install and check
Run these from inside the lab folder. The first line makes a virtual environment (`.venv`), a private toolbox for this project only.

Mac, Linux or Codespaces:
```bash
python3 -m venv .venv && source .venv/bin/activate
pip install -r requirements.txt
python3 data/make_data.py
bash setup/doctor.sh
```

Windows PowerShell:
```powershell
python -m venv .venv
.venv\Scripts\Activate.ps1
pip install -r requirements.txt
python data/make_data.py
```
Then run `bash setup/doctor.sh` from Git Bash (installed with Git) in the same folder.

You should see your prompt start with `(.venv)`, then:
```
wrote 5000 payments to data/transactions.csv (137 fraud)
  [ OK ]  Python 3.x.x
  [ OK ]  git version 2.x.x
  [ OK ]  package pandas
  ...
  [ OK ]  dataset ready
```
Every doctor line should say `[ OK ]`. Each `[WARN]` line tells you how to fix it.

## Step 4 · Quick test for each module
Run every command from the lab folder with `(.venv)` active.

**Module 1 · Talk to the Machine**
```bash
python3 module-1/hello.py
python3 module-1/explore.py
```
You should see `Hello, Sam!`, then on the last line of the second command:
`Your rule caught 61 of 137 frauds and raised 59 false alarms.`

**Module 2 · Teach a Machine the Rule**
```bash
python3 module-2/train.py --max_depth 3
python3 module-2/judge.py --threshold 0.2
```
You should see `train accuracy 97.7%   test accuracy 98.0%`, then the judge printing `'Always LEGIT' accuracy: 97.3%` and `recall    66.7%`.

**Module 3 · Put Your Model to Work**
```bash
python3 module-3/track.py --max_depth 4 --threshold 0.2
python3 module-3/best.py
python3 -m pytest module-3/tests -q
```
You should see `run 1: ... recall 67%  precision 34%`, then `Best: run 1 ...`, then `5 passed`.

Want to call the API yourself? Start it with `python3 module-3/api.py` (it keeps running; stop it with Ctrl-C). In a second terminal:
```bash
curl -X POST localhost:5000/predict -H "Content-Type: application/json" \
     -d '{"amount": 2500, "hour": 3, "new_device": 1}'
```
You should see `"label": "FRAUD"`. On Windows PowerShell, type `curl.exe` instead of `curl`.

## If something goes wrong
- **`python3` not found on Windows.** Type `python` instead. If that also fails, re-run the installer and tick **Add Python to PATH**, then open a new terminal.
- **A tool you just installed is "not found".** Close the terminal and open a new one. A terminal only learns where your tools live when it opens.
- **PowerShell says running scripts is disabled.** Run this once, then activate again:
  ```powershell
  Set-ExecutionPolicy -Scope CurrentUser RemoteSigned
  ```
- **Doctor says `package ... missing`.** Your `(.venv)` is probably off. Run the activate line from Step 3 again, then `pip install -r requirements.txt`.
- **`dataset missing` or `No such file: data/transactions.csv`.** Run `python3 data/make_data.py`, and run every script from the lab folder, not from inside `module-1/`.
- **Module 3 tests or `api.py` fail with `current.joblib` not found.** Run `track.py` and then `best.py` first. They create the model the API loads.
- **Still stuck after 15 minutes?** Switch to Codespaces (Option A). Nothing to install.

## Official guides
- GitHub Codespaces: https://docs.github.com/codespaces
- Python downloads: https://www.python.org/downloads/
- Git downloads: https://git-scm.com/downloads
- Course lab repo: https://github.com/Here2ServeU/zero-2-ai-foundations
