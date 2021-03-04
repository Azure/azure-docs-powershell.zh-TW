---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 66B25541-0FA5-46CF-90D8-FE9527BE11C6
online version: https://docs.microsoft.com/powershell/module/az.resources/remove-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTag.md
ms.openlocfilehash: 201e341ce05b22597f05601d7d269d2eb27c2358
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908778"
---
# Remove-AzTag

## 簡介
刪除預先定義的 Azure 標記或|刪除資源或訂閱上的整組標記。

## 語法

### RemovePredefinedTagParameterSet

```powershell
Remove-AzTag [-Name] <String> [[-Value] <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RemoveByResourceIdParameterSet

```powershell
Remove-AzTag
   -ResourceId <String>
   [-PassThru]
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

## 描述

**RemovePredefinedTagSet：Remove-AzTag** Cmdlet 會從您的訂閱中刪除預先定義的 Azure 標籤和值。 
若要從預先定義的標記中刪除特定值，請使用 *Value* 參數。
根據預設 **，Remove-AzTag** 會刪除指定的標記及其所有值。您無法刪除目前適用于資源或資源群組的標記或值。
使用 **Remove-AzTag** 之前，請使用 Set-AzResourceGroup Cmdlet 的 Tag 參數，從資源或資源群組中刪除標籤或值。
**Remove-AzTag** 是其中一部分的 Azure 標記模組，可協助管理預先定義的 Azure 標記。
Azure 標記是一組名稱值，可用於將 Azure 資源和資源群組分類，例如按部門或成本中心分類，或追蹤資源與群組的附注或批註。
您可以在單一步驟中定義並應用標記，但預先定義的標記讓您為訂閱中的標記建立標準、一致、可預測的名稱和值。

**RemoveByResourceIdParameterSet：****具有 ResourceId** 的 **Remove-AzTag** Cmdlet 會刪除資源或訂閱上的整組標籤。

## 例子

### 範例 1：刪除預先定義的標記
```powershell
PS C:\>Remove-AzTag -Name "Department"
```

此命令會刪除名為 Department 的預先定義標記及其所有值。
如果標記已適用于任何資源或資源群組，則命令會失敗。

### 範例 2：從預先定義的標記刪除值
```powershell
PS C:\>Remove-AzTag -Name "Department" -Value "HumanResources" -PassThru
Name:   Department
Count:  14
Values: 

        Name        Count
        =========   =====

        Finance        2
        IT            12
```

此命令會從預先定義的 Department 標記中刪除 HumanResources 值。
不會刪除標記。
如果該值已適用于任何資源或資源群組，則命令會失敗。

### 範例 3：刪除訂閱上的整組標記

```powershell
PS C:\>Remove-AzTag -ResourceId /subscriptions/{subId}
```

此命令會刪除訂閱上的 {subId} 整組標記。 如果未在 "-PassThru" 中傳遞，不會傳回已刪除的物件。

### 範例 4：刪除資源上的整組標記

```powershell
PS C:\>Remove-AzTag -ResourceId /subscriptions/{subId}/resourcegroups/{rg}/providers/Microsoft.Sql/servers/Server1 -PassThru

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             Dept     Finance
             Status   Normal
```

此命令會使用 {resourceId} 刪除資源上的整組標記。 傳回傳遞 "-PassThru" 時已刪除的 oject。

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
指定要移除的預先定義標記名稱。
根據預設 **，Remove-AzTag** 會移除指定的標記及其所有值。
若要刪除選取的值，但不要刪除標記，請使用 *Value* 參數。

```yaml
Type: System.String
Parameter Sets: RemovePredefinedTagParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -值
刪除預先定義的標記中的指定值，但不刪除標記。

```yaml
Type: System.String[]
Parameter Sets: RemovePredefinedTagParameterSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
標記實體的資源識別碼。 系統可能會標記資源、資源群組或訂閱。

```yaml
Type: System.String
Parameter Sets: RemoveByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
會返回代表已刪除標記的物件，或具有已刪除值的結果標記。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
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

### System.String[]

### System.Management.Automation.SwitchParameter

## 輸出

### Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag |Microsoft.Azure.Commands.Tags.Model.PSTagResource

## 筆記

## 相關連結

[Get-AzTag](./Get-AzTag.md)

[New-AzTag](./New-AzTag.md)

[Update-AzTag](./Update-AzTag.md)