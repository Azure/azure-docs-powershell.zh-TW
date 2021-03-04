---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 4E5C059B-36F3-41C8-9FDB-69F5318CF39B
online version: https://docs.microsoft.com/powershell/module/az.resources/set-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResourceGroup.md
ms.openlocfilehash: f344c3cd08fb717d1229fb0abb4386c8a2d39d5f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913334"
---
# Set-AzResourceGroup

## 簡介
修改資源群組。

## 語法

### SetByResourceGroupName (預設) 
```
Set-AzResourceGroup -Name <String> [-Tag] <Hashtable> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SetByResourceGroupId
```
Set-AzResourceGroup [-Tag] <Hashtable> -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 描述
**Set-AzResourceGroup** Cmdlet 會修改資源群組的屬性。
您可以使用此 Cmdlet 來新增、變更或刪除已適用于資源群組的 Azure 標籤。
指定 *名稱* 參數以識別資源群組，並指定 *Tag* 參數來修改標記。
您無法使用此 Cmdlet 變更資源組的名稱。

## 例子

### 範例 1：將標記適用于資源群組
```
PS C:\>Set-AzResourceGroup -Name "ContosoRG" -Tag @{Department="IT"}
```

此命令會將具有 IT 值的部門標記，適用于沒有現有標記的資源群組。

### 範例 2：新增標記至資源群組
```
PS C:\>$Tags = (Get-AzResourceGroup -Name "ContosoRG").Tags
PS C:\> $Tags
PS C:\> $Tags += @{"Status"="Approved"; "FY2016"=$null}
PS C:\> Set-AzResourceGroup -Name "ContosoRG" -Tag $Tags
PS C:> (Get-AzResourceGroup -Name "ContosoRG").Tags
```

此範例會將具有已核准值的狀態標記和 FY2016 標記新增到具有現有標記的資源群組。 由於您指定的標記會取代現有的標記，因此您必須將現有的標記納入新標記集合中，否則將會失去這些標記。
第一個命令會取得 ContosoRG 資源群組，並使用點方法取得其 Tags 屬性的值。 該命令會儲存變數中的$Tags標記。
第二個命令會獲得該變數$Tags標記。
第三個命令使用 += 工作分派運算子，將狀態和 FY2016 標記新加到變數中的$Tags陣列。
第四個命令使用 **Set-AzResourceGroup** 的 *Tag* 參數，將 $Tags 變數中的標籤套用至 ContosoRG 資源群組。
第五個命令會套用至 ContosoRG 資源群組的所有標籤。 輸出顯示資源群組有部門標記和兩個新標記：狀態和 FY2015。

### 範例 3：刪除資源群組的所有標記
```
PS C:\>Set-AzResourceGroup -Name "ContosoRG" -Tag @{}
```

此命令會指定具有空白雜湊表格值的 *Tag* 參數，以刪除 ContosoRG 資源群組的所有標籤。

## 參數

### -ApiVersion
指定資源提供者支援的 API 版本。
您可以指定與預設版本不同的版本。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
用於與 Azure 通訊的認證、帳戶、租使用者和訂閱

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

### -Id
指定要修改的資源群組識別碼。

```yaml
Type: System.String
Parameter Sets: SetByResourceGroupId
Aliases: ResourceGroupId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -名稱
指定要修改的資源組名。

```yaml
Type: System.String
Parameter Sets: SetByResourceGroupName
Aliases: ResourceGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Pre
表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮測試版 API 版本。

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

### -標記
以雜湊表格形式建立索引鍵值組。 例如：@{key0="value0";key1=$null;key2="value2"} 標記是一組名稱值，您可以建立並適用于資源和資源群組。 將標記指派給資源和群組後，您可以使用 Get-AzResource 和Get-AzResourceGroup 標記參數，根據標記名稱或名稱和值來搜尋資源和群組。 您可以使用標記來分類資源，例如按照部門或成本中心，或追蹤資源的附注或批註。
若要新增或變更標記，您必須取代資源群組的標記集合。 若要刪除標記，請從 **Get-AzResourceGroup** 輸入包含目前所有已適用于資源群組之標記的雜湊表格，但您想要刪除的標記除外。 若要刪除資源群組的所有標記，請指定空白雜湊表 `@{}` ：。

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。 詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)

## 輸入

### System.String

### System.Collections.Hashtable

## 輸出

### Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroup

## 筆記

## 相關連結

[Get-AzResource](./Get-AzResource.md)

[Get-AzResourceGroup](./Get-AzResourceGroup.md)

[New-AzResourceGroup](./New-AzResourceGroup.md)

[Remove-AzResourceGroup](./Remove-AzResourceGroup.md)
