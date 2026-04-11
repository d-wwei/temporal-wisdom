# Temporal Wisdom Anti-Patterns

Detailed reference for detecting and fixing reasoning failures specific to temporal thinking.

---

## 1. Short-Termism

**Pattern**: Choosing options with clear immediate payoff over options with superior compound trajectory. Discounting the future because it's uncertain, even when the compounding math is straightforward.

**Detection**:
- Decision framing focuses exclusively on "this quarter" or "this sprint" without projecting forward
- The phrase "we'll deal with that later" appears as a load-bearing argument
- Trade-offs are evaluated at a single point in time rather than across a trajectory
- Compound costs (tech debt interest, relationship erosion, skill atrophy) are treated as zero

**Fix**: Project both options forward 3 years. Calculate the compound divergence. If the "boring" option produces 10x better outcomes at the 3-year mark, the immediate payoff needs to be extraordinarily large to justify the short-term choice.

```
Bad: "We should ship the quick hack now and clean it up later."
     → "Later" never comes. Each hack compounds into a codebase where every change takes 3x longer.

Good: "This hack saves 2 days now but adds ~30 minutes to every future change in this module.
      We touch this module 4x/month. Break-even is 3 months. If this codebase will exist in a year,
      the clean solution is cheaper by month 4. What's our timeline?"
```

---

## 2. Pseudo-Patience

**Pattern**: Using "long-term thinking" or "strategic patience" as intellectual cover for avoiding difficult, necessary, immediate action. The time horizon becomes a shield against accountability.

**Detection**:
- "We're playing the long game" but no specific capability is being built during the wait
- Patience is cited when the actual problem is fear of conflict, uncertainty, or effort
- No measurable progress toward the stated long-term goal during the "patient" period
- The same "long-term play" justification has been used for 6+ months with no visible accumulation

**Fix**: Ask: "What specific capability, asset, or position am I accumulating during this wait? What is different about my situation each month?" If the answer is "nothing" or "we're just waiting for the market to turn," it's pseudo-patience.

```
Bad: "We're not worried about losing market share. We're focused on the long-term product vision."
     → Twelve months later, same market share loss, same "vision," no new capability built.

Good: "We're deliberately not competing on price this year because we're building the data flywheel
      that will make our product 10x better by Q3 next year. Here are our monthly accumulation
      metrics: data volume, model accuracy, user retention in the cohort using the new features."
```

---

## 3. Phase Mismatch

**Pattern**: Applying a strategy that belongs to a different phase of the situation. Offensive moves during defensive phases waste resources. Defensive caution during offensive windows wastes opportunity.

**Detection**:
- Aggressive expansion when cash runway is < 12 months (offensive in defensive)
- "Let's wait and see" when a competitive window is clearly closing (defensive in offensive)
- Major infrastructure investment when the product hasn't found market fit (stalemate action in defensive phase)
- Refusing to commit resources when accumulated advantage is clearly ready to deploy (defensive in offensive)

**Fix**: Explicitly name the current phase using the signals table (resource ratio, momentum, risk profile). Then check whether the proposed action matches. If someone proposes an offensive action, verify offensive-phase signals are present.

```
Bad: "We just raised our Series A, so let's expand to 5 new markets simultaneously!"
     → Series A = still defensive/early-stalemate. Resources are limited. 5 markets = offensive play.
     The money runs out before any market is won.

Good: "We raised Series A. Our phase: late defensive, entering stalemate in our core market.
      Strategy: deepen product-market fit in one market, accumulate the playbook and unit economics
      that will fuel expansion. We expand to market #2 when our core market is self-sustaining."
```

---

## 4. Linear Extrapolation

**Pattern**: Projecting current growth rates, decline rates, or competitive dynamics forward without considering phase transitions, tipping points, or structural changes in the environment.

**Detection**:
- Forecasts that extend current quarter's growth rate to 5-year projections
- "At this rate, we'll reach X by year Y" without identifying what changes at scale
- Ignoring S-curves, market saturation, competitive response, or regulatory reaction
- Treating early exponential growth as sustainable or treating temporary setback as permanent decline

**Fix**: Identify the nearest likely phase transition. Ask: "What changes at 2x, 5x, 10x the current scale? What assumptions break?" Model the phase transition explicitly rather than extrapolating through it.

```
Bad: "We're growing 20% month-over-month. At this rate we'll have 10M users by year-end."
     → Growth will hit an S-curve. Early adopters are not the same as mainstream users.
     Channel saturation, competitor response, and support scaling will all bend the curve.

Good: "We're growing 20% MoM in early-adopter channels. This rate likely holds until ~500K users
      (channel saturation). The phase transition to mainstream requires different acquisition
      strategies and likely drops growth to 5-8% MoM. Our 10M target requires solving
      the mainstream-crossover problem, not just extending current channels."
```

---

## 5. Sunk Cost Patience

**Pattern**: Persisting with a strategy not because it's right but because significant resources have already been invested. This disguises itself as "patience" or "commitment" but is actually inertia driven by loss aversion.

**Detection**:
- The primary argument for continuing is "we've already invested X" rather than "the future trajectory is promising"
- Switching costs are treated as reasons to stay rather than as sunk costs
- "We can't give up now, we're so close" — but "so close" has been the claim for multiple cycles
- The strategy would not be chosen if starting fresh today with current knowledge

**Fix**: Apply the clean-slate test: "If I were starting from zero today, with everything I now know, would I choose this same path?" If the answer is no, continuing is sunk-cost reasoning. The resources already spent are gone regardless — the only question is whether the future trajectory justifies future investment.

```
Bad: "We've spent 18 months and $2M building this platform. We can't abandon it now."
     → The 18 months and $2M are gone whether you continue or not. The question is whether
     the NEXT 6 months and $500K produce a better return here or elsewhere.

Good: "We've invested heavily in this platform, so let me apply the clean-slate test.
      If I were starting today with $500K and 6 months, would I build this? The answer is no —
      the market has shifted, and a lighter approach would serve better. The prior investment
      gave us knowledge (not wasted), but continuing on this path means the next $500K
      is also poorly allocated. Time to redirect."
```

---

## Quick Self-Check Sequence

When reviewing your output for temporal thinking anti-patterns, scan in this order:

1. **Time horizon** -> Short-termism? (Am I optimizing only for the immediate frame?)
2. **Action vs inaction** -> Pseudo-patience? (Am I using "long-term" to avoid acting?)
3. **Phase alignment** -> Phase mismatch? (Does my strategy match the current phase?)
4. **Projection method** -> Linear extrapolation? (Am I projecting through a phase boundary?)
5. **Persistence motive** -> Sunk cost patience? (Am I continuing because it's right, or because I've invested?)
