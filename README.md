# AI-Based-Minecraft-PBR-Texture-Generator

## 1. Data Collection and Preprocessing:
- **Input**: Collect diffuse maps as input images.
- **Output**: Prepare the corresponding Height maps, Normal maps, and MER maps for training. For MER maps:
  - **Red Channel**: Metalness.
  - **Green Channel**: Emissive.
  - **Blue Channel**: Roughness.
- **Normalization**: Normalize the input and output images to ensure consistency in the pixel values.

## U-Net Architecture:
  The U-Net architecture is a type of **convolutional neural network** (CNN) primarily designed for image segmentation tasks, where the goal is to classify each pixel in an image into a specific category. It was originally introduced for biomedical image segmentation but has since been applied to various other image processing tasks.

### Structure of U-Net:
- **Encoder**: Extracts features from the input image using convolutional layers (Conv2D) followed by max pooling (MaxPooling2D) to downsample the image.
- **Bottleneck**: The deepest part of the U-Net, where the most abstract features are learned.
- **Decoder**: Reconstructs the image to its original size using transposed convolutions (Conv2DTranspose) and concatenates (concatenate) the features from the corresponding encoder layer.
- **Output Layer**: A final convolutional layer with 7 output channels and a sigmoid activation function, which is typical for regression tasks involving image outputs.

## Generating PBR Maps:
**Prediction**: Once the model is trained, you can use it to generate PBR maps for new diffuse inputs. The trained model takes a diffuse map as input and outputs the corresponding height, normal, and MER maps.
**Post-processing**: The output from the model might need some post-processing to ensure they are in the correct format for PBR rendering engines.
