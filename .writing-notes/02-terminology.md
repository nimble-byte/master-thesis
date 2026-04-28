---
file: contents/02-terminology.tex
section: sssec:terminology
issue_id: "#32"
---

# Writing Notes

- utilise definition provided by *Arrieta et al. (2020)*
    - refers back to Cambridge dictionary for definition of **explanation**
        - "the details or reasons that someone gives to make something clear or easy to understand"
        - points out that **details and reasons** as well as the **clear understanding** highly depend on the audience
    - arrives at final definition: "Given an audience, an explainable artificial intelligence is one that produces details or reasons to make its functioning clear or easy to understand."
- discuss different terms used (**interpretability**, **explainability**, **transparency**)
	- particularly interpretability and explainability are erroneously used interchangeably in literature (*Arrieta et al. (2020)*)
	- **interpretability** refers to the provide meaning in terms understandable to a human (*Arrieta et al. (2020)*)
		- is a passive quality (*Arrieta et al. (2020)*)
		- is the more general term of the two
	- **explainability** is limited to the use of explanations as interface between AI and humans (*Guidotti et al. (2018)*)
		- is one mode of interpretability (*Lipton (2018)*)
		- term most often used by now (*utilise a figure showing timeline of publications under relevant keywords*)
	- **transparency** is quality informally defined as opposite of "back-box" (*Lipton (2018*)
		- models are transparent, if they are interpretable by themselves (i.e., dependent on audience)
		- three levels: whole model, individual components and training algorithm
		- **comprehensibility** as scale on which transparency is one extreme tied to model complexity (*Guidotti et al. (2018)*)
- discuss learnings from cognitive psychology (*Miller (2019)*)
	- primary interest in "explanation as a product"
        - "explanations represent the answer to a why question" (*Overton (2011), Lipton (1990)*)
        - three different types of questions behind "Why" (*Miller (2019)*) (*represent as table with columns Question, Reasoning, Description*)
            - **What**: Reason about which unobserved events could have occured given observed events (using Associative reasoning)
            - **How**: Simulate a change in the situation to see if the event still happens (using Interventionist reasoning)
            - **Why**: Simulating alternative causes to see whether the event still happens (using Counterfactual reasoning)
        - different explanation types are useful for different purposes and audiences (*Miller (2019)*)
	- people ask for explanations for different reasons (*which plays into the judgement of usefulness*)
		- primary reason is learning (*Lombrozo 2006*); understand a phenomenon (i.e. the output of a model)
		- lay user is interested in most complex "why" question; experts could be contempt with "how" or an approximation
	- computation of complete causal chains is not useful for XAI
		- computational complexity is very high for "complete causes" (*Lipton (1990)*)
		- humans usually look for contrastive explanations, that often provide "sufficient causes" (*Kelley (1987)*)
	- beliefs, desires, and intentions (BDI) play a crucial role in the judgement of explanations (*Kashima et al. (1998)*)

# Open Questions

- Which canonical source should be foregrounded for the definition: `Arrieta2020` or `Lipton2018`? (I recommend `Arrieta2020` for taxonomy; `Lipton2018` for critique.)
   - yes this is exactly right and matches my intention well
- Do you want to keep the Cambridge Dictionary quote as an explicit citation, or prefer strictly peer-reviewed sources?
   - retain the peer-reviewed sources; direct citation is not needed
- Shall we adopt one preferred term throughout the thesis (`explainability` vs `interpretability`) and note alternatives, or retain both depending on context?
   - we will use "explainability" as the preferred term, consistent with the majority of recent literature, but will note "interpretability" as the more general term and explain the distinction in the text
- Include a small figure (timeline of term use) and a table (What/How/Why) in the final subsection? I can draft both.
   - please prepare a stub figure with a placeholder caption and no image imported for now; figure will be added manually after the text is finalised; the table can just be generated as LaTeX code and included in the text, no need for a separate file
- Do we need short illustrative vignettes for each explanation type (what/how/why)?
	- yes, include one compact shared vignette that contrasts what/how/why explanations (about 2-4 lines total), and avoid extended examples in this subsection

# Missing Citations

- [x] `Guidotti2018` — Guidotti et al. (2018)
- [x] `Overton2011` — Overton (2011) or similar source on explanation-as-why
- [x] `Lombrozo2006` — Lombrozo (2006)
- [x] `Kelley1972` — Kelley (1972) updated to Kelley (1987)
- [x] `Kashima1998` — Kashima et al. (1998)
