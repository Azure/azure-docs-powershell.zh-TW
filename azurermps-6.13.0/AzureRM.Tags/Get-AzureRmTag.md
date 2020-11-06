---
external help file: Microsoft.Azure.Commands.Tags.dll-Help.xml
Module Name: AzureRM.Tags
ms.assetid: 726E01DD-D73C-4D4B-8FC0-52767927367C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.tags/get-azurermtag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Tags/Commands.Tags/help/Get-AzureRmTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Tags/Commands.Tags/help/Get-AzureRmTag.md
ms.openlocfilehash: 945af88df11e210c3af3a11bd69123dd32befe4a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455899"
---
# Get-AzureRmTag

## 摘要
取得預先定義的 Azure 標記。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Get-AzureRmTag [[-Name] <String>] [-Detailed] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**AzureRmTag** Cmdlet 會在您的訂閱中取得預先定義的 Azure 標記。
這個 Cmdlet 會傳回有關標記的基本資訊，或有關標籤及其值的詳細資訊。
所有輸出物件都包含 Count 屬性，代表已套用標籤和值的資源和資源群組數。
**AzureRMTag** 是的 Azure Tags 模組可協助您管理預先定義的 Azure 標記。
Azure 標記是一個名稱值對，您可以用來將您的 Azure 資源和資源群組分類（例如 [部門] 或 [成本中心]），或追蹤有關資源與群組的備忘稿或意見。
您可以在單一步驟中定義及套用標籤，但預先定義的標記可讓您為訂閱中的標記建立標準、一致且可預測的名稱和值。
若要建立預先定義的標記，請使用 New-AzureRmTag Cmdlet。
若要將預先定義的標記套用至資源群組，請使用 New-AzureRmTag Cmdlet 的 *tag* 參數。
若要在資源群組中搜尋特定的標籤名稱或名稱與值，請使用 Get-AzureRMResourceGroup Cmdlet 的 *tag* 參數。

## 示例

### 範例1：取得所有預先定義的標記
```
PS C:\>Get-AzureRmTag

Name      Count
========  =====

Department    5
FY2015        2
CostCenter   20
```

這個命令會取得訂閱中所有預先定義的標記。
Count 屬性顯示標籤已套用到訂閱中資源和資源群組的次數。

### 範例2：透過名稱取得標記
```
PS C:\>Get-AzureRmTag -Name "Department"

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
```
PS C:\>Get-AzureRmTag -Detailed

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

### -詳細資訊
指示此操作會將有關標籤值的資訊新增到輸出。

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

### -名稱
指定要取得的標記名稱。
根據預設， **AzureRmTag** 會取得訂閱中所有預先定義的標記的基本資訊。
當您指定 *Name* 參數時， *詳細* 的參數就不會有任何作用。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### System.object

### SwitchParameter 的系統管理功能

## 輸出

### PSTag 中的 [命令]。

## 筆記

## 相關連結

[新-AzureRmTag](./New-AzureRmTag.md)

[移除-AzureRmTag](./Remove-AzureRmTag.md)


