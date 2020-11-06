---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: 869167AA-54F8-4A1C-AC08-5555A63EE1BC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlAllowedVMSizesPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlAllowedVMSizesPolicy.md
ms.openlocfilehash: ae003c3c523c17db9c486edaa68d7e0991b0e6d2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451707"
---
# Get-AzureRmDtlAllowedVMSizesPolicy

## 摘要
在 DevTest Labs 中取得 lab 的允許虛擬機器大小原則。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Get-AzureRmDtlAllowedVMSizesPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**AzureRmDtlAllowedVMSizesPolicy** Cmdlet 會取得允許的虛擬機器大小原則，可讓您指定實驗室所允許的虛擬機器大小清單。
Cmdlet 會傳回原則的啟用或停用狀態，以及您已在指定原則中設定的所有允許虛擬機器大小清單。

## 示例

## 參數

### -LabName
指定此 Cmdlet 取得虛擬電腦大小原則之實驗的名稱。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
指定實驗室所屬之資源群組的名稱。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

## 輸出

### PSPolicy 中的 DevTestLabs。
這個 Cmdlet 會傳回指定實驗室所允許的虛擬機器大小清單的原則。

## 筆記

## 相關連結

[Set-AzureRmDtlAllowedVMSizesPolicy](./Set-AzureRmDtlAllowedVMSizesPolicy.md)

[Azure 開發測試實驗室 Cmdlet](./AzureRM.DevTestLabs.md)


