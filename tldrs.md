## Highly accurate protein structure prediction with AlphaFold
- TLDR ID: 1
- *John Jumper, Richard Evans, Alexander Pritzel, Tim Green, Michael Figurnov, Olaf Ronneberger, Kathryn Tunyasuvunakool, Russ Bates, Augustin Žídek, Anna Potapenko, Alex Bridgland, Clemens Meyer, Simon A. A. Kohl, Andrew J. Ballard, Andrew Cowie, Bernardino Romera-Paredes, Stanislav Nikolov, Rishub Jain, Jonas Adler, Trevor Back, Stig Petersen, David Reiman, Ellen Clancy, Michal Zielinski, Martin Steinegger, Michalina Pacholska, Tamas Berghammer, Sebastian Bodenstein, David Silver, Oriol Vinyals, Andrew W. Senior, Koray Kavukcuoglu, Pushmeet Kohli & Demis Hassabis*
- Nature (2021)
- https://www.nature.com/articles/s41586-021-03819-2
- Implementations:
  - https://github.com/deepmind/alphafold
### What?
- AlfaFold2 predicts 3D coordinates of a protein from its amino acid sequence.
- Inputs:
  - Query existing genetic databases to build the multiple sequence alignment.
  - Search for similar protein structures in the database for templates.
- Feed this to the transformer with a twist (Evoformer).
- Predictions are done in the iterative way.
### Why?
3D structure of a protein gives us information about the protein behaviour. Doing this experimentally takes long time and a lot of money.
### So What?
- Top 1 at ICASP14.
- Tremendous uptake in the community, AF2 is at the technology stage enabling novel research directions and bosting the old ones.
- DM releases a 200 mil + database of protein structures 
---

## Planning chemical syntheses with deep neural networks and symbolic AI
- TLDR ID: 2
- *Marwin Segler, Mike Preuss, Mark Waller*
- Nature (2018)
- https://www.nature.com/articles/nature25978
### What?
- Predicts how to synthesize target molecules.
- Idea:
  - "World model" pre-trained on chemical reactions predicts reverse chemical reactions.
  - Reaction feasibility model estimates whether a reaction is feasible.
  - The world model is a policy, which is then coupled with the feasibility model in an MCTS/RL-based search algorithm, which operates on a hypergraph representation.
  - Search is recursively done until molecule is decomposed in to a set of pre-defined building block molecules

### Why?
Chemical Synthesis can be a bottleneck in molecular drug discovery (in particular hit2lead and lead optimization) and drug manufacture, and is usally quite costly. Predicting chemical syntheses is also important for computational workflows which propose novel molecules.
### So What?
- Demonstrated for the first time that purely ML driven methods can provide reasonable synthesis routes.
- Paved the way for modern synthesis planning to become part of in-silico discovery pipelines.
- An early demonstration of RL-based planning in a fully learned world model.
---
