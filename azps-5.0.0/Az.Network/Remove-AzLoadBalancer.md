---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 31B0FBEF-366A-41AF-9182-2EB087019F36
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancer.md
ms.openlocfilehash: 271033c39e049a423a15228968ad20c985b57036
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94137527"
---
# <span data-ttu-id="ebb94-101">Remove-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ebb94-101">Remove-AzLoadBalancer</span></span>

## <span data-ttu-id="ebb94-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ebb94-102">SYNOPSIS</span></span>
<span data-ttu-id="ebb94-103">移除負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="ebb94-103">Removes a load balancer.</span></span>

## <span data-ttu-id="ebb94-104">句法</span><span class="sxs-lookup"><span data-stu-id="ebb94-104">SYNTAX</span></span>

```
Remove-AzLoadBalancer -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ebb94-105">說明</span><span class="sxs-lookup"><span data-stu-id="ebb94-105">DESCRIPTION</span></span>
<span data-ttu-id="ebb94-106">**AzLoadBalancer** Cmdlet 會移除 Azure 負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="ebb94-106">The **Remove-AzLoadBalancer** cmdlet removes an Azure load balancer.</span></span>

## <span data-ttu-id="ebb94-107">示例</span><span class="sxs-lookup"><span data-stu-id="ebb94-107">EXAMPLES</span></span>

### <span data-ttu-id="ebb94-108">範例1：移除負載平衡器</span><span class="sxs-lookup"><span data-stu-id="ebb94-108">Example 1: Remove a load balancer</span></span>
```
PS C:\>Remove-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="ebb94-109">這個命令會刪除名為 MyResourceGroup 的資源群組中名為 MyLoadBalancer 的負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="ebb94-109">This command deletes a load balancer named MyLoadBalancer in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="ebb94-110">參數</span><span class="sxs-lookup"><span data-stu-id="ebb94-110">PARAMETERS</span></span>

### <span data-ttu-id="ebb94-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ebb94-111">-AsJob</span></span>
<span data-ttu-id="ebb94-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ebb94-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ebb94-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebb94-113">-DefaultProfile</span></span>
<span data-ttu-id="ebb94-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ebb94-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ebb94-115">-Force</span><span class="sxs-lookup"><span data-stu-id="ebb94-115">-Force</span></span>
<span data-ttu-id="ebb94-116">指示此 Cmdlet 會移除負載平衡器，不論是否已將資源指派給它。</span><span class="sxs-lookup"><span data-stu-id="ebb94-116">Indicates that this cmdlet removes the load balancer regardless of whether resources are assigned to it.</span></span>

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

### <span data-ttu-id="ebb94-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="ebb94-117">-Name</span></span>
<span data-ttu-id="ebb94-118">指定要移除的負載平衡器的名稱。</span><span class="sxs-lookup"><span data-stu-id="ebb94-118">Specifies the name of the load balancer to remove.</span></span>

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

### <span data-ttu-id="ebb94-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ebb94-119">-PassThru</span></span>
<span data-ttu-id="ebb94-120">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="ebb94-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ebb94-121">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="ebb94-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ebb94-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ebb94-122">-ResourceGroupName</span></span>
<span data-ttu-id="ebb94-123">指定包含要移除之負載等化器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ebb94-123">Specifies the name of the resource group that contains the load balancer to remove.</span></span>

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

### <span data-ttu-id="ebb94-124">-確認</span><span class="sxs-lookup"><span data-stu-id="ebb94-124">-Confirm</span></span>
<span data-ttu-id="ebb94-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ebb94-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ebb94-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ebb94-126">-WhatIf</span></span>
<span data-ttu-id="ebb94-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ebb94-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ebb94-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ebb94-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ebb94-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebb94-129">CommonParameters</span></span>
<span data-ttu-id="ebb94-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ebb94-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebb94-131">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ebb94-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebb94-132">輸入</span><span class="sxs-lookup"><span data-stu-id="ebb94-132">INPUTS</span></span>

### <span data-ttu-id="ebb94-133">System.object</span><span class="sxs-lookup"><span data-stu-id="ebb94-133">System.String</span></span>

## <span data-ttu-id="ebb94-134">輸出</span><span class="sxs-lookup"><span data-stu-id="ebb94-134">OUTPUTS</span></span>

### <span data-ttu-id="ebb94-135">System.object</span><span class="sxs-lookup"><span data-stu-id="ebb94-135">System.Boolean</span></span>

## <span data-ttu-id="ebb94-136">筆記</span><span class="sxs-lookup"><span data-stu-id="ebb94-136">NOTES</span></span>

## <span data-ttu-id="ebb94-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="ebb94-137">RELATED LINKS</span></span>

[<span data-ttu-id="ebb94-138">AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ebb94-138">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="ebb94-139">新-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ebb94-139">New-AzLoadBalancer</span></span>](./New-AzLoadBalancer.md)

[<span data-ttu-id="ebb94-140">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ebb94-140">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)


