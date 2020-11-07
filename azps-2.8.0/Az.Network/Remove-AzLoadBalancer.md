---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 31B0FBEF-366A-41AF-9182-2EB087019F36
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancer.md
ms.openlocfilehash: b91a807d5499236d45e84a9a064e7f64daa1fb57
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93789142"
---
# <span data-ttu-id="fa19a-101">Remove-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="fa19a-101">Remove-AzLoadBalancer</span></span>

## <span data-ttu-id="fa19a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fa19a-102">SYNOPSIS</span></span>
<span data-ttu-id="fa19a-103">移除負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="fa19a-103">Removes a load balancer.</span></span>

## <span data-ttu-id="fa19a-104">句法</span><span class="sxs-lookup"><span data-stu-id="fa19a-104">SYNTAX</span></span>

```
Remove-AzLoadBalancer -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fa19a-105">說明</span><span class="sxs-lookup"><span data-stu-id="fa19a-105">DESCRIPTION</span></span>
<span data-ttu-id="fa19a-106">**AzLoadBalancer** Cmdlet 會移除 Azure 負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="fa19a-106">The **Remove-AzLoadBalancer** cmdlet removes an Azure load balancer.</span></span>

## <span data-ttu-id="fa19a-107">示例</span><span class="sxs-lookup"><span data-stu-id="fa19a-107">EXAMPLES</span></span>

### <span data-ttu-id="fa19a-108">範例1：移除負載平衡器</span><span class="sxs-lookup"><span data-stu-id="fa19a-108">Example 1: Remove a load balancer</span></span>
```
PS C:\>Remove-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="fa19a-109">這個命令會刪除名為 MyResourceGroup 的資源群組中名為 MyLoadBalancer 的負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="fa19a-109">This command deletes a load balancer named MyLoadBalancer in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="fa19a-110">參數</span><span class="sxs-lookup"><span data-stu-id="fa19a-110">PARAMETERS</span></span>

### <span data-ttu-id="fa19a-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fa19a-111">-AsJob</span></span>
<span data-ttu-id="fa19a-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="fa19a-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fa19a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa19a-113">-DefaultProfile</span></span>
<span data-ttu-id="fa19a-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="fa19a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fa19a-115">-Force</span><span class="sxs-lookup"><span data-stu-id="fa19a-115">-Force</span></span>
<span data-ttu-id="fa19a-116">指示此 Cmdlet 會移除負載平衡器，不論是否已將資源指派給它。</span><span class="sxs-lookup"><span data-stu-id="fa19a-116">Indicates that this cmdlet removes the load balancer regardless of whether resources are assigned to it.</span></span>

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

### <span data-ttu-id="fa19a-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="fa19a-117">-Name</span></span>
<span data-ttu-id="fa19a-118">指定要移除的負載平衡器的名稱。</span><span class="sxs-lookup"><span data-stu-id="fa19a-118">Specifies the name of the load balancer to remove.</span></span>

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

### <span data-ttu-id="fa19a-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fa19a-119">-PassThru</span></span>
<span data-ttu-id="fa19a-120">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="fa19a-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="fa19a-121">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="fa19a-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="fa19a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa19a-122">-ResourceGroupName</span></span>
<span data-ttu-id="fa19a-123">指定包含要移除之負載等化器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="fa19a-123">Specifies the name of the resource group that contains the load balancer to remove.</span></span>

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

### <span data-ttu-id="fa19a-124">-確認</span><span class="sxs-lookup"><span data-stu-id="fa19a-124">-Confirm</span></span>
<span data-ttu-id="fa19a-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="fa19a-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa19a-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa19a-126">-WhatIf</span></span>
<span data-ttu-id="fa19a-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="fa19a-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa19a-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fa19a-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa19a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa19a-129">CommonParameters</span></span>
<span data-ttu-id="fa19a-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fa19a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa19a-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="fa19a-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa19a-132">輸入</span><span class="sxs-lookup"><span data-stu-id="fa19a-132">INPUTS</span></span>

### <span data-ttu-id="fa19a-133">System.object</span><span class="sxs-lookup"><span data-stu-id="fa19a-133">System.String</span></span>

## <span data-ttu-id="fa19a-134">輸出</span><span class="sxs-lookup"><span data-stu-id="fa19a-134">OUTPUTS</span></span>

### <span data-ttu-id="fa19a-135">System.object</span><span class="sxs-lookup"><span data-stu-id="fa19a-135">System.Boolean</span></span>

## <span data-ttu-id="fa19a-136">筆記</span><span class="sxs-lookup"><span data-stu-id="fa19a-136">NOTES</span></span>

## <span data-ttu-id="fa19a-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="fa19a-137">RELATED LINKS</span></span>

[<span data-ttu-id="fa19a-138">AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="fa19a-138">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="fa19a-139">新-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="fa19a-139">New-AzLoadBalancer</span></span>](./New-AzLoadBalancer.md)

[<span data-ttu-id="fa19a-140">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="fa19a-140">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)


