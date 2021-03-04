---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvirtualnetworktap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkTap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkTap.md
ms.openlocfilehash: 93bc2a622d2bba077b5176c67df4d7894a95d4ae
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908486"
---
# <span data-ttu-id="31d22-101">New-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="31d22-101">New-AzVirtualNetworkTap</span></span>

## <span data-ttu-id="31d22-102">簡介</span><span class="sxs-lookup"><span data-stu-id="31d22-102">SYNOPSIS</span></span>
<span data-ttu-id="31d22-103">建立 VirtualNetworkTap 資源。</span><span class="sxs-lookup"><span data-stu-id="31d22-103">Creates a VirtualNetworkTap resource.</span></span>

## <span data-ttu-id="31d22-104">語法</span><span class="sxs-lookup"><span data-stu-id="31d22-104">SYNTAX</span></span>

### <span data-ttu-id="31d22-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="31d22-105">SetByResource (Default)</span></span>
```
New-AzVirtualNetworkTap -ResourceGroupName <String> -Name <String> [-DestinationPort <Int32>]
 [-Location <String>] [-Tag <Hashtable>]
 [-DestinationNetworkInterfaceIPConfiguration <PSNetworkInterfaceIPConfiguration>]
 [-DestinationLoadBalancerFrontEndIPConfiguration <PSFrontendIPConfiguration>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31d22-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="31d22-106">SetByResourceId</span></span>
```
New-AzVirtualNetworkTap -ResourceGroupName <String> -Name <String> [-DestinationPort <Int32>]
 [-Location <String>] [-Tag <Hashtable>] [-DestinationNetworkInterfaceIPConfigurationId <String>]
 [-DestinationLoadBalancerFrontEndIPConfigurationId <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="31d22-107">描述</span><span class="sxs-lookup"><span data-stu-id="31d22-107">DESCRIPTION</span></span>
<span data-ttu-id="31d22-108">**New-AzVirtualNetworkTap** Cmdlet 會建立 Azure 虛擬網路點符資源。</span><span class="sxs-lookup"><span data-stu-id="31d22-108">The **New-AzVirtualNetworkTap** cmdlet creates an Azure virtual network tap resource.</span></span>

## <span data-ttu-id="31d22-109">例子</span><span class="sxs-lookup"><span data-stu-id="31d22-109">EXAMPLES</span></span>

### <span data-ttu-id="31d22-110">範例 1：建立 Azure 虛擬網路點兩下</span><span class="sxs-lookup"><span data-stu-id="31d22-110">Example 1: Create an Azure virtual network tap</span></span>
```
PS C:\>New-AzVirtualNetworkTap -Name "VirtualNetworkTap1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -DestinationPort 8888 -DestinationNetworkInterfaceIPConfiguration $destinationNic.IpConfigurations[0]
```

<span data-ttu-id="31d22-111">此命令會建立名為「VirtualNetworkTap1」的虛擬網路點，其中具有目的地 VM 組 (DestinationIpConfiguration、DestinationPort) 。</span><span class="sxs-lookup"><span data-stu-id="31d22-111">This command creates a virtual network tap named "VirtualNetworkTap1" which has destination VM configuration details (DestinationIpConfiguration, DestinationPort).</span></span>
<span data-ttu-id="31d22-112">點一下所配置之 VM 流量的所有來源都會路由至此目的地 IP + 埠。</span><span class="sxs-lookup"><span data-stu-id="31d22-112">All the source tap configured VM's traffic will be routed to this Destination IP + Port.</span></span>

### <span data-ttu-id="31d22-113">範例 2：使用 LoadBalancer IP 建立 Azure 虛擬網路點一下</span><span class="sxs-lookup"><span data-stu-id="31d22-113">Example 2: Create an Azure virtual network tap using LoadBalancer IP</span></span>
```
# Create LoadBalancer
PS C:\>$frontend = New-AzLoadBalancerFrontendIpConfig -Name $frontendName -PublicIpAddress $publicip
PS C:\>New-AzVirtualNetworkTap -Name "VirtualNetworkTap1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -DestinationLoadBalancerFrontEndIPConfiguration $frontend
```

<span data-ttu-id="31d22-114">此命令會建立名為「VirtualNetworkTap1」的虛擬網路點 (FrontEndIpConfiguration) 。</span><span class="sxs-lookup"><span data-stu-id="31d22-114">This command creates a virtual network tap named "VirtualNetworkTap1" which has destination VM configuration details (FrontEndIpConfiguration).</span></span>
<span data-ttu-id="31d22-115">所有來源點一下所配置的 VM 流量都會路由到此 LoadBalancer IpConfiguration。</span><span class="sxs-lookup"><span data-stu-id="31d22-115">All the source tap configured VM's traffic will be routed to this LoadBalancer IpConfiguration.</span></span> <span data-ttu-id="31d22-116">預設目的地埠為 4789。</span><span class="sxs-lookup"><span data-stu-id="31d22-116">Default Destination Port is 4789.</span></span>

## <span data-ttu-id="31d22-117">參數</span><span class="sxs-lookup"><span data-stu-id="31d22-117">PARAMETERS</span></span>

### <span data-ttu-id="31d22-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="31d22-118">-AsJob</span></span>
<span data-ttu-id="31d22-119">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="31d22-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="31d22-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31d22-120">-DefaultProfile</span></span>
<span data-ttu-id="31d22-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="31d22-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="31d22-122">-DestinationLoadBalancerFrontEndIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="31d22-122">-DestinationLoadBalancerFrontEndIPConfiguration</span></span>
<span data-ttu-id="31d22-123">目的地負載平衡器前端 IP 組配置資源的參照。</span><span class="sxs-lookup"><span data-stu-id="31d22-123">The reference of the destination load balancer front end IP configuration resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31d22-124">-DestinationLoadBalancerFrontEndIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="31d22-124">-DestinationLoadBalancerFrontEndIPConfigurationId</span></span>
<span data-ttu-id="31d22-125">目的地負載平衡器前端 IP 組配置資源的參照。</span><span class="sxs-lookup"><span data-stu-id="31d22-125">The reference of the destination load balancer front end IP configuration resource.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31d22-126">-DestinationNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="31d22-126">-DestinationNetworkInterfaceIPConfiguration</span></span>
<span data-ttu-id="31d22-127">目的地網路介面 IP 組配置資源的參照。</span><span class="sxs-lookup"><span data-stu-id="31d22-127">The reference of the destination network interface IP configuration resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31d22-128">-DestinationNetworkInterfaceIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="31d22-128">-DestinationNetworkInterfaceIPConfigurationId</span></span>
<span data-ttu-id="31d22-129">目的地網路介面 IP 組配置資源的參照。</span><span class="sxs-lookup"><span data-stu-id="31d22-129">The reference of the destination network interface IP configuration resource.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31d22-130">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="31d22-130">-DestinationPort</span></span>
<span data-ttu-id="31d22-131">封包收集器的目的地埠</span><span class="sxs-lookup"><span data-stu-id="31d22-131">The Destination Port of the packet collector</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31d22-132">-強制</span><span class="sxs-lookup"><span data-stu-id="31d22-132">-Force</span></span>
<span data-ttu-id="31d22-133">如果您想要覆寫資源，請勿要求確認</span><span class="sxs-lookup"><span data-stu-id="31d22-133">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="31d22-134">-位置</span><span class="sxs-lookup"><span data-stu-id="31d22-134">-Location</span></span>
<span data-ttu-id="31d22-135">位置。</span><span class="sxs-lookup"><span data-stu-id="31d22-135">The location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31d22-136">-名稱</span><span class="sxs-lookup"><span data-stu-id="31d22-136">-Name</span></span>
<span data-ttu-id="31d22-137">點一下的名稱。</span><span class="sxs-lookup"><span data-stu-id="31d22-137">The name of the tap.</span></span>

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

### <span data-ttu-id="31d22-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31d22-138">-ResourceGroupName</span></span>
<span data-ttu-id="31d22-139">點一下虛擬網路的資源組名。</span><span class="sxs-lookup"><span data-stu-id="31d22-139">The resource group name of the virtual network tap.</span></span>

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

### <span data-ttu-id="31d22-140">-標記</span><span class="sxs-lookup"><span data-stu-id="31d22-140">-Tag</span></span>
<span data-ttu-id="31d22-141">代表資源標記的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="31d22-141">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31d22-142">-確認</span><span class="sxs-lookup"><span data-stu-id="31d22-142">-Confirm</span></span>
<span data-ttu-id="31d22-143">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="31d22-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="31d22-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31d22-144">-WhatIf</span></span>
<span data-ttu-id="31d22-145">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="31d22-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="31d22-146">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="31d22-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="31d22-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31d22-147">CommonParameters</span></span>
<span data-ttu-id="31d22-148">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="31d22-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31d22-149">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="31d22-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31d22-150">輸入</span><span class="sxs-lookup"><span data-stu-id="31d22-150">INPUTS</span></span>

### <span data-ttu-id="31d22-151">System.String</span><span class="sxs-lookup"><span data-stu-id="31d22-151">System.String</span></span>

### <span data-ttu-id="31d22-152">System.Int32</span><span class="sxs-lookup"><span data-stu-id="31d22-152">System.Int32</span></span>

### <span data-ttu-id="31d22-153">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="31d22-153">System.Collections.Hashtable</span></span>

### <span data-ttu-id="31d22-154">Microsoft.Azure.Commands.Network.models.PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="31d22-154">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration</span></span>

### <span data-ttu-id="31d22-155">Microsoft.Azure.Commands.Network.models.PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="31d22-155">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="31d22-156">輸出</span><span class="sxs-lookup"><span data-stu-id="31d22-156">OUTPUTS</span></span>

### <span data-ttu-id="31d22-157">Microsoft.Azure.Commands.Network.models.PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="31d22-157">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="31d22-158">筆記</span><span class="sxs-lookup"><span data-stu-id="31d22-158">NOTES</span></span>

## <span data-ttu-id="31d22-159">相關連結</span><span class="sxs-lookup"><span data-stu-id="31d22-159">RELATED LINKS</span></span>

[<span data-ttu-id="31d22-160">Get-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="31d22-160">Get-AzVirtualNetworkTap</span></span>](./Get-AzVirtualNetworkTap.md)

[<span data-ttu-id="31d22-161">Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="31d22-161">Remove-AzVirtualNetworkTap</span></span>](./Remove-AzVirtualNetworkTap.md)

[<span data-ttu-id="31d22-162">Set-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="31d22-162">Set-AzVirtualNetworkTap</span></span>](./Set-AzVirtualNetworkTap.md)
