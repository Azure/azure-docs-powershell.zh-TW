---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 4E5C059B-36F3-41C8-9FDB-69F5318CF39B
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResourceGroup.md
ms.openlocfilehash: 0523041357becb38475bb496c94ba1fd48c5acaf
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98280476"
---
# Set-AzResourceGroup

## 摘要
修改資源群組。

## 句法

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

## 說明
**AzResourceGroup** Cmdlet 會修改資源群組的屬性。
您可以使用此 Cmdlet 來新增、變更或刪除套用至資源群組的 Azure 標記。
指定 *Name* 參數來識別 [資源] 群組，以及要修改標籤的 *標記* 參數。
您無法使用這個 Cmdlet 來變更資源群組的名稱。

## 示例

### 範例1：將標籤套用至資源群組
```
PS C:\>Set-AzResourceGroup -Name "ContosoRG" -Tag @{Department="IT"}
```

這個命令會將部門標籤的值套用至沒有現有標籤的資源群組。

### 範例2：新增標籤至資源群組
```
PS C:\>$Tags = (Get-AzResourceGroup -Name "ContosoRG").Tags
PS C:\> $Tags
PS C:\> $Tags += @{"Status"="Approved"; "FY2016"=$null}
PS C:\> Set-AzResourceGroup -Name "ContosoRG" -Tag $Tags
PS C:> (Get-AzResourceGroup -Name "ContosoRG").Tags
```

這個範例會將狀態標記加上已核准的值，並將 [FY2016] 標籤新增至含有現有標記的資源群組中。 因為您指定的標記會取代現有的標記，所以您必須將現有的標記包含在新的標記集合中，否則您就會遺失它們。
第一個命令會取得 ContosoRG 資源群組，並使用點方法來取得其 Tags 屬性的值。 該命令會將標記儲存在 $Tags 變數中。
第二個命令會取得 $Tags 變數中的標記。
第三個命令使用 + = 指派運算子，將 Status 及 FY2016 標籤新增至 $Tags 變數中的標記陣列。
第四個命令使用 **AzResourceGroup 設定** 的 *Tag* 參數，將 $Tags 變數中的標籤套用至 ContosoRG 資源群組。
第五個命令會取得套用至 ContosoRG 資源群組的所有標記。 [輸出] 會顯示 [資源] 群組具有 [部門] 標記，以及兩個新的標籤： [狀態] 和 [FY2015]。

### 範例3：刪除資源群組的所有標籤
```
PS C:\>Set-AzResourceGroup -Name "ContosoRG" -Tag @{}
```

這個命令會將 *Tag* 參數指定為空白的雜湊資料表值，以刪除 ContosoRG 資源群組中的所有標記。

## 參數

### -ApiVersion
指定資源提供者支援的 API 版本。
您可以指定不同于預設版本的版本。

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
用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱

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

### -識別碼
指定要修改之資源群組的識別碼。

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
指定要修改之資源群組的名稱。

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

### -預先
表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。

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

### -Tag
雜湊資料表形式的索引鍵/值對。 例如： @ {key0 = "value0"; key1 = $null; key2 = "value2"} 標記是您可以建立並套用至資源和資源群組的名稱值對。 在您指派標籤至資源和群組之後，您可以使用 Get-AzResource 和 Get-AzResourceGroup 的 *tag* 參數，依標記名稱或名稱和值來搜尋資源和群組。 您可以使用標籤將資源分類（例如 [部門] 或 [成本中心]），或追蹤資源的備忘稿或意見。
若要新增或變更標記，您必須取代資源群組的標記集合。 若要刪除標籤，請輸入目前已套用至資源群組的所有標籤的雜湊資料表（從 **AzResourceGroup**，除了您要刪除的標記之外）。 若要刪除資源群組中的所有標記，請指定空的雜湊資料表： `@{}` 。

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
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。

## 輸入

### System.object

### [System.object] 集合. Hashtable

## 輸出

### PSResourceGroup 中的 SdkModels （）

## 筆記

## 相關連結

[AzResource](./Get-AzResource.md)

[AzResourceGroup](./Get-AzResourceGroup.md)

[新-AzResourceGroup](./New-AzResourceGroup.md)

[移除-AzResourceGroup](./Remove-AzResourceGroup.md)
