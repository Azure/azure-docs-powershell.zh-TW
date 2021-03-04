---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D2B5BC27-6D51-45BC-AE6A-F7FED11B8651
online version: https://docs.microsoft.com/powershell/module/az.compute/save-azvmimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Save-AzVMImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Save-AzVMImage.md
ms.openlocfilehash: d979e89583b19270dfd13bae85a3afe1505ed55e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913969"
---
# Save-AzVMImage

## 簡介
將虛擬機器存成 VMImage。

## 語法

### ResourceGroupNameParameterSetName (預設) 
```
Save-AzVMImage [-Name] <String> [-DestinationContainerName] <String> [-VHDNamePrefix] <String> [-Overwrite]
 [[-Path] <String>] [-ResourceGroupName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### IdParameterSetName
```
Save-AzVMImage [-DestinationContainerName] <String> [-VHDNamePrefix] <String> [-Overwrite] [[-Path] <String>]
 [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 描述
**Save-Az VMImage Cmdlet** 會將虛擬機器儲存為 VMImage。
建立虛擬機器映射之前，請複製虛擬機器，然後使用 Cmdlet 將其Set-AzVM通用。
此 Cmdlet 的輸出是 JSON 範本 (JavaScript) 標記法。
您可以從捕獲的圖像部署虛擬機器。

## 例子

### 範例 1：捕獲虛擬機器
```
PS C:\> Set-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized 
PS C:\> Save-AzVMImage -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -DestinationContainerName "VMContainer01" -VHDNamePrefix "VM07"
```

第一個命令將 VirtualMachine07 的虛擬機器標記為通用。
第二個命令會以 VMImage 來捕獲名為 VirtualMachine07 的虛擬機器。
Output **屬性** 會返回 JSON 範本。

## 參數

### -AsJob
在背景中執行 Cmdlet 並返回工作以追蹤進度。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

### -DestinationContainerName
指定要保存影像之「系統」容器內的容器名稱。
如果容器不存在，會建立您的容器。
虛擬硬碟 (VHDs) 構成此參數指定之容器中的 VMImage。
如果 VHD 分散在多個儲存帳戶中，此 Cmdlet 會在每個儲存帳戶中建立一個具有此名稱的容器。
已儲存圖像的 URL 類似：HTTPs:// \<storageAccountName\> \<imagesContainer\> / \<vhdPrefix-osDisk\> .blob.core.windows.net/system/Microsoft.Compute/Images/ .xxxxxxxx-xxxx-xxxx-xxxxxxxxx.vhd。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Id
指定虛擬機器的資源識別碼。

```yaml
Type: System.String
Parameter Sets: IdParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -名稱
指定名稱。

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases: VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -覆寫
表示此 Cmdlet 會覆寫目的地容器中具有相同首碼的任何 VHD。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -路徑
儲存所捕獲影像範本的檔案路徑。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
指定虛擬機器的資源組名。

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VHDNamePrefix
指定構成 VMImage 儲存設定檔之 Blob 名稱中的首碼。
例如，作業系統磁片的首碼 vhdPrefix 會導致 vhdPrefix-osax 名稱 \<guid\> 。vhd。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: VirtualHardDiskNamePrefix

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。 詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)

## 輸入

### System.String

### System.Management.Automation.SwitchParameter

## 輸出

### Microsoft.Azure.Commands.Compute.models.PSComputeLongRunningOperation

## 筆記

## 相關連結

[Get-AzMSIMage](./Get-AzVMImage.md)

[Get-AzEVImageOffer](./Get-AzVMImageOffer.md)

[Get-AzMSIMagePublisher](./Get-AzVMImagePublisher.md)

[Get-AzKUImageSku](./Get-AzVMImageSku.md)

[Set-AzMS](./Set-AzVM.md)


