---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: DFA41A2B-7C8A-42CB-B0B6-5E6FF853EFEE
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactorylinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryLinkedService.md
ms.openlocfilehash: 5f59dfeeb024b4a81554a700bdcebc9d7f39e80a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94128473"
---
# Get-AzDataFactoryLinkedService

## 摘要
取得 Azure 資料工廠中連結服務的相關資訊。

## 句法

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

## 說明
**AzDataFactoryLinkedService** Cmdlet 會取得 Azure 資料工廠中連結服務的相關資訊。
如果您指定連結服務的名稱，此 Cmdlet 會取得該連結服務的相關資訊。
如果您沒有指定名稱，此 Cmdlet 會取得資料工廠中所有連結服務的相關資訊。

## 示例

### 範例1：取得所有連結服務的相關資訊
```
PS C:\>Get-AzDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" | Format-List
```

這個命令會取得資料工廠（名為 WikiADF）中所有連結服務的相關資訊，然後使用管線運算子將連結的服務傳送到 Format-List Cmdlet。
該 Cmdlet 會格式化結果。
如需詳細資訊，請輸入 `Get-Help Format-List` 。

### 範例2：取得特定連結服務的相關資訊
```
PS C:\>Get-AzDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "HDILinkedService"
LinkedServiceName   ResourceGroupName     DataFactoryName              Properties
-----------------   -----------------     ---------------              ----------
HDILinkedService    ADF                   WikiADF                      Microsoft.DataFactories.HDInsightBYOCAsset
```

這個命令會在名為 WikiADF 的資料工廠中，取得名為 HDILinkedService 的連結服務的相關資訊。

### 範例3：指定 DataFactory 參數，以取得特定連結服務的相關資訊
```
PS C:\>$DataFactory = Get-AzDataFactory -ResourceGroupName "ADF" -Name "ContosoFactory"
PS C:\> Get-AzDataFactoryLinkedService -DataFactory $DataFactory | Format-Table -Property LinkedServiceName, DataFactoryName, ResourceGroupName
```

第一個命令使用 Get-AzDataFactory Cmdlet 來取得名為 ContosoFactory 的資料工廠，然後將它儲存在 $DataFactory 變數中。
第二個命令會針對儲存在 $DataFactory 中的資料工廠，取得連結服務的相關資訊，然後使用管線運算子將該資訊傳送到 Format-Table Cmdlet。
[ **格式]-表格** 將輸出格式設定為資料集，並將指定屬性做為資料集資料行。

## 參數

### -DataFactory
指定 **PSDataFactory** 物件。
這個 Cmdlet 會取得屬於此參數所指定之資料工廠的連結服務。

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
這個 Cmdlet 會取得屬於此參數所指定之資料工廠的連結服務。

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

### -名稱
指定要取得資訊之連結服務的名稱。

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
指定 Azure 資源群組的名稱。
這個 Cmdlet 會取得屬於此參數指定之群組的連結服務。

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
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory

### System.object

## 輸出

### PSLinkedService 中的 DataFactories。

## 筆記
* 關鍵字： azure，azurerm，arm，資源，管理，管理員，資料，工廠

## 相關連結

[新-AzDataFactoryLinkedService](./New-AzDataFactoryLinkedService.md)

[移除-AzDataFactoryLinkedService](./Remove-AzDataFactoryLinkedService.md)


