---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/update-azmysqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlServer.md
ms.openlocfilehash: 46408fc5cd6f718f26c4f55eb7f8bab56891d8b5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906110"
---
# <span data-ttu-id="05862-101">Update-AzMySqlServer</span><span class="sxs-lookup"><span data-stu-id="05862-101">Update-AzMySqlServer</span></span>

## <span data-ttu-id="05862-102">簡介</span><span class="sxs-lookup"><span data-stu-id="05862-102">SYNOPSIS</span></span>
<span data-ttu-id="05862-103">更新現有的伺服器。</span><span class="sxs-lookup"><span data-stu-id="05862-103">Updates an existing server.</span></span>
<span data-ttu-id="05862-104">要求內內容可以包含一到多個標準伺服器定義中呈現的屬性。</span><span class="sxs-lookup"><span data-stu-id="05862-104">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="05862-105">如果您想要Update-AzMySqlConfiguration伺服器參數 ，例如補救伺服器參數，wait_timeout或net_retry_count。</span><span class="sxs-lookup"><span data-stu-id="05862-105">Use Update-AzMySqlConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="05862-106">語法</span><span class="sxs-lookup"><span data-stu-id="05862-106">SYNTAX</span></span>

### <span data-ttu-id="05862-107">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="05862-107">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AdministratorLoginPassword <SecureString>] [-BackupRetentionDay <Int32>]
 [-MinimalTlsVersion <MinimalTlsVersionEnum>] [-ReplicationRole <String>] [-Sku <String>]
 [-SkuCapacity <Int32>] [-SkuFamily <String>] [-SkuTier <SkuTier>] [-SslEnforcement <SslEnforcementEnum>]
 [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="05862-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="05862-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlServer -InputObject <IMySqlIdentity> [-AdministratorLoginPassword <SecureString>]
 [-BackupRetentionDay <Int32>] [-MinimalTlsVersion <MinimalTlsVersionEnum>] [-ReplicationRole <String>]
 [-Sku <String>] [-SkuCapacity <Int32>] [-SkuFamily <String>] [-SkuTier <SkuTier>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="05862-109">描述</span><span class="sxs-lookup"><span data-stu-id="05862-109">DESCRIPTION</span></span>
<span data-ttu-id="05862-110">更新現有的伺服器。</span><span class="sxs-lookup"><span data-stu-id="05862-110">Updates an existing server.</span></span>
<span data-ttu-id="05862-111">要求內內容可以包含一到多個標準伺服器定義中呈現的屬性。</span><span class="sxs-lookup"><span data-stu-id="05862-111">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="05862-112">如果您想要Update-AzMySqlConfiguration伺服器參數 ，例如補救伺服器參數，wait_timeout或net_retry_count。</span><span class="sxs-lookup"><span data-stu-id="05862-112">Use Update-AzMySqlConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="05862-113">例子</span><span class="sxs-lookup"><span data-stu-id="05862-113">EXAMPLES</span></span>

### <span data-ttu-id="05862-114">範例 1：根據資源群組和伺服器名稱更新 MySql 伺服器</span><span class="sxs-lookup"><span data-stu-id="05862-114">Example 1: Update MySql server by resource group and server name</span></span>
```powershell
PS C:\> Update-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -SslEnforcement Disabled

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test    eastus   mysql_test         5.7     5120                    GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="05862-115">此 Cmdlet 會根據資源群組和伺服器名稱更新 MySql 伺服器。</span><span class="sxs-lookup"><span data-stu-id="05862-115">This cmdlet updates MySql server by resource group and server name.</span></span>

### <span data-ttu-id="05862-116">範例 2：根據身分識別更新 MySql 伺服器。</span><span class="sxs-lookup"><span data-stu-id="05862-116">Example 2: Update MySql server by identity.</span></span>
```powershell
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test | Update-AzMySqlServer -BackupRetentionDay 23 -StorageMb 10240

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test    eastus   mysql_test         5.7     10240                   GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="05862-117">此 Cmdlet 會以身分識別更新 MySql 伺服器。</span><span class="sxs-lookup"><span data-stu-id="05862-117">This cmdlet updates MySql server by identity.</span></span>

## <span data-ttu-id="05862-118">參數</span><span class="sxs-lookup"><span data-stu-id="05862-118">PARAMETERS</span></span>

### <span data-ttu-id="05862-119">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="05862-119">-AdministratorLoginPassword</span></span>
<span data-ttu-id="05862-120">系統管理員登入的密碼。</span><span class="sxs-lookup"><span data-stu-id="05862-120">The password of the administrator login.</span></span>

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

### <span data-ttu-id="05862-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="05862-121">-AsJob</span></span>
<span data-ttu-id="05862-122">以工作執行命令。</span><span class="sxs-lookup"><span data-stu-id="05862-122">Run the command as a job.</span></span>

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

### <span data-ttu-id="05862-123">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="05862-123">-BackupRetentionDay</span></span>
<span data-ttu-id="05862-124">伺服器的備份保留天數。</span><span class="sxs-lookup"><span data-stu-id="05862-124">Backup retention days for the server.</span></span>
<span data-ttu-id="05862-125">日計數介於 7 到 35 之間。</span><span class="sxs-lookup"><span data-stu-id="05862-125">Day count is between 7 and 35.</span></span>

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

### <span data-ttu-id="05862-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05862-126">-DefaultProfile</span></span>
<span data-ttu-id="05862-127">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="05862-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="05862-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="05862-128">-InputObject</span></span>
<span data-ttu-id="05862-129">身分識別參數。</span><span class="sxs-lookup"><span data-stu-id="05862-129">Identity Parameter.</span></span>
<span data-ttu-id="05862-130">若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="05862-130">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="05862-131">-MinimalTlsVersion</span><span class="sxs-lookup"><span data-stu-id="05862-131">-MinimalTlsVersion</span></span>
<span data-ttu-id="05862-132">在啟用 SSL 時，設定伺服器連至伺服器的最小 TLS 版本。</span><span class="sxs-lookup"><span data-stu-id="05862-132">Set the minimal TLS version for connections to server when SSL is enabled.</span></span>
<span data-ttu-id="05862-133">預設值為 TLSEnforcementDisabled.accepted 值：TLS1_0、TLS1_1、TLS1_2、TLSEnforcementDisabled。</span><span class="sxs-lookup"><span data-stu-id="05862-133">Default is TLSEnforcementDisabled.accepted values: TLS1_0, TLS1_1, TLS1_2, TLSEnforcementDisabled.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Support.MinimalTlsVersionEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05862-134">-名稱</span><span class="sxs-lookup"><span data-stu-id="05862-134">-Name</span></span>
<span data-ttu-id="05862-135">伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="05862-135">The name of the server.</span></span>

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

### <span data-ttu-id="05862-136">-NoWait</span><span class="sxs-lookup"><span data-stu-id="05862-136">-NoWait</span></span>
<span data-ttu-id="05862-137">非同步執行命令。</span><span class="sxs-lookup"><span data-stu-id="05862-137">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="05862-138">-ReplicationRole</span><span class="sxs-lookup"><span data-stu-id="05862-138">-ReplicationRole</span></span>
<span data-ttu-id="05862-139">伺服器的複製角色。</span><span class="sxs-lookup"><span data-stu-id="05862-139">The replication role of the server.</span></span>

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

### <span data-ttu-id="05862-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05862-140">-ResourceGroupName</span></span>
<span data-ttu-id="05862-141">包含資源的資源組名。</span><span class="sxs-lookup"><span data-stu-id="05862-141">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="05862-142">您可以從 Azure Resource Manager API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="05862-142">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="05862-143">-SKU</span><span class="sxs-lookup"><span data-stu-id="05862-143">-Sku</span></span>
<span data-ttu-id="05862-144">SKU 的名稱，通常是 tier + family + 核心，例如 B_Gen4_1、GP_Gen5_8。</span><span class="sxs-lookup"><span data-stu-id="05862-144">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="05862-145">-Sku以</span><span class="sxs-lookup"><span data-stu-id="05862-145">-SkuCapacity</span></span>
<span data-ttu-id="05862-146">向上/縮小容量，代表伺服器的計算單位。</span><span class="sxs-lookup"><span data-stu-id="05862-146">The scale up/out capacity, representing server's compute units.</span></span>

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

### <span data-ttu-id="05862-147">-SkuFamily</span><span class="sxs-lookup"><span data-stu-id="05862-147">-SkuFamily</span></span>
<span data-ttu-id="05862-148">硬體系列。</span><span class="sxs-lookup"><span data-stu-id="05862-148">The family of hardware.</span></span>

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

### <span data-ttu-id="05862-149">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="05862-149">-SkuTier</span></span>
<span data-ttu-id="05862-150">特定 SKU 的層級，例如基本。</span><span class="sxs-lookup"><span data-stu-id="05862-150">The tier of the particular SKU, e.g. Basic.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Support.SkuTier
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05862-151">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="05862-151">-SslEnforcement</span></span>
<span data-ttu-id="05862-152">在連接至伺服器時啟用 ssl 強制執行或不啟用。</span><span class="sxs-lookup"><span data-stu-id="05862-152">Enable ssl enforcement or not when connect to server.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Support.SslEnforcementEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05862-153">-StorageAuto上</span><span class="sxs-lookup"><span data-stu-id="05862-153">-StorageAutogrow</span></span>
<span data-ttu-id="05862-154">啟用儲存空間自動放大。</span><span class="sxs-lookup"><span data-stu-id="05862-154">Enable Storage Auto Grow.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Support.StorageAutogrow
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05862-155">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="05862-155">-StorageInMb</span></span>
<span data-ttu-id="05862-156">伺服器允許的最大儲存空間。</span><span class="sxs-lookup"><span data-stu-id="05862-156">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="05862-157">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="05862-157">-SubscriptionId</span></span>
<span data-ttu-id="05862-158">可識別 Azure 訂閱的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="05862-158">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="05862-159">-標記</span><span class="sxs-lookup"><span data-stu-id="05862-159">-Tag</span></span>
<span data-ttu-id="05862-160">以金鑰值組形式顯示的應用程式特定中繼資料。</span><span class="sxs-lookup"><span data-stu-id="05862-160">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="05862-161">-確認</span><span class="sxs-lookup"><span data-stu-id="05862-161">-Confirm</span></span>
<span data-ttu-id="05862-162">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="05862-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05862-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05862-163">-WhatIf</span></span>
<span data-ttu-id="05862-164">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="05862-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05862-165">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="05862-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05862-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05862-166">CommonParameters</span></span>
<span data-ttu-id="05862-167">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="05862-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05862-168">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="05862-168">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05862-169">輸入</span><span class="sxs-lookup"><span data-stu-id="05862-169">INPUTS</span></span>

### <span data-ttu-id="05862-170">Microsoft.Azure.PowerShell.Cmdlets.MySql.models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="05862-170">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="05862-171">輸出</span><span class="sxs-lookup"><span data-stu-id="05862-171">OUTPUTS</span></span>

### <span data-ttu-id="05862-172">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="05862-172">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="05862-173">筆記</span><span class="sxs-lookup"><span data-stu-id="05862-173">NOTES</span></span>

<span data-ttu-id="05862-174">別名</span><span class="sxs-lookup"><span data-stu-id="05862-174">ALIASES</span></span>

<span data-ttu-id="05862-175">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="05862-175">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="05862-176">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="05862-176">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="05862-177">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="05862-177">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="05862-178">INPUTOBJECT： <IMySqlIdentity> 身分識別參數。</span><span class="sxs-lookup"><span data-stu-id="05862-178">INPUTOBJECT <IMySqlIdentity>: Identity Parameter.</span></span>
  - <span data-ttu-id="05862-179">`[ConfigurationName <String>]`：伺服器組組的名稱。</span><span class="sxs-lookup"><span data-stu-id="05862-179">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="05862-180">`[DatabaseName <String>]`：資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="05862-180">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="05862-181">`[FirewallRuleName <String>]`：伺服器防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="05862-181">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="05862-182">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="05862-182">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="05862-183">`[KeyName <String>]`：伺服器金鑰的名稱。</span><span class="sxs-lookup"><span data-stu-id="05862-183">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="05862-184">`[LocationName <String>]`：位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="05862-184">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="05862-185">`[ResourceGroupName <String>]`：資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="05862-185">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="05862-186">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="05862-186">The name is case insensitive.</span></span>
  - <span data-ttu-id="05862-187">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`：安全性警示策略的名稱。</span><span class="sxs-lookup"><span data-stu-id="05862-187">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="05862-188">`[ServerName <String>]`：伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="05862-188">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="05862-189">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="05862-189">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="05862-190">`[VirtualNetworkRuleName <String>]`：虛擬網路規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="05862-190">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="05862-191">相關連結</span><span class="sxs-lookup"><span data-stu-id="05862-191">RELATED LINKS</span></span>

