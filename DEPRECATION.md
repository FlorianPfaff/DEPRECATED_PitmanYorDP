# Discontinuation and research lessons

Status: discontinued on 2026-11-11. These repositories preserve a reproducible
research record; development of this candidate into a full tracker or a new
tracking-method paper has stopped.

## What we learned

- Marginal birth counts, annotated target counts, and observed track spans do
  not by themselves select a Dirichlet-process or Pitman--Yor partition prior.
  Clip boundaries, missed detections, exposure, and population heterogeneity
  must be separated from genuine prior effects.
- For the tested point-target model with at most two frames, the discount's
  association effect disappears after matching the complete detected-identity
  count law conditional on each possible target-generated subset. Matching only
  a mean count is not enough.
- Three or more frames permit a residual occupancy preference. In three frames,
  the candidate is a one-parameter preference for triple-hit tracks; its factor
  can be absorbed into finite temporal-pattern weights. This is not, by itself,
  a novel random-process family or a new tracking contribution.
- A locked exact-inference study compared the residual discount against fitted
  homogeneous and heterogeneous survival models, with common count and
  measurement models and explicit latent clutter. It did not establish a
  useful improvement.

## Why we discontinued this direction

The confirmation experiment used **6,400 fresh scenes across 32 fixed regimes**.
The primary association-score gain was **-0.00022553 nats per observation**, with
a paired normal-approximation 95% interval of **[-0.00042184, -0.00002922]**.
Positive gain would favor the discount. The prespecified practically useful
gain was **+0.02 nats per observation**.

The selected discount procedure was slightly worse, by a small amount, rather
than meaningfully better. Development selected zero discount in 19 of 32
mixed-survival regimes and all 32 conventional PYP fits. The practical-benefit
gate failed, and a distinct new-method contribution remained unestablished.
We therefore stopped before building a full tracker or running independent
real-detector benchmarks. A scoped negative result does not automatically make
a publishable negative-results paper.

This conclusion concerns the tested finite-window candidate, not all Pitman--Yor
tracking. It is limited to three- and four-frame scenes conditioned on at most
nine observations, the specified population/survival laws, known observation
settings, and regime-specific fitted parameters. The intervals condition on the
locked development fits. No general rejection of PYP, live-cardinality result,
or real-data tracking-performance claim follows.

## Preserved evidence

- [Final code and experiment runner](https://github.com/FlorianPfaff/DEPRECATED_PitmanYorDP/tree/e0285377f05efe398372f9cb2632de546d6a565c).
- [Final manuscript and research record](https://github.com/FlorianPfaff/DEPRECATED_2026-07-PitmanYorDP-Paper/tree/5932dbf0b66e096677b03512c2a249c420451d88).
- [Detailed decision and limitations](https://github.com/FlorianPfaff/DEPRECATED_2026-07-PitmanYorDP-Paper/blob/5932dbf0b66e096677b03512c2a249c420451d88/notes/association-feasibility-decision.md).
- [Locked protocol and model](https://github.com/FlorianPfaff/DEPRECATED_2026-07-PitmanYorDP-Paper/blob/5932dbf0b66e096677b03512c2a249c420451d88/notes/association-feasibility.md).
- [Confirmation lock, source hashes, decision, and all paired scores](https://github.com/FlorianPfaff/DEPRECATED_2026-07-PitmanYorDP-Paper/tree/5932dbf0b66e096677b03512c2a249c420451d88/results/association_feasibility).

The final study remains in these preserved research commits; the deprecation
does not merge the experimental branches into the historical default-branch
scaffold. This note supersedes earlier count-tail-based rejection claims and
unvalidated prior-family recommendations. Existing repository visibility is
unchanged, so access to the paper's evidence requires its existing permissions.
