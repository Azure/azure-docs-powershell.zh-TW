---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: D2B5BC27-6D51-45BC-AE6A-F7FED11B8651
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Save-AzureRmVMImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Save-AzureRmVMImage.md
ms.openlocfilehash: 8f3aebe1e9e79423d7251fa79084d6fa85407b9d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455484"
---
# Save-AzureRmVMImage

## 摘要
將虛擬機器儲存為 VMImage。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

### ResourceGroupNameParameterSetName (預設) 
```
Save-AzureRmVMImage [-Name] <String> [-DestinationContainerName] <String> [-VHDNamePrefix] <String>
 [-Overwrite] [[-Path] <String>] [-ResourceGroupName] <String> [<CommonParameters>]
```

### IdParameterSetName
```
Save-AzureRmVMImage [-Name] <String> [-DestinationContainerName] <String> [-VHDNamePrefix] <String>
 [-Overwrite] [[-Path] <String>] [-Id] <String> [<CommonParameters>]
```

## 說明
AzureRmVMImage Cmdlet 會將虛擬機器 **儲存** 為 VMImage。
在您建立虛擬機器影像之前，請 sysprep 虛擬機器，然後使用 Set-AzureRmVM Cmdlet 將它標示為一般化。

這個 Cmdlet 的輸出是 (JSON) 範本的 JavaScript 物件符號。
您可以從捕獲的映射部署虛擬機器。

## 示例

### 範例1：捕獲虛擬機器
```
PS C:\> Set-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized 
PS C:\> Save-AzureRmVMImage -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -DestinationContainerName "VMContainer01" -VHDNamePrefix "VM07"
```

第一個命令會將名為 VirtualMachine07 的虛擬機器標示為「一般化」。

第二個命令會將名為 VirtualMachine07 的虛擬機器捕獲為 VMImage。
**Output** 屬性會傳回 JSON 範本。

## 參數

### -DestinationContainerName
指定您想要保留影像之「系統」容器內的容器名稱。

如果容器不存在，就會為您建立。
組成 VMImage 的虛擬硬碟 (Vhd) 會駐留在此參數指定的容器中。
如果 Vhd 分佈在多個儲存空間帳戶中，這個 Cmdlet 會在每個儲存空間帳戶中建立一個具有此名稱的容器。
所儲存影像的 URL 類似以下所示： 

\<storageAccountName\>blob.core.windows.net/system/Microsoft.Compute/Images/ \<imagesContainer\> / \<vhdPrefix-osDisk\> xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -識別碼
指定虛擬機器的資源識別碼。

```yaml
Type: String
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
Type: String
Parameter Sets: (All)
Aliases: VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Overwrite
表示此 Cmdlet 會覆寫目的地容器中具有相同前置詞的任何 Vhd。

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Path
指定 VHD 的路徑。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
指定虛擬機器之資源群組的名稱。

```yaml
Type: String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VHDNamePrefix
在組成 VMImage 儲存設定檔的 blob 名稱中，指定前置詞。

例如，作業系統磁片的首碼 vhdPrefix 會產生 name vhdPrefix- \<guid\> osdisk .。。vhd.

```yaml
Type: String
Parameter Sets: (All)
Aliases: VirtualHardDiskNamePrefix

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### 所有
這個 Cmdlet 不接受任何輸入。

## 輸出

## 筆記

## 相關連結

[AzureRmVMImage](./Get-AzureRmVMImage.md)

[AzureRmVMImageOffer](./Get-AzureRmVMImageOffer.md)

[AzureRmVMImagePublisher](./Get-AzureRmVMImagePublisher.md)

[AzureRmVMImageSku](./Get-AzureRmVMImageSku.md)

[Set-AzureRmVM](./Set-AzureRmVM.md)


