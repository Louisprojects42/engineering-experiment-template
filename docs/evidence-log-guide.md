# Evidence log guide

This is a manual recordkeeping workflow; it does not install a watcher or Git hook.

## How this must be maintained

1. Before a change set, read the existing project log and any applicable repository instructions.
2. Append a uniquely numbered entry for every change set. Account for every
   affected file, including notes, inputs, generated outputs and this log.
   Related edits can share one entry; a sentence such as "updated docs" is insufficient.
3. Give date/context, purpose, before/after changes, reasoning, contributor roles,
   assumptions, unresolved decisions, exact checks and actual outcomes.
4. Save useful raw check/diff/run evidence in a dedicated local evidence directory and link
   it. Capture external source versions/sections and dates when used; do not
   treat a rolling website or a mutable local path as immutable evidence.
5. Record the base commit/dirty state. Mark the resulting commit pending until
   it exists. Later associate entries with a verified commit; never guess a hash.
6. Preserve earlier entries; append corrections with an entry ID and evidence.
   An invalid assumption or failed run must remain visible.
7. Keep contributor reflections in their own words. Identify AI drafting
   and external work. Do not automatically populate reflections or assert learning.
