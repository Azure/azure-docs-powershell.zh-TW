---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/add-azurermstorageaccountnetworkrule
schema: 2.0.0
ms.openlocfilehash: 0b1d497bbd7e976d942bdc3f99c6bea2d4c2c1cb
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93800662"
---
# <span data-ttu-id="af78c-101">Add-AzureRmStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="af78c-101">Add-AzureRmStorageAccountNetworkRule</span></span>

## <span data-ttu-id="af78c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="af78c-102">SYNOPSIS</span></span>
 <span data-ttu-id="af78c-103">在儲存空間帳戶的 NetworkRule 屬性中新增 IpRules 或 VirtualNetworkRules</span><span class="sxs-lookup"><span data-stu-id="af78c-103">Add IpRules or VirtualNetworkRules to the NetworkRule property of a Storage account</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="af78c-104">句法</span><span class="sxs-lookup"><span data-stu-id="af78c-104">SYNTAX</span></span>

### <span data-ttu-id="af78c-105">NetWorkRuleString (預設) </span><span class="sxs-lookup"><span data-stu-id="af78c-105">NetWorkRuleString (Default)</span></span>
```
Add-AzureRmStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkResourceId <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="af78c-106">IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="af78c-106">IpRuleObject</span></span>
```
Add-AzureRmStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPRule <PSIpRule[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af78c-107">NetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="af78c-107">NetworkRuleObject</span></span>
```
Add-AzureRmStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkRule <PSVirtualNetworkRule[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af78c-108">IpRuleString</span><span class="sxs-lookup"><span data-stu-id="af78c-108">IpRuleString</span></span>
```
Add-AzureRmStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -IPAddressOrRange <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="af78c-109">說明</span><span class="sxs-lookup"><span data-stu-id="af78c-109">DESCRIPTION</span></span>
<span data-ttu-id="af78c-110">**AzureRmStorageAccountNetworkRule** Cmdlet 會將 IpRules 或 VirtualNetworkRules 新增至儲存空間帳戶的 NetworkRule 屬性</span><span class="sxs-lookup"><span data-stu-id="af78c-110">The **Add-AzureRmStorageAccountNetworkRule** cmdlet adds IpRules or VirtualNetworkRules to the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="af78c-111">示例</span><span class="sxs-lookup"><span data-stu-id="af78c-111">EXAMPLES</span></span>

### <span data-ttu-id="af78c-112">範例1：在 IPAddressOrRange 中新增數個 IpRules</span><span class="sxs-lookup"><span data-stu-id="af78c-112">Example 1: Add several IpRules with IPAddressOrRange</span></span>
```
PS C:\>Add-AzureRMStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount" -IPAddressOrRange "10.0.0.0/24","28.2.0.0/16"
```

<span data-ttu-id="af78c-113">這個命令在 IPAddressOrRange 中新增數個 IpRules。</span><span class="sxs-lookup"><span data-stu-id="af78c-113">This command add several IpRules with IPAddressOrRange.</span></span>

### <span data-ttu-id="af78c-114">範例2：使用 VirtualNetworkResourceID 新增 VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="af78c-114">Example 2: Add a VirtualNetworkRule with VirtualNetworkResourceID</span></span>
```
PS C:\>$subnet = Get-AzureRmVirtualNetwork -ResourceGroupName "myResourceGroup" -Name "myvirtualnetwork" | Get-AzureRmVirtualNetworkSubnetConfig
PS C:\>Add-AzureRMStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount" -VirtualNetworkResourceId $subnet[0].Id
```

<span data-ttu-id="af78c-115">這個命令會在 VirtualNetworkResourceID 中新增 VirtualNetworkRule。</span><span class="sxs-lookup"><span data-stu-id="af78c-115">This command add a VirtualNetworkRule with VirtualNetworkResourceID.</span></span>

### <span data-ttu-id="af78c-116">範例3：從另一個帳戶新增 VirtualNetworkRules 與 VirtualNetworkRule 物件</span><span class="sxs-lookup"><span data-stu-id="af78c-116">Example 3: Add VirtualNetworkRules with VirtualNetworkRule Objects from another account</span></span>
```
PS C:\> $networkrule = Get-AzureRMStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "mystorageaccount1"
PS C:\> Add-AzureRMStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount2" -VirtualNetworkRule $networkrule.VirtualNetworkRules
```

<span data-ttu-id="af78c-117">這個命令會從另一個帳戶新增 VirtualNetworkRules 與 VirtualNetworkRule 物件。</span><span class="sxs-lookup"><span data-stu-id="af78c-117">This command add VirtualNetworkRules with VirtualNetworkRule Objects from another account.</span></span>

### <span data-ttu-id="af78c-118">範例4：使用 IpRule 物件新增多個 IpRule，並以 JSON 輸入</span><span class="sxs-lookup"><span data-stu-id="af78c-118">Example 4: Add several IpRule with IpRule objects, input with JSON</span></span>
```
PS C:\>Add-AzureRMStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount" -IPRule (@{IPAddressOrRange="10.0.0.0/24";Action="allow"},@{IPAddressOrRange="28.2.0.0/16";Action="allow"})
```

<span data-ttu-id="af78c-119">這個命令會在多個 IpRule 物件中新增數個 IpRule，並以 JSON 進行輸入。</span><span class="sxs-lookup"><span data-stu-id="af78c-119">This command add several IpRule with IpRule objects, input with JSON.</span></span>

## <span data-ttu-id="af78c-120">參數</span><span class="sxs-lookup"><span data-stu-id="af78c-120">PARAMETERS</span></span>

### <span data-ttu-id="af78c-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="af78c-121">-AsJob</span></span>
<span data-ttu-id="af78c-122">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="af78c-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="af78c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af78c-123">-DefaultProfile</span></span>
<span data-ttu-id="af78c-124">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="af78c-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af78c-125">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="af78c-125">-IPAddressOrRange</span></span>
<span data-ttu-id="af78c-126">IpAddressOrRange 陣列，請在輸入 IpAddressOrRange 中新增 IpRules，並使用預設動作 [允許 NetworkRule] 屬性。</span><span class="sxs-lookup"><span data-stu-id="af78c-126">The Array of IpAddressOrRange, add IpRules with the input IpAddressOrRange and default Action Allow to NetworkRule Property.</span></span>

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

### <span data-ttu-id="af78c-127">-IPRule</span><span class="sxs-lookup"><span data-stu-id="af78c-127">-IPRule</span></span>
<span data-ttu-id="af78c-128">要新增至 NetworkRule 屬性的 IpRule 物件陣列。</span><span class="sxs-lookup"><span data-stu-id="af78c-128">The Array of IpRule objects to add to the NetworkRule Property.</span></span>

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

### <span data-ttu-id="af78c-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="af78c-129">-Name</span></span>
<span data-ttu-id="af78c-130">指定儲存空間帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="af78c-130">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="af78c-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af78c-131">-ResourceGroupName</span></span>
<span data-ttu-id="af78c-132">指定包含儲存空間帳戶之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="af78c-132">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="af78c-133">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="af78c-133">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="af78c-134">VirtualNetworkResourceId 陣列會將 VirtualNetworkRule 新增至輸入 VirtualNetworkResourceId，並將預設動作設為 NetworkRule 屬性。</span><span class="sxs-lookup"><span data-stu-id="af78c-134">The Array of VirtualNetworkResourceId, will add VirtualNetworkRule with input VirtualNetworkResourceId and default Action Allow to NetworkRule Property.</span></span>

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

### <span data-ttu-id="af78c-135">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="af78c-135">-VirtualNetworkRule</span></span>
<span data-ttu-id="af78c-136">要新增至 NetworkRule 屬性的 VirtualNetworkRule 物件陣列。</span><span class="sxs-lookup"><span data-stu-id="af78c-136">The Array of VirtualNetworkRule objects to add to the NetworkRule Property.</span></span>

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

### <span data-ttu-id="af78c-137">-確認</span><span class="sxs-lookup"><span data-stu-id="af78c-137">-Confirm</span></span>
<span data-ttu-id="af78c-138">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="af78c-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af78c-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af78c-139">-WhatIf</span></span>
<span data-ttu-id="af78c-140">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="af78c-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af78c-141">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="af78c-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af78c-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af78c-142">CommonParameters</span></span>
<span data-ttu-id="af78c-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="af78c-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af78c-144">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="af78c-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af78c-145">輸入</span><span class="sxs-lookup"><span data-stu-id="af78c-145">INPUTS</span></span>

### <span data-ttu-id="af78c-146">System.object</span><span class="sxs-lookup"><span data-stu-id="af78c-146">System.String</span></span>

### <span data-ttu-id="af78c-147">PSIpRule [] 的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="af78c-147">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span></span>
<span data-ttu-id="af78c-148">參數： IPRule (ByValue) </span><span class="sxs-lookup"><span data-stu-id="af78c-148">Parameters: IPRule (ByValue)</span></span>

### <span data-ttu-id="af78c-149">PSVirtualNetworkRule [] 的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="af78c-149">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span></span>
<span data-ttu-id="af78c-150">參數： VirtualNetworkRule (ByValue) </span><span class="sxs-lookup"><span data-stu-id="af78c-150">Parameters: VirtualNetworkRule (ByValue)</span></span>

## <span data-ttu-id="af78c-151">輸出</span><span class="sxs-lookup"><span data-stu-id="af78c-151">OUTPUTS</span></span>

### <span data-ttu-id="af78c-152">PSVirtualNetworkRule 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="af78c-152">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule</span></span>

### <span data-ttu-id="af78c-153">PSIpRule 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="af78c-153">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule</span></span>

## <span data-ttu-id="af78c-154">筆記</span><span class="sxs-lookup"><span data-stu-id="af78c-154">NOTES</span></span>

## <span data-ttu-id="af78c-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="af78c-155">RELATED LINKS</span></span>
