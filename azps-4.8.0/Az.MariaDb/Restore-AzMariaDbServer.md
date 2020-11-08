---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/restore-azmariadbserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Restore-AzMariaDbServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Restore-AzMariaDbServer.md
ms.openlocfilehash: 95988d83cbb4c3dcf0b5da890bf38f8c40eb4dfa
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93970998"
---
# <span data-ttu-id="83243-101">Restore-AzMariaDbServer</span><span class="sxs-lookup"><span data-stu-id="83243-101">Restore-AzMariaDbServer</span></span>

## <span data-ttu-id="83243-102">摘要</span><span class="sxs-lookup"><span data-stu-id="83243-102">SYNOPSIS</span></span>
<span data-ttu-id="83243-103">從現有的 MariaDB 還原 MariaDB。</span><span class="sxs-lookup"><span data-stu-id="83243-103">Restore a MariaDB from a existing MariaDB.</span></span>

## <span data-ttu-id="83243-104">句法</span><span class="sxs-lookup"><span data-stu-id="83243-104">SYNTAX</span></span>

```
Restore-AzMariaDbServer -Name <String> -RestorePointInTime <DateTime> [-InputObject <IServer>]
 [-ResourceGroupName <String>] [-ServerName <String>] [-SubscriptionId <String>] [-Location <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="83243-105">說明</span><span class="sxs-lookup"><span data-stu-id="83243-105">DESCRIPTION</span></span>
<span data-ttu-id="83243-106">從現有的 MariaDB 還原 MariaDB。</span><span class="sxs-lookup"><span data-stu-id="83243-106">Restore a MariaDB from a existing MariaDB.</span></span>

## <span data-ttu-id="83243-107">示例</span><span class="sxs-lookup"><span data-stu-id="83243-107">EXAMPLES</span></span>

### <span data-ttu-id="83243-108">範例1：依伺服器名稱還原 PointInTime MariaDB。</span><span class="sxs-lookup"><span data-stu-id="83243-108">Example 1: Restore a PointInTime MariaDB by server name.</span></span>
```powershell
PS C:\> Restore-AzMariaDbServer -Name restore-db01 -ServerName mariadb-test-usegeo -ResourceGroupName mariadb-test-4rih5z -UsePointInTimeRestore -RestorePointInTime $(Get-Date) -Location eastus

Name         Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----         -------- ------------------ ------- ----------------------- -------   -------        --------------
restore-db01 eastus   adminuser          10.2    5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="83243-109">這個命令會透過伺服器名稱還原 PointInTime MariaDB。</span><span class="sxs-lookup"><span data-stu-id="83243-109">This command restore a PointInTime MariaDB by server name.</span></span>

### <span data-ttu-id="83243-110">範例2：透過 server 物件還原 PointInTime MariaDB</span><span class="sxs-lookup"><span data-stu-id="83243-110">Example 2: Restore a PointInTime MariaDB by server object</span></span>
```powershell
PS C:\> $db = Get-AzMariaDbServer -Name mariadb-test-usegeo -ResourceGroupName mariadb-test-4rih5z
PS C:\>Restore-AzMariaDbServer -Name restore-db02 -InputObject $db -UsePointInTimeRestore -RestorePointInTime $(Get-Date) -Location eastus

Name         Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----         -------- ------------------ ------- ----------------------- -------   -------        --------------
restore-db02 eastus   adminuser          10.2    5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="83243-111">這個命令會透過 server 物件還原 PointInTime MariaDB。</span><span class="sxs-lookup"><span data-stu-id="83243-111">This command restore a PointInTime MariaDB by server object.</span></span>

## <span data-ttu-id="83243-112">參數</span><span class="sxs-lookup"><span data-stu-id="83243-112">PARAMETERS</span></span>

### <span data-ttu-id="83243-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="83243-113">-AsJob</span></span>
<span data-ttu-id="83243-114">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="83243-114">Run the command as a job</span></span>

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

### <span data-ttu-id="83243-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83243-115">-DefaultProfile</span></span>
<span data-ttu-id="83243-116">地區 DefaultParameters 用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="83243-116">region DefaultParameters The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="83243-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="83243-117">-InputObject</span></span>
<span data-ttu-id="83243-118">要從中還原的源伺服器物件。</span><span class="sxs-lookup"><span data-stu-id="83243-118">The source server object to restore from.</span></span>
<span data-ttu-id="83243-119">若要構造，請參閱適用于 INPUTOBJECT 屬性的 [記事] 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="83243-119">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="83243-120">-位置</span><span class="sxs-lookup"><span data-stu-id="83243-120">-Location</span></span>
<span data-ttu-id="83243-121">資源所在的位置。</span><span class="sxs-lookup"><span data-stu-id="83243-121">The location the resource resides in.</span></span>

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

### <span data-ttu-id="83243-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="83243-122">-Name</span></span>
<span data-ttu-id="83243-123">要還原的目標伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="83243-123">The dest server name to restore from.</span></span>

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

### <span data-ttu-id="83243-124">-NoWait</span><span class="sxs-lookup"><span data-stu-id="83243-124">-NoWait</span></span>
<span data-ttu-id="83243-125">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="83243-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="83243-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83243-126">-ResourceGroupName</span></span>
<span data-ttu-id="83243-127">包含資源之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="83243-127">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="83243-128">您可以從 Azure 資源管理器 API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="83243-128">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="83243-129">-RestorePointInTime</span><span class="sxs-lookup"><span data-stu-id="83243-129">-RestorePointInTime</span></span>
<span data-ttu-id="83243-130">[地區] PointInTimeRestore 資源所在的位置。</span><span class="sxs-lookup"><span data-stu-id="83243-130">region PointInTimeRestore The location the resource resides in.</span></span>

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

### <span data-ttu-id="83243-131">-ServerName</span><span class="sxs-lookup"><span data-stu-id="83243-131">-ServerName</span></span>
<span data-ttu-id="83243-132">要從中還原的源伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="83243-132">The source server name to restore from.</span></span>

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

### <span data-ttu-id="83243-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="83243-133">-SubscriptionId</span></span>
<span data-ttu-id="83243-134">取得唯一識別 Microsoft Azure 訂閱的訂閱 Id。</span><span class="sxs-lookup"><span data-stu-id="83243-134">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="83243-135">訂閱識別碼是每個服務呼叫 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="83243-135">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="83243-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="83243-136">-Tag</span></span>
<span data-ttu-id="83243-137">以鍵值對形式的特定應用程式中繼資料。</span><span class="sxs-lookup"><span data-stu-id="83243-137">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="83243-138">-確認</span><span class="sxs-lookup"><span data-stu-id="83243-138">-Confirm</span></span>
<span data-ttu-id="83243-139">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="83243-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83243-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83243-140">-WhatIf</span></span>
<span data-ttu-id="83243-141">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="83243-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83243-142">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="83243-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83243-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83243-143">CommonParameters</span></span>
<span data-ttu-id="83243-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="83243-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83243-145">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="83243-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83243-146">輸入</span><span class="sxs-lookup"><span data-stu-id="83243-146">INPUTS</span></span>

### <span data-ttu-id="83243-147">IServer （MariaDb）。 Api20180601Preview。</span><span class="sxs-lookup"><span data-stu-id="83243-147">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="83243-148">輸出</span><span class="sxs-lookup"><span data-stu-id="83243-148">OUTPUTS</span></span>

### <span data-ttu-id="83243-149">IServer （MariaDb）。 Api20180601Preview。</span><span class="sxs-lookup"><span data-stu-id="83243-149">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="83243-150">筆記</span><span class="sxs-lookup"><span data-stu-id="83243-150">NOTES</span></span>

<span data-ttu-id="83243-151">別名</span><span class="sxs-lookup"><span data-stu-id="83243-151">ALIASES</span></span>

<span data-ttu-id="83243-152">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="83243-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="83243-153">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="83243-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="83243-154">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="83243-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="83243-155">INPUTOBJECT <IServer> ：要從中還原的源伺服器物件。</span><span class="sxs-lookup"><span data-stu-id="83243-155">INPUTOBJECT <IServer>: The source server object to restore from.</span></span>
  - <span data-ttu-id="83243-156">`Location <String>`：資源所在的位置。</span><span class="sxs-lookup"><span data-stu-id="83243-156">`Location <String>`: The location the resource resides in.</span></span>
  - <span data-ttu-id="83243-157">`[Tag <ITrackedResourceTags>]`：以鍵值對形式的特定應用程式中繼資料。</span><span class="sxs-lookup"><span data-stu-id="83243-157">`[Tag <ITrackedResourceTags>]`: Application-specific metadata in the form of key-value pairs.</span></span>
    - <span data-ttu-id="83243-158">`[(Any) <String>]`：這表示您可以將任何屬性新增至此物件。</span><span class="sxs-lookup"><span data-stu-id="83243-158">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="83243-159">`[AdministratorLogin <String>]`：管理員的伺服器登入名稱。</span><span class="sxs-lookup"><span data-stu-id="83243-159">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="83243-160">只能在 (建立伺服器時指定，且在建立) 時需要。</span><span class="sxs-lookup"><span data-stu-id="83243-160">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="83243-161">`[EarliestRestoreDate <DateTime?>]`： (ISO8601 格式的最早還原點建立時間) </span><span class="sxs-lookup"><span data-stu-id="83243-161">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="83243-162">`[FullyQualifiedDomainName <String>]`：伺服器的完整功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="83243-162">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="83243-163">`[IdentityType <IdentityType?>]`：身分識別類型。</span><span class="sxs-lookup"><span data-stu-id="83243-163">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="83243-164">將此值設定為 ' SystemAssigned」，即可自動為資源建立並指派 Azure Active Directory 主體。</span><span class="sxs-lookup"><span data-stu-id="83243-164">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="83243-165">`[MasterServerId <String>]`：複本伺服器的主伺服器 id。</span><span class="sxs-lookup"><span data-stu-id="83243-165">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="83243-166">`[ReplicaCapacity <Int32?>]`：主伺服器可擁有的複本數目上限。</span><span class="sxs-lookup"><span data-stu-id="83243-166">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="83243-167">`[ReplicationRole <String>]`：伺服器的複製角色。</span><span class="sxs-lookup"><span data-stu-id="83243-167">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="83243-168">`[SkuCapacity <Int32?>]`： [擴大/縮小] 容量，代表伺服器的計算單位。</span><span class="sxs-lookup"><span data-stu-id="83243-168">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="83243-169">`[SkuFamily <String>]`：硬體系列。</span><span class="sxs-lookup"><span data-stu-id="83243-169">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="83243-170">`[SkuName <String>]`： Sku 的名稱，通常是 [層 + 家庭 + 核心]，例如 B_Gen4_1、GP_Gen5_8。</span><span class="sxs-lookup"><span data-stu-id="83243-170">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="83243-171">`[SkuSize <String>]`：根據需要由資源來轉譯的大小代碼。</span><span class="sxs-lookup"><span data-stu-id="83243-171">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="83243-172">`[SkuTier <SkuTier?>]`：特定 SKU 的層級，例如基本。</span><span class="sxs-lookup"><span data-stu-id="83243-172">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="83243-173">`[SslEnforcement <SslEnforcementEnum?>]`[：在連線至伺服器時，啟用 ssl 強制執行。</span><span class="sxs-lookup"><span data-stu-id="83243-173">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="83243-174">`[StorageProfileBackupRetentionDay <Int32?>]`：伺服器的備份保留天數。</span><span class="sxs-lookup"><span data-stu-id="83243-174">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="83243-175">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`：啟用地域冗余，或不用於伺服器備份。</span><span class="sxs-lookup"><span data-stu-id="83243-175">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="83243-176">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`：啟用儲存空間自動增長。</span><span class="sxs-lookup"><span data-stu-id="83243-176">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="83243-177">`[StorageProfileStorageMb <Int32?>]`：伺服器允許的最大儲存空間。</span><span class="sxs-lookup"><span data-stu-id="83243-177">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="83243-178">`[UserVisibleState <ServerState?>]`：使用者可看見的伺服器狀態。</span><span class="sxs-lookup"><span data-stu-id="83243-178">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="83243-179">`[Version <ServerVersion?>]`：伺服器版本。</span><span class="sxs-lookup"><span data-stu-id="83243-179">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="83243-180">相關連結</span><span class="sxs-lookup"><span data-stu-id="83243-180">RELATED LINKS</span></span>

