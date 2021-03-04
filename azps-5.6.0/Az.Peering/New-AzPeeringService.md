---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/new-azpeeringservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringService.md
ms.openlocfilehash: 1fc1d2f9269bf48d6f6dfd79caa8e34b3de51fee
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911434"
---
# <span data-ttu-id="69459-101">New-AzPeeringService</span><span class="sxs-lookup"><span data-stu-id="69459-101">New-AzPeeringService</span></span>

## <span data-ttu-id="69459-102">簡介</span><span class="sxs-lookup"><span data-stu-id="69459-102">SYNOPSIS</span></span>
<span data-ttu-id="69459-103">建立新的對等服務。</span><span class="sxs-lookup"><span data-stu-id="69459-103">Creates a new peering service.</span></span>

## <span data-ttu-id="69459-104">語法</span><span class="sxs-lookup"><span data-stu-id="69459-104">SYNTAX</span></span>

```
New-AzPeeringService [-ResourceGroupName] <String> [-Name] <String> [-PeeringLocation] <String>
 [-PeeringServiceProvider] <String> [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69459-105">描述</span><span class="sxs-lookup"><span data-stu-id="69459-105">DESCRIPTION</span></span>
<span data-ttu-id="69459-106">建立對等服務。</span><span class="sxs-lookup"><span data-stu-id="69459-106">Creates peering service.</span></span>

## <span data-ttu-id="69459-107">例子</span><span class="sxs-lookup"><span data-stu-id="69459-107">EXAMPLES</span></span>

### <span data-ttu-id="69459-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="69459-108">Example 1</span></span>
```powershell
PS C:\> New-AzPeeringService -ResourceGroupName $resourceGroup -Name $name -Location $loc -PeeringServiceProvider $provider

PeeringServiceLocation : Washington
PeeringServiceProvider : TestPeer1
ProvisioningState      : Succeeded
Location               : centralus
Tags                   : {}
Name                   : myPeeringService3990
Id                     : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService3990
Type                   : Microsoft.Peering/peeringServices
```

<span data-ttu-id="69459-109">建立具有提供者和對等位置的對等服務物件。</span><span class="sxs-lookup"><span data-stu-id="69459-109">Creates a peering service object with provider and peering location.</span></span> <span data-ttu-id="69459-110">用於與 `Get-AzPeeringServiceProvider``Get-AzPeeringServiceLocation`</span><span class="sxs-lookup"><span data-stu-id="69459-110">Use in conjuction with `Get-AzPeeringServiceProvider` and `Get-AzPeeringServiceLocation`</span></span>

## <span data-ttu-id="69459-111">參數</span><span class="sxs-lookup"><span data-stu-id="69459-111">PARAMETERS</span></span>

### <span data-ttu-id="69459-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="69459-112">-AsJob</span></span>
<span data-ttu-id="69459-113">在背景執行。</span><span class="sxs-lookup"><span data-stu-id="69459-113">Run in the background.</span></span>

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

### <span data-ttu-id="69459-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69459-114">-DefaultProfile</span></span>
<span data-ttu-id="69459-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="69459-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="69459-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="69459-116">-Name</span></span>
<span data-ttu-id="69459-117">PSPeering 的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="69459-117">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69459-118">-對等位置</span><span class="sxs-lookup"><span data-stu-id="69459-118">-PeeringLocation</span></span>
<span data-ttu-id="69459-119">與 Azure 區域不同的實體位置。</span><span class="sxs-lookup"><span data-stu-id="69459-119">The Physical Location Different from Azure Region.</span></span> <span data-ttu-id="69459-120">使用 Get-AzPeeringServiceLocation [-Country <country> ]</span><span class="sxs-lookup"><span data-stu-id="69459-120">Use Get-AzPeeringServiceLocation [-Country <country>]</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69459-121">-PeeringServiceProvider</span><span class="sxs-lookup"><span data-stu-id="69459-121">-PeeringServiceProvider</span></span>
<span data-ttu-id="69459-122">對等服務提供者名稱。</span><span class="sxs-lookup"><span data-stu-id="69459-122">The peering service provider name.</span></span>
<span data-ttu-id="69459-123">將Get-AzPeeringServiceProvider Cmdlet 用於清單</span><span class="sxs-lookup"><span data-stu-id="69459-123">Use Get-AzPeeringServiceProvider cmdlet for a list</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69459-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69459-124">-ResourceGroupName</span></span>
<span data-ttu-id="69459-125">建立或使用現有的資源組名。</span><span class="sxs-lookup"><span data-stu-id="69459-125">The create or use an existing resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69459-126">-標記</span><span class="sxs-lookup"><span data-stu-id="69459-126">-Tag</span></span>
<span data-ttu-id="69459-127">與 Microsoft InputObject Service 關聯的標記。</span><span class="sxs-lookup"><span data-stu-id="69459-127">The tags to associate with the Microsoft InputObject Service.</span></span>

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

### <span data-ttu-id="69459-128">-確認</span><span class="sxs-lookup"><span data-stu-id="69459-128">-Confirm</span></span>
<span data-ttu-id="69459-129">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="69459-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69459-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69459-130">-WhatIf</span></span>
<span data-ttu-id="69459-131">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="69459-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69459-132">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="69459-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69459-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69459-133">CommonParameters</span></span>
<span data-ttu-id="69459-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="69459-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69459-135">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="69459-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69459-136">輸入</span><span class="sxs-lookup"><span data-stu-id="69459-136">INPUTS</span></span>

### <span data-ttu-id="69459-137">沒有</span><span class="sxs-lookup"><span data-stu-id="69459-137">None</span></span>

## <span data-ttu-id="69459-138">輸出</span><span class="sxs-lookup"><span data-stu-id="69459-138">OUTPUTS</span></span>

### <span data-ttu-id="69459-139">Microsoft.Azure.PowerShell.Cmdlets.Peering.models.PSPeeringService</span><span class="sxs-lookup"><span data-stu-id="69459-139">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService</span></span>

## <span data-ttu-id="69459-140">筆記</span><span class="sxs-lookup"><span data-stu-id="69459-140">NOTES</span></span>

## <span data-ttu-id="69459-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="69459-141">RELATED LINKS</span></span>
