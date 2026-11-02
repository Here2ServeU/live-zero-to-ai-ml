# Zero to AI-ML Systems Engineering · Free Live Sessions

From your first terminal command to a tested fraud-detection API, no experience needed

**Free · Live · 30 minutes · Mondays and Thursdays, 7:30 PM Central** · with Emmanuel N. ([Transformed 2 Succeed](https://transformed2succeed.com))

### [Register free on Zoom](https://us06web.zoom.us/meeting/register/fT235rLjQaihJYrWj2_vjw)

Register once and you're in for every session. Zoom emails you the join link and reminders. Bring your questions: every session ends with live Q&A.

## Watch the recordings

Missed a session or want to watch it again? Recordings are added here after each live session.

| Date | Recording |
|---|---|
| _Coming after the first session_ | |

## Set up your lab (do this before you join)

Want to code along? Follow **[SETUP.md](SETUP.md)**. It takes about 15 minutes, once, and works on any computer (or right in your browser with GitHub Codespaces).

## Downloads

Everything you need is in the [`downloads`](downloads) folder:

| File | What it is |
|---|---|
| [03_Zero_to_AI_ML_Systems_Engineering_Free_Live_Session.pdf](downloads/03_Zero_to_AI_ML_Systems_Engineering_Free_Live_Session.pdf) | The session slides (PDF) |
| [03_Zero_to_AI_ML_Systems_Engineering_SETUP_GUIDE.pdf](downloads/03_Zero_to_AI_ML_Systems_Engineering_SETUP_GUIDE.pdf) | The setup guide (PDF version of SETUP.md) |
| [zero-2-ai-foundations-lab.zip](downloads/zero-2-ai-foundations-lab.zip) | The lab files (unzip, then follow SETUP.md) |


## What you'll learn

1. **Talk to the Machine**: Use a terminal, learn Python's five building blocks, test a rule on 5,000 payments.
2. **Teach a Machine the Rule**: Train a decision tree, catch it memorising, judge it with recall and a dial.
3. **Put Your Model to Work**: Track every run, crown a champion, serve it with Flask, test it with pytest.

## Three things to remember

- **Data in, decision out**: Module 1: terminal, five building blocks, a rule tested on 5,000 payments.
- **Never grade on the study pile**: Module 2: split, catch overfitting, judge with recall, precision and a dial.
- **Save it, serve it, test it**: Module 3: notebook, champion, a Flask API, and pytest checking it.

## Try it yourself

To get the lab files, download **[zero-2-ai-foundations-lab.zip](downloads/zero-2-ai-foundations-lab.zip)** from the downloads folder (see [SETUP.md](SETUP.md)).

**Module 1 · Talk to the Machine**: Run your rule, then test it on 5,000 payments

```bash
python3 module-1/hello.py
python3 module-1/rule.py
python3 module-1/explore.py
```

**Module 2 · Teach a Machine the Rule**: Train it, judge it, then turn the dial

```bash
python3 module-2/train.py --max_depth 3
python3 module-2/judge.py
python3 module-2/judge.py --threshold 0.2
```

**Module 3 · Put Your Model to Work**: Serve it, then knock on the door

```bash
python3 module-3/api.py        # terminal 1
curl -X POST localhost:5000/predict \
  -H "Content-Type: application/json" \
  -d '{"amount": 2500, "hour": 3, "new_device": 1}'
```

## All free live sessions

A different course every session. The rotation repeats every 4 weeks, so if you miss one, it comes back around.

| Week | Day | Course |
|---|---|---|
| Week 1 | Monday | [Linux for AI-ML Systems](https://github.com/Here2ServeU/live-linux-for-ai-ml) |
| Week 1 | Thursday | [Python for AI-ML](https://github.com/Here2ServeU/live-python-for-ai-ml) |
| Week 2 | Monday | **Zero to AI-ML Systems Engineering** (you are here) |
| Week 2 | Thursday | [DevOps for AI-ML Systems](https://github.com/Here2ServeU/live-devops-for-ai-ml) |
| Week 3 | Monday | [SRE for AI-ML Systems](https://github.com/Here2ServeU/live-sre-for-ai-ml) |
| Week 3 | Thursday | [GPU Optimization for AI-ML Systems](https://github.com/Here2ServeU/live-gpu-optimization-for-ai-ml) |
| Week 4 | Monday | [FinOps for AI-ML Systems](https://github.com/Here2ServeU/live-finops-for-ai-ml) |
| Week 4 | Thursday | [AI Agent Operations](https://github.com/Here2ServeU/live-ai-agent-operations) |

## Want the full course?

The membership gives you **all 8 courses, every module and every lab, for $49/month**, plus a live session every month where we build something together.

**[Join at transformed2succeed.com](https://transformed2succeed.com)**
