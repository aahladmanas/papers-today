# log

1. 4/9 - Grading, HW 3 solutions, GAN basic check, manifold-flow implementation
1. 4/10   
    1. First Manifold experiment after 100 epochs, reconstruction is not great.
    2. Set multiple inpainting GAN experiments to check whether the old results are reproducible at this stage.
    3. Continued default COVIDomaly auto-encoder experiment. Ran until 600 epochs
    4. Set different COVIDomaly experiments on 64x64 images, 64 latent dim, and l1loss.
1.4/11  
    1. [Inpainting GAN] Saw that default hyperparams + larger LR was getting decent generation at 64x64.
    2. [Inpainting GAN] Using this set of default hyperparams + LR in (1e-3, 1e-4), set experiments with conditional generation. Seem to be going well.
    3. [ERM on reconstructed images]
    4. [Manifold-flow]: Look at manifold-flow architecture, and set other manifold-flow experiments  
1. 5/6  
    1. [cardio data] Clean up code to include patient class in constructing visits which has implications for constructing condition occurrence.
    2. [NURD] pixelSNAIL generation takes forever to generate. 30 hours for the whole dataset. I'm generating a smaller data with only 1/3rd the samples and running  NURD and ERM  
    3. [NURD] Ran ensemble weight model with a resnet on the joint xray data to see if results improve.
    4. [NURD] Implemented the accuracy on randomly colored image to understand the interplay between statistical bias and optimization bias on CMNIST with exact weights (in range 0.6 --- 0.9)


# thoughts

1. Want to finish a high-level document over the workshop and send to Maggie.


# papers




# Tricks

1. scancel batch : ```squeue -u $USER | grep 6653 | awk '{print $1}' | xargs -n 1 scancel```
