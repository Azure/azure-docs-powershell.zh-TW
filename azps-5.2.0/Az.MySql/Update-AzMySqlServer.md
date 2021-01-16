---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/update-azmysqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlServer.md
ms.openlocfilehash: b205f3d4eb9b1ebce360596714ea2524fb2e3be2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98281800"
---
# <span data-ttu-id="c2aae-101">Update-AzMySqlServer</span><span class="sxs-lookup"><span data-stu-id="c2aae-101">Update-AzMySqlServer</span></span>

## <span data-ttu-id="c2aae-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c2aae-102">SYNOPSIS</span></span>
<span data-ttu-id="c2aae-103">更新現有的伺服器。</span><span class="sxs-lookup"><span data-stu-id="c2aae-103">Updates an existing server.</span></span>
<span data-ttu-id="c2aae-104">要求主體可以包含一個到在一般伺服器定義中存在的許多屬性。</span><span class="sxs-lookup"><span data-stu-id="c2aae-104">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="c2aae-105">如果您想要補救伺服器參數（例如 wait_timeout 或 net_retry_count），請改用 Update-AzMySqlConfiguration。</span><span class="sxs-lookup"><span data-stu-id="c2aae-105">Use Update-AzMySqlConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="c2aae-106">句法</span><span class="sxs-lookup"><span data-stu-id="c2aae-106">SYNTAX</span></span>

### <span data-ttu-id="c2aae-107">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="c2aae-107">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AdministratorLoginPassword <SecureString>] [-BackupRetentionDay <Int32>] [-ReplicationRole <String>]
 [-Sku <String>] [-SkuCapacity <Int32>] [-SkuFamily <String>] [-SkuTier <SkuTier>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c2aae-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="c2aae-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlServer -InputObject <IMySqlIdentity> [-AdministratorLoginPassword <SecureString>]
 [-BackupRetentionDay <Int32>] [-ReplicationRole <String>] [-Sku <String>] [-SkuCapacity <Int32>]
 [-SkuFamily <String>] [-SkuTier <SkuTier>] [-SslEnforcement <SslEnforcementEnum>]
 [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c2aae-109">說明</span><span class="sxs-lookup"><span data-stu-id="c2aae-109">DESCRIPTION</span></span>
<span data-ttu-id="c2aae-110">更新現有的伺服器。</span><span class="sxs-lookup"><span data-stu-id="c2aae-110">Updates an existing server.</span></span>
<span data-ttu-id="c2aae-111">要求主體可以包含一個到在一般伺服器定義中存在的許多屬性。</span><span class="sxs-lookup"><span data-stu-id="c2aae-111">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="c2aae-112">如果您想要補救伺服器參數（例如 wait_timeout 或 net_retry_count），請改用 Update-AzMySqlConfiguration。</span><span class="sxs-lookup"><span data-stu-id="c2aae-112">Use Update-AzMySqlConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="c2aae-113">示例</span><span class="sxs-lookup"><span data-stu-id="c2aae-113">EXAMPLES</span></span>

### <span data-ttu-id="c2aae-114">範例1：依資源群組和伺服器名稱更新 MySql 伺服器</span><span class="sxs-lookup"><span data-stu-id="c2aae-114">Example 1: Update MySql server by resource group and server name</span></span>
```powershell
PS C:\> Update-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -SslEnforcement Disabled

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test    eastus   mysql_test         5.7     5120                    GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="c2aae-115">這個 Cmdlet 會依資源群組和伺服器名稱更新 MySql 伺服器。</span><span class="sxs-lookup"><span data-stu-id="c2aae-115">This cmdlet updates MySql server by resource group and server name.</span></span>

### <span data-ttu-id="c2aae-116">範例2：依身分識別更新 MySql 伺服器。</span><span class="sxs-lookup"><span data-stu-id="c2aae-116">Example 2: Update MySql server by identity.</span></span>
```powershell
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test | Update-AzMySqlServer -BackupRetentionDay 23 -StorageMb 10240

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test    eastus   mysql_test         5.7     10240                   GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="c2aae-117">這個 Cmdlet 會依身分識別更新 MySql 伺服器。</span><span class="sxs-lookup"><span data-stu-id="c2aae-117">This cmdlet updates MySql server by identity.</span></span>

## <span data-ttu-id="c2aae-118">參數</span><span class="sxs-lookup"><span data-stu-id="c2aae-118">PARAMETERS</span></span>

### <span data-ttu-id="c2aae-119">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="c2aae-119">-AdministratorLoginPassword</span></span>
<span data-ttu-id="c2aae-120">系統管理員登入的密碼。</span><span class="sxs-lookup"><span data-stu-id="c2aae-120">The password of the administrator login.</span></span>

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

### <span data-ttu-id="c2aae-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c2aae-121">-AsJob</span></span>
<span data-ttu-id="c2aae-122">執行命令做為作業。</span><span class="sxs-lookup"><span data-stu-id="c2aae-122">Run the command as a job.</span></span>

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

### <span data-ttu-id="c2aae-123">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="c2aae-123">-BackupRetentionDay</span></span>
<span data-ttu-id="c2aae-124">伺服器的備份保留天數。</span><span class="sxs-lookup"><span data-stu-id="c2aae-124">Backup retention days for the server.</span></span>
<span data-ttu-id="c2aae-125">日算在7到35。</span><span class="sxs-lookup"><span data-stu-id="c2aae-125">Day count is between 7 and 35.</span></span>

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

### <span data-ttu-id="c2aae-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2aae-126">-DefaultProfile</span></span>
<span data-ttu-id="c2aae-127">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c2aae-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2aae-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c2aae-128">-InputObject</span></span>
<span data-ttu-id="c2aae-129">身分識別參數。</span><span class="sxs-lookup"><span data-stu-id="c2aae-129">Identity Parameter.</span></span>
<span data-ttu-id="c2aae-130">若要構造，請參閱適用于 INPUTOBJECT 屬性的 [記事] 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="c2aae-130">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="c2aae-131">-名稱</span><span class="sxs-lookup"><span data-stu-id="c2aae-131">-Name</span></span>
<span data-ttu-id="c2aae-132">伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="c2aae-132">The name of the server.</span></span>

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

### <span data-ttu-id="c2aae-133">-NoWait</span><span class="sxs-lookup"><span data-stu-id="c2aae-133">-NoWait</span></span>
<span data-ttu-id="c2aae-134">以非同步方式執行命令。</span><span class="sxs-lookup"><span data-stu-id="c2aae-134">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="c2aae-135">-ReplicationRole</span><span class="sxs-lookup"><span data-stu-id="c2aae-135">-ReplicationRole</span></span>
<span data-ttu-id="c2aae-136">伺服器的複製角色。</span><span class="sxs-lookup"><span data-stu-id="c2aae-136">The replication role of the server.</span></span>

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

### <span data-ttu-id="c2aae-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2aae-137">-ResourceGroupName</span></span>
<span data-ttu-id="c2aae-138">包含資源之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c2aae-138">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="c2aae-139">您可以從 Azure 資源管理器 API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="c2aae-139">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="c2aae-140">-Sku</span><span class="sxs-lookup"><span data-stu-id="c2aae-140">-Sku</span></span>
<span data-ttu-id="c2aae-141">Sku 的名稱，通常是 [層 + 家庭 + 核心]，例如 B_Gen4_1、GP_Gen5_8。</span><span class="sxs-lookup"><span data-stu-id="c2aae-141">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="c2aae-142">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="c2aae-142">-SkuCapacity</span></span>
<span data-ttu-id="c2aae-143">[擴大/縮小] 容量，代表伺服器的計算單位。</span><span class="sxs-lookup"><span data-stu-id="c2aae-143">The scale up/out capacity, representing server's compute units.</span></span>

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

### <span data-ttu-id="c2aae-144">-SkuFamily</span><span class="sxs-lookup"><span data-stu-id="c2aae-144">-SkuFamily</span></span>
<span data-ttu-id="c2aae-145">硬體系列。</span><span class="sxs-lookup"><span data-stu-id="c2aae-145">The family of hardware.</span></span>

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

### <span data-ttu-id="c2aae-146">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="c2aae-146">-SkuTier</span></span>
<span data-ttu-id="c2aae-147">特定 SKU 的層級，例如基本。</span><span class="sxs-lookup"><span data-stu-id="c2aae-147">The tier of the particular SKU, e.g. Basic.</span></span>

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

### <span data-ttu-id="c2aae-148">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="c2aae-148">-SslEnforcement</span></span>
<span data-ttu-id="c2aae-149">在連線至伺服器時啟用 ssl 強制執行。</span><span class="sxs-lookup"><span data-stu-id="c2aae-149">Enable ssl enforcement or not when connect to server.</span></span>

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

### <span data-ttu-id="c2aae-150">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="c2aae-150">-StorageAutogrow</span></span>
<span data-ttu-id="c2aae-151">啟用儲存空間自動增長。</span><span class="sxs-lookup"><span data-stu-id="c2aae-151">Enable Storage Auto Grow.</span></span>

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

### <span data-ttu-id="c2aae-152">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="c2aae-152">-StorageInMb</span></span>
<span data-ttu-id="c2aae-153">伺服器允許的最大儲存空間。</span><span class="sxs-lookup"><span data-stu-id="c2aae-153">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="c2aae-154">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c2aae-154">-SubscriptionId</span></span>
<span data-ttu-id="c2aae-155">識別 Azure 訂閱的訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="c2aae-155">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="c2aae-156">-Tag</span><span class="sxs-lookup"><span data-stu-id="c2aae-156">-Tag</span></span>
<span data-ttu-id="c2aae-157">以鍵值對形式的特定應用程式中繼資料。</span><span class="sxs-lookup"><span data-stu-id="c2aae-157">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="c2aae-158">-確認</span><span class="sxs-lookup"><span data-stu-id="c2aae-158">-Confirm</span></span>
<span data-ttu-id="c2aae-159">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c2aae-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2aae-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2aae-160">-WhatIf</span></span>
<span data-ttu-id="c2aae-161">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c2aae-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2aae-162">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c2aae-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2aae-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2aae-163">CommonParameters</span></span>
<span data-ttu-id="c2aae-164">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c2aae-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2aae-165">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c2aae-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2aae-166">輸入</span><span class="sxs-lookup"><span data-stu-id="c2aae-166">INPUTS</span></span>

### <span data-ttu-id="c2aae-167">IMySqlIdentity 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="c2aae-167">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="c2aae-168">輸出</span><span class="sxs-lookup"><span data-stu-id="c2aae-168">OUTPUTS</span></span>

### <span data-ttu-id="c2aae-169">IServer 中的 Api20171201 （）。</span><span class="sxs-lookup"><span data-stu-id="c2aae-169">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="c2aae-170">筆記</span><span class="sxs-lookup"><span data-stu-id="c2aae-170">NOTES</span></span>

<span data-ttu-id="c2aae-171">別名</span><span class="sxs-lookup"><span data-stu-id="c2aae-171">ALIASES</span></span>

<span data-ttu-id="c2aae-172">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="c2aae-172">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c2aae-173">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="c2aae-173">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c2aae-174">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="c2aae-174">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c2aae-175">INPUTOBJECT <IMySqlIdentity> ：身分識別參數。</span><span class="sxs-lookup"><span data-stu-id="c2aae-175">INPUTOBJECT <IMySqlIdentity>: Identity Parameter.</span></span>
  - <span data-ttu-id="c2aae-176">`[ConfigurationName <String>]`：伺服器配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="c2aae-176">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="c2aae-177">`[DatabaseName <String>]`：資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="c2aae-177">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="c2aae-178">`[FirewallRuleName <String>]`：伺服器防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="c2aae-178">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="c2aae-179">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="c2aae-179">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c2aae-180">`[KeyName <String>]`：伺服器金鑰的名稱。</span><span class="sxs-lookup"><span data-stu-id="c2aae-180">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="c2aae-181">`[LocationName <String>]`：位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="c2aae-181">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="c2aae-182">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c2aae-182">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="c2aae-183">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="c2aae-183">The name is case insensitive.</span></span>
  - <span data-ttu-id="c2aae-184">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`：安全警示原則的名稱。</span><span class="sxs-lookup"><span data-stu-id="c2aae-184">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="c2aae-185">`[ServerName <String>]`：伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="c2aae-185">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="c2aae-186">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="c2aae-186">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="c2aae-187">`[VirtualNetworkRuleName <String>]`：虛擬網路規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="c2aae-187">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="c2aae-188">相關連結</span><span class="sxs-lookup"><span data-stu-id="c2aae-188">RELATED LINKS</span></span>

