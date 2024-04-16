# BYOC
## External libraries in Relay
* External libraries such as cuBLAS, cuDNN, MIOpen, and rocBLAS can be configured in the Relay target
* <code>lib = relay.build_module.build(net, target, params=params)</code>
* To use cuBLAS, set <code>target = "cuda -libs=cublas"</code>
  * Fully connected layer is replaced
* To use cuDNN and cuBLAS, set <code>target = "cuda -libs=cudnn, cublas"</code>
  * Convolution is replaced
* To use MIOpen and rocBLAS, set <code>target = "rocm -libs=miopen, rocblas"</code>
* The usage of external libraries restrains operator fusion
* An external library has its own restrictions, such as data type and layout 
* Ref: https://tvm.apache.org/docs/how_to/work_with_relay/using_external_lib.html
