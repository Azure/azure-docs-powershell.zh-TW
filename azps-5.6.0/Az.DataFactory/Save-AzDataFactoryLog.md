---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 5490BB24-127E-4C21-B85F-B70D817B659A
online version: https://docs.microsoft.com/powershell/module/az.datafactory/save-azdatafactorylog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Save-AzDataFactoryLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Save-AzDataFactoryLog.md
ms.openlocfilehash: eb2e3c9acd93e8b20c7bdf6f4ee04ef2910a3cbb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916197"
---
# Save-AzDataFactoryLog

## 簡介
從 Azure HDInsight 處理下載記錄檔。

## 語法

### ByFactoryName (預設) 
```
Save-AzDataFactoryLog [-DataFactoryName] <String> [-Id] <String> [-DownloadLogs] [[-Output] <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByFactoryObject
```
Save-AzDataFactoryLog [-DataFactory] <PSDataFactory> [-Id] <String> [-DownloadLogs] [[-Output] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 描述
**Save-AzDataFactoryLog** Cmdlet 會下載與 Azure HDInsight 處理小明體或病毒專案相關的記錄檔案，或將自訂活動下載到您的本地硬碟。
您先執行 Get-AzDataFactoryRun Cmdlet，取得資料區執行之活動的識別碼，然後使用該識別碼從與 HDInsight 集區關聯的二進位大型物件 (BLOB) 儲存空間中，取得記錄檔。
如果您未指定 *DownloadLogs* 參數，Cmdlet 會直接返回記錄檔的位置。
如果您指定 *DownloadLogs* 而不指定輸出 (*輸出* 參數) ，記錄檔案會下載到預設的檔資料夾。
如果您指定 *DownloadLogs* 以及輸出檔案夾 (*輸出*) ，記錄檔會下載到指定的資料夾。

## 例子

### 範例 1：將記錄檔儲存至特定資料夾
```
PS C:\>Save-AzDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39" -DownloadLogs -Output "C:\Test"
```

此命令會針對使用識別碼為 841b77c9-d56c-48d1-99a3-8c16c3e77d39 的活動，其中活動屬於名為 ADF 之資源群組中 LogProcessingFactory 之資料工廠中的管線，因此會記錄記錄檔。
記錄檔案會儲存到 C：\Test 資料夾。

### 範例 2：將記錄檔案儲存到預設的檔資料夾
```
PS C:\>Save-AzDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39" -DownloadLogs
```

此命令會將記錄檔 (資料夾) 。

### 範例 3：取得記錄檔的位置
```
PS C:\>Save-AzDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39"
```

此命令會返回記錄檔的位置。
請注意，*未指定 DownloadLogs。*

## 參數

### -DataFactory
指定 **PSDataFactory** 物件。

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
此 Cmdlet 會下載此參數指定之資料工廠的記錄檔案。

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

### -DownloadLogs
表示此 Cmdlet 會下載記錄檔案至您的本地電腦。
如果 *未指定輸出* 資料夾，檔案會儲存至子資料夾下的檔資料夾。

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

### -Id
指定資料區執行之活動的識別碼。
使用 Get-AzDataFactoryRun Cmdlet 取得識別碼。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -輸出
指定儲存下載記錄檔案的輸出檔案夾。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
指定 Azure 資源組的名稱。
此 Cmdlet 會建立屬於此參數指定之群組的資料工廠。

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

### Microsoft.Azure.Commands.DataFactories.models.PSRunLogInfo

## 筆記
* 關鍵字：azure、azurerm、arm、resource、management、manager、data、azure

## 相關連結

[Get-AzDataFactoryRun](./Get-AzDataFactoryRun.md)

[Get-AzDataFactoryPipeline](./Get-AzDataFactoryPipeline.md)

[New-AzDataFactoryPipeline](./New-AzDataFactoryPipeline.md)

[Remove-AzDataFactoryPipeline](./Remove-AzDataFactoryPipeline.md)

[Set-AzDataFactoryPipelineActivePeriod](./Set-AzDataFactoryPipelineActivePeriod.md)

[Suspend-AzDataFactoryPipeline](./Suspend-AzDataFactoryPipeline.md)


