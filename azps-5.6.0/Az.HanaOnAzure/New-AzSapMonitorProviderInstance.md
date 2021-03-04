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
# <span data-ttu-id="98a22-101">New-AzSapMonitorProviderInstance</span><span class="sxs-lookup"><span data-stu-id="98a22-101">New-AzSapMonitorProviderInstance</span></span>

## <span data-ttu-id="98a22-102">簡介</span><span class="sxs-lookup"><span data-stu-id="98a22-102">SYNOPSIS</span></span>
<span data-ttu-id="98a22-103">為指定的訂閱、資源群組、SapMonitor 名稱和資源名稱建立提供者實例。</span><span class="sxs-lookup"><span data-stu-id="98a22-103">Creates a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="98a22-104">語法</span><span class="sxs-lookup"><span data-stu-id="98a22-104">SYNTAX</span></span>

### <span data-ttu-id="98a22-105">ByString (預設) </span><span class="sxs-lookup"><span data-stu-id="98a22-105">ByString (Default)</span></span>
```
New-AzSapMonitorProviderInstance -Name <String> -ResourceGroupName <String> -SapMonitorName <String>
 -HanaDatabaseName <String> -HanaDatabasePassword <SecureString> -HanaDatabaseSqlPort <Int32>
 -HanaDatabaseUsername <String> -HanaHostname <String> -ProviderType <String> [-SubscriptionId <String>]
 [-Metadata <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="98a22-106">ByDict</span><span class="sxs-lookup"><span data-stu-id="98a22-106">ByDict</span></span>
```
New-AzSapMonitorProviderInstance -Name <String> -ResourceGroupName <String> -SapMonitorName <String>
 -InstanceProperty <Hashtable> -ProviderType <String> [-SubscriptionId <String>] [-Metadata <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="98a22-107">ByKeyVault</span><span class="sxs-lookup"><span data-stu-id="98a22-107">ByKeyVault</span></span>
```
New-AzSapMonitorProviderInstance -Name <String> -ResourceGroupName <String> -SapMonitorName <String>
 -HanaDatabaseName <String> -HanaDatabasePasswordKeyVaultResourceId <String>
 -HanaDatabasePasswordSecretId <String> -HanaDatabaseSqlPort <Int32> -HanaDatabaseUsername <String>
 -HanaHostname <String> -ProviderType <String> [-SubscriptionId <String>] [-Metadata <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="98a22-108">描述</span><span class="sxs-lookup"><span data-stu-id="98a22-108">DESCRIPTION</span></span>
<span data-ttu-id="98a22-109">為指定的訂閱、資源群組、SapMonitor 名稱和資源名稱建立提供者實例。</span><span class="sxs-lookup"><span data-stu-id="98a22-109">Creates a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="98a22-110">例子</span><span class="sxs-lookup"><span data-stu-id="98a22-110">EXAMPLES</span></span>

### <span data-ttu-id="98a22-111">範例 1：針對 HANA 建立 SAP 監視器的字串實例</span><span class="sxs-lookup"><span data-stu-id="98a22-111">Example 1: Create an instance of SAP monitor by string for HANA</span></span>
```powershell
PS C:\> New-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -Name ps-sapmonitorins-t01 -SapMonitorName yemingmonitor -ProviderType SapHana -HanaHostname 'hdb1-0' -HanaDatabaseName 'SYSTEMDB' -HanaDatabaseSqlPort 30015 -HanaDatabaseUsername SYSTEM -HanaDatabasePassword (ConvertTo-SecureString "Manager1" -AsPlainText -Force)

Name                 Type
----                 ----
ps-sapmonitorins-t01 Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="98a22-112">此命令會針對 HANA 字串建立 SAP 監視器實例。</span><span class="sxs-lookup"><span data-stu-id="98a22-112">This command creates an instance of SAP monitor by string for HANA.</span></span>

### <span data-ttu-id="98a22-113">範例 2：針對 HANA 建立按金鑰庫的 SAP 監視器實例</span><span class="sxs-lookup"><span data-stu-id="98a22-113">Example 2: Create an instance of SAP monitor by key vault for HANA</span></span>
```powershell
PS C:\> New-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName sapMonitor-vayh7q-test -ProviderType SapHana -HanaHostname 'hdb1-0' -HanaDatabaseName 'SYSTEMDB' -HanaDatabaseSqlPort 30015 -HanaDatabaseUsername SYSTEM -HanaDatabasePasswordSecretId https://kv-9gosjc-test.vault.azure.net/secrets/hanaPassword/bf516d1dfcc144138e5cf55114f3344b -HanaDatabasePasswordKeyVaultResourceId /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/costmanagement-rg-8p50xe/providers/Microsoft.KeyVault/vaults/kv-9gosjc-test -Name sapins-kv-test

Name           Type
----           ----
sapins-kv-test Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="98a22-114">此命令會針對 HANA 建立按金鑰庫的 SAP 監視器實例。</span><span class="sxs-lookup"><span data-stu-id="98a22-114">This command creates an instance of SAP monitor by key vault for HANA.</span></span>

### <span data-ttu-id="98a22-115">範例 3：建立 PrometheusHaCluster 字典的 SAP 監視器實例</span><span class="sxs-lookup"><span data-stu-id="98a22-115">Example 3: Create an instance of SAP monitor by dictionary for PrometheusHaCluster</span></span>
```powershell
PS C:\> New-AzSapMonitorProviderInstance -ResourceGroupName donaliu-HN1 -Name dolauli-instance-promclt   -SapMonitorName dolauli-test04 -ProviderType PrometheusHaCluster -InstanceProperty @{prometheusUrl='http://10.4.1.10:9664/metrics'}


Name                     Type
----                     ----
dolauli-instance-promclt Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="98a22-116">此命令會以 PrometheusHaCluster 字典建立 SAP 監視器實例。</span><span class="sxs-lookup"><span data-stu-id="98a22-116">This command creates an instance of SAP monitor by dictionary for PrometheusHaCluster.</span></span>

### <span data-ttu-id="98a22-117">範例 4：建立 PrometheusOS 字典的 SAP 監視器實例</span><span class="sxs-lookup"><span data-stu-id="98a22-117">Example 4: Create an instance of SAP monitor by dictionary for PrometheusOS</span></span>
```powershell
PS C:\> New-AzSapMonitorProviderInstance -ResourceGroupName donaliu-HN1 -Name dolauli-instance-prom   -SapMonitorName dolauli-test04 -ProviderType PrometheusOS -InstanceProperty @{prometheusUrl='http://10.3.1.6:9100/metrics'}

Name                  Type
----                  ----
dolauli-instance-prom Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="98a22-118">此命令會針對 PrometheusOS 字典建立 SAP 監視器實例。</span><span class="sxs-lookup"><span data-stu-id="98a22-118">This command creates an instance of SAP monitor by dictionary for PrometheusOS.</span></span>

### <span data-ttu-id="98a22-119">範例 5：建立 MsSqlServer 的 SAP 監視器字典實例</span><span class="sxs-lookup"><span data-stu-id="98a22-119">Example 5: Create an instance of SAP monitor by dictionary for MsSqlServer</span></span>
```powershell
PS C:\> New-AzSapMonitorProviderInstance -ResourceGroupName donaliu-HN1 -Name dolauli-instance-ms   -SapMonitorName dolauli-test04 -ProviderType MsSqlServer -InstanceProperty @{sqlHostname="10.4.8.90";sqlPort=1433;sqlUsername="AMFSS";sqlPassword="fakepassword"}

Name                Type
----                ----
dolauli-instance-ms Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="98a22-120">此命令會針對 MsSqlServer 建立以字典顯示 SAP 監視器的實例。</span><span class="sxs-lookup"><span data-stu-id="98a22-120">This command creates an instance of SAP monitor by dictionary for MsSqlServer.</span></span>

### <span data-ttu-id="98a22-121">範例 6：為 SapHana 建立 SapHana 字典的 SAP 監視器實例</span><span class="sxs-lookup"><span data-stu-id="98a22-121">Example 6: Create an instance of SAP monitor by dictionary for SapHana</span></span>
```powershell
PS C:\> New-AzSapMonitorProviderInstance -ResourceGroupName donaliu-HN1 -Name dolauli-instance-hana   -SapMonitorName dolauli-test04 -ProviderType SapHana -InstanceProperty @{hanaHostname="10.1.2.6";hanaDbName="SYSTEMDB";hanaDbSqlPort=30113;hanaDbUsername="SYSTEM"; hanaDbPassword="Manager1"}

Name                  Type
----                  ----
dolauli-instance-hana Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="98a22-122">此命令會建立 SapHana 字典中的 SAP 監視器實例。</span><span class="sxs-lookup"><span data-stu-id="98a22-122">This command creates an instance of SAP monitor by dictionary for SapHana.</span></span>

## <span data-ttu-id="98a22-123">參數</span><span class="sxs-lookup"><span data-stu-id="98a22-123">PARAMETERS</span></span>

### <span data-ttu-id="98a22-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="98a22-124">-AsJob</span></span>
<span data-ttu-id="98a22-125">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="98a22-125">Run the command as a job</span></span>

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

### <span data-ttu-id="98a22-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98a22-126">-DefaultProfile</span></span>
<span data-ttu-id="98a22-127">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="98a22-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="98a22-128">-HanaDatabaseName</span><span class="sxs-lookup"><span data-stu-id="98a22-128">-HanaDatabaseName</span></span>
<span data-ttu-id="98a22-129">SAP HANA 實例的資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="98a22-129">The database name of SAP HANA instance.</span></span>

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

### <span data-ttu-id="98a22-130">-HanaDatabasePassword</span><span class="sxs-lookup"><span data-stu-id="98a22-130">-HanaDatabasePassword</span></span>
<span data-ttu-id="98a22-131">SAP HANA 實例資料庫的密碼。</span><span class="sxs-lookup"><span data-stu-id="98a22-131">The password of the database of SAP HANA instance.</span></span>

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

### <span data-ttu-id="98a22-132">-HanaDatabasePasswordKeyVaultResourceId</span><span class="sxs-lookup"><span data-stu-id="98a22-132">-HanaDatabasePasswordKeyVaultResourceId</span></span>
<span data-ttu-id="98a22-133">包含 HANA 認證之金鑰保存庫的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="98a22-133">Resource ID of the Key Vault that contains the HANA credentials.</span></span>

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

### <span data-ttu-id="98a22-134">-HanaDatabasePasswordSecretId</span><span class="sxs-lookup"><span data-stu-id="98a22-134">-HanaDatabasePasswordSecretId</span></span>
<span data-ttu-id="98a22-135">包含 HANA 認證之金鑰保存庫機密的機密識別碼。</span><span class="sxs-lookup"><span data-stu-id="98a22-135">Secret identifier to the Key Vault secret that contains the HANA credentials.</span></span>

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

### <span data-ttu-id="98a22-136">-HanaDatabaseSqlPort</span><span class="sxs-lookup"><span data-stu-id="98a22-136">-HanaDatabaseSqlPort</span></span>
<span data-ttu-id="98a22-137">SAP HANA 實例資料庫的 SQL 埠。</span><span class="sxs-lookup"><span data-stu-id="98a22-137">The SQL port of the database of SAP HANA instance.</span></span>

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

### <span data-ttu-id="98a22-138">-HanaDatabaseUsername</span><span class="sxs-lookup"><span data-stu-id="98a22-138">-HanaDatabaseUsername</span></span>
<span data-ttu-id="98a22-139">SAP HANA 實例資料庫使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="98a22-139">The username of the database of SAP HANA instance.</span></span>

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

### <span data-ttu-id="98a22-140">-HanaHostname</span><span class="sxs-lookup"><span data-stu-id="98a22-140">-HanaHostname</span></span>
<span data-ttu-id="98a22-141">SAP HANA 實例的主機名稱。</span><span class="sxs-lookup"><span data-stu-id="98a22-141">The hostname of SAP HANA instance.</span></span>

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

### <span data-ttu-id="98a22-142">-InstanceProperty</span><span class="sxs-lookup"><span data-stu-id="98a22-142">-InstanceProperty</span></span>
<span data-ttu-id="98a22-143">HANA 實例的屬性。</span><span class="sxs-lookup"><span data-stu-id="98a22-143">The property of HANA instance.</span></span>

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

### <span data-ttu-id="98a22-144">-中繼資料</span><span class="sxs-lookup"><span data-stu-id="98a22-144">-Metadata</span></span>
<span data-ttu-id="98a22-145">包含提供者實例中繼資料的 JSON 字串。</span><span class="sxs-lookup"><span data-stu-id="98a22-145">A JSON string containing metadata of the provider instance.</span></span>

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

### <span data-ttu-id="98a22-146">-名稱</span><span class="sxs-lookup"><span data-stu-id="98a22-146">-Name</span></span>
<span data-ttu-id="98a22-147">提供者實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="98a22-147">Name of the provider instance.</span></span>

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

### <span data-ttu-id="98a22-148">-NoWait</span><span class="sxs-lookup"><span data-stu-id="98a22-148">-NoWait</span></span>
<span data-ttu-id="98a22-149">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="98a22-149">Run the command asynchronously</span></span>

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

### <span data-ttu-id="98a22-150">-ProviderType</span><span class="sxs-lookup"><span data-stu-id="98a22-150">-ProviderType</span></span>
<span data-ttu-id="98a22-151">提供者實例的類型。</span><span class="sxs-lookup"><span data-stu-id="98a22-151">The type of provider instance.</span></span>
<span data-ttu-id="98a22-152">支援的值為：「SapHana」。</span><span class="sxs-lookup"><span data-stu-id="98a22-152">Supported values are: "SapHana".</span></span>

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

### <span data-ttu-id="98a22-153">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98a22-153">-ResourceGroupName</span></span>
<span data-ttu-id="98a22-154">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="98a22-154">Name of the resource group.</span></span>

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

### <span data-ttu-id="98a22-155">-SapMonitorName</span><span class="sxs-lookup"><span data-stu-id="98a22-155">-SapMonitorName</span></span>
<span data-ttu-id="98a22-156">SAP 監視器資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="98a22-156">Name of the SAP monitor resource.</span></span>

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

### <span data-ttu-id="98a22-157">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="98a22-157">-SubscriptionId</span></span>
<span data-ttu-id="98a22-158">可唯一識別 Microsoft Azure 訂閱的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="98a22-158">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="98a22-159">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="98a22-159">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="98a22-160">-確認</span><span class="sxs-lookup"><span data-stu-id="98a22-160">-Confirm</span></span>
<span data-ttu-id="98a22-161">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="98a22-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98a22-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98a22-162">-WhatIf</span></span>
<span data-ttu-id="98a22-163">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="98a22-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="98a22-164">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="98a22-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98a22-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98a22-165">CommonParameters</span></span>
<span data-ttu-id="98a22-166">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="98a22-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98a22-167">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="98a22-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98a22-168">輸入</span><span class="sxs-lookup"><span data-stu-id="98a22-168">INPUTS</span></span>

## <span data-ttu-id="98a22-169">輸出</span><span class="sxs-lookup"><span data-stu-id="98a22-169">OUTPUTS</span></span>

### <span data-ttu-id="98a22-170">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.models.Api20200207Preview.IProviderInstance</span><span class="sxs-lookup"><span data-stu-id="98a22-170">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.IProviderInstance</span></span>

## <span data-ttu-id="98a22-171">筆記</span><span class="sxs-lookup"><span data-stu-id="98a22-171">NOTES</span></span>

<span data-ttu-id="98a22-172">別名</span><span class="sxs-lookup"><span data-stu-id="98a22-172">ALIASES</span></span>

## <span data-ttu-id="98a22-173">相關連結</span><span class="sxs-lookup"><span data-stu-id="98a22-173">RELATED LINKS</span></span>

