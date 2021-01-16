---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/add-azstorageaccountnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzStorageAccountNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzStorageAccountNetworkRule.md
ms.openlocfilehash: e1517801c964c4794c21ada6b7d64152c6e58178
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98280171"
---
# <span data-ttu-id="bc2ba-101">Add-AzStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="bc2ba-101">Add-AzStorageAccountNetworkRule</span></span>

## <span data-ttu-id="bc2ba-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bc2ba-102">SYNOPSIS</span></span>
 <span data-ttu-id="bc2ba-103">在儲存空間帳戶的 NetworkRule 屬性中新增 IpRules 或 VirtualNetworkRules</span><span class="sxs-lookup"><span data-stu-id="bc2ba-103">Add IpRules or VirtualNetworkRules to the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="bc2ba-104">句法</span><span class="sxs-lookup"><span data-stu-id="bc2ba-104">SYNTAX</span></span>

### <span data-ttu-id="bc2ba-105">NetWorkRuleString (預設) </span><span class="sxs-lookup"><span data-stu-id="bc2ba-105">NetWorkRuleString (Default)</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkResourceId <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bc2ba-106">IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="bc2ba-106">IpRuleObject</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPRule <PSIpRule[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc2ba-107">NetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="bc2ba-107">NetworkRuleObject</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkRule <PSVirtualNetworkRule[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc2ba-108">IpRuleString</span><span class="sxs-lookup"><span data-stu-id="bc2ba-108">IpRuleString</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPAddressOrRange <String[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bc2ba-109">說明</span><span class="sxs-lookup"><span data-stu-id="bc2ba-109">DESCRIPTION</span></span>
<span data-ttu-id="bc2ba-110">**AzStorageAccountNetworkRule** Cmdlet 會將 IpRules 或 VirtualNetworkRules 新增至儲存空間帳戶的 NetworkRule 屬性</span><span class="sxs-lookup"><span data-stu-id="bc2ba-110">The **Add-AzStorageAccountNetworkRule** cmdlet adds IpRules or VirtualNetworkRules to the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="bc2ba-111">示例</span><span class="sxs-lookup"><span data-stu-id="bc2ba-111">EXAMPLES</span></span>

### <span data-ttu-id="bc2ba-112">範例1：在 IPAddressOrRange 中新增數個 IpRules</span><span class="sxs-lookup"><span data-stu-id="bc2ba-112">Example 1: Add several IpRules with IPAddressOrRange</span></span>
```
PS C:\>Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount" -IPAddressOrRange "10.0.0.0/24","28.2.0.0/16"
```

<span data-ttu-id="bc2ba-113">這個命令在 IPAddressOrRange 中新增數個 IpRules。</span><span class="sxs-lookup"><span data-stu-id="bc2ba-113">This command add several IpRules with IPAddressOrRange.</span></span>

### <span data-ttu-id="bc2ba-114">範例2：使用 VirtualNetworkResourceID 新增 VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="bc2ba-114">Example 2: Add a VirtualNetworkRule with VirtualNetworkResourceID</span></span>
```
PS C:\>$subnet = Get-AzVirtualNetwork -ResourceGroupName "myResourceGroup" -Name "myvirtualnetwork" | Get-AzVirtualNetworkSubnetConfig
PS C:\>Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount" -VirtualNetworkResourceId $subnet[0].Id
```

<span data-ttu-id="bc2ba-115">這個命令會在 VirtualNetworkResourceID 中新增 VirtualNetworkRule。</span><span class="sxs-lookup"><span data-stu-id="bc2ba-115">This command add a VirtualNetworkRule with VirtualNetworkResourceID.</span></span>

### <span data-ttu-id="bc2ba-116">範例3：從另一個帳戶新增 VirtualNetworkRules 與 VirtualNetworkRule 物件</span><span class="sxs-lookup"><span data-stu-id="bc2ba-116">Example 3: Add VirtualNetworkRules with VirtualNetworkRule Objects from another account</span></span>
```
PS C:\> $networkrule = Get-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "mystorageaccount1"
PS C:\> Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount2" -VirtualNetworkRule $networkrule.VirtualNetworkRules
```

<span data-ttu-id="bc2ba-117">這個命令會從另一個帳戶新增 VirtualNetworkRules 與 VirtualNetworkRule 物件。</span><span class="sxs-lookup"><span data-stu-id="bc2ba-117">This command add VirtualNetworkRules with VirtualNetworkRule Objects from another account.</span></span>

### <span data-ttu-id="bc2ba-118">範例4：使用 IpRule 物件新增多個 IpRule，並以 JSON 輸入</span><span class="sxs-lookup"><span data-stu-id="bc2ba-118">Example 4: Add several IpRule with IpRule objects, input with JSON</span></span>
```
PS C:\>Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount" -IPRule (@{IPAddressOrRange="10.0.0.0/24";Action="allow"},@{IPAddressOrRange="28.2.0.0/16";Action="allow"})
```

<span data-ttu-id="bc2ba-119">這個命令會在多個 IpRule 物件中新增數個 IpRule，並以 JSON 進行輸入。</span><span class="sxs-lookup"><span data-stu-id="bc2ba-119">This command add several IpRule with IpRule objects, input with JSON.</span></span>

## <span data-ttu-id="bc2ba-120">參數</span><span class="sxs-lookup"><span data-stu-id="bc2ba-120">PARAMETERS</span></span>

### <span data-ttu-id="bc2ba-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bc2ba-121">-AsJob</span></span>
<span data-ttu-id="bc2ba-122">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="bc2ba-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bc2ba-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc2ba-123">-DefaultProfile</span></span>
<span data-ttu-id="bc2ba-124">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="bc2ba-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bc2ba-125">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="bc2ba-125">-IPAddressOrRange</span></span>
<span data-ttu-id="bc2ba-126">IpAddressOrRange 陣列，請在輸入 IpAddressOrRange 中新增 IpRules，並使用預設動作 [允許 NetworkRule] 屬性。</span><span class="sxs-lookup"><span data-stu-id="bc2ba-126">The Array of IpAddressOrRange, add IpRules with the input IpAddressOrRange and default Action Allow to NetworkRule Property.</span></span>

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

### <span data-ttu-id="bc2ba-127">-IPRule</span><span class="sxs-lookup"><span data-stu-id="bc2ba-127">-IPRule</span></span>
<span data-ttu-id="bc2ba-128">要新增至 NetworkRule 屬性的 IpRule 物件陣列。</span><span class="sxs-lookup"><span data-stu-id="bc2ba-128">The Array of IpRule objects to add to the NetworkRule Property.</span></span>

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

### <span data-ttu-id="bc2ba-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="bc2ba-129">-Name</span></span>
<span data-ttu-id="bc2ba-130">指定儲存空間帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="bc2ba-130">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="bc2ba-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc2ba-131">-ResourceGroupName</span></span>
<span data-ttu-id="bc2ba-132">指定包含儲存空間帳戶之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="bc2ba-132">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="bc2ba-133">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="bc2ba-133">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="bc2ba-134">VirtualNetworkResourceId 陣列會將 VirtualNetworkRule 新增至輸入 VirtualNetworkResourceId，並將預設動作設為 NetworkRule 屬性。</span><span class="sxs-lookup"><span data-stu-id="bc2ba-134">The Array of VirtualNetworkResourceId, will add VirtualNetworkRule with input VirtualNetworkResourceId and default Action Allow to NetworkRule Property.</span></span>

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

### <span data-ttu-id="bc2ba-135">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="bc2ba-135">-VirtualNetworkRule</span></span>
<span data-ttu-id="bc2ba-136">要新增至 NetworkRule 屬性的 VirtualNetworkRule 物件陣列。</span><span class="sxs-lookup"><span data-stu-id="bc2ba-136">The Array of VirtualNetworkRule objects to add to the NetworkRule Property.</span></span>

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

### <span data-ttu-id="bc2ba-137">-確認</span><span class="sxs-lookup"><span data-stu-id="bc2ba-137">-Confirm</span></span>
<span data-ttu-id="bc2ba-138">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="bc2ba-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc2ba-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc2ba-139">-WhatIf</span></span>
<span data-ttu-id="bc2ba-140">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="bc2ba-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bc2ba-141">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bc2ba-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc2ba-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc2ba-142">CommonParameters</span></span>
<span data-ttu-id="bc2ba-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bc2ba-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc2ba-144">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="bc2ba-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc2ba-145">輸入</span><span class="sxs-lookup"><span data-stu-id="bc2ba-145">INPUTS</span></span>

### <span data-ttu-id="bc2ba-146">System.object</span><span class="sxs-lookup"><span data-stu-id="bc2ba-146">System.String</span></span>

### <span data-ttu-id="bc2ba-147">PSIpRule [] 的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="bc2ba-147">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span></span>

### <span data-ttu-id="bc2ba-148">PSVirtualNetworkRule [] 的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="bc2ba-148">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="bc2ba-149">輸出</span><span class="sxs-lookup"><span data-stu-id="bc2ba-149">OUTPUTS</span></span>

### <span data-ttu-id="bc2ba-150">PSVirtualNetworkRule 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="bc2ba-150">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule</span></span>

### <span data-ttu-id="bc2ba-151">PSIpRule 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="bc2ba-151">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule</span></span>

## <span data-ttu-id="bc2ba-152">筆記</span><span class="sxs-lookup"><span data-stu-id="bc2ba-152">NOTES</span></span>

## <span data-ttu-id="bc2ba-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="bc2ba-153">RELATED LINKS</span></span>
