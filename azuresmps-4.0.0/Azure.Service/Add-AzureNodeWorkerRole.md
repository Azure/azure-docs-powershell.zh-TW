---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 7190C668-6A0C-4E1D-9B5A-0CEEF53E3F85
online version: ''
schema: 2.0.0
ms.openlocfilehash: 93573caf43a6c711e1aa1308c851c82faaef5bcd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967835"
---
# Add-AzureNodeWorkerRole

## 摘要
建立 Node.js 應用程式所需的檔案和資料夾，以便透過 node.exe 在雲端中託管

## 句法

```
Add-AzureNodeWorkerRole [-Name <String>] [-Instances <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 說明
本主題描述 Microsoft Azure PowerShell 模組的0.8.10 版本中的 Cmdlet。
若要取得您正在使用的模組版本，請在 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。

**AzureNodeWorkerRole** Cmdlet 會建立必要的檔案和資料夾（有時稱為基架），以便透過 node.exe 在雲端中託管 Node.js 應用程式。

## 示例

### 範例1：單一實例 worker 角色
```
PS C:\> Add-AzureWorkerRole MyWorkerRole
```

這個範例會將一個名為 **MyWorkerRole** 的單一輔助角色角色的基架新增到目前的應用程式。

### 範例2：多個實例 worker 角色
```
PS C:\> Add-AzureNodeWorkerRole MyWorkerRole -I 2
```

這個範例會將一個名為 **MyWorkerRole** 的單一輔助角色角色的基架新增到目前的應用程式，角色實例計數為2。

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
此值會決定包含在 worker 角色中主持之 node.js 服務之基架的資料夾名稱。
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

[附加 AzureNodeWebRole](./Add-AzureNodeWebRole.md)

[新-AzureServiceProject](./New-AzureServiceProject.md)


