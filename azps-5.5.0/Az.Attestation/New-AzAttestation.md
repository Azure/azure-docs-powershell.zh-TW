---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/new-azattestation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/New-AzAttestation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/New-AzAttestation.md
ms.openlocfilehash: c9295883035ca7c53742fc9cb6d1b2e9a800eb3f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100136654"
---
# New-AzAttestation

## 摘要
建立證明

## 句法

```
New-AzAttestation -Name <String> -ResourceGroupName <String> -Location <String> [-Tag <Hashtable>]
 [-PolicySignersCertificateFile <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## 說明
New-AzAttestation Cmdlet 會在指定的資源群組中建立證明。

## 示例

### 範例1
```powershell
PS C:\> New-AzAttestation -Name pshtest4 -ResourceGroupName psh-test-rg -Location "East US" -Tags @{Test="true";CreationYear="2020"}                                                                                                                                                                                         
Id                : subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/psh-test-rg/providers/Microsoft.Attestation/attestationProviders/pshtest4
Location          : East US
ResourceGroupName : psh-test-rg
Name              : pshtest4
Status            : Ready
TrustModel        : AAD
AttestUri         : https://pshtest4.us.attest.azure.net
Tags              : {CreationYear, Test}
TagsTable         :
                    Name          Value
                    ============  =====
                    CreationYear  2020
                    Test          true
```

使用幾個標籤建立名為 *pshtest4* 的證明提供者的新實例，並使用主機名稱 t 原則的 AAD 信任。

### 範例2
```powershell
PS C:\> New-AzAttestation -Name pshtest3 -ResourceGroupName psh-test-rg -Location "East US" -PolicySignersCertificateFile .\cert1.pem                                                                                                                                                
Id                : subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/psh-test-rg/providers/Microsoft.Attestation/attestationProviders/pshtest3
Location          : East US
ResourceGroupName : psh-test-rg
Name              : pshtest3
Status            : Ready
TrustModel        : Isolated
AttestUri         : https://pshtest3.us.attest.azure.net
Tags              :
TagsTable         :
```

透過使用 PEM 檔案指定一組受信任的簽章金鑰，即可建立名為 *pshtest3*' 的證明提供者的新實例，該實例使用的是 Isoladed 信任。

## 參數

### -DefaultProfile
用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -位置
指定要在其中建立證明提供者的 Azure 區域。 將命令 Get-AzResourceProvider 與 ProviderNamespace 參數搭配使用，即可查看您的選擇。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -名稱
指定要建立之實例的名稱。
名稱可以是字母、數位或連字號的任何組合。
名稱必須以字母或數位開頭和結尾。
名稱必須是通用唯一的。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: InstanceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PolicySignersCertificateFile
在單一憑證檔案中指定發行原則的信任簽章金鑰集合。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
指定要在其中建立證明之現有資源群組的名稱。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tag
代表資源標記的雜湊資料表。

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -確認
在執行 Cmdlet 之前提示您進行確認。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
顯示在執行 Cmdlet 時會發生什麼情況。
未執行 Cmdlet。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。

## 輸入

### System.object

### [System.object] 集合. Hashtable

## 輸出

### PSAttestation 中的 [.]

## 筆記

## 相關連結
