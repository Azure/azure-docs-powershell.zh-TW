---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/en-us/powershell/module/az.hanaonazure/new-azsapmonitorproviderinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/New-AzSapMonitorProviderInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/New-AzSapMonitorProviderInstance.md
ms.openlocfilehash: f0d8486bc26043ee4f2cb2126c7ffdc64829a7cd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94136786"
---
# <span data-ttu-id="6725b-101">New-AzSapMonitorProviderInstance</span><span class="sxs-lookup"><span data-stu-id="6725b-101">New-AzSapMonitorProviderInstance</span></span>

## <span data-ttu-id="6725b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6725b-102">SYNOPSIS</span></span>
<span data-ttu-id="6725b-103">針對指定的訂閱、資源群組、SapMonitor 名稱和資源名稱建立提供者實例。</span><span class="sxs-lookup"><span data-stu-id="6725b-103">Creates a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="6725b-104">句法</span><span class="sxs-lookup"><span data-stu-id="6725b-104">SYNTAX</span></span>

### <span data-ttu-id="6725b-105">ByString (預設) </span><span class="sxs-lookup"><span data-stu-id="6725b-105">ByString (Default)</span></span>
```
New-AzSapMonitorProviderInstance -Name <String> -ResourceGroupName <String> -SapMonitorName <String>
 -HanaDatabaseName <String> -HanaDatabasePassword <SecureString> -HanaDatabaseSqlPort <Int32>
 -HanaDatabaseUsername <String> -HanaHostname <String> -ProviderType <String> [-SubscriptionId <String>]
 [-Metadata <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="6725b-106">ByKeyVault</span><span class="sxs-lookup"><span data-stu-id="6725b-106">ByKeyVault</span></span>
```
New-AzSapMonitorProviderInstance -Name <String> -ResourceGroupName <String> -SapMonitorName <String>
 -HanaDatabaseName <String> -HanaDatabasePasswordKeyVaultResourceId <String>
 -HanaDatabasePasswordSecretId <String> -HanaDatabaseSqlPort <Int32> -HanaDatabaseUsername <String>
 -HanaHostname <String> -ProviderType <String> [-SubscriptionId <String>] [-Metadata <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6725b-107">說明</span><span class="sxs-lookup"><span data-stu-id="6725b-107">DESCRIPTION</span></span>
<span data-ttu-id="6725b-108">針對指定的訂閱、資源群組、SapMonitor 名稱和資源名稱建立提供者實例。</span><span class="sxs-lookup"><span data-stu-id="6725b-108">Creates a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="6725b-109">示例</span><span class="sxs-lookup"><span data-stu-id="6725b-109">EXAMPLES</span></span>

### <span data-ttu-id="6725b-110">範例1：以 HANA 字串建立 SAP 監視器的實例</span><span class="sxs-lookup"><span data-stu-id="6725b-110">Example 1: Create an instance of SAP monitor by string for HANA</span></span>
```powershell
PS C:\> New-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -Name ps-sapmonitorins-t01 -SapMonitorName yemingmonitor -ProviderType SapHana -HanaHostname 'hdb1-0' -HanaDatabaseName 'SYSTEMDB' -HanaDatabaseSqlPort 30015 -HanaDatabaseUsername SYSTEM -HanaDatabasePassword (ConvertTo-SecureString "Manager1" -AsPlainText -Force)

Name                 Type
----                 ----
ps-sapmonitorins-t01 Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="6725b-111">這個命令會透過 HANA 的字串建立 SAP 監視器的實例。</span><span class="sxs-lookup"><span data-stu-id="6725b-111">This command creates an instance of SAP monitor by string for HANA.</span></span>

### <span data-ttu-id="6725b-112">範例2：使用 HANA 的主要保存庫建立 SAP 監視器的實例</span><span class="sxs-lookup"><span data-stu-id="6725b-112">Example 2: Create an instance of SAP monitor by key vault for HANA</span></span>
```powershell
PS C:\> New-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName sapMonitor-vayh7q-test -ProviderType SapHana -HanaHostname 'hdb1-0' -HanaDatabaseName 'SYSTEMDB' -HanaDatabaseSqlPort 30015 -HanaDatabaseUsername SYSTEM -HanaDatabasePasswordSecretId https://kv-9gosjc-test.vault.azure.net/secrets/hanaPassword/bf516d1dfcc144138e5cf55114f3344b -HanaDatabasePasswordKeyVaultResourceId /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/costmanagement-rg-8p50xe/providers/Microsoft.KeyVault/vaults/kv-9gosjc-test -Name sapins-kv-test

Name           Type
----           ----
sapins-kv-test Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="6725b-113">這個命令會透過 HANA 的主要保存庫建立 SAP 監視器的實例。</span><span class="sxs-lookup"><span data-stu-id="6725b-113">This command creates an instance of SAP monitor by key vault for HANA.</span></span>

## <span data-ttu-id="6725b-114">參數</span><span class="sxs-lookup"><span data-stu-id="6725b-114">PARAMETERS</span></span>

### <span data-ttu-id="6725b-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6725b-115">-AsJob</span></span>
<span data-ttu-id="6725b-116">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="6725b-116">Run the command as a job</span></span>

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

### <span data-ttu-id="6725b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6725b-117">-DefaultProfile</span></span>
<span data-ttu-id="6725b-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6725b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6725b-119">-HanaDatabaseName</span><span class="sxs-lookup"><span data-stu-id="6725b-119">-HanaDatabaseName</span></span>
<span data-ttu-id="6725b-120">SAP HANA 實例的資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="6725b-120">The database name of SAP HANA instance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HanaDbName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6725b-121">-HanaDatabasePassword</span><span class="sxs-lookup"><span data-stu-id="6725b-121">-HanaDatabasePassword</span></span>
<span data-ttu-id="6725b-122">SAP HANA 實例資料庫的密碼。</span><span class="sxs-lookup"><span data-stu-id="6725b-122">The password of the database of SAP HANA instance.</span></span>

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

### <span data-ttu-id="6725b-123">-HanaDatabasePasswordKeyVaultResourceId</span><span class="sxs-lookup"><span data-stu-id="6725b-123">-HanaDatabasePasswordKeyVaultResourceId</span></span>
<span data-ttu-id="6725b-124">包含 HANA 認證之主要電子倉庫的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="6725b-124">Resource ID of the Key Vault that contains the HANA credentials.</span></span>

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

### <span data-ttu-id="6725b-125">-HanaDatabasePasswordSecretId</span><span class="sxs-lookup"><span data-stu-id="6725b-125">-HanaDatabasePasswordSecretId</span></span>
<span data-ttu-id="6725b-126">包含 HANA 認證之主要保存庫密碼的秘密識別碼。</span><span class="sxs-lookup"><span data-stu-id="6725b-126">Secret identifier to the Key Vault secret that contains the HANA credentials.</span></span>

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

### <span data-ttu-id="6725b-127">-HanaDatabaseSqlPort</span><span class="sxs-lookup"><span data-stu-id="6725b-127">-HanaDatabaseSqlPort</span></span>
<span data-ttu-id="6725b-128">SAP HANA 實例之資料庫的 SQL 埠。</span><span class="sxs-lookup"><span data-stu-id="6725b-128">The SQL port of the database of SAP HANA instance.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: HanaDbSqlPort

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6725b-129">-HanaDatabaseUsername</span><span class="sxs-lookup"><span data-stu-id="6725b-129">-HanaDatabaseUsername</span></span>
<span data-ttu-id="6725b-130">SAP HANA 實例之資料庫的使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="6725b-130">The username of the database of SAP HANA instance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HanaDbUsername

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6725b-131">-HanaHostname</span><span class="sxs-lookup"><span data-stu-id="6725b-131">-HanaHostname</span></span>
<span data-ttu-id="6725b-132">SAP HANA 實例的主機名稱。</span><span class="sxs-lookup"><span data-stu-id="6725b-132">The hostname of SAP HANA instance.</span></span>

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

### <span data-ttu-id="6725b-133">-中繼資料</span><span class="sxs-lookup"><span data-stu-id="6725b-133">-Metadata</span></span>
<span data-ttu-id="6725b-134">包含提供者實例之中繼資料的 JSON 字串。</span><span class="sxs-lookup"><span data-stu-id="6725b-134">A JSON string containing metadata of the provider instance.</span></span>

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

### <span data-ttu-id="6725b-135">-名稱</span><span class="sxs-lookup"><span data-stu-id="6725b-135">-Name</span></span>
<span data-ttu-id="6725b-136">提供者實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="6725b-136">Name of the provider instance.</span></span>

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

### <span data-ttu-id="6725b-137">-NoWait</span><span class="sxs-lookup"><span data-stu-id="6725b-137">-NoWait</span></span>
<span data-ttu-id="6725b-138">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="6725b-138">Run the command asynchronously</span></span>

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

### <span data-ttu-id="6725b-139">-ProviderType</span><span class="sxs-lookup"><span data-stu-id="6725b-139">-ProviderType</span></span>
<span data-ttu-id="6725b-140">提供者實例的類型。</span><span class="sxs-lookup"><span data-stu-id="6725b-140">The type of provider instance.</span></span>
<span data-ttu-id="6725b-141">支援的值為： "SapHana"。</span><span class="sxs-lookup"><span data-stu-id="6725b-141">Supported values are: "SapHana".</span></span>

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

### <span data-ttu-id="6725b-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6725b-142">-ResourceGroupName</span></span>
<span data-ttu-id="6725b-143">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6725b-143">Name of the resource group.</span></span>

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

### <span data-ttu-id="6725b-144">-SapMonitorName</span><span class="sxs-lookup"><span data-stu-id="6725b-144">-SapMonitorName</span></span>
<span data-ttu-id="6725b-145">SAP 監視資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="6725b-145">Name of the SAP monitor resource.</span></span>

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

### <span data-ttu-id="6725b-146">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6725b-146">-SubscriptionId</span></span>
<span data-ttu-id="6725b-147">訂閱識別碼，可唯一識別 Microsoft Azure 訂閱。</span><span class="sxs-lookup"><span data-stu-id="6725b-147">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="6725b-148">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="6725b-148">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="6725b-149">-確認</span><span class="sxs-lookup"><span data-stu-id="6725b-149">-Confirm</span></span>
<span data-ttu-id="6725b-150">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6725b-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6725b-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6725b-151">-WhatIf</span></span>
<span data-ttu-id="6725b-152">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6725b-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6725b-153">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6725b-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6725b-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6725b-154">CommonParameters</span></span>
<span data-ttu-id="6725b-155">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6725b-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6725b-156">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="6725b-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6725b-157">輸入</span><span class="sxs-lookup"><span data-stu-id="6725b-157">INPUTS</span></span>

## <span data-ttu-id="6725b-158">輸出</span><span class="sxs-lookup"><span data-stu-id="6725b-158">OUTPUTS</span></span>

### <span data-ttu-id="6725b-159">IProviderInstance （HanaOnAzure）。 Api20200207Preview。</span><span class="sxs-lookup"><span data-stu-id="6725b-159">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.IProviderInstance</span></span>

## <span data-ttu-id="6725b-160">筆記</span><span class="sxs-lookup"><span data-stu-id="6725b-160">NOTES</span></span>

<span data-ttu-id="6725b-161">別名</span><span class="sxs-lookup"><span data-stu-id="6725b-161">ALIASES</span></span>

## <span data-ttu-id="6725b-162">相關連結</span><span class="sxs-lookup"><span data-stu-id="6725b-162">RELATED LINKS</span></span>

