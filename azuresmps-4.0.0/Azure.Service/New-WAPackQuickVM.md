---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 53BD6ED4-EA66-448B-8B18-F078C0738AF5
online version: ''
schema: 2.0.0
ms.openlocfilehash: 90f02a261dc804f46a7ef503879a8ce9f43fad35
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/08/2020
ms.locfileid: "93968846"
---
# New-WAPackQuickVM

## 摘要
根據範本建立虛擬機器。

## 句法

```
New-WAPackQuickVM -Name <String> -Template <VMTemplate> -VMCredential <PSCredential>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 說明
這些主題已棄用，未來將會移除。
本主題描述 Microsoft Azure PowerShell 模組的0.8.1 版本中的 Cmdlet。
若要找出您正在使用的模組版本，請從 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。

**新的-WAPackQuickVM** Cmdlet 會根據範本建立虛擬機器。

## 示例

### 範例1：根據範本建立虛擬機器
```
PS C:\> $Credentials = Get-Credential
PS C:\> $TemplateId = Get-WAPackVMTemplate -Id 66242D17-189F-480D-87CF-8E1D749998C8
PS C:\> New-WAPackQuickVM -Name "VirtualMachine023" -Template $TemplateId -VMCredential $Credentials
```

第一個命令會建立一個 **PSCredential** 物件，然後將它儲存在 $Credentials 變數中。
此 Cmdlet 會提示您輸入帳戶和密碼。
如需詳細資訊，請輸入 `Get-Help Get-Credential` 。

第二個命令會使用 **WAPackVMTemplate** Cmdlet 取得範本。
該命令會指定範本的識別碼。
該命令會將範本物件儲存在 $TemplateID 變數中。

最後一個命令會建立名為 VirtualMachine023 的虛擬機器。
命令會以儲存在 $TemplateId 的範本為基礎。

## 參數

### -名稱
指定虛擬機器的名稱。

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
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

### -範本
指定範本。
這個 Cmdlet 會根據您指定的範本建立虛擬機器。
若要取得範本物件，請使用 **WAPackVMTemplate** Cmdlet。

```yaml
Type: VMTemplate
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMCredential
指定本機系統管理員帳戶的認證。
若要取得 **PSCredential** 物件，請使用 **取得認證** Cmdlet。
如需詳細資訊，請輸入 `Get-Help Get-Credential` 。

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases:

Required: True
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

[新-WAPackVM](./New-WAPackVM.md)

[WAPackVMTemplate](./Get-WAPackVMTemplate.md)


