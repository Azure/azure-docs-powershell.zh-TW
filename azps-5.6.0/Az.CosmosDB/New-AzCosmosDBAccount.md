---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBAccount.md
ms.openlocfilehash: 75085bed9c1f9b0cd0c0328b9a166c6dc08a60b7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912430"
---
# <span data-ttu-id="b598f-101">New-AzCosmosDBAccount</span><span class="sxs-lookup"><span data-stu-id="b598f-101">New-AzCosmosDBAccount</span></span>

## <span data-ttu-id="b598f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b598f-102">SYNOPSIS</span></span>
<span data-ttu-id="b598f-103">建立新一個管理中心帳戶。</span><span class="sxs-lookup"><span data-stu-id="b598f-103">Create a new CosmosDB Account.</span></span>

## <span data-ttu-id="b598f-104">語法</span><span class="sxs-lookup"><span data-stu-id="b598f-104">SYNTAX</span></span>

```
New-AzCosmosDBAccount [-EnableAutomaticFailover] [-EnableMultipleWriteLocations] [-EnableVirtualNetwork]
 [-ApiKind <String>] [-DisableKeyBasedMetadataWriteAccess] [-EnableFreeTier <Boolean>] [-Location <String[]>]
 [-LocationObject <PSLocation[]>] -ResourceGroupName <String> -Name <String>
 [-DefaultConsistencyLevel <String>] [-IpRule <String[]>] [-MaxStalenessIntervalInSeconds <Int32>]
 [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>] [-VirtualNetworkRule <String[]>]
 [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>] [-PublicNetworkAccess <String>]
 [-KeyVaultKeyUri <String>] [-EnableAnalyticalStorage <Boolean>] [-AsJob] [-NetworkAclBypass <String>]
 [-NetworkAclBypassResourceId <String[]>] [-ServerVersion <String>] [-BackupIntervalInMinutes <Int32>]
 [-BackupRetentionIntervalInHours <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b598f-105">描述</span><span class="sxs-lookup"><span data-stu-id="b598f-105">DESCRIPTION</span></span>
<span data-ttu-id="b598f-106">在給定 ResourceGroup 中建立新一個管理中心帳戶。</span><span class="sxs-lookup"><span data-stu-id="b598f-106">Create a new CosmosDB Account in the given ResourceGroup.</span></span>

## <span data-ttu-id="b598f-107">例子</span><span class="sxs-lookup"><span data-stu-id="b598f-107">EXAMPLES</span></span>

### <span data-ttu-id="b598f-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="b598f-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBAccount -ResourceGroupName resourceGroupName -Name databaseAccountName  -Location "East US"

Kind                          : GlobalDocumentDB
ProvisioningState             : Initializing
DocumentEndpoint              :
DatabaseAccountOfferType      : Standard
IpRangeFilter                 :
IsVirtualNetworkFilterEnabled : False
EnableAutomaticFailover       : False
ConsistencyPolicy             : Microsoft.Azure.Management.CosmosDB.Models.ConsistencyPolicy
Capabilities                  : {}
WriteLocations                : {databaseAccountName-eastus}
ReadLocations                 : {databaseAccountName-eastus}
FailoverPolicies              : {databaseAccountName-eastus}
VirtualNetworkRules           : {}
EnableMultipleWriteLocations  : False
Location                      : East US
Tags                          : {}
Id                            : /subscriptions/{subscriptionid}/resourceGroups/resourceGroupName/providers/Microsoft.DocumentDB/databaseAccounts/databaseAccountName
Name                          : databaseAccountName
Type                          : Microsoft.DocumentDB/databaseAccounts
NetworkAclBypass              : None
NetworkAclBypassResourceIds   : {}
```

<span data-ttu-id="b598f-109">在 ResourceGroup resourceGroupName 中，會建立一個名稱資料庫AccountName 的新管理中心帳戶。</span><span class="sxs-lookup"><span data-stu-id="b598f-109">A new CosmosDB Account with name databaseAccountName is created in the ResourceGroup resourceGroupName.</span></span>

## <span data-ttu-id="b598f-110">參數</span><span class="sxs-lookup"><span data-stu-id="b598f-110">PARAMETERS</span></span>

### <span data-ttu-id="b598f-111">-ApiKind</span><span class="sxs-lookup"><span data-stu-id="b598f-111">-ApiKind</span></span>
<span data-ttu-id="b598f-112">要建立的一種更新 DB 資料庫帳戶類型。</span><span class="sxs-lookup"><span data-stu-id="b598f-112">The type of Cosmos DB database account to create.</span></span>
<span data-ttu-id="b598f-113">接受的值：Sql、MongoDB、亞力明、表格、雅可拉。</span><span class="sxs-lookup"><span data-stu-id="b598f-113">Accepted values: Sql, MongoDB, Gremlin, Table, Cassandra.</span></span>
<span data-ttu-id="b598f-114">預設值：Sql</span><span class="sxs-lookup"><span data-stu-id="b598f-114">Default value: Sql</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b598f-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b598f-115">-AsJob</span></span>
<span data-ttu-id="b598f-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b598f-116">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b598f-117">-BackupIntervalInMinutes</span><span class="sxs-lookup"><span data-stu-id="b598f-117">-BackupIntervalInMinutes</span></span>
<span data-ttu-id="b598f-118">備份 (分鐘) ，備份 (定期模式備份的帳戶) </span><span class="sxs-lookup"><span data-stu-id="b598f-118">The interval(in minutes) with which backup are taken (only for accounts with periodic mode backups)</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b598f-119">-BackupRetentionIntervalInHours</span><span class="sxs-lookup"><span data-stu-id="b598f-119">-BackupRetentionIntervalInHours</span></span>
<span data-ttu-id="b598f-120">每個 (備份) 保留的時間 (定期模式備份帳戶) </span><span class="sxs-lookup"><span data-stu-id="b598f-120">The time(in hours) for which each backup is retained (only for accounts with periodic mode backups)</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b598f-121">-確認</span><span class="sxs-lookup"><span data-stu-id="b598f-121">-Confirm</span></span>
<span data-ttu-id="b598f-122">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="b598f-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b598f-123">-DefaultLevel</span><span class="sxs-lookup"><span data-stu-id="b598f-123">-DefaultConsistencyLevel</span></span>
<span data-ttu-id="b598f-124">系統資料庫帳戶的預設一致性層級。</span><span class="sxs-lookup"><span data-stu-id="b598f-124">Default consistency level of the Cosmos DB database account.</span></span>
<span data-ttu-id="b598f-125">接受的值：BoundedStaleness， ConsistentPrefix， 解決， 會話， Strong</span><span class="sxs-lookup"><span data-stu-id="b598f-125">Accepted values: BoundedStaleness, ConsistentPrefix, Eventual, Session, Strong</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b598f-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b598f-126">-DefaultProfile</span></span>
<span data-ttu-id="b598f-127">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b598f-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b598f-128">-DisableKeyBasedMetadataWriteAccess</span><span class="sxs-lookup"><span data-stu-id="b598f-128">-DisableKeyBasedMetadataWriteAccess</span></span>
<span data-ttu-id="b598f-129">停用透過帳戶金鑰 (資料庫、容器、輸送量) 中繼資料資源的寫入作業</span><span class="sxs-lookup"><span data-stu-id="b598f-129">Disable write operations on metadata resources (databases, containers, throughput) via account keys</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b598f-130">-EnableAnalyticalStorage</span><span class="sxs-lookup"><span data-stu-id="b598f-130">-EnableAnalyticalStorage</span></span>
<span data-ttu-id="b598f-131">布林值，指出該帳戶上是否已啟用分析器功能。</span><span class="sxs-lookup"><span data-stu-id="b598f-131">Bool to indicate if AnalyticalStorage is enabled on the account.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b598f-132">-EnableAutomaticFailover</span><span class="sxs-lookup"><span data-stu-id="b598f-132">-EnableAutomaticFailover</span></span>
<span data-ttu-id="b598f-133">在因中斷而無法使用的少數情況下，啟用寫入地區的自動容錯移轉。</span><span class="sxs-lookup"><span data-stu-id="b598f-133">Enables automatic failover of the write region in the rare event that the region is unavailable due to an outage.</span></span>
<span data-ttu-id="b598f-134">自動容錯移轉會導致帳戶產生新的寫入區域，並且會根據針對帳戶所配置的容錯移轉優先順序來選擇。</span><span class="sxs-lookup"><span data-stu-id="b598f-134">Automatic failover will result in a new write region for the account and is chosen based on the failover priorities configured for the account.</span></span>
<span data-ttu-id="b598f-135">接受的值：False、true</span><span class="sxs-lookup"><span data-stu-id="b598f-135">Accepted values: false, true</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b598f-136">-EnableFreeTier</span><span class="sxs-lookup"><span data-stu-id="b598f-136">-EnableFreeTier</span></span>
<span data-ttu-id="b598f-137">布林值，指出該帳戶上是否已啟用 FreeTier。</span><span class="sxs-lookup"><span data-stu-id="b598f-137">Bool to indicate if FreeTier is enabled on the account.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b598f-138">-EnableMultipleWriteLocations</span><span class="sxs-lookup"><span data-stu-id="b598f-138">-EnableMultipleWriteLocations</span></span>
<span data-ttu-id="b598f-139">啟用多個寫入位置。</span><span class="sxs-lookup"><span data-stu-id="b598f-139">Enable Multiple Write Locations.</span></span>
<span data-ttu-id="b598f-140">接受的值：False、true</span><span class="sxs-lookup"><span data-stu-id="b598f-140">Accepted values: false, true</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b598f-141">-EnableVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b598f-141">-EnableVirtualNetwork</span></span>
<span data-ttu-id="b598f-142">啟用一個位於管理中心 DB 資料庫帳戶的虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="b598f-142">Enables virtual network on the Cosmos DB database account.</span></span>
<span data-ttu-id="b598f-143">接受的值：False、true</span><span class="sxs-lookup"><span data-stu-id="b598f-143">Accepted values: false, true</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b598f-144">-IpRule</span><span class="sxs-lookup"><span data-stu-id="b598f-144">-IpRule</span></span>
<span data-ttu-id="b598f-145">防火牆支援。</span><span class="sxs-lookup"><span data-stu-id="b598f-145">Firewall support.</span></span> <span data-ttu-id="b598f-146">指定 CIDR 表單中的一組 IP 位址或 IP 位址範圍，以做為指定資料庫帳戶的允許用戶端 IP 清單。</span><span class="sxs-lookup"><span data-stu-id="b598f-146">Specifies the set of IP addresses or IP address ranges in CIDR form to be included as the allowed list of client IPs for a given database account.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b598f-147">-KeyVaultKeyUri</span><span class="sxs-lookup"><span data-stu-id="b598f-147">-KeyVaultKeyUri</span></span>
<span data-ttu-id="b598f-148">KeyVault 的 URI</span><span class="sxs-lookup"><span data-stu-id="b598f-148">URI of the KeyVault</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b598f-149">-位置</span><span class="sxs-lookup"><span data-stu-id="b598f-149">-Location</span></span>
<span data-ttu-id="b598f-150">新增位置至一個管理資料庫帳戶。</span><span class="sxs-lookup"><span data-stu-id="b598f-150">Add a location to the Cosmos DB database account.</span></span>
<span data-ttu-id="b598f-151">字串陣列，以容錯移轉優先順序排序。</span><span class="sxs-lookup"><span data-stu-id="b598f-151">Array of strings, ordered by failover priority.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b598f-152">-LocationObject</span><span class="sxs-lookup"><span data-stu-id="b598f-152">-LocationObject</span></span>
<span data-ttu-id="b598f-153">新增位置至一個管理資料庫帳戶。</span><span class="sxs-lookup"><span data-stu-id="b598f-153">Add a location to the Cosmos DB database account.</span></span> <span data-ttu-id="b598f-154">PSLocation 物件的陣列。</span><span class="sxs-lookup"><span data-stu-id="b598f-154">Array of PSLocation objects.</span></span>

```yaml
Type: PSLocation[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b598f-155">-MaxStalenessIntervalIn以秒為單位</span><span class="sxs-lookup"><span data-stu-id="b598f-155">-MaxStalenessIntervalInSeconds</span></span>
<span data-ttu-id="b598f-156">當使用與限制的過時一致性時，此值代表在時間範圍中 (過期) 的時間量。</span><span class="sxs-lookup"><span data-stu-id="b598f-156">When used with Bounded Staleness consistency, this value represents the time amount of staleness (in timespan) tolerated.</span></span>
<span data-ttu-id="b598f-157">此值的接受範圍為 5-86400。</span><span class="sxs-lookup"><span data-stu-id="b598f-157">Accepted range for this value is 5-86400.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b598f-158">-MaxStalenessPrefix</span><span class="sxs-lookup"><span data-stu-id="b598f-158">-MaxStalenessPrefix</span></span>
<span data-ttu-id="b598f-159">當使用與限制的過期一致性時，此值代表要過期要求的數量。</span><span class="sxs-lookup"><span data-stu-id="b598f-159">When used with Bounded Staleness consistency, this value represents the number of stale requests tolerated.</span></span>
<span data-ttu-id="b598f-160">此值的接受範圍為 1 - 2，147，483，647。</span><span class="sxs-lookup"><span data-stu-id="b598f-160">Accepted range for this value is 1 - 2,147,483,647.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b598f-161">-名稱</span><span class="sxs-lookup"><span data-stu-id="b598f-161">-Name</span></span>
<span data-ttu-id="b598f-162">系統 DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="b598f-162">Name of the Cosmos DB database account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b598f-163">-NetworkAclBypass</span><span class="sxs-lookup"><span data-stu-id="b598f-163">-NetworkAclBypass</span></span>
<span data-ttu-id="b598f-164">此帳戶的 Synapse 連結是否已啟用網路 Acl 旁路。</span><span class="sxs-lookup"><span data-stu-id="b598f-164">Whether or not Network Acl Bypass is enabled for this account for Synapse Link.</span></span> <span data-ttu-id="b598f-165">可能的值包括：「無」、」AzureServices」。</span><span class="sxs-lookup"><span data-stu-id="b598f-165">Possible values include: 'None', 'AzureServices'.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b598f-166">-NetworkAclBypassResourceId</span><span class="sxs-lookup"><span data-stu-id="b598f-166">-NetworkAclBypassResourceId</span></span>
<span data-ttu-id="b598f-167">資源識別碼清單，以允許 Synapse 連結的網路 Acl 旁路。</span><span class="sxs-lookup"><span data-stu-id="b598f-167">List of Resource Ids to allow Network Acl Bypass for Synapse Link.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b598f-168">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="b598f-168">-PublicNetworkAccess</span></span>
<span data-ttu-id="b598f-169">此伺服器是否允許公用端點存取。</span><span class="sxs-lookup"><span data-stu-id="b598f-169">Whether or not public endpoint access is allowed for this server.</span></span> <span data-ttu-id="b598f-170">可能的值包括：'Enabled'， 'Disabled'</span><span class="sxs-lookup"><span data-stu-id="b598f-170">Possible values include: 'Enabled', 'Disabled'</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b598f-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b598f-171">-ResourceGroupName</span></span>
<span data-ttu-id="b598f-172">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b598f-172">Name of resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b598f-173">-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="b598f-173">-ServerVersion</span></span>
<span data-ttu-id="b598f-174">ServerVersion，僅適用于 MongoDB 帳戶。</span><span class="sxs-lookup"><span data-stu-id="b598f-174">ServerVersion, valid only in case of MongoDB Accounts.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b598f-175">-標記</span><span class="sxs-lookup"><span data-stu-id="b598f-175">-Tag</span></span>
<span data-ttu-id="b598f-176">將標記做為索引鍵值組合的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="b598f-176">Hashtable of tags as key-value pairs.</span></span>
<span data-ttu-id="b598f-177">使用空白字串來清除現有的標記。</span><span class="sxs-lookup"><span data-stu-id="b598f-177">Use empty string to clear existing tag.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b598f-178">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="b598f-178">-VirtualNetworkRule</span></span>
<span data-ttu-id="b598f-179">ACL 的虛擬網路字串值陣列。</span><span class="sxs-lookup"><span data-stu-id="b598f-179">Array of string values of ACL's for virtual network.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b598f-180">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="b598f-180">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="b598f-181">適用于虛擬網路的 PSVirtualNetworkRuleObjects 陣列。</span><span class="sxs-lookup"><span data-stu-id="b598f-181">Array of PSVirtualNetworkRuleObjects for virtual network.</span></span>

```yaml
Type: PSVirtualNetworkRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b598f-182">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b598f-182">-WhatIf</span></span>
<span data-ttu-id="b598f-183">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b598f-183">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b598f-184">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b598f-184">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b598f-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b598f-185">CommonParameters</span></span>
<span data-ttu-id="b598f-186">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b598f-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b598f-187">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b598f-187">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b598f-188">輸入</span><span class="sxs-lookup"><span data-stu-id="b598f-188">INPUTS</span></span>

### <span data-ttu-id="b598f-189">Microsoft.Azure.Commands.AzsDB.models.PSCorsRule[]</span><span class="sxs-lookup"><span data-stu-id="b598f-189">Microsoft.Azure.Commands.CosmosDB.Models.PSCorsRule[]</span></span>

## <span data-ttu-id="b598f-190">輸出</span><span class="sxs-lookup"><span data-stu-id="b598f-190">OUTPUTS</span></span>

### <span data-ttu-id="b598f-191">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="b598f-191">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="b598f-192">筆記</span><span class="sxs-lookup"><span data-stu-id="b598f-192">NOTES</span></span>

## <span data-ttu-id="b598f-193">相關連結</span><span class="sxs-lookup"><span data-stu-id="b598f-193">RELATED LINKS</span></span>
