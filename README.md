Here's where things stand. You want a requirements document for a new product, modeled on Linear where Linear already gets it right and new where your situation is different.

What to take from Linear:
- Its speed and strong defaults: keyboard-first, fast, and little to configure for most users
- Its core pieces: teams, projects, issues, iage inbox
- Intake from wherever people already are (Linear calls this Asks): Slack, email, forms, and in your case possibly from inside Maya or the engine editor
- Its delegation model: a person owns the ise, and each run is a session with a visiblestatus and a running log

What would be new (my proposals):
- A living spec as the source of truth for eain-language acceptance criteria. Every issue
 violation (fixed automatically, with a regression test added) or a spec gap (becomes a spec change the owner approves).
- Steering by editing documents: the owner changes the spec or the design, and the factory works out where to restart.
- Review built around evidence: preview environments, DCC captures, and test results, each tied back to the acceptance criteria it proves.
- Spec coverage: which criteria are actually verified, and which are only promised.
- Per-target adapters: git or Perforce, DCC version matrices, and deploy targets.
- Autonomy dials: how much the agent may do without asking, set per product.

Now your original question about configurability. My proposal has three levels:
1. Platform engineers write the workflow graphs, one template per kind of target, in the n8n-style editor.
2. Product owners pick a template and adjusts, required reviewers, autonomy level.
3. Screens are generated from what each step in the graph declares about itself, plus a small kit for building custom review pages.

The open part is how far product owners should go. Should they ever be able to change the steps themselves, for example adding an art director review before a Maya plugin ships? Or should they only adjust settings on steps the platform team provides? Letting them change but also many slightly different workflows to maintain, and it's the biggest factor in how complex the configuration interface gets.
