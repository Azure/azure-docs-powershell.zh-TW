---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTemplateSpec.md
ms.openlocfilehash: be3a16707303016e22be8052721efcb35c608b3e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98435484"
---
# Get-AzTemplateSpec

## 摘要
取得或列出範本規格

## 句法

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

## 說明
這個 Cmdlet 可用來列出訂閱/資源群組中的範本規格，或取得特定的範本規格（依名稱或 id）。以名稱/id 取得特定的範本規格時，可以選擇透過 **版本** 參數指定版本名稱來檢索特定版本。 使用 **-版本** 時，只會在 * 中顯示特定版本的詳細資料 *。* 傳回的範本規格物件上的版本。 如果您在以名稱/識別碼來檢索範本規格時沒有指定特定的版本，所有版本都將出現在 * 中 *。* 傳回物件的版本屬性。

**注意**：列出訂閱或資源群組中的所有範本規格時，每個傳回的範本規格是 *"。[版本]* 屬性將會是 *null*。 版本資訊只會包含在下列情況中提供的-名稱或-ResourceId 參數 (：您要求特定的範本規格/版本) 。

## 示例

### 範例1：清單範本規格在目前的訂閱中
```powershell
PS C:\> Get-AzTemplateSpec
```

列出目前訂閱中的所有範本規格。

### 範例2： [資源] 群組中的 [清單範本規格]
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG'
```

列出目前訂閱之資源群組 ' myRG」中的所有範本規格。

### 範例3：取得範本規格 (，並以名稱) 所有版本
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec'
```

取得資源群組 "myRG" 中名為「MyTemplateSpec」的範本規範的相關資訊。

**注意**：所有範本規格的版本都會出現在「中 *。* 返回物件的版本屬性。

### 範例4：取得範本規格 (依名稱) 特定版本
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec' -Version 'v1.0'
```

取得資源群組 "myRG" 中名為「MyTemplateSpec」的範本規格版本 ' v 1.0」的相關資訊。

**注意**：」 *。* 所傳回物件的版本屬性將只包含所要求的特定版本。

### 範例5：取得範本規格 (，並以資源識別碼) 所有版本
```powershell
PS C:\> Get-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec'
```

取得訂閱 subId 之資源群組 "myRG" 中名為 "MyTemplateSpec" 的範本規格資訊 \{ \} 。

**注意**：所有範本規格的版本都會出現在「中 *。* 返回物件的版本屬性。

### 範例6：取得範本規格 (由資源識別碼) 特定版本
```powershell
PS C:\> Get-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec' -Version 'v1.0'
```

取得訂閱 subId 之資源群組 "myRG" 中名為 "MyTemplateSpec" 的範本規格的版本 "v 1.0" 的相關資訊 \{ \} 。

**注意**：」 *。* 所傳回物件的版本屬性將只包含所要求的特定版本。

## 參數

### -DefaultProfile
用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。

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
資源群組的名稱。

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
範本規格的完全限定資源識別碼。範例：/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}

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
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。

## 輸入

### System.object

## 輸出

### PSTemplateSpec 中的 SdkModels （）

## 筆記

## 相關連結
