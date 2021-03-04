---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/powershell/module/az.postgresql/update-azpostgresqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlServer.md
ms.openlocfilehash: d6d4480f2a4be2fa10a6e6ea8b69da1de9c61f39
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907582"
---
# <span data-ttu-id="09382-101">Update-AzPostgreSqlServer</span><span class="sxs-lookup"><span data-stu-id="09382-101">Update-AzPostgreSqlServer</span></span>

## <span data-ttu-id="09382-102">簡介</span><span class="sxs-lookup"><span data-stu-id="09382-102">SYNOPSIS</span></span>
<span data-ttu-id="09382-103">更新現有的伺服器。</span><span class="sxs-lookup"><span data-stu-id="09382-103">Updates an existing server.</span></span>
<span data-ttu-id="09382-104">要求內內容可以包含一到多個標準伺服器定義中呈現的屬性。</span><span class="sxs-lookup"><span data-stu-id="09382-104">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="09382-105">如果您想要Update-AzPostSqlConfiguration伺服器參數 ，例如補救伺服器參數，wait_timeout或net_retry_count。</span><span class="sxs-lookup"><span data-stu-id="09382-105">Use Update-AzPostSqlConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="09382-106">語法</span><span class="sxs-lookup"><span data-stu-id="09382-106">SYNTAX</span></span>

### <span data-ttu-id="09382-107">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="09382-107">UpdateExpanded (Default)</span></span>
```
Update-AzPostgreSqlServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AdministratorLoginPassword <SecureString>] [-BackupRetentionDay <Int32>]
 [-MinimalTlsVersion <MinimalTlsVersionEnum>] [-ReplicationRole <String>] [-Sku <String>]
 [-SkuCapacity <Int32>] [-SkuFamily <String>] [-SkuTier <SkuTier>] [-SslEnforcement <SslEnforcementEnum>]
 [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="09382-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="09382-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzPostgreSqlServer -InputObject <IPostgreSqlIdentity> [-AdministratorLoginPassword <SecureString>]
 [-BackupRetentionDay <Int32>] [-MinimalTlsVersion <MinimalTlsVersionEnum>] [-ReplicationRole <String>]
 [-Sku <String>] [-SkuCapacity <Int32>] [-SkuFamily <String>] [-SkuTier <SkuTier>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="09382-109">描述</span><span class="sxs-lookup"><span data-stu-id="09382-109">DESCRIPTION</span></span>
<span data-ttu-id="09382-110">更新現有的伺服器。</span><span class="sxs-lookup"><span data-stu-id="09382-110">Updates an existing server.</span></span>
<span data-ttu-id="09382-111">要求內內容可以包含一到多個標準伺服器定義中呈現的屬性。</span><span class="sxs-lookup"><span data-stu-id="09382-111">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="09382-112">如果您想要Update-AzPostSqlConfiguration伺服器參數 ，例如補救伺服器參數，wait_timeout或net_retry_count。</span><span class="sxs-lookup"><span data-stu-id="09382-112">Use Update-AzPostSqlConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="09382-113">例子</span><span class="sxs-lookup"><span data-stu-id="09382-113">EXAMPLES</span></span>

### <span data-ttu-id="09382-114">範例 1：根據資源群組和伺服器名稱更新 PostgreSql 伺服器</span><span class="sxs-lookup"><span data-stu-id="09382-114">Example 1: Update PostgreSql server by resource group and server name</span></span>
```powershell
PS C:\> Update-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -SslEnforcement Disabled

Name                 Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                 -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="09382-115">此 Cmdlet 會根據資源群組和伺服器名稱更新 PostgreSql 伺服器。</span><span class="sxs-lookup"><span data-stu-id="09382-115">This cmdlet updates PostgreSql server by resource group and server name.</span></span>

### <span data-ttu-id="09382-116">範例 2：根據身分識別更新 PostgreSql 伺服器。</span><span class="sxs-lookup"><span data-stu-id="09382-116">Example 2: Update PostgreSql server by identity.</span></span>
```powershell
PS C:\> Get-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer | Update-AzPostgreSqlServer -BackupRetentionDay 23

Name                 Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                 -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="09382-117">此 Cmdlet 會以身分識別更新 PostgreSql 伺服器。</span><span class="sxs-lookup"><span data-stu-id="09382-117">This cmdlet updates PostgreSql server by identity.</span></span>

## <span data-ttu-id="09382-118">參數</span><span class="sxs-lookup"><span data-stu-id="09382-118">PARAMETERS</span></span>

### <span data-ttu-id="09382-119">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="09382-119">-AdministratorLoginPassword</span></span>
<span data-ttu-id="09382-120">系統管理員登入的密碼。</span><span class="sxs-lookup"><span data-stu-id="09382-120">The password of the administrator login.</span></span>

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

### <span data-ttu-id="09382-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="09382-121">-AsJob</span></span>
<span data-ttu-id="09382-122">以工作執行命令。</span><span class="sxs-lookup"><span data-stu-id="09382-122">Run the command as a job.</span></span>

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

### <span data-ttu-id="09382-123">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="09382-123">-BackupRetentionDay</span></span>
<span data-ttu-id="09382-124">伺服器的備份保留天數。</span><span class="sxs-lookup"><span data-stu-id="09382-124">Backup retention days for the server.</span></span>
<span data-ttu-id="09382-125">日計數介於 7 到 35 之間。</span><span class="sxs-lookup"><span data-stu-id="09382-125">Day count is between 7 and 35.</span></span>

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

### <span data-ttu-id="09382-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09382-126">-DefaultProfile</span></span>
<span data-ttu-id="09382-127">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="09382-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="09382-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="09382-128">-InputObject</span></span>
<span data-ttu-id="09382-129">身分識別參數。</span><span class="sxs-lookup"><span data-stu-id="09382-129">Identity Parameter.</span></span>
<span data-ttu-id="09382-130">若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="09382-130">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="09382-131">-MinimalTlsVersion</span><span class="sxs-lookup"><span data-stu-id="09382-131">-MinimalTlsVersion</span></span>
<span data-ttu-id="09382-132">在啟用 SSL 時，設定伺服器連至伺服器的最小 TLS 版本。</span><span class="sxs-lookup"><span data-stu-id="09382-132">Set the minimal TLS version for connections to server when SSL is enabled.</span></span>
<span data-ttu-id="09382-133">預設值為 TLSEnforcementDisabled.accepted 值：TLS1_0、TLS1_1、TLS1_2、TLSEnforcementDisabled。</span><span class="sxs-lookup"><span data-stu-id="09382-133">Default is TLSEnforcementDisabled.accepted values: TLS1_0, TLS1_1, TLS1_2, TLSEnforcementDisabled.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Support.MinimalTlsVersionEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09382-134">-名稱</span><span class="sxs-lookup"><span data-stu-id="09382-134">-Name</span></span>
<span data-ttu-id="09382-135">伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="09382-135">The name of the server.</span></span>

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

### <span data-ttu-id="09382-136">-NoWait</span><span class="sxs-lookup"><span data-stu-id="09382-136">-NoWait</span></span>
<span data-ttu-id="09382-137">非同步執行命令。</span><span class="sxs-lookup"><span data-stu-id="09382-137">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="09382-138">-ReplicationRole</span><span class="sxs-lookup"><span data-stu-id="09382-138">-ReplicationRole</span></span>
<span data-ttu-id="09382-139">伺服器的複製角色。</span><span class="sxs-lookup"><span data-stu-id="09382-139">The replication role of the server.</span></span>

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

### <span data-ttu-id="09382-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09382-140">-ResourceGroupName</span></span>
<span data-ttu-id="09382-141">包含資源的資源組名。</span><span class="sxs-lookup"><span data-stu-id="09382-141">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="09382-142">您可以從 Azure Resource Manager API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="09382-142">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="09382-143">-SKU</span><span class="sxs-lookup"><span data-stu-id="09382-143">-Sku</span></span>
<span data-ttu-id="09382-144">SKU 的名稱，通常是 tier + family + 核心，例如 B_Gen4_1、GP_Gen5_8。</span><span class="sxs-lookup"><span data-stu-id="09382-144">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="09382-145">-Sku以</span><span class="sxs-lookup"><span data-stu-id="09382-145">-SkuCapacity</span></span>
<span data-ttu-id="09382-146">向上/縮小容量，代表伺服器的計算單位。</span><span class="sxs-lookup"><span data-stu-id="09382-146">The scale up/out capacity, representing server's compute units.</span></span>

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

### <span data-ttu-id="09382-147">-SkuFamily</span><span class="sxs-lookup"><span data-stu-id="09382-147">-SkuFamily</span></span>
<span data-ttu-id="09382-148">硬體系列。</span><span class="sxs-lookup"><span data-stu-id="09382-148">The family of hardware.</span></span>

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

### <span data-ttu-id="09382-149">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="09382-149">-SkuTier</span></span>
<span data-ttu-id="09382-150">特定 SKU 的層級，例如基本。</span><span class="sxs-lookup"><span data-stu-id="09382-150">The tier of the particular SKU, e.g. Basic.</span></span>

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

### <span data-ttu-id="09382-151">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="09382-151">-SslEnforcement</span></span>
<span data-ttu-id="09382-152">在連接至伺服器時啟用 ssl 強制執行或不啟用。</span><span class="sxs-lookup"><span data-stu-id="09382-152">Enable ssl enforcement or not when connect to server.</span></span>

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

### <span data-ttu-id="09382-153">-StorageAuto上</span><span class="sxs-lookup"><span data-stu-id="09382-153">-StorageAutogrow</span></span>
<span data-ttu-id="09382-154">啟用儲存空間自動放大。</span><span class="sxs-lookup"><span data-stu-id="09382-154">Enable Storage Auto Grow.</span></span>

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

### <span data-ttu-id="09382-155">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="09382-155">-StorageInMb</span></span>
<span data-ttu-id="09382-156">伺服器允許的最大儲存空間。</span><span class="sxs-lookup"><span data-stu-id="09382-156">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="09382-157">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="09382-157">-SubscriptionId</span></span>
<span data-ttu-id="09382-158">可識別 Azure 訂閱的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="09382-158">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="09382-159">-標記</span><span class="sxs-lookup"><span data-stu-id="09382-159">-Tag</span></span>
<span data-ttu-id="09382-160">以金鑰值組形式顯示的應用程式特定中繼資料。</span><span class="sxs-lookup"><span data-stu-id="09382-160">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="09382-161">-確認</span><span class="sxs-lookup"><span data-stu-id="09382-161">-Confirm</span></span>
<span data-ttu-id="09382-162">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="09382-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09382-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09382-163">-WhatIf</span></span>
<span data-ttu-id="09382-164">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="09382-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="09382-165">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="09382-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09382-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09382-166">CommonParameters</span></span>
<span data-ttu-id="09382-167">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="09382-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09382-168">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="09382-168">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09382-169">輸入</span><span class="sxs-lookup"><span data-stu-id="09382-169">INPUTS</span></span>

### <span data-ttu-id="09382-170">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="09382-170">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="09382-171">輸出</span><span class="sxs-lookup"><span data-stu-id="09382-171">OUTPUTS</span></span>

### <span data-ttu-id="09382-172">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="09382-172">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="09382-173">筆記</span><span class="sxs-lookup"><span data-stu-id="09382-173">NOTES</span></span>

<span data-ttu-id="09382-174">別名</span><span class="sxs-lookup"><span data-stu-id="09382-174">ALIASES</span></span>

<span data-ttu-id="09382-175">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="09382-175">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="09382-176">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="09382-176">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="09382-177">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="09382-177">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="09382-178">INPUTOBJECT： <IPostgreSqlIdentity> 身分識別參數。</span><span class="sxs-lookup"><span data-stu-id="09382-178">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter.</span></span>
  - <span data-ttu-id="09382-179">`[ConfigurationName <String>]`：伺服器組組的名稱。</span><span class="sxs-lookup"><span data-stu-id="09382-179">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="09382-180">`[DatabaseName <String>]`：資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="09382-180">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="09382-181">`[FirewallRuleName <String>]`：伺服器防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="09382-181">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="09382-182">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="09382-182">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="09382-183">`[LocationName <String>]`：位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="09382-183">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="09382-184">`[ResourceGroupName <String>]`：資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="09382-184">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="09382-185">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="09382-185">The name is case insensitive.</span></span>
  - <span data-ttu-id="09382-186">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`：安全性警示策略的名稱。</span><span class="sxs-lookup"><span data-stu-id="09382-186">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="09382-187">`[ServerName <String>]`：伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="09382-187">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="09382-188">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="09382-188">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="09382-189">`[VirtualNetworkRuleName <String>]`：虛擬網路規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="09382-189">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="09382-190">相關連結</span><span class="sxs-lookup"><span data-stu-id="09382-190">RELATED LINKS</span></span>

