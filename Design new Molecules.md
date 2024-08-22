**Source:** [Automatic Chemical Design Using a Data-Driven Continuous Representation of Molecules](https://pubs.acs.org/doi/10.1021/acscentsci.7b00572)

Train a Variational Autoencoder to encode diagramtic representation of chemicals. Map them to a latent space, decode from the latent space. 

Take latent vector of trained network, dump it into a neural network which is trained to classify the chemical properties based on the latent vector.

Modify latent vector till you find the desired properties. Decode latent vector to find chemical design. 


**Idea:**
Does something similar work to interpret LLMs? -> It seems Neel Nanda did something like that 
[Gemma 2 Exploration](https://www.neuronpedia.org/gemma-scope#main)
[Twitter Post](https://x.com/NeelNanda5/status/1818680642621915527)
