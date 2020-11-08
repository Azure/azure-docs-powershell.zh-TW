---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/new-azpostgresqlreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlReplica.md
ms.openlocfilehash: e3c0d7e8d3b3d9fe42bc97c40ad54424b7bfd0da
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94139013"
---
# <span data-ttu-id="450e7-101">New-AzPostgreSqlReplica</span><span class="sxs-lookup"><span data-stu-id="450e7-101">New-AzPostgreSqlReplica</span></span>

## <span data-ttu-id="450e7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="450e7-102">SYNOPSIS</span></span>
<span data-ttu-id="450e7-103">從現有資料庫建立新的複本。</span><span class="sxs-lookup"><span data-stu-id="450e7-103">Creates a new replica from an existing database.</span></span>

## <span data-ttu-id="450e7-104">句法</span><span class="sxs-lookup"><span data-stu-id="450e7-104">SYNTAX</span></span>

```
New-AzPostgreSqlReplica -ReplicaName <String> -ResourceGroupName <String> -Master <IServer>
 [-SubscriptionId <String>] [-Location <String>] [-Sku <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="450e7-105">說明</span><span class="sxs-lookup"><span data-stu-id="450e7-105">DESCRIPTION</span></span>
<span data-ttu-id="450e7-106">從現有資料庫建立新的複本。</span><span class="sxs-lookup"><span data-stu-id="450e7-106">Creates a new replica from an existing database.</span></span>

## <span data-ttu-id="450e7-107">示例</span><span class="sxs-lookup"><span data-stu-id="450e7-107">EXAMPLES</span></span>

### <span data-ttu-id="450e7-108">範例1：建立新的 PostgreSql 伺服器複本</span><span class="sxs-lookup"><span data-stu-id="450e7-108">Example 1: Create a new PostgreSql server replica</span></span>
```powershell
PS C:\> Get-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer | New-AzPostgreSqlReplica -ReplicaName PostgreSqlTestServerReplica -ResourceGroupName PostgreSqlTestRG

Name                        Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                        -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserverreplica eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="450e7-109">這個 Cmdlet 會建立新的 PostgreSql 伺服器複製。</span><span class="sxs-lookup"><span data-stu-id="450e7-109">This cmdlet creates a new PostgreSql server replica.</span></span>

### <span data-ttu-id="450e7-110">範例2：建立新的 PostgreSql 伺服器複本</span><span class="sxs-lookup"><span data-stu-id="450e7-110">Example 2: Create a new PostgreSql server replica</span></span>
```powershell
PS C:\> $pgDb = Get-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer 
PS C:\> New-AzPostgreSqlReplica -Master $pgDb -ReplicaName PostgreSqlTestServerReplica -ResourceGroupName PostgreSqlTestRG

Name                        Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                        -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserverreplica eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="450e7-111">這個 Cmdlet 會建立新的 PostgreSql 伺服器複製。</span><span class="sxs-lookup"><span data-stu-id="450e7-111">This cmdlet creates a new PostgreSql server replica.</span></span>

## <span data-ttu-id="450e7-112">參數</span><span class="sxs-lookup"><span data-stu-id="450e7-112">PARAMETERS</span></span>

### <span data-ttu-id="450e7-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="450e7-113">-AsJob</span></span>
<span data-ttu-id="450e7-114">執行命令做為作業。</span><span class="sxs-lookup"><span data-stu-id="450e7-114">Run the command as a job.</span></span>

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

### <span data-ttu-id="450e7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="450e7-115">-DefaultProfile</span></span>
<span data-ttu-id="450e7-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="450e7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="450e7-117">-位置</span><span class="sxs-lookup"><span data-stu-id="450e7-117">-Location</span></span>
<span data-ttu-id="450e7-118">資源所在的位置。</span><span class="sxs-lookup"><span data-stu-id="450e7-118">The location the resource resides in.</span></span>

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

### <span data-ttu-id="450e7-119">-主要</span><span class="sxs-lookup"><span data-stu-id="450e7-119">-Master</span></span>
<span data-ttu-id="450e7-120">要從中建立複本的來源伺服器物件。</span><span class="sxs-lookup"><span data-stu-id="450e7-120">The source server object to create replica from.</span></span>
<span data-ttu-id="450e7-121">若要建立，請參閱 MASTER 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="450e7-121">To construct, see NOTES section for MASTER properties and create a hash table.</span></span>

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

### <span data-ttu-id="450e7-122">-NoWait</span><span class="sxs-lookup"><span data-stu-id="450e7-122">-NoWait</span></span>
<span data-ttu-id="450e7-123">以非同步方式執行命令。</span><span class="sxs-lookup"><span data-stu-id="450e7-123">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="450e7-124">-ReplicaName</span><span class="sxs-lookup"><span data-stu-id="450e7-124">-ReplicaName</span></span>
<span data-ttu-id="450e7-125">伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="450e7-125">The name of the server.</span></span>

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

### <span data-ttu-id="450e7-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="450e7-126">-ResourceGroupName</span></span>
<span data-ttu-id="450e7-127">包含資源之資源群組的名稱，您可以從 Azure 資源管理員 API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="450e7-127">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="450e7-128">-Sku</span><span class="sxs-lookup"><span data-stu-id="450e7-128">-Sku</span></span>
<span data-ttu-id="450e7-129">Sku 的名稱，通常是 [層 + 家庭 + 核心]，例如 B_Gen4_1、GP_Gen5_8。</span><span class="sxs-lookup"><span data-stu-id="450e7-129">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="450e7-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="450e7-130">-SubscriptionId</span></span>
<span data-ttu-id="450e7-131">識別 Azure 訂閱的訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="450e7-131">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="450e7-132">-確認</span><span class="sxs-lookup"><span data-stu-id="450e7-132">-Confirm</span></span>
<span data-ttu-id="450e7-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="450e7-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="450e7-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="450e7-134">-WhatIf</span></span>
<span data-ttu-id="450e7-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="450e7-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="450e7-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="450e7-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="450e7-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="450e7-137">CommonParameters</span></span>
<span data-ttu-id="450e7-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="450e7-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="450e7-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="450e7-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="450e7-140">輸入</span><span class="sxs-lookup"><span data-stu-id="450e7-140">INPUTS</span></span>

### <span data-ttu-id="450e7-141">IServer （PostgreSql）。 Api20171201。</span><span class="sxs-lookup"><span data-stu-id="450e7-141">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="450e7-142">輸出</span><span class="sxs-lookup"><span data-stu-id="450e7-142">OUTPUTS</span></span>

### <span data-ttu-id="450e7-143">IServer （PostgreSql）。 Api20171201。</span><span class="sxs-lookup"><span data-stu-id="450e7-143">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="450e7-144">筆記</span><span class="sxs-lookup"><span data-stu-id="450e7-144">NOTES</span></span>

<span data-ttu-id="450e7-145">別名</span><span class="sxs-lookup"><span data-stu-id="450e7-145">ALIASES</span></span>

<span data-ttu-id="450e7-146">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="450e7-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="450e7-147">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="450e7-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="450e7-148">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="450e7-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="450e7-149">MASTER <IServer> （主要）：要從中建立複本的來源伺服器物件。</span><span class="sxs-lookup"><span data-stu-id="450e7-149">MASTER <IServer>: The source server object to create replica from.</span></span>
  - <span data-ttu-id="450e7-150">`Location <String>`：資源所在的位置。</span><span class="sxs-lookup"><span data-stu-id="450e7-150">`Location <String>`: The location the resource resides in.</span></span>
  - <span data-ttu-id="450e7-151">`[Tag <ITrackedResourceTags>]`：以鍵值對形式的特定應用程式中繼資料。</span><span class="sxs-lookup"><span data-stu-id="450e7-151">`[Tag <ITrackedResourceTags>]`: Application-specific metadata in the form of key-value pairs.</span></span>
    - <span data-ttu-id="450e7-152">`[(Any) <String>]`：這表示您可以將任何屬性新增至此物件。</span><span class="sxs-lookup"><span data-stu-id="450e7-152">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="450e7-153">`[AdministratorLogin <String>]`：管理員的伺服器登入名稱。</span><span class="sxs-lookup"><span data-stu-id="450e7-153">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="450e7-154">只能在 (建立伺服器時指定，且在建立) 時需要。</span><span class="sxs-lookup"><span data-stu-id="450e7-154">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="450e7-155">`[EarliestRestoreDate <DateTime?>]`： (ISO8601 格式的最早還原點建立時間) </span><span class="sxs-lookup"><span data-stu-id="450e7-155">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="450e7-156">`[FullyQualifiedDomainName <String>]`：伺服器的完整功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="450e7-156">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="450e7-157">`[IdentityType <IdentityType?>]`：身分識別類型。</span><span class="sxs-lookup"><span data-stu-id="450e7-157">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="450e7-158">將此值設定為 ' SystemAssigned」，即可自動為資源建立並指派 Azure Active Directory 主體。</span><span class="sxs-lookup"><span data-stu-id="450e7-158">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="450e7-159">`[InfrastructureEncryption <InfrastructureEncryption?>]`：顯示伺服器是否已啟用基礎結構加密的狀態。</span><span class="sxs-lookup"><span data-stu-id="450e7-159">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Status showing whether the server enabled infrastructure encryption.</span></span>
  - <span data-ttu-id="450e7-160">`[MasterServerId <String>]`：複本伺服器的主伺服器 id。</span><span class="sxs-lookup"><span data-stu-id="450e7-160">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="450e7-161">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`：為伺服器強制執行最低的 Tls 版本。</span><span class="sxs-lookup"><span data-stu-id="450e7-161">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Enforce a minimal Tls version for the server.</span></span>
  - <span data-ttu-id="450e7-162">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`：此伺服器是否允許公用網路存取。</span><span class="sxs-lookup"><span data-stu-id="450e7-162">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Whether or not public network access is allowed for this server.</span></span> <span data-ttu-id="450e7-163">Value 是 optional，但如果傳入，就必須是「Enabled」或「Disabled」</span><span class="sxs-lookup"><span data-stu-id="450e7-163">Value is optional but if passed in, must be 'Enabled' or 'Disabled'</span></span>
  - <span data-ttu-id="450e7-164">`[ReplicaCapacity <Int32?>]`：主伺服器可擁有的複本數目上限。</span><span class="sxs-lookup"><span data-stu-id="450e7-164">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="450e7-165">`[ReplicationRole <String>]`：伺服器的複製角色。</span><span class="sxs-lookup"><span data-stu-id="450e7-165">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="450e7-166">`[SkuCapacity <Int32?>]`： [擴大/縮小] 容量，代表伺服器的計算單位。</span><span class="sxs-lookup"><span data-stu-id="450e7-166">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="450e7-167">`[SkuFamily <String>]`：硬體系列。</span><span class="sxs-lookup"><span data-stu-id="450e7-167">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="450e7-168">`[SkuName <String>]`： Sku 的名稱，通常是 [層 + 家庭 + 核心]，例如 B_Gen4_1、GP_Gen5_8。</span><span class="sxs-lookup"><span data-stu-id="450e7-168">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="450e7-169">`[SkuSize <String>]`：根據需要由資源來轉譯的大小代碼。</span><span class="sxs-lookup"><span data-stu-id="450e7-169">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="450e7-170">`[SkuTier <SkuTier?>]`：特定 SKU 的層級，例如基本。</span><span class="sxs-lookup"><span data-stu-id="450e7-170">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="450e7-171">`[SslEnforcement <SslEnforcementEnum?>]`[：在連線至伺服器時，啟用 ssl 強制執行。</span><span class="sxs-lookup"><span data-stu-id="450e7-171">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="450e7-172">`[StorageProfileBackupRetentionDay <Int32?>]`：伺服器的備份保留天數。</span><span class="sxs-lookup"><span data-stu-id="450e7-172">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="450e7-173">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`：啟用地域冗余，或不用於伺服器備份。</span><span class="sxs-lookup"><span data-stu-id="450e7-173">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="450e7-174">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`：啟用儲存空間自動增長。</span><span class="sxs-lookup"><span data-stu-id="450e7-174">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="450e7-175">`[StorageProfileStorageMb <Int32?>]`：伺服器允許的最大儲存空間。</span><span class="sxs-lookup"><span data-stu-id="450e7-175">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="450e7-176">`[UserVisibleState <ServerState?>]`：使用者可看見的伺服器狀態。</span><span class="sxs-lookup"><span data-stu-id="450e7-176">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="450e7-177">`[Version <ServerVersion?>]`：伺服器版本。</span><span class="sxs-lookup"><span data-stu-id="450e7-177">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="450e7-178">相關連結</span><span class="sxs-lookup"><span data-stu-id="450e7-178">RELATED LINKS</span></span>

