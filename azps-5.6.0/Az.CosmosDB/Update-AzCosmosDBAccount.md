---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/update-azcosmosdbaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccount.md
ms.openlocfilehash: cbee0ef9ce750dbb72af5be484106ccabec79321
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916768"
---
# <span data-ttu-id="09fed-101">Update-AzCosmosDBAccount</span><span class="sxs-lookup"><span data-stu-id="09fed-101">Update-AzCosmosDBAccount</span></span>

## <span data-ttu-id="09fed-102">簡介</span><span class="sxs-lookup"><span data-stu-id="09fed-102">SYNOPSIS</span></span>
<span data-ttu-id="09fed-103">更新一個一次更新的一個管理資料庫帳戶屬性。</span><span class="sxs-lookup"><span data-stu-id="09fed-103">Update a CosmosDB account attributes.</span></span>

## <span data-ttu-id="09fed-104">語法</span><span class="sxs-lookup"><span data-stu-id="09fed-104">SYNTAX</span></span>

### <span data-ttu-id="09fed-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="09fed-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBAccount [-EnableAutomaticFailover <Boolean>] [-EnableMultipleWriteLocations <Boolean>]
 [-EnableVirtualNetwork <Boolean>] [-DisableKeyBasedMetadataWriteAccess <Boolean>] -ResourceGroupName <String>
 -Name <String> [-DefaultConsistencyLevel <String>] [-IpRule <String[]>]
 [-MaxStalenessIntervalInSeconds <Int32>] [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>]
 [-VirtualNetworkRule <String[]>] [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>]
 [-PublicNetworkAccess <String>] [-KeyVaultKeyUri <String>] [-EnableAnalyticalStorage <Boolean>] [-AsJob]
 [-NetworkAclBypass <String>] [-NetworkAclBypassResourceId <String[]>] [-ServerVersion <String>]
 [-BackupIntervalInMinutes <Int32>] [-BackupRetentionIntervalInHours <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09fed-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="09fed-106">ByResourceIdParameterSet</span></span>
```
Update-AzCosmosDBAccount -ResourceId <String> [-EnableAutomaticFailover <Boolean>]
 [-EnableMultipleWriteLocations <Boolean>] [-EnableVirtualNetwork <Boolean>]
 [-DisableKeyBasedMetadataWriteAccess <Boolean>] [-DefaultConsistencyLevel <String>] [-IpRule <String[]>]
 [-MaxStalenessIntervalInSeconds <Int32>] [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>]
 [-VirtualNetworkRule <String[]>] [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>]
 [-PublicNetworkAccess <String>] [-KeyVaultKeyUri <String>] [-EnableAnalyticalStorage <Boolean>] [-AsJob]
 [-NetworkAclBypass <String>] [-NetworkAclBypassResourceId <String[]>] [-ServerVersion <String>]
 [-BackupIntervalInMinutes <Int32>] [-BackupRetentionIntervalInHours <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09fed-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="09fed-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBAccount -InputObject <PSDatabaseAccountGetResults> [-EnableAutomaticFailover <Boolean>]
 [-EnableMultipleWriteLocations <Boolean>] [-EnableVirtualNetwork <Boolean>]
 [-DisableKeyBasedMetadataWriteAccess <Boolean>] [-DefaultConsistencyLevel <String>] [-IpRule <String[]>]
 [-MaxStalenessIntervalInSeconds <Int32>] [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>]
 [-VirtualNetworkRule <String[]>] [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>]
 [-PublicNetworkAccess <String>] [-KeyVaultKeyUri <String>] [-EnableAnalyticalStorage <Boolean>] [-AsJob]
 [-NetworkAclBypass <String>] [-NetworkAclBypassResourceId <String[]>] [-ServerVersion <String>]
 [-BackupIntervalInMinutes <Int32>] [-BackupRetentionIntervalInHours <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09fed-108">描述</span><span class="sxs-lookup"><span data-stu-id="09fed-108">DESCRIPTION</span></span>
<span data-ttu-id="09fed-109">更新一個管理中心帳戶的屬性。</span><span class="sxs-lookup"><span data-stu-id="09fed-109">Update the properties of a CosmosDB account.</span></span> <span data-ttu-id="09fed-110">無法以模擬更新帳戶區域與其他屬性。</span><span class="sxs-lookup"><span data-stu-id="09fed-110">Cannot update Account Regions simulataneously with other properties.</span></span>

## <span data-ttu-id="09fed-111">例子</span><span class="sxs-lookup"><span data-stu-id="09fed-111">EXAMPLES</span></span>

### <span data-ttu-id="09fed-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="09fed-112">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBAccount -ResourceGroupName resourceGroupName -Name accountName -DefaultConsistencyLevel "Strong" -EnableAutomaticFailover 1 -EnableMultipleWriteLocations 1 -EnableVirtualNetwork 1

Kind                          : GlobalDocumentDB
ProvisioningState             : Initializing
DocumentEndpoint              :
DatabaseAccountOfferType      : Standard
IpRangeFilter                 :
IsVirtualNetworkFilterEnabled : True
EnableAutomaticFailover       : True
ConsistencyPolicy             : Microsoft.Azure.Management.CosmosDB.Fluent.Models.ConsistencyPolicy
Capabilities                  : {}
WriteLocations                : {accountName-eastus}
ReadLocations                 : {accountName-eastus}
FailoverPolicies              : {accountName-eastus}
VirtualNetworkRules           : {}
EnableMultipleWriteLocations  : True
Location                      : East US
Tags                          : {}
Id                            : /subscriptions/{subscriptionid}/resourceGroups/resourceGroupName/providers/Microsoft.DocumentDB/databaseAccounts/accountName
Name                          : accountName
Type                          : Microsoft.DocumentDB/databaseAccounts
NetworkAclBypass              : None
NetworkAclBypassResourceIds   : {}
```

<span data-ttu-id="09fed-113">將 DefaultLevel 更新為「強」、啟用的自動Failover、啟用多重WriteLocations，以及具有 name accountName 的 Enabled VirtualNetwork forLocationsDB 帳戶。</span><span class="sxs-lookup"><span data-stu-id="09fed-113">Updated DefaultConsistencyLevel to "Strong", Enabled AutomaticFailover, Enabled MultipleWriteLocations and Enabled VirtualNetwork for CosmosDB Account with name accountName.</span></span> 

## <span data-ttu-id="09fed-114">參數</span><span class="sxs-lookup"><span data-stu-id="09fed-114">PARAMETERS</span></span>

### <span data-ttu-id="09fed-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="09fed-115">-AsJob</span></span>
<span data-ttu-id="09fed-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="09fed-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="09fed-117">-BackupIntervalInMinutes</span><span class="sxs-lookup"><span data-stu-id="09fed-117">-BackupIntervalInMinutes</span></span>
<span data-ttu-id="09fed-118">備份 (分鐘) ，備份 (定期模式備份的帳戶) </span><span class="sxs-lookup"><span data-stu-id="09fed-118">The interval(in minutes) with which backup are taken (only for accounts with periodic mode backups)</span></span>

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

### <span data-ttu-id="09fed-119">-BackupRetentionIntervalInHours</span><span class="sxs-lookup"><span data-stu-id="09fed-119">-BackupRetentionIntervalInHours</span></span>
<span data-ttu-id="09fed-120">每個 (備份) 保留的時間 (定期模式備份帳戶) </span><span class="sxs-lookup"><span data-stu-id="09fed-120">The time(in hours) for which each backup is retained (only for accounts with periodic mode backups)</span></span>

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

### <span data-ttu-id="09fed-121">-確認</span><span class="sxs-lookup"><span data-stu-id="09fed-121">-Confirm</span></span>
<span data-ttu-id="09fed-122">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="09fed-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09fed-123">-DefaultLevel</span><span class="sxs-lookup"><span data-stu-id="09fed-123">-DefaultConsistencyLevel</span></span>
<span data-ttu-id="09fed-124">系統資料庫帳戶的預設一致性層級。</span><span class="sxs-lookup"><span data-stu-id="09fed-124">Default consistency level of the Cosmos DB database account.</span></span>
<span data-ttu-id="09fed-125">接受的值：BoundedStaleness， ConsistentPrefix， 解決， 會話， Strong</span><span class="sxs-lookup"><span data-stu-id="09fed-125">Accepted values: BoundedStaleness, ConsistentPrefix, Eventual, Session, Strong</span></span>

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

### <span data-ttu-id="09fed-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09fed-126">-DefaultProfile</span></span>
<span data-ttu-id="09fed-127">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="09fed-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="09fed-128">-DisableKeyBasedMetadataWriteAccess</span><span class="sxs-lookup"><span data-stu-id="09fed-128">-DisableKeyBasedMetadataWriteAccess</span></span>
<span data-ttu-id="09fed-129">停用透過帳戶金鑰 (資料庫、容器、輸送量) 中繼資料資源的寫入作業</span><span class="sxs-lookup"><span data-stu-id="09fed-129">Disable write operations on metadata resources (databases, containers, throughput) via account keys</span></span>

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

### <span data-ttu-id="09fed-130">-EnableAnalyticalStorage</span><span class="sxs-lookup"><span data-stu-id="09fed-130">-EnableAnalyticalStorage</span></span>
<span data-ttu-id="09fed-131">布林值，指出該帳戶上是否已啟用分析器功能。</span><span class="sxs-lookup"><span data-stu-id="09fed-131">Bool to indicate if AnalyticalStorage is enabled on the account.</span></span>

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

### <span data-ttu-id="09fed-132">-EnableAutomaticFailover</span><span class="sxs-lookup"><span data-stu-id="09fed-132">-EnableAutomaticFailover</span></span>
<span data-ttu-id="09fed-133">在因中斷而無法使用的少數情況下，啟用寫入地區的自動容錯移轉。</span><span class="sxs-lookup"><span data-stu-id="09fed-133">Enables automatic failover of the write region in the rare event that the region is unavailable due to an outage.</span></span>
<span data-ttu-id="09fed-134">自動容錯移轉會導致帳戶產生新的寫入區域，並且會根據針對帳戶所配置的容錯移轉優先順序來選擇。</span><span class="sxs-lookup"><span data-stu-id="09fed-134">Automatic failover will result in a new write region for the account and is chosen based on the failover priorities configured for the account.</span></span>
<span data-ttu-id="09fed-135">接受的值：False、true</span><span class="sxs-lookup"><span data-stu-id="09fed-135">Accepted values: false, true</span></span>

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

### <span data-ttu-id="09fed-136">-EnableMultipleWriteLocations</span><span class="sxs-lookup"><span data-stu-id="09fed-136">-EnableMultipleWriteLocations</span></span>
<span data-ttu-id="09fed-137">啟用多個寫入位置。</span><span class="sxs-lookup"><span data-stu-id="09fed-137">Enable Multiple Write Locations.</span></span>
<span data-ttu-id="09fed-138">接受的值：False、true</span><span class="sxs-lookup"><span data-stu-id="09fed-138">Accepted values: false, true</span></span>

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

### <span data-ttu-id="09fed-139">-EnableVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="09fed-139">-EnableVirtualNetwork</span></span>
<span data-ttu-id="09fed-140">啟用一個位於管理中心 DB 資料庫帳戶的虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="09fed-140">Enables virtual network on the Cosmos DB database account.</span></span>
<span data-ttu-id="09fed-141">接受的值：False、true</span><span class="sxs-lookup"><span data-stu-id="09fed-141">Accepted values: false, true</span></span>

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

### <span data-ttu-id="09fed-142">-InputObject</span><span class="sxs-lookup"><span data-stu-id="09fed-142">-InputObject</span></span>
<span data-ttu-id="09fed-143">因此，系統管理資料庫帳戶物件</span><span class="sxs-lookup"><span data-stu-id="09fed-143">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="09fed-144">-IpRule</span><span class="sxs-lookup"><span data-stu-id="09fed-144">-IpRule</span></span>
<span data-ttu-id="09fed-145">防火牆支援。</span><span class="sxs-lookup"><span data-stu-id="09fed-145">Firewall support.</span></span> <span data-ttu-id="09fed-146">指定 CIDR 表單中的一組 IP 位址或 IP 位址範圍，以做為指定資料庫帳戶的允許用戶端 IP 清單。</span><span class="sxs-lookup"><span data-stu-id="09fed-146">Specifies the set of IP addresses or IP address ranges in CIDR form to be included as the allowed list of client IPs for a given database account.</span></span>

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

### <span data-ttu-id="09fed-147">-KeyVaultKeyUri</span><span class="sxs-lookup"><span data-stu-id="09fed-147">-KeyVaultKeyUri</span></span>
<span data-ttu-id="09fed-148">KeyVault 的 URI</span><span class="sxs-lookup"><span data-stu-id="09fed-148">URI of the KeyVault</span></span>

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

### <span data-ttu-id="09fed-149">-MaxStalenessIntervalIn以秒為單位</span><span class="sxs-lookup"><span data-stu-id="09fed-149">-MaxStalenessIntervalInSeconds</span></span>
<span data-ttu-id="09fed-150">當使用與限制的過時一致性時，此值代表在時間範圍中 (過期) 的時間量。</span><span class="sxs-lookup"><span data-stu-id="09fed-150">When used with Bounded Staleness consistency, this value represents the time amount of staleness (in timespan) tolerated.</span></span>
<span data-ttu-id="09fed-151">此值的接受範圍為 5-86400。</span><span class="sxs-lookup"><span data-stu-id="09fed-151">Accepted range for this value is 5-86400.</span></span>

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

### <span data-ttu-id="09fed-152">-MaxStalenessPrefix</span><span class="sxs-lookup"><span data-stu-id="09fed-152">-MaxStalenessPrefix</span></span>
<span data-ttu-id="09fed-153">當使用與限制的過期一致性時，此值代表要過期要求的數量。</span><span class="sxs-lookup"><span data-stu-id="09fed-153">When used with Bounded Staleness consistency, this value represents the number of stale requests tolerated.</span></span>
<span data-ttu-id="09fed-154">此值的接受範圍為 1 - 2，147，483，647。</span><span class="sxs-lookup"><span data-stu-id="09fed-154">Accepted range for this value is 1 - 2,147,483,647.</span></span>

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

### <span data-ttu-id="09fed-155">-名稱</span><span class="sxs-lookup"><span data-stu-id="09fed-155">-Name</span></span>
<span data-ttu-id="09fed-156">系統 DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="09fed-156">Name of the Cosmos DB database account.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09fed-157">-NetworkAclBypass</span><span class="sxs-lookup"><span data-stu-id="09fed-157">-NetworkAclBypass</span></span>
<span data-ttu-id="09fed-158">此帳戶的 Synapse 連結是否已啟用網路 Acl 旁路。</span><span class="sxs-lookup"><span data-stu-id="09fed-158">Whether or not Network Acl Bypass is enabled for this account for Synapse Link.</span></span> <span data-ttu-id="09fed-159">可能的值包括：「無」、」AzureServices」。</span><span class="sxs-lookup"><span data-stu-id="09fed-159">Possible values include: 'None', 'AzureServices'.</span></span>

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

### <span data-ttu-id="09fed-160">-NetworkAclBypassResourceId</span><span class="sxs-lookup"><span data-stu-id="09fed-160">-NetworkAclBypassResourceId</span></span>
<span data-ttu-id="09fed-161">資源識別碼清單，以允許 Synapse 連結的網路 Acl 旁路。</span><span class="sxs-lookup"><span data-stu-id="09fed-161">List of Resource Ids to allow Network Acl Bypass for Synapse Link.</span></span>

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

### <span data-ttu-id="09fed-162">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="09fed-162">-PublicNetworkAccess</span></span>
<span data-ttu-id="09fed-163">此伺服器是否允許公用端點存取。</span><span class="sxs-lookup"><span data-stu-id="09fed-163">Whether or not public endpoint access is allowed for this server.</span></span> <span data-ttu-id="09fed-164">可能的值包括：'Enabled'， 'Disabled'</span><span class="sxs-lookup"><span data-stu-id="09fed-164">Possible values include: 'Enabled', 'Disabled'</span></span>

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

### <span data-ttu-id="09fed-165">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09fed-165">-ResourceGroupName</span></span>
<span data-ttu-id="09fed-166">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="09fed-166">Name of resource group.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09fed-167">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="09fed-167">-ResourceId</span></span>
<span data-ttu-id="09fed-168">資源的 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="09fed-168">ResourceId of the resource.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09fed-169">-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="09fed-169">-ServerVersion</span></span>
<span data-ttu-id="09fed-170">ServerVersion，僅適用于 MongoDB 帳戶。</span><span class="sxs-lookup"><span data-stu-id="09fed-170">ServerVersion, valid only in case of MongoDB Accounts.</span></span>

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

### <span data-ttu-id="09fed-171">-標記</span><span class="sxs-lookup"><span data-stu-id="09fed-171">-Tag</span></span>
<span data-ttu-id="09fed-172">將標記做為索引鍵值組合的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="09fed-172">Hashtable of tags as key-value pairs.</span></span>
<span data-ttu-id="09fed-173">使用空白字串來清除現有的標記。</span><span class="sxs-lookup"><span data-stu-id="09fed-173">Use empty string to clear existing tag.</span></span>

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

### <span data-ttu-id="09fed-174">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="09fed-174">-VirtualNetworkRule</span></span>
<span data-ttu-id="09fed-175">ACL 的虛擬網路字串值陣列。</span><span class="sxs-lookup"><span data-stu-id="09fed-175">Array of string values of ACL's for virtual network.</span></span>

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

### <span data-ttu-id="09fed-176">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="09fed-176">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="09fed-177">適用于虛擬網路的 PSVirtualNetworkRuleObjects 陣列。</span><span class="sxs-lookup"><span data-stu-id="09fed-177">Array of PSVirtualNetworkRuleObjects for virtual network.</span></span>

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

### <span data-ttu-id="09fed-178">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09fed-178">-WhatIf</span></span>
<span data-ttu-id="09fed-179">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="09fed-179">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="09fed-180">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="09fed-180">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09fed-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09fed-181">CommonParameters</span></span>
<span data-ttu-id="09fed-182">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="09fed-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09fed-183">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="09fed-183">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09fed-184">輸入</span><span class="sxs-lookup"><span data-stu-id="09fed-184">INPUTS</span></span>

### <span data-ttu-id="09fed-185">Microsoft.Azure.Commands.AzsDB.models.PSCorsRule[]</span><span class="sxs-lookup"><span data-stu-id="09fed-185">Microsoft.Azure.Commands.CosmosDB.Models.PSCorsRule[]</span></span>

## <span data-ttu-id="09fed-186">輸出</span><span class="sxs-lookup"><span data-stu-id="09fed-186">OUTPUTS</span></span>

### <span data-ttu-id="09fed-187">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="09fed-187">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="09fed-188">筆記</span><span class="sxs-lookup"><span data-stu-id="09fed-188">NOTES</span></span>

## <span data-ttu-id="09fed-189">相關連結</span><span class="sxs-lookup"><span data-stu-id="09fed-189">RELATED LINKS</span></span>
