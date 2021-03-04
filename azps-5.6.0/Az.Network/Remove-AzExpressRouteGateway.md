---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azexpressroutegateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteGateway.md
ms.openlocfilehash: 77c41a4565a517a51b02c904d79953d79e908c39
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913450"
---
# <span data-ttu-id="f52b4-101">Remove-AzExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="f52b4-101">Remove-AzExpressRouteGateway</span></span>

## <span data-ttu-id="f52b4-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f52b4-102">SYNOPSIS</span></span>
<span data-ttu-id="f52b4-103">Cmdlet Remove-AzExpressRouteGateway移除 Azure ExpressRoute 閘道。</span><span class="sxs-lookup"><span data-stu-id="f52b4-103">The Remove-AzExpressRouteGateway cmdlet removes an Azure ExpressRoute gateway.</span></span> <span data-ttu-id="f52b4-104">這是 Azure Virtual WAN 軟體定義之連接的特定閘道。</span><span class="sxs-lookup"><span data-stu-id="f52b4-104">This is a gateway specific to Azure Virtual WAN's software defined connectivity.</span></span>

## <span data-ttu-id="f52b4-105">語法</span><span class="sxs-lookup"><span data-stu-id="f52b4-105">SYNTAX</span></span>

### <span data-ttu-id="f52b4-106">ByExpressRouteGatewayName (預設) </span><span class="sxs-lookup"><span data-stu-id="f52b4-106">ByExpressRouteGatewayName (Default)</span></span>
```
Remove-AzExpressRouteGateway -ResourceGroupName <String> -Name <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f52b4-107">ByExpressRouteGatewayObject</span><span class="sxs-lookup"><span data-stu-id="f52b4-107">ByExpressRouteGatewayObject</span></span>
```
Remove-AzExpressRouteGateway -InputObject <PSExpressRouteGateway> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f52b4-108">ByExpressRouteGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="f52b4-108">ByExpressRouteGatewayResourceId</span></span>
```
Remove-AzExpressRouteGateway -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f52b4-109">描述</span><span class="sxs-lookup"><span data-stu-id="f52b4-109">DESCRIPTION</span></span>
<span data-ttu-id="f52b4-110">Cmdlet Remove-AzExpressRouteGateway移除 Azure ExpressRoute 閘道。</span><span class="sxs-lookup"><span data-stu-id="f52b4-110">The Remove-AzExpressRouteGateway cmdlet removes an Azure ExpressRoute gateway.</span></span> <span data-ttu-id="f52b4-111">這是 Azure Virtual WAN 軟體定義之連接的特定閘道。</span><span class="sxs-lookup"><span data-stu-id="f52b4-111">This is a gateway specific to Azure Virtual WAN's software defined connectivity.</span></span>

## <span data-ttu-id="f52b4-112">例子</span><span class="sxs-lookup"><span data-stu-id="f52b4-112">EXAMPLES</span></span>

### <span data-ttu-id="f52b4-113">範例 1</span><span class="sxs-lookup"><span data-stu-id="f52b4-113">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West Central US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West Central US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" -VirtualHubId $virtualHub.Id -MinScaleUnits 2
PS C:\> Remove-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" -Passthru
```

<span data-ttu-id="f52b4-114">此範例會在美國中建立資源群組、虛擬 WAN、虛擬中樞、可縮放的 ExpressRoute 閘道，然後立即刪除。</span><span class="sxs-lookup"><span data-stu-id="f52b4-114">This example creates a Resource group, Virtual WAN, Virtual Hub, scalable ExpressRoute gateway in Central US and then immediately deletes it.</span></span> <span data-ttu-id="f52b4-115">若要隱藏刪除虛擬閘道時提示，請使用 -Force 旗標。</span><span class="sxs-lookup"><span data-stu-id="f52b4-115">To suppress the prompt when deleting the Virtual Gateway, use the -Force flag.</span></span>
<span data-ttu-id="f52b4-116">這會刪除 ExpressRouteGateway 以及附加至該郵件的所有 ExpressRouteConnection。</span><span class="sxs-lookup"><span data-stu-id="f52b4-116">This will delete the ExpressRouteGateway and all ExpressRouteConnections attached to it.</span></span>

### <span data-ttu-id="f52b4-117">範例 2</span><span class="sxs-lookup"><span data-stu-id="f52b4-117">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West Central US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West Central US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" -VirtualHubId $virtualHub.Id -MinScaleUnits 2
PS C:\> Get-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" | Remove-AzExpressRouteGateway-Passthru
```

<span data-ttu-id="f52b4-118">此範例會在美國中西部建立資源群組、虛擬 WAN、虛擬中樞、可縮放的 ExpressRoute 閘道，然後立即刪除。</span><span class="sxs-lookup"><span data-stu-id="f52b4-118">This example creates a Resource group, Virtual WAN, Virtual Hub, scalable ExpressRoute gateway in West Central US and then immediately deletes it.</span></span> <span data-ttu-id="f52b4-119">此刪除會使用 powershell 管線執行，此管道使用由 Get-AzExpressRouteGateway 命令所返回的 ExpressRouteGateway 物件。</span><span class="sxs-lookup"><span data-stu-id="f52b4-119">This deletion happens using powershell piping, which uses the ExpressRouteGateway object returned by the Get-AzExpressRouteGateway command.</span></span>
<span data-ttu-id="f52b4-120">若要隱藏刪除虛擬閘道時提示，請使用 -Force 旗標。</span><span class="sxs-lookup"><span data-stu-id="f52b4-120">To suppress the prompt when deleting the Virtual Gateway, use the -Force flag.</span></span>
<span data-ttu-id="f52b4-121">這會刪除 ExpressRouteGateway 以及附加至該郵件的所有 ExpressRouteConnection。</span><span class="sxs-lookup"><span data-stu-id="f52b4-121">This will delete the ExpressRouteGateway and all ExpressRouteConnections attached to it.</span></span>

## <span data-ttu-id="f52b4-122">參數</span><span class="sxs-lookup"><span data-stu-id="f52b4-122">PARAMETERS</span></span>

### <span data-ttu-id="f52b4-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f52b4-123">-DefaultProfile</span></span>
<span data-ttu-id="f52b4-124">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f52b4-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f52b4-125">-強制</span><span class="sxs-lookup"><span data-stu-id="f52b4-125">-Force</span></span>
<span data-ttu-id="f52b4-126">請勿要求確認。</span><span class="sxs-lookup"><span data-stu-id="f52b4-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="f52b4-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f52b4-127">-InputObject</span></span>
<span data-ttu-id="f52b4-128">要刪除的 ExpressRouteGateway 物件。</span><span class="sxs-lookup"><span data-stu-id="f52b4-128">The ExpressRouteGateway object to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway
Parameter Sets: ByExpressRouteGatewayObject
Aliases: ExpressRouteGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f52b4-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="f52b4-129">-Name</span></span>
<span data-ttu-id="f52b4-130">ExpressRouteGateway 名稱。</span><span class="sxs-lookup"><span data-stu-id="f52b4-130">The ExpressRouteGateway name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteGatewayName
Aliases: ResourceName, ExpressRouteGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f52b4-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f52b4-131">-PassThru</span></span>
<span data-ttu-id="f52b4-132">會返回代表您處理之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="f52b4-132">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="f52b4-133">根據預設，此 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="f52b4-133">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f52b4-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f52b4-134">-ResourceGroupName</span></span>
<span data-ttu-id="f52b4-135">資源組名。</span><span class="sxs-lookup"><span data-stu-id="f52b4-135">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f52b4-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f52b4-136">-ResourceId</span></span>
<span data-ttu-id="f52b4-137">要刪除 ExpressRouteGateway 的 Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="f52b4-137">The Azure resource ID for the ExpressRouteGateway to be deleted.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteGatewayResourceId
Aliases: expressRouteGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f52b4-138">-確認</span><span class="sxs-lookup"><span data-stu-id="f52b4-138">-Confirm</span></span>
<span data-ttu-id="f52b4-139">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="f52b4-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f52b4-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f52b4-140">-WhatIf</span></span>
<span data-ttu-id="f52b4-141">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f52b4-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f52b4-142">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f52b4-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f52b4-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f52b4-143">CommonParameters</span></span>
<span data-ttu-id="f52b4-144">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f52b4-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f52b4-145">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="f52b4-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f52b4-146">輸入</span><span class="sxs-lookup"><span data-stu-id="f52b4-146">INPUTS</span></span>

### <span data-ttu-id="f52b4-147">Microsoft.Azure.Commands.Network.models.PSExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="f52b4-147">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span></span>

### <span data-ttu-id="f52b4-148">System.String</span><span class="sxs-lookup"><span data-stu-id="f52b4-148">System.String</span></span>

## <span data-ttu-id="f52b4-149">輸出</span><span class="sxs-lookup"><span data-stu-id="f52b4-149">OUTPUTS</span></span>

### <span data-ttu-id="f52b4-150">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f52b4-150">System.Boolean</span></span>

## <span data-ttu-id="f52b4-151">筆記</span><span class="sxs-lookup"><span data-stu-id="f52b4-151">NOTES</span></span>

## <span data-ttu-id="f52b4-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="f52b4-152">RELATED LINKS</span></span>
