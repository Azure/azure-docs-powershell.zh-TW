---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/restore-azpostgresqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Restore-AzPostgreSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Restore-AzPostgreSqlServer.md
ms.openlocfilehash: c9e4134b6787f78442a18836c15ce190c3e685d8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94126285"
---
# <span data-ttu-id="cbd04-101">Restore-AzPostgreSqlServer</span><span class="sxs-lookup"><span data-stu-id="cbd04-101">Restore-AzPostgreSqlServer</span></span>

## <span data-ttu-id="cbd04-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cbd04-102">SYNOPSIS</span></span>
<span data-ttu-id="cbd04-103">從現有的備份還原伺服器</span><span class="sxs-lookup"><span data-stu-id="cbd04-103">Restore a server from an existing backup</span></span>

## <span data-ttu-id="cbd04-104">句法</span><span class="sxs-lookup"><span data-stu-id="cbd04-104">SYNTAX</span></span>

### <span data-ttu-id="cbd04-105">GeoRestore (預設) </span><span class="sxs-lookup"><span data-stu-id="cbd04-105">GeoRestore (Default)</span></span>
```
Restore-AzPostgreSqlServer -Name <String> -ResourceGroupName <String> -InputObject <IServer> -UseGeoRestore
 [-SubscriptionId <String>] [-Location <String>] [-Sku <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="cbd04-106">PointInTimeRestore</span><span class="sxs-lookup"><span data-stu-id="cbd04-106">PointInTimeRestore</span></span>
```
Restore-AzPostgreSqlServer -Name <String> -ResourceGroupName <String> -InputObject <IServer>
 -RestorePointInTime <DateTime> -UsePointInTimeRestore [-SubscriptionId <String>] [-Location <String>]
 [-Sku <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="cbd04-107">說明</span><span class="sxs-lookup"><span data-stu-id="cbd04-107">DESCRIPTION</span></span>
<span data-ttu-id="cbd04-108">從現有的備份還原伺服器</span><span class="sxs-lookup"><span data-stu-id="cbd04-108">Restore a server from an existing backup</span></span>

## <span data-ttu-id="cbd04-109">示例</span><span class="sxs-lookup"><span data-stu-id="cbd04-109">EXAMPLES</span></span>

### <span data-ttu-id="cbd04-110">範例1：使用 GeoReplica Restore 還原 PostgreSql 伺服器</span><span class="sxs-lookup"><span data-stu-id="cbd04-110">Example 1: Restore PostgreSql server using GeoReplica Restore</span></span>
```powershell
PS C:\> Get-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -ServerName postgresqltestserverreplica | Restore-AzPostgreSqlServer -Name PostgreSqlTestServer -ResourceGroupName PostgreSqlTestRG -UseGeoRestore

Name                 Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                 -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="cbd04-111">這個 Cmdlet 會使用 GeoReplica 還原來還原 PostgreSql 伺服器。</span><span class="sxs-lookup"><span data-stu-id="cbd04-111">This cmdlet restores PostgreSql server using GeoReplica Restore.</span></span>

### <span data-ttu-id="cbd04-112">範例2：使用 PointInTime Restore 還原 PostgreSql 伺服器</span><span class="sxs-lookup"><span data-stu-id="cbd04-112">Example 2: Restore PostgreSql server using PointInTime Restore</span></span>
```powershell
PS C:\> $restorePointInTime = (Get-Date).AddMinutes(-10)
PS C:\> Get-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer | Restore-AzPostgreSqlServer -Name PostgreSqlTestServerGEO -ResourceGroupName PostgreSqlTestRG -RestorePointInTime $restorePointInTime -UsePointInTimeRestore

Name                    Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                    -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestservergeo eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="cbd04-113">這些 Cmdlet 會使用 PointInTime 還原來還原 PostgreSql 伺服器。</span><span class="sxs-lookup"><span data-stu-id="cbd04-113">These cmdlets restore PostgreSql server using PointInTime Restore.</span></span>

## <span data-ttu-id="cbd04-114">參數</span><span class="sxs-lookup"><span data-stu-id="cbd04-114">PARAMETERS</span></span>

### <span data-ttu-id="cbd04-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cbd04-115">-AsJob</span></span>
<span data-ttu-id="cbd04-116">執行命令做為作業。</span><span class="sxs-lookup"><span data-stu-id="cbd04-116">Run the command as a job.</span></span>

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

### <span data-ttu-id="cbd04-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbd04-117">-DefaultProfile</span></span>
<span data-ttu-id="cbd04-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="cbd04-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cbd04-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cbd04-119">-InputObject</span></span>
<span data-ttu-id="cbd04-120">要從中還原的源伺服器物件。</span><span class="sxs-lookup"><span data-stu-id="cbd04-120">The source server object to restore from.</span></span>
<span data-ttu-id="cbd04-121">若要構造，請參閱適用于 INPUTOBJECT 屬性的 [記事] 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="cbd04-121">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cbd04-122">-位置</span><span class="sxs-lookup"><span data-stu-id="cbd04-122">-Location</span></span>
<span data-ttu-id="cbd04-123">資源所在的位置。</span><span class="sxs-lookup"><span data-stu-id="cbd04-123">The location the resource resides in.</span></span>

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

### <span data-ttu-id="cbd04-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="cbd04-124">-Name</span></span>
<span data-ttu-id="cbd04-125">伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="cbd04-125">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbd04-126">-NoWait</span><span class="sxs-lookup"><span data-stu-id="cbd04-126">-NoWait</span></span>
<span data-ttu-id="cbd04-127">以非同步方式執行命令。</span><span class="sxs-lookup"><span data-stu-id="cbd04-127">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="cbd04-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cbd04-128">-ResourceGroupName</span></span>
<span data-ttu-id="cbd04-129">包含資源之資源群組的名稱，您可以從 Azure 資源管理員 API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="cbd04-129">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="cbd04-130">-RestorePointInTime</span><span class="sxs-lookup"><span data-stu-id="cbd04-130">-RestorePointInTime</span></span>
<span data-ttu-id="cbd04-131">資源所在的位置。</span><span class="sxs-lookup"><span data-stu-id="cbd04-131">The location the resource resides in.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: PointInTimeRestore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbd04-132">-Sku</span><span class="sxs-lookup"><span data-stu-id="cbd04-132">-Sku</span></span>
<span data-ttu-id="cbd04-133">Sku 的名稱，通常是 [層 + 家庭 + 核心]，例如 B_Gen4_1、GP_Gen5_8。</span><span class="sxs-lookup"><span data-stu-id="cbd04-133">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="cbd04-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cbd04-134">-SubscriptionId</span></span>
<span data-ttu-id="cbd04-135">識別 Azure 訂閱的訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="cbd04-135">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="cbd04-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="cbd04-136">-Tag</span></span>
<span data-ttu-id="cbd04-137">以鍵值對形式的特定應用程式中繼資料。</span><span class="sxs-lookup"><span data-stu-id="cbd04-137">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="cbd04-138">-UseGeoRestore</span><span class="sxs-lookup"><span data-stu-id="cbd04-138">-UseGeoRestore</span></span>
<span data-ttu-id="cbd04-139">使用 Geo 模式進行還原</span><span class="sxs-lookup"><span data-stu-id="cbd04-139">Use Geo mode to restore</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GeoRestore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbd04-140">-UsePointInTimeRestore</span><span class="sxs-lookup"><span data-stu-id="cbd04-140">-UsePointInTimeRestore</span></span>
<span data-ttu-id="cbd04-141">使用 PointInTime 模式來還原</span><span class="sxs-lookup"><span data-stu-id="cbd04-141">Use PointInTime mode to restore</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PointInTimeRestore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbd04-142">-確認</span><span class="sxs-lookup"><span data-stu-id="cbd04-142">-Confirm</span></span>
<span data-ttu-id="cbd04-143">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="cbd04-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cbd04-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cbd04-144">-WhatIf</span></span>
<span data-ttu-id="cbd04-145">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cbd04-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cbd04-146">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cbd04-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cbd04-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbd04-147">CommonParameters</span></span>
<span data-ttu-id="cbd04-148">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cbd04-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbd04-149">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="cbd04-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbd04-150">輸入</span><span class="sxs-lookup"><span data-stu-id="cbd04-150">INPUTS</span></span>

### <span data-ttu-id="cbd04-151">IServer （PostgreSql）。 Api20171201。</span><span class="sxs-lookup"><span data-stu-id="cbd04-151">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="cbd04-152">輸出</span><span class="sxs-lookup"><span data-stu-id="cbd04-152">OUTPUTS</span></span>

### <span data-ttu-id="cbd04-153">IServer （PostgreSql）。 Api20171201。</span><span class="sxs-lookup"><span data-stu-id="cbd04-153">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="cbd04-154">筆記</span><span class="sxs-lookup"><span data-stu-id="cbd04-154">NOTES</span></span>

<span data-ttu-id="cbd04-155">別名</span><span class="sxs-lookup"><span data-stu-id="cbd04-155">ALIASES</span></span>

<span data-ttu-id="cbd04-156">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="cbd04-156">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="cbd04-157">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="cbd04-157">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cbd04-158">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="cbd04-158">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="cbd04-159">INPUTOBJECT <IServer> ：要從中還原的源伺服器物件。</span><span class="sxs-lookup"><span data-stu-id="cbd04-159">INPUTOBJECT <IServer>: The source server object to restore from.</span></span>
  - <span data-ttu-id="cbd04-160">`Location <String>`：資源所在的位置。</span><span class="sxs-lookup"><span data-stu-id="cbd04-160">`Location <String>`: The location the resource resides in.</span></span>
  - <span data-ttu-id="cbd04-161">`[Tag <ITrackedResourceTags>]`：以鍵值對形式的特定應用程式中繼資料。</span><span class="sxs-lookup"><span data-stu-id="cbd04-161">`[Tag <ITrackedResourceTags>]`: Application-specific metadata in the form of key-value pairs.</span></span>
    - <span data-ttu-id="cbd04-162">`[(Any) <String>]`：這表示您可以將任何屬性新增至此物件。</span><span class="sxs-lookup"><span data-stu-id="cbd04-162">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="cbd04-163">`[AdministratorLogin <String>]`：管理員的伺服器登入名稱。</span><span class="sxs-lookup"><span data-stu-id="cbd04-163">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="cbd04-164">只能在 (建立伺服器時指定，且在建立) 時需要。</span><span class="sxs-lookup"><span data-stu-id="cbd04-164">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="cbd04-165">`[EarliestRestoreDate <DateTime?>]`： (ISO8601 格式的最早還原點建立時間) </span><span class="sxs-lookup"><span data-stu-id="cbd04-165">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="cbd04-166">`[FullyQualifiedDomainName <String>]`：伺服器的完整功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="cbd04-166">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="cbd04-167">`[IdentityType <IdentityType?>]`：身分識別類型。</span><span class="sxs-lookup"><span data-stu-id="cbd04-167">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="cbd04-168">將此值設定為 ' SystemAssigned」，即可自動為資源建立並指派 Azure Active Directory 主體。</span><span class="sxs-lookup"><span data-stu-id="cbd04-168">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="cbd04-169">`[InfrastructureEncryption <InfrastructureEncryption?>]`：顯示伺服器是否已啟用基礎結構加密的狀態。</span><span class="sxs-lookup"><span data-stu-id="cbd04-169">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Status showing whether the server enabled infrastructure encryption.</span></span>
  - <span data-ttu-id="cbd04-170">`[MasterServerId <String>]`：複本伺服器的主伺服器 id。</span><span class="sxs-lookup"><span data-stu-id="cbd04-170">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="cbd04-171">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`：為伺服器強制執行最低的 Tls 版本。</span><span class="sxs-lookup"><span data-stu-id="cbd04-171">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Enforce a minimal Tls version for the server.</span></span>
  - <span data-ttu-id="cbd04-172">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`：此伺服器是否允許公用網路存取。</span><span class="sxs-lookup"><span data-stu-id="cbd04-172">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Whether or not public network access is allowed for this server.</span></span> <span data-ttu-id="cbd04-173">Value 是 optional，但如果傳入，就必須是「Enabled」或「Disabled」</span><span class="sxs-lookup"><span data-stu-id="cbd04-173">Value is optional but if passed in, must be 'Enabled' or 'Disabled'</span></span>
  - <span data-ttu-id="cbd04-174">`[ReplicaCapacity <Int32?>]`：主伺服器可擁有的複本數目上限。</span><span class="sxs-lookup"><span data-stu-id="cbd04-174">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="cbd04-175">`[ReplicationRole <String>]`：伺服器的複製角色。</span><span class="sxs-lookup"><span data-stu-id="cbd04-175">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="cbd04-176">`[SkuCapacity <Int32?>]`： [擴大/縮小] 容量，代表伺服器的計算單位。</span><span class="sxs-lookup"><span data-stu-id="cbd04-176">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="cbd04-177">`[SkuFamily <String>]`：硬體系列。</span><span class="sxs-lookup"><span data-stu-id="cbd04-177">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="cbd04-178">`[SkuName <String>]`： Sku 的名稱，通常是 [層 + 家庭 + 核心]，例如 B_Gen4_1、GP_Gen5_8。</span><span class="sxs-lookup"><span data-stu-id="cbd04-178">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="cbd04-179">`[SkuSize <String>]`：根據需要由資源來轉譯的大小代碼。</span><span class="sxs-lookup"><span data-stu-id="cbd04-179">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="cbd04-180">`[SkuTier <SkuTier?>]`：特定 SKU 的層級，例如基本。</span><span class="sxs-lookup"><span data-stu-id="cbd04-180">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="cbd04-181">`[SslEnforcement <SslEnforcementEnum?>]`[：在連線至伺服器時，啟用 ssl 強制執行。</span><span class="sxs-lookup"><span data-stu-id="cbd04-181">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="cbd04-182">`[StorageProfileBackupRetentionDay <Int32?>]`：伺服器的備份保留天數。</span><span class="sxs-lookup"><span data-stu-id="cbd04-182">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="cbd04-183">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`：啟用地域冗余，或不用於伺服器備份。</span><span class="sxs-lookup"><span data-stu-id="cbd04-183">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="cbd04-184">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`：啟用儲存空間自動增長。</span><span class="sxs-lookup"><span data-stu-id="cbd04-184">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="cbd04-185">`[StorageProfileStorageMb <Int32?>]`：伺服器允許的最大儲存空間。</span><span class="sxs-lookup"><span data-stu-id="cbd04-185">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="cbd04-186">`[UserVisibleState <ServerState?>]`：使用者可看見的伺服器狀態。</span><span class="sxs-lookup"><span data-stu-id="cbd04-186">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="cbd04-187">`[Version <ServerVersion?>]`：伺服器版本。</span><span class="sxs-lookup"><span data-stu-id="cbd04-187">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="cbd04-188">相關連結</span><span class="sxs-lookup"><span data-stu-id="cbd04-188">RELATED LINKS</span></span>

