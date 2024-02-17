A state of the art model deals with denoising the images, which are combined with text prompt using U-Net model.
The description of this detailed work is given below, but let me tell you the brief description about the architecture of the system.
First of all Encoder is used for image to transfer image in latent space, and clip model is used for self attention or to find out the main points from the given prompt (basically, which part is given more attention than other part).
I have used VQ-VAE model to obtain a discrete latent representation, and later on during the decoding process of latent vectors we would replace this U-net output with codebook demonstrating the generative quality of VQ-VAE.
At last I have used discriminator for comparision of generated image and the real image, for better construction of those images.
