---
external help file: Microsoft.Azure.Commands.Tags.dll-Help.xml
Module Name: AzureRM
ms.assetid: 23DB0AD2-7EB7-4373-BB8D-BB6CB651DD54
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.tags/new-azurermtag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Tags/Commands.Tags/help/New-AzureRmTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Tags/Commands.Tags/help/New-AzureRmTag.md
ms.openlocfilehash: 77bf93905b0cba4e8f8a23cb9f3cb8945fff74f1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452963"
---
# New-AzureRmTag

## 摘要
建立預先定義的 Azure 標記，或將值新增到現有的標籤。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
New-AzureRmTag [-Name] <String> [[-Value] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 說明
**AzureRmTag** Cmdlet 會建立具有選擇性預先定義值的預先定義的 Azure 標記。
您也可以使用它將其他值新增到現有的預先定義標記。
若要建立預先定義的標記，請輸入唯一的標籤名稱。
若要將值新增到現有的預先定義標記，請指定現有標記的名稱和新值。

這個 Cmdlet 會傳回一個物件，該物件代表新的或修改過的標記及其值，以及已套用的資源數。

AzureRmTag 是 [Azure Tags] 模組的一部分，可協助您管理預先定義 **的** Azure 標記。
Azure 標記是一個名稱值對，您可以用來將您的 Azure 資源和資源群組分類（例如 [部門] 或 [成本中心]），或追蹤有關資源與群組的備忘稿或意見。

您可以在單一步驟中定義及套用標籤，但預先定義的標記可讓您為訂閱中的標記建立標準、一致且可預測的名稱和值。
如果訂閱包含任何預先定義的標記，您就無法將未定義的標籤或值套用到訂閱中的任何資源或資源群組。

若要將預先定義的標記套用至資源或資源群組，請使用 New-AzureRmTag Cmdlet 的 *tag* 參數。
若要搜尋具有指定標記名稱或名稱和值的資源群組，請使用 Get-AzureRMResourceGroup Cmdlet 的 *tag* 參數。

每個標記都有一個名稱。
這些值是選擇性的。
預先定義的 Azure 標記可以有多個值，但是當您將標籤套用至資源或資源群組時，會套用標籤名稱，且只套用其其中一個值。
例如，您可以建立預先定義的部門標記，其中包含每個部門的值，例如財務、人力資源及 IT。
當您將部門標記套用至資源時，只會套用一個預先定義的值（例如 [財務]）。

## 示例

### 範例1：建立預先定義的標記
```
PS C:\>New-AzureRmTag -Name "FY2015"
Name:   Department
Count:  0
Values: 

        Name        Count
        =========   =====

        Finance     0
```

這個命令會建立名為 FY2015 的預先定義標記。
此標記沒有值。
您可以將沒有值的標籤套用至資源或資源群組，或使用 [ **新-AzureRmTag** ]，將值新增到標籤。
您也可以在將標籤套用至 [資源] 或 [資源] 群組時，指定一個值。

### 範例2：使用值建立預先定義的標記
```
PS C:\>New-AzureRmTag -Name "Department" -Value "Finance"
Name:   Department
Count:  0
Values: 

        Name        Count
        =========   =====
        Finance     0
```

這個命令會建立名為「含財務價值」的「部門」的預先定義標籤。

### 範例3：將值新增至預先定義的標記
```
PS C:\>New-AzureRmTag -Name "Department" -Value "Finance"
Name:   Department
Count:  0
Values: 
        Name        Count
        =========   =====
        Finance     0 PS C:\>New-AzureRmTag -Name "Department" -Value "IT"
Name:   Department
Count:  0
Values: 
        Name        Count
        =========   =====
        Finance     0
        IT          0
```

這些命令會建立名為「具有兩個值的部門」的預先定義標記。
如果標籤名稱存在， **新的 AzureRmTag** 會將值新增到現有的標籤，而不是建立新的標記。

### 範例4：使用預先定義的標記
```
PS C:\>New-AzureRmTag -Name "CostCenter" -Value "0001"
Name:   CostCenter
Count:  0
Values: 
        Name        Count
        =========   =====
        0001        0 PS C:\>Set-AzureRmResourceGroup -Name "EngineerBlog" -Tag @{Name="CostCenter";Value="0001"}
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
    CostCenter   0001 PS C:\>Get-AzureRmTag -Name "CostCenter"
Name:   CostCenter
Count:  1
Values: 
        Name        Count
        =========   =====
        0001        1 PS C:\>Get-AzureRmResourceGroup -Tag @{Name="CostCenter"}
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

這個範例中的命令會建立並使用預先定義的標記。

## 參數

### -DefaultProfile
用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -名稱
指定標記名稱。
若要建立新的預先定義標記，請輸入唯一的名稱。

若要將值新增至現有的標籤，請輸入現有標記的名稱。
如果現有預先定義的標記具有指定的名稱， **新的 AzureRmTag** 會將指定的值（如果有的話）加到具有該名稱的標籤，而不是建立新的標記。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -值
指定標記值。
預先定義的標記可以有多個值，但您只能在每個命令中輸入一個值。
這個參數是選擇性的，因為標記可以有沒有值的名稱。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### 所有

## 輸出

### [PSTag] 命令。

## 筆記

## 相關連結

[AzureRmTag](./Get-AzureRmTag.md)

[移除-AzureRmTag](./Remove-AzureRmTag.md)


