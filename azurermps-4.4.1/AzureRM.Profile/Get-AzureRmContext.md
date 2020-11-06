---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmContext.md
ms.openlocfilehash: 3ad029e84245aee45bbcdd08ea0d78c5e57b985e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449563"
---
# Get-AzureRmContext

## 摘要
取得用來驗證 Azure 資源管理器要求的中繼資料。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

### GetSingleCoNtext (預設) 
```
Get-AzureRmContext [-DefaultProfile <IAzureContextContainer>] [[-Name] <String>] [<CommonParameters>]
```

### ListAllCoNtexts
```
Get-AzureRmContext [-ListAvailable] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
Get-AzureRmContext Cmdlet 會取得目前用來驗證 Azure 資源管理器要求的中繼資料。

這個 Cmdlet 會取得 Active Directory 帳戶、Active Directory 租使用者、Azure 訂閱及目標 Azure 環境。
Azure 資源管理器 Cmdlet 會在進行 Azure 資源管理員要求時預設使用這些設定。

## 示例

### 範例1：取得目前的內容
```
PS C:\> Add-AzureRmAccount
PS C:\> Get-AzureRmContext

Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :
```

在這個範例中，我們使用 AzureRmAccount，透過 Azure 訂閱登入我們的帳戶，然後透過呼叫 AzureRmCoNtext 來取得目前會話的內容。

### 範例2：列出所有可用的內容
```
PS C:\> Get-AzureRmContext -ListAvailable

Name                  : Test
Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :

Name                  : Production
Environment           : AzureCloud
Account               : prod@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Production Subscription
CurrentStorageAccount :
```

在這個範例中，會顯示所有目前可用的上下文。  使用者可以使用 AzureRmCoNtext 選取其中一個上下文。

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

### -ListAvailable
列出目前會話中所有可用的上下文。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ListAllContexts
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -名稱
內容的名稱

```yaml
Type: System.String
Parameter Sets: GetSingleContext
Aliases: 
Accepted values: [contrib@AzureSDKTeam.onmicrosoft.com, 0b1f6471-1bf0-4dda-aec3-cb9272f09590], [markcowl@microsoft.com, 00977cdb-163f-435f-9c32-39ec8ae61f4d]

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

## 輸出

### PSAzureCoNtext
這個 Cmdlet 會傳回 Azure 資源管理器 Cmdlet 所使用的帳戶、租使用者和訂閱。

## 筆記

## 相關連結

[Set-AzureRMCoNtext](./Set-AzureRMContext.md)

