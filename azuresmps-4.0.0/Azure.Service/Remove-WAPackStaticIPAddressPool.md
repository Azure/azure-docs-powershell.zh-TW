---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: CE618AD2-7E28-4012-BF3C-B932B95FFDD5
online version: ''
schema: 2.0.0
ms.openlocfilehash: a07358c37bf30e8d5fc3040cdfd174b800df96e4
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/08/2020
ms.locfileid: "93968858"
---
# Remove-WAPackStaticIPAddressPool

## 摘要
移除靜態 IP 位址池物件。

## 句法

```
Remove-WAPackStaticIPAddressPool -StaticIPAddressPool <StaticIPAddressPool> [-PassThru] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 說明
這些主題已棄用，未來將會移除。
本主題描述 Microsoft Azure PowerShell 模組的0.8.1 版本中的 Cmdlet。
若要找出您正在使用的模組版本，請從 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。

**WAPackStaticIPAddressPool** Cmdlet 會移除靜態 IP 位址池物件。

## 示例

### 範例1：移除靜態 IP 位址池
```
PS C:\> $StaticIPAddressPool = Get-WAPackStaticIPAddressPool -Name "ContosoStaticIPAddressPool01"
PS C:\> Remove-WAPackStaticIPAddressPool -StaticIPAddressPool $StaticIPAddressPool
```

第一個命令會使用 **WAPackStaticIPAddressPool** Cmdlet 取得名為 ContosoStaticIPAddressPool01 的靜態 IP 位址池，然後將該物件儲存在 $StaticIPAddressPool 變數中。

第二個命令會移除 $StaticIPAddressPool 中儲存的靜態 IP 位址池。
命令會提示您進行確認。

### 範例2：移除靜態 IP 位址池而不進行確認
```
PS C:\> $StaticIPAddressPool = Get-WAPackStaticIPAddressPool -Name "ContosoStaticIPAddressPool02"
PS C:\> Remove-WAPackStaticIPAddressPool -StaticIPAddressPool $StaticIPAddressPool -Force
```

第一個命令會使用 **WAPackStaticIPAddressPool** Cmdlet 取得名為 ContosoStaticIPAddressPool02 的靜態 IP 位址池，然後將該物件儲存在 $ StaticIPAddressPool 變數中。

第二個命令會移除 $StaticIPAddressPool 中儲存的靜態 IP 位址池。
這個命令包含 *Force* 參數。
該命令不會提示您進行確認。

## 參數

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

### -StaticIPAddressPool
指定 StaticIPAddressPool。
若要取得靜態 IP 位址池，請使用 **WAPackStaticIPAddressPool** Cmdlet。

```yaml
Type: StaticIPAddressPool
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

## 輸出

## 筆記

## 相關連結

[WAPackStaticIPAddressPool](./Get-WAPackStaticIPAddressPool.md)

[移除-WAPackStaticIPAddressPool](./Remove-WAPackStaticIPAddressPool.md)


