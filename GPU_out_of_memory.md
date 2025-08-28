If face any of the below error

**RuntimeError: NVML_SUCCESS == r INTERNAL ASSERT FAILED at "/opt/pytorch/pytorch/c10/cuda/CUDACachingAllocator.cpp":995, please report a bug to PyTorch**
<img width="1118" height="188" alt="image" src="https://github.com/user-attachments/assets/bf696c39-19a2-4502-a13d-9744abc57c73" />

**Or GPU out of memory**
Run nvidia-smi in terminal or !nvidia-smi in jupyter cell and make sure your gpu memory is almost full 
<img width="653" height="458" alt="Screenshot 2025-08-28 163010" src="https://github.com/user-attachments/assets/be392dd7-a509-4ec8-be5d-7e52b8fc8338" />

If above is the case then 

**Solutions**

1) Empty cuda reseve/buffer memory
   
import torch
torch.cuda.empty_cache()  

3) Do nvidia-smi and check buffer memory again
4) still its not reducing, then disconnect kernel from left top

**Allocate memory so that GPU can't use all GPU memory**

import torch

this allow this process to use only 50% of GPU memory

torch.cuda.set_per_process_memory_fraction(0.5, device=0)

**Follow a/c for tensorflow
https://www.tensorflow.org/api_docs/python/tf/config/experimental/set_memory_growth
