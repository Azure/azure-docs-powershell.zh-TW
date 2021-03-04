---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/restore-azmysqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Restore-AzMySqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Restore-AzMySqlServer.md
ms.openlocfilehash: 95807621ffb054610a5778872db243eea50a7efa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906150"
---
# <span data-ttu-id="e6fa5-101">Restore-AzMySqlServer</span><span class="sxs-lookup"><span data-stu-id="e6fa5-101">Restore-AzMySqlServer</span></span>

## <span data-ttu-id="e6fa5-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e6fa5-102">SYNOPSIS</span></span>
<span data-ttu-id="e6fa5-103">從現有的備份還原伺服器</span><span class="sxs-lookup"><span data-stu-id="e6fa5-103">Restore a server from an existing backup</span></span>

## <span data-ttu-id="e6fa5-104">語法</span><span class="sxs-lookup"><span data-stu-id="e6fa5-104">SYNTAX</span></span>

### <span data-ttu-id="e6fa5-105">GeoRestore (預設) </span><span class="sxs-lookup"><span data-stu-id="e6fa5-105">GeoRestore (Default)</span></span>
```
Restore-AzMySqlServer -Name <String> -ResourceGroupName <String> -InputObject <IServer> -UseGeoRestore
 [-SubscriptionId <String>] [-Location <String>] [-Sku <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e6fa5-106">PointInTimeRestore</span><span class="sxs-lookup"><span data-stu-id="e6fa5-106">PointInTimeRestore</span></span>
```
Restore-AzMySqlServer -Name <String> -ResourceGroupName <String> -InputObject <IServer>
 -RestorePointInTime <DateTime> -UsePointInTimeRestore [-SubscriptionId <String>] [-Location <String>]
 [-Sku <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="e6fa5-107">描述</span><span class="sxs-lookup"><span data-stu-id="e6fa5-107">DESCRIPTION</span></span>
<span data-ttu-id="e6fa5-108">從現有的備份還原伺服器</span><span class="sxs-lookup"><span data-stu-id="e6fa5-108">Restore a server from an existing backup</span></span>

## <span data-ttu-id="e6fa5-109">例子</span><span class="sxs-lookup"><span data-stu-id="e6fa5-109">EXAMPLES</span></span>

### <span data-ttu-id="e6fa5-110">範例 1：使用 GeoReplica Restore 還原 MySql 伺服器</span><span class="sxs-lookup"><span data-stu-id="e6fa5-110">Example 1: Restore MySql server using GeoReplica Restore</span></span>
```powershell
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test-replica | Restore-AzMySqlServer -Name mysql-test -ResourceGroupName PowershellMySqlTest -UseGeoRestore 

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test-11 eastus   mysql_test         5.7     10240                   GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="e6fa5-111">此 Cmdlet 會使用 GeoReplica Restore 還原 MySql 伺服器。</span><span class="sxs-lookup"><span data-stu-id="e6fa5-111">This cmdlet restores MySql server using GeoReplica Restore.</span></span>

### <span data-ttu-id="e6fa5-112">範例 2：使用 PointInTime Restore 還原 MySql 伺服器</span><span class="sxs-lookup"><span data-stu-id="e6fa5-112">Example 2: Restore MySql server using PointInTime Restore</span></span>
```powershell
PS C:\> $restorePointInTime = (Get-Date).AddMinutes(-10)
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test | Restore-AzMySqlServer -Name mysql-test-restore -ResourceGroupName PowershellMySqlTest -RestorePointInTime $restorePointInTime -UsePointInTimeRestore

Name               Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----               -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test-restore eastus   mysql_test         5.7     10240                   GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="e6fa5-113">這些 Cmdlet 會使用 PointInTime 還原還原 MySql 伺服器。</span><span class="sxs-lookup"><span data-stu-id="e6fa5-113">These cmdlets restore MySql server using PointInTime Restore.</span></span>

## <span data-ttu-id="e6fa5-114">參數</span><span class="sxs-lookup"><span data-stu-id="e6fa5-114">PARAMETERS</span></span>

### <span data-ttu-id="e6fa5-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e6fa5-115">-AsJob</span></span>
<span data-ttu-id="e6fa5-116">以工作執行命令。</span><span class="sxs-lookup"><span data-stu-id="e6fa5-116">Run the command as a job.</span></span>

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

### <span data-ttu-id="e6fa5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6fa5-117">-DefaultProfile</span></span>
<span data-ttu-id="e6fa5-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="e6fa5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6fa5-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e6fa5-119">-InputObject</span></span>
<span data-ttu-id="e6fa5-120">要還原的來源伺服器物件。</span><span class="sxs-lookup"><span data-stu-id="e6fa5-120">The source server object to restore from.</span></span>
<span data-ttu-id="e6fa5-121">若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="e6fa5-121">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e6fa5-122">-位置</span><span class="sxs-lookup"><span data-stu-id="e6fa5-122">-Location</span></span>
<span data-ttu-id="e6fa5-123">資源所在位置。</span><span class="sxs-lookup"><span data-stu-id="e6fa5-123">The location the resource resides in.</span></span>

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

### <span data-ttu-id="e6fa5-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="e6fa5-124">-Name</span></span>
<span data-ttu-id="e6fa5-125">伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="e6fa5-125">The name of the server.</span></span>

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

### <span data-ttu-id="e6fa5-126">-NoWait</span><span class="sxs-lookup"><span data-stu-id="e6fa5-126">-NoWait</span></span>
<span data-ttu-id="e6fa5-127">非同步執行命令。</span><span class="sxs-lookup"><span data-stu-id="e6fa5-127">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="e6fa5-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6fa5-128">-ResourceGroupName</span></span>
<span data-ttu-id="e6fa5-129">包含資源的資源組名，您可從 Azure Resource Manager API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="e6fa5-129">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="e6fa5-130">-RestorePointInTime</span><span class="sxs-lookup"><span data-stu-id="e6fa5-130">-RestorePointInTime</span></span>
<span data-ttu-id="e6fa5-131">資源所在位置。</span><span class="sxs-lookup"><span data-stu-id="e6fa5-131">The location the resource resides in.</span></span>

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

### <span data-ttu-id="e6fa5-132">-SKU</span><span class="sxs-lookup"><span data-stu-id="e6fa5-132">-Sku</span></span>
<span data-ttu-id="e6fa5-133">SKU 的名稱，通常是 tier + family + 核心，例如 B_Gen4_1、GP_Gen5_8。</span><span class="sxs-lookup"><span data-stu-id="e6fa5-133">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="e6fa5-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e6fa5-134">-SubscriptionId</span></span>
<span data-ttu-id="e6fa5-135">可識別 Azure 訂閱的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="e6fa5-135">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="e6fa5-136">-標記</span><span class="sxs-lookup"><span data-stu-id="e6fa5-136">-Tag</span></span>
<span data-ttu-id="e6fa5-137">以金鑰值組形式顯示的應用程式特定中繼資料。</span><span class="sxs-lookup"><span data-stu-id="e6fa5-137">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="e6fa5-138">-UseGeoRestore</span><span class="sxs-lookup"><span data-stu-id="e6fa5-138">-UseGeoRestore</span></span>
<span data-ttu-id="e6fa5-139">使用地理位置模式還原</span><span class="sxs-lookup"><span data-stu-id="e6fa5-139">Use Geo mode to restore</span></span>

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

### <span data-ttu-id="e6fa5-140">-UsePointInTimeRestore</span><span class="sxs-lookup"><span data-stu-id="e6fa5-140">-UsePointInTimeRestore</span></span>
<span data-ttu-id="e6fa5-141">使用 PointInTime 模式進行還原</span><span class="sxs-lookup"><span data-stu-id="e6fa5-141">Use PointInTime mode to restore</span></span>

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

### <span data-ttu-id="e6fa5-142">-確認</span><span class="sxs-lookup"><span data-stu-id="e6fa5-142">-Confirm</span></span>
<span data-ttu-id="e6fa5-143">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="e6fa5-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6fa5-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6fa5-144">-WhatIf</span></span>
<span data-ttu-id="e6fa5-145">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e6fa5-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e6fa5-146">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e6fa5-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6fa5-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6fa5-147">CommonParameters</span></span>
<span data-ttu-id="e6fa5-148">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e6fa5-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6fa5-149">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e6fa5-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6fa5-150">輸入</span><span class="sxs-lookup"><span data-stu-id="e6fa5-150">INPUTS</span></span>

### <span data-ttu-id="e6fa5-151">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="e6fa5-151">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="e6fa5-152">輸出</span><span class="sxs-lookup"><span data-stu-id="e6fa5-152">OUTPUTS</span></span>

### <span data-ttu-id="e6fa5-153">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="e6fa5-153">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="e6fa5-154">筆記</span><span class="sxs-lookup"><span data-stu-id="e6fa5-154">NOTES</span></span>

<span data-ttu-id="e6fa5-155">別名</span><span class="sxs-lookup"><span data-stu-id="e6fa5-155">ALIASES</span></span>

<span data-ttu-id="e6fa5-156">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="e6fa5-156">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e6fa5-157">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="e6fa5-157">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e6fa5-158">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="e6fa5-158">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e6fa5-159">INPUTOBJECT： <IServer> 要還原的來源伺服器物件。</span><span class="sxs-lookup"><span data-stu-id="e6fa5-159">INPUTOBJECT <IServer>: The source server object to restore from.</span></span>
  - <span data-ttu-id="e6fa5-160">`Location <String>`：資源所在地的地理位置</span><span class="sxs-lookup"><span data-stu-id="e6fa5-160">`Location <String>`: The geo-location where the resource lives</span></span>
  - <span data-ttu-id="e6fa5-161">`[Tag <ITrackedResourceTags>]`：資源標記。</span><span class="sxs-lookup"><span data-stu-id="e6fa5-161">`[Tag <ITrackedResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="e6fa5-162">`[(Any) <String>]`：這表示任何屬性都可以新增到這個物件。</span><span class="sxs-lookup"><span data-stu-id="e6fa5-162">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="e6fa5-163">`[AdministratorLogin <String>]`：系統管理員的伺服器登入名稱。</span><span class="sxs-lookup"><span data-stu-id="e6fa5-163">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="e6fa5-164">只能在建立伺服器時指定， (建立時) 。</span><span class="sxs-lookup"><span data-stu-id="e6fa5-164">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="e6fa5-165">`[EarliestRestoreDate <DateTime?>]`：ISO8601 格式的最早還原點建立時間 (ISO8601 格式) </span><span class="sxs-lookup"><span data-stu-id="e6fa5-165">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="e6fa5-166">`[FullyQualifiedDomainName <String>]`：伺服器完整功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="e6fa5-166">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="e6fa5-167">`[IdentityType <IdentityType?>]`：身分識別類型。</span><span class="sxs-lookup"><span data-stu-id="e6fa5-167">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="e6fa5-168">將此選項設定為 'SystemAssigned'，以自動建立及指派資源的 Azure Active Directory 主體。</span><span class="sxs-lookup"><span data-stu-id="e6fa5-168">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="e6fa5-169">`[InfrastructureEncryption <InfrastructureEncryption?>]`：狀態顯示伺服器是否啟用基礎結構加密。</span><span class="sxs-lookup"><span data-stu-id="e6fa5-169">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Status showing whether the server enabled infrastructure encryption.</span></span>
  - <span data-ttu-id="e6fa5-170">`[MasterServerId <String>]`：複本伺服器的主伺服器識別碼。</span><span class="sxs-lookup"><span data-stu-id="e6fa5-170">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="e6fa5-171">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`：針對伺服器強制執行最小 Tls 版本。</span><span class="sxs-lookup"><span data-stu-id="e6fa5-171">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Enforce a minimal Tls version for the server.</span></span>
  - <span data-ttu-id="e6fa5-172">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`：此伺服器是否允許公用網路存取。</span><span class="sxs-lookup"><span data-stu-id="e6fa5-172">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Whether or not public network access is allowed for this server.</span></span> <span data-ttu-id="e6fa5-173">Value 為選擇性，但如果傳遞，則必須是 'Enabled' 或 'Disabled'</span><span class="sxs-lookup"><span data-stu-id="e6fa5-173">Value is optional but if passed in, must be 'Enabled' or 'Disabled'</span></span>
  - <span data-ttu-id="e6fa5-174">`[ReplicaCapacity <Int32?>]`：主伺服器可擁有的最大複本數目。</span><span class="sxs-lookup"><span data-stu-id="e6fa5-174">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="e6fa5-175">`[ReplicationRole <String>]`：伺服器的複製角色。</span><span class="sxs-lookup"><span data-stu-id="e6fa5-175">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="e6fa5-176">`[SkuCapacity <Int32?>]`：向上/縮小容量，代表伺服器的計算單位。</span><span class="sxs-lookup"><span data-stu-id="e6fa5-176">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="e6fa5-177">`[SkuFamily <String>]`：硬體系列。</span><span class="sxs-lookup"><span data-stu-id="e6fa5-177">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="e6fa5-178">`[SkuName <String>]`：SKU 的名稱，通常是 tier + family + cores，例如B_Gen4_1、GP_Gen5_8。</span><span class="sxs-lookup"><span data-stu-id="e6fa5-178">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="e6fa5-179">`[SkuSize <String>]`：大小代碼，以適當的資源解譯。</span><span class="sxs-lookup"><span data-stu-id="e6fa5-179">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="e6fa5-180">`[SkuTier <SkuTier?>]`：特定 SKU 的層級，例如基本。</span><span class="sxs-lookup"><span data-stu-id="e6fa5-180">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="e6fa5-181">`[SslEnforcement <SslEnforcementEnum?>]`：在連接至伺服器時啟用 ssl 強制執行或不啟用。</span><span class="sxs-lookup"><span data-stu-id="e6fa5-181">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="e6fa5-182">`[StorageProfileBackupRetentionDay <Int32?>]`：伺服器的備份保留天數。</span><span class="sxs-lookup"><span data-stu-id="e6fa5-182">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="e6fa5-183">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`：針對伺服器備份啟用異地重複或不啟用。</span><span class="sxs-lookup"><span data-stu-id="e6fa5-183">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="e6fa5-184">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`：啟用儲存空間自動放大。</span><span class="sxs-lookup"><span data-stu-id="e6fa5-184">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="e6fa5-185">`[StorageProfileStorageMb <Int32?>]`：伺服器允許的最大儲存空間。</span><span class="sxs-lookup"><span data-stu-id="e6fa5-185">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="e6fa5-186">`[UserVisibleState <ServerState?>]`：使用者可看見的伺服器狀態。</span><span class="sxs-lookup"><span data-stu-id="e6fa5-186">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="e6fa5-187">`[Version <ServerVersion?>]`：伺服器版本。</span><span class="sxs-lookup"><span data-stu-id="e6fa5-187">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="e6fa5-188">相關連結</span><span class="sxs-lookup"><span data-stu-id="e6fa5-188">RELATED LINKS</span></span>

