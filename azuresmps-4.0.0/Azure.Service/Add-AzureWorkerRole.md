---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 8632A865-D4CC-4AE5-8307-055CDD776D26
online version: ''
schema: 2.0.0
ms.openlocfilehash: a2b79ee50bb5097896c2a120a9b7316adb2146b5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967156"
---
# Add-AzureWorkerRole

## 摘要
建立自訂工作人員角色所需的檔案和配置。

## 句法

```
Add-AzureWorkerRole [-TemplateFolder <String>] [-Name <String>] [-Instances <Int32>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 說明
本主題描述 Microsoft Azure PowerShell 模組的0.8.10 版本中的 Cmdlet。
若要取得您正在使用的模組版本，請在 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。

**AzureWorkerRole** Cmdlet 會針對自訂輔助角色建立必要的檔案和設定（有時稱為基架）。

## 示例

### 範例1：建立單一實例 worker 角色
```
PS C:\> Add-AzureWorkerRole -Name MyWorkerRole
```

這個範例會將一個名為 MyWorkerRole 的單一輔助角色角色的基架新增到目前的應用程式。

### 範例2：建立多個實例 worker 角色
```
PS C:\> Add-AzureWorkerRole MyWorkerRole -I 2
```

這個範例會將一個名為 MyWorkerRole 的新輔助角色角色的基架新增到目前的應用程式，而角色實例計數為2。

### 範例3：建立含自訂基架的 worker 角色
```
PS C:\> Add-AzureWorkerRole MyWorkerRole -TemplateFoldr .\MyWorkerRoleTemplate
```

這個範例會建立含自訂基架的 worker 角色。

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
這個值會決定包含自訂應用程式的基架的資料夾名稱，這些基架將寄宿在輔助角色中。
預設值為 WorkerRolenumber，其中 number 是服務中輔助角色的數目。

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

### -TemplateFolder
指定要用來建立 worker 角色的 [基架範本] 資料夾。

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

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

## 輸出

## 筆記

## 相關連結

[附加 AzureWebRole](./Add-AzureWebRole.md)

[新-AzureRoleTemplate](./New-AzureRoleTemplate.md)


