# gangrud
GANgrud


# Things I did
Copyed https://realpython.com/generative-adversarial-networks/ (FCNN)
Changed input/output to be images
Changed to LeakyReLU because it was just oputputting 0
Read https://arxiv.org/abs/1511.06434 (DCGAN)
Changed to CNN, training time decreased, got more "cloudy outputs" (Different from the pixelated outputs of the FCNN)
Added a FCNN to create the initial 128 features, starting to get images that have a good shape




# To get frames
ffmpeg -i src.mp4 frame%04d.png