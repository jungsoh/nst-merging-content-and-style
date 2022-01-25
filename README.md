# Neural style transfer: Merging content and style
[Neural style transfer](https://arxiv.org/abs/1508.06576) is one of the most fun and interesting optimization techniques in deep learning. It merges two images, namely: a **'content'** image (C) and a **'style'** image (S), to create a **'generated'** image (G). The generated image G combines the 'content' of the image C with the 'style' of image S. 

We will combine the Louvre museum in Paris (content image C) with the impressionist style of Claude Monet (style image S):

![louvre generated](images/louvre_generated.png)

Most of the deep learning algorithms optimize a cost function to get a set of parameter values. With neural style transfer, we optimize a cost function to get pixel values.

I did this project in the [Convolutional Neural Networks](https://www.coursera.org/learn/convolutional-neural-networks) course as part of the [Deep Learning Specialization](https://www.coursera.org/specializations/deep-learning).

## Pretrained model
Neural style transfer uses a previously trained convolutional network and builds on top of that. The idea of using a network trained on a different task and applying it to a new task is called transfer learning.

We use the the VGG network from the original paper, specifically VGG-19, a 19-layer version of the VGG network. This model has already been trained on the very large ImageNet database, and has learned to recognize a variety of low level features (at the shallower layers) and high level features (at the deeper layers).

## Generation results
The picture above shows the generated image after running around 20,000 epochs with a learning rate of 0.001 to merge the Louvre museum image and the impressionist style painting of Claude Monet.

A few other examples:
- The beautiful ruins of the ancient city of Persepolis (Iran) with the style of Van Gogh (The Starry Night):

![perspolis plus vangogh](images/perspolis_vangogh.png)

- The tomb of Cyrus the great in Pasargadae with the style of a Ceramic Kashi from Ispahan:

![pasargad plus kashi](images/pasargad_kashi.png)

- A scientific study of a turbulent fluid with the style of a abstract blue fluid painting:

![circle plus abstract](images/circle_abstract.png)
