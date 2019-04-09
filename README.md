# Video-Intermediate-Frame-Generation
Video intermediate frame generation based on GAN

The original code we used is a network code for high resolution. Therefore, the network need to be modified to a network structure suitable for generating video intermediate frames. Our input is three frames: the first frame, the intermediate frame, and the back frame, where the first frame and the back frame are used for input to the gan network for training, thereby outputting an intermediate frame picture, and then using the real intermediate frame and the generated intermediate frame to calculate losses.

Another contribution we make is the creation of a data set for intermediate frame generation. It includes three types of pictures with size of 64 * 64, 128 * 128, and 256 * 256. Each class has a data volume of 2000 to 4000, with images every three groups as our input. Note that in order to prevent the montage of the movie from causing the shot to switch, we use the image similarity algorithm to filter out the unqualified examples.
