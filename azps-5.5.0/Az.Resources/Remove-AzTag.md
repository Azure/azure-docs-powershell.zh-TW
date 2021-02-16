---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 66B25541-0FA5-46CF-90D8-FE9527BE11C6
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTag.md
ms.openlocfilehash: 22a43739ec63f8287ce51c4c4f4a125b4e5b1c65
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100133626"
---
# Remove-AzTag

## 摘要
刪除預先定義的 Azure 標記或值 |刪除資源或訂閱上的整個標記組。

## 句法

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

## 說明

**RemovePredefinedTagSet**： **Remove-AzTag** Cmdlet 會從您的訂閱中刪除預先定義的 Azure 標記和值。
若要從預先定義的標記中刪除特定值，請使用 *Value* 參數。
根據預設， **移除-AzTag** 會刪除指定的標記及其所有值。您無法刪除目前已套用至資源或資源群組的標記或值。
在使用 **Remove-AzTag** 之前，請使用 Set-AzResourceGroup Cmdlet 的 *tag* 參數來刪除 [資源] 或 [資源] 群組中的標籤或值。
AzTag 是其中一部分的 Azure Tags 模組可協助您管理預先定義 **的** Azure 標記。
Azure 標記是一個名稱值對，您可以用來將您的 Azure 資源和資源群組分類（例如 [部門] 或 [成本中心]），或追蹤有關資源與群組的備忘稿或意見。
您可以在單一步驟中定義及套用標籤，但預先定義的標記可讓您為訂閱中的標記建立標準、一致且可預測的名稱和值。

**RemoveByResourceIdParameterSet**： AzTag Cmdlet （含 **ResourceId** **）** 會刪除資源或訂閱上的整個標記組。

## 示例

### 範例1：刪除預先定義的標記
```powershell
PS C:\>Remove-AzTag -Name "Department"
```

這個命令會刪除名為「部門」及其所有值的預先定義標記。
如果已將標記套用至任何資源或資源群組，則命令會失敗。

### 範例2：從預先定義的標記中刪除值
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

這個命令會從預先定義的 [部門] 標記刪除 HumanResources 值。
它不會刪除標記。
如果該值已套用至任何資源或資源群組，命令就會失敗。

### 範例3：刪除訂閱上整套的標記

```powershell
PS C:\>Remove-AzTag -ResourceId /subscriptions/{subId}
```

這個命令會使用 {subId} 刪除訂閱上的整個標記組。 如果不是傳入 "-PassThru"，就不會傳回刪除的物件。

### 範例4：刪除資源的整個標記集

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

這個命令會在資源上使用 {resourceId} 刪除整個標記組。 傳入 "-PassThru" 時，會傳回已刪除的 oject。

## 參數

### -DefaultProfile
用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。

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
指定要移除的預先定義標記的名稱。
根據預設， **移除-AzTag** 會移除指定的標記及其所有值。
若要刪除選取的值，但不刪除標記，請使用 *Value* 參數。

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
從預先定義的標記中刪除指定的值，但不會刪除標籤。

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
標籤實體的資源識別碼。 資源、資源群組或訂閱可能會加上標籤。

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
傳回代表已刪除的標籤或含有已刪除之值的結果標記的物件。

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
在執行 Cmdlet 之前提示您進行確認。

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
顯示在執行 Cmdlet 時會發生什麼情況。
未執行 Cmdlet。

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
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。

## 輸入

### System.object

### System.object []

### SwitchParameter 的系統管理功能

## 輸出

### [PSTag |] （通用）命令。[PSTagResource] 命令。

## 筆記

## 相關連結

[AzTag](./Get-AzTag.md)

[新-AzTag](./New-AzTag.md)

[更新-AzTag](./Update-AzTag.md)