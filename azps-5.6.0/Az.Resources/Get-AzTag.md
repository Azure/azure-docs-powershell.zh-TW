---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 726E01DD-D73C-4D4B-8FC0-52767927367C
online version: https://docs.microsoft.com/powershell/module/az.resources/get-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTag.md
ms.openlocfilehash: b44c861e06c1043fd53e470cfba1e322ce1f1f48
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912322"
---
# Get-AzTag

## 簡介
預先定義 Azure 標記|在資源或訂閱上獲得整組標記。

## 語法

### GetPredefinedTagParameterSet
```
Get-AzTag [[-Name] <String>] [-Detailed] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByResourceIdParameterSet
```
Get-AzTag -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 描述

**GetPredefinedTagSet：Get-AzTag** Cmdlet 會取得訂閱中預先定義的 Azure 標籤。 
此 Cmdlet 會返回標籤的基本資訊，或標籤及其值的詳細資訊。
所有輸出物件都包含 Count 屬性，代表已將標記和值所使用之資源和資源群組的數量。
**Get-AzTag** 是其中一部分的 Azure 標記模組可協助管理預先定義的 Azure 標記。
Azure 標記是一組名稱值，可用於將 Azure 資源和資源群組分類，例如按部門或成本中心分類，或追蹤資源與群組的附注或批註。
您可以在單一步驟中定義並應用標記，但預先定義的標記讓您為訂閱中的標記建立標準、一致、可預測的名稱和值。
若要建立預先定義的標籤，請使用 New-AzTag Cmdlet。
若要將預先定義的標籤適用于資源群組，請使用Cmdlet New-AzTag標記參數。
若要搜尋資源群組中的特定標籤名稱或名稱與值，請使用Get-AzResourceGroup Cmdlet 的 Tag 參數。

**GetByResourceIdParameterSet：****具有 ResourceId** 的 **Get-AzTag** Cmdlet 會取得資源或訂閱上的整組標籤。

## 例子

### 範例 1：取得所有預先定義的標記
```powershell
PS C:\>Get-AzTag

Name      Count
========  =====

Department    5
FY2015        2
CostCenter   20
```

此命令會獲得訂閱中所有預先定義的標記。
Count 屬性會顯示該標記已對訂閱中的資源和資源群組所使用次數。

### 範例 2：按名稱取得標記
```powershell
PS C:\>Get-AzTag -Name "Department"

Name:   Department
Count:  5
Values: 

        Name        Count
        ==========  =====

        Finance       2
        IT            3
```

此命令會獲得部門標記及其值的詳細資訊。
Count 屬性會顯示標記及其每個值已對訂閱中的資源和資源群組所使用次數。

### 範例 3：取得所有標記的值
```powershell
PS C:\>Get-AzTag -Detailed

Name:   Department
Count:  5
Values: 

        Name        Count
        ==========  =====

        Finance       2
        IT            3


Name:   FY2015
Count:  2


Name:   CostCenter
Count:  20
Values: 

        Name        Count
        ==========  =====

        0001          5
        0002         10
        0003          5
```

此命令使用 *詳細參數* 取得訂閱中所有預先定義之標記的詳細資訊。
使用 *詳細* 參數相當於針對每個標記使用 *Name* 參數。

### 範例 4：取得訂閱上的整組標記

```powershell
PS C:\>Get-AzTag -ResourceId /subscriptions/{subId}

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             tagKey1  tagValue1
             tagKey2  tagValue2
```

此命令會使用 {subId} 在訂閱上獲得整組標記。

### 範例 5：取得資源上的整組標記

```powershell
PS C:\>Get-AzTag -ResourceId /subscriptions/{subId}/resourcegroups/{rg}/providers/Microsoft.Sql/servers/Server1

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             Dept     Finance
             Status   Normal
```

此命令會使用 {resourceId} 在資源上獲得整組標記。

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

### -詳細資料
表示此作業會將有關標記值的資訊新加到輸出中。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetPredefinedTagParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -名稱
預先定義的標記名稱。
根據預設 **，Get-AzTag** 會取得訂閱中所有預先定義之標記的基本資訊。
當您指定 *Name* 參數時， *詳細參數* 沒有作用。

```yaml
Type: System.String
Parameter Sets: GetPredefinedTagParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
標記實體的資源識別碼。 系統可能會標記資源、資源群組或訂閱。

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
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

### Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag |Microsoft.Azure.Commands.Tags.Model.PSTagResource

## 筆記

## 相關連結

[New-AzTag](./New-AzTag.md)

[Remove-AzTag](./Remove-AzTag.md)

[Update-AzTag](./Update-AzTag.md)
