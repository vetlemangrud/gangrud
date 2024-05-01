# gangrud
GANgrud


# Things I did
Copyed https://realpython.com/generative-adversarial-networks/ (FCNN)
Changed input/output to be images
Changed to LeakyReLU because it was just oputputting 0
Read https://arxiv.org/abs/1511.06434 (DCGAN)
Changed to CNN, training time decreased, got more "cloudy outputs" (Different from the pixelated outputs of the FCNN)
Added a FCNN to create the initial 128 features, starting to get images that have a good shape
Trained for 100 epochs ~5 hours  (output2)
Test improving the discriminator (I thought that as long as the losses are low, it's good. But of course thats not the case)
Try changing to leaky ReLU on the discriminator as well (From the DCGAN paper)
Both models got a very low loss. Can this be a sign of mode collapse?

Possible fixes for mode collapse: (https://spotintelligence.com/2023/10/11/mode-collapse-in-gans-explained-how-to-detect-it-practical-solutions/)
-   Add noise to training images (I don't want noisy results, so I don't dp this)
-   Add dropout
-   Increase complexity of the generator
-   Try another dataset

Still get bad images. Try to closer replicate the model from the paper.
Get repeated patterns and very low loss, but the training speed has increased significantly. Speed increase probably from not using FCNN
Optimize training https://pytorch.org/tutorials/beginner/dcgan_faces_tutorial.html
That made it MUCH better. Loss is much more equal
Isolated speed increase to also be greatly influenced by dataset

# To get frames
ffmpeg -i src.mp4 frame%04d.png