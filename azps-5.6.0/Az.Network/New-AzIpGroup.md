---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azipgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpGroup.md
ms.openlocfilehash: c8959d281c5eda7e2dd3f40941f5c727a000c588
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909521"
---
# <span data-ttu-id="fb641-101">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="fb641-101">New-AzIpGroup</span></span>

## <span data-ttu-id="fb641-102">簡介</span><span class="sxs-lookup"><span data-stu-id="fb641-102">SYNOPSIS</span></span>
<span data-ttu-id="fb641-103">建立 Azure IpGroup。</span><span class="sxs-lookup"><span data-stu-id="fb641-103">Creates an Azure IpGroup.</span></span>

## <span data-ttu-id="fb641-104">語法</span><span class="sxs-lookup"><span data-stu-id="fb641-104">SYNTAX</span></span>

```
New-AzIpGroup -Name <String> -ResourceGroupName <String> [-IpAddress <String[]>] -Location <String>
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fb641-105">描述</span><span class="sxs-lookup"><span data-stu-id="fb641-105">DESCRIPTION</span></span>
<span data-ttu-id="fb641-106">**New-AzIpGroup** Cmdlet 會建立 Azure IpGroup</span><span class="sxs-lookup"><span data-stu-id="fb641-106">The **New-AzIpGroup** cmdlet creates an Azure IpGroup</span></span>

## <span data-ttu-id="fb641-107">例子</span><span class="sxs-lookup"><span data-stu-id="fb641-107">EXAMPLES</span></span>

### <span data-ttu-id="fb641-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="fb641-108">Example 1</span></span>
```powershell
New-AzIpGroup -Name ipGroup -ResourceGroupName ipGroupRG -Location 'West US'
```

### <span data-ttu-id="fb641-109">範例 2</span><span class="sxs-lookup"><span data-stu-id="fb641-109">Example 2</span></span>
```powershell
New-AzIpGroup -Name ipGroup -ResourceGroupName ipGroupRG -Location 'West US' -IpAddress 10.0.0.0/24,11.9.0.0/24
```

## <span data-ttu-id="fb641-110">參數</span><span class="sxs-lookup"><span data-stu-id="fb641-110">PARAMETERS</span></span>

### <span data-ttu-id="fb641-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fb641-111">-AsJob</span></span>
<span data-ttu-id="fb641-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="fb641-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fb641-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb641-113">-DefaultProfile</span></span>
<span data-ttu-id="fb641-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="fb641-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb641-115">-強制</span><span class="sxs-lookup"><span data-stu-id="fb641-115">-Force</span></span>
<span data-ttu-id="fb641-116">如果您想要覆寫資源，請勿要求確認</span><span class="sxs-lookup"><span data-stu-id="fb641-116">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="fb641-117">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="fb641-117">-IpAddress</span></span>
<span data-ttu-id="fb641-118">在 IpGroup 中定義的 IpAddresses</span><span class="sxs-lookup"><span data-stu-id="fb641-118">IpAddresses defined in the IpGroup</span></span>

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

### <span data-ttu-id="fb641-119">-位置</span><span class="sxs-lookup"><span data-stu-id="fb641-119">-Location</span></span>
<span data-ttu-id="fb641-120">位置。</span><span class="sxs-lookup"><span data-stu-id="fb641-120">The location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb641-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="fb641-121">-Name</span></span>
<span data-ttu-id="fb641-122">ipgroup 的名稱。</span><span class="sxs-lookup"><span data-stu-id="fb641-122">The name of the ipgroup.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb641-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb641-123">-ResourceGroupName</span></span>
<span data-ttu-id="fb641-124">ipgroup 的資源組名。</span><span class="sxs-lookup"><span data-stu-id="fb641-124">The resource group name of the ipgroup.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb641-125">-標記</span><span class="sxs-lookup"><span data-stu-id="fb641-125">-Tag</span></span>
<span data-ttu-id="fb641-126">代表資源標記的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="fb641-126">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb641-127">-確認</span><span class="sxs-lookup"><span data-stu-id="fb641-127">-Confirm</span></span>
<span data-ttu-id="fb641-128">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="fb641-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb641-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb641-129">-WhatIf</span></span>
<span data-ttu-id="fb641-130">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="fb641-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb641-131">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fb641-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb641-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb641-132">CommonParameters</span></span>
<span data-ttu-id="fb641-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="fb641-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb641-134">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fb641-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb641-135">輸入</span><span class="sxs-lookup"><span data-stu-id="fb641-135">INPUTS</span></span>

### <span data-ttu-id="fb641-136">System.String</span><span class="sxs-lookup"><span data-stu-id="fb641-136">System.String</span></span>

### <span data-ttu-id="fb641-137">Microsoft.Azure.Commands.Network.models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="fb641-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="fb641-138">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="fb641-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="fb641-139">輸出</span><span class="sxs-lookup"><span data-stu-id="fb641-139">OUTPUTS</span></span>

### <span data-ttu-id="fb641-140">Microsoft.Azure.Commands.Network.models.PSIpGroup</span><span class="sxs-lookup"><span data-stu-id="fb641-140">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span></span>

## <span data-ttu-id="fb641-141">筆記</span><span class="sxs-lookup"><span data-stu-id="fb641-141">NOTES</span></span>

## <span data-ttu-id="fb641-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="fb641-142">RELATED LINKS</span></span>
