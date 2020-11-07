---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: E6E40D1B-A5BC-4B38-9D22-F06A8E4DABDF
online version: ''
schema: 2.0.0
ms.openlocfilehash: f1360f45b751088bd899282cee2e64ce965d11fb
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/08/2020
ms.locfileid: "93968798"
---
# Get-WAPackVMOSDisk

## 摘要
取得虛擬機器的作業系統磁片物件。

## 句法

### 空白 (預設) 
```
Get-WAPackVMOSDisk [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### FromId
```
Get-WAPackVMOSDisk [-ID <Guid>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### FromName
```
Get-WAPackVMOSDisk [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 說明
這些主題已棄用，未來將會移除。
本主題描述 Microsoft Azure PowerShell 模組的0.8.1 版本中的 Cmdlet。
若要找出您正在使用的模組版本，請從 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。

**WAPackVMOSDisk** Cmdlet 會取得虛擬機器的作業系統磁片物件。

## 示例

### 範例1：使用名稱取得作業系統磁片
```
PS C:\> Get-WAPackVMOSDisk -Name "ContosoOSDisk"
```

這個命令會取得一個名為 ContosoOSDisk 的作業系統磁片。

### 範例2：使用識別碼取得作業系統磁片
```
PS C:\> Get-WAPackVMOSDisk -Id 66242D17-189F-480D-87CF-8E1D749998C8
```

這個命令會取得具有指定識別碼的作業系統磁片。

### 範例3：取得所有作業系統磁片
```
PS C:\> Get-WAPackVMOSDisk
```

這個命令會取得所有作業系統磁片。

## 參數

### -識別碼
指定作業系統磁片的唯一識別碼。

```yaml
Type: Guid
Parameter Sets: FromId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -名稱
指定作業系統磁片的名稱。

```yaml
Type: String
Parameter Sets: FromName
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

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

## 輸出

## 筆記

## 相關連結

[WAPackVM](./Get-WAPackVM.md)


