---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM
ms.assetid: 22B63259-799B-4F25-A06B-7A818D295870
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servermanagement/reset-azurermservermanagementgatewayprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Reset-AzureRmServerManagementGatewayProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Reset-AzureRmServerManagementGatewayProfile.md
ms.openlocfilehash: 0833266bcd6e98a1d9744db2bc202bce5a01f3f8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447655"
---
# Reset-AzureRmServerManagementGatewayProfile

## 摘要
重設伺服器管理閘道的設定檔。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

### ByName
```
Reset-AzureRmServerManagementGatewayProfile [-ResourceGroupName] <String> [-GatewayName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByObject
```
Reset-AzureRmServerManagementGatewayProfile [-Gateway] <Gateway> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 說明
**Reset AzureRmServerManagementGatewayProfile** Cmdlet 會重設 Azure Server 管理閘道的設定檔。

您必須使用 Save-AzureRmServerManagementGatewayProfile Cmdlet 來下載設定檔，然後再使用 Install-AzureRmServerManagementGatewayProfile Cmdlet，在您重設設定檔之後進行儲存。

## 示例

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

### -閘道
指定 Cmdlet 針對其重設設定檔的閘道。

可以指定，而不是 ResourceGoupName 和 GatewayName

```yaml
Type: Gateway
Parameter Sets: ByObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -GatewayName
指定 Cmdlet 重設設定檔的閘道名稱。

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
指定閘道所屬之資源群組的名稱。

```yaml
Type: String
Parameter Sets: ByName
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

### 關
參數 "閘道" 接受管線中 "Gateway" 類型的值

## 輸出

## 筆記

## 相關連結

[安裝-AzureRmServerManagementGatewayProfile](./Install-AzureRmServerManagementGatewayProfile.md)

[儲存-AzureRmServerManagementGatewayProfile](./Save-AzureRmServerManagementGatewayProfile.md)


