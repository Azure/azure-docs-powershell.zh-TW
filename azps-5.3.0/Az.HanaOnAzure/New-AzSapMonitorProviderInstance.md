---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/en-us/powershell/module/az.hanaonazure/new-azsapmonitorproviderinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/New-AzSapMonitorProviderInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/New-AzSapMonitorProviderInstance.md
ms.openlocfilehash: c9ba83218e8be82716f4804444b7c52371fe764c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98438251"
---
# <span data-ttu-id="30f4c-101">New-AzSapMonitorProviderInstance</span><span class="sxs-lookup"><span data-stu-id="30f4c-101">New-AzSapMonitorProviderInstance</span></span>

## <span data-ttu-id="30f4c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="30f4c-102">SYNOPSIS</span></span>
<span data-ttu-id="30f4c-103">針對指定的訂閱、資源群組、SapMonitor 名稱和資源名稱建立提供者實例。</span><span class="sxs-lookup"><span data-stu-id="30f4c-103">Creates a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="30f4c-104">句法</span><span class="sxs-lookup"><span data-stu-id="30f4c-104">SYNTAX</span></span>

### <span data-ttu-id="30f4c-105">ByString (預設) </span><span class="sxs-lookup"><span data-stu-id="30f4c-105">ByString (Default)</span></span>
```
New-AzSapMonitorProviderInstance -Name <String> -ResourceGroupName <String> -SapMonitorName <String>
 -HanaDatabaseName <String> -HanaDatabasePassword <SecureString> -HanaDatabaseSqlPort <Int32>
 -HanaDatabaseUsername <String> -HanaHostname <String> -ProviderType <String> [-SubscriptionId <String>]
 [-Metadata <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="30f4c-106">ByDict</span><span class="sxs-lookup"><span data-stu-id="30f4c-106">ByDict</span></span>
```
New-AzSapMonitorProviderInstance -Name <String> -ResourceGroupName <String> -SapMonitorName <String>
 -InstanceProperty <Hashtable> -ProviderType <String> [-SubscriptionId <String>] [-Metadata <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="30f4c-107">ByKeyVault</span><span class="sxs-lookup"><span data-stu-id="30f4c-107">ByKeyVault</span></span>
```
New-AzSapMonitorProviderInstance -Name <String> -ResourceGroupName <String> -SapMonitorName <String>
 -HanaDatabaseName <String> -HanaDatabasePasswordKeyVaultResourceId <String>
 -HanaDatabasePasswordSecretId <String> -HanaDatabaseSqlPort <Int32> -HanaDatabaseUsername <String>
 -HanaHostname <String> -ProviderType <String> [-SubscriptionId <String>] [-Metadata <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="30f4c-108">說明</span><span class="sxs-lookup"><span data-stu-id="30f4c-108">DESCRIPTION</span></span>
<span data-ttu-id="30f4c-109">針對指定的訂閱、資源群組、SapMonitor 名稱和資源名稱建立提供者實例。</span><span class="sxs-lookup"><span data-stu-id="30f4c-109">Creates a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="30f4c-110">示例</span><span class="sxs-lookup"><span data-stu-id="30f4c-110">EXAMPLES</span></span>

### <span data-ttu-id="30f4c-111">範例1：以 HANA 字串建立 SAP 監視器的實例</span><span class="sxs-lookup"><span data-stu-id="30f4c-111">Example 1: Create an instance of SAP monitor by string for HANA</span></span>
```powershell
PS C:\> New-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -Name ps-sapmonitorins-t01 -SapMonitorName yemingmonitor -ProviderType SapHana -HanaHostname 'hdb1-0' -HanaDatabaseName 'SYSTEMDB' -HanaDatabaseSqlPort 30015 -HanaDatabaseUsername SYSTEM -HanaDatabasePassword (ConvertTo-SecureString "Manager1" -AsPlainText -Force)

Name                 Type
----                 ----
ps-sapmonitorins-t01 Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="30f4c-112">這個命令會透過 HANA 的字串建立 SAP 監視器的實例。</span><span class="sxs-lookup"><span data-stu-id="30f4c-112">This command creates an instance of SAP monitor by string for HANA.</span></span>

### <span data-ttu-id="30f4c-113">範例2：使用 HANA 的主要保存庫建立 SAP 監視器的實例</span><span class="sxs-lookup"><span data-stu-id="30f4c-113">Example 2: Create an instance of SAP monitor by key vault for HANA</span></span>
```powershell
PS C:\> New-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName sapMonitor-vayh7q-test -ProviderType SapHana -HanaHostname 'hdb1-0' -HanaDatabaseName 'SYSTEMDB' -HanaDatabaseSqlPort 30015 -HanaDatabaseUsername SYSTEM -HanaDatabasePasswordSecretId https://kv-9gosjc-test.vault.azure.net/secrets/hanaPassword/bf516d1dfcc144138e5cf55114f3344b -HanaDatabasePasswordKeyVaultResourceId /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/costmanagement-rg-8p50xe/providers/Microsoft.KeyVault/vaults/kv-9gosjc-test -Name sapins-kv-test

Name           Type
----           ----
sapins-kv-test Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="30f4c-114">這個命令會透過 HANA 的主要保存庫建立 SAP 監視器的實例。</span><span class="sxs-lookup"><span data-stu-id="30f4c-114">This command creates an instance of SAP monitor by key vault for HANA.</span></span>

### <span data-ttu-id="30f4c-115">範例3：依字典 PrometheusHaCluster 建立 SAP 監視器的實例</span><span class="sxs-lookup"><span data-stu-id="30f4c-115">Example 3: Create an instance of SAP monitor by dictionary for PrometheusHaCluster</span></span>
```powershell
PS C:\> New-AzSapMonitorProviderInstance -ResourceGroupName donaliu-HN1 -Name dolauli-instance-promclt   -SapMonitorName dolauli-test04 -ProviderType PrometheusHaCluster -InstanceProperty @{prometheusUrl='http://10.4.1.10:9664/metrics'}


Name                     Type
----                     ----
dolauli-instance-promclt Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="30f4c-116">這個命令會依 PrometheusHaCluster 的字典，建立 SAP 監視器的實例。</span><span class="sxs-lookup"><span data-stu-id="30f4c-116">This command creates an instance of SAP monitor by dictionary for PrometheusHaCluster.</span></span>

### <span data-ttu-id="30f4c-117">範例4：依字典 PrometheusOS 建立 SAP 監視器的實例</span><span class="sxs-lookup"><span data-stu-id="30f4c-117">Example 4: Create an instance of SAP monitor by dictionary for PrometheusOS</span></span>
```powershell
PS C:\> New-AzSapMonitorProviderInstance -ResourceGroupName donaliu-HN1 -Name dolauli-instance-prom   -SapMonitorName dolauli-test04 -ProviderType PrometheusOS -InstanceProperty @{prometheusUrl='http://10.3.1.6:9100/metrics'}

Name                  Type
----                  ----
dolauli-instance-prom Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="30f4c-118">這個命令會依 PrometheusOS 的字典，建立 SAP 監視器的實例。</span><span class="sxs-lookup"><span data-stu-id="30f4c-118">This command creates an instance of SAP monitor by dictionary for PrometheusOS.</span></span>

### <span data-ttu-id="30f4c-119">範例5：依字典 MsSqlServer 建立 SAP 監視器的實例</span><span class="sxs-lookup"><span data-stu-id="30f4c-119">Example 5: Create an instance of SAP monitor by dictionary for MsSqlServer</span></span>
```powershell
PS C:\> New-AzSapMonitorProviderInstance -ResourceGroupName donaliu-HN1 -Name dolauli-instance-ms   -SapMonitorName dolauli-test04 -ProviderType MsSqlServer -InstanceProperty @{sqlHostname="10.4.8.90";sqlPort=1433;sqlUsername="AMFSS";sqlPassword="fakepassword"}

Name                Type
----                ----
dolauli-instance-ms Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="30f4c-120">這個命令會依 MsSqlServer 的字典，建立 SAP 監視器的實例。</span><span class="sxs-lookup"><span data-stu-id="30f4c-120">This command creates an instance of SAP monitor by dictionary for MsSqlServer.</span></span>

### <span data-ttu-id="30f4c-121">範例6：依字典 SapHana 建立 SAP 監視器的實例</span><span class="sxs-lookup"><span data-stu-id="30f4c-121">Example 6: Create an instance of SAP monitor by dictionary for SapHana</span></span>
```powershell
PS C:\> New-AzSapMonitorProviderInstance -ResourceGroupName donaliu-HN1 -Name dolauli-instance-hana   -SapMonitorName dolauli-test04 -ProviderType SapHana -InstanceProperty @{hanaHostname="10.1.2.6";hanaDbName="SYSTEMDB";hanaDbSqlPort=30113;hanaDbUsername="SYSTEM"; hanaDbPassword="Manager1"}

Name                  Type
----                  ----
dolauli-instance-hana Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="30f4c-122">這個命令會依 SapHana 的字典，建立 SAP 監視器的實例。</span><span class="sxs-lookup"><span data-stu-id="30f4c-122">This command creates an instance of SAP monitor by dictionary for SapHana.</span></span>

## <span data-ttu-id="30f4c-123">參數</span><span class="sxs-lookup"><span data-stu-id="30f4c-123">PARAMETERS</span></span>

### <span data-ttu-id="30f4c-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="30f4c-124">-AsJob</span></span>
<span data-ttu-id="30f4c-125">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="30f4c-125">Run the command as a job</span></span>

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

### <span data-ttu-id="30f4c-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30f4c-126">-DefaultProfile</span></span>
<span data-ttu-id="30f4c-127">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="30f4c-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="30f4c-128">-HanaDatabaseName</span><span class="sxs-lookup"><span data-stu-id="30f4c-128">-HanaDatabaseName</span></span>
<span data-ttu-id="30f4c-129">SAP HANA 實例的資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="30f4c-129">The database name of SAP HANA instance.</span></span>

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

### <span data-ttu-id="30f4c-130">-HanaDatabasePassword</span><span class="sxs-lookup"><span data-stu-id="30f4c-130">-HanaDatabasePassword</span></span>
<span data-ttu-id="30f4c-131">SAP HANA 實例資料庫的密碼。</span><span class="sxs-lookup"><span data-stu-id="30f4c-131">The password of the database of SAP HANA instance.</span></span>

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

### <span data-ttu-id="30f4c-132">-HanaDatabasePasswordKeyVaultResourceId</span><span class="sxs-lookup"><span data-stu-id="30f4c-132">-HanaDatabasePasswordKeyVaultResourceId</span></span>
<span data-ttu-id="30f4c-133">包含 HANA 認證之主要電子倉庫的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="30f4c-133">Resource ID of the Key Vault that contains the HANA credentials.</span></span>

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

### <span data-ttu-id="30f4c-134">-HanaDatabasePasswordSecretId</span><span class="sxs-lookup"><span data-stu-id="30f4c-134">-HanaDatabasePasswordSecretId</span></span>
<span data-ttu-id="30f4c-135">包含 HANA 認證之主要保存庫密碼的秘密識別碼。</span><span class="sxs-lookup"><span data-stu-id="30f4c-135">Secret identifier to the Key Vault secret that contains the HANA credentials.</span></span>

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

### <span data-ttu-id="30f4c-136">-HanaDatabaseSqlPort</span><span class="sxs-lookup"><span data-stu-id="30f4c-136">-HanaDatabaseSqlPort</span></span>
<span data-ttu-id="30f4c-137">SAP HANA 實例之資料庫的 SQL 埠。</span><span class="sxs-lookup"><span data-stu-id="30f4c-137">The SQL port of the database of SAP HANA instance.</span></span>

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

### <span data-ttu-id="30f4c-138">-HanaDatabaseUsername</span><span class="sxs-lookup"><span data-stu-id="30f4c-138">-HanaDatabaseUsername</span></span>
<span data-ttu-id="30f4c-139">SAP HANA 實例之資料庫的使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="30f4c-139">The username of the database of SAP HANA instance.</span></span>

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

### <span data-ttu-id="30f4c-140">-HanaHostname</span><span class="sxs-lookup"><span data-stu-id="30f4c-140">-HanaHostname</span></span>
<span data-ttu-id="30f4c-141">SAP HANA 實例的主機名稱。</span><span class="sxs-lookup"><span data-stu-id="30f4c-141">The hostname of SAP HANA instance.</span></span>

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

### <span data-ttu-id="30f4c-142">-InstanceProperty</span><span class="sxs-lookup"><span data-stu-id="30f4c-142">-InstanceProperty</span></span>
<span data-ttu-id="30f4c-143">HANA 實例的屬性。</span><span class="sxs-lookup"><span data-stu-id="30f4c-143">The property of HANA instance.</span></span>

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

### <span data-ttu-id="30f4c-144">-中繼資料</span><span class="sxs-lookup"><span data-stu-id="30f4c-144">-Metadata</span></span>
<span data-ttu-id="30f4c-145">包含提供者實例之中繼資料的 JSON 字串。</span><span class="sxs-lookup"><span data-stu-id="30f4c-145">A JSON string containing metadata of the provider instance.</span></span>

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

### <span data-ttu-id="30f4c-146">-名稱</span><span class="sxs-lookup"><span data-stu-id="30f4c-146">-Name</span></span>
<span data-ttu-id="30f4c-147">提供者實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="30f4c-147">Name of the provider instance.</span></span>

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

### <span data-ttu-id="30f4c-148">-NoWait</span><span class="sxs-lookup"><span data-stu-id="30f4c-148">-NoWait</span></span>
<span data-ttu-id="30f4c-149">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="30f4c-149">Run the command asynchronously</span></span>

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

### <span data-ttu-id="30f4c-150">-ProviderType</span><span class="sxs-lookup"><span data-stu-id="30f4c-150">-ProviderType</span></span>
<span data-ttu-id="30f4c-151">提供者實例的類型。</span><span class="sxs-lookup"><span data-stu-id="30f4c-151">The type of provider instance.</span></span>
<span data-ttu-id="30f4c-152">支援的值為： "SapHana"。</span><span class="sxs-lookup"><span data-stu-id="30f4c-152">Supported values are: "SapHana".</span></span>

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

### <span data-ttu-id="30f4c-153">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30f4c-153">-ResourceGroupName</span></span>
<span data-ttu-id="30f4c-154">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="30f4c-154">Name of the resource group.</span></span>

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

### <span data-ttu-id="30f4c-155">-SapMonitorName</span><span class="sxs-lookup"><span data-stu-id="30f4c-155">-SapMonitorName</span></span>
<span data-ttu-id="30f4c-156">SAP 監視資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="30f4c-156">Name of the SAP monitor resource.</span></span>

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

### <span data-ttu-id="30f4c-157">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="30f4c-157">-SubscriptionId</span></span>
<span data-ttu-id="30f4c-158">訂閱識別碼，可唯一識別 Microsoft Azure 訂閱。</span><span class="sxs-lookup"><span data-stu-id="30f4c-158">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="30f4c-159">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="30f4c-159">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="30f4c-160">-確認</span><span class="sxs-lookup"><span data-stu-id="30f4c-160">-Confirm</span></span>
<span data-ttu-id="30f4c-161">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="30f4c-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30f4c-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30f4c-162">-WhatIf</span></span>
<span data-ttu-id="30f4c-163">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="30f4c-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="30f4c-164">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="30f4c-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30f4c-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30f4c-165">CommonParameters</span></span>
<span data-ttu-id="30f4c-166">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="30f4c-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30f4c-167">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="30f4c-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30f4c-168">輸入</span><span class="sxs-lookup"><span data-stu-id="30f4c-168">INPUTS</span></span>

## <span data-ttu-id="30f4c-169">輸出</span><span class="sxs-lookup"><span data-stu-id="30f4c-169">OUTPUTS</span></span>

### <span data-ttu-id="30f4c-170">IProviderInstance （HanaOnAzure）。 Api20200207Preview。</span><span class="sxs-lookup"><span data-stu-id="30f4c-170">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.IProviderInstance</span></span>

## <span data-ttu-id="30f4c-171">筆記</span><span class="sxs-lookup"><span data-stu-id="30f4c-171">NOTES</span></span>

<span data-ttu-id="30f4c-172">別名</span><span class="sxs-lookup"><span data-stu-id="30f4c-172">ALIASES</span></span>

## <span data-ttu-id="30f4c-173">相關連結</span><span class="sxs-lookup"><span data-stu-id="30f4c-173">RELATED LINKS</span></span>

