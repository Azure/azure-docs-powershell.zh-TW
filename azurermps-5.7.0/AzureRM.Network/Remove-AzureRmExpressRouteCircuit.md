---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: EDB94194-650C-4892-8DDC-E67D435522DD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmExpressRouteCircuit.md
ms.openlocfilehash: 3ea8e43710d9e195218cc1b96a2656af2a7e2adf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447037"
---
# <span data-ttu-id="74eee-101">Remove-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="74eee-101">Remove-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="74eee-102">摘要</span><span class="sxs-lookup"><span data-stu-id="74eee-102">SYNOPSIS</span></span>
<span data-ttu-id="74eee-103">移除 ExpressRoute 回路。</span><span class="sxs-lookup"><span data-stu-id="74eee-103">Removes an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="74eee-104">句法</span><span class="sxs-lookup"><span data-stu-id="74eee-104">SYNTAX</span></span>

```
Remove-AzureRmExpressRouteCircuit -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74eee-105">說明</span><span class="sxs-lookup"><span data-stu-id="74eee-105">DESCRIPTION</span></span>
<span data-ttu-id="74eee-106">**AzureRmExpressRouteCircuit** Cmdlet 會移除 ExpressRoute 回路。</span><span class="sxs-lookup"><span data-stu-id="74eee-106">The **Remove-AzureRmExpressRouteCircuit** cmdlet removes an ExpressRoute circuit.</span></span>

## <span data-ttu-id="74eee-107">示例</span><span class="sxs-lookup"><span data-stu-id="74eee-107">EXAMPLES</span></span>

### <span data-ttu-id="74eee-108">範例1：刪除 ExpressRoute 回路</span><span class="sxs-lookup"><span data-stu-id="74eee-108">Example 1: Delete an ExpressRoute circuit</span></span>
```
Remove-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
```

### <span data-ttu-id="74eee-109">範例2：使用管線刪除 ExpressRoute 電路</span><span class="sxs-lookup"><span data-stu-id="74eee-109">Example 2: Delete an ExpressRoute circuit using the pipeline</span></span>
```
Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg | Remove-AzureRmExpressRouteCircuit
```

## <span data-ttu-id="74eee-110">參數</span><span class="sxs-lookup"><span data-stu-id="74eee-110">PARAMETERS</span></span>

### <span data-ttu-id="74eee-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="74eee-111">-AsJob</span></span>
<span data-ttu-id="74eee-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="74eee-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="74eee-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74eee-113">-DefaultProfile</span></span>
<span data-ttu-id="74eee-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="74eee-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74eee-115">-Force</span><span class="sxs-lookup"><span data-stu-id="74eee-115">-Force</span></span>
<span data-ttu-id="74eee-116">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="74eee-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="74eee-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="74eee-117">-Name</span></span>
<span data-ttu-id="74eee-118">要移除的 ExpressRoute 電路名稱。</span><span class="sxs-lookup"><span data-stu-id="74eee-118">The name of the ExpressRoute circuit to be removed.</span></span>

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

### <span data-ttu-id="74eee-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="74eee-119">-PassThru</span></span>
<span data-ttu-id="74eee-120">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="74eee-120">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="74eee-121">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="74eee-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="74eee-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74eee-122">-ResourceGroupName</span></span>
<span data-ttu-id="74eee-123">指定此 ExpressRoute 線路所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="74eee-123">Specifies the name of the resource group that this ExpressRoute circuit belongs to.</span></span>

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

### <span data-ttu-id="74eee-124">-確認</span><span class="sxs-lookup"><span data-stu-id="74eee-124">-Confirm</span></span>
<span data-ttu-id="74eee-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="74eee-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74eee-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74eee-126">-WhatIf</span></span>
<span data-ttu-id="74eee-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="74eee-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74eee-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="74eee-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74eee-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74eee-129">CommonParameters</span></span>
<span data-ttu-id="74eee-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="74eee-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74eee-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="74eee-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74eee-132">輸入</span><span class="sxs-lookup"><span data-stu-id="74eee-132">INPUTS</span></span>

### <span data-ttu-id="74eee-133">所有</span><span class="sxs-lookup"><span data-stu-id="74eee-133">None</span></span>
<span data-ttu-id="74eee-134">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="74eee-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="74eee-135">輸出</span><span class="sxs-lookup"><span data-stu-id="74eee-135">OUTPUTS</span></span>

## <span data-ttu-id="74eee-136">筆記</span><span class="sxs-lookup"><span data-stu-id="74eee-136">NOTES</span></span>

## <span data-ttu-id="74eee-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="74eee-137">RELATED LINKS</span></span>

[<span data-ttu-id="74eee-138">AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="74eee-138">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="74eee-139">移動流覽 AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="74eee-139">Move-AzureRmExpressRouteCircuit</span></span>](Move-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="74eee-140">新-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="74eee-140">New-AzureRmExpressRouteCircuit</span></span>](New-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="74eee-141">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="74eee-141">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)
