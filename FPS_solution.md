# 更改远程会话中的帧速率限制

远程会话中的实际帧速率取决于其他因素，如应用程序和计算机硬件资源。 此外，并非所有远程显示协议都支持大于 30 FPS 的帧速率。 例如，远程桌面协议 (RDP) 将帧速率限制为 30 FPS。若要解决此问题，在注册表子项中创建一个 DWMFRAMEINTERVAL 条目，以更改远程会话主机上的最大帧 HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Terminal Server\WinStations 速率限制。 为此，请按照下列步骤操作：

1. 启动注册表编辑器。
2. 找到并单击下面的注册表子项：
3. HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Terminal Server\WinStations
4. 在" 编辑 "菜单上，单击 " 新建"，然后单击 DWORD (32 位) 值。
5. 键入 DWMFRAMEINTERVAL， 然后按 Enter。
6. 右键单击 DWMFRAMEINTERVAL， 单击"修改"。
7. 单击 "十 进制"，在"值 "数据 框中键入 15，然后单击"确定"。 这会将 FPS 的最大帧速率 (60 帧) 。
