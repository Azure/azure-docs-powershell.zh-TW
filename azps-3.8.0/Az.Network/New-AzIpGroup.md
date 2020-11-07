---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azipgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpGroup.md
ms.openlocfilehash: 6ae61090f98cbb9929cc5ad1b2745fbf88f21a2a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93957749"
---
# <span data-ttu-id="9ee48-101">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="9ee48-101">New-AzIpGroup</span></span>

## <span data-ttu-id="9ee48-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9ee48-102">SYNOPSIS</span></span>
<span data-ttu-id="9ee48-103">建立 Azure IpGroup。</span><span class="sxs-lookup"><span data-stu-id="9ee48-103">Creates an Azure IpGroup.</span></span>

## <span data-ttu-id="9ee48-104">句法</span><span class="sxs-lookup"><span data-stu-id="9ee48-104">SYNTAX</span></span>

```
New-AzIpGroup -Name <String> -ResourceGroupName <String> [-IpAddress <String[]>] -Location <String>
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9ee48-105">說明</span><span class="sxs-lookup"><span data-stu-id="9ee48-105">DESCRIPTION</span></span>
<span data-ttu-id="9ee48-106">**新的-AzIpGroup** Cmdlet 會建立 Azure IpGroup</span><span class="sxs-lookup"><span data-stu-id="9ee48-106">The **New-AzIpGroup** cmdlet creates an Azure IpGroup</span></span>

## <span data-ttu-id="9ee48-107">示例</span><span class="sxs-lookup"><span data-stu-id="9ee48-107">EXAMPLES</span></span>

### <span data-ttu-id="9ee48-108">範例1</span><span class="sxs-lookup"><span data-stu-id="9ee48-108">Example 1</span></span>
```powershell
New-AzIpGroup -Name ipGroup -ResourceGroupName ipGroupRG -Location 'West US'
```

### <span data-ttu-id="9ee48-109">範例2</span><span class="sxs-lookup"><span data-stu-id="9ee48-109">Example 2</span></span>
```powershell
New-AzIpGroup -Name ipGroup -ResourceGroupName ipGroupRG -Location 'West US' -IpAddress 10.0.0.0/24,11.9.0.0/24
```

## <span data-ttu-id="9ee48-110">參數</span><span class="sxs-lookup"><span data-stu-id="9ee48-110">PARAMETERS</span></span>

### <span data-ttu-id="9ee48-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9ee48-111">-AsJob</span></span>
<span data-ttu-id="9ee48-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="9ee48-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9ee48-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ee48-113">-DefaultProfile</span></span>
<span data-ttu-id="9ee48-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9ee48-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ee48-115">-Force</span><span class="sxs-lookup"><span data-stu-id="9ee48-115">-Force</span></span>
<span data-ttu-id="9ee48-116">若要覆寫資源，請不要要求確認</span><span class="sxs-lookup"><span data-stu-id="9ee48-116">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="9ee48-117">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="9ee48-117">-IpAddress</span></span>
<span data-ttu-id="9ee48-118">在 IpGroup 中定義的 IpAddresses</span><span class="sxs-lookup"><span data-stu-id="9ee48-118">IpAddresses defined in the IpGroup</span></span>

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

### <span data-ttu-id="9ee48-119">-位置</span><span class="sxs-lookup"><span data-stu-id="9ee48-119">-Location</span></span>
<span data-ttu-id="9ee48-120">位置。</span><span class="sxs-lookup"><span data-stu-id="9ee48-120">The location.</span></span>

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

### <span data-ttu-id="9ee48-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="9ee48-121">-Name</span></span>
<span data-ttu-id="9ee48-122">Ipgroup 的名稱。</span><span class="sxs-lookup"><span data-stu-id="9ee48-122">The name of the ipgroup.</span></span>

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

### <span data-ttu-id="9ee48-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ee48-123">-ResourceGroupName</span></span>
<span data-ttu-id="9ee48-124">Ipgroup 的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="9ee48-124">The resource group name of the ipgroup.</span></span>

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

### <span data-ttu-id="9ee48-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="9ee48-125">-Tag</span></span>
<span data-ttu-id="9ee48-126">代表資源標記的 hashtable。</span><span class="sxs-lookup"><span data-stu-id="9ee48-126">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="9ee48-127">-確認</span><span class="sxs-lookup"><span data-stu-id="9ee48-127">-Confirm</span></span>
<span data-ttu-id="9ee48-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9ee48-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ee48-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ee48-129">-WhatIf</span></span>
<span data-ttu-id="9ee48-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9ee48-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ee48-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9ee48-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ee48-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ee48-132">CommonParameters</span></span>
<span data-ttu-id="9ee48-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9ee48-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ee48-134">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="9ee48-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ee48-135">輸入</span><span class="sxs-lookup"><span data-stu-id="9ee48-135">INPUTS</span></span>

### <span data-ttu-id="9ee48-136">System.object</span><span class="sxs-lookup"><span data-stu-id="9ee48-136">System.String</span></span>

### <span data-ttu-id="9ee48-137">PSVirtualNetworkGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="9ee48-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="9ee48-138">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="9ee48-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="9ee48-139">輸出</span><span class="sxs-lookup"><span data-stu-id="9ee48-139">OUTPUTS</span></span>

### <span data-ttu-id="9ee48-140">PSIpGroup 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="9ee48-140">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span></span>

## <span data-ttu-id="9ee48-141">筆記</span><span class="sxs-lookup"><span data-stu-id="9ee48-141">NOTES</span></span>

## <span data-ttu-id="9ee48-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="9ee48-142">RELATED LINKS</span></span>
