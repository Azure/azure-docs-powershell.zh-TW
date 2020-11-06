---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/get-azurermcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmContext.md
ms.openlocfilehash: dbe93ca98fe8cf7a0a22f2b52a17a17e7222c261
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446923"
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
PS C:\> Connect-AzureRmAccount
PS C:\> Get-AzureRmContext

Name                                     Account             SubscriptionName    Environment         TenantId
----                                     -------             ----------------    -----------         --------
Subscription1 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription1       AzureCloud          xxxxxxxx-x...
```

在這個範例中，我們會使用 Connect AzureRmAccount，透過 Azure 訂閱登入我們的帳戶，然後我們會呼叫 AzureRmCoNtext 以取得目前會話的內容。

### 範例2：列出所有可用的內容
```
PS C:\> Get-AzureRmContext -ListAvailable

Name                                     Account             SubscriptionName    Environment         TenantId
----                                     -------             ----------------    -----------         --------
Subscription1 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription1       AzureCloud          xxxxxxxx-x...
Subscription2 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription2       AzureCloud          xxxxxxxx-x...
Subscription3 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription3       AzureCloud          xxxxxxxx-x...
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
Accepted values: Default

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### 所有

## 輸出

### PSAzureCoNtext 的設定檔。

## 筆記

## 相關連結

[Set-AzureRMCoNtext](./Set-AzureRMContext.md)

