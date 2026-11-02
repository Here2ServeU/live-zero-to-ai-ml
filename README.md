# Zero to AI-ML Systems Engineering · Free Live Sessions

From your first terminal command to a tested fraud-detection API, no experience needed

Free, live, 30-minute sessions with **Dr. Emmanuel Naweji** ([Transformed 2 Succeed](https://transformed2succeed.com)).
This course is presented on **Week 2, Monday at 7:30 PM Central** of a 4-week rotation (8 courses, every Monday and Thursday).
This repo holds the slides, the recording of every live session, and the notes and links from each one.

## Session recordings

| Date | Recording | Notes |
|---|---|---|
| _First session coming soon_ | | |
<!-- sessions:end -->

## What the session covers

1. **Talk to the Machine**: Use a terminal, learn Python's five building blocks, test a rule on 5,000 payments.
2. **Teach a Machine the Rule**: Train a decision tree, catch it memorising, judge it with recall and a dial.
3. **Put Your Model to Work**: Track every run, crown a champion, serve it with Flask, test it with pytest.

## Three things to remember

- **Data in, decision out**: Module 1: terminal, five building blocks, a rule tested on 5,000 payments.
- **Never grade on the study pile**: Module 2: split, catch overfitting, judge with recall, precision and a dial.
- **Save it, serve it, test it**: Module 3: notebook, champion, a Flask API, and pytest checking it.

## Try it yourself

Clone the course lab repo: [zero-2-ai-foundations](https://github.com/Here2ServeU/zero-2-ai-foundations)

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

## Slides

[`slides/03_Zero_to_AI_ML_Systems_Engineering_Free_Live_Session.pptx`](slides/03_Zero_to_AI_ML_Systems_Engineering_Free_Live_Session.pptx): the presenter deck, with full speaker notes.

## Free live session schedule (Mondays and Thursdays, 7:30 PM Central)

| Week | Day | Course |
|---|---|---|
| Week 1 | Monday | [Linux for AI-ML Systems](https://github.com/Here2ServeU/live-linux-for-ai-ml) |
| Week 1 | Thursday | [Python for AI-ML](https://github.com/Here2ServeU/live-python-for-ai-ml) |
| Week 2 | Monday | **Zero to AI-ML Systems Engineering** (this repo) |
| Week 2 | Thursday | [DevOps for AI-ML Systems](https://github.com/Here2ServeU/live-devops-for-ai-ml) |
| Week 3 | Monday | [SRE for AI-ML Systems](https://github.com/Here2ServeU/live-sre-for-ai-ml) |
| Week 3 | Thursday | [GPU Optimization for AI-ML Systems](https://github.com/Here2ServeU/live-gpu-optimization-for-ai-ml) |
| Week 4 | Monday | [FinOps for AI-ML Systems](https://github.com/Here2ServeU/live-finops-for-ai-ml) |
| Week 4 | Thursday | [AI Agent Operations](https://github.com/Here2ServeU/live-ai-agent-operations) |

## Want all of it?

The membership gives you **all 8 courses, every module and every lab, for $49/month**, plus a live session every month where we build something together.
Join at **https://transformed2succeed.com**.

---

### For the presenter: logging a session

After each live session, run:

```bash
bash scripts/new-session.sh 2026-11-03 "https://link-to-the-recording"
git add -A && git commit -m "Session 2026-11-03" && git push
```

This creates `sessions/2026-11-03.md` from the template (fill in the Q&A and links) and adds a row to the recordings table above.
