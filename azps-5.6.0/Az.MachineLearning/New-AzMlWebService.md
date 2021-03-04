---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/powershell/module/az.machinelearning/new-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlWebService.md
ms.openlocfilehash: 1a48438d6cec1621361a00cefa2bfead28117b97
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904062"
---
# New-AzMlWebService

## 簡介
建立新 Web 服務。

## 語法

### CreateFromFile
```
New-AzMlWebService -ResourceGroupName <String> -Location <String> -Name <String> -DefinitionFile <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### CreateFromInstance
```
New-AzMlWebService -ResourceGroupName <String> -Location <String> -Name <String>
 -NewWebServiceDefinition <WebService> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## 描述
在現有的資源群組中建立 Azure 機器學習 Web 服務。
如果相同名稱的 Web 服務存在於資源群組中，則呼叫會做為更新作業，且會覆蓋現有的 Web 服務。

## 例子

### 範例 1：從 Json 檔案定義建立新服務
```
New-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Location "South Central US" -DefinitionFile "C:\mlservice.json"
```

根據參照 json 檔案中的定義，在 "myresourcegroup" 群組和美國中南部地區建立名為 "mywebservicename" 的新 Azure 機器學習 Web 服務。

### 範例 2：從物件實例建立新服務
```
New-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Location "South Central US" -NewWebServiceDefinition $serviceDefinitionObject
```

您可以使用 Cmdlet 取得 Web 服務物件實例以自訂，然後再發佈為Import-AzMlWebService資源。

## 參數

### -DefaultProfile
用於與 Azure 通訊的認證、帳戶、租使用者和訂閱

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefinitionFile
指定包含 Web 服務 JSON 格式定義的檔案路徑。
您可以在 swagger 規格下找到 Web 服務定義的最新規格 https://github.com/Azure/azure-rest-api-specs/tree/master/arm-machinelearning 。

```yaml
Type: System.String
Parameter Sets: CreateFromFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -強制
請勿要求確認。

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

### -位置
Web 服務的區域。
輸入 Azure 資料中心區域，例如「美國西部」或「東南亞」。
您可以將 Web 服務放在任何支援該類型資源的區域。
Web 服務不一定在 Azure 訂閱的同一區域，或與資源群組相同的區域。
資源群組可以包含不同區域的 Web 服務。
若要判斷哪些區域支援每種資源類型，請使用 Get-AzResourceProvider ProviderNamespace 參數 Cmdlet。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -名稱
Web 服務的名稱。
名稱在資源群組中必須是唯一的。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NewWebServiceDefinition
新 Web 服務的定義，其中包含服務的所有屬性。
此參數為必填專案，且代表 Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService 類的實例。
您可以在 swagger 規格下找到 Web 服務定義的最新規格 https://github.com/Azure/azure-rest-api-specs/blob/master/arm-machinelearning/2017-01-01/swagger/webservices.json 。

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService
Parameter Sets: CreateFromInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ResourceGroupName
放置 Web 服務的資源群組。
輸入 Azure 資料中心區域，例如「美國西部」或「東南亞」。
您可以將 Web 服務放在任何支援該類型資源的區域。
Web 服務不一定在 Azure 訂閱的同一區域，或與資源群組相同的區域。
資源群組可以包含不同區域的 Web 服務。
若要判斷哪些區域支援每種資源類型，請使用 Get-AzResourceProvider ProviderNamespace 參數 Cmdlet。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -確認
執行 Cmdlet 之前，提示您確認。

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
顯示 Cmdlet 執行時會發生什麼情況。
不會執行 Cmdlet。

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
此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。 詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。

## 輸入

### Microsoft.Azure.management.MachineLearning.WebServices.models.WebService

## 輸出

### Microsoft.Azure.management.MachineLearning.WebServices.models.WebService

## 筆記
關鍵字：azure、azurerm、arm、resource、management、manager、machine、機器學習、azureml

## 相關連結
