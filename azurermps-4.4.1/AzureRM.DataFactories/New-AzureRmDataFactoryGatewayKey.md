---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 8546C3FE-5396-4027-BF33-F98F6C018A67
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryGatewayKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryGatewayKey.md
ms.openlocfilehash: f1676d385b23711e71fbec5fb5d9131add4daaf4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449629"
---
# New-AzureRmDataFactoryGatewayKey

## 摘要
建立 Azure 資料工廠的閘道金鑰。 此 Cmdlet 已棄用，您應該改為使用 **新的 AzureRmDataFactoryGatewayAuthKey** 。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

### ByFactoryName (預設) 
```
New-AzureRmDataFactoryGatewayKey [-DataFactoryName] <String> [-GatewayName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByFactoryObject
```
New-AzureRmDataFactoryGatewayKey [-DataFactory] <PSDataFactory> [-GatewayName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**新的-AzureRmDataFactoryGatewayKey** Cmdlet 會為指定的 Azure 資料工廠閘道建立閘道金鑰。
您可以使用此金鑰，透過雲端服務註冊閘道。 此 Cmdlet 已棄用，您應該改為使用 **新的 AzureRmDataFactoryGatewayAuthKey** 。

## 示例

### 範例1：建立閘道金鑰
```
PS C:\>New-AzureRmDataFactoryGatewayKey -ResourceGroupName "ADF" -GatewayName "ContosoGateway" -DataFactoryName "WikiADF" | Format-List
GatewayKey : ADF#40cbb3d9-2736-4794-a8a6-e6b839b4894f@a2d875ce-c9d7-4b8b-ad65-dd3ebbb9a940@8c0d1801-e863-44af-82e6-fb2f0c00f2ae@xz#Y9R0NhAeH3u7wgnrJyiWj4Y/QIhH4fFilIdzZgwsVQA=
```

這個命令會為名為 ContosoGateway 的資料工廠閘道建立閘道金鑰，然後使用管線運算子將閘道金鑰傳送至 Format-List Cmdlet。
如需詳細資訊，請輸入 `Get-Help Format-List` 。

## 參數

### -DataFactory
指定 **PSDataFactory** 物件。
這個 Cmdlet 會為此參數指定的資料工廠建立閘道金鑰。

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DataFactoryName
指定資料工廠的名稱。
這個 Cmdlet 會為此參數指定的資料工廠建立閘道金鑰。

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -GatewayName
指定閘道的名稱。
這個 Cmdlet 會為此參數指定的閘道建立金鑰。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
指定 Azure 資源群組的名稱。
這個 Cmdlet 會為屬於此參數指定之群組的閘道建立金鑰。

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
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

### Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryGatewayKey

## 筆記
* 關鍵字： azure，azurerm，arm，資源，管理，管理員，資料，工廠

## 相關連結

[新-AzureRmDataFactoryGateway](./New-AzureRmDataFactoryGateway.md) 
[AzureRmDataFactoryGatewayAuthKey](./Get-AzureRmDataFactoryGatewayAuthKey.md) 
[新-AzureRmDataFactoryGatewayAuthKey](./New-AzureRmDataFactoryGatewayAuthKey.md)


