# Anthropic Just Told Us How to Prompt Claude

Source: https://www.youtube.com/watch?v=3F75mndbrxg  
Channel: John Kim (https://www.youtube.com/@JohnKimLife)  
Date: November 14, 2026

This note is based on the video's spoken transcript (auto-generated captions, lightly cleaned for readability). It was not based on a separately published official transcript.

## Key points

- Kim reads Addy Osmani's article "You're probably overprompting Claude" and adds his own take. He says he has felt this way for a while, including the view that skills can be band-aids for things a model could not previously do well.
- He agrees with the core pairing of a clear goal (a good spec or plan) and a way to verify that the goal was accomplished, then letting Claude figure out the rest. He starts with `/effort medium`, as the article recommends.
- He warns that people who built many skills on older models (he mentions Opus 4.8) and keep using them unchanged are probably overprompting without realizing it. His advice is to audit skills, try deleting some, and see whether Claude can still figure the work out.
- If you do not know what you want yet, he is less attached to specialized "interview me" skills. He says a recursive question, such as asking Claude what you might be missing, is often enough to surface things to consider.
- He agrees that if Claude can run a pass/fail or numeric check and read the report, it can keep going unattended. He is personally on auto mode and uses `/goal` often: he spends a lot of time planning, then lets long goals run, sometimes for days.
- He notes that verification works best where correctness is clear (pass/fail, faster or not). Subjective work such as writing, art, or comedy is improving but is not "technically solved," and human taste still shows up in editing and similar work.
- He calls the 80% system-prompt reduction, with no measurable coding-eval drop, striking, and says he has been deleting skills he no longer needs because the model can figure more out on its own. Rule files and skill files are context added because the model failed in the past; some domain context is still needed, but process instructions may now get in the way.
- He had not known about `/doctor prompt-audit` and says he wants to try it.
- On subagents, he agrees they should be reserved for substantial standalone work. He has used them for adversarial review (a second agent that did not write the code) and for parallelization. He now finds "agent teams" often overkill because the model can do more itself, though he still uses a captain or chief-of-staff orchestration pattern, which he treats as different from ordinary subagents.
- He restates Osmani's point that a single agent with skills can outperform a subagent design on quality, often at lower cost and latency.
- On cloud sessions, he repeats the article's workflow and adds that some high-tier Claude plans include separate cloud-session API credits, which he thinks people should try for work that can leave the local machine.
- He already uses a project or chief-of-staff pattern (one lead agent juggling sub-sessions, with the option to jump into a sub-agent and steer it). He had not used the Claude Code Projects feature described in the article and wants to try it. He notes it sometimes asks for extra allow lists, even with bypass permissions, which he dislikes.
- Review still matters. He points viewers to his earlier videos on code review and on how Anthropic reviews code.
- He agrees you should audit how you work when new models arrive and test new capabilities (he mentions visual understanding and video editing). His closing argument is that software practice is changing faster than it did for years, and engineers who want to stay relevant need to adapt, even if they do not chase every new tool. He still prefers coding in Codex or Claude Code.

## Takeaway

The useful habit is not writing more skills. It is pruning the ones written for older models, giving Claude a clear goal plus a check it can run, and keeping humans in the loop for taste and review.
