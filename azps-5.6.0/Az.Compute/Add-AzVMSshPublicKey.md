---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 3CE367B1-7685-4046-8E9C-CE680B5AE03F
online version: https://docs.microsoft.com/powershell/module/az.compute/add-azvmsshpublickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMSshPublicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMSshPublicKey.md
ms.openlocfilehash: 4c6d2b3376bb5e92d048db61d68c7cfb1b94ee01
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909201"
---
# Add-AzVMSshPublicKey

## 簡介
在僅建立 VM 時，新增虛擬機器 SSH 的公開金鑰。

## 語法

```
Add-AzVMSshPublicKey [-VM] <PSVirtualMachine> [[-KeyData] <String>] [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 描述
**Add-AzMSshPublicKey Cmdlet** 會新增您可用於在 Secure Shell (SSH) 上連接至 Linux 虛擬機器的公開金鑰。 建立 VM 之後，就無法使用此功能，如果您在建立 VM 後嘗試使用這個命令，而不使用 Update-Az VM，則沒有錯誤;如果您使用 Update-Az VM 命令，則命令會發生錯誤。

## 例子

### 範例 1：新增公開金鑰至虛擬機器
```
PS C:\> $VirtualMachine = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> $VirtualMachine = Add-AzVMSshPublicKey -VM $VirtualMachine -KeyData "MIIDszCCApugAwIBAgIJALBV9YJCF/tAMA0GCSq12Ib3DQEB21QUAMEUxCzAJBgNV" -Path "/home/admin/.ssh/authorized_keys"
```

第一個命令會使用 **Get-Az VIRTUAL** Cmdlet 取得名為 VirtualMachine07 的虛擬機器。
該命令將虛擬機器儲存在 $VirtualMachine 變數中。
第二個命令會將公開金鑰新增到 VirtualMachine07 上 Path 參數指定的位置。

## 參數

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

### -KeyData
指定公用鍵的底數 64 編碼。
您可以使用 SSH 或此參數指定的金鑰來連接到 Linux 虛擬機器。

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

### -路徑
指定檔案的完整路徑，位於此 Cmdlet 儲存 SSH 公開金鑰的虛擬機器上。
如果檔案已存在，此 Cmdlet 會附加該金鑰至檔案。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VM
指定此 Cmdlet 修改的虛擬機器物件。
若要取得虛擬機器物件，請使用[Get-Az%。CMdlet。](./Get-AzVM.md)
您可以使用 [New-AzMSConfig](./New-AzVMConfig.md) Cmdlet 來建立虛擬機器物件。

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

## 輸出

### Microsoft.Azure.Commands.Compute.models.PSVirtualMachine

## 筆記

## 相關連結

[Get-AzMS](./Get-AzVM.md)

[New-AzMSCONFIG](./New-AzVMConfig.md)
