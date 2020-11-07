---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: FB5CD696-108D-4A3E-8983-1C6562E8795A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 25ade8ccf395d37ab0856742fe473a6508c9d63b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967157"
---
# Add-AzureWebRole

## 摘要
新增 web worker 角色。

## 句法

```
Add-AzureWebRole [-TemplateFolder <String>] [-Name <String>] [-Instances <Int32>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## 說明
本主題描述 Microsoft Azure PowerShell 模組的0.8.10 版本中的 Cmdlet。
若要取得您正在使用的模組版本，請在 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。

**AzureWebRole** Cmdlet 會新增 web worker 角色。

## 示例

### 範例1：新增預設角色
```
PS C:\> Add-AzureWebRole
```

這個命令會新增網頁角色，此角色的預設設定為 Webrole1 名稱與單一實例。

### 範例2：新增具有名稱的角色
```
PS C:\> Add-AzureWebRole -Name "MyWebRole"
```

這個命令會將一個名為 MyWebRole 的單一網頁角色新增至目前的應用程式。

### 範例3：新增具有名稱和實例計數的角色
```
PS C:\> Add-AzureWebRole -Name "MyWebRole" -Instance 2
```

這個命令會將名為 MyWebRole 的網站角色新增至目前的應用程式。
Cmdlet 的角色實例計數為2。

### 範例4：新增具有名稱和範本的角色
```
PS C:\> Add-AzureWebRole -Name "MyWebRole" -TemplateFolder ".\MyWebTemplateFolder"
```

這個命令會將一個名為 MyWebRole 的單一網頁角色新增至目前的應用程式。
該命令會將名為 MyWebTemplateFolder 的資料夾指定為基架範本。

## 參數

### -實例
指定實例數。

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
指定 [範本] 資料夾。

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

[附加 AzureWorkerRole](./Add-AzureWorkerRole.md)

[新-AzureRoleTemplate](./New-AzureRoleTemplate.md)


