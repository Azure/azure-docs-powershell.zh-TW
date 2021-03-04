---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/powershell/module/az.mariadb/new-azmariadbreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbReplica.md
ms.openlocfilehash: 3e3e63bee89eb9ae89cb647b81ea7d0da792ae3e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906570"
---
# <span data-ttu-id="0553e-101">New-AzMariaDbReplica</span><span class="sxs-lookup"><span data-stu-id="0553e-101">New-AzMariaDbReplica</span></span>

## <span data-ttu-id="0553e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="0553e-102">SYNOPSIS</span></span>
<span data-ttu-id="0553e-103">建立 MariaDB 伺服器的複本。</span><span class="sxs-lookup"><span data-stu-id="0553e-103">Creates a replica of a MariaDB server.</span></span>

## <span data-ttu-id="0553e-104">語法</span><span class="sxs-lookup"><span data-stu-id="0553e-104">SYNTAX</span></span>

### <span data-ttu-id="0553e-105">ServerName (預設) </span><span class="sxs-lookup"><span data-stu-id="0553e-105">ServerName (Default)</span></span>
```
New-AzMariaDbReplica -MasterName <String> -ReplicaName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Location <String>] [-Sku <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="0553e-106">ServerObject</span><span class="sxs-lookup"><span data-stu-id="0553e-106">ServerObject</span></span>
```
New-AzMariaDbReplica -Master <IServer> -ReplicaName <String> [-SubscriptionId <String>] [-Location <String>]
 [-Sku <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="0553e-107">描述</span><span class="sxs-lookup"><span data-stu-id="0553e-107">DESCRIPTION</span></span>
<span data-ttu-id="0553e-108">建立 MariaDB 伺服器的複本。</span><span class="sxs-lookup"><span data-stu-id="0553e-108">Creates a replica of a MariaDB server.</span></span>

## <span data-ttu-id="0553e-109">例子</span><span class="sxs-lookup"><span data-stu-id="0553e-109">EXAMPLES</span></span>

### <span data-ttu-id="0553e-110">範例 1：為 MariaDB 建立複本 db</span><span class="sxs-lookup"><span data-stu-id="0553e-110">Example 1: Create a replica db for a MariaDB</span></span>
```powershell
PS C:\> New-AzMariaDbReplica -MasterName mariadb-test-9pebvn -ReplicaName mariadb-test-9pebvn-rep01 -ResourceGroupName mariadb-test-qu5ov0

Name                      Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                      -------- ------------------ ------- ----------------------- -------   -------        --------------
mariadb-test-9pebvn-rep01 eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="0553e-111">此命令會為 MariaDB 建立複本 db。</span><span class="sxs-lookup"><span data-stu-id="0553e-111">This command creates a replica db for a MariaDB.</span></span>

### <span data-ttu-id="0553e-112">範例 2：為 MariaDB 建立複本 db</span><span class="sxs-lookup"><span data-stu-id="0553e-112">Example 2: Create a replica db for a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbServer -Name mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0 | New-AzMariaDbReplica -ReplicaName mariadb-test-9pebvn-rep02

Name                      Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                      -------- ------------------ ------- ----------------------- -------   -------        --------------
mariadb-test-9pebvn-rep02 eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="0553e-113">此命令會為 MariaDB 建立複本 db。</span><span class="sxs-lookup"><span data-stu-id="0553e-113">This command creates a replica db for a MariaDB.</span></span>

### <span data-ttu-id="0553e-114">範例 3：為 MariaDB 建立複本 db</span><span class="sxs-lookup"><span data-stu-id="0553e-114">Example 3: Create a replica db for a MariaDB</span></span>
```powershell
PS C:\> $mariaDb = Get-AzMariaDbServer -Name mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0 
PS C:\> New-AzMariaDbReplica -Master $mariaDb -ReplicaName mariadb-test-9pebvn-rep03

Name                      Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                      -------- ------------------ ------- ----------------------- -------   -------        --------------
mariadb-test-9pebvn-rep03 eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="0553e-115">這個包含參數輸入指令的命令會為 MariaDB 建立包含參數輸入object 的複本 db。</span><span class="sxs-lookup"><span data-stu-id="0553e-115">This command with parameter inputobject creates a replica db with parameter inputobject for a MariaDB.</span></span>

## <span data-ttu-id="0553e-116">參數</span><span class="sxs-lookup"><span data-stu-id="0553e-116">PARAMETERS</span></span>

### <span data-ttu-id="0553e-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0553e-117">-AsJob</span></span>
<span data-ttu-id="0553e-118">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="0553e-118">Run the command as a job</span></span>

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

### <span data-ttu-id="0553e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0553e-119">-DefaultProfile</span></span>
<span data-ttu-id="0553e-120">區域 DefaultParameters 用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="0553e-120">region DefaultParameters The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0553e-121">-位置</span><span class="sxs-lookup"><span data-stu-id="0553e-121">-Location</span></span>
<span data-ttu-id="0553e-122">資源所在位置。</span><span class="sxs-lookup"><span data-stu-id="0553e-122">The location the resource resides in.</span></span>

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

### <span data-ttu-id="0553e-123">-主控點</span><span class="sxs-lookup"><span data-stu-id="0553e-123">-Master</span></span>
<span data-ttu-id="0553e-124">要還原的來源伺服器物件。</span><span class="sxs-lookup"><span data-stu-id="0553e-124">The source server object to restore from.</span></span>
<span data-ttu-id="0553e-125">若要建構，請參閱 MASTER 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="0553e-125">To construct, see NOTES section for MASTER properties and create a hash table.</span></span>

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

### <span data-ttu-id="0553e-126">-MasterName</span><span class="sxs-lookup"><span data-stu-id="0553e-126">-MasterName</span></span>
<span data-ttu-id="0553e-127">MariaDB 伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="0553e-127">MariaDB server name.</span></span>

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

### <span data-ttu-id="0553e-128">-NoWait</span><span class="sxs-lookup"><span data-stu-id="0553e-128">-NoWait</span></span>
<span data-ttu-id="0553e-129">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="0553e-129">Run the command asynchronously</span></span>

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

### <span data-ttu-id="0553e-130">-副本名稱</span><span class="sxs-lookup"><span data-stu-id="0553e-130">-ReplicaName</span></span>
<span data-ttu-id="0553e-131">複本名稱。</span><span class="sxs-lookup"><span data-stu-id="0553e-131">Replica name.</span></span>

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

### <span data-ttu-id="0553e-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0553e-132">-ResourceGroupName</span></span>
<span data-ttu-id="0553e-133">您可以從 Azure Resource Manager API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="0553e-133">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="0553e-134">-SKU</span><span class="sxs-lookup"><span data-stu-id="0553e-134">-Sku</span></span>
<span data-ttu-id="0553e-135">SKU 的名稱，通常是 tier + family + 核心，例如 B_Gen4_1、GP_Gen5_8。</span><span class="sxs-lookup"><span data-stu-id="0553e-135">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="0553e-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0553e-136">-SubscriptionId</span></span>
<span data-ttu-id="0553e-137">訂閱識別碼是每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="0553e-137">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="0553e-138">-標記</span><span class="sxs-lookup"><span data-stu-id="0553e-138">-Tag</span></span>
<span data-ttu-id="0553e-139">以金鑰值組形式顯示的應用程式特定中繼資料。</span><span class="sxs-lookup"><span data-stu-id="0553e-139">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="0553e-140">-確認</span><span class="sxs-lookup"><span data-stu-id="0553e-140">-Confirm</span></span>
<span data-ttu-id="0553e-141">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="0553e-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0553e-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0553e-142">-WhatIf</span></span>
<span data-ttu-id="0553e-143">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0553e-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0553e-144">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0553e-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0553e-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0553e-145">CommonParameters</span></span>
<span data-ttu-id="0553e-146">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="0553e-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0553e-147">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0553e-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0553e-148">輸入</span><span class="sxs-lookup"><span data-stu-id="0553e-148">INPUTS</span></span>

### <span data-ttu-id="0553e-149">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.models.Api20180601Preview.IServer</span><span class="sxs-lookup"><span data-stu-id="0553e-149">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="0553e-150">輸出</span><span class="sxs-lookup"><span data-stu-id="0553e-150">OUTPUTS</span></span>

### <span data-ttu-id="0553e-151">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.models.Api20180601Preview.IServer</span><span class="sxs-lookup"><span data-stu-id="0553e-151">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="0553e-152">筆記</span><span class="sxs-lookup"><span data-stu-id="0553e-152">NOTES</span></span>

<span data-ttu-id="0553e-153">別名</span><span class="sxs-lookup"><span data-stu-id="0553e-153">ALIASES</span></span>

<span data-ttu-id="0553e-154">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="0553e-154">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0553e-155">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="0553e-155">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0553e-156">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="0553e-156">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0553e-157"><IServer>MASTER：要還原的來源伺服器物件。</span><span class="sxs-lookup"><span data-stu-id="0553e-157">MASTER <IServer>: The source server object to restore from.</span></span>
  - <span data-ttu-id="0553e-158">`Location <String>`：資源所在的位置。</span><span class="sxs-lookup"><span data-stu-id="0553e-158">`Location <String>`: The location the resource resides in.</span></span>
  - <span data-ttu-id="0553e-159">`[Tag <ITrackedResourceTags>]`：金鑰值組形式的應用程式特定中繼資料。</span><span class="sxs-lookup"><span data-stu-id="0553e-159">`[Tag <ITrackedResourceTags>]`: Application-specific metadata in the form of key-value pairs.</span></span>
    - <span data-ttu-id="0553e-160">`[(Any) <String>]`：這表示任何屬性都可以新增到這個物件。</span><span class="sxs-lookup"><span data-stu-id="0553e-160">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="0553e-161">`[AdministratorLogin <String>]`：系統管理員的伺服器登入名稱。</span><span class="sxs-lookup"><span data-stu-id="0553e-161">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="0553e-162">只能在建立伺服器時指定， (建立時) 。</span><span class="sxs-lookup"><span data-stu-id="0553e-162">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="0553e-163">`[EarliestRestoreDate <DateTime?>]`：ISO8601 格式的最早還原點建立時間 (ISO8601 格式) </span><span class="sxs-lookup"><span data-stu-id="0553e-163">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="0553e-164">`[FullyQualifiedDomainName <String>]`：伺服器完整功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="0553e-164">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="0553e-165">`[IdentityType <IdentityType?>]`：身分識別類型。</span><span class="sxs-lookup"><span data-stu-id="0553e-165">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="0553e-166">將此選項設定為 'SystemAssigned'，以自動建立及指派資源的 Azure Active Directory 主體。</span><span class="sxs-lookup"><span data-stu-id="0553e-166">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="0553e-167">`[MasterServerId <String>]`：複本伺服器的主伺服器識別碼。</span><span class="sxs-lookup"><span data-stu-id="0553e-167">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="0553e-168">`[ReplicaCapacity <Int32?>]`：主伺服器可擁有的最大複本數目。</span><span class="sxs-lookup"><span data-stu-id="0553e-168">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="0553e-169">`[ReplicationRole <String>]`：伺服器的複製角色。</span><span class="sxs-lookup"><span data-stu-id="0553e-169">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="0553e-170">`[SkuCapacity <Int32?>]`：向上/縮小容量，代表伺服器的計算單位。</span><span class="sxs-lookup"><span data-stu-id="0553e-170">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="0553e-171">`[SkuFamily <String>]`：硬體系列。</span><span class="sxs-lookup"><span data-stu-id="0553e-171">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="0553e-172">`[SkuName <String>]`：SKU 的名稱，通常是 tier + family + cores，例如B_Gen4_1、GP_Gen5_8。</span><span class="sxs-lookup"><span data-stu-id="0553e-172">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="0553e-173">`[SkuSize <String>]`：大小代碼，以適當的資源解譯。</span><span class="sxs-lookup"><span data-stu-id="0553e-173">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="0553e-174">`[SkuTier <SkuTier?>]`：特定 SKU 的層級，例如基本。</span><span class="sxs-lookup"><span data-stu-id="0553e-174">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="0553e-175">`[SslEnforcement <SslEnforcementEnum?>]`：在連接至伺服器時啟用 ssl 強制執行或不啟用。</span><span class="sxs-lookup"><span data-stu-id="0553e-175">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="0553e-176">`[StorageProfileBackupRetentionDay <Int32?>]`：伺服器的備份保留天數。</span><span class="sxs-lookup"><span data-stu-id="0553e-176">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="0553e-177">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`：針對伺服器備份啟用異地重複或不啟用。</span><span class="sxs-lookup"><span data-stu-id="0553e-177">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="0553e-178">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`：啟用儲存空間自動放大。</span><span class="sxs-lookup"><span data-stu-id="0553e-178">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="0553e-179">`[StorageProfileStorageMb <Int32?>]`：伺服器允許的最大儲存空間。</span><span class="sxs-lookup"><span data-stu-id="0553e-179">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="0553e-180">`[UserVisibleState <ServerState?>]`：使用者可看見的伺服器狀態。</span><span class="sxs-lookup"><span data-stu-id="0553e-180">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="0553e-181">`[Version <ServerVersion?>]`：伺服器版本。</span><span class="sxs-lookup"><span data-stu-id="0553e-181">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="0553e-182">相關連結</span><span class="sxs-lookup"><span data-stu-id="0553e-182">RELATED LINKS</span></span>

