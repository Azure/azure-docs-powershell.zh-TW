---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/new-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlWebService.md
ms.openlocfilehash: 5988aed4ca0560daedc1470198e0b02975f18196
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100134163"
---
# New-AzMlWebService

## 摘要
建立新的 web 服務。

## 句法

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

## 說明
在現有的資源群組中建立 Azure 機器學習 web 服務。
如果資源群組中存在具有相同名稱的 web 服務，該呼叫就會做為更新作業，而現有的 web 服務會覆寫。

## 示例

### 範例1：從以 Json 檔案為基礎的定義建立新服務
```
New-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Location "South Central US" -DefinitionFile "C:\mlservice.json"
```

根據參照的 json 檔案中提供的定義，在 "myresourcegroup" 群組和華南美國地區建立名為 "mywebservicename" 的新 Azure 電腦學習 web 服務。

### 範例2：從物件實例建立新的服務
```
New-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Location "South Central US" -NewWebServiceDefinition $serviceDefinitionObject
```

您可以透過使用 Import-AzMlWebService Cmdlet，在發佈為資源前取得要自訂的 web 服務物件實例。

## 參數

### -DefaultProfile
用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱

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
指定包含 web 服務 JSON 格式定義之檔案的路徑。
您可以在 [swagger 規範] 底下的 [swagger] 中找到最新的 web 服務定義規格 https://github.com/Azure/azure-rest-api-specs/tree/master/arm-machinelearning 。

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

### -Force
不要要求確認。

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
輸入 Azure 資料中心區域，例如「美國西部」或「東南部亞洲」。
您可以將 web 服務放在支援該類型之資源的任何區域中。
Web 服務不必須位於與您的 Azure 訂閱或與其資源群組相同的區域中。
資源群組可以包含來自不同地區的 web 服務。
若要判斷哪些區域支援每個資源類型，請將 Get-AzResourceProvider 與 ProviderNamespace 參數 Cmdlet 搭配使用。

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
該名稱在 [資源] 群組中必須是唯一的。

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
新 web 服務的定義，包含組成服務的所有屬性。
這個參數是必要的，且代表 MachineLearning WebServices 的實例。在 WebService 類別中，
您可以在 [swagger 規範] 底下的 [swagger] 中找到最新的 web 服務定義規格 https://github.com/Azure/azure-rest-api-specs/blob/master/arm-machinelearning/2017-01-01/swagger/webservices.json 。

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
要放置 web 服務的資源群組。
輸入 Azure 資料中心區域，例如「美國西部」或「東南部亞洲」。
您可以將 web 服務放在支援該類型之資源的任何區域中。
Web 服務不必須位於與您的 Azure 訂閱或與其資源群組相同的區域中。
資源群組可以包含來自不同地區的 web 服務。
若要判斷哪些區域支援每個資源類型，請將 Get-AzResourceProvider 與 ProviderNamespace 參數 Cmdlet 搭配使用。

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
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### [MachineLearning] WebServices 的 Web 元件

## 輸出

### [MachineLearning] WebServices 的 Web 元件

## 筆記
關鍵字： azure，azurerm，arm，資源，管理，管理員，機器，機器學習，azureml

## 相關連結
