---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/powershell/module/az.mariadb/update-azmariadbserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbServer.md
ms.openlocfilehash: 0db4d25f224f1c6984ba9b57184859e8fa2c6c28
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915421"
---
# <span data-ttu-id="8dacb-101">Update-AzMariaDbServer</span><span class="sxs-lookup"><span data-stu-id="8dacb-101">Update-AzMariaDbServer</span></span>

## <span data-ttu-id="8dacb-102">簡介</span><span class="sxs-lookup"><span data-stu-id="8dacb-102">SYNOPSIS</span></span>
<span data-ttu-id="8dacb-103">更新現有的伺服器。</span><span class="sxs-lookup"><span data-stu-id="8dacb-103">Updates an existing server.</span></span>
<span data-ttu-id="8dacb-104">要求內內容可以包含一到多個標準伺服器定義中呈現的屬性。</span><span class="sxs-lookup"><span data-stu-id="8dacb-104">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="8dacb-105">如果您想要Update-AzMariaDbConfiguration伺服器參數 ，例如補救伺服器參數，wait_timeout或net_retry_count。</span><span class="sxs-lookup"><span data-stu-id="8dacb-105">Use Update-AzMariaDbConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="8dacb-106">語法</span><span class="sxs-lookup"><span data-stu-id="8dacb-106">SYNTAX</span></span>

### <span data-ttu-id="8dacb-107">ServerName (預設) </span><span class="sxs-lookup"><span data-stu-id="8dacb-107">ServerName (Default)</span></span>
```
Update-AzMariaDbServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AdministratorLoginPassword <SecureString>] [-BackupRetentionDay <Int32>]
 [-GeoRedundantBackup <GeoRedundantBackup>] [-ReplicationRole <String>] [-Sku <String>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8dacb-108">ServerObject</span><span class="sxs-lookup"><span data-stu-id="8dacb-108">ServerObject</span></span>
```
Update-AzMariaDbServer -InputObject <IMariaDbIdentity> [-AdministratorLoginPassword <SecureString>]
 [-BackupRetentionDay <Int32>] [-GeoRedundantBackup <GeoRedundantBackup>] [-ReplicationRole <String>]
 [-Sku <String>] [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>]
 [-StorageInMb <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8dacb-109">描述</span><span class="sxs-lookup"><span data-stu-id="8dacb-109">DESCRIPTION</span></span>
<span data-ttu-id="8dacb-110">更新現有的伺服器。</span><span class="sxs-lookup"><span data-stu-id="8dacb-110">Updates an existing server.</span></span>
<span data-ttu-id="8dacb-111">要求內內容可以包含一到多個標準伺服器定義中呈現的屬性。</span><span class="sxs-lookup"><span data-stu-id="8dacb-111">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="8dacb-112">如果您想要Update-AzMariaDbConfiguration伺服器參數 ，例如補救伺服器參數，wait_timeout或net_retry_count。</span><span class="sxs-lookup"><span data-stu-id="8dacb-112">Use Update-AzMariaDbConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="8dacb-113">例子</span><span class="sxs-lookup"><span data-stu-id="8dacb-113">EXAMPLES</span></span>

### <span data-ttu-id="8dacb-114">範例 1：Update MariaDB</span><span class="sxs-lookup"><span data-stu-id="8dacb-114">Example 1: Update MariaDB</span></span>
```powershell
PS C:\> Update-AzMariaDbServer -Name mariadb-test-4rmtig -ResourceGroupName mariadb-test-qu5ov0 -StorageInMb 8192

Name                Location AdministratorLogin Version StorageProfileStorageMb SkuName  SkuTier SslEnforcement
----                -------- ------------------ ------- ----------------------- -------  ------- --------------
mariadb-test-4rmtig eastus   xofavpndqj         10.2    8192                    B_Gen5_1 Basic   Enabled
```

<span data-ttu-id="8dacb-115">此命令會更新 MariaDB。</span><span class="sxs-lookup"><span data-stu-id="8dacb-115">This command updates a MariaDB.</span></span>

### <span data-ttu-id="8dacb-116">範例 2：Update MariaDB</span><span class="sxs-lookup"><span data-stu-id="8dacb-116">Example 2: Update MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbServer -Name mariadb-test-4rmtig -ResourceGroupName mariadb-test-qu5ov0 | Update-AzMariaDbServer -StorageInMb (8192+1024)

Name                Location AdministratorLogin Version StorageProfileStorageMb SkuName  SkuTier SslEnforcement
----                -------- ------------------ ------- ----------------------- -------  ------- --------------
mariadb-test-4rmtig eastus   xofavpndqj         10.2    9216                    B_Gen5_1 Basic   Enabled
```

<span data-ttu-id="8dacb-117">此命令會更新 MariaDB。</span><span class="sxs-lookup"><span data-stu-id="8dacb-117">This command updates a MariaDB.</span></span>

## <span data-ttu-id="8dacb-118">參數</span><span class="sxs-lookup"><span data-stu-id="8dacb-118">PARAMETERS</span></span>

### <span data-ttu-id="8dacb-119">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="8dacb-119">-AdministratorLoginPassword</span></span>
<span data-ttu-id="8dacb-120">系統管理員登入的密碼。</span><span class="sxs-lookup"><span data-stu-id="8dacb-120">The password of the administrator login.</span></span>

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

### <span data-ttu-id="8dacb-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8dacb-121">-AsJob</span></span>
<span data-ttu-id="8dacb-122">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="8dacb-122">Run the command as a job</span></span>

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

### <span data-ttu-id="8dacb-123">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="8dacb-123">-BackupRetentionDay</span></span>
<span data-ttu-id="8dacb-124">伺服器的備份保留天數。</span><span class="sxs-lookup"><span data-stu-id="8dacb-124">Backup retention days for the server.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dacb-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8dacb-125">-DefaultProfile</span></span>
<span data-ttu-id="8dacb-126">區域 DefaultParameters 用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="8dacb-126">region DefaultParameters The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8dacb-127">-GeoRedundantBackup</span><span class="sxs-lookup"><span data-stu-id="8dacb-127">-GeoRedundantBackup</span></span>
<span data-ttu-id="8dacb-128">針對伺服器備份啟用異地重複或不啟用。</span><span class="sxs-lookup"><span data-stu-id="8dacb-128">Enable Geo-redundant or not for server backup.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Support.GeoRedundantBackup
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dacb-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8dacb-129">-InputObject</span></span>
<span data-ttu-id="8dacb-130">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="8dacb-130">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity
Parameter Sets: ServerObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8dacb-131">-名稱</span><span class="sxs-lookup"><span data-stu-id="8dacb-131">-Name</span></span>
<span data-ttu-id="8dacb-132">MariaDB 伺服器名稱</span><span class="sxs-lookup"><span data-stu-id="8dacb-132">MariaDB server name</span></span>

```yaml
Type: System.String
Parameter Sets: ServerName
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dacb-133">-NoWait</span><span class="sxs-lookup"><span data-stu-id="8dacb-133">-NoWait</span></span>
<span data-ttu-id="8dacb-134">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="8dacb-134">Run the command asynchronously</span></span>

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

### <span data-ttu-id="8dacb-135">-ReplicationRole</span><span class="sxs-lookup"><span data-stu-id="8dacb-135">-ReplicationRole</span></span>
<span data-ttu-id="8dacb-136">伺服器的複製角色。</span><span class="sxs-lookup"><span data-stu-id="8dacb-136">The replication role of the server.</span></span>

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

### <span data-ttu-id="8dacb-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8dacb-137">-ResourceGroupName</span></span>
<span data-ttu-id="8dacb-138">包含資源的資源組名。</span><span class="sxs-lookup"><span data-stu-id="8dacb-138">The name of the resource group that contains the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dacb-139">-SKU</span><span class="sxs-lookup"><span data-stu-id="8dacb-139">-Sku</span></span>
<span data-ttu-id="8dacb-140">SKU 的名稱，通常是 tier + family + 核心，例如 B_Gen4_1、GP_Gen5_8。</span><span class="sxs-lookup"><span data-stu-id="8dacb-140">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="8dacb-141">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="8dacb-141">-SslEnforcement</span></span>
<span data-ttu-id="8dacb-142">在連接至伺服器時啟用 ssl 強制執行或不啟用。</span><span class="sxs-lookup"><span data-stu-id="8dacb-142">Enable ssl enforcement or not when connect to server.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Support.SslEnforcementEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dacb-143">-StorageAuto上</span><span class="sxs-lookup"><span data-stu-id="8dacb-143">-StorageAutogrow</span></span>
<span data-ttu-id="8dacb-144">啟用儲存空間自動放大。</span><span class="sxs-lookup"><span data-stu-id="8dacb-144">Enable Storage Auto Grow.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Support.StorageAutogrow
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dacb-145">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="8dacb-145">-StorageInMb</span></span>
<span data-ttu-id="8dacb-146">伺服器允許的最大儲存空間。</span><span class="sxs-lookup"><span data-stu-id="8dacb-146">Max storage allowed for a server.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dacb-147">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8dacb-147">-SubscriptionId</span></span>
<span data-ttu-id="8dacb-148">訂閱識別碼是每個服務通話 URI 的一部分</span><span class="sxs-lookup"><span data-stu-id="8dacb-148">The subscription ID is part of the URI for every service call</span></span>

```yaml
Type: System.String
Parameter Sets: ServerName
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dacb-149">-標記</span><span class="sxs-lookup"><span data-stu-id="8dacb-149">-Tag</span></span>
<span data-ttu-id="8dacb-150">以金鑰值組形式顯示的應用程式特定中繼資料。</span><span class="sxs-lookup"><span data-stu-id="8dacb-150">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="8dacb-151">-確認</span><span class="sxs-lookup"><span data-stu-id="8dacb-151">-Confirm</span></span>
<span data-ttu-id="8dacb-152">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="8dacb-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8dacb-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8dacb-153">-WhatIf</span></span>
<span data-ttu-id="8dacb-154">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8dacb-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8dacb-155">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8dacb-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8dacb-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8dacb-156">CommonParameters</span></span>
<span data-ttu-id="8dacb-157">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="8dacb-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8dacb-158">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8dacb-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8dacb-159">輸入</span><span class="sxs-lookup"><span data-stu-id="8dacb-159">INPUTS</span></span>

### <span data-ttu-id="8dacb-160">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.models.IAzaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="8dacb-160">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="8dacb-161">輸出</span><span class="sxs-lookup"><span data-stu-id="8dacb-161">OUTPUTS</span></span>

### <span data-ttu-id="8dacb-162">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.models.Api20180601Preview.IServer</span><span class="sxs-lookup"><span data-stu-id="8dacb-162">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="8dacb-163">筆記</span><span class="sxs-lookup"><span data-stu-id="8dacb-163">NOTES</span></span>

<span data-ttu-id="8dacb-164">別名</span><span class="sxs-lookup"><span data-stu-id="8dacb-164">ALIASES</span></span>

<span data-ttu-id="8dacb-165">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="8dacb-165">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8dacb-166">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="8dacb-166">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8dacb-167">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="8dacb-167">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8dacb-168">INPUTOBJECT： <IMariaDbIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="8dacb-168">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8dacb-169">`[ConfigurationName <String>]`：伺服器組組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8dacb-169">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="8dacb-170">`[DatabaseName <String>]`：資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="8dacb-170">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="8dacb-171">`[FirewallRuleName <String>]`：伺服器防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="8dacb-171">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="8dacb-172">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="8dacb-172">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8dacb-173">`[LocationName <String>]`：位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="8dacb-173">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="8dacb-174">`[ResourceGroupName <String>]`：包含資源的資源組名。</span><span class="sxs-lookup"><span data-stu-id="8dacb-174">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="8dacb-175">您可以從 Azure Resource Manager API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="8dacb-175">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="8dacb-176">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`：安全性警示策略的名稱。</span><span class="sxs-lookup"><span data-stu-id="8dacb-176">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="8dacb-177">`[ServerName <String>]`：伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="8dacb-177">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="8dacb-178">`[SubscriptionId <String>]`：識別 Azure 訂閱的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="8dacb-178">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="8dacb-179">`[VirtualNetworkRuleName <String>]`：虛擬網路規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="8dacb-179">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="8dacb-180">相關連結</span><span class="sxs-lookup"><span data-stu-id="8dacb-180">RELATED LINKS</span></span>

