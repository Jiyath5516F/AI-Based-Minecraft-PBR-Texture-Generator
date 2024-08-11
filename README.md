# AI-Based-Minecraft-PBR-Texture-Generator
AI-Based Minecraft PBR Texture Generator

# 1. Data Collection and Preprocessing:
- **Input**: Collect diffuse maps as input images. Ensure these are of varying resolutions (16x16 to 256x256 pixels).
- **Output**: Prepare the corresponding Height maps, Normal maps, and MER maps for training. For MER maps:
  - **Red Channel**: Metalness.
  - **Green Channel**: Emissive.
  - **Blue Channel**: Roughness.
- **Normalization**: Normalize the input and output images to ensure consistency in the pixel values.
