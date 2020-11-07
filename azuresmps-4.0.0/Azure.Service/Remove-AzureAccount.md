---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 3CD1A989-902C-48B3-81E9-7B78EDA5F880
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7003abf263fd4c669956f65c990246295cf7158d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967316"
---
# Remove-AzureAccount

## 摘要
從 Windows PowerShell 刪除 Azure 帳戶。

## 句法

```
Remove-AzureAccount -Name <String> [-Force] [-PassThru] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## 說明
**AzureAccount** Cmdlet 會從您漫遊使用者設定檔中的訂閱資料檔刪除 Azure 帳戶及其訂閱。
它不會從 Microsoft Azure 刪除帳戶，或以任何方式變更實際的帳戶。

使用這個 Cmdlet 很像是從您的 Azure 帳戶登入。
而且，如果您想要再次登入帳戶，請使用 [ **載入 AzureAccount** ] 或 [匯 **入-AzurePublishSettingsFile** ]，將該帳戶再次新增至 Windows PowerShell。

您也可以使用 **AzureAccount** Cmdlet 來變更 azure PowerShell Cmdlet 登入 azure 帳戶的方式。
如果您的帳戶同時有來自 **Import AzurePublishSettingsFile** 的管理憑證和來自 **Add AzureAccount** 的存取權杖，則 Azure PowerShell Cmdlet 只會使用存取權杖;它們會忽略管理憑證。
若要使用管理憑證，請執行 **移除-AzureAccount** 。
當 **AzureAccount** 發現管理憑證和存取權杖時，只會刪除存取權杖，而不會刪除帳戶。
管理憑證仍然存在，因此 Windows PowerShell 仍可使用帳戶。

本主題描述 Microsoft Azure PowerShell 模組的0.8.10 版本中的 Cmdlet。
若要取得您正在使用的模組版本，請在 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。

## 示例

### 範例1：移除帳戶
```
PS C:\> Remove-AzureAccount -Name admin@contoso.com
```

這個命令會 admin@contoso.com 從您的訂閱資料檔案中移除。
命令完成後，Windows PowerShell 將無法再使用該帳戶。

## 參數

### -Force
取消確認提示。
根據預設， **AzureAccount** 會在您從 Windows PowerShell 移除帳戶之前提示您。

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

### -名稱
指定要移除的帳戶名稱。
參數值區分大小寫。
不支援萬用字元。

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

### -PassThru
如果命令成功，則傳回 $True，且 $False 失敗。
根據預設，這個 Cmdlet 不會傳回任何輸出。

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
指定此 Cmdlet 讀取的 Azure 設定檔。 如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。

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

### 所有
您可以透過屬性名稱（而不是依值），將輸入管到這個 Cmdlet。

## 輸出

### None 或 System.object
如果您使用 *PassThru* 參數，這個 Cmdlet 會傳回布林值。
否則，它不會傳回任何輸出。

## 筆記

## 相關連結

[附加 AzureAccount](./Add-AzureAccount.md)

[AzureAccount](./Get-AzureAccount.md)


