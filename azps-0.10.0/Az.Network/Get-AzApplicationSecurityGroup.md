---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationsecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationSecurityGroup.md
ms.openlocfilehash: b23901a79262f4eb63e34b99c10b82442cb2fe6a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794445"
---
# Get-AzApplicationSecurityGroup

## 摘要
取得應用程式安全性群組。

## 句法

```
Get-AzApplicationSecurityGroup [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**AzApplicationSecurityGroup** Cmdlet 會取得應用程式安全性群組。

## 示例

### 範例1：檢索所有應用程式的安全性群組。
```
PS C:\> Get-AzApplicationSecurityGroup
```

上述命令會傳回訂閱中的所有應用程式安全性群組。

### 範例2：在資源群組中取得應用程式安全性群組。
```
PS C:\> Get-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup
```

上述命令會傳回屬於資源群組 MyResourceGroup 的所有應用程式安全性群組。

### 範例3：檢索特定的應用程式安全性群組。
```
PS C:\> Get-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name MyApplicationSecurityGroup
```

上述命令會傳回 [資源] 群組 MyResourceGroup 底下的 [應用程式安全性群組 MyApplicationSecurityGroup]。

## 參數

### -DefaultProfile
用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -名稱
資源名稱。

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
資源群組的名稱。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### System.object

## 輸出

### PSApplicationSecurityGroup 中的 [.]

## 筆記

## 相關連結

[新-AzApplicationSecurityGroup](./New-AzApplicationSecurityGroup.md)

[移除-AzApplicationSecurityGroup](./Remove-AzApplicationSecurityGroup.md)

[AzNetworkSecurityRuleConfig](./Get-AzNetworkSecurityRuleConfig.md)

[AzNetworkInterfaceIpConfig](./Get-AzNetworkInterfaceIpConfig.md)
