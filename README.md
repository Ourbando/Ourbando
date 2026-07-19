<!-- You read the source before trusting the render. We will get along. ourbando@proton.me -->
<div align="center">
  <img src="https://raw.githubusercontent.com/Ourbando/Ourbando/main/assets/hero.gif" width="760" alt="Pixel film: a small green creature rides its own pipeline around a looping world, is refused at the diamond gate with a red flash, gets a lightbulb idea, passes when the gate turns green through the green run-chamber while the vault seals the record, blows a bug infestation off the pipes in a moonlit grove, rests by an aurora-lit cove with a lighthouse, then rides on home as the world wraps around" />
  <br/>
  <sub><em>Even the keeper goes through the gate.</em></sub>
</div>

<h1 align="center">Armando Shkambi</h1>

<div align="center"><strong>The AI can propose any action but execute none. A deterministic gate it cannot reach decides what runs.</strong></div>

<div align="center">
  <br/>
  <strong>400+ merged pull requests</strong> &nbsp;·&nbsp; <strong>5,500+ passing tests</strong> &nbsp;·&nbsp; <strong>over 60,000+ lines</strong> &nbsp;·&nbsp; <strong>330+ modules</strong>
</div>

In under a year, working solo on one laptop, I built a control layer that keeps AI coding agents in check. The agents write the code. The architecture, the debugging, and every call about what the system is allowed to trust are mine. Self-taught, in London.

<div align="center">
  <img src="https://raw.githubusercontent.com/Ourbando/Ourbando/main/assets/divider.svg" width="760" alt="" />
</div>

### Why I built it

I didn't plan to build this. I wanted to take on bigger projects than I could handle alone, and AI agents were the obvious way there. The catch was trusting them. Before I could build anything ambitious on top of them, I had to build the layer that makes an unreliable agent trustworthy enough to hand real work to. That turned into the actual work, and the part I care about most. It started as a means to an end and is becoming valuable on its own, and there is a lot further I want to take it.

<div align="center">
  <img src="https://raw.githubusercontent.com/Ourbando/Ourbando/main/assets/divider.svg" width="760" alt="" />
</div>

### What it does

Teams are pointing AI agents at real codebases, and almost no one can show the agents stay contained. My system closes that gap: a deterministic gate makes every decision, and the model can't reach it, so a jailbreak or a prompt injection changes what the agent asks for, never what it can do. With agents writing the code, the hard part is deciding what is allowed to run, and that layer is the system.

<div align="center">
  <picture>
    <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/Ourbando/Ourbando/main/assets/gatecheck_light.svg?v=1" />
    <img src="https://raw.githubusercontent.com/Ourbando/Ourbando/main/assets/gatecheck.svg?v=5" width="760" alt="Pixel flow diagram: an untrusted AI agent console emits proposal pulses up a feeder pipe into the main line and through the deterministic gate. Allowed pulses run on through the green chamber and a streak seals the signed, tamper-evident log in the vault. Blocked pulses are refused, dropping into the red drain." />
  </picture>
</div>

Every run leaves a signed record anyone can re-run and check, on a tamper-evident history, with an honest line between what it proves and what still needs a person.

```diff
  $ verify --receipt latest
+ ALLOW    write tests/test_rate_limit.py    ran, logged
+ ALLOW    run pytest -q                     ran, logged
- REFUSED  git push --force origin main      blocked, logged
+ receipt verified: signature good, history intact, re-run matches
```

<div align="center">
  <strong>It runs air-gapped &nbsp;·&nbsp; on your own hardware &nbsp;·&nbsp; in pure Python &nbsp;·&nbsp; with almost no third-party code</strong>
</div>

It isn't safe, because nothing autonomous is. The point is to make the risk small, checkable, and provable. The how stays off this page on purpose: it is the part that makes it work, and the part worth protecting.

<div align="center">
  <img src="https://raw.githubusercontent.com/Ourbando/Ourbando/main/assets/divider.svg" width="760" alt="" />
</div>

### The scar tissue

Every safeguard exists because something got through first.

<details><summary><strong>700,000 orphaned files</strong> a runaway agent left behind</summary>
<br/>One agent, one bad loop, one weekend of cleanup. The rule it produced runs in milliseconds and has caught the same mistake since.
</details>
<details><summary>tests that passed alone and <strong>failed only in parallel</strong></summary>
<br/>Green a thousand times solo, red the moment they shared a machine. Hunting that class of failure changed how every test here is allowed to run.
</details>
<details><summary>a safety check that <strong>ran green while doing nothing</strong></summary>
<br/>The most dangerous kind of passing: a guard that never actually guarded. The fix was structural, and the full story is better in person.
</details>

Ask me about any of them.

<div align="center">
  <img src="https://raw.githubusercontent.com/Ourbando/Ourbando/main/assets/divider.svg" width="760" alt="" />
</div>

### Now

Open to AI-engineering roles, London or remote UK, and I can start immediately (no notice period). It stays private while I turn it into a product, and I am happy to walk a serious party through it live.

[ourbando@proton.me](mailto:ourbando@proton.me)

<div align="center">
  <a href="mailto:ourbando@proton.me">
    <img src="https://raw.githubusercontent.com/Ourbando/Ourbando/main/assets/footer_world.svg?v=3" width="760" alt="The keeper stands at the centre of his miniature pixel ring world under floating stars and an aurora, with a speech bubble inviting you to click and message his creator" />
  </a>
</div>
