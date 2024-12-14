## Idea:
Add an auto-regressively generated memory to NAR processor (fuse information from it via cross-attention) and use contrastive objective (just like in [THIS](https://arxiv.org/pdf/2302.10258) and [THIS](https://arxiv.org/pdf/2306.13411) papers). Suggested architecture sketch:
![extra-ARM-GNN](https://github.com/user-attachments/assets/0320d72f-5717-42d9-96ed-f441f93aa2f9)

## Motivation 
* Much less constraint compared to usual hint-prediction mode
* Force processor to extract similar features (<<ideas>>) for similar algorithms at each step, not trying to make trajectories identical. That might help to learn multiple algorithms at once.
* <<Remembers>> first extracted (presumably simplest) features that might be helpful at later steps (eg. the shortest edge for each vertex for search algorithms).
