# 体验Flutter

[https://flutterchina.club/get-started/test-drive/#androidsstudio](https://flutterchina.club/get-started/test-drive/#androidsstudio)



> 名词解释:
>
> VT-x: 虚拟化技术( Virtualization Technology)

在Android Studio 中创建新应用时, 运行时需要创建一个虚拟机设备, 创建时, 提示如下:

![1557890055482](E:\workspace\flutter-docs\安装和起步\assets\1557890055482.png)

``VT-x is disabled in BIOS` , 点击提示下的 `Troubleshoot` 是弹出以下错误提示: `Enable VT-x in your BIOS security settings (refer to documentation for your computer)`



在选择该虚拟机时, 编辑器给出如下报错:

emulator: ERROR: x86 emulation currently requires hardware acceleration! Please ensure Windows Hypervisor Platform (WHPX) is properly installed and usable. CPU acceleration status: VT feature disabled in BIOS/UEFI More info on configuring VM acceleration on Windows: https://developer.android.google.cn/studio/run/emulator-acceleration#vm-windows  If you are using an Intel CPU: please check that virtualization is enabled in the BIOS and that HAXM is installed and usable. Note: if Hyper-V or Credential Guard is enabled, the emulator will not work with HAXM. See https://github.com/intel/haxm/issues/105#issuecomment-470927735 for info on how to disable Credential Guard. If you are using an AMD CPU or need to run alongside Hyper-V-based apps such as Docker, we recommend using Windows Hypervisor Platform.General information on acceleration: https://developer.android.google.cn/studio/run/emulator-acceleration.

模拟器：错误：x86仿真目前需要硬件加速！ 请确保Windows Hypervisor Platform（WHPX）已正确安装和使用。 CPU加速状态：BIOS / UEFI中禁用VT功能有关在Windows上配置VM加速的更多信息： https：//developer.android.google.cn/studio/run/emulator-acceleration#vm-windows 如果您使用的是Intel CPU ：请检查BIOS中是否已启用虚拟化，并且HAXM已安装且可用。 注意：如果启用了Hyper-V或Credential Guard，则模拟器将无法与HAXM一起使用。 有关如何禁用Credential Guard的信息，请参阅https://github.com/intel/haxm/issues/105#issuecomment-470927735。 如果您使用的是AMD CPU或需要与基于Hyper-V的应用程序（如Docker）一起运行，我们建议您使用Windows Hypervisor Platform。有关加速的一般信息：https：//developer.android.google.cn/studio/run/仿真器加速。

解决办法:

- 重启电脑
- 进入 `BIOS` (不同电脑进入方式不同, F1 / F10 etc)
- 左右方向键(或者 `Tab键` ) 进入 `Security` 选项卡
- 选择 `Virtualization`
- 将选项 `Intel virtualization Technology` 设置为 `Enable`
- `F10` 保存并退出
- 重新启动 Flutter 项目即可



修改完上述配置后, 选择虚拟机可以启动一个安卓模拟器



