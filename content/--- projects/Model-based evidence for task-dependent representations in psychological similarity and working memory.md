---
updated: 2026-11-03
project_name: orientationModeling
project_status: under review
aliases:
  - orientationModeling
concept(s):
  - "[[representational geometry]]"
  - continuous report
  - psychological similarity
lab_members:
collaborator(s): Michael Lee
prereg_url:
data_repo: https://github.com/mdlee/orientationModeling
code_repo: https://github.com/mdlee/orientationModeling
preprint: https://osf.io/preprints/psyarxiv/fm9vz_v3
paper_doi:
paper_journal:
---
Classic formal models of cognition rely on multidimensional scaling (MDS) of similarity-based ratings or judgments to derive a psychological representation ([[representational geometry]]). The distances in this representation can be used to predict different cognitive behaviours, such as generalisations or categorisation. A recently developed model, the [[Target Confusability Competition model]] ([[Schurgin et al., 2020]]), _similarly_ uses empirical similarity-based ratings to model error distributions from continuous report tasks.

We set out to build a model that infers what the underlying representation in a cognitive task (a Thurstonian model) with a Bayesian approach. In brief, the model assumes that the latent representation of a stimulus is a circular Gaussian distribution centred on a certain value ($\mu$) with some dispersion ($\sigma$); in this case, $\mu$ for a particular stimulus representation lies between 0 and $\pi$ (the possible orientation angles of a bar). Then, by asserting how the cognitive task is completed, we can derive posterior likelihoods for each parameter for each stimulus. 

This figure shows our key result – each panel corresponds to the cognitive tasks (a perceptual reproduction task, a working memory (continuous report) task, a quad psychophysical similarity task) and a common-core model (a shared representation across all cognitive tasks). The horizontal axis refers to the orientation angle of the shown line; the vertical axis refers to the credible interval of the $\mu$ value of each stimulus. It is clear that the latent representations (or the [[representational geometry]]) for the orientation of lines varies across the different cognitive tasks.

![[imgs/fourScatter.png]]

--- 
#project