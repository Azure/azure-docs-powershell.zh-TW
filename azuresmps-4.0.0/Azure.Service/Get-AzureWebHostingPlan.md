---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 3B3F1870-348D-4303-9520-FD81D4650F5F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2103a155b12fdf1e481173d529ff3308a3b2200b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967958"
---
# Get-AzureWebHostingPlan

## 摘要
在目前的訂閱中取得 Azure web 託管方案。

## 句法

```
Get-AzureWebHostingPlan [-WebSpaceName <String>] [-Name <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## 說明
本主題描述 Microsoft Azure PowerShell 模組的0.8.10 版本中的 Cmdlet。
若要取得您正在使用的模組版本，請在 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。

**AzureWebHostingPlan** Cmdlet 會在目前的訂閱中取得 Azure web 託管方案。

根據預設， **AzureWebHostingPlan** 會取得目前訂閱中的所有 Azure 託管方案，並傳回提供方案基本資訊的物件。
當您使用 *Web 空間* 和 *名稱* 參數時， **AzureWebHostingPlan** 會傳回特定的託管方案物件。

若要尋找目前的訂閱，請使用 **AzureSubscription** Cmdlet 的 *目前* 參數。
若要變更目前的訂閱，請使用 **AzureSubscription** Cmdlet。

## 示例

### 範例1：取得訂閱中的所有 web 主機託管方案
```
PS C:\> Get-AzureWebHostingPlan 

Name : Default1 
SKU : Basic 
WorkerSize : Small 
NumberOfWorkers : 1 
CurrentWorkerSize : Small 
CurrentNumberOfWorkers : 1 
Status : Ready 
WebSpace : eastuswebspace 
Name : Default0 
SKU : Free 
WorkerSize : Small 
NumberOfWorkers : 0 
CurrentWorkerSize : Small 
CurrentNumberOfWorkers : 0 
Status : Ready
```

這個命令會在目前的訂閱中取得所有的 Azure web 主機託管方案。

### 範例2：在訂閱中取得特定的 web 主機託管方案
```
PS C:\> Get-AzureWebHostingPlan -WebSpaceName "westeuropewebspace" -Name "Default0" 

Name : Default0 
SKU : Free 
WorkerSize : Small 
NumberOfWorkers : 0 
CurrentWorkerSize : Small 
CurrentNumberOfWorkers : 0 
Status : Ready 
WebSpace : westeuropewebspace
```

這個命令會在目前訂閱中名為 westeuropewebspace 的 web 空間中，取得名為 Default0 的 web 託管方案。

## 參數

### -名稱
指定訂閱中的方案名稱。
根據預設，此 Cmdlet 會取得目前訂閱中的所有方案。
這個參數不支援萬用字元字元。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -設定檔
指定此 Cmdlet 讀取的 Azure 設定檔。
如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WebSpaceName
指定訂閱中的 web 空間名稱。
根據預設，此 Cmdlet 會取得指定 web 空間中的所有網站。
這個參數不支援萬用字元字元。

```yaml
Type: String
Parameter Sets: (All)
Aliases: WebSpace

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

###  
您可以透過屬性名稱（而不是依值），將輸入傳遞到此 Cmdlet。

## 輸出

### WindowsAzure. WebEntities. WebHostingPlan （）
根據預設， **AzureWebHostingPlan** 會傳回 **WebHostingPlan** 物件的陣列。

## 筆記

## 相關連結

