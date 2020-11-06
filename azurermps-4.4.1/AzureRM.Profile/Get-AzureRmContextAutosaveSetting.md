---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmContextAutosaveSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmContextAutosaveSetting.md
ms.openlocfilehash: 60120e66596830e018351ceb492a36cd1ad1032d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449562"
---
# Get-AzureRmContextAutosaveSetting

## 摘要
顯示有關內容自動儲存功能的中繼資料，包括 whterh 內容是 automaticallys aved，以及可以找到已儲存的內容和認證資訊的位置。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Get-AzureRmContextAutosaveSetting [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
顯示有關內容自動儲存功能的中繼資料，包括是否自動儲存內容，以及可以在何處找到已儲存的內容和認證資訊。

## 示例

### 取得目前會話的內容儲存中繼資料
```
PS C:\> Get-AzureRmContextAutosaveSetting

Mode             : Process
ContextDirectory : None
ContextFile      : None
CacheDirectory   : None
CacheFile        : None
Settings         : {}
```

取得有關是否已儲存內容的詳細資料 wehere。  在上述範例中，已停用 [自動儲存] 功能。

### 取得目前使用者的內容儲存中繼資料
```
PS C:\> Get-AzureRmContextAutosaveSetting -Scope CurrentUser

Mode             : CurrentUser
ContextDirectory : C:\Users\contoso\AppData\Roaming\Windows Azure Powershell
ContextFile      : AzureRmContext.json
CacheDirectory   : C:\Users\contoso\AppData\Roaming\Windows Azure Powershell
CacheFile        : TokenCache.dat
Settings         : {}
```

取得目前使用者預設是否已儲存內容的詳細資料。  請注意，這可能與目前會話中使用中的設定不同。 在上述範例中，已啟用 [自動儲存] 功能，並將資料儲存到預設位置。

## 參數

### -DefaultProfile
用於與 azure 進行通訊的認證、帳戶、租使用者與訂閱

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

### -範圍
決定內容變更的範圍，例如，變更只適用于目前的進程，或只適用于此使用者開始的所有會話。

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases: 
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### 所有

## 輸出

### CoNtextAutosaveSettings 的常見驗證。
目前使用者的 [自動儲存] 設定的相關資訊，包括是否已針對目前使用者啟用自動儲存，以及內容和認證檔案的儲存位置。

## 筆記

## 相關連結

