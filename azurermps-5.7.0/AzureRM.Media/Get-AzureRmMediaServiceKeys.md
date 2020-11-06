---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: 2099938F-5325-416C-AE10-6813546A1055
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.media/get-azurermmediaservicekeys
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Get-AzureRmMediaServiceKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Get-AzureRmMediaServiceKeys.md
ms.openlocfilehash: 368423076003b03524272977ff8721db57721232
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449325"
---
# Get-AzureRmMediaServiceKeys

## 摘要
取得存取與媒體服務相關聯之 REST 端點的重要資訊。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Get-AzureRmMediaServiceKeys [-ResourceGroupName] <String> [-AccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**AzureRmMediaServiceKeys** Cmdlet 會取得存取 Representational 狀態轉移 (REST 與 Azure 媒體服務相關聯的) 端點的重要資訊。

## 示例

### 範例1：取得存取媒體服務的重要資訊
```
PS C:\>Get-AzureRmMediaServiceKeys -ResourceGroupName "ResourceGroup001" -AccountName "MediaService001"
```

這個命令會取得從屬於名為 ResourceGroup001 之資源群組的名為 MediaService001 的媒體服務的重要資訊。

## 參數

### -AccountName
指定此 Cmdlet 取得媒體服務金鑰的媒體服務名稱。

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱

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

### -ResourceGroupName
指定包含媒體服務之資源群組的名稱。

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

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### 所有
這個 Cmdlet 不接受任何輸入。

## 輸出

### PSServiceKeys 中的 [.]

## 筆記

## 相關連結

[Set-AzureRmMediaServiceKey](./Set-AzureRmMediaServiceKey.md)


