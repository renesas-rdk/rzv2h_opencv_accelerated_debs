

# rzv2h_opencv_accelerated_debs

Prebuilt OpenCV 4.6.0 `.deb` packages with **Renesas DRP hardware acceleration** for **RZ/V2H** on Ubuntu 24.04 (Noble) ARM64.

These packages are built from the [official Ubuntu OpenCV source package](https://launchpad.net/ubuntu/+source/opencv/4.6.0+dfsg-13.1ubuntu1) with DRP acceleration patches from [renesas-rz/rzv2h_opencv_accelerator](https://github.com/renesas-rz/rzv2h_opencv_accelerator).

## Supported Platform

| Item              | Detail                                     |
| :---------------- | :----------------------------------------- |
| **SoC**           | Renesas RZ/V2H (R9A09G057)                |
| **OS**            | Ubuntu 24.04 Noble Numbat                  |
| **Arch**          | ARM64 (aarch64)                            |
| **OpenCV**        | 4.6.0                                      |
| **Acceleration**  | DRP (Dynamically Reconfigurable Processor) |

## Quick Install

```bash
wget -qO install_opencv_arm64.sh https://raw.githubusercontent.com/renesas-rdk/rzv2h_opencv_accelerated_debs/main/install_opencv_arm64.sh
sudo bash install_opencv_arm64.sh
```

## DRP-Accelerated Functions

The following table lists the OpenCV functions that can be executed using DRP in the OpenCVA.

| OpenCV Function     | Description                                                              |
| :------------------ | :----------------------------------------------------------------------- |
| resize              | Image Resize                                                             |
| cvtColor            | Change color space                                                       |
| cvtColorTwoPlane    | Change color space                                                       |
| GaussianBlur        | Gaussian filter process                                                  |
| dilate              | Areas of bright regions grow                                             |
| erode               | Areas of dark regions grow                                               |
| morphologyEx        | Combination of dilate and erode                                          |
| filter2D            | Image convolving                                                         |
| Sobel               | Extracting image edges                                                   |
| adaptiveThreshold   | Transforms a grayscale image to a binary image                           |
| matchTemplate       | Compares a template against overlapped image regions                     |
| warpAffine          | Transforms the source image using the 2x3 matrix                         |
| warpPerspective     | Transforms the source image using the 3x3 matrix                         |
| pyrDown             | Downsampling step of the Gaussian pyramid construction                   |
| pyrUp               | Upsampling step of the Gaussian pyramid construction                     |
| FAST                | Detects corners using the FAST algorithm                                 |
| remap               | Applies a generic geometrical transformation to an image                 |
| StereoSGBM          | Creates StereoSGBM object for the modified H. Hirschmuller algorithm     |

> For full details, see [rzv2h_opencv_accelerator](https://github.com/renesas-rz/rzv2h_opencv_accelerator/blob/main/README.md).

## Build Info

| Item              | Value                                                                                          |
| :---------------- | :--------------------------------------------------------------------------------------------- |
| **Base**          | Ubuntu source `opencv 4.6.0+dfsg-13.1ubuntu1`                                                 |
| **DRP patches**   | [rzv2h_opencv_accelerator](https://github.com/renesas-rz/rzv2h_opencv_accelerator)            |
| **Version**       | `4.6.0+dfsg-99v2hcva1~13.1ubuntu1`                                                            |
| **Build**         | Cross-compiled for ARM64                                                                       |

## License

| Software              | License                                                                                                          |
| :-------------------- | :--------------------------------------------------------------------------------------------------------------- |
| **OpenCV**            | [Apache License 2.0](https://opensource.org/licenses/Apache-2.0)                                                 |
| **OpenCV Accelerator**| [3-clause BSD](licenses/opencva/LICENSE)                                                                         |
| **DRP Driver**        | [GPL-2.0](licenses/drp-driver/LICENSE)                                                                           |

## References

- [renesas-rz/rzv2h_opencv_accelerator](https://github.com/renesas-rz/rzv2h_opencv_accelerator) — DRP acceleration patches
- [Renesas RZ/V2H](https://www.renesas.com/en/products/rz-v2h?srsltid=AfmBOorWalMi11eOzXWACc069wvNA3dMnn7ykKPNNYO2RGj00tFfOWVd) — Product page
- [OpenCV 4.6.0 Documentation](https://docs.opencv.org/4.6.0/)