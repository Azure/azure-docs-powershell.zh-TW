---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/new-azmariadbreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbReplica.md
ms.openlocfilehash: 0ce25af607d2460abf2ec4585dacc124a1f2e65c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98438060"
---
# <span data-ttu-id="fe4bb-101">New-AzMariaDbReplica</span><span class="sxs-lookup"><span data-stu-id="fe4bb-101">New-AzMariaDbReplica</span></span>

## <span data-ttu-id="fe4bb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fe4bb-102">SYNOPSIS</span></span>
<span data-ttu-id="fe4bb-103">建立 MariaDB 伺服器的複本。</span><span class="sxs-lookup"><span data-stu-id="fe4bb-103">Creates a replica of a MariaDB server.</span></span>

## <span data-ttu-id="fe4bb-104">句法</span><span class="sxs-lookup"><span data-stu-id="fe4bb-104">SYNTAX</span></span>

### <span data-ttu-id="fe4bb-105">ServerName (預設) </span><span class="sxs-lookup"><span data-stu-id="fe4bb-105">ServerName (Default)</span></span>
```
New-AzMariaDbReplica -MasterName <String> -ReplicaName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Location <String>] [-Sku <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="fe4bb-106">ServerObject</span><span class="sxs-lookup"><span data-stu-id="fe4bb-106">ServerObject</span></span>
```
New-AzMariaDbReplica -Master <IServer> -ReplicaName <String> [-SubscriptionId <String>] [-Location <String>]
 [-Sku <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="fe4bb-107">說明</span><span class="sxs-lookup"><span data-stu-id="fe4bb-107">DESCRIPTION</span></span>
<span data-ttu-id="fe4bb-108">建立 MariaDB 伺服器的複本。</span><span class="sxs-lookup"><span data-stu-id="fe4bb-108">Creates a replica of a MariaDB server.</span></span>

## <span data-ttu-id="fe4bb-109">示例</span><span class="sxs-lookup"><span data-stu-id="fe4bb-109">EXAMPLES</span></span>

### <span data-ttu-id="fe4bb-110">範例1：建立 MariaDB 的複本資料庫</span><span class="sxs-lookup"><span data-stu-id="fe4bb-110">Example 1: Create a replica db for a MariaDB</span></span>
```powershell
PS C:\> New-AzMariaDbReplica -MasterName mariadb-test-9pebvn -ReplicaName mariadb-test-9pebvn-rep01 -ResourceGroupName mariadb-test-qu5ov0

Name                      Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                      -------- ------------------ ------- ----------------------- -------   -------        --------------
mariadb-test-9pebvn-rep01 eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="fe4bb-111">這個命令會建立 MariaDB 的複本資料庫。</span><span class="sxs-lookup"><span data-stu-id="fe4bb-111">This command creates a replica db for a MariaDB.</span></span>

### <span data-ttu-id="fe4bb-112">範例2：建立 MariaDB 的複本資料庫</span><span class="sxs-lookup"><span data-stu-id="fe4bb-112">Example 2: Create a replica db for a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbServer -Name mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0 | New-AzMariaDbReplica -ReplicaName mariadb-test-9pebvn-rep02

Name                      Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                      -------- ------------------ ------- ----------------------- -------   -------        --------------
mariadb-test-9pebvn-rep02 eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="fe4bb-113">這個命令會建立 MariaDB 的複本資料庫。</span><span class="sxs-lookup"><span data-stu-id="fe4bb-113">This command creates a replica db for a MariaDB.</span></span>

### <span data-ttu-id="fe4bb-114">範例3：建立 MariaDB 的複本資料庫</span><span class="sxs-lookup"><span data-stu-id="fe4bb-114">Example 3: Create a replica db for a MariaDB</span></span>
```powershell
PS C:\> $mariaDb = Get-AzMariaDbServer -Name mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0 
PS C:\> New-AzMariaDbReplica -Master $mariaDb -ReplicaName mariadb-test-9pebvn-rep03

Name                      Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                      -------- ------------------ ------- ----------------------- -------   -------        --------------
mariadb-test-9pebvn-rep03 eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="fe4bb-115">這個含有參數 inputobject 的命令會為 MariaDB 建立含參數 inputobject 的複本資料庫。</span><span class="sxs-lookup"><span data-stu-id="fe4bb-115">This command with parameter inputobject creates a replica db with parameter inputobject for a MariaDB.</span></span>

## <span data-ttu-id="fe4bb-116">參數</span><span class="sxs-lookup"><span data-stu-id="fe4bb-116">PARAMETERS</span></span>

### <span data-ttu-id="fe4bb-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fe4bb-117">-AsJob</span></span>
<span data-ttu-id="fe4bb-118">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="fe4bb-118">Run the command as a job</span></span>

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

### <span data-ttu-id="fe4bb-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe4bb-119">-DefaultProfile</span></span>
<span data-ttu-id="fe4bb-120">地區 DefaultParameters 用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="fe4bb-120">region DefaultParameters The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe4bb-121">-位置</span><span class="sxs-lookup"><span data-stu-id="fe4bb-121">-Location</span></span>
<span data-ttu-id="fe4bb-122">資源所在的位置。</span><span class="sxs-lookup"><span data-stu-id="fe4bb-122">The location the resource resides in.</span></span>

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

### <span data-ttu-id="fe4bb-123">-主要</span><span class="sxs-lookup"><span data-stu-id="fe4bb-123">-Master</span></span>
<span data-ttu-id="fe4bb-124">要從中還原的源伺服器物件。</span><span class="sxs-lookup"><span data-stu-id="fe4bb-124">The source server object to restore from.</span></span>
<span data-ttu-id="fe4bb-125">若要建立，請參閱 MASTER 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="fe4bb-125">To construct, see NOTES section for MASTER properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer
Parameter Sets: ServerObject
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fe4bb-126">-MasterName</span><span class="sxs-lookup"><span data-stu-id="fe4bb-126">-MasterName</span></span>
<span data-ttu-id="fe4bb-127">MariaDB [伺服器名稱]。</span><span class="sxs-lookup"><span data-stu-id="fe4bb-127">MariaDB server name.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerName
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe4bb-128">-NoWait</span><span class="sxs-lookup"><span data-stu-id="fe4bb-128">-NoWait</span></span>
<span data-ttu-id="fe4bb-129">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="fe4bb-129">Run the command asynchronously</span></span>

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

### <span data-ttu-id="fe4bb-130">-ReplicaName</span><span class="sxs-lookup"><span data-stu-id="fe4bb-130">-ReplicaName</span></span>
<span data-ttu-id="fe4bb-131">複本名稱。</span><span class="sxs-lookup"><span data-stu-id="fe4bb-131">Replica name.</span></span>

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

### <span data-ttu-id="fe4bb-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe4bb-132">-ResourceGroupName</span></span>
<span data-ttu-id="fe4bb-133">您可以從 Azure 資源管理器 API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="fe4bb-133">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe4bb-134">-Sku</span><span class="sxs-lookup"><span data-stu-id="fe4bb-134">-Sku</span></span>
<span data-ttu-id="fe4bb-135">Sku 的名稱，通常是 [層 + 家庭 + 核心]，例如 B_Gen4_1、GP_Gen5_8。</span><span class="sxs-lookup"><span data-stu-id="fe4bb-135">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="fe4bb-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fe4bb-136">-SubscriptionId</span></span>
<span data-ttu-id="fe4bb-137">訂閱識別碼是每個服務呼叫 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="fe4bb-137">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="fe4bb-138">-Tag</span><span class="sxs-lookup"><span data-stu-id="fe4bb-138">-Tag</span></span>
<span data-ttu-id="fe4bb-139">以鍵值對形式的特定應用程式中繼資料。</span><span class="sxs-lookup"><span data-stu-id="fe4bb-139">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="fe4bb-140">-確認</span><span class="sxs-lookup"><span data-stu-id="fe4bb-140">-Confirm</span></span>
<span data-ttu-id="fe4bb-141">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="fe4bb-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe4bb-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe4bb-142">-WhatIf</span></span>
<span data-ttu-id="fe4bb-143">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="fe4bb-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe4bb-144">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fe4bb-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe4bb-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe4bb-145">CommonParameters</span></span>
<span data-ttu-id="fe4bb-146">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fe4bb-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe4bb-147">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="fe4bb-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe4bb-148">輸入</span><span class="sxs-lookup"><span data-stu-id="fe4bb-148">INPUTS</span></span>

### <span data-ttu-id="fe4bb-149">IServer （MariaDb）。 Api20180601Preview。</span><span class="sxs-lookup"><span data-stu-id="fe4bb-149">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="fe4bb-150">輸出</span><span class="sxs-lookup"><span data-stu-id="fe4bb-150">OUTPUTS</span></span>

### <span data-ttu-id="fe4bb-151">IServer （MariaDb）。 Api20180601Preview。</span><span class="sxs-lookup"><span data-stu-id="fe4bb-151">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="fe4bb-152">筆記</span><span class="sxs-lookup"><span data-stu-id="fe4bb-152">NOTES</span></span>

<span data-ttu-id="fe4bb-153">別名</span><span class="sxs-lookup"><span data-stu-id="fe4bb-153">ALIASES</span></span>

<span data-ttu-id="fe4bb-154">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="fe4bb-154">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="fe4bb-155">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="fe4bb-155">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="fe4bb-156">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="fe4bb-156">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="fe4bb-157">MASTER <IServer> （主要）：要還原的來源伺服器物件。</span><span class="sxs-lookup"><span data-stu-id="fe4bb-157">MASTER <IServer>: The source server object to restore from.</span></span>
  - <span data-ttu-id="fe4bb-158">`Location <String>`：資源所在的位置。</span><span class="sxs-lookup"><span data-stu-id="fe4bb-158">`Location <String>`: The location the resource resides in.</span></span>
  - <span data-ttu-id="fe4bb-159">`[Tag <ITrackedResourceTags>]`：以鍵值對形式的特定應用程式中繼資料。</span><span class="sxs-lookup"><span data-stu-id="fe4bb-159">`[Tag <ITrackedResourceTags>]`: Application-specific metadata in the form of key-value pairs.</span></span>
    - <span data-ttu-id="fe4bb-160">`[(Any) <String>]`：這表示您可以將任何屬性新增至此物件。</span><span class="sxs-lookup"><span data-stu-id="fe4bb-160">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="fe4bb-161">`[AdministratorLogin <String>]`：管理員的伺服器登入名稱。</span><span class="sxs-lookup"><span data-stu-id="fe4bb-161">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="fe4bb-162">只能在 (建立伺服器時指定，且在建立) 時需要。</span><span class="sxs-lookup"><span data-stu-id="fe4bb-162">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="fe4bb-163">`[EarliestRestoreDate <DateTime?>]`： (ISO8601 格式的最早還原點建立時間) </span><span class="sxs-lookup"><span data-stu-id="fe4bb-163">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="fe4bb-164">`[FullyQualifiedDomainName <String>]`：伺服器的完整功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="fe4bb-164">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="fe4bb-165">`[IdentityType <IdentityType?>]`：身分識別類型。</span><span class="sxs-lookup"><span data-stu-id="fe4bb-165">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="fe4bb-166">將此值設定為 ' SystemAssigned」，即可自動為資源建立並指派 Azure Active Directory 主體。</span><span class="sxs-lookup"><span data-stu-id="fe4bb-166">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="fe4bb-167">`[MasterServerId <String>]`：複本伺服器的主伺服器 id。</span><span class="sxs-lookup"><span data-stu-id="fe4bb-167">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="fe4bb-168">`[ReplicaCapacity <Int32?>]`：主伺服器可擁有的複本數目上限。</span><span class="sxs-lookup"><span data-stu-id="fe4bb-168">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="fe4bb-169">`[ReplicationRole <String>]`：伺服器的複製角色。</span><span class="sxs-lookup"><span data-stu-id="fe4bb-169">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="fe4bb-170">`[SkuCapacity <Int32?>]`： [擴大/縮小] 容量，代表伺服器的計算單位。</span><span class="sxs-lookup"><span data-stu-id="fe4bb-170">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="fe4bb-171">`[SkuFamily <String>]`：硬體系列。</span><span class="sxs-lookup"><span data-stu-id="fe4bb-171">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="fe4bb-172">`[SkuName <String>]`： Sku 的名稱，通常是 [層 + 家庭 + 核心]，例如 B_Gen4_1、GP_Gen5_8。</span><span class="sxs-lookup"><span data-stu-id="fe4bb-172">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="fe4bb-173">`[SkuSize <String>]`：根據需要由資源來轉譯的大小代碼。</span><span class="sxs-lookup"><span data-stu-id="fe4bb-173">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="fe4bb-174">`[SkuTier <SkuTier?>]`：特定 SKU 的層級，例如基本。</span><span class="sxs-lookup"><span data-stu-id="fe4bb-174">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="fe4bb-175">`[SslEnforcement <SslEnforcementEnum?>]`[：在連線至伺服器時，啟用 ssl 強制執行。</span><span class="sxs-lookup"><span data-stu-id="fe4bb-175">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="fe4bb-176">`[StorageProfileBackupRetentionDay <Int32?>]`：伺服器的備份保留天數。</span><span class="sxs-lookup"><span data-stu-id="fe4bb-176">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="fe4bb-177">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`：啟用地域冗余，或不用於伺服器備份。</span><span class="sxs-lookup"><span data-stu-id="fe4bb-177">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="fe4bb-178">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`：啟用儲存空間自動增長。</span><span class="sxs-lookup"><span data-stu-id="fe4bb-178">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="fe4bb-179">`[StorageProfileStorageMb <Int32?>]`：伺服器允許的最大儲存空間。</span><span class="sxs-lookup"><span data-stu-id="fe4bb-179">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="fe4bb-180">`[UserVisibleState <ServerState?>]`：使用者可看見的伺服器狀態。</span><span class="sxs-lookup"><span data-stu-id="fe4bb-180">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="fe4bb-181">`[Version <ServerVersion?>]`：伺服器版本。</span><span class="sxs-lookup"><span data-stu-id="fe4bb-181">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="fe4bb-182">相關連結</span><span class="sxs-lookup"><span data-stu-id="fe4bb-182">RELATED LINKS</span></span>

