---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 63D48BA4-EE80-4740-90B9-0EE05B3F6536
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVmssVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVmssVM.md
ms.openlocfilehash: fcde9de2862590cbf05d680c130bbf7b7f3070d9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445104"
---
# Get-AzureRmVmssVM

## 摘要
取得 VMSS 虛擬機器的屬性。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

### DefaultParameter (預設) 
```
Get-AzureRmVmssVM [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [[-InstanceId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### FriendMethod
```
Get-AzureRmVmssVM [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [[-InstanceId] <String>]
 [-InstanceView] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**AzureRmVmssVM** Cmdlet 會取得虛擬機器規模集的模型視圖和實例視圖， (VMSS) 虛擬機器。
模型視圖是使用者指定的虛擬機器屬性。
[實例] 視圖是虛擬機器的實例層級狀態。
指定 *Status* 參數，只取得虛擬機器的 [實例] 視圖。

## 示例

### 範例1：取得 VMSS 虛擬機器的屬性
```
PS C:\> Get-AzureRmVmssVM -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

這個命令會取得名為 VMSS001 的 VMSS 虛擬電腦的屬性，該虛擬機器屬於名為 Group001 的資源群組。
由於命令不會指定 *InstanceView* 切換參數，因此 Cmdlet 會取得虛擬機器的模型視圖。

### 範例2：取得 VMSS 虛擬機器的模型視圖屬性
```
PS C:\> Get-AzureRmVmssVM -ResourceGroupName "Group002" -VMScaleSetName "VMSS004" -InstanceId $ID
```

這個命令會取得名為 VMSS004 的 VMSS 虛擬電腦的屬性，該虛擬機器屬於名為 Group002 的資源群組。
命令會取得儲存在變數 $ID 中的實例識別碼，以取得模型視圖。

### 範例3：取得 VMSS 虛擬機器的實例視圖屬性
```
PS C:\> Get-AzureRmVmssVM -InstanceView  -ResourceGroupName $rgname  -VMScaleSetName $vmssName -InstanceId $ID
```

這個命令會取得名為 VMSS004 的 VMSS 虛擬電腦的屬性，該虛擬機器屬於名為 Group002 的資源群組。
由於命令會指定 *InstanceView* 切換參數，因此 Cmdlet 會取得虛擬機器的實例視圖。
命令會取得儲存在變數 $ID 中的實例識別碼，以取得實例視圖。

## 參數

### -DefaultProfile
用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InstanceId
指定要取得模型視圖的實例識別碼。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -InstanceView
表示此 Cmdlet 只會取得虛擬機器的實例視圖。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
指定 VMSS 之資源群組的名稱。

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

### -VMScaleSetName
Species VMSS 的名稱。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

## 輸出

### 這個 Cmdlet 不會產生任何輸出。

## 筆記

## 相關連結

[Set-AzureRmVmssVM](./Set-AzureRmVmssVM.md)

[AzureRmVmss](./Get-AzureRmVmss.md)


