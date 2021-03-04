---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/powershell/module/az.mariadb/restore-azmariadbserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Restore-AzMariaDbServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Restore-AzMariaDbServer.md
ms.openlocfilehash: 092e109de5fd38fcad924886f55d918a91e12aed
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915429"
---
# <span data-ttu-id="dd4eb-101">Restore-AzMariaDbServer</span><span class="sxs-lookup"><span data-stu-id="dd4eb-101">Restore-AzMariaDbServer</span></span>

## <span data-ttu-id="dd4eb-102">簡介</span><span class="sxs-lookup"><span data-stu-id="dd4eb-102">SYNOPSIS</span></span>
<span data-ttu-id="dd4eb-103">從現有的 MariaDB 還原 MariaDB。</span><span class="sxs-lookup"><span data-stu-id="dd4eb-103">Restore a MariaDB from a existing MariaDB.</span></span>

## <span data-ttu-id="dd4eb-104">語法</span><span class="sxs-lookup"><span data-stu-id="dd4eb-104">SYNTAX</span></span>

```
Restore-AzMariaDbServer -Name <String> -RestorePointInTime <DateTime> [-InputObject <IServer>]
 [-ResourceGroupName <String>] [-ServerName <String>] [-SubscriptionId <String>] [-Location <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="dd4eb-105">描述</span><span class="sxs-lookup"><span data-stu-id="dd4eb-105">DESCRIPTION</span></span>
<span data-ttu-id="dd4eb-106">從現有的 MariaDB 還原 MariaDB。</span><span class="sxs-lookup"><span data-stu-id="dd4eb-106">Restore a MariaDB from a existing MariaDB.</span></span>

## <span data-ttu-id="dd4eb-107">例子</span><span class="sxs-lookup"><span data-stu-id="dd4eb-107">EXAMPLES</span></span>

### <span data-ttu-id="dd4eb-108">範例 1：根據伺服器名稱還原 PointInTime MariaDB。</span><span class="sxs-lookup"><span data-stu-id="dd4eb-108">Example 1: Restore a PointInTime MariaDB by server name.</span></span>
```powershell
PS C:\> Restore-AzMariaDbServer -Name restore-db01 -ServerName mariadb-test-usegeo -ResourceGroupName mariadb-test-4rih5z -UsePointInTimeRestore -RestorePointInTime $(Get-Date) -Location eastus

Name         Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----         -------- ------------------ ------- ----------------------- -------   -------        --------------
restore-db01 eastus   adminuser          10.2    5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="dd4eb-109">此命令會按伺服器名稱還原 PointInTime MariaDB。</span><span class="sxs-lookup"><span data-stu-id="dd4eb-109">This command restore a PointInTime MariaDB by server name.</span></span>

### <span data-ttu-id="dd4eb-110">範例 2：根據伺服器物件還原 PointInTime MariaDB</span><span class="sxs-lookup"><span data-stu-id="dd4eb-110">Example 2: Restore a PointInTime MariaDB by server object</span></span>
```powershell
PS C:\> $db = Get-AzMariaDbServer -Name mariadb-test-usegeo -ResourceGroupName mariadb-test-4rih5z
PS C:\>Restore-AzMariaDbServer -Name restore-db02 -InputObject $db -UsePointInTimeRestore -RestorePointInTime $(Get-Date) -Location eastus

Name         Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----         -------- ------------------ ------- ----------------------- -------   -------        --------------
restore-db02 eastus   adminuser          10.2    5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="dd4eb-111">此命令會按伺服器物件還原 PointInTime MariaDB。</span><span class="sxs-lookup"><span data-stu-id="dd4eb-111">This command restore a PointInTime MariaDB by server object.</span></span>

## <span data-ttu-id="dd4eb-112">參數</span><span class="sxs-lookup"><span data-stu-id="dd4eb-112">PARAMETERS</span></span>

### <span data-ttu-id="dd4eb-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dd4eb-113">-AsJob</span></span>
<span data-ttu-id="dd4eb-114">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="dd4eb-114">Run the command as a job</span></span>

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

### <span data-ttu-id="dd4eb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd4eb-115">-DefaultProfile</span></span>
<span data-ttu-id="dd4eb-116">區域 DefaultParameters 用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="dd4eb-116">region DefaultParameters The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd4eb-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dd4eb-117">-InputObject</span></span>
<span data-ttu-id="dd4eb-118">要還原的來源伺服器物件。</span><span class="sxs-lookup"><span data-stu-id="dd4eb-118">The source server object to restore from.</span></span>
<span data-ttu-id="dd4eb-119">若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="dd4eb-119">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dd4eb-120">-位置</span><span class="sxs-lookup"><span data-stu-id="dd4eb-120">-Location</span></span>
<span data-ttu-id="dd4eb-121">資源所在位置。</span><span class="sxs-lookup"><span data-stu-id="dd4eb-121">The location the resource resides in.</span></span>

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

### <span data-ttu-id="dd4eb-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="dd4eb-122">-Name</span></span>
<span data-ttu-id="dd4eb-123">這是要還原的最快伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="dd4eb-123">The dest server name to restore from.</span></span>

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

### <span data-ttu-id="dd4eb-124">-NoWait</span><span class="sxs-lookup"><span data-stu-id="dd4eb-124">-NoWait</span></span>
<span data-ttu-id="dd4eb-125">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="dd4eb-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="dd4eb-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd4eb-126">-ResourceGroupName</span></span>
<span data-ttu-id="dd4eb-127">包含資源的資源組名。</span><span class="sxs-lookup"><span data-stu-id="dd4eb-127">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="dd4eb-128">您可以從 Azure Resource Manager API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="dd4eb-128">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="dd4eb-129">-RestorePointInTime</span><span class="sxs-lookup"><span data-stu-id="dd4eb-129">-RestorePointInTime</span></span>
<span data-ttu-id="dd4eb-130">區域 PointInTimeRestore 資源所在的位置。</span><span class="sxs-lookup"><span data-stu-id="dd4eb-130">region PointInTimeRestore The location the resource resides in.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd4eb-131">-ServerName</span><span class="sxs-lookup"><span data-stu-id="dd4eb-131">-ServerName</span></span>
<span data-ttu-id="dd4eb-132">要還原的來源伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="dd4eb-132">The source server name to restore from.</span></span>

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

### <span data-ttu-id="dd4eb-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="dd4eb-133">-SubscriptionId</span></span>
<span data-ttu-id="dd4eb-134">獲得可唯一識別 Microsoft Azure 訂閱的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="dd4eb-134">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="dd4eb-135">訂閱識別碼是每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="dd4eb-135">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="dd4eb-136">-標記</span><span class="sxs-lookup"><span data-stu-id="dd4eb-136">-Tag</span></span>
<span data-ttu-id="dd4eb-137">以金鑰值組形式顯示的應用程式特定中繼資料。</span><span class="sxs-lookup"><span data-stu-id="dd4eb-137">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="dd4eb-138">-確認</span><span class="sxs-lookup"><span data-stu-id="dd4eb-138">-Confirm</span></span>
<span data-ttu-id="dd4eb-139">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="dd4eb-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd4eb-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd4eb-140">-WhatIf</span></span>
<span data-ttu-id="dd4eb-141">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="dd4eb-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd4eb-142">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="dd4eb-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd4eb-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd4eb-143">CommonParameters</span></span>
<span data-ttu-id="dd4eb-144">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="dd4eb-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd4eb-145">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dd4eb-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd4eb-146">輸入</span><span class="sxs-lookup"><span data-stu-id="dd4eb-146">INPUTS</span></span>

### <span data-ttu-id="dd4eb-147">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.models.Api20180601Preview.IServer</span><span class="sxs-lookup"><span data-stu-id="dd4eb-147">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="dd4eb-148">輸出</span><span class="sxs-lookup"><span data-stu-id="dd4eb-148">OUTPUTS</span></span>

### <span data-ttu-id="dd4eb-149">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.models.Api20180601Preview.IServer</span><span class="sxs-lookup"><span data-stu-id="dd4eb-149">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="dd4eb-150">筆記</span><span class="sxs-lookup"><span data-stu-id="dd4eb-150">NOTES</span></span>

<span data-ttu-id="dd4eb-151">別名</span><span class="sxs-lookup"><span data-stu-id="dd4eb-151">ALIASES</span></span>

<span data-ttu-id="dd4eb-152">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="dd4eb-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="dd4eb-153">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="dd4eb-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="dd4eb-154">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="dd4eb-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="dd4eb-155">INPUTOBJECT： <IServer> 要還原的來源伺服器物件。</span><span class="sxs-lookup"><span data-stu-id="dd4eb-155">INPUTOBJECT <IServer>: The source server object to restore from.</span></span>
  - <span data-ttu-id="dd4eb-156">`Location <String>`：資源所在的位置。</span><span class="sxs-lookup"><span data-stu-id="dd4eb-156">`Location <String>`: The location the resource resides in.</span></span>
  - <span data-ttu-id="dd4eb-157">`[Tag <ITrackedResourceTags>]`：金鑰值組形式的應用程式特定中繼資料。</span><span class="sxs-lookup"><span data-stu-id="dd4eb-157">`[Tag <ITrackedResourceTags>]`: Application-specific metadata in the form of key-value pairs.</span></span>
    - <span data-ttu-id="dd4eb-158">`[(Any) <String>]`：這表示任何屬性都可以新增到這個物件。</span><span class="sxs-lookup"><span data-stu-id="dd4eb-158">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="dd4eb-159">`[AdministratorLogin <String>]`：系統管理員的伺服器登入名稱。</span><span class="sxs-lookup"><span data-stu-id="dd4eb-159">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="dd4eb-160">只能在建立伺服器時指定， (建立時) 。</span><span class="sxs-lookup"><span data-stu-id="dd4eb-160">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="dd4eb-161">`[EarliestRestoreDate <DateTime?>]`：ISO8601 格式的最早還原點建立時間 (ISO8601 格式) </span><span class="sxs-lookup"><span data-stu-id="dd4eb-161">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="dd4eb-162">`[FullyQualifiedDomainName <String>]`：伺服器完整功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="dd4eb-162">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="dd4eb-163">`[IdentityType <IdentityType?>]`：身分識別類型。</span><span class="sxs-lookup"><span data-stu-id="dd4eb-163">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="dd4eb-164">將此選項設定為 'SystemAssigned'，以自動建立及指派資源的 Azure Active Directory 主體。</span><span class="sxs-lookup"><span data-stu-id="dd4eb-164">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="dd4eb-165">`[MasterServerId <String>]`：複本伺服器的主伺服器識別碼。</span><span class="sxs-lookup"><span data-stu-id="dd4eb-165">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="dd4eb-166">`[ReplicaCapacity <Int32?>]`：主伺服器可擁有的最大複本數目。</span><span class="sxs-lookup"><span data-stu-id="dd4eb-166">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="dd4eb-167">`[ReplicationRole <String>]`：伺服器的複製角色。</span><span class="sxs-lookup"><span data-stu-id="dd4eb-167">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="dd4eb-168">`[SkuCapacity <Int32?>]`：向上/縮小容量，代表伺服器的計算單位。</span><span class="sxs-lookup"><span data-stu-id="dd4eb-168">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="dd4eb-169">`[SkuFamily <String>]`：硬體系列。</span><span class="sxs-lookup"><span data-stu-id="dd4eb-169">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="dd4eb-170">`[SkuName <String>]`：SKU 的名稱，通常是 tier + family + cores，例如B_Gen4_1、GP_Gen5_8。</span><span class="sxs-lookup"><span data-stu-id="dd4eb-170">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="dd4eb-171">`[SkuSize <String>]`：大小代碼，以適當的資源解譯。</span><span class="sxs-lookup"><span data-stu-id="dd4eb-171">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="dd4eb-172">`[SkuTier <SkuTier?>]`：特定 SKU 的層級，例如基本。</span><span class="sxs-lookup"><span data-stu-id="dd4eb-172">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="dd4eb-173">`[SslEnforcement <SslEnforcementEnum?>]`：在連接至伺服器時啟用 ssl 強制執行或不啟用。</span><span class="sxs-lookup"><span data-stu-id="dd4eb-173">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="dd4eb-174">`[StorageProfileBackupRetentionDay <Int32?>]`：伺服器的備份保留天數。</span><span class="sxs-lookup"><span data-stu-id="dd4eb-174">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="dd4eb-175">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`：針對伺服器備份啟用異地重複或不啟用。</span><span class="sxs-lookup"><span data-stu-id="dd4eb-175">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="dd4eb-176">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`：啟用儲存空間自動放大。</span><span class="sxs-lookup"><span data-stu-id="dd4eb-176">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="dd4eb-177">`[StorageProfileStorageMb <Int32?>]`：伺服器允許的最大儲存空間。</span><span class="sxs-lookup"><span data-stu-id="dd4eb-177">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="dd4eb-178">`[UserVisibleState <ServerState?>]`：使用者可看見的伺服器狀態。</span><span class="sxs-lookup"><span data-stu-id="dd4eb-178">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="dd4eb-179">`[Version <ServerVersion?>]`：伺服器版本。</span><span class="sxs-lookup"><span data-stu-id="dd4eb-179">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="dd4eb-180">相關連結</span><span class="sxs-lookup"><span data-stu-id="dd4eb-180">RELATED LINKS</span></span>

