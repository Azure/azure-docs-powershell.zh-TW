---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/get-azpostgresqlconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlConnectionString.md
ms.openlocfilehash: 8df35a38889e2c91bd74625ae916fd10739d9db1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93970230"
---
# <span data-ttu-id="e3918-101">Get-AzPostgreSqlConnectionString</span><span class="sxs-lookup"><span data-stu-id="e3918-101">Get-AzPostgreSqlConnectionString</span></span>

## <span data-ttu-id="e3918-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e3918-102">SYNOPSIS</span></span>
<span data-ttu-id="e3918-103">根據用戶端連線提供者取得連接字串。</span><span class="sxs-lookup"><span data-stu-id="e3918-103">Get the connection string according to client connection provider.</span></span>

## <span data-ttu-id="e3918-104">句法</span><span class="sxs-lookup"><span data-stu-id="e3918-104">SYNTAX</span></span>

### <span data-ttu-id="e3918-105">取得 (預設) </span><span class="sxs-lookup"><span data-stu-id="e3918-105">Get (Default)</span></span>
```
Get-AzPostgreSqlConnectionString -Client <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e3918-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e3918-106">GetViaIdentity</span></span>
```
Get-AzPostgreSqlConnectionString -Client <String> -InputObject <IServer> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="e3918-107">說明</span><span class="sxs-lookup"><span data-stu-id="e3918-107">DESCRIPTION</span></span>
<span data-ttu-id="e3918-108">根據用戶端連線提供者取得連接字串。</span><span class="sxs-lookup"><span data-stu-id="e3918-108">Get the connection string according to client connection provider.</span></span>

## <span data-ttu-id="e3918-109">示例</span><span class="sxs-lookup"><span data-stu-id="e3918-109">EXAMPLES</span></span>

### <span data-ttu-id="e3918-110">範例1：透過資源群組和伺服器名稱取得 PostgreSql 伺服器連接字串</span><span class="sxs-lookup"><span data-stu-id="e3918-110">Example 1: Get PostgreSql server connection string by resource group and server name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlConnectionString -Client ADO.NET -Name PostgreSqlTestServer -ResourceGroupName PostgreSqlTestRG

Server=postgresqltestserver.postgres.database.azure.com;Database={your_database};Port=5432;User Id=pwsh@postgresqltestserver;Password={your_password};Ssl Mode=Require;
```

<span data-ttu-id="e3918-111">這個 Cmdlet 會透過資源群組和伺服器名稱取得 PostgreSql server 連接字串。</span><span class="sxs-lookup"><span data-stu-id="e3918-111">This cmdlet gets PostgreSql server connection string by resource group and server name.</span></span>

### <span data-ttu-id="e3918-112">範例2：透過身分識別來取得 PostgreSql server 連接字串</span><span class="sxs-lookup"><span data-stu-id="e3918-112">Example 2: Get PostgreSql server connection string by identity</span></span>
```powershell
PS C:\> Get-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer | Get-AzPostgreSqlConnectionString -Client PHP

host=postgresqltestserver.postgres.database.azure.com port=5432 dbname={your_database} user=pwsh@postgresqltestserver password={your_password} sslmode=require
```

<span data-ttu-id="e3918-113">這個 Cmdlet 會透過身分識別來取得 PostgreSql server 連接字串。</span><span class="sxs-lookup"><span data-stu-id="e3918-113">This cmdlet gets PostgreSql server connection string by identity.</span></span>

## <span data-ttu-id="e3918-114">參數</span><span class="sxs-lookup"><span data-stu-id="e3918-114">PARAMETERS</span></span>

### <span data-ttu-id="e3918-115">-用戶端</span><span class="sxs-lookup"><span data-stu-id="e3918-115">-Client</span></span>
<span data-ttu-id="e3918-116">用戶端連線提供者。</span><span class="sxs-lookup"><span data-stu-id="e3918-116">Client connection provider.</span></span>

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

### <span data-ttu-id="e3918-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3918-117">-DefaultProfile</span></span>
<span data-ttu-id="e3918-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e3918-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3918-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e3918-119">-InputObject</span></span>
<span data-ttu-id="e3918-120">要從中建立複本的來源伺服器物件。</span><span class="sxs-lookup"><span data-stu-id="e3918-120">The source server object to create replica from.</span></span>
<span data-ttu-id="e3918-121">若要構造，請參閱適用于 INPUTOBJECT 屬性的 [記事] 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="e3918-121">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e3918-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="e3918-122">-Name</span></span>
<span data-ttu-id="e3918-123">伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="e3918-123">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3918-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3918-124">-ResourceGroupName</span></span>
<span data-ttu-id="e3918-125">包含資源之資源群組的名稱，您可以從 Azure 資源管理員 API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="e3918-125">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3918-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e3918-126">-SubscriptionId</span></span>
<span data-ttu-id="e3918-127">識別 Azure 訂閱的訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="e3918-127">The subscription ID that identifies an Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3918-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3918-128">CommonParameters</span></span>
<span data-ttu-id="e3918-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e3918-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3918-130">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e3918-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3918-131">輸入</span><span class="sxs-lookup"><span data-stu-id="e3918-131">INPUTS</span></span>

### <span data-ttu-id="e3918-132">IServer （PostgreSql）。 Api20171201。</span><span class="sxs-lookup"><span data-stu-id="e3918-132">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="e3918-133">輸出</span><span class="sxs-lookup"><span data-stu-id="e3918-133">OUTPUTS</span></span>

### <span data-ttu-id="e3918-134">System.object</span><span class="sxs-lookup"><span data-stu-id="e3918-134">System.String</span></span>

## <span data-ttu-id="e3918-135">筆記</span><span class="sxs-lookup"><span data-stu-id="e3918-135">NOTES</span></span>

<span data-ttu-id="e3918-136">別名</span><span class="sxs-lookup"><span data-stu-id="e3918-136">ALIASES</span></span>

<span data-ttu-id="e3918-137">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="e3918-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e3918-138">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="e3918-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e3918-139">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="e3918-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e3918-140">INPUTOBJECT <IServer> ：要從中建立複本的來源伺服器物件。</span><span class="sxs-lookup"><span data-stu-id="e3918-140">INPUTOBJECT <IServer>: The source server object to create replica from.</span></span>
  - <span data-ttu-id="e3918-141">`Location <String>`：資源所在的位置。</span><span class="sxs-lookup"><span data-stu-id="e3918-141">`Location <String>`: The location the resource resides in.</span></span>
  - <span data-ttu-id="e3918-142">`[Tag <ITrackedResourceTags>]`：以鍵值對形式的特定應用程式中繼資料。</span><span class="sxs-lookup"><span data-stu-id="e3918-142">`[Tag <ITrackedResourceTags>]`: Application-specific metadata in the form of key-value pairs.</span></span>
    - <span data-ttu-id="e3918-143">`[(Any) <String>]`：這表示您可以將任何屬性新增至此物件。</span><span class="sxs-lookup"><span data-stu-id="e3918-143">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="e3918-144">`[AdministratorLogin <String>]`：管理員的伺服器登入名稱。</span><span class="sxs-lookup"><span data-stu-id="e3918-144">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="e3918-145">只能在 (建立伺服器時指定，且在建立) 時需要。</span><span class="sxs-lookup"><span data-stu-id="e3918-145">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="e3918-146">`[EarliestRestoreDate <DateTime?>]`： (ISO8601 格式的最早還原點建立時間) </span><span class="sxs-lookup"><span data-stu-id="e3918-146">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="e3918-147">`[FullyQualifiedDomainName <String>]`：伺服器的完整功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="e3918-147">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="e3918-148">`[IdentityType <IdentityType?>]`：身分識別類型。</span><span class="sxs-lookup"><span data-stu-id="e3918-148">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="e3918-149">將此值設定為 ' SystemAssigned」，即可自動為資源建立並指派 Azure Active Directory 主體。</span><span class="sxs-lookup"><span data-stu-id="e3918-149">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="e3918-150">`[InfrastructureEncryption <InfrastructureEncryption?>]`：顯示伺服器是否已啟用基礎結構加密的狀態。</span><span class="sxs-lookup"><span data-stu-id="e3918-150">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Status showing whether the server enabled infrastructure encryption.</span></span>
  - <span data-ttu-id="e3918-151">`[MasterServerId <String>]`：複本伺服器的主伺服器 id。</span><span class="sxs-lookup"><span data-stu-id="e3918-151">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="e3918-152">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`：為伺服器強制執行最低的 Tls 版本。</span><span class="sxs-lookup"><span data-stu-id="e3918-152">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Enforce a minimal Tls version for the server.</span></span>
  - <span data-ttu-id="e3918-153">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`：此伺服器是否允許公用網路存取。</span><span class="sxs-lookup"><span data-stu-id="e3918-153">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Whether or not public network access is allowed for this server.</span></span> <span data-ttu-id="e3918-154">Value 是 optional，但如果傳入，就必須是「Enabled」或「Disabled」</span><span class="sxs-lookup"><span data-stu-id="e3918-154">Value is optional but if passed in, must be 'Enabled' or 'Disabled'</span></span>
  - <span data-ttu-id="e3918-155">`[ReplicaCapacity <Int32?>]`：主伺服器可擁有的複本數目上限。</span><span class="sxs-lookup"><span data-stu-id="e3918-155">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="e3918-156">`[ReplicationRole <String>]`：伺服器的複製角色。</span><span class="sxs-lookup"><span data-stu-id="e3918-156">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="e3918-157">`[SkuCapacity <Int32?>]`： [擴大/縮小] 容量，代表伺服器的計算單位。</span><span class="sxs-lookup"><span data-stu-id="e3918-157">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="e3918-158">`[SkuFamily <String>]`：硬體系列。</span><span class="sxs-lookup"><span data-stu-id="e3918-158">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="e3918-159">`[SkuName <String>]`： Sku 的名稱，通常是 [層 + 家庭 + 核心]，例如 B_Gen4_1、GP_Gen5_8。</span><span class="sxs-lookup"><span data-stu-id="e3918-159">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="e3918-160">`[SkuSize <String>]`：根據需要由資源來轉譯的大小代碼。</span><span class="sxs-lookup"><span data-stu-id="e3918-160">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="e3918-161">`[SkuTier <SkuTier?>]`：特定 SKU 的層級，例如基本。</span><span class="sxs-lookup"><span data-stu-id="e3918-161">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="e3918-162">`[SslEnforcement <SslEnforcementEnum?>]`[：在連線至伺服器時，啟用 ssl 強制執行。</span><span class="sxs-lookup"><span data-stu-id="e3918-162">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="e3918-163">`[StorageProfileBackupRetentionDay <Int32?>]`：伺服器的備份保留天數。</span><span class="sxs-lookup"><span data-stu-id="e3918-163">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="e3918-164">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`：啟用地域冗余，或不用於伺服器備份。</span><span class="sxs-lookup"><span data-stu-id="e3918-164">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="e3918-165">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`：啟用儲存空間自動增長。</span><span class="sxs-lookup"><span data-stu-id="e3918-165">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="e3918-166">`[StorageProfileStorageMb <Int32?>]`：伺服器允許的最大儲存空間。</span><span class="sxs-lookup"><span data-stu-id="e3918-166">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="e3918-167">`[UserVisibleState <ServerState?>]`：使用者可看見的伺服器狀態。</span><span class="sxs-lookup"><span data-stu-id="e3918-167">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="e3918-168">`[Version <ServerVersion?>]`：伺服器版本。</span><span class="sxs-lookup"><span data-stu-id="e3918-168">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="e3918-169">相關連結</span><span class="sxs-lookup"><span data-stu-id="e3918-169">RELATED LINKS</span></span>

