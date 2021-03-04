---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/powershell/module/az.postgresql/get-azpostgresqlconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlConnectionString.md
ms.openlocfilehash: ae0a5f2130ea4b5120fdbe78ab4cc23a7eba29a7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913365"
---
# <span data-ttu-id="ff8ad-101">Get-AzPostgreSqlConnectionString</span><span class="sxs-lookup"><span data-stu-id="ff8ad-101">Get-AzPostgreSqlConnectionString</span></span>

## <span data-ttu-id="ff8ad-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ff8ad-102">SYNOPSIS</span></span>
<span data-ttu-id="ff8ad-103">根據用戶端連接提供者取得連接字串。</span><span class="sxs-lookup"><span data-stu-id="ff8ad-103">Get the connection string according to client connection provider.</span></span>

## <span data-ttu-id="ff8ad-104">語法</span><span class="sxs-lookup"><span data-stu-id="ff8ad-104">SYNTAX</span></span>

### <span data-ttu-id="ff8ad-105">取得 (預設) </span><span class="sxs-lookup"><span data-stu-id="ff8ad-105">Get (Default)</span></span>
```
Get-AzPostgreSqlConnectionString -Client <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ff8ad-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ff8ad-106">GetViaIdentity</span></span>
```
Get-AzPostgreSqlConnectionString -Client <String> -InputObject <IServer> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="ff8ad-107">描述</span><span class="sxs-lookup"><span data-stu-id="ff8ad-107">DESCRIPTION</span></span>
<span data-ttu-id="ff8ad-108">根據用戶端連接提供者取得連接字串。</span><span class="sxs-lookup"><span data-stu-id="ff8ad-108">Get the connection string according to client connection provider.</span></span>

## <span data-ttu-id="ff8ad-109">例子</span><span class="sxs-lookup"><span data-stu-id="ff8ad-109">EXAMPLES</span></span>

### <span data-ttu-id="ff8ad-110">範例 1：根據資源群組和伺服器名稱取得 PostgreSql 伺服器連接字串</span><span class="sxs-lookup"><span data-stu-id="ff8ad-110">Example 1: Get PostgreSql server connection string by resource group and server name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlConnectionString -Client ADO.NET -Name PostgreSqlTestServer -ResourceGroupName PostgreSqlTestRG

Server=postgresqltestserver.postgres.database.azure.com;Database={your_database};Port=5432;User Id=pwsh@postgresqltestserver;Password={your_password};Ssl Mode=Require;
```

<span data-ttu-id="ff8ad-111">此 Cmdlet 會根據資源群組和伺服器名稱，獲得 PostgreSql 伺服器連接字串。</span><span class="sxs-lookup"><span data-stu-id="ff8ad-111">This cmdlet gets PostgreSql server connection string by resource group and server name.</span></span>

### <span data-ttu-id="ff8ad-112">範例 2：根據身分識別取得 PostgreSql 伺服器連接字串</span><span class="sxs-lookup"><span data-stu-id="ff8ad-112">Example 2: Get PostgreSql server connection string by identity</span></span>
```powershell
PS C:\> Get-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer | Get-AzPostgreSqlConnectionString -Client PHP

host=postgresqltestserver.postgres.database.azure.com port=5432 dbname={your_database} user=pwsh@postgresqltestserver password={your_password} sslmode=require
```

<span data-ttu-id="ff8ad-113">此 Cmdlet 會以身分識別方式獲得 PostgreSql 伺服器連接字串。</span><span class="sxs-lookup"><span data-stu-id="ff8ad-113">This cmdlet gets PostgreSql server connection string by identity.</span></span>

## <span data-ttu-id="ff8ad-114">參數</span><span class="sxs-lookup"><span data-stu-id="ff8ad-114">PARAMETERS</span></span>

### <span data-ttu-id="ff8ad-115">-用戶端</span><span class="sxs-lookup"><span data-stu-id="ff8ad-115">-Client</span></span>
<span data-ttu-id="ff8ad-116">用戶端連接提供者。</span><span class="sxs-lookup"><span data-stu-id="ff8ad-116">Client connection provider.</span></span>

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

### <span data-ttu-id="ff8ad-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff8ad-117">-DefaultProfile</span></span>
<span data-ttu-id="ff8ad-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="ff8ad-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ff8ad-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ff8ad-119">-InputObject</span></span>
<span data-ttu-id="ff8ad-120">連接字串的伺服器若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="ff8ad-120">The server for the connection string To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ff8ad-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="ff8ad-121">-Name</span></span>
<span data-ttu-id="ff8ad-122">伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="ff8ad-122">The name of the server.</span></span>

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

### <span data-ttu-id="ff8ad-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff8ad-123">-ResourceGroupName</span></span>
<span data-ttu-id="ff8ad-124">包含資源的資源組名，您可從 Azure Resource Manager API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="ff8ad-124">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="ff8ad-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ff8ad-125">-SubscriptionId</span></span>
<span data-ttu-id="ff8ad-126">可識別 Azure 訂閱的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="ff8ad-126">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="ff8ad-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff8ad-127">CommonParameters</span></span>
<span data-ttu-id="ff8ad-128">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ff8ad-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff8ad-129">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ff8ad-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff8ad-130">輸入</span><span class="sxs-lookup"><span data-stu-id="ff8ad-130">INPUTS</span></span>

### <span data-ttu-id="ff8ad-131">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="ff8ad-131">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="ff8ad-132">輸出</span><span class="sxs-lookup"><span data-stu-id="ff8ad-132">OUTPUTS</span></span>

### <span data-ttu-id="ff8ad-133">System.String</span><span class="sxs-lookup"><span data-stu-id="ff8ad-133">System.String</span></span>

## <span data-ttu-id="ff8ad-134">筆記</span><span class="sxs-lookup"><span data-stu-id="ff8ad-134">NOTES</span></span>

<span data-ttu-id="ff8ad-135">別名</span><span class="sxs-lookup"><span data-stu-id="ff8ad-135">ALIASES</span></span>

<span data-ttu-id="ff8ad-136">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="ff8ad-136">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ff8ad-137">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="ff8ad-137">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ff8ad-138">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="ff8ad-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ff8ad-139">INPUTOBJECT： <IServer> 連接字串的伺服器</span><span class="sxs-lookup"><span data-stu-id="ff8ad-139">INPUTOBJECT <IServer>: The server for the connection string</span></span>
  - <span data-ttu-id="ff8ad-140">`Location <String>`：資源所在地的地理位置</span><span class="sxs-lookup"><span data-stu-id="ff8ad-140">`Location <String>`: The geo-location where the resource lives</span></span>
  - <span data-ttu-id="ff8ad-141">`[Tag <ITrackedResourceTags>]`：資源標記。</span><span class="sxs-lookup"><span data-stu-id="ff8ad-141">`[Tag <ITrackedResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="ff8ad-142">`[(Any) <String>]`：這表示任何屬性都可以新增到這個物件。</span><span class="sxs-lookup"><span data-stu-id="ff8ad-142">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="ff8ad-143">`[AdministratorLogin <String>]`：系統管理員的伺服器登入名稱。</span><span class="sxs-lookup"><span data-stu-id="ff8ad-143">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="ff8ad-144">只能在建立伺服器時指定， (建立時) 。</span><span class="sxs-lookup"><span data-stu-id="ff8ad-144">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="ff8ad-145">`[EarliestRestoreDate <DateTime?>]`：ISO8601 格式的最早還原點建立時間 (ISO8601 格式) </span><span class="sxs-lookup"><span data-stu-id="ff8ad-145">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="ff8ad-146">`[FullyQualifiedDomainName <String>]`：伺服器完整功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="ff8ad-146">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="ff8ad-147">`[IdentityType <IdentityType?>]`：身分識別類型。</span><span class="sxs-lookup"><span data-stu-id="ff8ad-147">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="ff8ad-148">將此選項設定為 'SystemAssigned'，以自動建立及指派資源的 Azure Active Directory 主體。</span><span class="sxs-lookup"><span data-stu-id="ff8ad-148">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="ff8ad-149">`[InfrastructureEncryption <InfrastructureEncryption?>]`：狀態顯示伺服器是否啟用基礎結構加密。</span><span class="sxs-lookup"><span data-stu-id="ff8ad-149">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Status showing whether the server enabled infrastructure encryption.</span></span>
  - <span data-ttu-id="ff8ad-150">`[MasterServerId <String>]`：複本伺服器的主伺服器識別碼。</span><span class="sxs-lookup"><span data-stu-id="ff8ad-150">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="ff8ad-151">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`：針對伺服器強制執行最小 Tls 版本。</span><span class="sxs-lookup"><span data-stu-id="ff8ad-151">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Enforce a minimal Tls version for the server.</span></span>
  - <span data-ttu-id="ff8ad-152">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`：此伺服器是否允許公用網路存取。</span><span class="sxs-lookup"><span data-stu-id="ff8ad-152">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Whether or not public network access is allowed for this server.</span></span> <span data-ttu-id="ff8ad-153">Value 為選擇性，但如果傳遞，則必須是 'Enabled' 或 'Disabled'</span><span class="sxs-lookup"><span data-stu-id="ff8ad-153">Value is optional but if passed in, must be 'Enabled' or 'Disabled'</span></span>
  - <span data-ttu-id="ff8ad-154">`[ReplicaCapacity <Int32?>]`：主伺服器可擁有的最大複本數目。</span><span class="sxs-lookup"><span data-stu-id="ff8ad-154">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="ff8ad-155">`[ReplicationRole <String>]`：伺服器的複製角色。</span><span class="sxs-lookup"><span data-stu-id="ff8ad-155">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="ff8ad-156">`[SkuCapacity <Int32?>]`：向上/縮小容量，代表伺服器的計算單位。</span><span class="sxs-lookup"><span data-stu-id="ff8ad-156">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="ff8ad-157">`[SkuFamily <String>]`：硬體系列。</span><span class="sxs-lookup"><span data-stu-id="ff8ad-157">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="ff8ad-158">`[SkuName <String>]`：SKU 的名稱，通常是 tier + family + cores，例如B_Gen4_1、GP_Gen5_8。</span><span class="sxs-lookup"><span data-stu-id="ff8ad-158">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="ff8ad-159">`[SkuSize <String>]`：大小代碼，以適當的資源解譯。</span><span class="sxs-lookup"><span data-stu-id="ff8ad-159">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="ff8ad-160">`[SkuTier <SkuTier?>]`：特定 SKU 的層級，例如基本。</span><span class="sxs-lookup"><span data-stu-id="ff8ad-160">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="ff8ad-161">`[SslEnforcement <SslEnforcementEnum?>]`：在連接至伺服器時啟用 ssl 強制執行或不啟用。</span><span class="sxs-lookup"><span data-stu-id="ff8ad-161">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="ff8ad-162">`[StorageProfileBackupRetentionDay <Int32?>]`：伺服器的備份保留天數。</span><span class="sxs-lookup"><span data-stu-id="ff8ad-162">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="ff8ad-163">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`：針對伺服器備份啟用異地重複或不啟用。</span><span class="sxs-lookup"><span data-stu-id="ff8ad-163">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="ff8ad-164">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`：啟用儲存空間自動放大。</span><span class="sxs-lookup"><span data-stu-id="ff8ad-164">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="ff8ad-165">`[StorageProfileStorageMb <Int32?>]`：伺服器允許的最大儲存空間。</span><span class="sxs-lookup"><span data-stu-id="ff8ad-165">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="ff8ad-166">`[UserVisibleState <ServerState?>]`：使用者可看見的伺服器狀態。</span><span class="sxs-lookup"><span data-stu-id="ff8ad-166">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="ff8ad-167">`[Version <ServerVersion?>]`：伺服器版本。</span><span class="sxs-lookup"><span data-stu-id="ff8ad-167">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="ff8ad-168">相關連結</span><span class="sxs-lookup"><span data-stu-id="ff8ad-168">RELATED LINKS</span></span>

