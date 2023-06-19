# JPEG Image Compression

This repository contains code for JPEG image compression implemented in Python using the OpenCV library. The code includes encoding and decoding processes to compress and decompress an image, respectively.

## Requirements
- Python 3.x
- OpenCV
- NumPy
- Matplotlib

## Usage

1. Ensure that you have the required dependencies installed.
2. Place the image file (`city.jpg`) in the same directory as the notebook.
3. Run the notebook to perform the encoding and decoding processes.
4. The encoded data will be saved as `output_jpeg_encoded.npy`.
5. The decoded image will be saved as `compressed_image.jpg`.
6. The original and compressed images will be displayed side by side, along with the RMSE, PSNR, and compression ratio.

## Results
The encoding process quantizes the image using a predefined quantization matrix and performs discrete cosine transform (DCT) on the quantized coefficients. These coefficients are then serialized and saved as `output_jpeg_encoded.npy`.

The decoding process reads the serialized data from `output_jpeg_encoded.npy` and performs inverse DCT and dequantization to obtain the decompressed image, which is saved as `compressed_image.jpg`. The RMSE, PSNR, and compression ratio between the original and compressed images are also calculated and displayed.

## Notes
- The code assumes that the input image is in the RGB color space. If the image is in a different color space, modification to the code may be required.
- The code uses predefined quantization matrices for luminance (Y) and chrominance (U and V) channels. These matrices can be customized according to specific requirements.
- The code saves the compressed image as JPEG format (`compressed_image.jpg`). However, the image quality may vary depending on the desired compression ratio and the input image characteristics.
