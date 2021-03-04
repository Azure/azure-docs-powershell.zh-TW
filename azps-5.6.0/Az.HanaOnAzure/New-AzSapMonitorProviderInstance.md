---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/powershell/module/az.hanaonazure/new-azsapmonitorproviderinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/New-AzSapMonitorProviderInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/New-AzSapMonitorProviderInstance.md
ms.openlocfilehash: eb84936310be355ece858884a1e27b7cc954cb51
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917261"
---
# New-AzSapMonitorProviderInstance

## 簡介
為指定的訂閱、資源群組、SapMonitor 名稱和資源名稱建立提供者實例。

## 語法

### ByString (預設) 
```
New-AzSapMonitorProviderInstance -Name <String> -ResourceGroupName <String> -SapMonitorName <String>
 -HanaDatabaseName <String> -HanaDatabasePassword <SecureString> -HanaDatabaseSqlPort <Int32>
 -HanaDatabaseUsername <String> -HanaHostname <String> -ProviderType <String> [-SubscriptionId <String>]
 [-Metadata <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### ByDict
```
New-AzSapMonitorProviderInstance -Name <String> -ResourceGroupName <String> -SapMonitorName <String>
 -InstanceProperty <Hashtable> -ProviderType <String> [-SubscriptionId <String>] [-Metadata <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### ByKeyVault
```
New-AzSapMonitorProviderInstance -Name <String> -ResourceGroupName <String> -SapMonitorName <String>
 -HanaDatabaseName <String> -HanaDatabasePasswordKeyVaultResourceId <String>
 -HanaDatabasePasswordSecretId <String> -HanaDatabaseSqlPort <Int32> -HanaDatabaseUsername <String>
 -HanaHostname <String> -ProviderType <String> [-SubscriptionId <String>] [-Metadata <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## 描述
為指定的訂閱、資源群組、SapMonitor 名稱和資源名稱建立提供者實例。

## 例子

### 範例 1：針對 HANA 建立 SAP 監視器的字串實例
```powershell
PS C:\> New-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -Name ps-sapmonitorins-t01 -SapMonitorName yemingmonitor -ProviderType SapHana -HanaHostname 'hdb1-0' -HanaDatabaseName 'SYSTEMDB' -HanaDatabaseSqlPort 30015 -HanaDatabaseUsername SYSTEM -HanaDatabasePassword (ConvertTo-SecureString "Manager1" -AsPlainText -Force)

Name                 Type
----                 ----
ps-sapmonitorins-t01 Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

此命令會針對 HANA 字串建立 SAP 監視器實例。

### 範例 2：針對 HANA 建立按金鑰庫的 SAP 監視器實例
```powershell
PS C:\> New-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName sapMonitor-vayh7q-test -ProviderType SapHana -HanaHostname 'hdb1-0' -HanaDatabaseName 'SYSTEMDB' -HanaDatabaseSqlPort 30015 -HanaDatabaseUsername SYSTEM -HanaDatabasePasswordSecretId https://kv-9gosjc-test.vault.azure.net/secrets/hanaPassword/bf516d1dfcc144138e5cf55114f3344b -HanaDatabasePasswordKeyVaultResourceId /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/costmanagement-rg-8p50xe/providers/Microsoft.KeyVault/vaults/kv-9gosjc-test -Name sapins-kv-test

Name           Type
----           ----
sapins-kv-test Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

此命令會針對 HANA 建立按金鑰庫的 SAP 監視器實例。

### 範例 3：建立 PrometheusHaCluster 字典的 SAP 監視器實例
```powershell
PS C:\> New-AzSapMonitorProviderInstance -ResourceGroupName donaliu-HN1 -Name dolauli-instance-promclt   -SapMonitorName dolauli-test04 -ProviderType PrometheusHaCluster -InstanceProperty @{prometheusUrl='http://10.4.1.10:9664/metrics'}


Name                     Type
----                     ----
dolauli-instance-promclt Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

此命令會以 PrometheusHaCluster 字典建立 SAP 監視器實例。

### 範例 4：建立 PrometheusOS 字典的 SAP 監視器實例
```powershell
PS C:\> New-AzSapMonitorProviderInstance -ResourceGroupName donaliu-HN1 -Name dolauli-instance-prom   -SapMonitorName dolauli-test04 -ProviderType PrometheusOS -InstanceProperty @{prometheusUrl='http://10.3.1.6:9100/metrics'}

Name                  Type
----                  ----
dolauli-instance-prom Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

此命令會針對 PrometheusOS 字典建立 SAP 監視器實例。

### 範例 5：建立 MsSqlServer 的 SAP 監視器字典實例
```powershell
PS C:\> New-AzSapMonitorProviderInstance -ResourceGroupName donaliu-HN1 -Name dolauli-instance-ms   -SapMonitorName dolauli-test04 -ProviderType MsSqlServer -InstanceProperty @{sqlHostname="10.4.8.90";sqlPort=1433;sqlUsername="AMFSS";sqlPassword="fakepassword"}

Name                Type
----                ----
dolauli-instance-ms Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

此命令會針對 MsSqlServer 建立以字典顯示 SAP 監視器的實例。

### 範例 6：為 SapHana 建立 SapHana 字典的 SAP 監視器實例
```powershell
PS C:\> New-AzSapMonitorProviderInstance -ResourceGroupName donaliu-HN1 -Name dolauli-instance-hana   -SapMonitorName dolauli-test04 -ProviderType SapHana -InstanceProperty @{hanaHostname="10.1.2.6";hanaDbName="SYSTEMDB";hanaDbSqlPort=30113;hanaDbUsername="SYSTEM"; hanaDbPassword="Manager1"}

Name                  Type
----                  ----
dolauli-instance-hana Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

此命令會建立 SapHana 字典中的 SAP 監視器實例。

## 參數

### -AsJob
以工作執行命令

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
用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。

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

### -HanaDatabaseName
SAP HANA 實例的資料庫名稱。

```yaml
Type: System.String
Parameter Sets: ByKeyVault, ByString
Aliases: HanaDbName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HanaDatabasePassword
SAP HANA 實例資料庫的密碼。

```yaml
Type: System.Security.SecureString
Parameter Sets: ByString
Aliases: HanaDbPassword

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HanaDatabasePasswordKeyVaultResourceId
包含 HANA 認證之金鑰保存庫的資源識別碼。

```yaml
Type: System.String
Parameter Sets: ByKeyVault
Aliases: HanaDbPasswordKeyVaultId, KeyVaultId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HanaDatabasePasswordSecretId
包含 HANA 認證之金鑰保存庫機密的機密識別碼。

```yaml
Type: System.String
Parameter Sets: ByKeyVault
Aliases: HanaDbPasswordSecretId, SecretId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HanaDatabaseSqlPort
SAP HANA 實例資料庫的 SQL 埠。

```yaml
Type: System.Int32
Parameter Sets: ByKeyVault, ByString
Aliases: HanaDbSqlPort

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HanaDatabaseUsername
SAP HANA 實例資料庫使用者名稱。

```yaml
Type: System.String
Parameter Sets: ByKeyVault, ByString
Aliases: HanaDbUsername

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HanaHostname
SAP HANA 實例的主機名稱。

```yaml
Type: System.String
Parameter Sets: ByKeyVault, ByString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InstanceProperty
HANA 實例的屬性。

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByDict
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -中繼資料
包含提供者實例中繼資料的 JSON 字串。

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

### -名稱
提供者實例的名稱。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ProviderInstanceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoWait
非同步執行命令

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

### -ProviderType
提供者實例的類型。
支援的值為：「SapHana」。

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

### -ResourceGroupName
資源組的名稱。

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

### -SapMonitorName
SAP 監視器資源的名稱。

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

### -SubscriptionId
可唯一識別 Microsoft Azure 訂閱的訂閱識別碼。
訂閱識別碼會構成每個服務通話 URI 的一部分。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### -確認
執行 Cmdlet 之前，提示您確認。

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
顯示 Cmdlet 執行時會發生什麼情況。
不會執行 Cmdlet。

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
此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。 詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)

## 輸入

## 輸出

### Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.models.Api20200207Preview.IProviderInstance

## 筆記

別名

## 相關連結

