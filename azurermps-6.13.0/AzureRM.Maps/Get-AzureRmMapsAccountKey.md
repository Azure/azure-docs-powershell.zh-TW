---
external help file: Microsoft.Azure.Commands.Maps.dll-Help.xml
Module Name: AzureRM.Maps
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.maps/get-azurermmapsaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Maps/Commands.Maps/help/Get-AzureRmMapsAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Maps/Commands.Maps/help/Get-AzureRmMapsAccountKey.md
ms.openlocfilehash: 1afe0f8f93bd00a384e1bb741ed8ea54e1ae66d1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449758"
---
# Get-AzureRmMapsAccountKey

## 摘要
取得帳戶的 API 金鑰。
這些金鑰是在對 Azure 對應進行後續呼叫時所使用的驗證機制。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

### NameParameterSet (預設) 
```
Get-AzureRmMapsAccountKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### InputObjectParameterSet
```
Get-AzureRmMapsAccountKey [-InputObject <PSMapsAccount>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ResourceIdParameterSet
```
Get-AzureRmMapsAccountKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 說明
Get-AzureRmMapsAccountKey Cmdlet 會取得已置備之 Azure 地圖帳戶的 API 金鑰。
Azure 地圖帳戶有兩個 API 金鑰：主要和次要。
這些金鑰可讓您與 Azure Maps 帳戶端點互動。
使用 New-AzureRmMapsAccountKey (New-AzureRmMapsAccountKey.md) 重新產生金鑰。

## 示例

### 範例1
```powershell
PS C:\> Get-AzureRmMapsAccountKey -ResourceGroupName MyResourceGroup -Name MyAccount

PrimaryKey                                  SecondaryKey
----------                                  ------------
******************************************* *******************************************
```

傳回 [資源群組 MyResourceGroup] 中名為 [我的帳戶] 的帳戶按鍵。

### 範例2
```powershell
PS C:\> Get-AzureRmMapsAccountKey -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount

PrimaryKey                                  SecondaryKey
----------                                  ------------
******************************************* *******************************************
```

傳回指定 Azure Maps 帳戶的按鍵。

## 參數

### -DefaultProfile
用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。

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

### -InputObject
從 AzureRmMapsAccount 將 [地圖] 帳戶成管道。

```yaml
Type: Microsoft.Azure.Commands.Maps.Models.PSMapsAccount
Parameter Sets: InputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -名稱
地圖帳戶名稱。

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases: MapsAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
資源組名稱。

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
地圖帳戶 ResourceId。

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
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

### System.object

### PSMapsAccount 中的 [.]
參數： InputObject (ByValue) 

## 輸出

### PSMapsAccountKeys 中的 [.]

## 筆記

## 相關連結
