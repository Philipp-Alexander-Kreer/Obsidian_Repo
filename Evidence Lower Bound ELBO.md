$$
\log \mathbb{E}_{q_{\phi}(z)}\left[\frac{p_{\theta}(x|z) \, p(z)}{q_{\phi}(z)}\right] \geq \mathbb{E}_{q_{\phi}(z)}\left[\log \frac{p_{\theta}(x|z) \, p(z)}{q_{\phi}(z)}\right]
$$
The ELBO is an approximation which is very useful to train [[Latent Variable Models]], by beeing useful to approximate the loss function.

Training = Maximize ELBO while minimizing KL divergence.