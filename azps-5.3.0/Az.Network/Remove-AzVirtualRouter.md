---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualRouter.md
ms.openlocfilehash: 691abfe3f6ca58e1fbef6c1120ce13b64fd62566
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98288647"
---
# <span data-ttu-id="95dfe-101">Remove-AzVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="95dfe-101">Remove-AzVirtualRouter</span></span>

## <span data-ttu-id="95dfe-102">摘要</span><span class="sxs-lookup"><span data-stu-id="95dfe-102">SYNOPSIS</span></span>
<span data-ttu-id="95dfe-103">刪除 Azure VirtualRouter。</span><span class="sxs-lookup"><span data-stu-id="95dfe-103">Deletes an Azure VirtualRouter.</span></span>

## <span data-ttu-id="95dfe-104">句法</span><span class="sxs-lookup"><span data-stu-id="95dfe-104">SYNTAX</span></span>

### <span data-ttu-id="95dfe-105">VirtualRouterNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="95dfe-105">VirtualRouterNameParameterSet (Default)</span></span>
```
Remove-AzVirtualRouter -ResourceGroupName <String> -RouterName <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="95dfe-106">VirtualRouterInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="95dfe-106">VirtualRouterInputObjectParameterSet</span></span>
```
Remove-AzVirtualRouter -InputObject <PSVirtualRouter> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="95dfe-107">VirtualRouterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="95dfe-107">VirtualRouterResourceIdParameterSet</span></span>
```
Remove-AzVirtualRouter -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95dfe-108">說明</span><span class="sxs-lookup"><span data-stu-id="95dfe-108">DESCRIPTION</span></span>
<span data-ttu-id="95dfe-109">**AzVirtualRouter** Cmdlet 會刪除 Azure VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="95dfe-109">The **Remove-AzVirtualRouter** cmdlet deletes an Azure VirtualRouter</span></span>

## <span data-ttu-id="95dfe-110">示例</span><span class="sxs-lookup"><span data-stu-id="95dfe-110">EXAMPLES</span></span>

### <span data-ttu-id="95dfe-111">範例1</span><span class="sxs-lookup"><span data-stu-id="95dfe-111">Example 1</span></span>
```powershell
Remove-AzVirtualRouter -ResourceGroupName virtualRouterRG -RouterName virtualRouter
```

### <span data-ttu-id="95dfe-112">範例2</span><span class="sxs-lookup"><span data-stu-id="95dfe-112">Example 2</span></span>
```powershell
$virtualRouterId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/virtualRouter'
Remove-AzVirtualRouter -ResourceId $virtualRouterId
```

### <span data-ttu-id="95dfe-113">範例3</span><span class="sxs-lookup"><span data-stu-id="95dfe-113">Example 3</span></span>
```powershell
$virtualRouter = Get-AzVirtualRouter -ResourceGroupName virtualRouterRG -RouterName virtualRouter
Remove-AzVirtualRouter -InputObject $virtualRouter
```

## <span data-ttu-id="95dfe-114">參數</span><span class="sxs-lookup"><span data-stu-id="95dfe-114">PARAMETERS</span></span>

### <span data-ttu-id="95dfe-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="95dfe-115">-AsJob</span></span>
<span data-ttu-id="95dfe-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="95dfe-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="95dfe-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95dfe-117">-DefaultProfile</span></span>
<span data-ttu-id="95dfe-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="95dfe-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="95dfe-119">-Force</span><span class="sxs-lookup"><span data-stu-id="95dfe-119">-Force</span></span>
<span data-ttu-id="95dfe-120">若要覆寫資源，請不要要求確認</span><span class="sxs-lookup"><span data-stu-id="95dfe-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="95dfe-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="95dfe-121">-InputObject</span></span>
<span data-ttu-id="95dfe-122">虛擬路由器輸入物件。</span><span class="sxs-lookup"><span data-stu-id="95dfe-122">The virtual router input object.</span></span>

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

### <span data-ttu-id="95dfe-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="95dfe-123">-PassThru</span></span>
<span data-ttu-id="95dfe-124">傳回代表執行此作業之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="95dfe-124">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="95dfe-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95dfe-125">-ResourceGroupName</span></span>
<span data-ttu-id="95dfe-126">虛擬路由器的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="95dfe-126">The resource group name of the virtual router.</span></span>

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

### <span data-ttu-id="95dfe-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="95dfe-127">-ResourceId</span></span>
<span data-ttu-id="95dfe-128">虛擬路由器資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="95dfe-128">The virtual router resource Id.</span></span>

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

### <span data-ttu-id="95dfe-129">-RouterName</span><span class="sxs-lookup"><span data-stu-id="95dfe-129">-RouterName</span></span>
<span data-ttu-id="95dfe-130">虛擬路由器的名稱。</span><span class="sxs-lookup"><span data-stu-id="95dfe-130">The name of the virtual router.</span></span>

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

### <span data-ttu-id="95dfe-131">-確認</span><span class="sxs-lookup"><span data-stu-id="95dfe-131">-Confirm</span></span>
<span data-ttu-id="95dfe-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="95dfe-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95dfe-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95dfe-133">-WhatIf</span></span>
<span data-ttu-id="95dfe-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="95dfe-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="95dfe-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="95dfe-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95dfe-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95dfe-136">CommonParameters</span></span>
<span data-ttu-id="95dfe-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="95dfe-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95dfe-138">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="95dfe-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95dfe-139">輸入</span><span class="sxs-lookup"><span data-stu-id="95dfe-139">INPUTS</span></span>

### <span data-ttu-id="95dfe-140">System.object</span><span class="sxs-lookup"><span data-stu-id="95dfe-140">System.String</span></span>

### <span data-ttu-id="95dfe-141">PSVirtualRouter 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="95dfe-141">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="95dfe-142">輸出</span><span class="sxs-lookup"><span data-stu-id="95dfe-142">OUTPUTS</span></span>

### <span data-ttu-id="95dfe-143">System.object</span><span class="sxs-lookup"><span data-stu-id="95dfe-143">System.Boolean</span></span>

## <span data-ttu-id="95dfe-144">筆記</span><span class="sxs-lookup"><span data-stu-id="95dfe-144">NOTES</span></span>

## <span data-ttu-id="95dfe-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="95dfe-145">RELATED LINKS</span></span>
