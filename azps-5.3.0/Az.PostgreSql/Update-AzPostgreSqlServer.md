---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/update-azpostgresqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlServer.md
ms.openlocfilehash: ecb568a356d0f1cf5ed36d966028e2d0ca4f813a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98437343"
---
# <span data-ttu-id="9788b-101">Update-AzPostgreSqlServer</span><span class="sxs-lookup"><span data-stu-id="9788b-101">Update-AzPostgreSqlServer</span></span>

## <span data-ttu-id="9788b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9788b-102">SYNOPSIS</span></span>
<span data-ttu-id="9788b-103">更新現有的伺服器。</span><span class="sxs-lookup"><span data-stu-id="9788b-103">Updates an existing server.</span></span>
<span data-ttu-id="9788b-104">要求主體可以包含一個到在一般伺服器定義中存在的許多屬性。</span><span class="sxs-lookup"><span data-stu-id="9788b-104">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="9788b-105">如果您想要補救伺服器參數（例如 wait_timeout 或 net_retry_count），請改用 Update-AzPostSqlConfiguration。</span><span class="sxs-lookup"><span data-stu-id="9788b-105">Use Update-AzPostSqlConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="9788b-106">句法</span><span class="sxs-lookup"><span data-stu-id="9788b-106">SYNTAX</span></span>

### <span data-ttu-id="9788b-107">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="9788b-107">UpdateExpanded (Default)</span></span>
```
Update-AzPostgreSqlServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AdministratorLoginPassword <SecureString>] [-BackupRetentionDay <Int32>] [-ReplicationRole <String>]
 [-Sku <String>] [-SkuCapacity <Int32>] [-SkuFamily <String>] [-SkuTier <SkuTier>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="9788b-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="9788b-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzPostgreSqlServer -InputObject <IPostgreSqlIdentity> [-AdministratorLoginPassword <SecureString>]
 [-BackupRetentionDay <Int32>] [-ReplicationRole <String>] [-Sku <String>] [-SkuCapacity <Int32>]
 [-SkuFamily <String>] [-SkuTier <SkuTier>] [-SslEnforcement <SslEnforcementEnum>]
 [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9788b-109">說明</span><span class="sxs-lookup"><span data-stu-id="9788b-109">DESCRIPTION</span></span>
<span data-ttu-id="9788b-110">更新現有的伺服器。</span><span class="sxs-lookup"><span data-stu-id="9788b-110">Updates an existing server.</span></span>
<span data-ttu-id="9788b-111">要求主體可以包含一個到在一般伺服器定義中存在的許多屬性。</span><span class="sxs-lookup"><span data-stu-id="9788b-111">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="9788b-112">如果您想要補救伺服器參數（例如 wait_timeout 或 net_retry_count），請改用 Update-AzPostSqlConfiguration。</span><span class="sxs-lookup"><span data-stu-id="9788b-112">Use Update-AzPostSqlConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="9788b-113">示例</span><span class="sxs-lookup"><span data-stu-id="9788b-113">EXAMPLES</span></span>

### <span data-ttu-id="9788b-114">範例1：依資源群組和伺服器名稱更新 PostgreSql 伺服器</span><span class="sxs-lookup"><span data-stu-id="9788b-114">Example 1: Update PostgreSql server by resource group and server name</span></span>
```powershell
PS C:\> Update-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -SslEnforcement Disabled

Name                 Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                 -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="9788b-115">這個 Cmdlet 會依資源群組和伺服器名稱來更新 PostgreSql server。</span><span class="sxs-lookup"><span data-stu-id="9788b-115">This cmdlet updates PostgreSql server by resource group and server name.</span></span>

### <span data-ttu-id="9788b-116">範例2：依身分識別更新 PostgreSql 伺服器。</span><span class="sxs-lookup"><span data-stu-id="9788b-116">Example 2: Update PostgreSql server by identity.</span></span>
```powershell
PS C:\> Get-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer | Update-AzPostgreSqlServer -BackupRetentionDay 23

Name                 Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                 -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="9788b-117">這個 Cmdlet 會依身分識別來更新 PostgreSql 伺服器。</span><span class="sxs-lookup"><span data-stu-id="9788b-117">This cmdlet updates PostgreSql server by identity.</span></span>

## <span data-ttu-id="9788b-118">參數</span><span class="sxs-lookup"><span data-stu-id="9788b-118">PARAMETERS</span></span>

### <span data-ttu-id="9788b-119">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="9788b-119">-AdministratorLoginPassword</span></span>
<span data-ttu-id="9788b-120">系統管理員登入的密碼。</span><span class="sxs-lookup"><span data-stu-id="9788b-120">The password of the administrator login.</span></span>

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

### <span data-ttu-id="9788b-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9788b-121">-AsJob</span></span>
<span data-ttu-id="9788b-122">執行命令做為作業。</span><span class="sxs-lookup"><span data-stu-id="9788b-122">Run the command as a job.</span></span>

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

### <span data-ttu-id="9788b-123">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="9788b-123">-BackupRetentionDay</span></span>
<span data-ttu-id="9788b-124">伺服器的備份保留天數。</span><span class="sxs-lookup"><span data-stu-id="9788b-124">Backup retention days for the server.</span></span>
<span data-ttu-id="9788b-125">日算在7到35。</span><span class="sxs-lookup"><span data-stu-id="9788b-125">Day count is between 7 and 35.</span></span>

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

### <span data-ttu-id="9788b-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9788b-126">-DefaultProfile</span></span>
<span data-ttu-id="9788b-127">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9788b-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9788b-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9788b-128">-InputObject</span></span>
<span data-ttu-id="9788b-129">身分識別參數。</span><span class="sxs-lookup"><span data-stu-id="9788b-129">Identity Parameter.</span></span>
<span data-ttu-id="9788b-130">若要構造，請參閱適用于 INPUTOBJECT 屬性的 [記事] 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="9788b-130">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="9788b-131">-名稱</span><span class="sxs-lookup"><span data-stu-id="9788b-131">-Name</span></span>
<span data-ttu-id="9788b-132">伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="9788b-132">The name of the server.</span></span>

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

### <span data-ttu-id="9788b-133">-NoWait</span><span class="sxs-lookup"><span data-stu-id="9788b-133">-NoWait</span></span>
<span data-ttu-id="9788b-134">以非同步方式執行命令。</span><span class="sxs-lookup"><span data-stu-id="9788b-134">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="9788b-135">-ReplicationRole</span><span class="sxs-lookup"><span data-stu-id="9788b-135">-ReplicationRole</span></span>
<span data-ttu-id="9788b-136">伺服器的複製角色。</span><span class="sxs-lookup"><span data-stu-id="9788b-136">The replication role of the server.</span></span>

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

### <span data-ttu-id="9788b-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9788b-137">-ResourceGroupName</span></span>
<span data-ttu-id="9788b-138">包含資源之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9788b-138">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="9788b-139">您可以從 Azure 資源管理器 API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="9788b-139">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="9788b-140">-Sku</span><span class="sxs-lookup"><span data-stu-id="9788b-140">-Sku</span></span>
<span data-ttu-id="9788b-141">Sku 的名稱，通常是 [層 + 家庭 + 核心]，例如 B_Gen4_1、GP_Gen5_8。</span><span class="sxs-lookup"><span data-stu-id="9788b-141">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="9788b-142">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="9788b-142">-SkuCapacity</span></span>
<span data-ttu-id="9788b-143">[擴大/縮小] 容量，代表伺服器的計算單位。</span><span class="sxs-lookup"><span data-stu-id="9788b-143">The scale up/out capacity, representing server's compute units.</span></span>

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

### <span data-ttu-id="9788b-144">-SkuFamily</span><span class="sxs-lookup"><span data-stu-id="9788b-144">-SkuFamily</span></span>
<span data-ttu-id="9788b-145">硬體系列。</span><span class="sxs-lookup"><span data-stu-id="9788b-145">The family of hardware.</span></span>

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

### <span data-ttu-id="9788b-146">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="9788b-146">-SkuTier</span></span>
<span data-ttu-id="9788b-147">特定 SKU 的層級，例如基本。</span><span class="sxs-lookup"><span data-stu-id="9788b-147">The tier of the particular SKU, e.g. Basic.</span></span>

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

### <span data-ttu-id="9788b-148">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="9788b-148">-SslEnforcement</span></span>
<span data-ttu-id="9788b-149">在連線至伺服器時啟用 ssl 強制執行。</span><span class="sxs-lookup"><span data-stu-id="9788b-149">Enable ssl enforcement or not when connect to server.</span></span>

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

### <span data-ttu-id="9788b-150">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="9788b-150">-StorageAutogrow</span></span>
<span data-ttu-id="9788b-151">啟用儲存空間自動增長。</span><span class="sxs-lookup"><span data-stu-id="9788b-151">Enable Storage Auto Grow.</span></span>

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

### <span data-ttu-id="9788b-152">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="9788b-152">-StorageInMb</span></span>
<span data-ttu-id="9788b-153">伺服器允許的最大儲存空間。</span><span class="sxs-lookup"><span data-stu-id="9788b-153">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="9788b-154">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9788b-154">-SubscriptionId</span></span>
<span data-ttu-id="9788b-155">識別 Azure 訂閱的訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="9788b-155">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="9788b-156">-Tag</span><span class="sxs-lookup"><span data-stu-id="9788b-156">-Tag</span></span>
<span data-ttu-id="9788b-157">以鍵值對形式的特定應用程式中繼資料。</span><span class="sxs-lookup"><span data-stu-id="9788b-157">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="9788b-158">-確認</span><span class="sxs-lookup"><span data-stu-id="9788b-158">-Confirm</span></span>
<span data-ttu-id="9788b-159">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9788b-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9788b-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9788b-160">-WhatIf</span></span>
<span data-ttu-id="9788b-161">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9788b-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9788b-162">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9788b-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9788b-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9788b-163">CommonParameters</span></span>
<span data-ttu-id="9788b-164">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9788b-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9788b-165">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="9788b-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9788b-166">輸入</span><span class="sxs-lookup"><span data-stu-id="9788b-166">INPUTS</span></span>

### <span data-ttu-id="9788b-167">IPostgreSqlIdentity （PostgreSql）的</span><span class="sxs-lookup"><span data-stu-id="9788b-167">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="9788b-168">輸出</span><span class="sxs-lookup"><span data-stu-id="9788b-168">OUTPUTS</span></span>

### <span data-ttu-id="9788b-169">IServer （PostgreSql）。 Api20171201。</span><span class="sxs-lookup"><span data-stu-id="9788b-169">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="9788b-170">筆記</span><span class="sxs-lookup"><span data-stu-id="9788b-170">NOTES</span></span>

<span data-ttu-id="9788b-171">別名</span><span class="sxs-lookup"><span data-stu-id="9788b-171">ALIASES</span></span>

<span data-ttu-id="9788b-172">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="9788b-172">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9788b-173">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="9788b-173">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9788b-174">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="9788b-174">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9788b-175">INPUTOBJECT <IPostgreSqlIdentity> ：身分識別參數。</span><span class="sxs-lookup"><span data-stu-id="9788b-175">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter.</span></span>
  - <span data-ttu-id="9788b-176">`[ConfigurationName <String>]`：伺服器配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="9788b-176">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="9788b-177">`[DatabaseName <String>]`：資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="9788b-177">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="9788b-178">`[FirewallRuleName <String>]`：伺服器防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="9788b-178">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="9788b-179">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="9788b-179">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9788b-180">`[LocationName <String>]`：位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="9788b-180">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="9788b-181">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9788b-181">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="9788b-182">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="9788b-182">The name is case insensitive.</span></span>
  - <span data-ttu-id="9788b-183">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`：安全警示原則的名稱。</span><span class="sxs-lookup"><span data-stu-id="9788b-183">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="9788b-184">`[ServerName <String>]`：伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="9788b-184">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="9788b-185">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="9788b-185">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="9788b-186">`[VirtualNetworkRuleName <String>]`：虛擬網路規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="9788b-186">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="9788b-187">相關連結</span><span class="sxs-lookup"><span data-stu-id="9788b-187">RELATED LINKS</span></span>

