---
external help file: Microsoft.Azure.Commands.AnalysisServices.Dataplane.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/sync-azureanalysisservicesinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Sync-AzureAnalysisServicesInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Sync-AzureAnalysisServicesInstance.md
ms.openlocfilehash: f3fb2377fd78db4b330afd39a8691f958597f07a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447101"
---
# Sync-AzureAnalysisServicesInstance

## 摘要

將指定的 Analysis Services 伺服器實例上的指定資料庫同步處理到目前登入的 scaleout 中的所有查詢實例，如 Add-AzureAnalysisServicesAccount 命令中所指定

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Sync-AzureAnalysisServicesInstance [-Instance] <String> [-Database] <String> [-Passthru]
```

## 說明

Sync-AzureAnalysisServicesInstance Cmdlet 會將指定的 Analysis Services 伺服器實例上的指定資料庫同步處理到目前已登入的 [Add-AzureAnalysisServicesAccount] 命令中指定的所有查詢 scaleout 實例

## 示例

### 範例1

```
PS C:\>Sync-AzureAnalysisServicesInstance -Instance asazure://westus.asazure.windows.net/contoso -Database SalesOrders
```

這個命令會在環境 westus.asazure.windows.net 中，同步處理名為「contoso」的伺服器中名為 SalesOrders 的資料庫，前提是使用者已使用 Add-AzureAnalysisServicesAccount 命令登入此環境。

## 參數

### -實例

要重新開機之 Analysis Services 伺服器實例的名稱

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -資料庫

要同步處理的資料庫身分識別

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru

如果命令成功，則指定此值會傳回 true。

```yaml
Type: Switch
Parameter Sets: (All)
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## 輸入

### 所有
這個 Cmdlet 不接受任何輸入。

## 輸出

### System.object

## 筆記

別名： Sync-AzureAsInstance

## 相關連結
