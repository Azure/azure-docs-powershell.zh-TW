---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 31B0FBEF-366A-41AF-9182-2EB087019F36
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancer.md
ms.openlocfilehash: efe24ad1feae60ed71bd65206c52cfbf0b27df18
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913422"
---
# <span data-ttu-id="010a1-101">Remove-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="010a1-101">Remove-AzLoadBalancer</span></span>

## <span data-ttu-id="010a1-102">簡介</span><span class="sxs-lookup"><span data-stu-id="010a1-102">SYNOPSIS</span></span>
<span data-ttu-id="010a1-103">移除負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="010a1-103">Removes a load balancer.</span></span>

## <span data-ttu-id="010a1-104">語法</span><span class="sxs-lookup"><span data-stu-id="010a1-104">SYNTAX</span></span>

```
Remove-AzLoadBalancer -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="010a1-105">描述</span><span class="sxs-lookup"><span data-stu-id="010a1-105">DESCRIPTION</span></span>
<span data-ttu-id="010a1-106">**Remove-AzLoadBalancer** Cmdlet 會移除 Azure 負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="010a1-106">The **Remove-AzLoadBalancer** cmdlet removes an Azure load balancer.</span></span>

## <span data-ttu-id="010a1-107">例子</span><span class="sxs-lookup"><span data-stu-id="010a1-107">EXAMPLES</span></span>

### <span data-ttu-id="010a1-108">範例 1：移除負載平衡器</span><span class="sxs-lookup"><span data-stu-id="010a1-108">Example 1: Remove a load balancer</span></span>
```
PS C:\>Remove-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="010a1-109">此命令會刪除名為 MyResourceGroup 的資源群組中名為 MyLoadBalancer 的負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="010a1-109">This command deletes a load balancer named MyLoadBalancer in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="010a1-110">參數</span><span class="sxs-lookup"><span data-stu-id="010a1-110">PARAMETERS</span></span>

### <span data-ttu-id="010a1-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="010a1-111">-AsJob</span></span>
<span data-ttu-id="010a1-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="010a1-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="010a1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="010a1-113">-DefaultProfile</span></span>
<span data-ttu-id="010a1-114">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="010a1-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="010a1-115">-強制</span><span class="sxs-lookup"><span data-stu-id="010a1-115">-Force</span></span>
<span data-ttu-id="010a1-116">表示此 Cmdlet 會移除負載平衡器，無論資源是否指派給負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="010a1-116">Indicates that this cmdlet removes the load balancer regardless of whether resources are assigned to it.</span></span>

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

### <span data-ttu-id="010a1-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="010a1-117">-Name</span></span>
<span data-ttu-id="010a1-118">指定要移除的負載平衡器名稱。</span><span class="sxs-lookup"><span data-stu-id="010a1-118">Specifies the name of the load balancer to remove.</span></span>

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

### <span data-ttu-id="010a1-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="010a1-119">-PassThru</span></span>
<span data-ttu-id="010a1-120">會返回代表您處理之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="010a1-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="010a1-121">根據預設，此 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="010a1-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="010a1-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="010a1-122">-ResourceGroupName</span></span>
<span data-ttu-id="010a1-123">指定包含要移除之負載平衡器的資源組名。</span><span class="sxs-lookup"><span data-stu-id="010a1-123">Specifies the name of the resource group that contains the load balancer to remove.</span></span>

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

### <span data-ttu-id="010a1-124">-確認</span><span class="sxs-lookup"><span data-stu-id="010a1-124">-Confirm</span></span>
<span data-ttu-id="010a1-125">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="010a1-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="010a1-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="010a1-126">-WhatIf</span></span>
<span data-ttu-id="010a1-127">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="010a1-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="010a1-128">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="010a1-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="010a1-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="010a1-129">CommonParameters</span></span>
<span data-ttu-id="010a1-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="010a1-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="010a1-131">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="010a1-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="010a1-132">輸入</span><span class="sxs-lookup"><span data-stu-id="010a1-132">INPUTS</span></span>

### <span data-ttu-id="010a1-133">System.String</span><span class="sxs-lookup"><span data-stu-id="010a1-133">System.String</span></span>

## <span data-ttu-id="010a1-134">輸出</span><span class="sxs-lookup"><span data-stu-id="010a1-134">OUTPUTS</span></span>

### <span data-ttu-id="010a1-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="010a1-135">System.Boolean</span></span>

## <span data-ttu-id="010a1-136">筆記</span><span class="sxs-lookup"><span data-stu-id="010a1-136">NOTES</span></span>

## <span data-ttu-id="010a1-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="010a1-137">RELATED LINKS</span></span>

[<span data-ttu-id="010a1-138">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="010a1-138">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="010a1-139">New-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="010a1-139">New-AzLoadBalancer</span></span>](./New-AzLoadBalancer.md)

[<span data-ttu-id="010a1-140">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="010a1-140">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)


