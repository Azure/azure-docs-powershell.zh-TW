---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/update-azmysqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlServer.md
ms.openlocfilehash: 6168c557e3ae3a417f4c04195e6ef166ea3a01d8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100134027"
---
# <span data-ttu-id="ca8b1-101">Update-AzMySqlServer</span><span class="sxs-lookup"><span data-stu-id="ca8b1-101">Update-AzMySqlServer</span></span>

## <span data-ttu-id="ca8b1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ca8b1-102">SYNOPSIS</span></span>
<span data-ttu-id="ca8b1-103">更新現有的伺服器。</span><span class="sxs-lookup"><span data-stu-id="ca8b1-103">Updates an existing server.</span></span>
<span data-ttu-id="ca8b1-104">要求主體可以包含一個到在一般伺服器定義中存在的許多屬性。</span><span class="sxs-lookup"><span data-stu-id="ca8b1-104">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="ca8b1-105">如果您想要補救伺服器參數（例如 wait_timeout 或 net_retry_count），請改用 Update-AzMySqlConfiguration。</span><span class="sxs-lookup"><span data-stu-id="ca8b1-105">Use Update-AzMySqlConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="ca8b1-106">句法</span><span class="sxs-lookup"><span data-stu-id="ca8b1-106">SYNTAX</span></span>

### <span data-ttu-id="ca8b1-107">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="ca8b1-107">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AdministratorLoginPassword <SecureString>] [-BackupRetentionDay <Int32>]
 [-MinimalTlsVersion <MinimalTlsVersionEnum>] [-ReplicationRole <String>] [-Sku <String>]
 [-SkuCapacity <Int32>] [-SkuFamily <String>] [-SkuTier <SkuTier>] [-SslEnforcement <SslEnforcementEnum>]
 [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ca8b1-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="ca8b1-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlServer -InputObject <IMySqlIdentity> [-AdministratorLoginPassword <SecureString>]
 [-BackupRetentionDay <Int32>] [-MinimalTlsVersion <MinimalTlsVersionEnum>] [-ReplicationRole <String>]
 [-Sku <String>] [-SkuCapacity <Int32>] [-SkuFamily <String>] [-SkuTier <SkuTier>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ca8b1-109">說明</span><span class="sxs-lookup"><span data-stu-id="ca8b1-109">DESCRIPTION</span></span>
<span data-ttu-id="ca8b1-110">更新現有的伺服器。</span><span class="sxs-lookup"><span data-stu-id="ca8b1-110">Updates an existing server.</span></span>
<span data-ttu-id="ca8b1-111">要求主體可以包含一個到在一般伺服器定義中存在的許多屬性。</span><span class="sxs-lookup"><span data-stu-id="ca8b1-111">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="ca8b1-112">如果您想要補救伺服器參數（例如 wait_timeout 或 net_retry_count），請改用 Update-AzMySqlConfiguration。</span><span class="sxs-lookup"><span data-stu-id="ca8b1-112">Use Update-AzMySqlConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="ca8b1-113">示例</span><span class="sxs-lookup"><span data-stu-id="ca8b1-113">EXAMPLES</span></span>

### <span data-ttu-id="ca8b1-114">範例1：依資源群組和伺服器名稱更新 MySql 伺服器</span><span class="sxs-lookup"><span data-stu-id="ca8b1-114">Example 1: Update MySql server by resource group and server name</span></span>
```powershell
PS C:\> Update-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -SslEnforcement Disabled

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test    eastus   mysql_test         5.7     5120                    GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="ca8b1-115">這個 Cmdlet 會依資源群組和伺服器名稱更新 MySql 伺服器。</span><span class="sxs-lookup"><span data-stu-id="ca8b1-115">This cmdlet updates MySql server by resource group and server name.</span></span>

### <span data-ttu-id="ca8b1-116">範例2：依身分識別更新 MySql 伺服器。</span><span class="sxs-lookup"><span data-stu-id="ca8b1-116">Example 2: Update MySql server by identity.</span></span>
```powershell
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test | Update-AzMySqlServer -BackupRetentionDay 23 -StorageMb 10240

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test    eastus   mysql_test         5.7     10240                   GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="ca8b1-117">這個 Cmdlet 會依身分識別更新 MySql 伺服器。</span><span class="sxs-lookup"><span data-stu-id="ca8b1-117">This cmdlet updates MySql server by identity.</span></span>

## <span data-ttu-id="ca8b1-118">參數</span><span class="sxs-lookup"><span data-stu-id="ca8b1-118">PARAMETERS</span></span>

### <span data-ttu-id="ca8b1-119">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="ca8b1-119">-AdministratorLoginPassword</span></span>
<span data-ttu-id="ca8b1-120">系統管理員登入的密碼。</span><span class="sxs-lookup"><span data-stu-id="ca8b1-120">The password of the administrator login.</span></span>

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

### <span data-ttu-id="ca8b1-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ca8b1-121">-AsJob</span></span>
<span data-ttu-id="ca8b1-122">執行命令做為作業。</span><span class="sxs-lookup"><span data-stu-id="ca8b1-122">Run the command as a job.</span></span>

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

### <span data-ttu-id="ca8b1-123">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="ca8b1-123">-BackupRetentionDay</span></span>
<span data-ttu-id="ca8b1-124">伺服器的備份保留天數。</span><span class="sxs-lookup"><span data-stu-id="ca8b1-124">Backup retention days for the server.</span></span>
<span data-ttu-id="ca8b1-125">日算在7到35。</span><span class="sxs-lookup"><span data-stu-id="ca8b1-125">Day count is between 7 and 35.</span></span>

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

### <span data-ttu-id="ca8b1-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca8b1-126">-DefaultProfile</span></span>
<span data-ttu-id="ca8b1-127">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ca8b1-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca8b1-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ca8b1-128">-InputObject</span></span>
<span data-ttu-id="ca8b1-129">身分識別參數。</span><span class="sxs-lookup"><span data-stu-id="ca8b1-129">Identity Parameter.</span></span>
<span data-ttu-id="ca8b1-130">若要構造，請參閱適用于 INPUTOBJECT 屬性的 [記事] 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="ca8b1-130">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ca8b1-131">-MinimalTlsVersion</span><span class="sxs-lookup"><span data-stu-id="ca8b1-131">-MinimalTlsVersion</span></span>
<span data-ttu-id="ca8b1-132">設定啟用 SSL 時連線至伺服器的最小 TLS 版本。</span><span class="sxs-lookup"><span data-stu-id="ca8b1-132">Set the minimal TLS version for connections to server when SSL is enabled.</span></span>
<span data-ttu-id="ca8b1-133">預設值為 TLSEnforcementDisabled。可接受的值： TLS1_0、TLS1_1、TLS1_2、TLSEnforcementDisabled。</span><span class="sxs-lookup"><span data-stu-id="ca8b1-133">Default is TLSEnforcementDisabled.accepted values: TLS1_0, TLS1_1, TLS1_2, TLSEnforcementDisabled.</span></span>

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

### <span data-ttu-id="ca8b1-134">-名稱</span><span class="sxs-lookup"><span data-stu-id="ca8b1-134">-Name</span></span>
<span data-ttu-id="ca8b1-135">伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="ca8b1-135">The name of the server.</span></span>

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

### <span data-ttu-id="ca8b1-136">-NoWait</span><span class="sxs-lookup"><span data-stu-id="ca8b1-136">-NoWait</span></span>
<span data-ttu-id="ca8b1-137">以非同步方式執行命令。</span><span class="sxs-lookup"><span data-stu-id="ca8b1-137">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="ca8b1-138">-ReplicationRole</span><span class="sxs-lookup"><span data-stu-id="ca8b1-138">-ReplicationRole</span></span>
<span data-ttu-id="ca8b1-139">伺服器的複製角色。</span><span class="sxs-lookup"><span data-stu-id="ca8b1-139">The replication role of the server.</span></span>

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

### <span data-ttu-id="ca8b1-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca8b1-140">-ResourceGroupName</span></span>
<span data-ttu-id="ca8b1-141">包含資源之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ca8b1-141">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="ca8b1-142">您可以從 Azure 資源管理器 API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="ca8b1-142">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="ca8b1-143">-Sku</span><span class="sxs-lookup"><span data-stu-id="ca8b1-143">-Sku</span></span>
<span data-ttu-id="ca8b1-144">Sku 的名稱，通常是 [層 + 家庭 + 核心]，例如 B_Gen4_1、GP_Gen5_8。</span><span class="sxs-lookup"><span data-stu-id="ca8b1-144">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="ca8b1-145">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="ca8b1-145">-SkuCapacity</span></span>
<span data-ttu-id="ca8b1-146">[擴大/縮小] 容量，代表伺服器的計算單位。</span><span class="sxs-lookup"><span data-stu-id="ca8b1-146">The scale up/out capacity, representing server's compute units.</span></span>

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

### <span data-ttu-id="ca8b1-147">-SkuFamily</span><span class="sxs-lookup"><span data-stu-id="ca8b1-147">-SkuFamily</span></span>
<span data-ttu-id="ca8b1-148">硬體系列。</span><span class="sxs-lookup"><span data-stu-id="ca8b1-148">The family of hardware.</span></span>

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

### <span data-ttu-id="ca8b1-149">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="ca8b1-149">-SkuTier</span></span>
<span data-ttu-id="ca8b1-150">特定 SKU 的層級，例如基本。</span><span class="sxs-lookup"><span data-stu-id="ca8b1-150">The tier of the particular SKU, e.g. Basic.</span></span>

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

### <span data-ttu-id="ca8b1-151">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="ca8b1-151">-SslEnforcement</span></span>
<span data-ttu-id="ca8b1-152">在連線至伺服器時啟用 ssl 強制執行。</span><span class="sxs-lookup"><span data-stu-id="ca8b1-152">Enable ssl enforcement or not when connect to server.</span></span>

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

### <span data-ttu-id="ca8b1-153">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="ca8b1-153">-StorageAutogrow</span></span>
<span data-ttu-id="ca8b1-154">啟用儲存空間自動增長。</span><span class="sxs-lookup"><span data-stu-id="ca8b1-154">Enable Storage Auto Grow.</span></span>

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

### <span data-ttu-id="ca8b1-155">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="ca8b1-155">-StorageInMb</span></span>
<span data-ttu-id="ca8b1-156">伺服器允許的最大儲存空間。</span><span class="sxs-lookup"><span data-stu-id="ca8b1-156">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="ca8b1-157">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ca8b1-157">-SubscriptionId</span></span>
<span data-ttu-id="ca8b1-158">識別 Azure 訂閱的訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="ca8b1-158">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="ca8b1-159">-Tag</span><span class="sxs-lookup"><span data-stu-id="ca8b1-159">-Tag</span></span>
<span data-ttu-id="ca8b1-160">以鍵值對形式的特定應用程式中繼資料。</span><span class="sxs-lookup"><span data-stu-id="ca8b1-160">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="ca8b1-161">-確認</span><span class="sxs-lookup"><span data-stu-id="ca8b1-161">-Confirm</span></span>
<span data-ttu-id="ca8b1-162">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ca8b1-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca8b1-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca8b1-163">-WhatIf</span></span>
<span data-ttu-id="ca8b1-164">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ca8b1-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca8b1-165">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ca8b1-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca8b1-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca8b1-166">CommonParameters</span></span>
<span data-ttu-id="ca8b1-167">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ca8b1-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca8b1-168">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ca8b1-168">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca8b1-169">輸入</span><span class="sxs-lookup"><span data-stu-id="ca8b1-169">INPUTS</span></span>

### <span data-ttu-id="ca8b1-170">IMySqlIdentity 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="ca8b1-170">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="ca8b1-171">輸出</span><span class="sxs-lookup"><span data-stu-id="ca8b1-171">OUTPUTS</span></span>

### <span data-ttu-id="ca8b1-172">IServer 中的 Api20171201 （）。</span><span class="sxs-lookup"><span data-stu-id="ca8b1-172">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="ca8b1-173">筆記</span><span class="sxs-lookup"><span data-stu-id="ca8b1-173">NOTES</span></span>

<span data-ttu-id="ca8b1-174">別名</span><span class="sxs-lookup"><span data-stu-id="ca8b1-174">ALIASES</span></span>

<span data-ttu-id="ca8b1-175">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="ca8b1-175">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ca8b1-176">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="ca8b1-176">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ca8b1-177">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="ca8b1-177">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ca8b1-178">INPUTOBJECT <IMySqlIdentity> ：身分識別參數。</span><span class="sxs-lookup"><span data-stu-id="ca8b1-178">INPUTOBJECT <IMySqlIdentity>: Identity Parameter.</span></span>
  - <span data-ttu-id="ca8b1-179">`[ConfigurationName <String>]`：伺服器配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="ca8b1-179">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="ca8b1-180">`[DatabaseName <String>]`：資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="ca8b1-180">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="ca8b1-181">`[FirewallRuleName <String>]`：伺服器防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="ca8b1-181">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="ca8b1-182">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="ca8b1-182">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ca8b1-183">`[KeyName <String>]`：伺服器金鑰的名稱。</span><span class="sxs-lookup"><span data-stu-id="ca8b1-183">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="ca8b1-184">`[LocationName <String>]`：位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="ca8b1-184">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="ca8b1-185">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ca8b1-185">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="ca8b1-186">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="ca8b1-186">The name is case insensitive.</span></span>
  - <span data-ttu-id="ca8b1-187">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`：安全警示原則的名稱。</span><span class="sxs-lookup"><span data-stu-id="ca8b1-187">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="ca8b1-188">`[ServerName <String>]`：伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="ca8b1-188">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="ca8b1-189">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="ca8b1-189">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="ca8b1-190">`[VirtualNetworkRuleName <String>]`：虛擬網路規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="ca8b1-190">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="ca8b1-191">相關連結</span><span class="sxs-lookup"><span data-stu-id="ca8b1-191">RELATED LINKS</span></span>

