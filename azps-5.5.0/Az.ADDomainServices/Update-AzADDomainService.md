---
external help file: ''
Module Name: Az.ADDomainServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.addomainservices/update-azaddomainservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/Update-AzADDomainService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/Update-AzADDomainService.md
ms.openlocfilehash: 7acebe247009c95f9d504dc09b2729eeb5aabbbc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100127307"
---
# Update-AzADDomainService

## 摘要
更新網域服務操作可用來更新現有的部署。
更新呼叫只支援修補程式本文中所列的屬性。

## 句法

### UpdateExpanded (預設) 
```
Update-AzADDomainService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DomainConfigurationType <String>] [-DomainSecuritySettingNtlmV1 <String>]
 [-DomainSecuritySettingSyncKerberosPassword <String>] [-DomainSecuritySettingSyncNtlmPassword <String>]
 [-DomainSecuritySettingSyncOnPremPassword <String>] [-DomainSecuritySettingTlsV1 <String>]
 [-FilteredSync <String>] [-ForestTrust <IForestTrust[]>] [-LdapSettingExternalAccess <String>]
 [-LdapSettingLdaps <String>] [-LdapSettingPfxCertificate <String>]
 [-LdapSettingPfxCertificatePassword <SecureString>] [-NotificationSettingAdditionalRecipient <String[]>]
 [-NotificationSettingNotifyDcAdmin <String>] [-NotificationSettingNotifyGlobalAdmin <String>]
 [-ReplicaSet <IReplicaSet[]>] [-ResourceForest <String>] [-Sku <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### UpdateViaIdentityExpanded
```
Update-AzADDomainService -InputObject <IAdDomainServicesIdentity> [-DomainConfigurationType <String>]
 [-DomainSecuritySettingNtlmV1 <String>] [-DomainSecuritySettingSyncKerberosPassword <String>]
 [-DomainSecuritySettingSyncNtlmPassword <String>] [-DomainSecuritySettingSyncOnPremPassword <String>]
 [-DomainSecuritySettingTlsV1 <String>] [-FilteredSync <String>] [-ForestTrust <IForestTrust[]>]
 [-LdapSettingExternalAccess <String>] [-LdapSettingLdaps <String>] [-LdapSettingPfxCertificate <String>]
 [-LdapSettingPfxCertificatePassword <SecureString>] [-NotificationSettingAdditionalRecipient <String[]>]
 [-NotificationSettingNotifyDcAdmin <String>] [-NotificationSettingNotifyGlobalAdmin <String>]
 [-ReplicaSet <IReplicaSet[]>] [-ResourceForest <String>] [-Sku <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## 說明
更新網域服務操作可用來更新現有的部署。
更新呼叫只支援修補程式本文中所列的屬性。

## 示例

### 範例1：依 ResourceGroupName 和 Name 更新 AzADDomainService
```powershell
PS C:\> $ADDomainSetting = New-AzADDomainServiceDomainSecuritySettingObject -TlsV1 Disabled
Update-AzADDomainService -Name youriADdomain -ResourceGroupName youriADdomain -DomainSecuritySetting $ADDomainSetting

Name          Domain Name       Location Sku
----          -----------       -------- ---
youriADdomain youriAddomain.com westus   Enterprise
```

依 ResourceGroupName 和 Name 更新 AzADDomainService

### 範例2：由 Inputobject 更新 AzADDomainService
```powershell
PS C:\> $getAzAddomain = Get-AzADDomainService -Name youriADdomain -ResourceGroupName youriADdomain
$ADDomainSetting = New-AzADDomainServiceDomainSecuritySettingObject -TlsV1 Disabled
Update-AzADDomainService -InputObject $getAzAddomain -DomainSecuritySetting $ADDomainSetting

Name          Domain Name       Location Sku
----          -----------       -------- ---
youriADdomain youriAddomain.com westus   Enterprise
```

以 Inputobject 更新 AzADDomainService

## 參數

### -AsJob
執行命令做為工作

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DomainConfigurationType
網域配置類型

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DomainSecuritySettingNtlmV1
判斷是否已啟用或停用 NtlmV1 的標誌。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DomainSecuritySettingSyncKerberosPassword
判斷是否已啟用或停用 SyncKerberosPasswords 的標誌。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DomainSecuritySettingSyncNtlmPassword
判斷是否已啟用或停用 SyncNtlmPasswords 的標誌。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DomainSecuritySettingSyncOnPremPassword
判斷是否已啟用或停用 SyncOnPremPasswords 的標誌。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DomainSecuritySettingTlsV1
判斷是否已啟用或停用 TlsV1 的標誌。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FilteredSync
啟用或停用標誌以開啟群組式篩選同步處理

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ForestTrust
要構造之資原始目錄林的設定清單，請參閱 FORESTTRUST 屬性的 [記事] 區段，然後建立雜湊表。

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.IForestTrust[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.IAdDomainServicesIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -LdapSettingExternalAccess
[標誌] 可判斷是否已啟用或停用網際網路的安全 LDAP 存取。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LdapSettingLdaps
用於判斷是否已啟用或停用 [安全 LDAP] 的標誌。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LdapSettingPfxCertificate
要設定安全 LDAP 所需的憑證。
在此傳遞的參數應該是憑證 pfx 檔案的 base64encoded 標記法。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LdapSettingPfxCertificatePassword
解密提供的安全 LDAP 憑證 pfx 檔案的密碼。

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -名稱
網域服務的名稱。

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: DomainServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NotificationSettingAdditionalRecipient
其他收件者清單

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

### -NotificationSettingNotifyDcAdmin
是否應該通知網網域控制站管理員

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NotificationSettingNotifyGlobalAdmin
系統應通知全域管理員

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoWait
以非同步方式執行命令

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReplicaSet
要構造的 ReplicaSets 清單，請參閱 REPLICASET 屬性的 [記事] 區段，然後建立雜湊表。

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.IReplicaSet[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceForest
資原始目錄林

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
使用者訂閱中資源群組的名稱。
名稱不區分大小寫。

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Sku
Sku 類型

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
取得可唯一識別 Microsoft Azure 訂閱的訂閱認證。
[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tag
資源標記

```yaml
Type: System.Collections.Hashtable
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

### IAdDomainServicesIdentity （ADDomainServices）的

## 輸出

### IDomainService （ADDomainServices）。 Api202001。

## 筆記

別名

複雜的參數屬性

若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。 如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。


FORESTTRUST <IForestTrust [] >：資原始目錄林的設定清單
  - `[FriendlyName <String>]`：易記的名稱
  - `[RemoteDnsIP <String>]`：遠端 Dns ip
  - `[TrustDirection <String>]`：信任方向
  - `[TrustPassword <String>]`：信任密碼
  - `[TrustedDomainFqdn <String>]`：受信任的網域 FQDN

INPUTOBJECT <IAdDomainServicesIdentity> ：身分識別參數
  - `[DomainServiceName <String>]`：網域服務的名稱。
  - `[Id <String>]`：資源身分識別路徑
  - `[ResourceGroupName <String>]`：使用者訂閱中資源群組的名稱。 名稱不區分大小寫。
  - `[SubscriptionId <String>]`：取得可唯一識別 Microsoft Azure 訂閱的訂閱認證。 [訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。

REPLICASET <IReplicaSet [] >： ReplicaSets 清單
  - `[Location <String>]`：虛擬網路位置
  - `[SubnetId <String>]`：將在其上部署網域服務的虛擬網路的名稱。 要在其上部署網域服務的子網之 id。 /virtualNetwork/vnetName/subnets/subnetName.

## 相關連結

