# Architecture examination

Examine the assigned architecture in light of the supplied intent and constraints. Be rigorous about its concepts, boundaries, and tradeoffs. Work from the actual code or design and its surrounding context, not from a preference for a particular pattern. Raise grounded concerns even when there is no demonstrated bug; distinguish evidence from assumptions and questions for the programmer.

Investigate these lenses where relevant:

- **Depth:** What useful behavior and difficult decisions does a module hide, and what must its callers understand, configure, sequence, or handle? A deep module offers substantial value through a comparatively simple interface. Assess the abstraction's value rather than counting lines or methods. A thin adapter can still have a useful boundary.
- **Responsibility at each level:** What decisions, rules, and invariants does each module own? Look for unrelated responsibilities that change independently, as well as one responsibility scattered across modules. A parent may coordinate distinct responsibilities owned by submodules, but its own interface should express a focused responsibility. Coordination is not necessarily ownership of the children's rules.
- **Interface breadth:** Consider the whole burden on callers, including informal obligations, side effects, ordering, errors, and assumptions. A wide interface can be appropriate when it serves the module's coherent responsibility; method count alone is not a finding.
- **Information hiding and change:** Identify difficult or likely-to-change decisions and trace where their details are known. Would a relevant change require unrelated parts to change together? Examine whether decomposition follows the knowledge being managed or merely the order of execution.
- **Dependencies and layers:** Trace significant calls, data, shared assumptions, and dependency direction. Does each layer offer a meaningful abstraction? Do boundaries or cycles make the system harder to understand or change? Coupling and forwarding are not automatically defects.
- **Contracts and quality goals:** Examine the ownership of important invariants and guarantees, including failure behavior and relevant trust boundaries. Consider concrete usage, change, load, or failure scenarios where appropriate, and how design choices affect the qualities the project actually needs.

For each suspicion, identify the relevant locations or design elements, the concern and reasoning, and any assumptions or uncertainty. Explain a concrete consequence or scenario when available; otherwise explain the question the programmer should clarify. Suggest an alternative and its tradeoffs when useful. Do not require a demonstrated defect or an invented future requirement to raise a concern.

Background: [Ousterhout on modular design](https://web.stanford.edu/~ouster/cgi-bin/cs190-winter18/lecture.php%3Ftopic=modularDesign); [Parnas on decomposing systems into modules](https://doi.org/10.1145/361598.361623); [CMU on architectural tradeoffs](https://www.sei.cmu.edu/library/architecture-tradeoff-analysis-method-collection/).
