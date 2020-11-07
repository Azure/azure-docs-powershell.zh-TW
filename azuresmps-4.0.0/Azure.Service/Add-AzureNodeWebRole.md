---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: C2DAFB2C-A58B-406C-8349-8728771B279E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 59aef29c27d7eb96834d270c2fce48ff3acb9554
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967838"
---
# Add-AzureNodeWebRole

## 摘要
為 Node.js 應用程式建立必要的檔案和資料夾。

## 句法

```
Add-AzureNodeWebRole [-Name <String>] [-Instances <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 說明
本主題描述 Microsoft Azure PowerShell 模組的0.8.10 版本中的 Cmdlet。
若要取得您正在使用的模組版本，請在 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。

**載入 AzureNodeWebRole** 會建立必要的檔案和資料夾（有時稱為基架），以供在雲端透過 IIS 託管的 Node.js 應用程式使用。

## 示例

### 範例1：單一實例網頁角色
```
PS C:\> Add-AzureNodeWebRole -Name MyWebRole
```

這個範例會將一個名為 **MyWebRole** 的單一網頁角色的基架新增到目前的應用程式。

### 範例2：多重實例網頁角色
```
PS C:\> Add-AzureNodeWebRole MyWebRole -I 2
```

這個範例會將一個名為 **MyWebRole** 的新網頁角色的基架新增到目前的應用程式，而角色實例計數為2。

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
它也會決定包含要以網頁角色託管之 node.js 應用程式的基架的目錄名稱。
預設值為 WebRole #，其中 # 代表服務中的網頁角色數目。

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

[附加 AzureNodeWorkerRole](./Add-AzureNodeWorkerRole.md)

[新-AzureServiceProject](./New-AzureServiceProject.md)


