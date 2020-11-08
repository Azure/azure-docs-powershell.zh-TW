---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutegateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteGateway.md
ms.openlocfilehash: 73bf40456b1fa99093f2c84c11f71e945004a8fa
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94135536"
---
# <span data-ttu-id="82cb1-101">Remove-AzExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="82cb1-101">Remove-AzExpressRouteGateway</span></span>

## <span data-ttu-id="82cb1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="82cb1-102">SYNOPSIS</span></span>
<span data-ttu-id="82cb1-103">Remove-AzExpressRouteGateway Cmdlet 會移除 Azure ExpressRoute 閘道。</span><span class="sxs-lookup"><span data-stu-id="82cb1-103">The Remove-AzExpressRouteGateway cmdlet removes an Azure ExpressRoute gateway.</span></span> <span data-ttu-id="82cb1-104">這是 Azure 虛擬 WAN 的軟體定義連線所專用的閘道。</span><span class="sxs-lookup"><span data-stu-id="82cb1-104">This is a gateway specific to Azure Virtual WAN's software defined connectivity.</span></span>

## <span data-ttu-id="82cb1-105">句法</span><span class="sxs-lookup"><span data-stu-id="82cb1-105">SYNTAX</span></span>

### <span data-ttu-id="82cb1-106">ByExpressRouteGatewayName (預設) </span><span class="sxs-lookup"><span data-stu-id="82cb1-106">ByExpressRouteGatewayName (Default)</span></span>
```
Remove-AzExpressRouteGateway -ResourceGroupName <String> -Name <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="82cb1-107">ByExpressRouteGatewayObject</span><span class="sxs-lookup"><span data-stu-id="82cb1-107">ByExpressRouteGatewayObject</span></span>
```
Remove-AzExpressRouteGateway -InputObject <PSExpressRouteGateway> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="82cb1-108">ByExpressRouteGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="82cb1-108">ByExpressRouteGatewayResourceId</span></span>
```
Remove-AzExpressRouteGateway -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="82cb1-109">說明</span><span class="sxs-lookup"><span data-stu-id="82cb1-109">DESCRIPTION</span></span>
<span data-ttu-id="82cb1-110">Remove-AzExpressRouteGateway Cmdlet 會移除 Azure ExpressRoute 閘道。</span><span class="sxs-lookup"><span data-stu-id="82cb1-110">The Remove-AzExpressRouteGateway cmdlet removes an Azure ExpressRoute gateway.</span></span> <span data-ttu-id="82cb1-111">這是 Azure 虛擬 WAN 的軟體定義連線所專用的閘道。</span><span class="sxs-lookup"><span data-stu-id="82cb1-111">This is a gateway specific to Azure Virtual WAN's software defined connectivity.</span></span>

## <span data-ttu-id="82cb1-112">示例</span><span class="sxs-lookup"><span data-stu-id="82cb1-112">EXAMPLES</span></span>

### <span data-ttu-id="82cb1-113">範例1</span><span class="sxs-lookup"><span data-stu-id="82cb1-113">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West Central US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West Central US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" -VirtualHubId $virtualHub.Id -MinScaleUnits 2
PS C:\> Remove-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" -Passthru
```

<span data-ttu-id="82cb1-114">這個範例會在美國中部建立資源群組、虛擬 WAN、虛擬中樞、可伸縮的 ExpressRoute 閘道，然後立即將其刪除。</span><span class="sxs-lookup"><span data-stu-id="82cb1-114">This example creates a Resource group, Virtual WAN, Virtual Hub, scalable ExpressRoute gateway in Central US and then immediately deletes it.</span></span> <span data-ttu-id="82cb1-115">若要在刪除虛擬閘道時取消提示，請使用-Force 標誌。</span><span class="sxs-lookup"><span data-stu-id="82cb1-115">To suppress the prompt when deleting the Virtual Gateway, use the -Force flag.</span></span>
<span data-ttu-id="82cb1-116">這將會刪除 ExpressRouteGateway 及其附加的所有 ExpressRouteConnections。</span><span class="sxs-lookup"><span data-stu-id="82cb1-116">This will delete the ExpressRouteGateway and all ExpressRouteConnections attached to it.</span></span>

### <span data-ttu-id="82cb1-117">範例2</span><span class="sxs-lookup"><span data-stu-id="82cb1-117">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West Central US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West Central US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" -VirtualHubId $virtualHub.Id -MinScaleUnits 2
PS C:\> Get-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" | Remove-AzExpressRouteGateway-Passthru
```

<span data-ttu-id="82cb1-118">這個範例會在 West 中建立一個資源群組、虛擬 WAN、虛擬中樞、可伸縮的 ExpressRoute 閘道，然後立即將其刪除。</span><span class="sxs-lookup"><span data-stu-id="82cb1-118">This example creates a Resource group, Virtual WAN, Virtual Hub, scalable ExpressRoute gateway in West Central US and then immediately deletes it.</span></span> <span data-ttu-id="82cb1-119">此刪除會使用 powershell 管道執行，這會使用 Get-AzExpressRouteGateway 命令所傳回的 ExpressRouteGateway 物件。</span><span class="sxs-lookup"><span data-stu-id="82cb1-119">This deletion happens using powershell piping, which uses the ExpressRouteGateway object returned by the Get-AzExpressRouteGateway command.</span></span>
<span data-ttu-id="82cb1-120">若要在刪除虛擬閘道時取消提示，請使用-Force 標誌。</span><span class="sxs-lookup"><span data-stu-id="82cb1-120">To suppress the prompt when deleting the Virtual Gateway, use the -Force flag.</span></span>
<span data-ttu-id="82cb1-121">這將會刪除 ExpressRouteGateway 及其附加的所有 ExpressRouteConnections。</span><span class="sxs-lookup"><span data-stu-id="82cb1-121">This will delete the ExpressRouteGateway and all ExpressRouteConnections attached to it.</span></span>

## <span data-ttu-id="82cb1-122">參數</span><span class="sxs-lookup"><span data-stu-id="82cb1-122">PARAMETERS</span></span>

### <span data-ttu-id="82cb1-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82cb1-123">-DefaultProfile</span></span>
<span data-ttu-id="82cb1-124">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="82cb1-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="82cb1-125">-Force</span><span class="sxs-lookup"><span data-stu-id="82cb1-125">-Force</span></span>
<span data-ttu-id="82cb1-126">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="82cb1-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="82cb1-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="82cb1-127">-InputObject</span></span>
<span data-ttu-id="82cb1-128">要刪除的 ExpressRouteGateway 物件。</span><span class="sxs-lookup"><span data-stu-id="82cb1-128">The ExpressRouteGateway object to be deleted.</span></span>

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

### <span data-ttu-id="82cb1-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="82cb1-129">-Name</span></span>
<span data-ttu-id="82cb1-130">ExpressRouteGateway 的名稱。</span><span class="sxs-lookup"><span data-stu-id="82cb1-130">The ExpressRouteGateway name.</span></span>

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

### <span data-ttu-id="82cb1-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="82cb1-131">-PassThru</span></span>
<span data-ttu-id="82cb1-132">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="82cb1-132">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="82cb1-133">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="82cb1-133">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="82cb1-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82cb1-134">-ResourceGroupName</span></span>
<span data-ttu-id="82cb1-135">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="82cb1-135">The resource group name.</span></span>

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

### <span data-ttu-id="82cb1-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="82cb1-136">-ResourceId</span></span>
<span data-ttu-id="82cb1-137">要刪除之 ExpressRouteGateway 的 Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="82cb1-137">The Azure resource ID for the ExpressRouteGateway to be deleted.</span></span>

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

### <span data-ttu-id="82cb1-138">-確認</span><span class="sxs-lookup"><span data-stu-id="82cb1-138">-Confirm</span></span>
<span data-ttu-id="82cb1-139">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="82cb1-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="82cb1-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82cb1-140">-WhatIf</span></span>
<span data-ttu-id="82cb1-141">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="82cb1-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="82cb1-142">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="82cb1-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="82cb1-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82cb1-143">CommonParameters</span></span>
<span data-ttu-id="82cb1-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="82cb1-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82cb1-145">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="82cb1-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82cb1-146">輸入</span><span class="sxs-lookup"><span data-stu-id="82cb1-146">INPUTS</span></span>

### <span data-ttu-id="82cb1-147">PSExpressRouteGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="82cb1-147">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span></span>

### <span data-ttu-id="82cb1-148">System.object</span><span class="sxs-lookup"><span data-stu-id="82cb1-148">System.String</span></span>

## <span data-ttu-id="82cb1-149">輸出</span><span class="sxs-lookup"><span data-stu-id="82cb1-149">OUTPUTS</span></span>

### <span data-ttu-id="82cb1-150">System.object</span><span class="sxs-lookup"><span data-stu-id="82cb1-150">System.Boolean</span></span>

## <span data-ttu-id="82cb1-151">筆記</span><span class="sxs-lookup"><span data-stu-id="82cb1-151">NOTES</span></span>

## <span data-ttu-id="82cb1-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="82cb1-152">RELATED LINKS</span></span>
