---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 50B64FFE-8277-4DAA-805A-271123B35355
online version: https://docs.microsoft.com/powershell/module/az.compute/add-azvmadditionalunattendcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMAdditionalUnattendContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMAdditionalUnattendContent.md
ms.openlocfilehash: 2ec50d8e0c11143f72e327a7b73784c1a49e926c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912070"
---
# Add-AzVMAdditionalUnattendContent

## 簡介
將資訊新增到自動啟動的 Windows 安裝程式答案檔案。

## 語法

```
Add-AzVMAdditionalUnattendContent [-VM] <PSVirtualMachine> [[-Content] <String>]
 [[-SettingName] <SettingNames>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 描述
**Add-AzCMAdditionalUnattendContent** Cmdlet 會將資訊新增到自動 Windows Setup 答案檔案。
指定此 Cmdlet 新增到檔案的其他基礎 64 編碼 .xml 格式資訊unattend.xml檔案。

## 例子

### 範例 1：新增內容至unattend.xml
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> $Credential = Get-Credential
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine  -Windows -ComputerName "Contoso26" -Credential $Credential
PS C:\> $AucContent = "<UserAccounts><AdministratorPassword><Value>" + "Password" + "</Value><PlainText>true</PlainText></AdministratorPassword></UserAccounts>";
PS C:\> $VirtualMachine = Add-AzVMAdditionalUnattendContent -VM $VirtualMachine -Content $AucContent -SettingName "AutoLogon"
```

第一個命令會獲得名為 ResourceGroup11 的資源群組中名為 AvailabilitySet03 的可用性集，然後將該物件儲存在 $AvailabilitySet 變數中。
第二個命令會建立虛擬機器物件，然後將它儲存在$VirtualMachine變數中。
該命令會為虛擬機器指定名稱和大小。
虛擬機器屬於儲存在 $AvailabilitySet 的可用性集。
第三個命令會使用 Get-Credential Cmdlet 建立認證物件，然後將結果儲存在$Credential變數中。
命令會提示您輸入使用者名稱和密碼。
如需要詳細資訊，請鍵入 `Get-Help Get-Credential` 。
第四個命令使用 **Set-Az VIRTUALOperatingSystem** Cmdlet 來設定儲存在 $VirtualMachine 中的虛擬機器。
第五個命令會指派內容給$AucContent變數。
內容包含密碼。
最後一個命令會將儲存在 $AucContent 中unattend.xml檔案。

## 參數

### -內容
指定以 64 編碼的 XML 格式內容為底數。
此 Cmdlet 會將內容新unattend.xml檔案。
XML 內容必須小於 4 KB，且必須包含此 Cmdlet 所插入之設定或功能的基本元素。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
用於與 azure 通訊的認證、帳戶、租使用者和訂閱。

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SettingName
指定內容所適用的設定名稱。
此參數可接受的值為：
- FirstLogonCommands
- AutoLogon

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.SettingNames]
Parameter Sets: (All)
Aliases:
Accepted values: AutoLogon, FirstLogonCommands

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VM
指定此 Cmdlet 修改的虛擬機器物件。
若要取得虛擬機器物件，請使用[Get-Az%。CMdlet。](./Get-AzVM.md)
使用 [New-AzMSConfig](./New-AzVMConfig.md) Cmdlet 建立虛擬機器物件。

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。 詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)

## 輸入

### Microsoft.Azure.Commands.Compute.models.PSVirtualMachine

### System.String

### System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.SettingNames, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]

## 輸出

### Microsoft.Azure.Commands.Compute.models.PSVirtualMachine

## 筆記

## 相關連結

[Get-AzAvailabilitySet](./Get-AzAvailabilitySet.md)

[Set-AzEVOperatingSystem](./Set-AzVMOperatingSystem.md)

[New-AzMSCONFIG](./New-AzVMConfig.md)
