---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Add-AzureRmStorageAccountNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Add-AzureRmStorageAccountNetworkRule.md
ms.openlocfilehash: 9f8d098cb27532980b01cf46da6c83d4da30ed48
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624536"
---
# <span data-ttu-id="83ead-101">Add-AzureRmStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="83ead-101">Add-AzureRmStorageAccountNetworkRule</span></span>

## <span data-ttu-id="83ead-102">摘要</span><span class="sxs-lookup"><span data-stu-id="83ead-102">SYNOPSIS</span></span>
 <span data-ttu-id="83ead-103">在儲存空間帳戶的 NetworkRule 屬性中新增 IpRules 或 VirtualNetworkRules</span><span class="sxs-lookup"><span data-stu-id="83ead-103">Add IpRules or VirtualNetworkRules to the NetworkRule property of a Storage Account</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="83ead-104">句法</span><span class="sxs-lookup"><span data-stu-id="83ead-104">SYNTAX</span></span>

### <span data-ttu-id="83ead-105">NetWorkRuleString (預設) </span><span class="sxs-lookup"><span data-stu-id="83ead-105">NetWorkRuleString (Default)</span></span>
```
Add-AzureRmStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkResourceId <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="83ead-106">IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="83ead-106">IpRuleObject</span></span>
```
Add-AzureRmStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPRule <PSIpRule[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83ead-107">NetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="83ead-107">NetworkRuleObject</span></span>
```
Add-AzureRmStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkRule <PSVirtualNetworkRule[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="83ead-108">IpRuleString</span><span class="sxs-lookup"><span data-stu-id="83ead-108">IpRuleString</span></span>
```
Add-AzureRmStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -IPAddressOrRange <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="83ead-109">說明</span><span class="sxs-lookup"><span data-stu-id="83ead-109">DESCRIPTION</span></span>
<span data-ttu-id="83ead-110">**AzureRmStorageAccountNetworkRule** Cmdlet 會將 IpRules 或 VirtualNetworkRules 新增至儲存空間帳戶的 NetworkRule 屬性</span><span class="sxs-lookup"><span data-stu-id="83ead-110">The **Add-AzureRmStorageAccountNetworkRule** cmdlet adds IpRules or VirtualNetworkRules to the NetworkRule property of a Storage Account</span></span>

## <span data-ttu-id="83ead-111">示例</span><span class="sxs-lookup"><span data-stu-id="83ead-111">EXAMPLES</span></span>

### <span data-ttu-id="83ead-112">範例1：在 IPAddressOrRange 中新增數個 IpRules</span><span class="sxs-lookup"><span data-stu-id="83ead-112">Example 1: Add several IpRules with IPAddressOrRange</span></span>
```
PS C:\>Add-AzureRMStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -IPAddressOrRange "10.0.0.0/24","28.2.0.0/16"
```

<span data-ttu-id="83ead-113">這個命令在 IPAddressOrRange 中新增數個 IpRules。</span><span class="sxs-lookup"><span data-stu-id="83ead-113">This command add several IpRules with IPAddressOrRange.</span></span>

### <span data-ttu-id="83ead-114">範例2：使用 VirtualNetworkResourceID 新增 VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="83ead-114">Example 2: Add a VirtualNetworkRule with VirtualNetworkResourceID</span></span>
```
PS C:\>$subnet = Get-AzureRmVirtualNetwork -ResourceGroupName "myResourceGroup" -Name "myvirtualnetwork" | Get-AzureRmVirtualNetworkSubnetConfig
PS C:\>Add-AzureRMStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -VirtualNetworkResourceId $subnet[0].Id
```

<span data-ttu-id="83ead-115">這個命令會在 VirtualNetworkResourceID 中新增 VirtualNetworkRule。</span><span class="sxs-lookup"><span data-stu-id="83ead-115">This command add a VirtualNetworkRule with VirtualNetworkResourceID.</span></span>

### <span data-ttu-id="83ead-116">範例3：從另一個帳戶新增 VirtualNetworkRules 與 VirtualNetworkRule 物件</span><span class="sxs-lookup"><span data-stu-id="83ead-116">Example 3: Add VirtualNetworkRules with VirtualNetworkRule Objects from another account</span></span>
```
PS C:\> $networkrule = Get-AzureRMStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount1"
PS C:\> Add-AzureRMStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount2" -VirtualNetworkRule $networkrule.VirtualNetworkRules
```

<span data-ttu-id="83ead-117">這個命令會從另一個帳戶新增 VirtualNetworkRules 與 VirtualNetworkRule 物件。</span><span class="sxs-lookup"><span data-stu-id="83ead-117">This command add VirtualNetworkRules with VirtualNetworkRule Objects from another account.</span></span>

### <span data-ttu-id="83ead-118">範例4：使用 IpRule 物件新增多個 IpRule，並以 JSON 輸入</span><span class="sxs-lookup"><span data-stu-id="83ead-118">Example 4: Add several IpRule with IpRule objects, input with JSON</span></span>
```
PS C:\>Add-AzureRMStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -IPRule (@{IPAddressOrRange="10.0.0.0/24";Action="allow"},@{IPAddressOrRange="28.2.0.0/16";Action="allow"})
```

<span data-ttu-id="83ead-119">這個命令會在多個 IpRule 物件中新增數個 IpRule，並以 JSON 進行輸入。</span><span class="sxs-lookup"><span data-stu-id="83ead-119">This command add several IpRule with IpRule objects, input with JSON.</span></span>

## <span data-ttu-id="83ead-120">參數</span><span class="sxs-lookup"><span data-stu-id="83ead-120">PARAMETERS</span></span>

### <span data-ttu-id="83ead-121">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="83ead-121">-IPAddressOrRange</span></span>
<span data-ttu-id="83ead-122">IpAddressOrRange 陣列，請在輸入 IpAddressOrRange 中新增 IpRules，並使用預設動作 [允許 NetworkRule] 屬性。</span><span class="sxs-lookup"><span data-stu-id="83ead-122">The Array of IpAddressOrRange, add IpRules with the input IpAddressOrRange and default Action Allow to NetworkRule Property.</span></span>

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

### <span data-ttu-id="83ead-123">-IPRule</span><span class="sxs-lookup"><span data-stu-id="83ead-123">-IPRule</span></span>
<span data-ttu-id="83ead-124">要新增至 NetworkRule 屬性的 IpRule 物件陣列。</span><span class="sxs-lookup"><span data-stu-id="83ead-124">The Array of IpRule objects to add to the NetworkRule Property.</span></span>

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

### <span data-ttu-id="83ead-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="83ead-125">-Name</span></span>
<span data-ttu-id="83ead-126">指定儲存空間帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="83ead-126">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="83ead-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83ead-127">-ResourceGroupName</span></span>
<span data-ttu-id="83ead-128">指定包含儲存空間帳戶之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="83ead-128">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="83ead-129">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="83ead-129">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="83ead-130">VirtualNetworkResourceId 陣列會將 VirtualNetworkRule 新增至輸入 VirtualNetworkResourceId，並將預設動作設為 NetworkRule 屬性。</span><span class="sxs-lookup"><span data-stu-id="83ead-130">The Array of VirtualNetworkResourceId, will add VirtualNetworkRule with input VirtualNetworkResourceId and default Action Allow to NetworkRule Property.</span></span>

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

### <span data-ttu-id="83ead-131">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="83ead-131">-VirtualNetworkRule</span></span>
<span data-ttu-id="83ead-132">要新增至 NetworkRule 屬性的 VirtualNetworkRule 物件陣列。</span><span class="sxs-lookup"><span data-stu-id="83ead-132">The Array of VirtualNetworkRule objects to add to the NetworkRule Property.</span></span>

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

### <span data-ttu-id="83ead-133">-確認</span><span class="sxs-lookup"><span data-stu-id="83ead-133">-Confirm</span></span>
<span data-ttu-id="83ead-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="83ead-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83ead-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83ead-135">-WhatIf</span></span>
<span data-ttu-id="83ead-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="83ead-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83ead-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="83ead-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83ead-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83ead-138">-DefaultProfile</span></span>
<span data-ttu-id="83ead-139">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="83ead-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="83ead-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83ead-140">CommonParameters</span></span>
<span data-ttu-id="83ead-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="83ead-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83ead-142">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="83ead-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83ead-143">輸入</span><span class="sxs-lookup"><span data-stu-id="83ead-143">INPUTS</span></span>

### <span data-ttu-id="83ead-144">System.object</span><span class="sxs-lookup"><span data-stu-id="83ead-144">System.String</span></span>
<span data-ttu-id="83ead-145">PSIpRule [] PSVirtualNetworkRule [].. [] 的 [] （[]）</span><span class="sxs-lookup"><span data-stu-id="83ead-145">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[] Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="83ead-146">輸出</span><span class="sxs-lookup"><span data-stu-id="83ead-146">OUTPUTS</span></span>

### <span data-ttu-id="83ead-147">PSVirtualNetworkRule 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="83ead-147">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule</span></span>
<span data-ttu-id="83ead-148">PSIpRule 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="83ead-148">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule</span></span>

## <span data-ttu-id="83ead-149">筆記</span><span class="sxs-lookup"><span data-stu-id="83ead-149">NOTES</span></span>

## <span data-ttu-id="83ead-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="83ead-150">RELATED LINKS</span></span>

