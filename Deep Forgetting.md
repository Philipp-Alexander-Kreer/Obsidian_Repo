[Deep Forgetting  & Underlearning for Safely Scoped LLMs](https://www.alignmentforum.org/posts/mFAvspg4sXkrfZ7FA/deep-forgetting-and-unlearning-for-safely-scoped-llms)

Fine-tuning can rapidly undo safety training.
## Scoping latent capabilities
- Passive: only allows specific types of tasks on which the model is trained for.
  $\Rightarrow$ Incapable of anything else.
- Active: makes the model forget only specific undesired properties.

---

## Various methods to make model forget (or not even learn)

- **Clean data:** Prevent the model from learning undesired behavior in the first place.
- **Compress model:** Is that really useful?
- **Meta learning:** Not only train to perform good on a specific task but also perform bad on others.
- **Interpret model and change its behavior:** (e.g., mechanism interpretation)
