---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 23DB0AD2-7EB7-4373-BB8D-BB6CB651DD54
online version: https://docs.microsoft.com/powershell/module/az.resources/new-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTag.md
ms.openlocfilehash: b5f80abac4c114ab60dcb130f229265c4aafd78f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906869"
---
# New-AzTag

## 簡介
建立預先定義的 Azure 標記，或將值加到現有的標記|在資源或訂閱上建立或更新整組標記。

## 語法

### CreatePredefinedTagParameterSet

```powershell
New-AzTag [-Name] <String> [[-Value] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### CreateByResourceIdParameterSet

```powershell
New-AzTag
   -ResourceId <String>
   -Tag <Hashtable>
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

## 描述

**CreatePredefinedTagSet：New-AzTag** Cmdlet 會建立預先定義的 Azure 標籤，以及選擇性的預先定義值。 
您也可以使用它，將其他值新增到現有的預先定義標記。
若要建立預先定義的標記，請輸入唯一的標記名稱。
若要新增值至現有的預先定義標記，請指定現有標記的名稱及新值。
此 Cmdlet 會以其值及已使用的資源數目，來代表新的或修改過標記的物件。
**New-AzTag** 屬於 Azure 標記模組的一部分，可協助管理預先定義的 Azure 標記。
Azure 標記是一組名稱值，可用於將 Azure 資源和資源群組分類，例如按部門或成本中心分類，或追蹤資源與群組的附注或批註。
您可以在單一步驟中定義並應用標記，但預先定義的標記讓您為訂閱中的標記建立標準、一致、可預測的名稱和值。
若要將預先定義的標籤適用于資源或資源群組，請使用Cmdlet New-AzTag標記參數。
若要搜尋具有指定標籤名稱或名稱和值的資源群組，請使用 Get-AzResourceGroup  Cmdlet 的 Tag 參數。
每個標記都有一個名稱。
這些值為選擇性。
預先定義的 Azure 標記可以有多個值，但當您將標記適用于資源或資源群組時，您只會將標記名稱及其中一個值進行設定。
例如，您可以針對每個部門建立預先定義的部門標記，例如財務、人力資源和 IT。
當您將部門標記適用于資源時，您只會使用一個預先定義的值，例如財務。

**CreateByResourceIdParameterSet：****具有 ResourceId** 的 **New-AzTag** Cmdlet 會建立或更新資源或訂閱上的整組標籤。
這項作業允許在指定的資源或訂閱上新增或取代整組標記。 指定實體最多可以有 50 個標記。

## 例子

### 範例 1：建立預先定義的標記
```powershell
PS C:\>New-AzTag -Name "FY2015"
                                
Name   ValuesTable Count Values 
----   ----------- ----- ------
FY2015             0     {}
```

此命令會建立名為 FY2015 的預先定義標記。
此標記沒有值。
您可以將沒有值的標記適用于資源或資源群組，或使用 **New-AzTag** 在標記中新增值。
您也可以在將標記適用于資源或資源群組時指定值。

### 範例 2：使用值建立預先定義的標記
```powershell
PS C:\>New-AzTag -Name "Department" -Value "Finance"
Name:   Department
Count:  0
Values: 

        Name        Count
        =========   =====
        Finance     0
```

此命令會建立名為 Department 的預先定義標記，並包含財務值。

### 範例 3：在預先定義的標記中新增值
```powershell
PS C:\>New-AzTag -Name "Department" -Value "Finance"
Name:   Department
Count:  0
Values: 
        Name        Count
        =========   =====
        Finance     0 
PS C:\>New-AzTag -Name "Department" -Value "IT"
Name:   Department
Count:  0
Values: 
        Name        Count
        =========   =====
        Finance     0
        IT          0
```

這些命令會建立一個名為 Department 的預先定義標記，並包含兩個值。
如果標記名稱存在 **，New-AzTag** 會新增值至現有標記，而不是建立新標記。

### 範例 4：使用預先定義的標記
```powershell
PS C:\>New-AzTag -Name "CostCenter" -Value "0001"
Name:   CostCenter
Count:  0
Values: 
        Name        Count
        =========   =====
        0001        0 
PS C:\>Set-AzResourceGroup -Name "EngineerBlog" -Tag @{Name="CostCenter";Value="0001"}
Name:      EngineerBlog
Location:  East US
Resources: 
            
  Name             Type                     Location
    ===============  =======================  ========
    EngineerBlog     Microsoft.Web/sites      West US
    EngSvr01         Microsoft.Sql/servers    West US
    EngDB02          Microsoft.Sql/databases  West US
Tags: 
    Name         Value
    ==========   =====
    CostCenter   0001 
PS C:\>Get-AzTag -Name "CostCenter"
Name:   CostCenter
Count:  1
Values: 
        Name        Count
        =========   =====
        0001        1 
PS C:\>Get-AzResourceGroup -Tag @{Name="CostCenter"}
Name:      EngineerBlog
Location:  East US
Resources: 
     Name             Type                     Location
    ===============  =======================  ========
    EngineerBlog     Microsoft.Web/sites      West US

    EngSvr01         Microsoft.Sql/servers    West US
    EngDB02          Microsoft.Sql/databases  West US
Tags: 
    Name         Value
    ==========   =====
    CostCenter   0001
```

此範例中的命令會建立並使用預先定義的標記。

### 範例 5：在訂閱上建立或更新整組標記

```powershell
PS C:\>$Tags = @{"tagKey1"="tagValue1"; "tagKey2"="tagValue2"}
PS C:\>New-AzTag -ResourceId /subscriptions/{subId} -Tag $Tags

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             tagKey1  tagValue1
             tagKey2  tagValue2
```

此命令會使用 {subId} 建立或更新訂閱上的整組標記。

### 範例 6：建立或更新資源上的整組標記

```powershell
PS C:\>$Tags = @{"Dept"="Finance"; "Status"="Normal"}
PS C:\>New-AzTag -ResourceId /subscriptions/{subId}/resourcegroups/{rg}/providers/Microsoft.Sql/servers/Server1 -Tag $Tags

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             Dept     Finance
             Status   Normal
```

此命令會使用 {resourceId} 建立或更新資源上的整組標記。

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

### -名稱
指定預先定義的標記名稱。
若要建立新的預先定義標記，請輸入唯一的名稱。
若要新增值至現有的標記，請輸入現有標記的名稱。
如果現有的預先定義標記有指定的名稱 **，New-AzTag** 會新增指定值至具有該名稱的標記 ，而不是建立新標記。

```yaml
Type: System.String
Parameter Sets: CreatePredefinedTagParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -值
指定預先定義的標記值。
預先定義的標記可以有多個值，但您可以在每個命令中只輸入一個值。
此參數為選擇性，因為標記的名稱可以沒有值。

```yaml
Type: System.String
Parameter Sets: CreatePredefinedTagParameterSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
要標記之實體的資源識別碼。 系統可能會標記資源、資源群組或訂閱。

```yaml
Type: System.String
Parameter Sets: CreateByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -標記
要放在資源上的標記。

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateByResourceIdParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -確認
執行 Cmdlet 之前，提示您確認。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
顯示 Cmdlet 執行時會發生什麼情況。
不會執行 Cmdlet。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。 詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)

## 輸入

### System.String

### System.Collections.Hashtable

## 輸出

### Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag |Microsoft.Azure.Commands.Tags.Model.PSTagResource

## 筆記

## 相關連結

[Get-AzTag](./Get-AzTag.md)

[Remove-AzTag](./Remove-AzTag.md)

[Update-AzTag](./Update-AzTag.md)