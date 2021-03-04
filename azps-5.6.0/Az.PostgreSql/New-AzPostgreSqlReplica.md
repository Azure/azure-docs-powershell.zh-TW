---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/powershell/module/az.postgresql/new-azpostgresqlreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlReplica.md
ms.openlocfilehash: 5aed092485bf90418f467a2857716496f2979454
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910962"
---
# <span data-ttu-id="7ace7-101">New-AzPostgreSqlReplica</span><span class="sxs-lookup"><span data-stu-id="7ace7-101">New-AzPostgreSqlReplica</span></span>

## <span data-ttu-id="7ace7-102">簡介</span><span class="sxs-lookup"><span data-stu-id="7ace7-102">SYNOPSIS</span></span>
<span data-ttu-id="7ace7-103">從現有資料庫建立新複本。</span><span class="sxs-lookup"><span data-stu-id="7ace7-103">Creates a new replica from an existing database.</span></span>

## <span data-ttu-id="7ace7-104">語法</span><span class="sxs-lookup"><span data-stu-id="7ace7-104">SYNTAX</span></span>

```
New-AzPostgreSqlReplica -ReplicaName <String> -ResourceGroupName <String> -Master <IServer>
 [-SubscriptionId <String>] [-Location <String>] [-Sku <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7ace7-105">描述</span><span class="sxs-lookup"><span data-stu-id="7ace7-105">DESCRIPTION</span></span>
<span data-ttu-id="7ace7-106">從現有資料庫建立新複本。</span><span class="sxs-lookup"><span data-stu-id="7ace7-106">Creates a new replica from an existing database.</span></span>

## <span data-ttu-id="7ace7-107">例子</span><span class="sxs-lookup"><span data-stu-id="7ace7-107">EXAMPLES</span></span>

### <span data-ttu-id="7ace7-108">範例 1：建立新的 PostgreSql 伺服器複本</span><span class="sxs-lookup"><span data-stu-id="7ace7-108">Example 1: Create a new PostgreSql server replica</span></span>
```powershell
PS C:\> Get-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer | New-AzPostgreSqlReplica -ReplicaName PostgreSqlTestServerReplica -ResourceGroupName PostgreSqlTestRG

Name                        Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                        -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserverreplica eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="7ace7-109">此 Cmdlet 會建立一個新的 PostgreSql 伺服器複本。</span><span class="sxs-lookup"><span data-stu-id="7ace7-109">This cmdlet creates a new PostgreSql server replica.</span></span>

### <span data-ttu-id="7ace7-110">範例 2：建立新的 PostgreSql 伺服器複本</span><span class="sxs-lookup"><span data-stu-id="7ace7-110">Example 2: Create a new PostgreSql server replica</span></span>
```powershell
PS C:\> $pgDb = Get-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer 
PS C:\> New-AzPostgreSqlReplica -Master $pgDb -ReplicaName PostgreSqlTestServerReplica -ResourceGroupName PostgreSqlTestRG

Name                        Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                        -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserverreplica eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="7ace7-111">此 Cmdlet 會建立一個新的 PostgreSql 伺服器複本。</span><span class="sxs-lookup"><span data-stu-id="7ace7-111">This cmdlet creates a new PostgreSql server replica.</span></span>

## <span data-ttu-id="7ace7-112">參數</span><span class="sxs-lookup"><span data-stu-id="7ace7-112">PARAMETERS</span></span>

### <span data-ttu-id="7ace7-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7ace7-113">-AsJob</span></span>
<span data-ttu-id="7ace7-114">以工作執行命令。</span><span class="sxs-lookup"><span data-stu-id="7ace7-114">Run the command as a job.</span></span>

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

### <span data-ttu-id="7ace7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ace7-115">-DefaultProfile</span></span>
<span data-ttu-id="7ace7-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="7ace7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7ace7-117">-位置</span><span class="sxs-lookup"><span data-stu-id="7ace7-117">-Location</span></span>
<span data-ttu-id="7ace7-118">資源所在位置。</span><span class="sxs-lookup"><span data-stu-id="7ace7-118">The location the resource resides in.</span></span>

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

### <span data-ttu-id="7ace7-119">-主控點</span><span class="sxs-lookup"><span data-stu-id="7ace7-119">-Master</span></span>
<span data-ttu-id="7ace7-120">要建立複本的來源伺服器物件。</span><span class="sxs-lookup"><span data-stu-id="7ace7-120">The source server object to create replica from.</span></span>
<span data-ttu-id="7ace7-121">若要建構，請參閱 MASTER 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="7ace7-121">To construct, see NOTES section for MASTER properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7ace7-122">-NoWait</span><span class="sxs-lookup"><span data-stu-id="7ace7-122">-NoWait</span></span>
<span data-ttu-id="7ace7-123">非同步執行命令。</span><span class="sxs-lookup"><span data-stu-id="7ace7-123">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="7ace7-124">-副本名稱</span><span class="sxs-lookup"><span data-stu-id="7ace7-124">-ReplicaName</span></span>
<span data-ttu-id="7ace7-125">伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="7ace7-125">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ReplicaServerName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ace7-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ace7-126">-ResourceGroupName</span></span>
<span data-ttu-id="7ace7-127">包含資源的資源組名，您可從 Azure Resource Manager API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="7ace7-127">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="7ace7-128">-SKU</span><span class="sxs-lookup"><span data-stu-id="7ace7-128">-Sku</span></span>
<span data-ttu-id="7ace7-129">SKU 的名稱，通常是 tier + family + 核心，例如 B_Gen4_1、GP_Gen5_8。</span><span class="sxs-lookup"><span data-stu-id="7ace7-129">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="7ace7-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7ace7-130">-SubscriptionId</span></span>
<span data-ttu-id="7ace7-131">可識別 Azure 訂閱的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="7ace7-131">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="7ace7-132">-確認</span><span class="sxs-lookup"><span data-stu-id="7ace7-132">-Confirm</span></span>
<span data-ttu-id="7ace7-133">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="7ace7-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ace7-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ace7-134">-WhatIf</span></span>
<span data-ttu-id="7ace7-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7ace7-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ace7-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7ace7-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ace7-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ace7-137">CommonParameters</span></span>
<span data-ttu-id="7ace7-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="7ace7-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ace7-139">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7ace7-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ace7-140">輸入</span><span class="sxs-lookup"><span data-stu-id="7ace7-140">INPUTS</span></span>

### <span data-ttu-id="7ace7-141">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="7ace7-141">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="7ace7-142">輸出</span><span class="sxs-lookup"><span data-stu-id="7ace7-142">OUTPUTS</span></span>

### <span data-ttu-id="7ace7-143">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="7ace7-143">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="7ace7-144">筆記</span><span class="sxs-lookup"><span data-stu-id="7ace7-144">NOTES</span></span>

<span data-ttu-id="7ace7-145">別名</span><span class="sxs-lookup"><span data-stu-id="7ace7-145">ALIASES</span></span>

<span data-ttu-id="7ace7-146">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="7ace7-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7ace7-147">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="7ace7-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7ace7-148">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="7ace7-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7ace7-149"><IServer>MASTER：建立複本的來源伺服器物件。</span><span class="sxs-lookup"><span data-stu-id="7ace7-149">MASTER <IServer>: The source server object to create replica from.</span></span>
  - <span data-ttu-id="7ace7-150">`Location <String>`：資源所在地的地理位置</span><span class="sxs-lookup"><span data-stu-id="7ace7-150">`Location <String>`: The geo-location where the resource lives</span></span>
  - <span data-ttu-id="7ace7-151">`[Tag <ITrackedResourceTags>]`：資源標記。</span><span class="sxs-lookup"><span data-stu-id="7ace7-151">`[Tag <ITrackedResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="7ace7-152">`[(Any) <String>]`：這表示任何屬性都可以新增到這個物件。</span><span class="sxs-lookup"><span data-stu-id="7ace7-152">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="7ace7-153">`[AdministratorLogin <String>]`：系統管理員的伺服器登入名稱。</span><span class="sxs-lookup"><span data-stu-id="7ace7-153">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="7ace7-154">只能在建立伺服器時指定， (建立時) 。</span><span class="sxs-lookup"><span data-stu-id="7ace7-154">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="7ace7-155">`[EarliestRestoreDate <DateTime?>]`：ISO8601 格式的最早還原點建立時間 (ISO8601 格式) </span><span class="sxs-lookup"><span data-stu-id="7ace7-155">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="7ace7-156">`[FullyQualifiedDomainName <String>]`：伺服器完整功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="7ace7-156">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="7ace7-157">`[IdentityType <IdentityType?>]`：身分識別類型。</span><span class="sxs-lookup"><span data-stu-id="7ace7-157">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="7ace7-158">將此選項設定為 'SystemAssigned'，以自動建立及指派資源的 Azure Active Directory 主體。</span><span class="sxs-lookup"><span data-stu-id="7ace7-158">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="7ace7-159">`[InfrastructureEncryption <InfrastructureEncryption?>]`：狀態顯示伺服器是否啟用基礎結構加密。</span><span class="sxs-lookup"><span data-stu-id="7ace7-159">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Status showing whether the server enabled infrastructure encryption.</span></span>
  - <span data-ttu-id="7ace7-160">`[MasterServerId <String>]`：複本伺服器的主伺服器識別碼。</span><span class="sxs-lookup"><span data-stu-id="7ace7-160">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="7ace7-161">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`：針對伺服器強制執行最小 Tls 版本。</span><span class="sxs-lookup"><span data-stu-id="7ace7-161">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Enforce a minimal Tls version for the server.</span></span>
  - <span data-ttu-id="7ace7-162">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`：此伺服器是否允許公用網路存取。</span><span class="sxs-lookup"><span data-stu-id="7ace7-162">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Whether or not public network access is allowed for this server.</span></span> <span data-ttu-id="7ace7-163">Value 為選擇性，但如果傳遞，則必須是 'Enabled' 或 'Disabled'</span><span class="sxs-lookup"><span data-stu-id="7ace7-163">Value is optional but if passed in, must be 'Enabled' or 'Disabled'</span></span>
  - <span data-ttu-id="7ace7-164">`[ReplicaCapacity <Int32?>]`：主伺服器可擁有的最大複本數量。</span><span class="sxs-lookup"><span data-stu-id="7ace7-164">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="7ace7-165">`[ReplicationRole <String>]`：伺服器的複製角色。</span><span class="sxs-lookup"><span data-stu-id="7ace7-165">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="7ace7-166">`[SkuCapacity <Int32?>]`：向上/縮小容量，代表伺服器的計算單位。</span><span class="sxs-lookup"><span data-stu-id="7ace7-166">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="7ace7-167">`[SkuFamily <String>]`：硬體系列。</span><span class="sxs-lookup"><span data-stu-id="7ace7-167">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="7ace7-168">`[SkuName <String>]`：SKU 的名稱，通常是 tier + family + cores，例如 B_Gen4_1、GP_Gen5_8。</span><span class="sxs-lookup"><span data-stu-id="7ace7-168">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="7ace7-169">`[SkuSize <String>]`：大小代碼，以適當的資源解譯。</span><span class="sxs-lookup"><span data-stu-id="7ace7-169">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="7ace7-170">`[SkuTier <SkuTier?>]`：特定 SKU 的層級，例如基本。</span><span class="sxs-lookup"><span data-stu-id="7ace7-170">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="7ace7-171">`[SslEnforcement <SslEnforcementEnum?>]`：在連接至伺服器時啟用 ssl 強制執行或不啟用。</span><span class="sxs-lookup"><span data-stu-id="7ace7-171">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="7ace7-172">`[StorageProfileBackupRetentionDay <Int32?>]`：伺服器的備份保留天數。</span><span class="sxs-lookup"><span data-stu-id="7ace7-172">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="7ace7-173">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`：針對伺服器備份啟用異地重複或不啟用。</span><span class="sxs-lookup"><span data-stu-id="7ace7-173">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="7ace7-174">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`：啟用儲存空間自動放大。</span><span class="sxs-lookup"><span data-stu-id="7ace7-174">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="7ace7-175">`[StorageProfileStorageMb <Int32?>]`：伺服器允許的最大儲存空間。</span><span class="sxs-lookup"><span data-stu-id="7ace7-175">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="7ace7-176">`[UserVisibleState <ServerState?>]`：使用者可看見的伺服器狀態。</span><span class="sxs-lookup"><span data-stu-id="7ace7-176">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="7ace7-177">`[Version <ServerVersion?>]`：伺服器版本。</span><span class="sxs-lookup"><span data-stu-id="7ace7-177">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="7ace7-178">相關連結</span><span class="sxs-lookup"><span data-stu-id="7ace7-178">RELATED LINKS</span></span>

