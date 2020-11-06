---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 5CC89899-00B6-424A-8896-FD32DE9DDA28
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVmssVaultCertificateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVmssVaultCertificateConfig.md
ms.openlocfilehash: 9014c91626d41e66f316b870e042af7d5655f07a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450684"
---
# New-AzureRmVmssVaultCertificateConfig

## 摘要
建立金鑰 Vault 憑證設定。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
New-AzureRmVmssVaultCertificateConfig [[-CertificateUrl] <String>] [[-CertificateStore] <String>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## 說明
**新的-AzureRmVmssVaultCertificateConfig** Cmdlet 會指定必須放在虛擬機器縮放集 (VMSS) 虛擬機器上的機密。
這個 Cmdlet 的輸出應該與 Add-AzureRmVmssSecret Cmdlet 搭配使用。

## 示例

### 範例1：建立主要電子倉庫憑證設定
```
PS C:\> New-AzureRmVmssVaultCertificateConfig -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion" -CertificateStore "MyCerts"
```

這個命令會建立一個主要的電子倉庫憑證配置，該設定會使用位於指定憑證 URL 之名為 MyCerts 的憑證存放區。

## 參數

### -CertificateStore
在新增憑證的規模集中，指定虛擬機器上的憑證存放區。
這僅適用于 Windows 虛擬電腦縮放集。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CertificateUrl
指定儲存在金鑰儲存庫中之憑證的 URI。

它是以 UTF-8 編碼的下列 JSON 物件的 base64 編碼：


{"data"： " \<Base64-encoded-certificate\> "，"資料類型"： "pfx"，"password"： " \<pfx-file-password\> "}

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
顯示在執行 Cmdlet 時會發生什麼情況。 未執行 Cmdlet。

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### 所有
這個 Cmdlet 不接受任何輸入。

## 輸出

###  
這個 Cmdlet 不會產生任何輸出。

## 筆記

## 相關連結

[附加 AzureRmVmssSecret](./Add-AzureRmVmssSecret.md)
