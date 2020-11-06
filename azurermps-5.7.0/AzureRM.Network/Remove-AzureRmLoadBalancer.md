---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 31B0FBEF-366A-41AF-9182-2EB087019F36
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancer.md
ms.openlocfilehash: 13ece8d5bb6ec42e59f6a44910d3a3d46dd9d844
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447034"
---
# <span data-ttu-id="d2f43-101">Remove-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d2f43-101">Remove-AzureRmLoadBalancer</span></span>

## <span data-ttu-id="d2f43-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d2f43-102">SYNOPSIS</span></span>
<span data-ttu-id="d2f43-103">移除負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="d2f43-103">Removes a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d2f43-104">句法</span><span class="sxs-lookup"><span data-stu-id="d2f43-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancer -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2f43-105">說明</span><span class="sxs-lookup"><span data-stu-id="d2f43-105">DESCRIPTION</span></span>
<span data-ttu-id="d2f43-106">**AzureRmLoadBalancer** Cmdlet 會移除 Azure 負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="d2f43-106">The **Remove-AzureRmLoadBalancer** cmdlet removes an Azure load balancer.</span></span>

## <span data-ttu-id="d2f43-107">示例</span><span class="sxs-lookup"><span data-stu-id="d2f43-107">EXAMPLES</span></span>

### <span data-ttu-id="d2f43-108">範例1：移除負載平衡器</span><span class="sxs-lookup"><span data-stu-id="d2f43-108">Example 1: Remove a load balancer</span></span>
```
PS C:\>Remove-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="d2f43-109">這個命令會刪除名為 MyResourceGroup 的資源群組中名為 MyLoadBalancer 的負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="d2f43-109">This command deletes a load balancer named MyLoadBalancer in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="d2f43-110">參數</span><span class="sxs-lookup"><span data-stu-id="d2f43-110">PARAMETERS</span></span>

### <span data-ttu-id="d2f43-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d2f43-111">-AsJob</span></span>
<span data-ttu-id="d2f43-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="d2f43-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d2f43-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2f43-113">-DefaultProfile</span></span>
<span data-ttu-id="d2f43-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d2f43-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d2f43-115">-Force</span><span class="sxs-lookup"><span data-stu-id="d2f43-115">-Force</span></span>
<span data-ttu-id="d2f43-116">指示此 Cmdlet 會移除負載平衡器，不論是否已將資源指派給它。</span><span class="sxs-lookup"><span data-stu-id="d2f43-116">Indicates that this cmdlet removes the load balancer regardless of whether resources are assigned to it.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2f43-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="d2f43-117">-Name</span></span>
<span data-ttu-id="d2f43-118">指定要移除的負載平衡器的名稱。</span><span class="sxs-lookup"><span data-stu-id="d2f43-118">Specifies the name of the load balancer to remove.</span></span>

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

### <span data-ttu-id="d2f43-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d2f43-119">-PassThru</span></span>
<span data-ttu-id="d2f43-120">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="d2f43-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d2f43-121">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="d2f43-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d2f43-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2f43-122">-ResourceGroupName</span></span>
<span data-ttu-id="d2f43-123">指定包含要移除之負載等化器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d2f43-123">Specifies the name of the resource group that contains the load balancer to remove.</span></span>

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

### <span data-ttu-id="d2f43-124">-確認</span><span class="sxs-lookup"><span data-stu-id="d2f43-124">-Confirm</span></span>
<span data-ttu-id="d2f43-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d2f43-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2f43-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2f43-126">-WhatIf</span></span>
<span data-ttu-id="d2f43-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d2f43-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2f43-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d2f43-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2f43-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2f43-129">CommonParameters</span></span>
<span data-ttu-id="d2f43-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d2f43-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2f43-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d2f43-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2f43-132">輸入</span><span class="sxs-lookup"><span data-stu-id="d2f43-132">INPUTS</span></span>

### <span data-ttu-id="d2f43-133">所有</span><span class="sxs-lookup"><span data-stu-id="d2f43-133">None</span></span>
<span data-ttu-id="d2f43-134">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="d2f43-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d2f43-135">輸出</span><span class="sxs-lookup"><span data-stu-id="d2f43-135">OUTPUTS</span></span>

## <span data-ttu-id="d2f43-136">筆記</span><span class="sxs-lookup"><span data-stu-id="d2f43-136">NOTES</span></span>

## <span data-ttu-id="d2f43-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="d2f43-137">RELATED LINKS</span></span>

[<span data-ttu-id="d2f43-138">AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d2f43-138">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="d2f43-139">新-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d2f43-139">New-AzureRmLoadBalancer</span></span>](./New-AzureRmLoadBalancer.md)

[<span data-ttu-id="d2f43-140">Set-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d2f43-140">Set-AzureRmLoadBalancer</span></span>](./Set-AzureRmLoadBalancer.md)

