# Vitis-XGpioPs_CfgInitialize
## 定义
这是一个 Xilinx 提供的 API 函数，用于初始化一个 `XGpioPs` 实例（PS GPIO 控制器）。该函数会将 GPIO 控制器与硬件配置绑定，设置好所需的寄存器和地址。函数的原型通常是这样的：
`s32 XGpioPs_CfgInitialize(XGpioPs *InstancePtr, const XGpioPs_Config *ConfigPtr , u32 EffectiveAddr){...}`

1.`XGpioPs *InstancePtr`：这是一个指向 `XGpioPs` 类型实例的指针。
2.`const XGpioPs_Config *ConfigPtr`：这是一个指向 `XGpioPs_Config` 类型的常量指针。
3.`u32 EffectiveAddr`：这是 GPIO 控制器的基地址，用于访问硬件寄存器,是一个32位无符号整数。基地址通常来自 `XGpioPs_Config` 结构体中的`BaseAddr` 字段。

这个函数的返回类型是一个32位带符号整数。如果初始化成功，返回`XST_SUCCESS`（通常是0）。如果初始化失败，返回错误代码。
