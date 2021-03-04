---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/update-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoCluster.md
ms.openlocfilehash: 21a2869a7a8006fdc0a570ebf4176f28c3a44efc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909018"
---
# <span data-ttu-id="87eaf-101">Update-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="87eaf-101">Update-AzKustoCluster</span></span>

## <span data-ttu-id="87eaf-102">簡介</span><span class="sxs-lookup"><span data-stu-id="87eaf-102">SYNOPSIS</span></span>
<span data-ttu-id="87eaf-103">更新 Kusto 集區。</span><span class="sxs-lookup"><span data-stu-id="87eaf-103">Update a Kusto cluster.</span></span>

## <span data-ttu-id="87eaf-104">語法</span><span class="sxs-lookup"><span data-stu-id="87eaf-104">SYNTAX</span></span>

### <span data-ttu-id="87eaf-105">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="87eaf-105">UpdateExpanded (Default)</span></span>
```
Update-AzKustoCluster -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-EnableDiskEncryption] [-EnableDoubleEncryption] [-EnablePurge] [-EnableStreamingIngest]
 [-EngineType <EngineType>] [-IdentityType <IdentityType>] [-IdentityUserAssignedIdentity <Hashtable>]
 [-KeyVaultPropertyKeyName <String>] [-KeyVaultPropertyKeyVaultUri <String>]
 [-KeyVaultPropertyKeyVersion <String>] [-KeyVaultPropertyUserIdentity <String>]
 [-LanguageExtensionValue <ILanguageExtension[]>] [-Location <String>] [-OptimizedAutoscaleIsEnabled]
 [-OptimizedAutoscaleMaximum <Int32>] [-OptimizedAutoscaleMinimum <Int32>]
 [-OptimizedAutoscaleVersion <Int32>] [-SkuCapacity <Int32>] [-SkuName <AzureSkuName>]
 [-SkuTier <AzureSkuTier>] [-Tag <Hashtable>] [-TrustedExternalTenant <ITrustedExternalTenant[]>]
 [-VirtualNetworkConfigurationDataManagementPublicIPId <String>]
 [-VirtualNetworkConfigurationEnginePublicIPId <String>] [-VirtualNetworkConfigurationSubnetId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="87eaf-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="87eaf-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzKustoCluster -InputObject <IKustoIdentity> [-EnableDiskEncryption] [-EnableDoubleEncryption]
 [-EnablePurge] [-EnableStreamingIngest] [-EngineType <EngineType>] [-IdentityType <IdentityType>]
 [-IdentityUserAssignedIdentity <Hashtable>] [-KeyVaultPropertyKeyName <String>]
 [-KeyVaultPropertyKeyVaultUri <String>] [-KeyVaultPropertyKeyVersion <String>]
 [-KeyVaultPropertyUserIdentity <String>] [-LanguageExtensionValue <ILanguageExtension[]>]
 [-Location <String>] [-OptimizedAutoscaleIsEnabled] [-OptimizedAutoscaleMaximum <Int32>]
 [-OptimizedAutoscaleMinimum <Int32>] [-OptimizedAutoscaleVersion <Int32>] [-SkuCapacity <Int32>]
 [-SkuName <AzureSkuName>] [-SkuTier <AzureSkuTier>] [-Tag <Hashtable>]
 [-TrustedExternalTenant <ITrustedExternalTenant[]>]
 [-VirtualNetworkConfigurationDataManagementPublicIPId <String>]
 [-VirtualNetworkConfigurationEnginePublicIPId <String>] [-VirtualNetworkConfigurationSubnetId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="87eaf-107">描述</span><span class="sxs-lookup"><span data-stu-id="87eaf-107">DESCRIPTION</span></span>
<span data-ttu-id="87eaf-108">更新 Kusto 集區。</span><span class="sxs-lookup"><span data-stu-id="87eaf-108">Update a Kusto cluster.</span></span>

## <span data-ttu-id="87eaf-109">例子</span><span class="sxs-lookup"><span data-stu-id="87eaf-109">EXAMPLES</span></span>

### <span data-ttu-id="87eaf-110">範例 1：更新現有組名</span><span class="sxs-lookup"><span data-stu-id="87eaf-110">Example 1: Update an existing cluster by name</span></span>
```powershell
PS C:\> Update-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster -SkuName Standard_D12_v2 -SkuTier Standard -EngineType 'V2'

Location Name                Type                     Zone
-------- ----                ----                     ----
East US  testnewkustocluster Microsoft.Kusto/Clusters
```

<span data-ttu-id="87eaf-111">上述命令會更新在資源群組 "testrg" 中找到的 Kusto 叢集 「testnewkustocluster」SKU。</span><span class="sxs-lookup"><span data-stu-id="87eaf-111">The above command updates the sku of the Kusto cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="87eaf-112">範例 2：更新現有組名</span><span class="sxs-lookup"><span data-stu-id="87eaf-112">Example 2: Update an existing cluster by name</span></span>
```powershell
PS C:\> Update-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster -KeyVaultPropertyKeyName "TestKey" -KeyVaultPropertyKeyVaultUri "https://testpskeyvault.vault.azure.net" -KeyVaultPropertyKeyVersion "4bd66f0e0d7c403fac80305e0355d982"

Location Name                Type                     Zone
-------- ----                ----                     ----
East US  testnewkustocluster Microsoft.Kusto/Clusters
```

<span data-ttu-id="87eaf-113">上述命令會使用客戶管理的金鑰更新資源群組 "testrg" 中找到的叢集「testnewkustocluster」。</span><span class="sxs-lookup"><span data-stu-id="87eaf-113">The above command updates the cluster "testnewkustocluster" found in the resource group "testrg" with a customer managed key.</span></span>

## <span data-ttu-id="87eaf-114">參數</span><span class="sxs-lookup"><span data-stu-id="87eaf-114">PARAMETERS</span></span>

### <span data-ttu-id="87eaf-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="87eaf-115">-AsJob</span></span>
<span data-ttu-id="87eaf-116">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="87eaf-116">Run the command as a job</span></span>

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

### <span data-ttu-id="87eaf-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87eaf-117">-DefaultProfile</span></span>
<span data-ttu-id="87eaf-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="87eaf-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="87eaf-119">-EnableCryptEncryption</span><span class="sxs-lookup"><span data-stu-id="87eaf-119">-EnableDiskEncryption</span></span>
<span data-ttu-id="87eaf-120">這是一個布林值，指出該組群的磁片是否經過加密。</span><span class="sxs-lookup"><span data-stu-id="87eaf-120">A boolean value that indicates if the cluster's disks are encrypted.</span></span>

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

### <span data-ttu-id="87eaf-121">-EnableDoubleEncryption</span><span class="sxs-lookup"><span data-stu-id="87eaf-121">-EnableDoubleEncryption</span></span>
<span data-ttu-id="87eaf-122">這是一個布林值，指出是否已啟用雙加密。</span><span class="sxs-lookup"><span data-stu-id="87eaf-122">A boolean value that indicates if double encryption is enabled.</span></span>

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

### <span data-ttu-id="87eaf-123">-EnablePurge</span><span class="sxs-lookup"><span data-stu-id="87eaf-123">-EnablePurge</span></span>
<span data-ttu-id="87eaf-124">這是一個布林值，指出是否已啟用清除作業。</span><span class="sxs-lookup"><span data-stu-id="87eaf-124">A boolean value that indicates if the purge operations are enabled.</span></span>

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

### <span data-ttu-id="87eaf-125">-EnableStreamingIngest</span><span class="sxs-lookup"><span data-stu-id="87eaf-125">-EnableStreamingIngest</span></span>
<span data-ttu-id="87eaf-126">這是一個布林值，指出是否已啟用串流處理。</span><span class="sxs-lookup"><span data-stu-id="87eaf-126">A boolean value that indicates if the streaming ingest is enabled.</span></span>

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

### <span data-ttu-id="87eaf-127">-EngineType</span><span class="sxs-lookup"><span data-stu-id="87eaf-127">-EngineType</span></span>
<span data-ttu-id="87eaf-128">引擎類型</span><span class="sxs-lookup"><span data-stu-id="87eaf-128">The engine type</span></span>

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

### <span data-ttu-id="87eaf-129">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="87eaf-129">-IdentityType</span></span>
<span data-ttu-id="87eaf-130">使用的受管理身分識別類型。</span><span class="sxs-lookup"><span data-stu-id="87eaf-130">The type of managed identity used.</span></span>
<span data-ttu-id="87eaf-131">'SystemAssigned， UserAssigned' 類型包含隱含建立身分識別，以及一組使用者指派的身分識別。</span><span class="sxs-lookup"><span data-stu-id="87eaf-131">The type 'SystemAssigned, UserAssigned' includes both an implicitly created identity and a set of user-assigned identities.</span></span>
<span data-ttu-id="87eaf-132">類型為 "None" 會移除所有身分。</span><span class="sxs-lookup"><span data-stu-id="87eaf-132">The type 'None' will remove all identities.</span></span>

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

### <span data-ttu-id="87eaf-133">-IdentityUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="87eaf-133">-IdentityUserAssignedIdentity</span></span>
<span data-ttu-id="87eaf-134">與 Kusto 組群相關聯的使用者身分清單。</span><span class="sxs-lookup"><span data-stu-id="87eaf-134">The list of user identities associated with the Kusto cluster.</span></span>
<span data-ttu-id="87eaf-135">使用者身分識別字典的金鑰參照為表單中的 ARM 資源識別碼：'/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'。</span><span class="sxs-lookup"><span data-stu-id="87eaf-135">The user identity dictionary key references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span></span>

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

### <span data-ttu-id="87eaf-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="87eaf-136">-InputObject</span></span>
<span data-ttu-id="87eaf-137">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="87eaf-137">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="87eaf-138">-KeyVaultPropertyKeyName</span><span class="sxs-lookup"><span data-stu-id="87eaf-138">-KeyVaultPropertyKeyName</span></span>
<span data-ttu-id="87eaf-139">金鑰庫金鑰的名稱。</span><span class="sxs-lookup"><span data-stu-id="87eaf-139">The name of the key vault key.</span></span>

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

### <span data-ttu-id="87eaf-140">-KeyVaultPropertyKeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="87eaf-140">-KeyVaultPropertyKeyVaultUri</span></span>
<span data-ttu-id="87eaf-141">金鑰庫的 Uri。</span><span class="sxs-lookup"><span data-stu-id="87eaf-141">The Uri of the key vault.</span></span>

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

### <span data-ttu-id="87eaf-142">-KeyVaultPropertyKeyVersion</span><span class="sxs-lookup"><span data-stu-id="87eaf-142">-KeyVaultPropertyKeyVersion</span></span>
<span data-ttu-id="87eaf-143">金鑰庫金鑰的版本。</span><span class="sxs-lookup"><span data-stu-id="87eaf-143">The version of the key vault key.</span></span>

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

### <span data-ttu-id="87eaf-144">-KeyVaultPropertyUserIdentity</span><span class="sxs-lookup"><span data-stu-id="87eaf-144">-KeyVaultPropertyUserIdentity</span></span>
<span data-ttu-id="87eaf-145">使用者指派的身分識別 (ARM 資源識別碼) 具有該金鑰存取權。</span><span class="sxs-lookup"><span data-stu-id="87eaf-145">The user assigned identity (ARM resource id) that has access to the key.</span></span>

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

### <span data-ttu-id="87eaf-146">-LanguageExtensionValue</span><span class="sxs-lookup"><span data-stu-id="87eaf-146">-LanguageExtensionValue</span></span>
<span data-ttu-id="87eaf-147">語言延伸模組清單。</span><span class="sxs-lookup"><span data-stu-id="87eaf-147">The list of language extensions.</span></span>
<span data-ttu-id="87eaf-148">若要建構，請參閱 LANGUAGEEXTENSIONVALUE 屬性的 NOTES 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="87eaf-148">To construct, see NOTES section for LANGUAGEEXTENSIONVALUE properties and create a hash table.</span></span>

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

### <span data-ttu-id="87eaf-149">-位置</span><span class="sxs-lookup"><span data-stu-id="87eaf-149">-Location</span></span>
<span data-ttu-id="87eaf-150">資源位置。</span><span class="sxs-lookup"><span data-stu-id="87eaf-150">Resource location.</span></span>

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

### <span data-ttu-id="87eaf-151">-名稱</span><span class="sxs-lookup"><span data-stu-id="87eaf-151">-Name</span></span>
<span data-ttu-id="87eaf-152">Kusto 組名。</span><span class="sxs-lookup"><span data-stu-id="87eaf-152">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87eaf-153">-NoWait</span><span class="sxs-lookup"><span data-stu-id="87eaf-153">-NoWait</span></span>
<span data-ttu-id="87eaf-154">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="87eaf-154">Run the command asynchronously</span></span>

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

### <span data-ttu-id="87eaf-155">-OptimizedAutoscaleIsEnabled</span><span class="sxs-lookup"><span data-stu-id="87eaf-155">-OptimizedAutoscaleIsEnabled</span></span>
<span data-ttu-id="87eaf-156">布林值，指出優化的自動縮放功能是否已啟用。</span><span class="sxs-lookup"><span data-stu-id="87eaf-156">A boolean value that indicate if the optimized autoscale feature is enabled or not.</span></span>

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

### <span data-ttu-id="87eaf-157">-OptimizedAutoscaleMaximum</span><span class="sxs-lookup"><span data-stu-id="87eaf-157">-OptimizedAutoscaleMaximum</span></span>
<span data-ttu-id="87eaf-158">允許的實例計數上限。</span><span class="sxs-lookup"><span data-stu-id="87eaf-158">Maximum allowed instances count.</span></span>

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

### <span data-ttu-id="87eaf-159">-OptimizedAutoscaleMinimum</span><span class="sxs-lookup"><span data-stu-id="87eaf-159">-OptimizedAutoscaleMinimum</span></span>
<span data-ttu-id="87eaf-160">允許實例計數的最小值。</span><span class="sxs-lookup"><span data-stu-id="87eaf-160">Minimum allowed instances count.</span></span>

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

### <span data-ttu-id="87eaf-161">-OptimizedAutoscaleVersion</span><span class="sxs-lookup"><span data-stu-id="87eaf-161">-OptimizedAutoscaleVersion</span></span>
<span data-ttu-id="87eaf-162">已定義的範本版本，例如 1。</span><span class="sxs-lookup"><span data-stu-id="87eaf-162">The version of the template defined, for instance 1.</span></span>

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

### <span data-ttu-id="87eaf-163">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87eaf-163">-ResourceGroupName</span></span>
<span data-ttu-id="87eaf-164">包含 Kusto 群組的資源組名。</span><span class="sxs-lookup"><span data-stu-id="87eaf-164">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87eaf-165">-Sku以</span><span class="sxs-lookup"><span data-stu-id="87eaf-165">-SkuCapacity</span></span>
<span data-ttu-id="87eaf-166">這是該組群的實例數目。</span><span class="sxs-lookup"><span data-stu-id="87eaf-166">The number of instances of the cluster.</span></span>

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

### <span data-ttu-id="87eaf-167">-SKUName</span><span class="sxs-lookup"><span data-stu-id="87eaf-167">-SkuName</span></span>
<span data-ttu-id="87eaf-168">SKU 名稱。</span><span class="sxs-lookup"><span data-stu-id="87eaf-168">SKU name.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.AzureSkuName
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87eaf-169">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="87eaf-169">-SkuTier</span></span>
<span data-ttu-id="87eaf-170">SKU 層級。</span><span class="sxs-lookup"><span data-stu-id="87eaf-170">SKU tier.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.AzureSkuTier
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87eaf-171">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="87eaf-171">-SubscriptionId</span></span>
<span data-ttu-id="87eaf-172">獲得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="87eaf-172">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="87eaf-173">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="87eaf-173">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87eaf-174">-標記</span><span class="sxs-lookup"><span data-stu-id="87eaf-174">-Tag</span></span>
<span data-ttu-id="87eaf-175">資源標記。</span><span class="sxs-lookup"><span data-stu-id="87eaf-175">Resource tags.</span></span>

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

### <span data-ttu-id="87eaf-176">-TrustedExternalTenant</span><span class="sxs-lookup"><span data-stu-id="87eaf-176">-TrustedExternalTenant</span></span>
<span data-ttu-id="87eaf-177">該群的外部租使用者。</span><span class="sxs-lookup"><span data-stu-id="87eaf-177">The cluster's external tenants.</span></span>
<span data-ttu-id="87eaf-178">若要建構，請參閱 TRUSTEDEXTERNALTENANT 屬性的 NOTES 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="87eaf-178">To construct, see NOTES section for TRUSTEDEXTERNALTENANT properties and create a hash table.</span></span>

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

### <span data-ttu-id="87eaf-179">-VirtualNetworkConfigurationDataManagementPublicIPId</span><span class="sxs-lookup"><span data-stu-id="87eaf-179">-VirtualNetworkConfigurationDataManagementPublicIPId</span></span>
<span data-ttu-id="87eaf-180">資料管理的服務公用 IP 位址資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="87eaf-180">Data management's service public IP address resource id.</span></span>

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

### <span data-ttu-id="87eaf-181">-VirtualNetworkConfigurationEnginePublicIPId</span><span class="sxs-lookup"><span data-stu-id="87eaf-181">-VirtualNetworkConfigurationEnginePublicIPId</span></span>
<span data-ttu-id="87eaf-182">引擎服務的公用 IP 位址資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="87eaf-182">Engine service's public IP address resource id.</span></span>

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

### <span data-ttu-id="87eaf-183">-VirtualNetworkConfigurationSubnetId</span><span class="sxs-lookup"><span data-stu-id="87eaf-183">-VirtualNetworkConfigurationSubnetId</span></span>
<span data-ttu-id="87eaf-184">子網資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="87eaf-184">The subnet resource id.</span></span>

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

### <span data-ttu-id="87eaf-185">-確認</span><span class="sxs-lookup"><span data-stu-id="87eaf-185">-Confirm</span></span>
<span data-ttu-id="87eaf-186">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="87eaf-186">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87eaf-187">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87eaf-187">-WhatIf</span></span>
<span data-ttu-id="87eaf-188">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="87eaf-188">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="87eaf-189">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="87eaf-189">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87eaf-190">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87eaf-190">CommonParameters</span></span>
<span data-ttu-id="87eaf-191">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="87eaf-191">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87eaf-192">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="87eaf-192">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87eaf-193">輸入</span><span class="sxs-lookup"><span data-stu-id="87eaf-193">INPUTS</span></span>

### <span data-ttu-id="87eaf-194">Microsoft.Azure.PowerShell.Cmdlets.Kusto.models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="87eaf-194">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="87eaf-195">輸出</span><span class="sxs-lookup"><span data-stu-id="87eaf-195">OUTPUTS</span></span>

### <span data-ttu-id="87eaf-196">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICluster</span><span class="sxs-lookup"><span data-stu-id="87eaf-196">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICluster</span></span>

## <span data-ttu-id="87eaf-197">筆記</span><span class="sxs-lookup"><span data-stu-id="87eaf-197">NOTES</span></span>

<span data-ttu-id="87eaf-198">別名</span><span class="sxs-lookup"><span data-stu-id="87eaf-198">ALIASES</span></span>

<span data-ttu-id="87eaf-199">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="87eaf-199">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="87eaf-200">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="87eaf-200">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="87eaf-201">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="87eaf-201">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="87eaf-202">INPUTOBJECT： <IKustoIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="87eaf-202">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="87eaf-203">`[AttachedDatabaseConfigurationName <String>]`：附加資料庫組配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="87eaf-203">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="87eaf-204">`[ClusterName <String>]`：Kusto 組名。</span><span class="sxs-lookup"><span data-stu-id="87eaf-204">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="87eaf-205">`[DataConnectionName <String>]`：資料連線的名稱。</span><span class="sxs-lookup"><span data-stu-id="87eaf-205">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="87eaf-206">`[DatabaseName <String>]`：Kusto cluster 中的資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="87eaf-206">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="87eaf-207">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="87eaf-207">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="87eaf-208">`[Location <String>]`：Azure 位置。</span><span class="sxs-lookup"><span data-stu-id="87eaf-208">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="87eaf-209">`[PrincipalAssignmentName <String>]`：Kusto principalAssignment 的名稱。</span><span class="sxs-lookup"><span data-stu-id="87eaf-209">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="87eaf-210">`[ResourceGroupName <String>]`：包含 Kusto 群組的資源組名。</span><span class="sxs-lookup"><span data-stu-id="87eaf-210">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="87eaf-211">`[SubscriptionId <String>]`：獲得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="87eaf-211">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="87eaf-212">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="87eaf-212">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="87eaf-213">LANGUAGEEXTENSIONVALUE <ILanguageExtension[]>：語言擴充功能清單。</span><span class="sxs-lookup"><span data-stu-id="87eaf-213">LANGUAGEEXTENSIONVALUE <ILanguageExtension[]>: The list of language extensions.</span></span>
  - <span data-ttu-id="87eaf-214">`[Name <LanguageExtensionName?>]`：語言副檔名。</span><span class="sxs-lookup"><span data-stu-id="87eaf-214">`[Name <LanguageExtensionName?>]`: The language extension name.</span></span>

<span data-ttu-id="87eaf-215">TrustEDEXTERNALTENANT <ITrustedExternalTenant[]>：該群的外部租使用者。</span><span class="sxs-lookup"><span data-stu-id="87eaf-215">TRUSTEDEXTERNALTENANT <ITrustedExternalTenant[]>: The cluster's external tenants.</span></span>
  - <span data-ttu-id="87eaf-216">`[Value <String>]`：代表外部租使用者 GUID。</span><span class="sxs-lookup"><span data-stu-id="87eaf-216">`[Value <String>]`: GUID representing an external tenant.</span></span>

## <span data-ttu-id="87eaf-217">相關連結</span><span class="sxs-lookup"><span data-stu-id="87eaf-217">RELATED LINKS</span></span>

