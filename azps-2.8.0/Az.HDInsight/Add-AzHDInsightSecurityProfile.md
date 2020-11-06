---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: FB37494B-4035-45B7-88AB-DF33CEEF0D0A
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/add-azhdinsightsecurityprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightSecurityProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightSecurityProfile.md
ms.openlocfilehash: c0e54e92336b7b084448a980f632c886c24dc07c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93612325"
---
# Add-AzHDInsightSecurityProfile

## 摘要
新增安全設定檔至群集設定物件。

## 句法

```
Add-AzHDInsightSecurityProfile [-Config] <AzureHDInsightConfig> -Domain <String>
 -DomainUserCredential <PSCredential> -OrganizationalUnitDN <String> -LdapsUrls <String[]>
 [-ClusterUsersGroupDNs <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## 說明
安全設定檔是透過 kerberizing 來建立安全的群集。
安全性設定檔包含將群集加入 Active Directory 網域的相關設定。

## 示例

### 範例1
```
PS C:\> {{ Add example code here }}
```

{{在此處新增範例描述}}

## 參數

### -ClusterUsersGroupDNs
將可在 Ambari 和 Ranger 中使用之 Active Directory 群組的可分辨名稱

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Config
指定此 Cmdlet 修改的 HDInsight 群集設定物件。
這個物件是由 New-AzHDInsightClusterConfig Cmdlet 建立的。

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱

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

### -網域
群集的 Active Directory 網域

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DomainUserCredential
具有足夠許可權的網域使用者帳號憑證來建立群集。
[使用者名] 應為 [ user@domain 格式]

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LdapsUrls
Active Directory 的一或多個 LDAPS 伺服器的 url

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OrganizationalUnitDN
在 Active directory 中將會建立使用者和電腦帳戶的組織單位的可分辨名稱

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
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
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### AzureHDInsightConfig （即 Azure。

## 輸出

### AzureHDInsightSecurityProfile （即 Azure。

## 筆記

## 相關連結
