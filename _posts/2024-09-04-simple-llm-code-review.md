---
layout: post
title: Simple LLM code review
author: mattipulkkinen
excerpt: I created a simple script that does code reviews using LLM. Here's how I did it.
tags:
  - LLM
  - AI
  - GenAI
  - PowerShell
  - CI/CD
---

- had the opportunity (past six months or so, I've been playing with GenAI tools)
- found the idea interesting. When discussed about it the first time, I received a comment that LLM PR Code review feedback loop is too long. Noted and I agree.
- Azure DevOps didn't really have good ready-made solutions (some where there, but only dozens or few hundred downloads and no sources available. WHAT ARE THEY DOING WITH MY CODES??)
- So I created it myself. Can't be that hard, right?
- If you want to skip the text and just see the full implementations, you can find them [here](https://github.com/solita/llm-code-review)

## The solution

- PowerShell script, that works in localhost and in CI/CD pipelines
- Azure DevOps pipeline configuration
- Setup Azure DevOps pull request build validation
- An alias to make local usage easier

But before we get any further, a couple of disclaimers:

- this is a PoC
- there are limitations, e.g. I have limited the number of line changes allowed
- ...

## PowerShell script

I'll skip some parts as they're not that interesting or relevant. You can find them in the

```powershell
Write-Output 'Hello World!'
```

## Azure DevOps pipeline yaml

```yaml
triggers: none
```

## Azure DevOps pull request build validation

- These instructions only work if your codes are in Azure DevOps. PR build validation is configured differently if your codes are e.g. in GitHub!
- Short instructions with screenshots
- Link to more detailed instructions

## After thoughts

- Really cost efficients, running LLM for reasonable size requests isn't that expensive and a single good point is worth it!
- Add some actual token / cost -example here
- Getting markdown from GPT models is quite nice, as Azure DevOps renders them
- Different runs return different comments -> ???

## Warning

- Don't trust this blindly, LLMs do a lot of mistakes (as do people), so think as a nice addition, rather than a replacement for a human PR review.
