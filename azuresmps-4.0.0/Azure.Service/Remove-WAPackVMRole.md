---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 9999E0EE-4A32-4C18-A6EC-2A073DC08710
online version: ''
schema: 2.0.0
ms.openlocfilehash: e5dfe0f42987ba51613ff9bafa000713456dfaf7
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/08/2020
ms.locfileid: "93968857"
---
# Remove-WAPackVMRole

## 摘要
移除虛擬機器角色物件。

## 句法

### FromVMRoleObject (預設) 
```
Remove-WAPackVMRole -VMRole <VMRole> [-PassThru] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### FromCloudService
```
Remove-WAPackVMRole -VMRole <VMRole> -CloudServiceName <String> [-PassThru] [-Force]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 說明
這些主題已棄用，未來將會移除。
本主題描述 Microsoft Azure PowerShell 模組的0.8.1 版本中的 Cmdlet。
若要找出您正在使用的模組版本，請從 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。

**WAPackVMRole** Cmdlet 會移除虛擬機器角色物件。

## 示例

### 範例1：移除使用 WAP 入口網站建立的虛擬機器角色 () 
```
PS C:\> $VMRole = Get-WAPackVMRole -Name "ContosoVMRole01"
PS C:\> Remove-WAPackVMRole -VMRole $VMRole
```

第一個命令會使用 **WAPackVMRole** Cmdlet 取得名為 ContosoVMRole01 的虛擬機器角色，然後將該物件儲存在 $VMRole 變數中。

第二個命令會移除 $VMRole 中儲存的虛擬機器角色。
命令會提示您進行確認。假設此虛擬機器角色是使用 WAP 入口網站建立的，就不需要指定雲端服務名稱。

### 範例2：移除在手動建立雲端服務之後建立的虛擬機器角色
```
PS C:\> $VMRole = Get-WAPackVMRole -Name "ContosoVMRole02"
PS C:\> Remove-WAPackVMRole -VMRole $VMRole -CloudServiceName "ContosoCloudService02"
```

第一個命令會使用 **WAPackVMRole** Cmdlet 取得名為 "ContosoVMRole02" 的虛擬機器角色，然後將該物件儲存在 $VMRole 變數中。

第二個命令會移除 $VMRole 中儲存的虛擬機器角色。
命令會提示您進行確認。
假設此虛擬機器角色不是使用入口網站建立，則使用者必須指定雲端服務名稱。
在這種情況下，名為 "ContosoCloudService02"。

### 範例3：移除虛擬機器角色而不進行確認
```
PS C:\> $VMRole = Get-WAPackVMRole -Name "ContosoVMRole03"
PS C:\> Remove-WAPackVMRole -VMRole $VMRole -Force
```

第一個命令會使用 **WAPackVMRole** Cmdlet 取得名為 ContosoVMRole03 的雲端服務，然後將該物件儲存在 $VMRole 變數中。

第二個命令會移除 $VMRole 中儲存的虛擬機器角色。
這個命令包含 *Force* 參數。
該命令不會提示您進行確認。

## 參數

### -CloudServiceName
指定虛擬機器角色的雲端服務名稱。

```yaml
Type: String
Parameter Sets: FromCloudService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
強制執行命令，而不要求使用者確認。

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
傳回代表您正在使用之專案的物件。
根據預設，這個 Cmdlet 不會產生任何輸出。

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

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

### -VMRole
指定虛擬機器角色。
若要取得虛擬機器角色，請使用 **WAPackVMRole** Cmdlet。

```yaml
Type: VMRole
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -確認
在執行 Cmdlet 之前提示您進行確認。

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
顯示在執行 Cmdlet 時會發生什麼情況。
未執行 Cmdlet。

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

## 輸出

## 筆記

## 相關連結

[WAPackVMRole](./Get-WAPackVMRole.md)

[新-WAPackVMRole](./New-WAPackVMRole.md)

[Set-WAPackVMRole](./Set-WAPackVMRole.md)


