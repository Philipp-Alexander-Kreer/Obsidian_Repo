
Add iteratively noise to data (e.g., Gaussian) to the extent that model seems to only noise. Reconstruct data from noisy representation.

**Interpretation of Difusion Models:**
1. Denoising model: removes step by step the noise.
2. Noise predictor: Predicts the noise added when going from $t_{i-1}$ to $t_i$.
3. Matches [[Denoising Score]]

You can make more sophisticated versions of this by adding conditions to the probability distribution which generates the noise. 