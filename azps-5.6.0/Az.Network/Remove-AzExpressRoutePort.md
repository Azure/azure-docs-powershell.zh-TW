---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRoutePort.md
ms.openlocfilehash: c0110186277df7e41b9110b1cfdf2fa7b948b50e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913446"
---
# <span data-ttu-id="333ca-101">Remove-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="333ca-101">Remove-AzExpressRoutePort</span></span>

## <span data-ttu-id="333ca-102">簡介</span><span class="sxs-lookup"><span data-stu-id="333ca-102">SYNOPSIS</span></span>
<span data-ttu-id="333ca-103">移除 ExpressRoutePort。</span><span class="sxs-lookup"><span data-stu-id="333ca-103">Removes an ExpressRoutePort.</span></span>

## <span data-ttu-id="333ca-104">語法</span><span class="sxs-lookup"><span data-stu-id="333ca-104">SYNTAX</span></span>

### <span data-ttu-id="333ca-105">ResourceNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="333ca-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzExpressRoutePort -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="333ca-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="333ca-106">InputObjectParameterSet</span></span>
```
Remove-AzExpressRoutePort -InputObject <PSExpressRoutePort> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="333ca-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="333ca-107">ResourceIdParameterSet</span></span>
```
Remove-AzExpressRoutePort -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="333ca-108">描述</span><span class="sxs-lookup"><span data-stu-id="333ca-108">DESCRIPTION</span></span>
<span data-ttu-id="333ca-109">**Remove-AzExpressRoutePort** Cmdlet 會移除 ExpressRoutePort。</span><span class="sxs-lookup"><span data-stu-id="333ca-109">The **Remove-AzExpressRoutePort** cmdlet removes an ExpressRoutePort.</span></span>

## <span data-ttu-id="333ca-110">例子</span><span class="sxs-lookup"><span data-stu-id="333ca-110">EXAMPLES</span></span>

### <span data-ttu-id="333ca-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="333ca-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
```

<span data-ttu-id="333ca-112">移除$PortName訂閱中$rg資源群組中的 ExpressRoutePort 資源。</span><span class="sxs-lookup"><span data-stu-id="333ca-112">Removes $PortName ExpressRoutePort resource in $rg resource group in your subscription.</span></span>

### <span data-ttu-id="333ca-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="333ca-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzExpressRoutePort -InputObject $erPort
```

<span data-ttu-id="333ca-114">移除 InputObject 中的 ExpressRoutePort 資源。</span><span class="sxs-lookup"><span data-stu-id="333ca-114">Removes the ExpressRoutePort resource in InputObject.</span></span>

### <span data-ttu-id="333ca-115">範例 3</span><span class="sxs-lookup"><span data-stu-id="333ca-115">Example 3</span></span>
```powershell
PS C:\> Remove-AzExpressRoutePort -Name $ResourceId $id
```

<span data-ttu-id="333ca-116">移除具有 ResourceId $id 的 ExpressRoutePort $id。</span><span class="sxs-lookup"><span data-stu-id="333ca-116">Removes the ExpressRoutePort resource with ResourceId $id.</span></span>

## <span data-ttu-id="333ca-117">參數</span><span class="sxs-lookup"><span data-stu-id="333ca-117">PARAMETERS</span></span>

### <span data-ttu-id="333ca-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="333ca-118">-AsJob</span></span>
<span data-ttu-id="333ca-119">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="333ca-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="333ca-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="333ca-120">-DefaultProfile</span></span>
<span data-ttu-id="333ca-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="333ca-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="333ca-122">-強制</span><span class="sxs-lookup"><span data-stu-id="333ca-122">-Force</span></span>
<span data-ttu-id="333ca-123">如果您要刪除資源，請勿要求確認</span><span class="sxs-lookup"><span data-stu-id="333ca-123">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="333ca-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="333ca-124">-InputObject</span></span>
<span data-ttu-id="333ca-125">Express 路由埠物件</span><span class="sxs-lookup"><span data-stu-id="333ca-125">The express route port object</span></span>

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

### <span data-ttu-id="333ca-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="333ca-126">-Name</span></span>
<span data-ttu-id="333ca-127">ExpressRoutePort 的名稱。</span><span class="sxs-lookup"><span data-stu-id="333ca-127">The name of the ExpressRoutePort.</span></span>

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

### <span data-ttu-id="333ca-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="333ca-128">-PassThru</span></span>
<span data-ttu-id="333ca-129">會返回代表您處理之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="333ca-129">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="333ca-130">根據預設，此 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="333ca-130">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="333ca-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="333ca-131">-ResourceGroupName</span></span>
<span data-ttu-id="333ca-132">ExpressRoutePort 的資源組名。</span><span class="sxs-lookup"><span data-stu-id="333ca-132">The resource group name of the ExpressRoutePort.</span></span>

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

### <span data-ttu-id="333ca-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="333ca-133">-ResourceId</span></span>
<span data-ttu-id="333ca-134">Express 路由埠的 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="333ca-134">ResourceId of the express route port.</span></span>

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

### <span data-ttu-id="333ca-135">-確認</span><span class="sxs-lookup"><span data-stu-id="333ca-135">-Confirm</span></span>
<span data-ttu-id="333ca-136">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="333ca-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="333ca-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="333ca-137">-WhatIf</span></span>
<span data-ttu-id="333ca-138">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="333ca-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="333ca-139">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="333ca-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="333ca-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="333ca-140">CommonParameters</span></span>
<span data-ttu-id="333ca-141">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="333ca-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="333ca-142">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="333ca-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="333ca-143">輸入</span><span class="sxs-lookup"><span data-stu-id="333ca-143">INPUTS</span></span>

### <span data-ttu-id="333ca-144">Microsoft.Azure.Commands.Network.models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="333ca-144">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

### <span data-ttu-id="333ca-145">System.String</span><span class="sxs-lookup"><span data-stu-id="333ca-145">System.String</span></span>

## <span data-ttu-id="333ca-146">輸出</span><span class="sxs-lookup"><span data-stu-id="333ca-146">OUTPUTS</span></span>

### <span data-ttu-id="333ca-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="333ca-147">System.Boolean</span></span>

## <span data-ttu-id="333ca-148">筆記</span><span class="sxs-lookup"><span data-stu-id="333ca-148">NOTES</span></span>

## <span data-ttu-id="333ca-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="333ca-149">RELATED LINKS</span></span>

[<span data-ttu-id="333ca-150">Get-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="333ca-150">Get-AzExpressRoutePort</span></span>](./Get-AzExpressRoutePort.md)

[<span data-ttu-id="333ca-151">New-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="333ca-151">New-AzExpressRoutePort</span></span>](./New-AzExpressRoutePort.md)

[<span data-ttu-id="333ca-152">Set-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="333ca-152">Set-AzExpressRoutePort</span></span>](./Set-AzExpressRoutePort.md)
