---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/powershell/module/az.postgresql/update-azpostgresqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlFlexibleServer.md
ms.openlocfilehash: 65004c35ffa9c4cb227845787c91219a319789fe
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907589"
---
# <span data-ttu-id="3996a-101">Update-AzPostgreSqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="3996a-101">Update-AzPostgreSqlFlexibleServer</span></span>

## <span data-ttu-id="3996a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="3996a-102">SYNOPSIS</span></span>
<span data-ttu-id="3996a-103">更新現有的伺服器。</span><span class="sxs-lookup"><span data-stu-id="3996a-103">Updates an existing server.</span></span>
<span data-ttu-id="3996a-104">要求內內容可以包含一到多個標準伺服器定義中呈現的屬性。</span><span class="sxs-lookup"><span data-stu-id="3996a-104">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="3996a-105">如果您想要Update-AzPostSqlFlexibleServerConfiguration伺服器參數 ，例如補救伺服器參數，wait_timeout或net_retry_count。</span><span class="sxs-lookup"><span data-stu-id="3996a-105">Use Update-AzPostSqlFlexibleServerConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="3996a-106">語法</span><span class="sxs-lookup"><span data-stu-id="3996a-106">SYNTAX</span></span>

### <span data-ttu-id="3996a-107">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="3996a-107">UpdateExpanded (Default)</span></span>
```
Update-AzPostgreSqlFlexibleServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AdministratorLoginPassword <SecureString>] [-BackupRetentionDay <Int32>] [-HaEnabled <HaEnabledEnum>]
 [-MaintenanceWindow <String>] [-ReplicationRole <String>] [-Sku <String>] [-SkuTier <SkuTier>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3996a-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="3996a-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzPostgreSqlFlexibleServer -InputObject <IPostgreSqlIdentity>
 [-AdministratorLoginPassword <SecureString>] [-BackupRetentionDay <Int32>] [-HaEnabled <HaEnabledEnum>]
 [-MaintenanceWindow <String>] [-ReplicationRole <String>] [-Sku <String>] [-SkuTier <SkuTier>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3996a-109">描述</span><span class="sxs-lookup"><span data-stu-id="3996a-109">DESCRIPTION</span></span>
<span data-ttu-id="3996a-110">更新現有的伺服器。</span><span class="sxs-lookup"><span data-stu-id="3996a-110">Updates an existing server.</span></span>
<span data-ttu-id="3996a-111">要求內內容可以包含一到多個標準伺服器定義中呈現的屬性。</span><span class="sxs-lookup"><span data-stu-id="3996a-111">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="3996a-112">如果您想要Update-AzPostgreSqlFlexibleServerConfiguration伺服器參數 ，例如補救伺服器參數，wait_timeout或net_retry_count。</span><span class="sxs-lookup"><span data-stu-id="3996a-112">Use Update-AzPostgreSqlFlexibleServerConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="3996a-113">例子</span><span class="sxs-lookup"><span data-stu-id="3996a-113">EXAMPLES</span></span>

### <span data-ttu-id="3996a-114">範例 1：根據資源群組和伺服器名稱更新 PostgreSql 伺服器</span><span class="sxs-lookup"><span data-stu-id="3996a-114">Example 1: Update PostgreSql server by resource group and server name</span></span>
```powershell
PS C:\> Update-AzPostgreSqlFlexibleServer -ResourceGroupName PowershellPostgreSqlTest -Name postgresql-test -Sku Standard_D4s_v3

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- ---------------- -------------
postgresql-test eastus postgresql_test     12     131072                  Standard_D4s_v3 GeneralPurpose
```

<span data-ttu-id="3996a-115">此 Cmdlet 會根據資源群組和伺服器名稱更新 PostgreSql 伺服器。</span><span class="sxs-lookup"><span data-stu-id="3996a-115">This cmdlet updates PostgreSql server by resource group and server name.</span></span>

### <span data-ttu-id="3996a-116">範例 2：根據身分識別更新 PostgreSql 伺服器。</span><span class="sxs-lookup"><span data-stu-id="3996a-116">Example 2: Update PostgreSql server by identity.</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFlexibleServer -ResourceGroupName PowershellPostgreSqlTest -ServerName postgresql-test | Update-AzPostgreSqlFlexibleServer -BackupRetentionDay 23 -StorageMb 10240

Name            Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----            -------- ------------------ ------- ----------------------- ---------------- -------------
postgresql-test eastus   postgresql_test     12     131072                  Standard_D2s_v3 GeneralPurpose
```

<span data-ttu-id="3996a-117">此 Cmdlet 會以身分識別更新 PostgreSql 伺服器。</span><span class="sxs-lookup"><span data-stu-id="3996a-117">This cmdlet updates PostgreSql server by identity.</span></span>

## <span data-ttu-id="3996a-118">參數</span><span class="sxs-lookup"><span data-stu-id="3996a-118">PARAMETERS</span></span>

### <span data-ttu-id="3996a-119">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="3996a-119">-AdministratorLoginPassword</span></span>
<span data-ttu-id="3996a-120">系統管理員登入的密碼。</span><span class="sxs-lookup"><span data-stu-id="3996a-120">The password of the administrator login.</span></span>

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

### <span data-ttu-id="3996a-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3996a-121">-AsJob</span></span>
<span data-ttu-id="3996a-122">以工作執行命令。</span><span class="sxs-lookup"><span data-stu-id="3996a-122">Run the command as a job.</span></span>

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

### <span data-ttu-id="3996a-123">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="3996a-123">-BackupRetentionDay</span></span>
<span data-ttu-id="3996a-124">伺服器的備份保留天數。</span><span class="sxs-lookup"><span data-stu-id="3996a-124">Backup retention days for the server.</span></span>
<span data-ttu-id="3996a-125">日計數介於 7 到 35 之間。</span><span class="sxs-lookup"><span data-stu-id="3996a-125">Day count is between 7 and 35.</span></span>

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

### <span data-ttu-id="3996a-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3996a-126">-DefaultProfile</span></span>
<span data-ttu-id="3996a-127">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="3996a-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3996a-128">-HaEnabled</span><span class="sxs-lookup"><span data-stu-id="3996a-128">-HaEnabled</span></span>
<span data-ttu-id="3996a-129">啟用或停用高可用性功能。</span><span class="sxs-lookup"><span data-stu-id="3996a-129">Enable or disable high availability feature.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Support.HaEnabledEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3996a-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3996a-130">-InputObject</span></span>
<span data-ttu-id="3996a-131">身分識別參數。</span><span class="sxs-lookup"><span data-stu-id="3996a-131">Identity Parameter.</span></span>
<span data-ttu-id="3996a-132">若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="3996a-132">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3996a-133">-維護視窗</span><span class="sxs-lookup"><span data-stu-id="3996a-133">-MaintenanceWindow</span></span>
<span data-ttu-id="3996a-134">指定維護 (UTC) 的時間。</span><span class="sxs-lookup"><span data-stu-id="3996a-134">Period of time (UTC) designated for maintenance.</span></span>
<span data-ttu-id="3996a-135">範例：「星期日：23：30」以排定在星期日，下午 11：30 UTC。</span><span class="sxs-lookup"><span data-stu-id="3996a-135">Examples: "Sun:23:30" to schedule on Sunday, 11:30pm UTC.</span></span>
<span data-ttu-id="3996a-136">若要在「已停用」中設定回預設傳遞</span><span class="sxs-lookup"><span data-stu-id="3996a-136">To set back to default pass in "Disabled"</span></span>

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

### <span data-ttu-id="3996a-137">-名稱</span><span class="sxs-lookup"><span data-stu-id="3996a-137">-Name</span></span>
<span data-ttu-id="3996a-138">伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="3996a-138">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3996a-139">-NoWait</span><span class="sxs-lookup"><span data-stu-id="3996a-139">-NoWait</span></span>
<span data-ttu-id="3996a-140">非同步執行命令。</span><span class="sxs-lookup"><span data-stu-id="3996a-140">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="3996a-141">-ReplicationRole</span><span class="sxs-lookup"><span data-stu-id="3996a-141">-ReplicationRole</span></span>
<span data-ttu-id="3996a-142">伺服器的複製角色。</span><span class="sxs-lookup"><span data-stu-id="3996a-142">The replication role of the server.</span></span>

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

### <span data-ttu-id="3996a-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3996a-143">-ResourceGroupName</span></span>
<span data-ttu-id="3996a-144">包含資源的資源組名。</span><span class="sxs-lookup"><span data-stu-id="3996a-144">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="3996a-145">您可以從 Azure Resource Manager API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="3996a-145">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="3996a-146">-SKU</span><span class="sxs-lookup"><span data-stu-id="3996a-146">-Sku</span></span>
<span data-ttu-id="3996a-147">SKU 的名稱，例如 Burstable_B1ms、Standard_D2ds_v4</span><span class="sxs-lookup"><span data-stu-id="3996a-147">The name of the sku, e.g. Burstable_B1ms, Standard_D2ds_v4</span></span>

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

### <span data-ttu-id="3996a-148">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="3996a-148">-SkuTier</span></span>
<span data-ttu-id="3996a-149">特定 SKU 的層級。</span><span class="sxs-lookup"><span data-stu-id="3996a-149">The tier of the particular SKU.</span></span>
<span data-ttu-id="3996a-150">接受的值：可重值、GeneralPurpose、記憶體優化。</span><span class="sxs-lookup"><span data-stu-id="3996a-150">Accepted values: Burstable, GeneralPurpose, Memory Optimized.</span></span>
<span data-ttu-id="3996a-151">預設值：可重複。</span><span class="sxs-lookup"><span data-stu-id="3996a-151">Default: Burstable.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Support.SkuTier
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3996a-152">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="3996a-152">-SslEnforcement</span></span>
<span data-ttu-id="3996a-153">在連接至伺服器時啟用 ssl 強制執行或不啟用。</span><span class="sxs-lookup"><span data-stu-id="3996a-153">Enable ssl enforcement or not when connect to server.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Support.SslEnforcementEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3996a-154">-StorageAuto上</span><span class="sxs-lookup"><span data-stu-id="3996a-154">-StorageAutogrow</span></span>
<span data-ttu-id="3996a-155">啟用儲存空間自動放大。</span><span class="sxs-lookup"><span data-stu-id="3996a-155">Enable Storage Auto Grow.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Support.StorageAutogrow
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3996a-156">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="3996a-156">-StorageInMb</span></span>
<span data-ttu-id="3996a-157">伺服器允許的最大儲存空間。</span><span class="sxs-lookup"><span data-stu-id="3996a-157">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="3996a-158">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3996a-158">-SubscriptionId</span></span>
<span data-ttu-id="3996a-159">可識別 Azure 訂閱的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="3996a-159">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="3996a-160">-標記</span><span class="sxs-lookup"><span data-stu-id="3996a-160">-Tag</span></span>
<span data-ttu-id="3996a-161">以金鑰值組形式顯示的應用程式特定中繼資料。</span><span class="sxs-lookup"><span data-stu-id="3996a-161">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="3996a-162">-確認</span><span class="sxs-lookup"><span data-stu-id="3996a-162">-Confirm</span></span>
<span data-ttu-id="3996a-163">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="3996a-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3996a-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3996a-164">-WhatIf</span></span>
<span data-ttu-id="3996a-165">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3996a-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3996a-166">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3996a-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3996a-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3996a-167">CommonParameters</span></span>
<span data-ttu-id="3996a-168">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="3996a-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3996a-169">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3996a-169">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3996a-170">輸入</span><span class="sxs-lookup"><span data-stu-id="3996a-170">INPUTS</span></span>

### <span data-ttu-id="3996a-171">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="3996a-171">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="3996a-172">輸出</span><span class="sxs-lookup"><span data-stu-id="3996a-172">OUTPUTS</span></span>

### <span data-ttu-id="3996a-173">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.IServerAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="3996a-173">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.IServerAutoGenerated</span></span>

## <span data-ttu-id="3996a-174">筆記</span><span class="sxs-lookup"><span data-stu-id="3996a-174">NOTES</span></span>

<span data-ttu-id="3996a-175">別名</span><span class="sxs-lookup"><span data-stu-id="3996a-175">ALIASES</span></span>

<span data-ttu-id="3996a-176">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="3996a-176">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3996a-177">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="3996a-177">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3996a-178">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="3996a-178">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3996a-179">INPUTOBJECT： <IPostgreSqlIdentity> 身分識別參數。</span><span class="sxs-lookup"><span data-stu-id="3996a-179">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter.</span></span>
  - <span data-ttu-id="3996a-180">`[ConfigurationName <String>]`：伺服器組組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3996a-180">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="3996a-181">`[DatabaseName <String>]`：資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="3996a-181">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="3996a-182">`[FirewallRuleName <String>]`：伺服器防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="3996a-182">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="3996a-183">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="3996a-183">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3996a-184">`[LocationName <String>]`：位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="3996a-184">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="3996a-185">`[ResourceGroupName <String>]`：資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3996a-185">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="3996a-186">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="3996a-186">The name is case insensitive.</span></span>
  - <span data-ttu-id="3996a-187">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`：安全性警示策略的名稱。</span><span class="sxs-lookup"><span data-stu-id="3996a-187">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="3996a-188">`[ServerName <String>]`：伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="3996a-188">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="3996a-189">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="3996a-189">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="3996a-190">`[VirtualNetworkRuleName <String>]`：虛擬網路規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="3996a-190">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="3996a-191">相關連結</span><span class="sxs-lookup"><span data-stu-id="3996a-191">RELATED LINKS</span></span>

