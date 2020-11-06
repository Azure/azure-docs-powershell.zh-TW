---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 89ED4231-7616-47D0-BDAA-D849C245DC79
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmAppServicePlan.md
ms.openlocfilehash: 9fe7d3d9580411c31fdf5ca7e21ba1c4379217a4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449676"
---
# Get-AzureRmAppServicePlan

## 摘要
在指定的資源群組中取得 Azure App Service 方案。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

### S1
```
Get-AzureRmAppServicePlan [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### S2
```
Get-AzureRmAppServicePlan [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**AzureRmAppServicePlan** Cmdlet 會取得指定資源群組中的 Azure App 服務方案。

## 示例

### 範例1：從資源群組取得 App 服務方案
```
PS C:\>Get-AzureRmAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

這個命令會取得名為 ContosoASP 的應用程式服務方案，這些名稱屬於名為「預設-Web-WestUS」的資源群組。

### 範例2：取得位置中的所有 App 服務方案
```
PS C:\>Get-AzureRmAppServicePlan -Location "West US"
```

這個命令會取得位於「美國西部」區域中的所有 App 服務方案。

## 參數

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

### -位置
位於 

```yaml
Type: System.String
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -名稱
App 服務方案名稱

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
資源群組名稱

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

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

### AppServicePlan 中的 [網站]。

## 筆記

## 相關連結

[新-AzureRmAppServicePlan](./New-AzureRmAppServicePlan.md)

[移除-AzureRmAppServicePlan](./Remove-AzureRmAppServicePlan.md)

[Set-AzureRmAppServicePlan](./Set-AzureRmAppServicePlan.md)


