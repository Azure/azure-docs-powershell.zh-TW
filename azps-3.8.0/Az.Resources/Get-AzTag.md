---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 726E01DD-D73C-4D4B-8FC0-52767927367C
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTag.md
ms.openlocfilehash: 058f4a61f1e7ff2fe7f416ea0e4ada098c9efe51
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93959722"
---
# Get-AzTag

## 摘要
取得預先定義的 Azure 標記 |取得資源或訂閱上的整個標記集。

## 句法

### GetPredefinedTagParameterSet
```
Get-AzTag [[-Name] <String>] [-Detailed] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByResourceIdParameterSet
```
Get-AzTag -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明

**GetPredefinedTagSet** ： **AzTag** Cmdlet 會在您的訂閱中取得預先定義的 Azure 標記。
這個 Cmdlet 會傳回有關標記的基本資訊，或有關標籤及其值的詳細資訊。
所有輸出物件都包含 Count 屬性，代表已套用標籤和值的資源和資源群組數。
**AzTag** 是的 Azure Tags 模組可協助您管理預先定義的 Azure 標記。
Azure 標記是一個名稱值對，您可以用來將您的 Azure 資源和資源群組分類（例如 [部門] 或 [成本中心]），或追蹤有關資源與群組的備忘稿或意見。
您可以在單一步驟中定義及套用標籤，但預先定義的標記可讓您為訂閱中的標記建立標準、一致且可預測的名稱和值。
若要建立預先定義的標記，請使用 New-AzTag Cmdlet。
若要將預先定義的標記套用至資源群組，請使用 New-AzTag Cmdlet 的 *tag* 參數。
若要在資源群組中搜尋特定的標籤名稱或名稱與值，請使用 Get-AzResourceGroup Cmdlet 的 *tag* 參數。

**GetByResourceIdParameterSet** ： AzTag Cmdlet （含 **ResourceId** **）** 會取得資源或訂閱上的整個標記集。

## 示例

### 範例1：取得所有預先定義的標記
```powershell
PS C:\>Get-AzTag

Name      Count
========  =====

Department    5
FY2015        2
CostCenter   20
```

這個命令會取得訂閱中所有預先定義的標記。
Count 屬性顯示標籤已套用到訂閱中資源和資源群組的次數。

### 範例2：透過名稱取得標記
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

這個命令會取得部門標記及其值的詳細資訊。
Count 屬性會顯示標籤及其每個值已套用到訂閱中資源和資源群組的多少次。

### 範例3：取得所有標記的值
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

這個命令會使用 *詳細* 的參數，以取得訂閱中所有預先定義的標記的詳細資訊。
使用 *詳細* 的參數，相當於使用每個標記的 *Name* 參數。

### 範例4：取得訂閱上的整個標記集

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

這個命令會在訂閱上使用 {subId} 來取得一組完整的標記。

### 範例5：在資源上取得整個標記集

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

這個命令會在資源上使用 {resourceId} 來取得整個標記組。

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

### -詳細資訊
指示此操作會將有關標籤值的資訊新增到輸出。

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
預先定義標記的名稱。
根據預設， **AzTag** 會取得訂閱中所有預先定義的標記的基本資訊。
當您指定 *Name* 參數時， *詳細* 的參數就不會有任何作用。

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
標籤實體的資源識別碼。 資源、資源群組或訂閱可能會加上標籤。

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
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。

## 輸入

### System.object

### SwitchParameter 的系統管理功能

## 輸出

### [PSTag |] （通用）命令。[PSTagResource] 命令。

## 筆記

## 相關連結

[新-AzTag](./New-AzTag.md)

[移除-AzTag](./Remove-AzTag.md)

[更新-AzTag](./Update-AzTag.md)
