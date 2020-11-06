---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 5490BB24-127E-4C21-B85F-B70D817B659A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Save-AzureRmDataFactoryLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Save-AzureRmDataFactoryLog.md
ms.openlocfilehash: 8525333f2be148b59053c62fc4d0f95dda8949a7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451727"
---
# Save-AzureRmDataFactoryLog

## 摘要
從 Azure HDInsight 處理下載記錄檔。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

### ByFactoryName (預設) 
```
Save-AzureRmDataFactoryLog [-DataFactoryName] <String> [-Id] <String> [-DownloadLogs] [[-Output] <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByFactoryObject
```
Save-AzureRmDataFactoryLog [-DataFactory] <PSDataFactory> [-Id] <String> [-DownloadLogs] [[-Output] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**AzureRmDataFactoryLog** Cmdlet 會將與 Azure HDInsight 處理的記錄檔案下載到豬或 Hive 專案或自訂活動到您的本機硬碟。
您必須先執行 Get-AzureRmDataFactoryRun Cmdlet，以取得資料切片的活動執行 ID，然後使用該識別碼來從二進位大型物件中檢索記錄檔， (BLOB) 與 HDInsight 群集相關聯的儲存空間。

如果您沒有指定 *DownloadLogs* 參數，則此 Cmdlet 只會傳回記錄檔的位置。

如果您指定 *DownloadLogs* 但未指定輸出目錄 ( *輸出* 參數) ，則會將記錄檔案下載到預設的 [檔] 資料夾。

如果您指定 *DownloadLogs* ，並將輸出檔案夾 ( *輸出* ) ，則會將記錄檔案下載到指定的資料夾。

## 示例

### 範例1：將記錄檔儲存至特定資料夾
```
PS C:\>Save-AzureRmDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39" -DownloadLogs -Output "C:\Test"
```

這個命令會將活動執行的記錄檔儲存在名為841b77c9-d56c-48d1-99a3-8c16c3e77d39 的資料工廠中，其中的活動屬於名為「ADF」的資源群組中名為 LogProcessingFactory 的管線。
記錄檔會儲存到 [C:\Test] 資料夾。

### 範例2：將記錄檔儲存至預設的檔資料夾
```
PS C:\>Save-AzureRmDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39" -DownloadLogs
```

這個命令會將記錄檔案儲存到 [檔] 資料夾 (預設) 。

### 範例3：取得記錄檔的位置
```
PS C:\>Save-AzureRmDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39"
```

這個命令會傳回記錄檔的位置。
請注意，未指定 *DownloadLogs* 。

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
這個 Cmdlet 會下載此參數指定之資料工廠的記錄檔案。

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

### -DownloadLogs
表示此 Cmdlet 會將記錄檔案下載到您的本機電腦。
如果未指定 *Ouptut* 資料夾，檔案會儲存至子資料夾底下的 [檔] 資料夾。

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

### -識別碼
指定資料切片的活動執行 ID。
使用 Get-AzureRmDataFactoryRun Cmdlet 來取得 ID。

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
指定儲存下載的記錄檔的輸出檔案夾。

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
指定 Azure 資源群組的名稱。
這個 Cmdlet 會建立屬於此參數指定之群組的資料工廠。

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

### PSRunLogInfo 中的 DataFactories。

## 筆記
* 關鍵字： azure，azurerm，arm，資源，管理，管理員，資料，工廠

## 相關連結

[AzureRmDataFactoryRun](./Get-AzureRmDataFactoryRun.md)

[AzureRmDataFactoryPipeline](./Get-AzureRmDataFactoryPipeline.md)

[新-AzureRmDataFactoryPipeline](./New-AzureRmDataFactoryPipeline.md)

[移除-AzureRmDataFactoryPipeline](./Remove-AzureRmDataFactoryPipeline.md)

[Set-AzureRmDataFactoryPipelineActivePeriod](./Set-AzureRmDataFactoryPipelineActivePeriod.md)

[暫停-AzureRmDataFactoryPipeline](./Suspend-AzureRmDataFactoryPipeline.md)


