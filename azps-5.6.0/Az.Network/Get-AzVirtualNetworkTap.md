---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualnetworktap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkTap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkTap.md
ms.openlocfilehash: 154cededf20ceb88fdbc851b96189282e1b6123a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915353"
---
# <span data-ttu-id="ae2e7-101">Get-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="ae2e7-101">Get-AzVirtualNetworkTap</span></span>

## <span data-ttu-id="ae2e7-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ae2e7-102">SYNOPSIS</span></span>
<span data-ttu-id="ae2e7-103">點一下虛擬網路</span><span class="sxs-lookup"><span data-stu-id="ae2e7-103">Gets a virtual network tap</span></span>

## <span data-ttu-id="ae2e7-104">語法</span><span class="sxs-lookup"><span data-stu-id="ae2e7-104">SYNTAX</span></span>

### <span data-ttu-id="ae2e7-105">ListParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="ae2e7-105">ListParameterSet (Default)</span></span>
```
Get-AzVirtualNetworkTap [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae2e7-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ae2e7-106">GetByResourceIdParameterSet</span></span>
```
Get-AzVirtualNetworkTap -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ae2e7-107">描述</span><span class="sxs-lookup"><span data-stu-id="ae2e7-107">DESCRIPTION</span></span>
<span data-ttu-id="ae2e7-108">**Get-AzVirtualNetworkTap** Cmdlet 會取得 Azure 虛擬網路點一下，或在資源群組中點一下 Azure 虛擬網路清單。</span><span class="sxs-lookup"><span data-stu-id="ae2e7-108">The **Get-AzVirtualNetworkTap** cmdlet gets an Azure virtual network tap or a list of Azure virtual network taps in a resource group.</span></span>

## <span data-ttu-id="ae2e7-109">例子</span><span class="sxs-lookup"><span data-stu-id="ae2e7-109">EXAMPLES</span></span>

### <span data-ttu-id="ae2e7-110">範例 1：取得虛擬網路點一下</span><span class="sxs-lookup"><span data-stu-id="ae2e7-110">Example 1: Get a virtual network tap</span></span>
```
PS C:\> Get-AzVirtualNetworkTap -ResourceGroupName "ResourceGroup1" -Name "VirtualTap1"
```

<span data-ttu-id="ae2e7-111">此命令會針對 "ResourceGroup1" 中給 "VirtualTap1" 的 VirtualNetwork 點一下參照。</span><span class="sxs-lookup"><span data-stu-id="ae2e7-111">This command gets a VirtualNetwork tap reference for given "VirtualTap1" in "ResourceGroup1".</span></span>

### <span data-ttu-id="ae2e7-112">範例 2：使用篩選取得所有虛擬網路點一下</span><span class="sxs-lookup"><span data-stu-id="ae2e7-112">Example 2: Get all virtual network taps using filtering</span></span>
```
PS C:\> Get-AzVirtualNetworkTap -Name "VirtualTap*"
```

<span data-ttu-id="ae2e7-113">此命令會獲得以 "VirtualTap" 為起點的所有 VirtualNetwork 點一下參照。</span><span class="sxs-lookup"><span data-stu-id="ae2e7-113">This command gets all VirtualNetwork tap references that start with "VirtualTap".</span></span>

## <span data-ttu-id="ae2e7-114">參數</span><span class="sxs-lookup"><span data-stu-id="ae2e7-114">PARAMETERS</span></span>

### <span data-ttu-id="ae2e7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae2e7-115">-DefaultProfile</span></span>
<span data-ttu-id="ae2e7-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="ae2e7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae2e7-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="ae2e7-117">-Name</span></span>
<span data-ttu-id="ae2e7-118">點一下的名稱。</span><span class="sxs-lookup"><span data-stu-id="ae2e7-118">The name of the tap.</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="ae2e7-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae2e7-119">-ResourceGroupName</span></span>
<span data-ttu-id="ae2e7-120">點一下虛擬網路的資源組名。</span><span class="sxs-lookup"><span data-stu-id="ae2e7-120">The resource group name of the virtual network tap.</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="ae2e7-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ae2e7-121">-ResourceId</span></span>
<span data-ttu-id="ae2e7-122">VirtualNetworkTap 資源的 ResourceId</span><span class="sxs-lookup"><span data-stu-id="ae2e7-122">ResourceId of the VirtualNetworkTap resource</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae2e7-123">-確認</span><span class="sxs-lookup"><span data-stu-id="ae2e7-123">-Confirm</span></span>
<span data-ttu-id="ae2e7-124">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="ae2e7-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae2e7-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae2e7-125">-WhatIf</span></span>
<span data-ttu-id="ae2e7-126">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ae2e7-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ae2e7-127">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ae2e7-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae2e7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae2e7-128">CommonParameters</span></span>
<span data-ttu-id="ae2e7-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ae2e7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae2e7-130">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ae2e7-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae2e7-131">輸入</span><span class="sxs-lookup"><span data-stu-id="ae2e7-131">INPUTS</span></span>

### <span data-ttu-id="ae2e7-132">System.String</span><span class="sxs-lookup"><span data-stu-id="ae2e7-132">System.String</span></span>

## <span data-ttu-id="ae2e7-133">輸出</span><span class="sxs-lookup"><span data-stu-id="ae2e7-133">OUTPUTS</span></span>

### <span data-ttu-id="ae2e7-134">Microsoft.Azure.Commands.Network.models.PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="ae2e7-134">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="ae2e7-135">筆記</span><span class="sxs-lookup"><span data-stu-id="ae2e7-135">NOTES</span></span>

## <span data-ttu-id="ae2e7-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="ae2e7-136">RELATED LINKS</span></span>

[<span data-ttu-id="ae2e7-137">New-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="ae2e7-137">New-AzVirtualNetworkTap</span></span>](./New-AzVirtualNetworkTap.md)

[<span data-ttu-id="ae2e7-138">Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="ae2e7-138">Remove-AzVirtualNetworkTap</span></span>](./Remove-AzVirtualNetworkTap.md)

[<span data-ttu-id="ae2e7-139">Set-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="ae2e7-139">Set-AzVirtualNetworkTap</span></span>](./Set-AzVirtualNetworkTap.md)
