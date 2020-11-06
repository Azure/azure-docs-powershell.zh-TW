---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C257E62F-1535-4626-A12B-F4572D00BB13
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: 1165d7abccdbf21dc94e4f39b8b2dad953fdba07
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621875"
---
# New-AzApplicationGatewayBackendAddressPool

## 摘要
建立應用程式閘道的後端位址集區。

## 句法

```
New-AzApplicationGatewayBackendAddressPool -Name <String> [-BackendIPAddresses <String[]>]
 [-BackendFqdns <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## 說明
**新的 AzApplicationGatewayBackendAddressPool** Cmdlet 會建立 Azure 應用程式閘道的後端位址集區。
後端位址可以指定為 IP 位址、完全合格的功能變數名稱 (FQDN) 或 IP 配置 ID。

## 示例

### 範例1：使用後端伺服器的 FQDN 建立後端位址集區
```
PS C:\>$Pool = New-AzApplicationGatewayBackendAddressPool -Name "Pool01" -BackendFqdns "contoso1.com", "contoso2.com"
```

這個命令會使用後端伺服器的 Fqdn 建立名為 Pool01 的後端位址集區，並將它儲存在 $Pool 變數中。

### 範例2：使用後端伺服器的 IP 位址來建立後端位址集區
```
PS C:\>$Pool = New-AzApplicationGatewayBackendAddressPool -Name "Pool02" -BackendFqdns "10.10.10.10", "10.10.10.11"
```

這個命令會使用後端伺服器的 IP 位址，建立名為 Pool02 的後端位址集區，並將它儲存在 $Pool 變數中。

## 參數

### -BackendFqdns
指定此 Cmdlet 與後端伺服器池相關聯的後端 Fqdn 清單。

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

### -BackendIPAddresses
指定此 Cmdlet 與後端伺服器池相關聯的後端 IP 位址清單。

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

### -DefaultProfile
用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。

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

### -名稱
指定此 Cmdlet 建立的後端伺服器池的名稱。

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
Default value: False
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### 所有

## 輸出

### PSApplicationGatewayBackendAddressPool 中的 [.]

## 筆記

## 相關連結

[附加 AzApplicationGatewayBackendAddressPool](./Add-AzApplicationGatewayBackendAddressPool.md)

[AzApplicationGatewayBackendAddressPool](./Get-AzApplicationGatewayBackendAddressPool.md)

[移除-AzApplicationGatewayBackendAddressPool](./Remove-AzApplicationGatewayBackendAddressPool.md)

[Set-AzApplicationGatewayBackendAddressPool](./Set-AzApplicationGatewayBackendAddressPool.md)


