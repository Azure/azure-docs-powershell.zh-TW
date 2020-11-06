---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/save-azurermcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Save-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Save-AzureRmContext.md
ms.openlocfilehash: 451498760d85cc018b8fbade625625ec6ecc1910
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447290"
---
# Save-AzureRmContext

## 摘要
儲存目前的驗證資訊以供在其他 PowerShell 會話中使用。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Save-AzureRmContext [[-Profile] <AzureRmProfile>] [-Path] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 說明
Save-AzureRmContext Cmdlet 會儲存目前的驗證資訊，以供在其他 PowerShell 會話中使用。

## 示例

### 範例1：儲存目前會話的內容
```
PS C:\> Connect-AzureRmAccount
PS C:\> Save-AzureRmContext -Path C:\test.json
```

這個範例會將目前會話的 Azure 內容儲存至提供的 JSON 檔案。

### 範例2：儲存指定內容
```
PS C:\> Save-AzureRmContext -Profile (Connect-AzureRmAccount) -Path C:\test.json
```

這個範例會將傳遞到 Cmdlet 的 Azure 內容儲存到提供的 JSON 檔案。

## 參數

### -DefaultProfile
用於與 azure 進行通訊的認證、租使用者及訂閱。

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

### -Force
覆寫指定的檔案（如果有的話）

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Path
指定要儲存驗證資訊之檔案的路徑。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -設定檔
指定此 Cmdlet 讀取的 Azure 內容。
如果您沒有指定內容，這個 Cmdlet 會從本機預設的內容讀取。

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Models.AzureRmProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
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
Default value: None
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### AzureRmProfile 中的 [Common.]
參數：設定檔 (ByValue) 

## 輸出

### PSAzureProfile 的設定檔。

## 筆記

## 相關連結
