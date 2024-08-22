
The perturbation of the model's parameters induces a perturbation on the model's output $z^{(L)}$ 

$$
p(z^{(L)} \mid \mathcal{D}) = \int  \prod_{\mu=1}^{N_p} d\theta_{\mu} \; p(z^{(L)} \mid \theta, \mathcal{D})\, p(\theta)
$$

where $\theta$ is the vector of all parameters with $\operatorname{dim}(\theta) = N_P$, and $\mathcal{D}$ is the input data. The parameters are drawn from the distribution 

$$
p(\theta) = \delta(\theta^* - \theta) + \epsilon \mathcal{N}(\theta, \mu,\sigma), 
$$
where $\theta^*$ are the trained original parameters $\mathcal{N}$ is a normal distribution with mean $\mu$ and standard deviation $\sigma$. The $\epsilon$ is a small number reminding us that the perturbation is small. 

Substituting this expression into the induced distribution we find

$$
p(z^{(L)} \mid \mathcal{D}) = p(z^{* (L)} \mid \mathcal{D}) + \epsilon \int  \prod_{\mu=1}^{N_P} d\theta_{\mu} \, p(z^{(L)} \mid \theta, \mathcal{D}) \mathcal{N}(\theta, \mu,\sigma)
$$

The first term is the unperturbed model while the second term is a small perturbation. At first order in the large width approximation the network is Gaussian 
$$
p(z^{(L)} \mid \theta, \mathcal{D}) = \mathcal{N}(z, \tilde{\mu}, \tilde{\sigma}) + \mathcal{O}({\Delta}),
$$
where $\tilde{\mu}$ and $\tilde{\sigma}$ are the mean and standard deviation of the gaussian distribution, and $\mathcal{O}(\Delta)$ are higher-order corrections in the depth to width ratio $\Delta$. In the strict limit of infinite width networks, we get exact equality. 

Since the convolution of two gaussians is again gaussian, we find for the final distribution 

$$
p(z^{(L)} \mid \mathcal{D}) = p(z^{* (L)} \mid \mathcal{D}) + \epsilon \mathcal{N}(z, \mu + \tilde{\mu}, \sqrt{\sigma^2 + \tilde{\sigma}^2}) + \mathcal{O}(\Delta) 
$$

We see that the induced distribution is the unperturbed model distribution plus Gaussian noise up to higher order width corrections. Hence, steering the activation is equivalent to perturbing the model weights. 
