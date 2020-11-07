---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: FEFBF1EF-FBCE-45D8-8455-F3F8662F1F36
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4ddf78f30cb6938571fc967d510e4ab99a0cfc80
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967833"
---
# Add-AzurePHPWorkerRole

## 摘要
針對將由 php.exe 託管至 Azure 的 PHP 應用程式建立所需的檔案和配置。

## 句法

```
Add-AzurePHPWorkerRole [-Name <String>] [-Instances <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 說明
本主題描述 Microsoft Azure PowerShell 模組的0.8.10 版本中的 Cmdlet。
若要取得您正在使用的模組版本，請在 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。

針對將由 php.exe 託管至 Azure 的 PHP 應用程式，建立所需的檔案和設定（有時稱為基架）。

## 示例

### 範例1：使用單一實例建立 worker 角色
```
PS C:\> Add-AzurePHPWorkerRole MyWorkerRole
```

這個範例會將一個名為 MyWorkerRole 的單一輔助角色角色所需的檔案和配置新增至目前的應用程式。

### 範例2：建立具有多個實例的 worker 角色
```
PS C:\> Add-AzurePHPWorkerRole MyWorkerRole -I 2
```

這個範例會將新的 worker 角色所需的檔案和配置新增至目前的應用程式，並使用 name MyWorkerRole，角色實例計數為2。

## 參數

### -實例
指定此 worker 角色的角色實例數。
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
指定 worker 角色的名稱。
名稱會決定包含在 worker 角色中託管之 PHP 服務所需的檔案和配置的資料夾名稱。
預設值為 WorkerRole1。

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

[新-AzureServiceProject](./New-AzureServiceProject.md)

[附加 AzurePHPWebRole](./Add-AzurePHPWebRole.md)


