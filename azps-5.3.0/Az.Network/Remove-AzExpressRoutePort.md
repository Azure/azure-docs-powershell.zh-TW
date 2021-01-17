---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRoutePort.md
ms.openlocfilehash: 7e6ee711de551de00a54930be2bdb285998e3ccb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98437579"
---
# <span data-ttu-id="7c9a7-101">Remove-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="7c9a7-101">Remove-AzExpressRoutePort</span></span>

## <span data-ttu-id="7c9a7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7c9a7-102">SYNOPSIS</span></span>
<span data-ttu-id="7c9a7-103">移除 ExpressRoutePort。</span><span class="sxs-lookup"><span data-stu-id="7c9a7-103">Removes an ExpressRoutePort.</span></span>

## <span data-ttu-id="7c9a7-104">句法</span><span class="sxs-lookup"><span data-stu-id="7c9a7-104">SYNTAX</span></span>

### <span data-ttu-id="7c9a7-105">ResourceNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="7c9a7-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzExpressRoutePort -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c9a7-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7c9a7-106">InputObjectParameterSet</span></span>
```
Remove-AzExpressRoutePort -InputObject <PSExpressRoutePort> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c9a7-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7c9a7-107">ResourceIdParameterSet</span></span>
```
Remove-AzExpressRoutePort -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c9a7-108">說明</span><span class="sxs-lookup"><span data-stu-id="7c9a7-108">DESCRIPTION</span></span>
<span data-ttu-id="7c9a7-109">**AzExpressRoutePort** Cmdlet 會移除 ExpressRoutePort。</span><span class="sxs-lookup"><span data-stu-id="7c9a7-109">The **Remove-AzExpressRoutePort** cmdlet removes an ExpressRoutePort.</span></span>

## <span data-ttu-id="7c9a7-110">示例</span><span class="sxs-lookup"><span data-stu-id="7c9a7-110">EXAMPLES</span></span>

### <span data-ttu-id="7c9a7-111">範例1</span><span class="sxs-lookup"><span data-stu-id="7c9a7-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
```

<span data-ttu-id="7c9a7-112">移除訂閱中 $rg 資源群組中的 $PortName ExpressRoutePort 資源。</span><span class="sxs-lookup"><span data-stu-id="7c9a7-112">Removes $PortName ExpressRoutePort resource in $rg resource group in your subscription.</span></span>

### <span data-ttu-id="7c9a7-113">範例2</span><span class="sxs-lookup"><span data-stu-id="7c9a7-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzExpressRoutePort -InputObject $erPort
```

<span data-ttu-id="7c9a7-114">移除 InputObject 中的 ExpressRoutePort 資源。</span><span class="sxs-lookup"><span data-stu-id="7c9a7-114">Removes the ExpressRoutePort resource in InputObject.</span></span>

### <span data-ttu-id="7c9a7-115">範例3</span><span class="sxs-lookup"><span data-stu-id="7c9a7-115">Example 3</span></span>
```powershell
PS C:\> Remove-AzExpressRoutePort -Name $ResourceId $id
```

<span data-ttu-id="7c9a7-116">移除 ResourceId $id 的 ExpressRoutePort 資源。</span><span class="sxs-lookup"><span data-stu-id="7c9a7-116">Removes the ExpressRoutePort resource with ResourceId $id.</span></span>

## <span data-ttu-id="7c9a7-117">參數</span><span class="sxs-lookup"><span data-stu-id="7c9a7-117">PARAMETERS</span></span>

### <span data-ttu-id="7c9a7-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7c9a7-118">-AsJob</span></span>
<span data-ttu-id="7c9a7-119">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="7c9a7-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7c9a7-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c9a7-120">-DefaultProfile</span></span>
<span data-ttu-id="7c9a7-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7c9a7-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c9a7-122">-Force</span><span class="sxs-lookup"><span data-stu-id="7c9a7-122">-Force</span></span>
<span data-ttu-id="7c9a7-123">如果您想要刪除資源，請不要要求確認</span><span class="sxs-lookup"><span data-stu-id="7c9a7-123">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="7c9a7-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7c9a7-124">-InputObject</span></span>
<span data-ttu-id="7c9a7-125">快速路由埠物件</span><span class="sxs-lookup"><span data-stu-id="7c9a7-125">The express route port object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7c9a7-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="7c9a7-126">-Name</span></span>
<span data-ttu-id="7c9a7-127">ExpressRoutePort 的名稱。</span><span class="sxs-lookup"><span data-stu-id="7c9a7-127">The name of the ExpressRoutePort.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c9a7-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7c9a7-128">-PassThru</span></span>
<span data-ttu-id="7c9a7-129">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="7c9a7-129">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="7c9a7-130">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="7c9a7-130">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="7c9a7-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c9a7-131">-ResourceGroupName</span></span>
<span data-ttu-id="7c9a7-132">ExpressRoutePort 的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="7c9a7-132">The resource group name of the ExpressRoutePort.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c9a7-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7c9a7-133">-ResourceId</span></span>
<span data-ttu-id="7c9a7-134">快速路由埠的 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="7c9a7-134">ResourceId of the express route port.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c9a7-135">-確認</span><span class="sxs-lookup"><span data-stu-id="7c9a7-135">-Confirm</span></span>
<span data-ttu-id="7c9a7-136">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7c9a7-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c9a7-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c9a7-137">-WhatIf</span></span>
<span data-ttu-id="7c9a7-138">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7c9a7-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c9a7-139">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7c9a7-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c9a7-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c9a7-140">CommonParameters</span></span>
<span data-ttu-id="7c9a7-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7c9a7-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c9a7-142">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7c9a7-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c9a7-143">輸入</span><span class="sxs-lookup"><span data-stu-id="7c9a7-143">INPUTS</span></span>

### <span data-ttu-id="7c9a7-144">PSExpressRoutePort 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="7c9a7-144">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

### <span data-ttu-id="7c9a7-145">System.object</span><span class="sxs-lookup"><span data-stu-id="7c9a7-145">System.String</span></span>

## <span data-ttu-id="7c9a7-146">輸出</span><span class="sxs-lookup"><span data-stu-id="7c9a7-146">OUTPUTS</span></span>

### <span data-ttu-id="7c9a7-147">System.object</span><span class="sxs-lookup"><span data-stu-id="7c9a7-147">System.Boolean</span></span>

## <span data-ttu-id="7c9a7-148">筆記</span><span class="sxs-lookup"><span data-stu-id="7c9a7-148">NOTES</span></span>

## <span data-ttu-id="7c9a7-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="7c9a7-149">RELATED LINKS</span></span>

[<span data-ttu-id="7c9a7-150">AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="7c9a7-150">Get-AzExpressRoutePort</span></span>](./Get-AzExpressRoutePort.md)

[<span data-ttu-id="7c9a7-151">新-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="7c9a7-151">New-AzExpressRoutePort</span></span>](./New-AzExpressRoutePort.md)

[<span data-ttu-id="7c9a7-152">Set-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="7c9a7-152">Set-AzExpressRoutePort</span></span>](./Set-AzExpressRoutePort.md)
