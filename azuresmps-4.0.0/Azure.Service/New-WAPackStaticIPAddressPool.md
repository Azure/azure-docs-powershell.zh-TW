---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 22A9B83D-789D-4722-BDD1-D8C448CFB88A
online version: ''
schema: 2.0.0
ms.openlocfilehash: c809a49e2e8c1a534d6868c99bcc7cab1d20ccd1
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/08/2020
ms.locfileid: "93968827"
---
# New-WAPackStaticIPAddressPool

## 摘要
建立靜態 IP 位址池。

## 句法

```
New-WAPackStaticIPAddressPool -VMSubnet <VMSubnet> -Name <String> -IPAddressRangeStart <String>
 -IPAddressRangeEnd <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 說明
這些主題已棄用，未來將會移除。
本主題描述 Microsoft Azure PowerShell 模組的0.8.1 版本中的 Cmdlet。
若要找出您正在使用的模組版本，請從 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。

**新的-WAPackStaticIPAddressPool** Cmdlet 會建立靜態 IP 位址池。

## 示例

### 範例1：建立靜態 IP 位址池
```
PS C:\> $VNet = Get-WAPackVNet -Name "ContosoVNet01"
PS C:\> $VMSubnet = Get-WAPackVMSubnet -VNet $VNet -Name "ContosoVMSubnet01"
PS C:\> New-WAPackStaticIpAddressPool ?VMSubnet $VMSubnet -Name "ContosoStaticIpAddressPool01" -IPAddressRangeStart "192.168.1.0" -IPAddressRangeEnd "192.168.1.10"
```

第一個命令首先會檢索要新增靜態 IP 位址池的虛擬機器網路。
此虛擬機器網路稱為 [ContosoVNet01]。

第二個命令使用先前檢索的虛擬機器網路來取得名為 ContosoVMSubnet01 的虛擬電腦子網，我們想要新增靜態 IP 位址池。

最後一個命令會建立新的靜態 IP 位址池，其名稱為 ContosoStaticIpAddressPool01 且範圍開始192.168.1.0 與範圍結束192.168.1.10。

## 參數

### -IPAddressRangeEnd
指定靜態 IP 位址池的 IP 位址範圍結束時間。

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IPAddressRangeStart
指定靜態 IP 位址池的 IP 位址範圍起始。

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -名稱
指定靜態 IP 位址池的名稱。

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
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

### -VMSubnet
指定與靜態 IP 位址池相關聯的 VMSubnet。

```yaml
Type: VMSubnet
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


