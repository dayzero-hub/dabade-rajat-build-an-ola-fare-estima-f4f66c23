# Ola — fare estimate API (Python)

Welcome. This repository is **empty on purpose**. Everything in it is yours to create.

## Where the work is

Open the **Issues** tab. There are four, in order. Each one says exactly what done looks like,
and the fare rules are written out in full — there is nothing to invent.

One issue at a time:

```bash
git checkout main
git pull
git checkout -b issue-1
# ...make your changes...
git add .
git commit -m "Add the fare endpoint"
git push -u origin issue-1
```

Then open a **Pull Request** with `Closes #1` in the description. Raj reviews it.

## Setting up, once

You need Python 3. Check with `python3 --version`.

```bash
python3 -m venv .venv
source .venv/bin/activate          # Windows: .venv\Scripts\activate
pip install flask
python app.py
```

**The bit that catches everyone:** `source .venv/bin/activate` has to be run again in every
new terminal window. If `flask` is suddenly "not found", that is almost always why — you are
in a shell where the venv was never activated.

No database. No Docker. One dependency.

## Checking it worked

With the server running, in another terminal:

```bash
curl http://127.0.0.1:5000/health
```

Expect `{"status":"ok"}`.
