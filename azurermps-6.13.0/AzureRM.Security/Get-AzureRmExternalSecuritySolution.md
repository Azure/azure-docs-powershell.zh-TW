---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmExternalSecuritySolution.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmExternalSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmExternalSecuritySolution.md
ms.openlocfilehash: 4ef54651b5490161d7fc28c4a0c068f7b4a1ed76
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451767"
---
# Get-AzureRmExternalSecuritySolution

## 摘要
取得外部安全性解決方案 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

### SubscriptionScope (預設) 
```
Get-AzureRmExternalSecuritySolution [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceGroupLevelResource
```
Get-AzureRmExternalSecuritySolution -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SubscriptionLevelResource
```
Get-AzureRmExternalSecuritySolution -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ResourceId
```
Get-AzureRmExternalSecuritySolution -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 說明
取得外部安全性解決方案

## 示例

### 範例1
```powershell
PS C:\> Get-AzureRmExternalSecuritySolution
ConnectivityState : Discovered
DeviceType        : Azure Active Directory Identity Protection
DeviceVendor      : microsoft
Workspace         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/defaultresourcegroup-eus/provide
                    rs/microsoft.operationalinsights/workspaces/defaultworkspace-487bb485-b5b0-471e-9c0d-10717612f869-e
                    us
Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/defaultresourcegroup-eus/provide
                    rs/Microsoft.Security/locations/centralus/externalSecuritySolutions/aad_defaultworkspace-487bb485-b
                    5b0-471e-9c0d-10717612f869-eus
Name              : aad_defaultworkspace-487bb485-b5b0-471e-9c0d-10717612f869-eus
Kind              : AAD

ConnectivityState : Discovered
DeviceType        : Azure Active Directory Identity Protection
DeviceVendor      : microsoft
Workspace         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/defaultresourcegroup-weu/provide
                    rs/microsoft.operationalinsights/workspaces/defaultworkspace-487bb485-b5b0-471e-9c0d-10717612f869-w
                    eu
Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/defaultresourcegroup-weu/provide
                    rs/Microsoft.Security/locations/centralus/externalSecuritySolutions/aad_defaultworkspace-487bb485-b
                    5b0-471e-9c0d-10717612f869-weu
Name              : aad_defaultworkspace-487bb485-b5b0-471e-9c0d-10717612f869-weu
Kind              : AAD

ConnectivityState : Discovered
DeviceType        : Azure Active Directory Identity Protection
DeviceVendor      : microsoft
Workspace         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/mainws/providers/microsoft.opera
                    tionalinsights/workspaces/securityuserws
Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/mainws/providers/Microsoft.Secur
                    ity/locations/centralus/externalSecuritySolutions/aad_securityuserws
Name              : aad_securityuserws
Kind              : AAD

ConnectivityState : Discovered
DeviceType        : Azure Active Directory Identity Protection
DeviceVendor      : microsoft
Workspace         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/myservice1/providers/microsoft.o
                    perationalinsights/workspaces/testservicews
Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myservice1/providers/Microsoft.S
                    ecurity/locations/centralus/externalSecuritySolutions/aad_testservicews
Name              : aad_testservicews
Kind              : AAD
```

取得訂閱中的所有外部安全性解決方案

### 範例2
```powershell
PS C:\> Get-AzureRmExternalSecuritySolution -ResourceGroupName "myservice1" -Location "centralus" -Name "aad_testservicews"
ConnectivityState : Discovered
DeviceType        : Azure Active Directory Identity Protection
DeviceVendor      : microsoft
Workspace         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/myservice1/providers/microsoft.operationalinsights/workspaces/testservicews
Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myservice1/providers/Microsoft.Security/locations/centralus/externalSecuritySolutions/aad_testservicews
Name              : aad_testservicews
Kind              : AAD
```

取得特定的外部安全性解決方案

## 參數

### -DefaultProfile
用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。

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

### -位置
位於.

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource, SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -名稱
資源名稱。

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
資源組名稱。

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
[資源識別碼]。

```yaml
Type: String
Parameter Sets: ResourceId
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

### System.object

## 輸出

### PSSecurityExternalSecuritySolution 中的 ExternalSecuritySolutions （Security..。

## 筆記

## 相關連結
