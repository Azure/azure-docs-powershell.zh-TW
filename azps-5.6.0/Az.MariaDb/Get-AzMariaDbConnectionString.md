---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/powershell/module/az.mariadb/get-azmariadbconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbConnectionString.md
ms.openlocfilehash: 6b0aad7829dc337869c26656135d039b5f74974f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909677"
---
# <span data-ttu-id="79736-101">Get-AzMariaDbConnectionString</span><span class="sxs-lookup"><span data-stu-id="79736-101">Get-AzMariaDbConnectionString</span></span>

## <span data-ttu-id="79736-102">簡介</span><span class="sxs-lookup"><span data-stu-id="79736-102">SYNOPSIS</span></span>
<span data-ttu-id="79736-103">取得指定架構下的 MariaDB 連接字串。</span><span class="sxs-lookup"><span data-stu-id="79736-103">Get connection string of a MariaDB under a given framework.</span></span>

## <span data-ttu-id="79736-104">語法</span><span class="sxs-lookup"><span data-stu-id="79736-104">SYNTAX</span></span>

### <span data-ttu-id="79736-105">ServerName (預設) </span><span class="sxs-lookup"><span data-stu-id="79736-105">ServerName (Default)</span></span>
```
Get-AzMariaDbConnectionString -Client <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="79736-106">ServerObject</span><span class="sxs-lookup"><span data-stu-id="79736-106">ServerObject</span></span>
```
Get-AzMariaDbConnectionString -Client <String> -InputObject <IServer> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="79736-107">描述</span><span class="sxs-lookup"><span data-stu-id="79736-107">DESCRIPTION</span></span>
<span data-ttu-id="79736-108">取得指定架構下的 MariaDB 連接字串。</span><span class="sxs-lookup"><span data-stu-id="79736-108">Get connection string of a MariaDB under a given framework.</span></span>

## <span data-ttu-id="79736-109">例子</span><span class="sxs-lookup"><span data-stu-id="79736-109">EXAMPLES</span></span>

### <span data-ttu-id="79736-110">範例 1：取得 MariaDB 的連接字串</span><span class="sxs-lookup"><span data-stu-id="79736-110">Example 1: Get a connection string of MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbConnectionString -ServerName mariadb-asd-01 -ResourceGroupName mariadb-test-qu5ov0 -Client ADO.NET

Server=mariadb-asd-01.mariadb.database.azure.com; Port=3306; Database={your_database}; Uid=adminuser@mariadb-asd-01; Pwd={your_password}; SslMode=Preferred;
```

<span data-ttu-id="79736-111">此命令會獲得 MariaDB 的連接字串。</span><span class="sxs-lookup"><span data-stu-id="79736-111">This command gets a connection string of MariaDB.</span></span>

### <span data-ttu-id="79736-112">範例 2：取得 MariaDB 的連接字串</span><span class="sxs-lookup"><span data-stu-id="79736-112">Example 2: Get a connection string of MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbServer -Name mariadb-gp-t03 -ResourceGroupName lucas-manual-test | Get-AzMariaDbConnectionString -Client PHP

$con=mysqli_init();mysqli_ssl_set($con, NULL, NULL, {ca-cert filename}, NULL, NULL); mysqli_real_connect($con, "mariadb-gp-t03.mariadb.database.azure.com", "adminuser@mariadb-gp-t03", {your_password}, {your_database}, 3306);
```

<span data-ttu-id="79736-113">此命令會獲得 MariaDB 的連接字串。</span><span class="sxs-lookup"><span data-stu-id="79736-113">This command gets a connection string of MariaDB.</span></span>

## <span data-ttu-id="79736-114">參數</span><span class="sxs-lookup"><span data-stu-id="79736-114">PARAMETERS</span></span>

### <span data-ttu-id="79736-115">-用戶端</span><span class="sxs-lookup"><span data-stu-id="79736-115">-Client</span></span>
<span data-ttu-id="79736-116">連接用戶端類型</span><span class="sxs-lookup"><span data-stu-id="79736-116">Connect client type</span></span>

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

### <span data-ttu-id="79736-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79736-117">-DefaultProfile</span></span>
<span data-ttu-id="79736-118">區域 DefaultParameters 用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="79736-118">region DefaultParameters The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="79736-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="79736-119">-InputObject</span></span>
<span data-ttu-id="79736-120">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="79736-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="79736-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="79736-121">-Name</span></span>
<span data-ttu-id="79736-122">伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="79736-122">The name of the server.</span></span>

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

### <span data-ttu-id="79736-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79736-123">-ResourceGroupName</span></span>
<span data-ttu-id="79736-124">包含資源的資源組名。</span><span class="sxs-lookup"><span data-stu-id="79736-124">The name of the resource group that contains the resource.</span></span>

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

### <span data-ttu-id="79736-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="79736-125">-SubscriptionId</span></span>
<span data-ttu-id="79736-126">訂閱識別碼是每個服務通話 URI 的一部分</span><span class="sxs-lookup"><span data-stu-id="79736-126">The subscription ID is part of the URI for every service call</span></span>

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

### <span data-ttu-id="79736-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79736-127">CommonParameters</span></span>
<span data-ttu-id="79736-128">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="79736-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79736-129">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="79736-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79736-130">輸入</span><span class="sxs-lookup"><span data-stu-id="79736-130">INPUTS</span></span>

### <span data-ttu-id="79736-131">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.models.Api20180601Preview.IServer</span><span class="sxs-lookup"><span data-stu-id="79736-131">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="79736-132">輸出</span><span class="sxs-lookup"><span data-stu-id="79736-132">OUTPUTS</span></span>

### <span data-ttu-id="79736-133">System.String</span><span class="sxs-lookup"><span data-stu-id="79736-133">System.String</span></span>

## <span data-ttu-id="79736-134">筆記</span><span class="sxs-lookup"><span data-stu-id="79736-134">NOTES</span></span>

<span data-ttu-id="79736-135">別名</span><span class="sxs-lookup"><span data-stu-id="79736-135">ALIASES</span></span>

<span data-ttu-id="79736-136">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="79736-136">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="79736-137">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="79736-137">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="79736-138">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="79736-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="79736-139">INPUTOBJECT： <IServer> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="79736-139">INPUTOBJECT <IServer>: Identity Parameter</span></span>
  - <span data-ttu-id="79736-140">`Location <String>`：資源所在的位置。</span><span class="sxs-lookup"><span data-stu-id="79736-140">`Location <String>`: The location the resource resides in.</span></span>
  - <span data-ttu-id="79736-141">`[Tag <ITrackedResourceTags>]`：金鑰值組形式的應用程式特定中繼資料。</span><span class="sxs-lookup"><span data-stu-id="79736-141">`[Tag <ITrackedResourceTags>]`: Application-specific metadata in the form of key-value pairs.</span></span>
    - <span data-ttu-id="79736-142">`[(Any) <String>]`：這表示任何屬性都可以新增到這個物件。</span><span class="sxs-lookup"><span data-stu-id="79736-142">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="79736-143">`[AdministratorLogin <String>]`：系統管理員的伺服器登入名稱。</span><span class="sxs-lookup"><span data-stu-id="79736-143">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="79736-144">只能在建立伺服器時指定， (建立時) 。</span><span class="sxs-lookup"><span data-stu-id="79736-144">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="79736-145">`[EarliestRestoreDate <DateTime?>]`：ISO8601 格式的最早還原點建立時間 (ISO8601 格式) </span><span class="sxs-lookup"><span data-stu-id="79736-145">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="79736-146">`[FullyQualifiedDomainName <String>]`：伺服器完整功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="79736-146">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="79736-147">`[IdentityType <IdentityType?>]`：身分識別類型。</span><span class="sxs-lookup"><span data-stu-id="79736-147">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="79736-148">將此選項設定為 'SystemAssigned'，以自動建立及指派資源的 Azure Active Directory 主體。</span><span class="sxs-lookup"><span data-stu-id="79736-148">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="79736-149">`[MasterServerId <String>]`：複本伺服器的主伺服器識別碼。</span><span class="sxs-lookup"><span data-stu-id="79736-149">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="79736-150">`[ReplicaCapacity <Int32?>]`：主伺服器可擁有的最大複本數目。</span><span class="sxs-lookup"><span data-stu-id="79736-150">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="79736-151">`[ReplicationRole <String>]`：伺服器的複製角色。</span><span class="sxs-lookup"><span data-stu-id="79736-151">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="79736-152">`[SkuCapacity <Int32?>]`：向上/縮小容量，代表伺服器的計算單位。</span><span class="sxs-lookup"><span data-stu-id="79736-152">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="79736-153">`[SkuFamily <String>]`：硬體系列。</span><span class="sxs-lookup"><span data-stu-id="79736-153">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="79736-154">`[SkuName <String>]`：SKU 的名稱，通常是 tier + family + cores，例如B_Gen4_1、GP_Gen5_8。</span><span class="sxs-lookup"><span data-stu-id="79736-154">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="79736-155">`[SkuSize <String>]`：大小代碼，以適當的資源解譯。</span><span class="sxs-lookup"><span data-stu-id="79736-155">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="79736-156">`[SkuTier <SkuTier?>]`：特定 SKU 的層級，例如基本。</span><span class="sxs-lookup"><span data-stu-id="79736-156">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="79736-157">`[SslEnforcement <SslEnforcementEnum?>]`：在連接至伺服器時啟用 ssl 強制執行或不啟用。</span><span class="sxs-lookup"><span data-stu-id="79736-157">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="79736-158">`[StorageProfileBackupRetentionDay <Int32?>]`：伺服器的備份保留天數。</span><span class="sxs-lookup"><span data-stu-id="79736-158">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="79736-159">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`：針對伺服器備份啟用異地重複或不啟用。</span><span class="sxs-lookup"><span data-stu-id="79736-159">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="79736-160">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`：啟用儲存空間自動放大。</span><span class="sxs-lookup"><span data-stu-id="79736-160">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="79736-161">`[StorageProfileStorageMb <Int32?>]`：伺服器允許的最大儲存空間。</span><span class="sxs-lookup"><span data-stu-id="79736-161">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="79736-162">`[UserVisibleState <ServerState?>]`：使用者可看見的伺服器狀態。</span><span class="sxs-lookup"><span data-stu-id="79736-162">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="79736-163">`[Version <ServerVersion?>]`：伺服器版本。</span><span class="sxs-lookup"><span data-stu-id="79736-163">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="79736-164">相關連結</span><span class="sxs-lookup"><span data-stu-id="79736-164">RELATED LINKS</span></span>

