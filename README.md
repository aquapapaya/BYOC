# BYOC
## External libraries in Relay
* External libraries such as cuBLAS, cuDNN, MIOpen, and rocBLAS can be configured in the Relay target.
  * <code>lib = relay.build_module.build(net, target, params=params)</code>
## Ref
* https://tvm.apache.org/docs/how_to/work_with_relay/using_external_lib.html
