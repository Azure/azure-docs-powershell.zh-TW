---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/get-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTemplateSpec.md
ms.openlocfilehash: 0b2018eecc081f2fcee5da63ed17cc2e01486777
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903950"
---
# Get-AzTemplateSpec

## 簡介
獲取或列出範本規格

## 語法

### ListTemplateSpecsParameterSet (預設) 
```
Get-AzTemplateSpec [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### GetTemplateSpecByNameParameterSet
```
Get-AzTemplateSpec [-ResourceGroupName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetTemplateSpecByIdParameterSet
```
Get-AzTemplateSpec [[-Version] <String>] [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 描述
此 Cmdlet 可用來列出訂閱/資源群組中的範本規格，或按名稱或識別碼取得特定的範本規格。取得特定範本規格時，可透過 **-Version** 參數指定版本名稱，以選擇性地取得特定版本。 使用 **-Version** 時，* 中只會顯示特定的版本詳細資料 *。所返回* 的範本規格物件上的版本。 如果在按名稱/id 來取回範本規格時未指定特定版本，所有版本都會在 * 內 *顯示。所返回物件的 Versions* 屬性。

**注意**：當列出訂閱或資源群組內的所有範本規格時，每個會退回的範本規格 *"。Versions"* 屬性為 *Null。* 版本資訊只有在提供 -Name 或 -ResourceId 參數時 (例如：您要求特定的範本規格/版本) 。

## 例子

### 範例 1：列出目前訂閱中的範本規格
```powershell
PS C:\> Get-AzTemplateSpec
```

列出目前訂閱中所有的範本規格。

### 範例 2：資源群組中的清單範本規格
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG'
```

列出目前訂閱之資源群組 "myRG" 中所有的範本規格。

### 範例 3：取得所有 (範本規格) 名稱
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec'
```

在資源群組 "myRG" 中，獲得名為 "MyTemplateSpec" 的範本規格相關資訊。

**注意**：所有範本規格的版本都會在 "中顯示 *。Return 物件的 Versions*" 屬性。

### 範例 4：根據名稱取得 (範本規格) 範本規格
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec' -Version 'v1.0'
```

在資源群組 "myRG" 中，獲得名為 "MyTemplateSpec" 的範本規格版本 "v1.0" 相關資訊。

**注意***："。所退回物件的 Versions"* 屬性只會包含要求的特定版本。

### 範例 5：使用所有 (資源識別碼取得範本規格) 範本規格
```powershell
PS C:\> Get-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec'
```

在訂閱子Id 的資源群組 "myRG" 中，獲得名為 "MyTemplateSpec" 的範本規格 \{ 相關資訊 \} 。

**注意**：所有範本規格的版本都會在 "中顯示 *。Return 物件的 Versions*" 屬性。

### 範例 6：根據資源識別碼 (範本規格) 範本規格
```powershell
PS C:\> Get-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec' -Version 'v1.0'
```

在訂閱子Id 的資源群組 "myRG" 中，獲得名為 "MyTemplateSpec" 的範本規格版本 "v1.0" \{ 相關資訊 \} 。

**注意***："。所退回物件的 Versions"* 屬性只會包含要求的特定版本。

## 參數

### -DefaultProfile
用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。

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
範本規格的名稱。

```yaml
Type: System.String
Parameter Sets: GetTemplateSpecByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
資源組的名稱。

```yaml
Type: System.String
Parameter Sets: ListTemplateSpecsParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetTemplateSpecByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
範本規格的完全合格的資源識別碼。範例：/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}

```yaml
Type: System.String
Parameter Sets: GetTemplateSpecByIdParameterSet
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -版本
範本規格的版本。

```yaml
Type: System.String
Parameter Sets: GetTemplateSpecByNameParameterSet, GetTemplateSpecByIdParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。 詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)

## 輸入

### System.String

## 輸出

### Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplateSpec

## 筆記

## 相關連結
