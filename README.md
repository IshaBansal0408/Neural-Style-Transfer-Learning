# Neural Style Transfer Learning

Neural style transfer is an optimization technique used to take three images, a content image, a style reference image (such as an artwork by a famous painter), and the input image you want to style and blend them together such that the input image is transformed to look like the content image, but “painted” in the style of the style image. 

Style transfer is a fun and interesting technique that showcases the capabilities and internal representations of neural networks.

## Why Neural Style Transfer Learning?

Deep neural networks have already surpassed human level performance in tasks such as object recognition and detection. However, deep networks were lagging far behind in tasks like generating artistic artefacts having high perceptual quality until recent times. 

Creating better quality art using machine learning techniques is imperative for reaching human-like capabilities, as well as opens a new spectrum of possibilities. And with the advancement of computer hardware as well as the proliferation of deep learning, deep learning is right now being used to create art.

## How does Neural Style Transfer Work?

NST takes a content image, a style image and a generated image as inputs. It defines a loss function which blends two images seamlessly to create visually appealing art. NST uses a pre-trained model trained on ImageNet- VGG in TensorFlow. 

Images themselves make no sense to the model. These must be converted into raw pixels and given to the model to transform it into a set of features, which is what Convolutional Neural Networks are responsible for. 

Thus, somewhere in between the layers, where the image is fed into the model, and the layer, which gives the output, the model serves as a complex feature extractor. All we need to leverage from the model is its intermediate layers, and then use them to describe the content and style of the input images. 

The input image is transformed into representations that have more information about the content of the image, rather than the detailed pixel value. The features that we get from the higher levels of the model can be considered more related to the content of the image. To obtain a representation of the style of a reference image, we use the correlation between different filter responses. 

Neural networks are employed to recreate the styled images in a single, feed-forward pass. For example, VGG16 models pre-trained on ImageNet are employed. Each model is small and compact both in terms of the model’s depth and size and is trained for a single style blend at a particular pass. 

A single transmission network may create images in a variety of styles and merge them together. Style transfer networks are fed a content image and style images with an additional vector, indicating how much of each style should be applied to the image. This is a good technique to blend multiple styles and eliminates the overhead to train and store various models for different styles