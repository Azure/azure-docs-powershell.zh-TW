---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azprivateendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateEndpoint.md
ms.openlocfilehash: f7ec596a73c3659584d1e0b80c899b4bf9aad8d2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909510"
---
# <span data-ttu-id="91b93-101">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="91b93-101">New-AzPrivateEndpoint</span></span>

## <span data-ttu-id="91b93-102">簡介</span><span class="sxs-lookup"><span data-stu-id="91b93-102">SYNOPSIS</span></span>
<span data-ttu-id="91b93-103">建立私人端點。</span><span class="sxs-lookup"><span data-stu-id="91b93-103">Creates a private endpoint.</span></span>

## <span data-ttu-id="91b93-104">語法</span><span class="sxs-lookup"><span data-stu-id="91b93-104">SYNTAX</span></span>

### <span data-ttu-id="91b93-105">所有</span><span class="sxs-lookup"><span data-stu-id="91b93-105">All</span></span>

```
New-AzPrivateEndpoint -Name <String> -ResourceGroupName <String> -Location <String> -Subnet <PSSubnet>
 -PrivateLinkServiceConnection <PSPrivateLinkServiceConnection[]> [-ByManualRequest] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="91b93-106">描述</span><span class="sxs-lookup"><span data-stu-id="91b93-106">DESCRIPTION</span></span>

<span data-ttu-id="91b93-107">**New-AzPrivateEndpoint** Cmdlet 會建立私人端點。</span><span class="sxs-lookup"><span data-stu-id="91b93-107">The **New-AzPrivateEndpoint** cmdlet creates a private endpoint.</span></span>

## <span data-ttu-id="91b93-108">例子</span><span class="sxs-lookup"><span data-stu-id="91b93-108">EXAMPLES</span></span>

### <span data-ttu-id="91b93-109">範例 1：建立私人端點</span><span class="sxs-lookup"><span data-stu-id="91b93-109">Example 1: Create a private endpoint</span></span>

<span data-ttu-id="91b93-110">下列範例會建立專用端點，在虛擬網路中指定的子網中具有特定的私人連結服務識別碼。</span><span class="sxs-lookup"><span data-stu-id="91b93-110">The following example creates a private endpoint with a specific private link service ID in the specified subnet in a virtual network.</span></span>

```powershell
$virtualNetwork = Get-AzVirtualNetwork -ResourceName 'myVirtualNetwork' -ResourceGroupName 'myResourceGroup'
$subnet = $virtualNetwork | Select-Object -ExpandProperty subnets | Where-Object Name -eq 'mySubnet'
$plsConnection= New-AzPrivateLinkServiceConnection -Name 'MyPLSConnections' -PrivateLinkServiceId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myResourceGroup/providers/Microsoft.Network/privateLinkServices/privateLinkService' -RequestMessage 'Please Approve my request'
New-AzPrivateEndpoint -Name 'MyPrivateEndpoint' -ResourceGroup 'myResourceGroup' -Location 'centralus' -PrivateLinkServiceConnection $plsConnection -Subnet $subnet
```

## <span data-ttu-id="91b93-111">參數</span><span class="sxs-lookup"><span data-stu-id="91b93-111">PARAMETERS</span></span>

### <span data-ttu-id="91b93-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="91b93-112">-AsJob</span></span>

<span data-ttu-id="91b93-113">在背景中以工作執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="91b93-113">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="91b93-114">-ByManualRequest</span><span class="sxs-lookup"><span data-stu-id="91b93-114">-ByManualRequest</span></span>

<span data-ttu-id="91b93-115">使用手動要求建立連接。</span><span class="sxs-lookup"><span data-stu-id="91b93-115">Use manual request to establish the connection.</span></span>

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

### <span data-ttu-id="91b93-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91b93-116">-DefaultProfile</span></span>

<span data-ttu-id="91b93-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="91b93-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="91b93-118">-強制</span><span class="sxs-lookup"><span data-stu-id="91b93-118">-Force</span></span>

<span data-ttu-id="91b93-119">請勿要求確認以覆寫資源。</span><span class="sxs-lookup"><span data-stu-id="91b93-119">Do not ask for confirmation to overwrite a resource.</span></span>

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

### <span data-ttu-id="91b93-120">-位置</span><span class="sxs-lookup"><span data-stu-id="91b93-120">-Location</span></span>

<span data-ttu-id="91b93-121">指定私人端點的位置。</span><span class="sxs-lookup"><span data-stu-id="91b93-121">Specifies a location for the private endpoint.</span></span> <span data-ttu-id="91b93-122">使用 [Get-AzLocation](/powershell/module/az.resources/get-azlocation) 來判斷此參數的有效值。</span><span class="sxs-lookup"><span data-stu-id="91b93-122">Use [Get-AzLocation](/powershell/module/az.resources/get-azlocation) to determine valid values for this parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91b93-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="91b93-123">-Name</span></span>

<span data-ttu-id="91b93-124">私人端點的名稱。</span><span class="sxs-lookup"><span data-stu-id="91b93-124">Name of the private endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91b93-125">-PrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="91b93-125">-PrivateLinkServiceConnection</span></span>

<span data-ttu-id="91b93-126">連接私人端點的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="91b93-126">The resource ID to connect the private endpoint.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceConnection[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91b93-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91b93-127">-ResourceGroupName</span></span>

<span data-ttu-id="91b93-128">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="91b93-128">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91b93-129">-子網</span><span class="sxs-lookup"><span data-stu-id="91b93-129">-Subnet</span></span>

<span data-ttu-id="91b93-130">私人端點的子網。</span><span class="sxs-lookup"><span data-stu-id="91b93-130">The subnet of the private endpoint.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91b93-131">-標記</span><span class="sxs-lookup"><span data-stu-id="91b93-131">-Tag</span></span>

<span data-ttu-id="91b93-132">以雜湊表格形式建立索引鍵值組。</span><span class="sxs-lookup"><span data-stu-id="91b93-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="91b93-133">例如：@{key0='value0';key1=$null;key2='value2'}</span><span class="sxs-lookup"><span data-stu-id="91b93-133">For example: @{key0='value0';key1=$null;key2='value2'}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91b93-134">-確認</span><span class="sxs-lookup"><span data-stu-id="91b93-134">-Confirm</span></span>

<span data-ttu-id="91b93-135">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="91b93-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91b93-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91b93-136">-WhatIf</span></span>

<span data-ttu-id="91b93-137">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="91b93-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="91b93-138">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="91b93-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91b93-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91b93-139">CommonParameters</span></span>

<span data-ttu-id="91b93-140">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="91b93-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91b93-141">詳細資訊[請參閱about_CommonParameters。](/powershell/module/microsoft.powershell.core/about/about_commonparameters)</span><span class="sxs-lookup"><span data-stu-id="91b93-141">For more information, see [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).</span></span>

## <span data-ttu-id="91b93-142">輸入</span><span class="sxs-lookup"><span data-stu-id="91b93-142">INPUTS</span></span>

### <span data-ttu-id="91b93-143">System.String</span><span class="sxs-lookup"><span data-stu-id="91b93-143">System.String</span></span>

### <span data-ttu-id="91b93-144">Microsoft.Azure.Commands.Network.models.PSSubnet</span><span class="sxs-lookup"><span data-stu-id="91b93-144">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="91b93-145">Microsoft.Azure.Commands.Network.models.PSPrivateLinkServiceConnection[]</span><span class="sxs-lookup"><span data-stu-id="91b93-145">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceConnection[]</span></span>

## <span data-ttu-id="91b93-146">輸出</span><span class="sxs-lookup"><span data-stu-id="91b93-146">OUTPUTS</span></span>

### <span data-ttu-id="91b93-147">Microsoft.Azure.Commands.Network.models.PSPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="91b93-147">Microsoft.Azure.Commands.Network.Models.PSPrivateEndpoint</span></span>

## <span data-ttu-id="91b93-148">筆記</span><span class="sxs-lookup"><span data-stu-id="91b93-148">NOTES</span></span>

## <span data-ttu-id="91b93-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="91b93-149">RELATED LINKS</span></span>

[<span data-ttu-id="91b93-150">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="91b93-150">Get-AzPrivateEndpoint</span></span>](./Get-AzPrivateEndpoint.md)

[<span data-ttu-id="91b93-151">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="91b93-151">Remove-AzPrivateEndpoint</span></span>](./Remove-AzPrivateEndpoint.md)

[<span data-ttu-id="91b93-152">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="91b93-152">New-AzPrivateLinkServiceConnection</span></span>](./New-AzPrivateLinkServiceConnection.md)