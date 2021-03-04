---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azvirtualrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualRouter.md
ms.openlocfilehash: 6def67720ee11a2057267845ef458d0759aec589
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915938"
---
# <span data-ttu-id="a9414-101">Remove-AzVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="a9414-101">Remove-AzVirtualRouter</span></span>

## <span data-ttu-id="a9414-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a9414-102">SYNOPSIS</span></span>
<span data-ttu-id="a9414-103">刪除 Azure VirtualRouter。</span><span class="sxs-lookup"><span data-stu-id="a9414-103">Deletes an Azure VirtualRouter.</span></span>

## <span data-ttu-id="a9414-104">語法</span><span class="sxs-lookup"><span data-stu-id="a9414-104">SYNTAX</span></span>

### <span data-ttu-id="a9414-105">VirtualRouterNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="a9414-105">VirtualRouterNameParameterSet (Default)</span></span>
```
Remove-AzVirtualRouter -ResourceGroupName <String> -RouterName <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9414-106">VirtualRouterInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a9414-106">VirtualRouterInputObjectParameterSet</span></span>
```
Remove-AzVirtualRouter -InputObject <PSVirtualRouter> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9414-107">VirtualRouterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a9414-107">VirtualRouterResourceIdParameterSet</span></span>
```
Remove-AzVirtualRouter -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9414-108">描述</span><span class="sxs-lookup"><span data-stu-id="a9414-108">DESCRIPTION</span></span>
<span data-ttu-id="a9414-109">**Remove-AzVirtualRouter** Cmdlet 會刪除 Azure VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="a9414-109">The **Remove-AzVirtualRouter** cmdlet deletes an Azure VirtualRouter</span></span>

## <span data-ttu-id="a9414-110">例子</span><span class="sxs-lookup"><span data-stu-id="a9414-110">EXAMPLES</span></span>

### <span data-ttu-id="a9414-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="a9414-111">Example 1</span></span>
```powershell
Remove-AzVirtualRouter -ResourceGroupName virtualRouterRG -RouterName virtualRouter
```

### <span data-ttu-id="a9414-112">範例 2</span><span class="sxs-lookup"><span data-stu-id="a9414-112">Example 2</span></span>
```powershell
$virtualRouterId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/virtualRouter'
Remove-AzVirtualRouter -ResourceId $virtualRouterId
```

### <span data-ttu-id="a9414-113">範例 3</span><span class="sxs-lookup"><span data-stu-id="a9414-113">Example 3</span></span>
```powershell
$virtualRouter = Get-AzVirtualRouter -ResourceGroupName virtualRouterRG -RouterName virtualRouter
Remove-AzVirtualRouter -InputObject $virtualRouter
```

## <span data-ttu-id="a9414-114">參數</span><span class="sxs-lookup"><span data-stu-id="a9414-114">PARAMETERS</span></span>

### <span data-ttu-id="a9414-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a9414-115">-AsJob</span></span>
<span data-ttu-id="a9414-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="a9414-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a9414-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9414-117">-DefaultProfile</span></span>
<span data-ttu-id="a9414-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a9414-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9414-119">-強制</span><span class="sxs-lookup"><span data-stu-id="a9414-119">-Force</span></span>
<span data-ttu-id="a9414-120">如果您想要覆寫資源，請勿要求確認</span><span class="sxs-lookup"><span data-stu-id="a9414-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="a9414-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a9414-121">-InputObject</span></span>
<span data-ttu-id="a9414-122">虛擬路由器輸入物件。</span><span class="sxs-lookup"><span data-stu-id="a9414-122">The virtual router input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualRouter
Parameter Sets: VirtualRouterInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a9414-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a9414-123">-PassThru</span></span>
<span data-ttu-id="a9414-124">會返回代表執行此作業之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="a9414-124">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="a9414-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9414-125">-ResourceGroupName</span></span>
<span data-ttu-id="a9414-126">虛擬路由器的資源組名。</span><span class="sxs-lookup"><span data-stu-id="a9414-126">The resource group name of the virtual router.</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9414-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a9414-127">-ResourceId</span></span>
<span data-ttu-id="a9414-128">虛擬路由器資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="a9414-128">The virtual router resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9414-129">-RouterName</span><span class="sxs-lookup"><span data-stu-id="a9414-129">-RouterName</span></span>
<span data-ttu-id="a9414-130">虛擬路由器的名稱。</span><span class="sxs-lookup"><span data-stu-id="a9414-130">The name of the virtual router.</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9414-131">-確認</span><span class="sxs-lookup"><span data-stu-id="a9414-131">-Confirm</span></span>
<span data-ttu-id="a9414-132">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="a9414-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9414-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9414-133">-WhatIf</span></span>
<span data-ttu-id="a9414-134">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a9414-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9414-135">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a9414-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9414-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9414-136">CommonParameters</span></span>
<span data-ttu-id="a9414-137">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a9414-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9414-138">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a9414-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9414-139">輸入</span><span class="sxs-lookup"><span data-stu-id="a9414-139">INPUTS</span></span>

### <span data-ttu-id="a9414-140">System.String</span><span class="sxs-lookup"><span data-stu-id="a9414-140">System.String</span></span>

### <span data-ttu-id="a9414-141">Microsoft.Azure.Commands.Network.models.PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="a9414-141">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="a9414-142">輸出</span><span class="sxs-lookup"><span data-stu-id="a9414-142">OUTPUTS</span></span>

### <span data-ttu-id="a9414-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a9414-143">System.Boolean</span></span>

## <span data-ttu-id="a9414-144">筆記</span><span class="sxs-lookup"><span data-stu-id="a9414-144">NOTES</span></span>

## <span data-ttu-id="a9414-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="a9414-145">RELATED LINKS</span></span>
