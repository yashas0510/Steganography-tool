# Image Steganography Tool

## Description

This project is a Python-based tool for hiding secret messages within image files using steganography techniques. The tool utilizes the Least Significant Bit (LSB) method to embed messages into the pixel data of images, allowing users to encode and decode messages seamlessly.

### Features

- Encode secret messages into PNG or JPEG images.
- Decode hidden messages from encoded images.
- User-friendly command-line interface.
- Supports termination character to indicate the end of the message.

## Requirements

- Python 3.x
- Pillow library for image processing

## Installation

1. **Clone the Repository**:
git clone https://github.com/yourusername/steganography-tool.git
cd steganography-tool
text

2. **Install Pillow**:
Ensure you have `pip` installed, then run:
pip install Pillow
text

## Usage

1. **Run the Tool**:
Execute the script in your terminal:
python steganography.py
text

2. **Choose an Operation**:
- When prompted, choose whether to encode or decode a message.

3. **Encoding a Message**:
- Input the name of the image file you want to use (e.g., `input_image.png`).
- Enter the secret message you wish to hide.
- Specify the name for the output encoded image (e.g., `output_image.png`).

4. **Decoding a Message**:
- Input the name of the encoded image file (e.g., `output_image.png`).
- The tool will display the decoded hidden message.

### Example

To encode a message:
Do you want to (e)ncode or (d)ecode? (e/d): e
Enter the name of the input image (e.g., input_image.png): input_image.png
Enter the secret message you want to hide: Hello World!
Enter the name for the output encoded image (e.g., output_image.png): output_image.png
Data encoded successfully into output_image.png
text

To decode a message:
Do you want to (e)ncode or (d)ecode? (e/d): d
Enter the name of the encoded image (e.g., output_image.png): output_image.png
Decoded message: Hello World!
text

## Code Explanation

### Functions

- **`gen_data(data)`**: Converts the input string into binary format and appends a null character (`'\0'`) to indicate the end of the message.

- **`mod_pix(pix, data, img_width, img_height)`**: Modifies the pixel values in an image according to the binary representation of the secret message.

- **`encode_image(image_path, secret_data, output_path)`**: Opens an image file, modifies its pixels to embed the secret message, and saves it as a new file.

- **`decode_image(image_path)`**: Reads an encoded image and reconstructs the hidden message from its pixel data.

### Main Loop

The script continuously prompts users to either encode or decode messages until they choose to exit.

## Contributing

Contributions are welcome! If you'd like to contribute to this project, please fork the repository and submit a pull request with your changes.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- [Pillow Documentation](https://pillow.readthedocs.io/en/stable/)
