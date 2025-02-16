
# Image Processing with CUDA  

This repository contains high-performance, GPU-accelerated image processing algorithms implemented in CUDA and C++. It demonstrates efficient parallelization techniques, leveraging shared memory and optimized memory access patterns. Implemented filters include image blurring, flipping, and edge detection, running in real-time on NVIDIA GPUs.  

## 🚀 Getting Started  

### Prerequisites  
Ensure your system supports CUDA and has the necessary drivers installed. Learn more about CUDA [here](https://developer.nvidia.com/about-cuda).  

### Compilation  
Before running the filters, compile the `main.cu` file using:  
```bash
nvcc main.cu -o image_processor
```

### Running Filters  
To apply a filter, use:  
```bash
./image_processor <input_image> <output_image> <filter_arg>
```  
Example:  
```bash
./image_processor images/lena_rgb.png output/lena_blur.png blur
```

Alternatively, batch processing can be executed using:  
```bash
sbatch runs/filter_run
```  

### Available Filters  
| Filter          | Argument  |
|----------------|----------|
| Horizontal Flip | `hflip`  |
| Vertical Flip   | `vflip`  |
| Sharpening      | `sharpen` |
| Blurring        | `blur`   |

## 🧪 Running Tests  

Execute test cases with:  
```bash
chmod u+x ex_single.sh && ./ex_single.sh
chmod u+x ex_batch.sh && ./ex_batch.sh
```  
- **Single Image Mode:** Runs all filters on `images/lena_rgb.png` and saves outputs in `output/`.  
- **Batch Mode:** Processes multiple copies of `lena_rgb.png` using the edge detection filter for performance evaluation.  

## 📁 Repository Structure  

- **`main.cu`** – Parses arguments and executes filters.  
- **`stb_image/`** – Image handling library.  
- **`image.h`** – Wrapper for image operations.  
- **`filters/`** – CUDA-accelerated filter implementations.  
- **`expected_output/`** – Reference images for validation.  
- **`images/`** – Sample input images.  

This project highlights expertise in **GPU programming, CUDA optimization, and parallel processing**, ensuring high-performance execution of image processing tasks. 🚀  
