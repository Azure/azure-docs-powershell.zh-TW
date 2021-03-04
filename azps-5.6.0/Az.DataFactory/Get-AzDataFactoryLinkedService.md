---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: DFA41A2B-7C8A-42CB-B0B6-5E6FF853EFEE
online version: https://docs.microsoft.com/powershell/module/az.datafactory/get-azdatafactorylinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryLinkedService.md
ms.openlocfilehash: 9f52e2a709e2518dbc749b20afc97125e9b3ae64
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907777"
---
# Get-AzDataFactoryLinkedService

## 簡介
在 Azure Data Factory 中，獲得連結服務的資訊。

## 語法

### ByFactoryName (預設) 
```
Get-AzDataFactoryLinkedService [-DataFactoryName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByFactoryObject
```
Get-AzDataFactoryLinkedService [-DataFactory] <PSDataFactory> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 描述
**Get-AzDataFactoryLinkedService** Cmdlet 會取得 Azure Data Factory 中連結服務的資訊。
如果您指定連結服務的名稱，此 Cmdlet 會獲得該連結服務的資訊。
如果您未指定名稱，此 Cmdlet 會獲得資料工廠中所有連結服務的資訊。

## 例子

### 範例 1：取得所有連結服務的資訊
```
PS C:\>Get-AzDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" | Format-List
```

此命令會獲得名稱為 WikiADF 的資料工廠中所有連結服務的資訊，然後使用管線運算子將連結服務Format-List Cmdlet。
該 Cmdlet 會格式化結果。
如需要詳細資訊，請鍵入 `Get-Help Format-List` 。

### 範例 2：取得特定連結服務的資訊
```
PS C:\>Get-AzDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "HDILinkedService"
LinkedServiceName   ResourceGroupName     DataFactoryName              Properties
-----------------   -----------------     ---------------              ----------
HDILinkedService    ADF                   WikiADF                      Microsoft.DataFactories.HDInsightBYOCAsset
```

此命令會從名為 WikiADF 的資料工廠中，獲得名為 HDILinkedService 的連結服務相關資訊。

### 範例 3：指定 DataFactory 參數以取得特定連結服務的資訊
```
PS C:\>$DataFactory = Get-AzDataFactory -ResourceGroupName "ADF" -Name "ContosoFactory"
PS C:\> Get-AzDataFactoryLinkedService -DataFactory $DataFactory | Format-Table -Property LinkedServiceName, DataFactoryName, ResourceGroupName
```

第一個命令使用 Get-AzDataFactory Cmdlet 取得名為 ContosoFactory 的資料工廠，然後將它儲存在 $DataFactory 變數中。
第二個命令會獲得儲存在 $DataFactory 之資料工廠的連結服務相關資訊，然後使用管線運算子將該資訊傳遞至 Format-Table Cmdlet。
**Format-Table** 將輸出格式化為資料集，將指定的屬性格式化為資料集欄。

## 參數

### -DataFactory
指定 **PSDataFactory** 物件。
此 Cmdlet 會獲得屬於此參數指定之資料工廠的連結服務。

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
此 Cmdlet 會獲得屬於此參數指定之資料工廠的連結服務。

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

### -名稱
指定取得相關資訊之連結服務的名稱。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
指定 Azure 資源組的名稱。
此 Cmdlet 會獲得屬於此參數指定之群組的連結服務。

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

### CommonParameters
此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。 詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。

## 輸入

### Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory

### System.String

## 輸出

### Microsoft.Azure.Commands.DataFactories.models.PSLinkedService

## 筆記
* 關鍵字：azure、azurerm、arm、resource、management、manager、data、azure

## 相關連結

[New-AzDataFactoryLinkedService](./New-AzDataFactoryLinkedService.md)

[Remove-AzDataFactoryLinkedService](./Remove-AzDataFactoryLinkedService.md)


