---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 929F4593-2A71-49B9-87F8-F24FA9F6E314
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Test-AzureRmLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Test-AzureRmLogicApp.md
ms.openlocfilehash: fa848a8249fa01a61a7aa50855f24b2813b9fdf9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93457555"
---
# Test-AzureRmLogicApp

## 摘要
驗證邏輯應用程式定義。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

### LogicAppWithDefinitionParameterSet
```
Test-AzureRmLogicApp -ResourceGroupName <String> -Name <String> -Location <String> [-State <String>]
 [-Definition <Object>] [-IntegrationAccountId <String>] [-Parameters <Object>] [-ParameterFilePath <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### LogicAppWithDefinitionFileParameterSet
```
Test-AzureRmLogicApp -ResourceGroupName <String> -Name <String> -Location <String> [-State <String>]
 [-DefinitionFilePath <String>] [-IntegrationAccountId <String>] [-Parameters <Object>]
 [-ParameterFilePath <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**Test AzureRmLogicApp** Cmdlet 會驗證資源群組中的邏輯 app 定義。
指定邏輯應用程式名稱、資源組名稱、位置、狀態、整合帳戶識別碼或參數。

此模組支援動態參數。
若要使用動態參數，請在命令中輸入。
若要探索動態參數的名稱，請在 Cmdlet 名稱後輸入連字號 ( ) ，然後重複按 Tab 鍵以迴圈顯示可用的參數。
如果您省略必要的範本參數，則 Cmdlet 會提示您輸入值。

## 示例

### 範例1：使用檔路徑驗證邏輯 app
```
PS C:\>Test-AzureRmLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp01" -Location "westus" -State "Enabled" -DefinitionFilePath "d:\workflows\Definition.json" -ParameterFilePath "d:\workflows\Parameters.json"
```

這個命令會驗證指定資源群組中名為 LogicApp01 的邏輯 app。
此命令指定定義和參數檔案路徑。

### 範例2：使用物件驗證邏輯 app
```
PS C:\>Test-AzureRmLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp01" -Location "westus" -State "Enabled" -Definition [IO.File]::ReadAllText("d:\Workflows\Definition.json") -Parameters @{name1="value1", name2="value2"}
```

這個命令會驗證指定資源群組中名為 LogicApp01 的邏輯 app。
此命令指定定義和參數物件。

## 參數

### -定義
將邏輯 app 的定義指定為 JavaScript 物件符號 (JSON) 格式中的物件或字串。

```yaml
Type: System.Object
Parameter Sets: LogicAppWithDefinitionParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefinitionFilePath
將您的邏輯 app 的定義指定為 JSON 格式之定義檔案的路徑。

```yaml
Type: System.String
Parameter Sets: LogicAppWithDefinitionFileParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IntegrationAccountId
指定邏輯 app 的整合帳戶識別碼。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -位置
指定邏輯 app 的位置。
輸入 Azure 資料中心的位置，例如 [西部] 或 [東南部]。
您可以將邏輯 app 放置在任何位置。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -名稱
指定邏輯應用程式的名稱。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ParameterFilePath
指定 JSON 格式化參數檔的路徑。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -參數
指定邏輯 app 的參數集合物件。
指定雜湊資料表、字典 \<string\> 或字典 \<string, WorkflowParameter\> 。

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
指定資源群組的名稱。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -State
指定邏輯 app 的狀態。
此參數可接受的值為： [已啟用] 和 [已停用]。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

### System.object

## 筆記

## 相關連結

[AzureRmLogicApp](./Get-AzureRmLogicApp.md)

[新-AzureRmLogicApp](./New-AzureRmLogicApp.md)

[移除-AzureRmLogicApp](./Remove-AzureRmLogicApp.md)

[Set-AzureRmLogicApp](./Set-AzureRmLogicApp.md)

[開始-AzureRmLogicApp](./Start-AzureRmLogicApp.md)


