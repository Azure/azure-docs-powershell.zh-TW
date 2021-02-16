---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/update-azpostgresqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlFlexibleServer.md
ms.openlocfilehash: f6634f83e89abe4c775779c052ad9ee7b21bea6c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100131015"
---
# <span data-ttu-id="6db6b-101">Update-AzPostgreSqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="6db6b-101">Update-AzPostgreSqlFlexibleServer</span></span>

## <span data-ttu-id="6db6b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6db6b-102">SYNOPSIS</span></span>
<span data-ttu-id="6db6b-103">更新現有的伺服器。</span><span class="sxs-lookup"><span data-stu-id="6db6b-103">Updates an existing server.</span></span>
<span data-ttu-id="6db6b-104">要求主體可以包含一個到在一般伺服器定義中存在的許多屬性。</span><span class="sxs-lookup"><span data-stu-id="6db6b-104">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="6db6b-105">如果您想要補救伺服器參數（例如 wait_timeout 或 net_retry_count），請改用 Update-AzPostSqlFlexibleServerConfiguration。</span><span class="sxs-lookup"><span data-stu-id="6db6b-105">Use Update-AzPostSqlFlexibleServerConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="6db6b-106">句法</span><span class="sxs-lookup"><span data-stu-id="6db6b-106">SYNTAX</span></span>

### <span data-ttu-id="6db6b-107">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="6db6b-107">UpdateExpanded (Default)</span></span>
```
Update-AzPostgreSqlFlexibleServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AdministratorLoginPassword <SecureString>] [-BackupRetentionDay <Int32>] [-HaEnabled <HaEnabledEnum>]
 [-ReplicationRole <String>] [-Sku <String>] [-SkuTier <SkuTier>] [-SslEnforcement <SslEnforcementEnum>]
 [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6db6b-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="6db6b-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzPostgreSqlFlexibleServer -InputObject <IPostgreSqlIdentity>
 [-AdministratorLoginPassword <SecureString>] [-BackupRetentionDay <Int32>] [-HaEnabled <HaEnabledEnum>]
 [-ReplicationRole <String>] [-Sku <String>] [-SkuTier <SkuTier>] [-SslEnforcement <SslEnforcementEnum>]
 [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6db6b-109">說明</span><span class="sxs-lookup"><span data-stu-id="6db6b-109">DESCRIPTION</span></span>
<span data-ttu-id="6db6b-110">更新現有的伺服器。</span><span class="sxs-lookup"><span data-stu-id="6db6b-110">Updates an existing server.</span></span>
<span data-ttu-id="6db6b-111">要求主體可以包含一個到在一般伺服器定義中存在的許多屬性。</span><span class="sxs-lookup"><span data-stu-id="6db6b-111">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="6db6b-112">如果您想要補救伺服器參數（例如 wait_timeout 或 net_retry_count），請改用 Update-AzPostgreSqlFlexibleServerConfiguration。</span><span class="sxs-lookup"><span data-stu-id="6db6b-112">Use Update-AzPostgreSqlFlexibleServerConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="6db6b-113">示例</span><span class="sxs-lookup"><span data-stu-id="6db6b-113">EXAMPLES</span></span>

### <span data-ttu-id="6db6b-114">範例1：依資源群組和伺服器名稱更新 PostgreSql 伺服器</span><span class="sxs-lookup"><span data-stu-id="6db6b-114">Example 1: Update PostgreSql server by resource group and server name</span></span>
```powershell
PS C:\> Update-AzPostgreSqlFlexibleServer -ResourceGroupName PowershellPostgreSqlTest -Name postgresql-test -Sku Standard_D4s_v3

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- ---------------- -------------
postgresql-test eastus postgresql_test     12     131072                  Standard_D4s_v3 GeneralPurpose
```

<span data-ttu-id="6db6b-115">這個 Cmdlet 會依資源群組和伺服器名稱來更新 PostgreSql server。</span><span class="sxs-lookup"><span data-stu-id="6db6b-115">This cmdlet updates PostgreSql server by resource group and server name.</span></span>

### <span data-ttu-id="6db6b-116">範例2：依身分識別更新 PostgreSql 伺服器。</span><span class="sxs-lookup"><span data-stu-id="6db6b-116">Example 2: Update PostgreSql server by identity.</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFlexibleServer -ResourceGroupName PowershellPostgreSqlTest -ServerName postgresql-test | Update-AzPostgreSqlFlexibleServer -BackupRetentionDay 23 -StorageMb 10240

Name            Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----            -------- ------------------ ------- ----------------------- ---------------- -------------
postgresql-test eastus   postgresql_test     12     131072                  Standard_D2s_v3 GeneralPurpose
```

<span data-ttu-id="6db6b-117">這個 Cmdlet 會依身分識別來更新 PostgreSql 伺服器。</span><span class="sxs-lookup"><span data-stu-id="6db6b-117">This cmdlet updates PostgreSql server by identity.</span></span>

## <span data-ttu-id="6db6b-118">參數</span><span class="sxs-lookup"><span data-stu-id="6db6b-118">PARAMETERS</span></span>

### <span data-ttu-id="6db6b-119">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="6db6b-119">-AdministratorLoginPassword</span></span>
<span data-ttu-id="6db6b-120">系統管理員登入的密碼。</span><span class="sxs-lookup"><span data-stu-id="6db6b-120">The password of the administrator login.</span></span>

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

### <span data-ttu-id="6db6b-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6db6b-121">-AsJob</span></span>
<span data-ttu-id="6db6b-122">執行命令做為作業。</span><span class="sxs-lookup"><span data-stu-id="6db6b-122">Run the command as a job.</span></span>

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

### <span data-ttu-id="6db6b-123">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="6db6b-123">-BackupRetentionDay</span></span>
<span data-ttu-id="6db6b-124">伺服器的備份保留天數。</span><span class="sxs-lookup"><span data-stu-id="6db6b-124">Backup retention days for the server.</span></span>
<span data-ttu-id="6db6b-125">日算在7到35。</span><span class="sxs-lookup"><span data-stu-id="6db6b-125">Day count is between 7 and 35.</span></span>

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

### <span data-ttu-id="6db6b-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6db6b-126">-DefaultProfile</span></span>
<span data-ttu-id="6db6b-127">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6db6b-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6db6b-128">-HaEnabled</span><span class="sxs-lookup"><span data-stu-id="6db6b-128">-HaEnabled</span></span>
<span data-ttu-id="6db6b-129">啟用或停用高可用性功能。</span><span class="sxs-lookup"><span data-stu-id="6db6b-129">Enable or disable high availability feature.</span></span>

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

### <span data-ttu-id="6db6b-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6db6b-130">-InputObject</span></span>
<span data-ttu-id="6db6b-131">身分識別參數。</span><span class="sxs-lookup"><span data-stu-id="6db6b-131">Identity Parameter.</span></span>
<span data-ttu-id="6db6b-132">若要構造，請參閱適用于 INPUTOBJECT 屬性的 [記事] 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="6db6b-132">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="6db6b-133">-名稱</span><span class="sxs-lookup"><span data-stu-id="6db6b-133">-Name</span></span>
<span data-ttu-id="6db6b-134">伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="6db6b-134">The name of the server.</span></span>

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

### <span data-ttu-id="6db6b-135">-NoWait</span><span class="sxs-lookup"><span data-stu-id="6db6b-135">-NoWait</span></span>
<span data-ttu-id="6db6b-136">以非同步方式執行命令。</span><span class="sxs-lookup"><span data-stu-id="6db6b-136">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="6db6b-137">-ReplicationRole</span><span class="sxs-lookup"><span data-stu-id="6db6b-137">-ReplicationRole</span></span>
<span data-ttu-id="6db6b-138">伺服器的複製角色。</span><span class="sxs-lookup"><span data-stu-id="6db6b-138">The replication role of the server.</span></span>

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

### <span data-ttu-id="6db6b-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6db6b-139">-ResourceGroupName</span></span>
<span data-ttu-id="6db6b-140">包含資源之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6db6b-140">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="6db6b-141">您可以從 Azure 資源管理器 API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="6db6b-141">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="6db6b-142">-Sku</span><span class="sxs-lookup"><span data-stu-id="6db6b-142">-Sku</span></span>
<span data-ttu-id="6db6b-143">Sku 的名稱，通常是 [層 + 家庭 + 核心]，例如 B_Gen4_1、GP_Gen5_8。</span><span class="sxs-lookup"><span data-stu-id="6db6b-143">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="6db6b-144">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="6db6b-144">-SkuTier</span></span>
<span data-ttu-id="6db6b-145">特定 SKU 的層級，例如基本。</span><span class="sxs-lookup"><span data-stu-id="6db6b-145">The tier of the particular SKU, e.g. Basic.</span></span>

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

### <span data-ttu-id="6db6b-146">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="6db6b-146">-SslEnforcement</span></span>
<span data-ttu-id="6db6b-147">在連線至伺服器時啟用 ssl 強制執行。</span><span class="sxs-lookup"><span data-stu-id="6db6b-147">Enable ssl enforcement or not when connect to server.</span></span>

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

### <span data-ttu-id="6db6b-148">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="6db6b-148">-StorageAutogrow</span></span>
<span data-ttu-id="6db6b-149">啟用儲存空間自動增長。</span><span class="sxs-lookup"><span data-stu-id="6db6b-149">Enable Storage Auto Grow.</span></span>

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

### <span data-ttu-id="6db6b-150">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="6db6b-150">-StorageInMb</span></span>
<span data-ttu-id="6db6b-151">伺服器允許的最大儲存空間。</span><span class="sxs-lookup"><span data-stu-id="6db6b-151">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="6db6b-152">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6db6b-152">-SubscriptionId</span></span>
<span data-ttu-id="6db6b-153">識別 Azure 訂閱的訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="6db6b-153">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="6db6b-154">-Tag</span><span class="sxs-lookup"><span data-stu-id="6db6b-154">-Tag</span></span>
<span data-ttu-id="6db6b-155">以鍵值對形式的特定應用程式中繼資料。</span><span class="sxs-lookup"><span data-stu-id="6db6b-155">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="6db6b-156">-確認</span><span class="sxs-lookup"><span data-stu-id="6db6b-156">-Confirm</span></span>
<span data-ttu-id="6db6b-157">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6db6b-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6db6b-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6db6b-158">-WhatIf</span></span>
<span data-ttu-id="6db6b-159">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6db6b-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6db6b-160">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6db6b-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6db6b-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6db6b-161">CommonParameters</span></span>
<span data-ttu-id="6db6b-162">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6db6b-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6db6b-163">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="6db6b-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6db6b-164">輸入</span><span class="sxs-lookup"><span data-stu-id="6db6b-164">INPUTS</span></span>

### <span data-ttu-id="6db6b-165">IPostgreSqlIdentity （PostgreSql）的</span><span class="sxs-lookup"><span data-stu-id="6db6b-165">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="6db6b-166">輸出</span><span class="sxs-lookup"><span data-stu-id="6db6b-166">OUTPUTS</span></span>

### <span data-ttu-id="6db6b-167">IServerAutoGenerated （PostgreSql）。 Api20200214Preview。</span><span class="sxs-lookup"><span data-stu-id="6db6b-167">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.IServerAutoGenerated</span></span>

## <span data-ttu-id="6db6b-168">筆記</span><span class="sxs-lookup"><span data-stu-id="6db6b-168">NOTES</span></span>

<span data-ttu-id="6db6b-169">別名</span><span class="sxs-lookup"><span data-stu-id="6db6b-169">ALIASES</span></span>

<span data-ttu-id="6db6b-170">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="6db6b-170">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6db6b-171">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="6db6b-171">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6db6b-172">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="6db6b-172">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6db6b-173">INPUTOBJECT <IPostgreSqlIdentity> ：身分識別參數。</span><span class="sxs-lookup"><span data-stu-id="6db6b-173">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter.</span></span>
  - <span data-ttu-id="6db6b-174">`[ConfigurationName <String>]`：伺服器配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="6db6b-174">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="6db6b-175">`[DatabaseName <String>]`：資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="6db6b-175">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="6db6b-176">`[FirewallRuleName <String>]`：伺服器防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="6db6b-176">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="6db6b-177">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="6db6b-177">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6db6b-178">`[LocationName <String>]`：位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="6db6b-178">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="6db6b-179">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6db6b-179">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="6db6b-180">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="6db6b-180">The name is case insensitive.</span></span>
  - <span data-ttu-id="6db6b-181">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`：安全警示原則的名稱。</span><span class="sxs-lookup"><span data-stu-id="6db6b-181">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="6db6b-182">`[ServerName <String>]`：伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="6db6b-182">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="6db6b-183">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="6db6b-183">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="6db6b-184">`[VirtualNetworkRuleName <String>]`：虛擬網路規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="6db6b-184">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="6db6b-185">相關連結</span><span class="sxs-lookup"><span data-stu-id="6db6b-185">RELATED LINKS</span></span>

