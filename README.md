# Convolutional Neural Networks for Tissue Screening in Intestinal Immunohistochemistry Images

MSc Computer Science dissertation, University of Bath, September 2026.

**[Read the dissertation (PDF)](dissertation.pdf)**

The Human Protein Atlas holds millions of immunohistochemistry images, but analysis of a slide cannot start until an expert judges whether the tissue section is readable, and the atlas does not record that judgement anywhere. This project formalises the judgement for small-intestine tissue and then automates it:

- A usability rubric written with a domain expert, and a web annotation tool the expert used to label 847 slides.
- That dataset extended to 5,900 images with a vision-language model that matched the expert's labels 85% of the time.
- A ResNet-50 readability classifier reaching macro-F1 0.82 under donor-grouped cross-validation (grouped so that similar slides from one donor never sit on both sides of a split).
- A weakly supervised localiser trained only on whole-slide labels; its top pick lands on an expert-confirmed readable region in 90% of slides.

One result I did not expect going in: expert label quality, not data volume, set the ceiling on what the screening models could achieve.

The code and datasets live in a separate private repository (they include collaborator credentials and bulk image data). I'm happy to walk through them on request.
