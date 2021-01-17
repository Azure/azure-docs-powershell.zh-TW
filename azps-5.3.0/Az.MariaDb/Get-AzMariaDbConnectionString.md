---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/get-azmariadbconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbConnectionString.md
ms.openlocfilehash: 1a6e96a8b8e030628655bdf95c58b726341dd2cc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98287364"
---
# <span data-ttu-id="48d82-101">Get-AzMariaDbConnectionString</span><span class="sxs-lookup"><span data-stu-id="48d82-101">Get-AzMariaDbConnectionString</span></span>

## <span data-ttu-id="48d82-102">摘要</span><span class="sxs-lookup"><span data-stu-id="48d82-102">SYNOPSIS</span></span>
<span data-ttu-id="48d82-103">在指定架構下取得 MariaDB 的連線字串。</span><span class="sxs-lookup"><span data-stu-id="48d82-103">Get connection string of a MariaDB under a given framework.</span></span>

## <span data-ttu-id="48d82-104">句法</span><span class="sxs-lookup"><span data-stu-id="48d82-104">SYNTAX</span></span>

### <span data-ttu-id="48d82-105">ServerName (預設) </span><span class="sxs-lookup"><span data-stu-id="48d82-105">ServerName (Default)</span></span>
```
Get-AzMariaDbConnectionString -Client <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="48d82-106">ServerObject</span><span class="sxs-lookup"><span data-stu-id="48d82-106">ServerObject</span></span>
```
Get-AzMariaDbConnectionString -Client <String> -InputObject <IServer> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="48d82-107">說明</span><span class="sxs-lookup"><span data-stu-id="48d82-107">DESCRIPTION</span></span>
<span data-ttu-id="48d82-108">在指定架構下取得 MariaDB 的連線字串。</span><span class="sxs-lookup"><span data-stu-id="48d82-108">Get connection string of a MariaDB under a given framework.</span></span>

## <span data-ttu-id="48d82-109">示例</span><span class="sxs-lookup"><span data-stu-id="48d82-109">EXAMPLES</span></span>

### <span data-ttu-id="48d82-110">範例1：取得 MariaDB 的連線字串</span><span class="sxs-lookup"><span data-stu-id="48d82-110">Example 1: Get a connection string of MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbConnectionString -ServerName mariadb-asd-01 -ResourceGroupName mariadb-test-qu5ov0 -Client ADO.NET

Server=mariadb-asd-01.mariadb.database.azure.com; Port=3306; Database={your_database}; Uid=adminuser@mariadb-asd-01; Pwd={your_password}; SslMode=Preferred;
```

<span data-ttu-id="48d82-111">這個命令會取得 MariaDB 的連線字串。</span><span class="sxs-lookup"><span data-stu-id="48d82-111">This command gets a connection string of MariaDB.</span></span>

### <span data-ttu-id="48d82-112">範例2：取得 MariaDB 的連線字串</span><span class="sxs-lookup"><span data-stu-id="48d82-112">Example 2: Get a connection string of MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbServer -Name mariadb-gp-t03 -ResourceGroupName lucas-manual-test | Get-AzMariaDbConnectionString -Client PHP

$con=mysqli_init();mysqli_ssl_set($con, NULL, NULL, {ca-cert filename}, NULL, NULL); mysqli_real_connect($con, "mariadb-gp-t03.mariadb.database.azure.com", "adminuser@mariadb-gp-t03", {your_password}, {your_database}, 3306);
```

<span data-ttu-id="48d82-113">這個命令會取得 MariaDB 的連線字串。</span><span class="sxs-lookup"><span data-stu-id="48d82-113">This command gets a connection string of MariaDB.</span></span>

## <span data-ttu-id="48d82-114">參數</span><span class="sxs-lookup"><span data-stu-id="48d82-114">PARAMETERS</span></span>

### <span data-ttu-id="48d82-115">-用戶端</span><span class="sxs-lookup"><span data-stu-id="48d82-115">-Client</span></span>
<span data-ttu-id="48d82-116">連接用戶端類型</span><span class="sxs-lookup"><span data-stu-id="48d82-116">Connect client type</span></span>

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

### <span data-ttu-id="48d82-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48d82-117">-DefaultProfile</span></span>
<span data-ttu-id="48d82-118">地區 DefaultParameters 用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="48d82-118">region DefaultParameters The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="48d82-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="48d82-119">-InputObject</span></span>
<span data-ttu-id="48d82-120">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="48d82-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer
Parameter Sets: ServerObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="48d82-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="48d82-121">-Name</span></span>
<span data-ttu-id="48d82-122">伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="48d82-122">The name of the server.</span></span>

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

### <span data-ttu-id="48d82-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48d82-123">-ResourceGroupName</span></span>
<span data-ttu-id="48d82-124">包含資源之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="48d82-124">The name of the resource group that contains the resource.</span></span>

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

### <span data-ttu-id="48d82-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="48d82-125">-SubscriptionId</span></span>
<span data-ttu-id="48d82-126">訂閱識別碼是每個服務通話的 URI 的一部分</span><span class="sxs-lookup"><span data-stu-id="48d82-126">The subscription ID is part of the URI for every service call</span></span>

```yaml
Type: System.String
Parameter Sets: ServerName
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48d82-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48d82-127">CommonParameters</span></span>
<span data-ttu-id="48d82-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="48d82-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48d82-129">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="48d82-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48d82-130">輸入</span><span class="sxs-lookup"><span data-stu-id="48d82-130">INPUTS</span></span>

### <span data-ttu-id="48d82-131">IServer （MariaDb）。 Api20180601Preview。</span><span class="sxs-lookup"><span data-stu-id="48d82-131">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="48d82-132">輸出</span><span class="sxs-lookup"><span data-stu-id="48d82-132">OUTPUTS</span></span>

### <span data-ttu-id="48d82-133">System.object</span><span class="sxs-lookup"><span data-stu-id="48d82-133">System.String</span></span>

## <span data-ttu-id="48d82-134">筆記</span><span class="sxs-lookup"><span data-stu-id="48d82-134">NOTES</span></span>

<span data-ttu-id="48d82-135">別名</span><span class="sxs-lookup"><span data-stu-id="48d82-135">ALIASES</span></span>

<span data-ttu-id="48d82-136">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="48d82-136">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="48d82-137">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="48d82-137">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="48d82-138">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="48d82-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="48d82-139">INPUTOBJECT <IServer> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="48d82-139">INPUTOBJECT <IServer>: Identity Parameter</span></span>
  - <span data-ttu-id="48d82-140">`Location <String>`：資源所在的位置。</span><span class="sxs-lookup"><span data-stu-id="48d82-140">`Location <String>`: The location the resource resides in.</span></span>
  - <span data-ttu-id="48d82-141">`[Tag <ITrackedResourceTags>]`：以鍵值對形式的特定應用程式中繼資料。</span><span class="sxs-lookup"><span data-stu-id="48d82-141">`[Tag <ITrackedResourceTags>]`: Application-specific metadata in the form of key-value pairs.</span></span>
    - <span data-ttu-id="48d82-142">`[(Any) <String>]`：這表示您可以將任何屬性新增至此物件。</span><span class="sxs-lookup"><span data-stu-id="48d82-142">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="48d82-143">`[AdministratorLogin <String>]`：管理員的伺服器登入名稱。</span><span class="sxs-lookup"><span data-stu-id="48d82-143">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="48d82-144">只能在 (建立伺服器時指定，且在建立) 時需要。</span><span class="sxs-lookup"><span data-stu-id="48d82-144">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="48d82-145">`[EarliestRestoreDate <DateTime?>]`： (ISO8601 格式的最早還原點建立時間) </span><span class="sxs-lookup"><span data-stu-id="48d82-145">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="48d82-146">`[FullyQualifiedDomainName <String>]`：伺服器的完整功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="48d82-146">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="48d82-147">`[IdentityType <IdentityType?>]`：身分識別類型。</span><span class="sxs-lookup"><span data-stu-id="48d82-147">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="48d82-148">將此值設定為 ' SystemAssigned」，即可自動為資源建立並指派 Azure Active Directory 主體。</span><span class="sxs-lookup"><span data-stu-id="48d82-148">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="48d82-149">`[MasterServerId <String>]`：複本伺服器的主伺服器 id。</span><span class="sxs-lookup"><span data-stu-id="48d82-149">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="48d82-150">`[ReplicaCapacity <Int32?>]`：主伺服器可擁有的複本數目上限。</span><span class="sxs-lookup"><span data-stu-id="48d82-150">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="48d82-151">`[ReplicationRole <String>]`：伺服器的複製角色。</span><span class="sxs-lookup"><span data-stu-id="48d82-151">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="48d82-152">`[SkuCapacity <Int32?>]`： [擴大/縮小] 容量，代表伺服器的計算單位。</span><span class="sxs-lookup"><span data-stu-id="48d82-152">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="48d82-153">`[SkuFamily <String>]`：硬體系列。</span><span class="sxs-lookup"><span data-stu-id="48d82-153">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="48d82-154">`[SkuName <String>]`： Sku 的名稱，通常是 [層 + 家庭 + 核心]，例如 B_Gen4_1、GP_Gen5_8。</span><span class="sxs-lookup"><span data-stu-id="48d82-154">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="48d82-155">`[SkuSize <String>]`：根據需要由資源來轉譯的大小代碼。</span><span class="sxs-lookup"><span data-stu-id="48d82-155">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="48d82-156">`[SkuTier <SkuTier?>]`：特定 SKU 的層級，例如基本。</span><span class="sxs-lookup"><span data-stu-id="48d82-156">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="48d82-157">`[SslEnforcement <SslEnforcementEnum?>]`[：在連線至伺服器時，啟用 ssl 強制執行。</span><span class="sxs-lookup"><span data-stu-id="48d82-157">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="48d82-158">`[StorageProfileBackupRetentionDay <Int32?>]`：伺服器的備份保留天數。</span><span class="sxs-lookup"><span data-stu-id="48d82-158">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="48d82-159">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`：啟用地域冗余，或不用於伺服器備份。</span><span class="sxs-lookup"><span data-stu-id="48d82-159">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="48d82-160">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`：啟用儲存空間自動增長。</span><span class="sxs-lookup"><span data-stu-id="48d82-160">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="48d82-161">`[StorageProfileStorageMb <Int32?>]`：伺服器允許的最大儲存空間。</span><span class="sxs-lookup"><span data-stu-id="48d82-161">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="48d82-162">`[UserVisibleState <ServerState?>]`：使用者可看見的伺服器狀態。</span><span class="sxs-lookup"><span data-stu-id="48d82-162">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="48d82-163">`[Version <ServerVersion?>]`：伺服器版本。</span><span class="sxs-lookup"><span data-stu-id="48d82-163">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="48d82-164">相關連結</span><span class="sxs-lookup"><span data-stu-id="48d82-164">RELATED LINKS</span></span>

