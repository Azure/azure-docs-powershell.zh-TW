---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/new-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoCluster.md
ms.openlocfilehash: c8378e9be3c92cc799eb92b9ff913be98116b019
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903821"
---
# <span data-ttu-id="adfe9-101">New-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="adfe9-101">New-AzKustoCluster</span></span>

## <span data-ttu-id="adfe9-102">簡介</span><span class="sxs-lookup"><span data-stu-id="adfe9-102">SYNOPSIS</span></span>
<span data-ttu-id="adfe9-103">建立或更新 Kusto 集區。</span><span class="sxs-lookup"><span data-stu-id="adfe9-103">Create or update a Kusto cluster.</span></span>

## <span data-ttu-id="adfe9-104">語法</span><span class="sxs-lookup"><span data-stu-id="adfe9-104">SYNTAX</span></span>

```
New-AzKustoCluster -Name <String> -ResourceGroupName <String> -Location <String> -SkuName <AzureSkuName>
 -SkuTier <AzureSkuTier> [-SubscriptionId <String>] [-EnableDiskEncryption] [-EnableDoubleEncryption]
 [-EnablePurge] [-EnableStreamingIngest] [-EngineType <EngineType>] [-IdentityType <IdentityType>]
 [-IdentityUserAssignedIdentity <Hashtable>] [-KeyVaultPropertyKeyName <String>]
 [-KeyVaultPropertyKeyVaultUri <String>] [-KeyVaultPropertyKeyVersion <String>]
 [-KeyVaultPropertyUserIdentity <String>] [-LanguageExtensionValue <ILanguageExtension[]>]
 [-OptimizedAutoscaleIsEnabled] [-OptimizedAutoscaleMaximum <Int32>] [-OptimizedAutoscaleMinimum <Int32>]
 [-OptimizedAutoscaleVersion <Int32>] [-SkuCapacity <Int32>] [-Tag <Hashtable>]
 [-TrustedExternalTenant <ITrustedExternalTenant[]>]
 [-VirtualNetworkConfigurationDataManagementPublicIPId <String>]
 [-VirtualNetworkConfigurationEnginePublicIPId <String>] [-VirtualNetworkConfigurationSubnetId <String>]
 [-Zone <String[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="adfe9-105">描述</span><span class="sxs-lookup"><span data-stu-id="adfe9-105">DESCRIPTION</span></span>
<span data-ttu-id="adfe9-106">建立或更新 Kusto 集區。</span><span class="sxs-lookup"><span data-stu-id="adfe9-106">Create or update a Kusto cluster.</span></span>

## <span data-ttu-id="adfe9-107">例子</span><span class="sxs-lookup"><span data-stu-id="adfe9-107">EXAMPLES</span></span>

### <span data-ttu-id="adfe9-108">範例 1：建立新 Kusto cluster</span><span class="sxs-lookup"><span data-stu-id="adfe9-108">Example 1: Create a new Kusto cluster</span></span>
```powershell
PS C:\> New-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster -Location 'East US' -SkuName Standard_D11_v2 -SkuTier Standard -EnableDoubleEncryption true -EngineType 'V2'

Location Name                Type                     Zone
-------- ----                ----                     ----
East US  testnewkustocluster Microsoft.Kusto/Clusters
```

<span data-ttu-id="adfe9-109">上述命令在資源群組"testrg"中，會建立名為"testnewkustocluster"的新 Kusto 叢集。</span><span class="sxs-lookup"><span data-stu-id="adfe9-109">The above command creates a new Kusto cluster named "testnewkustocluster" in the resource group "testrg".</span></span>

## <span data-ttu-id="adfe9-110">參數</span><span class="sxs-lookup"><span data-stu-id="adfe9-110">PARAMETERS</span></span>

### <span data-ttu-id="adfe9-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="adfe9-111">-AsJob</span></span>
<span data-ttu-id="adfe9-112">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="adfe9-112">Run the command as a job</span></span>

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

### <span data-ttu-id="adfe9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="adfe9-113">-DefaultProfile</span></span>
<span data-ttu-id="adfe9-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="adfe9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="adfe9-115">-EnableCryptEncryption</span><span class="sxs-lookup"><span data-stu-id="adfe9-115">-EnableDiskEncryption</span></span>
<span data-ttu-id="adfe9-116">這是一個布林值，指出該組群的磁片是否經過加密。</span><span class="sxs-lookup"><span data-stu-id="adfe9-116">A boolean value that indicates if the cluster's disks are encrypted.</span></span>

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

### <span data-ttu-id="adfe9-117">-EnableDoubleEncryption</span><span class="sxs-lookup"><span data-stu-id="adfe9-117">-EnableDoubleEncryption</span></span>
<span data-ttu-id="adfe9-118">這是一個布林值，指出是否已啟用雙加密。</span><span class="sxs-lookup"><span data-stu-id="adfe9-118">A boolean value that indicates if double encryption is enabled.</span></span>

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

### <span data-ttu-id="adfe9-119">-EnablePurge</span><span class="sxs-lookup"><span data-stu-id="adfe9-119">-EnablePurge</span></span>
<span data-ttu-id="adfe9-120">這是一個布林值，指出是否已啟用清除作業。</span><span class="sxs-lookup"><span data-stu-id="adfe9-120">A boolean value that indicates if the purge operations are enabled.</span></span>

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

### <span data-ttu-id="adfe9-121">-EnableStreamingIngest</span><span class="sxs-lookup"><span data-stu-id="adfe9-121">-EnableStreamingIngest</span></span>
<span data-ttu-id="adfe9-122">這是一個布林值，指出是否已啟用串流處理。</span><span class="sxs-lookup"><span data-stu-id="adfe9-122">A boolean value that indicates if the streaming ingest is enabled.</span></span>

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

### <span data-ttu-id="adfe9-123">-EngineType</span><span class="sxs-lookup"><span data-stu-id="adfe9-123">-EngineType</span></span>
<span data-ttu-id="adfe9-124">引擎類型</span><span class="sxs-lookup"><span data-stu-id="adfe9-124">The engine type</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.EngineType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adfe9-125">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="adfe9-125">-IdentityType</span></span>
<span data-ttu-id="adfe9-126">使用的受管理身分識別類型。</span><span class="sxs-lookup"><span data-stu-id="adfe9-126">The type of managed identity used.</span></span>
<span data-ttu-id="adfe9-127">'SystemAssigned， UserAssigned' 類型包含隱含建立身分識別，以及一組使用者指派的身分識別。</span><span class="sxs-lookup"><span data-stu-id="adfe9-127">The type 'SystemAssigned, UserAssigned' includes both an implicitly created identity and a set of user-assigned identities.</span></span>
<span data-ttu-id="adfe9-128">類型為 "None" 會移除所有身分。</span><span class="sxs-lookup"><span data-stu-id="adfe9-128">The type 'None' will remove all identities.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.IdentityType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adfe9-129">-IdentityUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="adfe9-129">-IdentityUserAssignedIdentity</span></span>
<span data-ttu-id="adfe9-130">與 Kusto 組群相關聯的使用者身分清單。</span><span class="sxs-lookup"><span data-stu-id="adfe9-130">The list of user identities associated with the Kusto cluster.</span></span>
<span data-ttu-id="adfe9-131">使用者身分識別字典的金鑰參照為表單中的 ARM 資源識別碼：'/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'。</span><span class="sxs-lookup"><span data-stu-id="adfe9-131">The user identity dictionary key references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span></span>

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

### <span data-ttu-id="adfe9-132">-KeyVaultPropertyKeyName</span><span class="sxs-lookup"><span data-stu-id="adfe9-132">-KeyVaultPropertyKeyName</span></span>
<span data-ttu-id="adfe9-133">金鑰庫金鑰的名稱。</span><span class="sxs-lookup"><span data-stu-id="adfe9-133">The name of the key vault key.</span></span>

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

### <span data-ttu-id="adfe9-134">-KeyVaultPropertyKeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="adfe9-134">-KeyVaultPropertyKeyVaultUri</span></span>
<span data-ttu-id="adfe9-135">金鑰庫的 Uri。</span><span class="sxs-lookup"><span data-stu-id="adfe9-135">The Uri of the key vault.</span></span>

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

### <span data-ttu-id="adfe9-136">-KeyVaultPropertyKeyVersion</span><span class="sxs-lookup"><span data-stu-id="adfe9-136">-KeyVaultPropertyKeyVersion</span></span>
<span data-ttu-id="adfe9-137">金鑰庫金鑰的版本。</span><span class="sxs-lookup"><span data-stu-id="adfe9-137">The version of the key vault key.</span></span>

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

### <span data-ttu-id="adfe9-138">-KeyVaultPropertyUserIdentity</span><span class="sxs-lookup"><span data-stu-id="adfe9-138">-KeyVaultPropertyUserIdentity</span></span>
<span data-ttu-id="adfe9-139">使用者指派的身分識別 (ARM 資源識別碼) 具有該金鑰存取權。</span><span class="sxs-lookup"><span data-stu-id="adfe9-139">The user assigned identity (ARM resource id) that has access to the key.</span></span>

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

### <span data-ttu-id="adfe9-140">-LanguageExtensionValue</span><span class="sxs-lookup"><span data-stu-id="adfe9-140">-LanguageExtensionValue</span></span>
<span data-ttu-id="adfe9-141">語言延伸模組清單。</span><span class="sxs-lookup"><span data-stu-id="adfe9-141">The list of language extensions.</span></span>
<span data-ttu-id="adfe9-142">若要建構，請參閱 LANGUAGEEXTENSIONVALUE 屬性的 NOTES 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="adfe9-142">To construct, see NOTES section for LANGUAGEEXTENSIONVALUE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ILanguageExtension[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adfe9-143">-位置</span><span class="sxs-lookup"><span data-stu-id="adfe9-143">-Location</span></span>
<span data-ttu-id="adfe9-144">資源所在地的地理位置</span><span class="sxs-lookup"><span data-stu-id="adfe9-144">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="adfe9-145">-名稱</span><span class="sxs-lookup"><span data-stu-id="adfe9-145">-Name</span></span>
<span data-ttu-id="adfe9-146">Kusto 組名。</span><span class="sxs-lookup"><span data-stu-id="adfe9-146">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adfe9-147">-NoWait</span><span class="sxs-lookup"><span data-stu-id="adfe9-147">-NoWait</span></span>
<span data-ttu-id="adfe9-148">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="adfe9-148">Run the command asynchronously</span></span>

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

### <span data-ttu-id="adfe9-149">-OptimizedAutoscaleIsEnabled</span><span class="sxs-lookup"><span data-stu-id="adfe9-149">-OptimizedAutoscaleIsEnabled</span></span>
<span data-ttu-id="adfe9-150">布林值，指出優化的自動縮放功能是否已啟用。</span><span class="sxs-lookup"><span data-stu-id="adfe9-150">A boolean value that indicate if the optimized autoscale feature is enabled or not.</span></span>

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

### <span data-ttu-id="adfe9-151">-OptimizedAutoscaleMaximum</span><span class="sxs-lookup"><span data-stu-id="adfe9-151">-OptimizedAutoscaleMaximum</span></span>
<span data-ttu-id="adfe9-152">允許的實例計數上限。</span><span class="sxs-lookup"><span data-stu-id="adfe9-152">Maximum allowed instances count.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adfe9-153">-OptimizedAutoscaleMinimum</span><span class="sxs-lookup"><span data-stu-id="adfe9-153">-OptimizedAutoscaleMinimum</span></span>
<span data-ttu-id="adfe9-154">允許實例計數的最小值。</span><span class="sxs-lookup"><span data-stu-id="adfe9-154">Minimum allowed instances count.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adfe9-155">-OptimizedAutoscaleVersion</span><span class="sxs-lookup"><span data-stu-id="adfe9-155">-OptimizedAutoscaleVersion</span></span>
<span data-ttu-id="adfe9-156">已定義的範本版本，例如 1。</span><span class="sxs-lookup"><span data-stu-id="adfe9-156">The version of the template defined, for instance 1.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adfe9-157">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="adfe9-157">-ResourceGroupName</span></span>
<span data-ttu-id="adfe9-158">包含 Kusto 群組的資源組名。</span><span class="sxs-lookup"><span data-stu-id="adfe9-158">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="adfe9-159">-Sku以</span><span class="sxs-lookup"><span data-stu-id="adfe9-159">-SkuCapacity</span></span>
<span data-ttu-id="adfe9-160">這是該組群的實例數目。</span><span class="sxs-lookup"><span data-stu-id="adfe9-160">The number of instances of the cluster.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adfe9-161">-SKUName</span><span class="sxs-lookup"><span data-stu-id="adfe9-161">-SkuName</span></span>
<span data-ttu-id="adfe9-162">SKU 名稱。</span><span class="sxs-lookup"><span data-stu-id="adfe9-162">SKU name.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.AzureSkuName
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adfe9-163">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="adfe9-163">-SkuTier</span></span>
<span data-ttu-id="adfe9-164">SKU 層級。</span><span class="sxs-lookup"><span data-stu-id="adfe9-164">SKU tier.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.AzureSkuTier
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adfe9-165">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="adfe9-165">-SubscriptionId</span></span>
<span data-ttu-id="adfe9-166">獲得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="adfe9-166">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="adfe9-167">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="adfe9-167">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="adfe9-168">-標記</span><span class="sxs-lookup"><span data-stu-id="adfe9-168">-Tag</span></span>
<span data-ttu-id="adfe9-169">資源標記。</span><span class="sxs-lookup"><span data-stu-id="adfe9-169">Resource tags.</span></span>

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

### <span data-ttu-id="adfe9-170">-TrustedExternalTenant</span><span class="sxs-lookup"><span data-stu-id="adfe9-170">-TrustedExternalTenant</span></span>
<span data-ttu-id="adfe9-171">該群的外部租使用者。</span><span class="sxs-lookup"><span data-stu-id="adfe9-171">The cluster's external tenants.</span></span>
<span data-ttu-id="adfe9-172">若要建構，請參閱 TRUSTEDEXTERNALTENANT 屬性的 NOTES 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="adfe9-172">To construct, see NOTES section for TRUSTEDEXTERNALTENANT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ITrustedExternalTenant[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adfe9-173">-VirtualNetworkConfigurationDataManagementPublicIPId</span><span class="sxs-lookup"><span data-stu-id="adfe9-173">-VirtualNetworkConfigurationDataManagementPublicIPId</span></span>
<span data-ttu-id="adfe9-174">資料管理的服務公用 IP 位址資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="adfe9-174">Data management's service public IP address resource id.</span></span>

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

### <span data-ttu-id="adfe9-175">-VirtualNetworkConfigurationEnginePublicIPId</span><span class="sxs-lookup"><span data-stu-id="adfe9-175">-VirtualNetworkConfigurationEnginePublicIPId</span></span>
<span data-ttu-id="adfe9-176">引擎服務的公用 IP 位址資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="adfe9-176">Engine service's public IP address resource id.</span></span>

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

### <span data-ttu-id="adfe9-177">-VirtualNetworkConfigurationSubnetId</span><span class="sxs-lookup"><span data-stu-id="adfe9-177">-VirtualNetworkConfigurationSubnetId</span></span>
<span data-ttu-id="adfe9-178">子網資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="adfe9-178">The subnet resource id.</span></span>

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

### <span data-ttu-id="adfe9-179">-區域</span><span class="sxs-lookup"><span data-stu-id="adfe9-179">-Zone</span></span>
<span data-ttu-id="adfe9-180">該組的可用性區域。</span><span class="sxs-lookup"><span data-stu-id="adfe9-180">The availability zones of the cluster.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adfe9-181">-確認</span><span class="sxs-lookup"><span data-stu-id="adfe9-181">-Confirm</span></span>
<span data-ttu-id="adfe9-182">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="adfe9-182">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="adfe9-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="adfe9-183">-WhatIf</span></span>
<span data-ttu-id="adfe9-184">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="adfe9-184">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="adfe9-185">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="adfe9-185">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="adfe9-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adfe9-186">CommonParameters</span></span>
<span data-ttu-id="adfe9-187">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="adfe9-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adfe9-188">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="adfe9-188">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adfe9-189">輸入</span><span class="sxs-lookup"><span data-stu-id="adfe9-189">INPUTS</span></span>

## <span data-ttu-id="adfe9-190">輸出</span><span class="sxs-lookup"><span data-stu-id="adfe9-190">OUTPUTS</span></span>

### <span data-ttu-id="adfe9-191">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICluster</span><span class="sxs-lookup"><span data-stu-id="adfe9-191">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICluster</span></span>

## <span data-ttu-id="adfe9-192">筆記</span><span class="sxs-lookup"><span data-stu-id="adfe9-192">NOTES</span></span>

<span data-ttu-id="adfe9-193">別名</span><span class="sxs-lookup"><span data-stu-id="adfe9-193">ALIASES</span></span>

<span data-ttu-id="adfe9-194">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="adfe9-194">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="adfe9-195">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="adfe9-195">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="adfe9-196">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="adfe9-196">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="adfe9-197">LANGUAGEEXTENSIONVALUE <ILanguageExtension[]>：語言擴充功能清單。</span><span class="sxs-lookup"><span data-stu-id="adfe9-197">LANGUAGEEXTENSIONVALUE <ILanguageExtension[]>: The list of language extensions.</span></span>
  - <span data-ttu-id="adfe9-198">`[Name <LanguageExtensionName?>]`：語言副檔名。</span><span class="sxs-lookup"><span data-stu-id="adfe9-198">`[Name <LanguageExtensionName?>]`: The language extension name.</span></span>

<span data-ttu-id="adfe9-199">TrustEDEXTERNALTENANT <ITrustedExternalTenant[]>：該群的外部租使用者。</span><span class="sxs-lookup"><span data-stu-id="adfe9-199">TRUSTEDEXTERNALTENANT <ITrustedExternalTenant[]>: The cluster's external tenants.</span></span>
  - <span data-ttu-id="adfe9-200">`[Value <String>]`：代表外部租使用者 GUID。</span><span class="sxs-lookup"><span data-stu-id="adfe9-200">`[Value <String>]`: GUID representing an external tenant.</span></span>

## <span data-ttu-id="adfe9-201">相關連結</span><span class="sxs-lookup"><span data-stu-id="adfe9-201">RELATED LINKS</span></span>

