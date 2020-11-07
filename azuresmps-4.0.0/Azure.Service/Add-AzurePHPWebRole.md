---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: F9A06B8B-55DB-48A5-B246-53347E759E64
online version: ''
schema: 2.0.0
ms.openlocfilehash: 050c05f2cdad546388744bcebca4f28a12a03038
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967836"
---
# Add-AzurePHPWebRole

## 摘要
建立 PHP 應用程式所需的檔案和配置。

## 句法

```
Add-AzurePHPWebRole [-Name <String>] [-Instances <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 說明
本主題描述 Microsoft Azure PowerShell 模組的0.8.10 版本中的 Cmdlet。
若要取得您正在使用的模組版本，請在 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。

**AzurePHPWebRole** Cmdlet 會針對將透過 IIS 託管在 Azure 中的 PHP 應用程式，建立檔案和設定（有時稱為基架）。

## 示例

### 範例1：使用預設值新增網頁角色
```
PS C:\> Add-AzurePHPWebRole
```

這個範例會使用一個名為 "WebRole1" 的服務的預設值，為新的網頁角色新增所需的檔案和配置，其中包含1個實例。

### 範例2：新增具有多個實例的網頁角色
```
PS C:\> Add-AzurePHPWebRole MyWebRole -I 2
```

這個範例會將新網頁角色所需的檔案和配置，新增至目前的應用程式，並使用名稱 "MyWebRole" 和角色實例計數2。

## 參數

### -實例
指定此網頁角色的角色實例數。
預設值為1。

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: i

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -名稱
指定網頁角色的名稱。
名稱會決定包含 PHP 應用程式所需檔案和配置的目錄名稱。
預設值為 WebRole #，其中 # 是服務中網頁角色的數目。

```yaml
Type: String
Parameter Sets: (All)
Aliases: n

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

## 輸出

## 筆記

## 相關連結

[附加 AzurePHPWorkerRole](./Add-AzurePHPWorkerRole.md)

[新-AzureServiceProject](./New-AzureServiceProject.md)


