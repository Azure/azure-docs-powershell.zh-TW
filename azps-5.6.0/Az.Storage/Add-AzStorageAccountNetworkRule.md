---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/add-azstorageaccountnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzStorageAccountNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzStorageAccountNetworkRule.md
ms.openlocfilehash: 0104c64bf65acc945609f4e2e0ae78ff288b142d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907966"
---
# <span data-ttu-id="52414-101">Add-AzStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="52414-101">Add-AzStorageAccountNetworkRule</span></span>

## <span data-ttu-id="52414-102">簡介</span><span class="sxs-lookup"><span data-stu-id="52414-102">SYNOPSIS</span></span>
 <span data-ttu-id="52414-103">新增 IpRules 或 VirtualNetworkRules 至儲存空間帳戶的 NetworkRule 屬性</span><span class="sxs-lookup"><span data-stu-id="52414-103">Add IpRules or VirtualNetworkRules to the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="52414-104">語法</span><span class="sxs-lookup"><span data-stu-id="52414-104">SYNTAX</span></span>

### <span data-ttu-id="52414-105">NetWorkRuleString (預設) </span><span class="sxs-lookup"><span data-stu-id="52414-105">NetWorkRuleString (Default)</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkResourceId <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="52414-106">IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="52414-106">IpRuleObject</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPRule <PSIpRule[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52414-107">NetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="52414-107">NetworkRuleObject</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkRule <PSVirtualNetworkRule[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52414-108">ResourceAccessRuleObject</span><span class="sxs-lookup"><span data-stu-id="52414-108">ResourceAccessRuleObject</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -ResourceAccessRule <PSResourceAccessRule[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52414-109">IpRuleString</span><span class="sxs-lookup"><span data-stu-id="52414-109">IpRuleString</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPAddressOrRange <String[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52414-110">ResourceAccessRuleString</span><span class="sxs-lookup"><span data-stu-id="52414-110">ResourceAccessRuleString</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -TenantId <String>
 -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="52414-111">描述</span><span class="sxs-lookup"><span data-stu-id="52414-111">DESCRIPTION</span></span>
<span data-ttu-id="52414-112">**Add-AzStorageAccountNetworkRule** Cmdlet 會將 IpRules 或 VirtualNetworkRules 新增到儲存帳戶的 NetworkRule 屬性</span><span class="sxs-lookup"><span data-stu-id="52414-112">The **Add-AzStorageAccountNetworkRule** cmdlet adds IpRules or VirtualNetworkRules to the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="52414-113">例子</span><span class="sxs-lookup"><span data-stu-id="52414-113">EXAMPLES</span></span>

### <span data-ttu-id="52414-114">範例 1：使用 IPAddressOrRange 新增多個 IpRules</span><span class="sxs-lookup"><span data-stu-id="52414-114">Example 1: Add several IpRules with IPAddressOrRange</span></span>
```
PS C:\>Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount" -IPAddressOrRange "10.0.0.0/24","28.2.0.0/16"
```

<span data-ttu-id="52414-115">此命令會使用 IPAddressOrRange 新增數個 IpRules。</span><span class="sxs-lookup"><span data-stu-id="52414-115">This command add several IpRules with IPAddressOrRange.</span></span>

### <span data-ttu-id="52414-116">範例 2：使用 VirtualNetworkResourceID 新增 VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="52414-116">Example 2: Add a VirtualNetworkRule with VirtualNetworkResourceID</span></span>
```
PS C:\>$subnet = Get-AzVirtualNetwork -ResourceGroupName "myResourceGroup" -Name "myvirtualnetwork" | Get-AzVirtualNetworkSubnetConfig
PS C:\>Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount" -VirtualNetworkResourceId $subnet[0].Id
```

<span data-ttu-id="52414-117">此命令會新增 VirtualNetworkRule 與 VirtualNetworkResourceID。</span><span class="sxs-lookup"><span data-stu-id="52414-117">This command add a VirtualNetworkRule with VirtualNetworkResourceID.</span></span>

### <span data-ttu-id="52414-118">範例 3：使用 VirtualNetworkRule Objects 從另一個帳戶新增 VirtualNetworkRules</span><span class="sxs-lookup"><span data-stu-id="52414-118">Example 3: Add VirtualNetworkRules with VirtualNetworkRule Objects from another account</span></span>
```
PS C:\> $networkrule = Get-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "mystorageaccount1"
PS C:\> Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount2" -VirtualNetworkRule $networkrule.VirtualNetworkRules
```

<span data-ttu-id="52414-119">此命令會使用 VirtualNetworkRule Objects 從另一個帳戶新增 VirtualNetworkRules。</span><span class="sxs-lookup"><span data-stu-id="52414-119">This command add VirtualNetworkRules with VirtualNetworkRule Objects from another account.</span></span>

### <span data-ttu-id="52414-120">範例 4：使用 IpRule 物件新增多個 IpRule，使用 JSON 輸入</span><span class="sxs-lookup"><span data-stu-id="52414-120">Example 4: Add several IpRule with IpRule objects, input with JSON</span></span>
```
PS C:\>Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount" -IPRule (@{IPAddressOrRange="10.0.0.0/24";Action="allow"},@{IPAddressOrRange="28.2.0.0/16";Action="allow"})
```

<span data-ttu-id="52414-121">此命令會使用 IpRule 物件新增數個 IpRule，並輸入 JSON。</span><span class="sxs-lookup"><span data-stu-id="52414-121">This command add several IpRule with IpRule objects, input with JSON.</span></span>

### <span data-ttu-id="52414-122">範例 5：新增資源存取規則</span><span class="sxs-lookup"><span data-stu-id="52414-122">Example 5: Add a resource access rule</span></span>
```
PS C:\>Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount" -TenantId $tenantId -ResourceId $ResourceId
```

<span data-ttu-id="52414-123">此命令會使用 TenantId 和 ResourceId 新增資源存取規則。</span><span class="sxs-lookup"><span data-stu-id="52414-123">This command adds a resource access rule with TenantId and ResourceId.</span></span>

### <span data-ttu-id="52414-124">範例 6：新增一個儲存帳戶的所有資源存取規則至另一個儲存帳戶</span><span class="sxs-lookup"><span data-stu-id="52414-124">Example 6: Add all resource access rules of one storage account to another storage account</span></span>
```
PS C:\> (Get-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "mystorageaccount1").ResourceAccessRules | Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount2"
```

<span data-ttu-id="52414-125">此命令會從一個儲存帳戶取得所有資源存取規則，並新增到另一個儲存帳戶。</span><span class="sxs-lookup"><span data-stu-id="52414-125">This command gets all resource access rules from one storage account, and adds them to another storage account.</span></span>

## <span data-ttu-id="52414-126">參數</span><span class="sxs-lookup"><span data-stu-id="52414-126">PARAMETERS</span></span>

### <span data-ttu-id="52414-127">-AsJob</span><span class="sxs-lookup"><span data-stu-id="52414-127">-AsJob</span></span>
<span data-ttu-id="52414-128">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="52414-128">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="52414-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52414-129">-DefaultProfile</span></span>
<span data-ttu-id="52414-130">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="52414-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52414-131">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="52414-131">-IPAddressOrRange</span></span>
<span data-ttu-id="52414-132">IpAddressOrRange 陣列，新增 IpRules 與輸入 IpAddressOrRange 和預設動作 Allow to NetworkRule 屬性。</span><span class="sxs-lookup"><span data-stu-id="52414-132">The Array of IpAddressOrRange, add IpRules with the input IpAddressOrRange and default Action Allow to NetworkRule Property.</span></span>

```yaml
Type: System.String[]
Parameter Sets: IpRuleString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52414-133">-IPRule</span><span class="sxs-lookup"><span data-stu-id="52414-133">-IPRule</span></span>
<span data-ttu-id="52414-134">要新加入 NetworkRule 屬性的 IpRule 物件的陣列。</span><span class="sxs-lookup"><span data-stu-id="52414-134">The Array of IpRule objects to add to the NetworkRule Property.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]
Parameter Sets: IpRuleObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="52414-135">-名稱</span><span class="sxs-lookup"><span data-stu-id="52414-135">-Name</span></span>
<span data-ttu-id="52414-136">指定儲存空間帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="52414-136">Specifies the name of the Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52414-137">-ResourceAccessRule</span><span class="sxs-lookup"><span data-stu-id="52414-137">-ResourceAccessRule</span></span>
<span data-ttu-id="52414-138">儲存帳戶 NetworkRule ResourceAccessRules.</span><span class="sxs-lookup"><span data-stu-id="52414-138">Storage Account NetworkRule ResourceAccessRules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSResourceAccessRule[]
Parameter Sets: ResourceAccessRuleObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="52414-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52414-139">-ResourceGroupName</span></span>
<span data-ttu-id="52414-140">指定包含儲存空間帳戶的資源組名。</span><span class="sxs-lookup"><span data-stu-id="52414-140">Specifies the name of the resource group contains the Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52414-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="52414-141">-ResourceId</span></span>
<span data-ttu-id="52414-142">儲存帳戶 ResourceAccessRule ResourceId in string.</span><span class="sxs-lookup"><span data-stu-id="52414-142">Storage Account ResourceAccessRule ResourceId  in string.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceAccessRuleString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52414-143">-TenantId</span><span class="sxs-lookup"><span data-stu-id="52414-143">-TenantId</span></span>
<span data-ttu-id="52414-144">儲存帳戶 ResourceAccessRule TenantId in string.</span><span class="sxs-lookup"><span data-stu-id="52414-144">Storage Account ResourceAccessRule TenantId  in string.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceAccessRuleString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52414-145">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="52414-145">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="52414-146">VirtualNetworkResourceId 陣列會新增 VirtualNetworkRule 與 Input VirtualNetworkResourceId 和預設動作 Allow to NetworkRule 屬性。</span><span class="sxs-lookup"><span data-stu-id="52414-146">The Array of VirtualNetworkResourceId, will add VirtualNetworkRule with input VirtualNetworkResourceId and default Action Allow to NetworkRule Property.</span></span>

```yaml
Type: System.String[]
Parameter Sets: NetWorkRuleString
Aliases: SubnetId, VirtualNetworkId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52414-147">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="52414-147">-VirtualNetworkRule</span></span>
<span data-ttu-id="52414-148">要新加入 NetworkRule 屬性的 VirtualNetworkRule 物件的陣列。</span><span class="sxs-lookup"><span data-stu-id="52414-148">The Array of VirtualNetworkRule objects to add to the NetworkRule Property.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]
Parameter Sets: NetworkRuleObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="52414-149">-確認</span><span class="sxs-lookup"><span data-stu-id="52414-149">-Confirm</span></span>
<span data-ttu-id="52414-150">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="52414-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52414-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52414-151">-WhatIf</span></span>
<span data-ttu-id="52414-152">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="52414-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52414-153">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="52414-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52414-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52414-154">CommonParameters</span></span>
<span data-ttu-id="52414-155">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="52414-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52414-156">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="52414-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52414-157">輸入</span><span class="sxs-lookup"><span data-stu-id="52414-157">INPUTS</span></span>

### <span data-ttu-id="52414-158">System.String</span><span class="sxs-lookup"><span data-stu-id="52414-158">System.String</span></span>

### <span data-ttu-id="52414-159">Microsoft.Azure.Commands.management.storage.models.PSIpRule[]</span><span class="sxs-lookup"><span data-stu-id="52414-159">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span></span>

### <span data-ttu-id="52414-160">Microsoft.Azure.Commands.management.storage.models.PSVirtualNetworkRule[]</span><span class="sxs-lookup"><span data-stu-id="52414-160">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="52414-161">輸出</span><span class="sxs-lookup"><span data-stu-id="52414-161">OUTPUTS</span></span>

### <span data-ttu-id="52414-162">Microsoft.Azure.Commands.management.storage.models.PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="52414-162">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule</span></span>

### <span data-ttu-id="52414-163">Microsoft.Azure.Commands.management.storage.models.PSIpRule</span><span class="sxs-lookup"><span data-stu-id="52414-163">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule</span></span>

## <span data-ttu-id="52414-164">筆記</span><span class="sxs-lookup"><span data-stu-id="52414-164">NOTES</span></span>

## <span data-ttu-id="52414-165">相關連結</span><span class="sxs-lookup"><span data-stu-id="52414-165">RELATED LINKS</span></span>
