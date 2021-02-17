---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/update-azpostgresqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlServer.md
ms.openlocfilehash: 4b0d2f01336de83acbd904e08b0d0cbc62c0aca6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100140103"
---
# <span data-ttu-id="65c0a-101">Update-AzPostgreSqlServer</span><span class="sxs-lookup"><span data-stu-id="65c0a-101">Update-AzPostgreSqlServer</span></span>

## <span data-ttu-id="65c0a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="65c0a-102">SYNOPSIS</span></span>
<span data-ttu-id="65c0a-103">更新現有的伺服器。</span><span class="sxs-lookup"><span data-stu-id="65c0a-103">Updates an existing server.</span></span>
<span data-ttu-id="65c0a-104">要求主體可以包含一個到在一般伺服器定義中存在的許多屬性。</span><span class="sxs-lookup"><span data-stu-id="65c0a-104">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="65c0a-105">如果您想要補救伺服器參數（例如 wait_timeout 或 net_retry_count），請改用 Update-AzPostSqlConfiguration。</span><span class="sxs-lookup"><span data-stu-id="65c0a-105">Use Update-AzPostSqlConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="65c0a-106">句法</span><span class="sxs-lookup"><span data-stu-id="65c0a-106">SYNTAX</span></span>

### <span data-ttu-id="65c0a-107">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="65c0a-107">UpdateExpanded (Default)</span></span>
```
Update-AzPostgreSqlServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AdministratorLoginPassword <SecureString>] [-BackupRetentionDay <Int32>]
 [-MinimalTlsVersion <MinimalTlsVersionEnum>] [-ReplicationRole <String>] [-Sku <String>]
 [-SkuCapacity <Int32>] [-SkuFamily <String>] [-SkuTier <SkuTier>] [-SslEnforcement <SslEnforcementEnum>]
 [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="65c0a-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="65c0a-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzPostgreSqlServer -InputObject <IPostgreSqlIdentity> [-AdministratorLoginPassword <SecureString>]
 [-BackupRetentionDay <Int32>] [-MinimalTlsVersion <MinimalTlsVersionEnum>] [-ReplicationRole <String>]
 [-Sku <String>] [-SkuCapacity <Int32>] [-SkuFamily <String>] [-SkuTier <SkuTier>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="65c0a-109">說明</span><span class="sxs-lookup"><span data-stu-id="65c0a-109">DESCRIPTION</span></span>
<span data-ttu-id="65c0a-110">更新現有的伺服器。</span><span class="sxs-lookup"><span data-stu-id="65c0a-110">Updates an existing server.</span></span>
<span data-ttu-id="65c0a-111">要求主體可以包含一個到在一般伺服器定義中存在的許多屬性。</span><span class="sxs-lookup"><span data-stu-id="65c0a-111">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="65c0a-112">如果您想要補救伺服器參數（例如 wait_timeout 或 net_retry_count），請改用 Update-AzPostSqlConfiguration。</span><span class="sxs-lookup"><span data-stu-id="65c0a-112">Use Update-AzPostSqlConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="65c0a-113">示例</span><span class="sxs-lookup"><span data-stu-id="65c0a-113">EXAMPLES</span></span>

### <span data-ttu-id="65c0a-114">範例1：依資源群組和伺服器名稱更新 PostgreSql 伺服器</span><span class="sxs-lookup"><span data-stu-id="65c0a-114">Example 1: Update PostgreSql server by resource group and server name</span></span>
```powershell
PS C:\> Update-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -SslEnforcement Disabled

Name                 Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                 -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="65c0a-115">這個 Cmdlet 會依資源群組和伺服器名稱來更新 PostgreSql server。</span><span class="sxs-lookup"><span data-stu-id="65c0a-115">This cmdlet updates PostgreSql server by resource group and server name.</span></span>

### <span data-ttu-id="65c0a-116">範例2：依身分識別更新 PostgreSql 伺服器。</span><span class="sxs-lookup"><span data-stu-id="65c0a-116">Example 2: Update PostgreSql server by identity.</span></span>
```powershell
PS C:\> Get-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer | Update-AzPostgreSqlServer -BackupRetentionDay 23

Name                 Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                 -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="65c0a-117">這個 Cmdlet 會依身分識別來更新 PostgreSql 伺服器。</span><span class="sxs-lookup"><span data-stu-id="65c0a-117">This cmdlet updates PostgreSql server by identity.</span></span>

## <span data-ttu-id="65c0a-118">參數</span><span class="sxs-lookup"><span data-stu-id="65c0a-118">PARAMETERS</span></span>

### <span data-ttu-id="65c0a-119">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="65c0a-119">-AdministratorLoginPassword</span></span>
<span data-ttu-id="65c0a-120">系統管理員登入的密碼。</span><span class="sxs-lookup"><span data-stu-id="65c0a-120">The password of the administrator login.</span></span>

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

### <span data-ttu-id="65c0a-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="65c0a-121">-AsJob</span></span>
<span data-ttu-id="65c0a-122">執行命令做為作業。</span><span class="sxs-lookup"><span data-stu-id="65c0a-122">Run the command as a job.</span></span>

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

### <span data-ttu-id="65c0a-123">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="65c0a-123">-BackupRetentionDay</span></span>
<span data-ttu-id="65c0a-124">伺服器的備份保留天數。</span><span class="sxs-lookup"><span data-stu-id="65c0a-124">Backup retention days for the server.</span></span>
<span data-ttu-id="65c0a-125">日算在7到35。</span><span class="sxs-lookup"><span data-stu-id="65c0a-125">Day count is between 7 and 35.</span></span>

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

### <span data-ttu-id="65c0a-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65c0a-126">-DefaultProfile</span></span>
<span data-ttu-id="65c0a-127">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="65c0a-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65c0a-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="65c0a-128">-InputObject</span></span>
<span data-ttu-id="65c0a-129">身分識別參數。</span><span class="sxs-lookup"><span data-stu-id="65c0a-129">Identity Parameter.</span></span>
<span data-ttu-id="65c0a-130">若要構造，請參閱適用于 INPUTOBJECT 屬性的 [記事] 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="65c0a-130">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="65c0a-131">-MinimalTlsVersion</span><span class="sxs-lookup"><span data-stu-id="65c0a-131">-MinimalTlsVersion</span></span>
<span data-ttu-id="65c0a-132">設定啟用 SSL 時連線至伺服器的最小 TLS 版本。</span><span class="sxs-lookup"><span data-stu-id="65c0a-132">Set the minimal TLS version for connections to server when SSL is enabled.</span></span>
<span data-ttu-id="65c0a-133">預設值為 TLSEnforcementDisabled。可接受的值： TLS1_0、TLS1_1、TLS1_2、TLSEnforcementDisabled。</span><span class="sxs-lookup"><span data-stu-id="65c0a-133">Default is TLSEnforcementDisabled.accepted values: TLS1_0, TLS1_1, TLS1_2, TLSEnforcementDisabled.</span></span>

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

### <span data-ttu-id="65c0a-134">-名稱</span><span class="sxs-lookup"><span data-stu-id="65c0a-134">-Name</span></span>
<span data-ttu-id="65c0a-135">伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="65c0a-135">The name of the server.</span></span>

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

### <span data-ttu-id="65c0a-136">-NoWait</span><span class="sxs-lookup"><span data-stu-id="65c0a-136">-NoWait</span></span>
<span data-ttu-id="65c0a-137">以非同步方式執行命令。</span><span class="sxs-lookup"><span data-stu-id="65c0a-137">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="65c0a-138">-ReplicationRole</span><span class="sxs-lookup"><span data-stu-id="65c0a-138">-ReplicationRole</span></span>
<span data-ttu-id="65c0a-139">伺服器的複製角色。</span><span class="sxs-lookup"><span data-stu-id="65c0a-139">The replication role of the server.</span></span>

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

### <span data-ttu-id="65c0a-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65c0a-140">-ResourceGroupName</span></span>
<span data-ttu-id="65c0a-141">包含資源之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="65c0a-141">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="65c0a-142">您可以從 Azure 資源管理器 API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="65c0a-142">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="65c0a-143">-Sku</span><span class="sxs-lookup"><span data-stu-id="65c0a-143">-Sku</span></span>
<span data-ttu-id="65c0a-144">Sku 的名稱，通常是 [層 + 家庭 + 核心]，例如 B_Gen4_1、GP_Gen5_8。</span><span class="sxs-lookup"><span data-stu-id="65c0a-144">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="65c0a-145">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="65c0a-145">-SkuCapacity</span></span>
<span data-ttu-id="65c0a-146">[擴大/縮小] 容量，代表伺服器的計算單位。</span><span class="sxs-lookup"><span data-stu-id="65c0a-146">The scale up/out capacity, representing server's compute units.</span></span>

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

### <span data-ttu-id="65c0a-147">-SkuFamily</span><span class="sxs-lookup"><span data-stu-id="65c0a-147">-SkuFamily</span></span>
<span data-ttu-id="65c0a-148">硬體系列。</span><span class="sxs-lookup"><span data-stu-id="65c0a-148">The family of hardware.</span></span>

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

### <span data-ttu-id="65c0a-149">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="65c0a-149">-SkuTier</span></span>
<span data-ttu-id="65c0a-150">特定 SKU 的層級，例如基本。</span><span class="sxs-lookup"><span data-stu-id="65c0a-150">The tier of the particular SKU, e.g. Basic.</span></span>

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

### <span data-ttu-id="65c0a-151">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="65c0a-151">-SslEnforcement</span></span>
<span data-ttu-id="65c0a-152">在連線至伺服器時啟用 ssl 強制執行。</span><span class="sxs-lookup"><span data-stu-id="65c0a-152">Enable ssl enforcement or not when connect to server.</span></span>

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

### <span data-ttu-id="65c0a-153">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="65c0a-153">-StorageAutogrow</span></span>
<span data-ttu-id="65c0a-154">啟用儲存空間自動增長。</span><span class="sxs-lookup"><span data-stu-id="65c0a-154">Enable Storage Auto Grow.</span></span>

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

### <span data-ttu-id="65c0a-155">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="65c0a-155">-StorageInMb</span></span>
<span data-ttu-id="65c0a-156">伺服器允許的最大儲存空間。</span><span class="sxs-lookup"><span data-stu-id="65c0a-156">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="65c0a-157">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="65c0a-157">-SubscriptionId</span></span>
<span data-ttu-id="65c0a-158">識別 Azure 訂閱的訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="65c0a-158">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="65c0a-159">-Tag</span><span class="sxs-lookup"><span data-stu-id="65c0a-159">-Tag</span></span>
<span data-ttu-id="65c0a-160">以鍵值對形式的特定應用程式中繼資料。</span><span class="sxs-lookup"><span data-stu-id="65c0a-160">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="65c0a-161">-確認</span><span class="sxs-lookup"><span data-stu-id="65c0a-161">-Confirm</span></span>
<span data-ttu-id="65c0a-162">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="65c0a-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65c0a-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65c0a-163">-WhatIf</span></span>
<span data-ttu-id="65c0a-164">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="65c0a-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65c0a-165">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="65c0a-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65c0a-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65c0a-166">CommonParameters</span></span>
<span data-ttu-id="65c0a-167">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="65c0a-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65c0a-168">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="65c0a-168">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65c0a-169">輸入</span><span class="sxs-lookup"><span data-stu-id="65c0a-169">INPUTS</span></span>

### <span data-ttu-id="65c0a-170">IPostgreSqlIdentity （PostgreSql）的</span><span class="sxs-lookup"><span data-stu-id="65c0a-170">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="65c0a-171">輸出</span><span class="sxs-lookup"><span data-stu-id="65c0a-171">OUTPUTS</span></span>

### <span data-ttu-id="65c0a-172">IServer （PostgreSql）。 Api20171201。</span><span class="sxs-lookup"><span data-stu-id="65c0a-172">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="65c0a-173">筆記</span><span class="sxs-lookup"><span data-stu-id="65c0a-173">NOTES</span></span>

<span data-ttu-id="65c0a-174">別名</span><span class="sxs-lookup"><span data-stu-id="65c0a-174">ALIASES</span></span>

<span data-ttu-id="65c0a-175">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="65c0a-175">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="65c0a-176">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="65c0a-176">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="65c0a-177">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="65c0a-177">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="65c0a-178">INPUTOBJECT <IPostgreSqlIdentity> ：身分識別參數。</span><span class="sxs-lookup"><span data-stu-id="65c0a-178">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter.</span></span>
  - <span data-ttu-id="65c0a-179">`[ConfigurationName <String>]`：伺服器配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="65c0a-179">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="65c0a-180">`[DatabaseName <String>]`：資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="65c0a-180">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="65c0a-181">`[FirewallRuleName <String>]`：伺服器防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="65c0a-181">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="65c0a-182">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="65c0a-182">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="65c0a-183">`[LocationName <String>]`：位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="65c0a-183">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="65c0a-184">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="65c0a-184">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="65c0a-185">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="65c0a-185">The name is case insensitive.</span></span>
  - <span data-ttu-id="65c0a-186">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`：安全警示原則的名稱。</span><span class="sxs-lookup"><span data-stu-id="65c0a-186">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="65c0a-187">`[ServerName <String>]`：伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="65c0a-187">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="65c0a-188">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="65c0a-188">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="65c0a-189">`[VirtualNetworkRuleName <String>]`：虛擬網路規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="65c0a-189">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="65c0a-190">相關連結</span><span class="sxs-lookup"><span data-stu-id="65c0a-190">RELATED LINKS</span></span>

