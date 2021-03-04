---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DDB38A77-E5C0-47DD-BADD-94488F661CD5
online version: https://docs.microsoft.com/powershell/module/az.network/set-aznetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterface.md
ms.openlocfilehash: 0afd299103f1595afd100a7e9a72c4045896419d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910966"
---
# <span data-ttu-id="808c3-101">Set-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="808c3-101">Set-AzNetworkInterface</span></span>

## <span data-ttu-id="808c3-102">簡介</span><span class="sxs-lookup"><span data-stu-id="808c3-102">SYNOPSIS</span></span>
<span data-ttu-id="808c3-103">更新網路介面。</span><span class="sxs-lookup"><span data-stu-id="808c3-103">Updates a network interface.</span></span>

## <span data-ttu-id="808c3-104">語法</span><span class="sxs-lookup"><span data-stu-id="808c3-104">SYNTAX</span></span>

```
Set-AzNetworkInterface -NetworkInterface <PSNetworkInterface> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="808c3-105">描述</span><span class="sxs-lookup"><span data-stu-id="808c3-105">DESCRIPTION</span></span>
<span data-ttu-id="808c3-106">**Set-AzNetworkInterface 會** 更新網路介面。</span><span class="sxs-lookup"><span data-stu-id="808c3-106">The **Set-AzNetworkInterface** updates a network interface.</span></span>

## <span data-ttu-id="808c3-107">例子</span><span class="sxs-lookup"><span data-stu-id="808c3-107">EXAMPLES</span></span>

### <span data-ttu-id="808c3-108">範例 1：設定網路介面</span><span class="sxs-lookup"><span data-stu-id="808c3-108">Example 1: Configure a network interface</span></span>
```
$Nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$Nic.IpConfigurations[0].PrivateIpAddress = "10.0.1.20"
$Nic.IpConfigurations[0].PrivateIpAllocationMethod = "Static"
$Nic.Tag = @{Name = "Name"; Value = "Value"}
Set-AzNetworkInterface -NetworkInterface $Nic
```

<span data-ttu-id="808c3-109">此範例會設定網路介面。</span><span class="sxs-lookup"><span data-stu-id="808c3-109">This example configures a network interface.</span></span>
<span data-ttu-id="808c3-110">第一個命令會獲得資源群組 ResourceGroup1 中名為 NetworkInterface1 的網路介面。</span><span class="sxs-lookup"><span data-stu-id="808c3-110">The first command gets a network interface named NetworkInterface1 in resource group ResourceGroup1.</span></span>
<span data-ttu-id="808c3-111">第二個命令會設定 IP 設定的私人 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="808c3-111">The second command sets the private IP address of the IP configuration.</span></span>
<span data-ttu-id="808c3-112">第三個命令將私人 IP 分配方法設定為靜態。</span><span class="sxs-lookup"><span data-stu-id="808c3-112">The third command sets the private IP allocation method to Static.</span></span>
<span data-ttu-id="808c3-113">第四個命令會設定網路介面上的標記。</span><span class="sxs-lookup"><span data-stu-id="808c3-113">The fourth command sets a tag on the network interface.</span></span>
<span data-ttu-id="808c3-114">第五個命令使用儲存在 $Nic 變數的資訊來設定網路介面。</span><span class="sxs-lookup"><span data-stu-id="808c3-114">The fifth command uses the information stored in the $Nic variable to set the network interface.</span></span>

### <span data-ttu-id="808c3-115">範例 2：變更網路介面上的 DNS 設定</span><span class="sxs-lookup"><span data-stu-id="808c3-115">Example 2: Change DNS settings on a network interface</span></span>
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nic.DnsSettings.DnsServers.Add("192.168.1.100")
$nic | Set-AzNetworkInterface
```

<span data-ttu-id="808c3-116">第一個命令會獲得名稱為 NetworkInterface1 的網路介面，該介面存在於資源群組 ResourceGroup1 中。</span><span class="sxs-lookup"><span data-stu-id="808c3-116">The first command gets a network interface named NetworkInterface1 that exists within resource group ResourceGroup1.</span></span> <span data-ttu-id="808c3-117">第二個命令會將 DNS 伺服器 192.168.1.100 新增到此介面。</span><span class="sxs-lookup"><span data-stu-id="808c3-117">The second command adds DNS server 192.168.1.100 to this interface.</span></span> <span data-ttu-id="808c3-118">第三個命令會將這些變更適用于網路介面。</span><span class="sxs-lookup"><span data-stu-id="808c3-118">The third command applies these changes to the network interface.</span></span> <span data-ttu-id="808c3-119">若要移除 DNS 伺服器，請遵循上述命令，但取代 "。新增" 加上 "。第二個命令中的移除」。</span><span class="sxs-lookup"><span data-stu-id="808c3-119">To remove a DNS server, follow the commands listed above, but replace ".Add" with ".Remove" in the second command.</span></span>

### <span data-ttu-id="808c3-120">範例 3：在網路介面上啟用 IP 轉轉</span><span class="sxs-lookup"><span data-stu-id="808c3-120">Example 3: Enable IP forwarding on a network interface</span></span>
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nic.EnableIPForwarding = 1
$nic | Set-AzNetworkInterface
```

<span data-ttu-id="808c3-121">第一個命令會獲得稱為 NetworkInterface1 的現有網路介面，並儲存在$nic變數。</span><span class="sxs-lookup"><span data-stu-id="808c3-121">The first command gets an existing network interface called NetworkInterface1 and stores it in the $nic variable.</span></span> <span data-ttu-id="808c3-122">第二個命令將 IP 轉轉值變更為 True。</span><span class="sxs-lookup"><span data-stu-id="808c3-122">The second command changes the IP forwarding value to true.</span></span> <span data-ttu-id="808c3-123">最後，第三個命令將變更適用于網路介面。</span><span class="sxs-lookup"><span data-stu-id="808c3-123">Finally, the third command applies the changes to the network interface.</span></span> <span data-ttu-id="808c3-124">若要停用網路介面上的 IP 轉轉，請遵循範例範例，但請務必將第二個命令變更為「$nic。EnableIPForwarding = 0"。</span><span class="sxs-lookup"><span data-stu-id="808c3-124">To disable IP forwarding on a network interface, follow the sample example, but be sure to change the second command to "$nic.EnableIPForwarding = 0".</span></span>

### <span data-ttu-id="808c3-125">範例 4：變更網路介面的子網</span><span class="sxs-lookup"><span data-stu-id="808c3-125">Example 4: Change the subnet of a network interface</span></span>
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$vnet = Get-AzVirtualNetwork -Name VNet1 -ResourceGroupName crosssubcrossversionpeering
$subnet2 = Get-AzVirtualNetworkSubnetConfig -Name Subnet2 -VirtualNetwork $vnet
$nic.IpConfigurations[0].Subnet.Id = $subnet2.Id
$nic | Set-AzNetworkInterface
```

<span data-ttu-id="808c3-126">第一個命令會獲得網路介面 NetworkInterface1，並儲存在$nic變數。</span><span class="sxs-lookup"><span data-stu-id="808c3-126">The first command gets the network interface NetworkInterface1 and stores it in the $nic variable.</span></span> <span data-ttu-id="808c3-127">第二個命令會獲得與網路介面將要關聯的子網相關聯的虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="808c3-127">The second command gets the virtual network associated with the subnet that the network interface is going to be associated with.</span></span> <span data-ttu-id="808c3-128">第二個命令會獲得子網，並儲存在 $subnet 2 變數中。</span><span class="sxs-lookup"><span data-stu-id="808c3-128">The second command gets the subnet and stores it in the $subnet2 variable.</span></span> <span data-ttu-id="808c3-129">第三個命令會關聯網路介面的主要私人 IP 位址與新的子網。</span><span class="sxs-lookup"><span data-stu-id="808c3-129">The third command associated the primary private IP address of the network interface with the new subnet.</span></span> <span data-ttu-id="808c3-130">最後，最後一個命令將這些變更應用在網路介面上。</span><span class="sxs-lookup"><span data-stu-id="808c3-130">Finally the last command applied these changes on the network interface.</span></span>
>[!NOTE] 
><span data-ttu-id="808c3-131">IP 組配置必須是動態的，您才能變更子網。</span><span class="sxs-lookup"><span data-stu-id="808c3-131">The IP configurations must be dynamic before you can change the subnet.</span></span> <span data-ttu-id="808c3-132">如果您有靜態 IP 組案，請變更為動態，再繼續進行。</span><span class="sxs-lookup"><span data-stu-id="808c3-132">If you have static IP configurations, change then to dynamic before proceeding.</span></span> 
>[!NOTE]
><span data-ttu-id="808c3-133">如果網路介面有多個 IP 組配置，則必須針對所有這些 IP 組配置執行第四個命令，才能執行Set-AzNetworkInterface命令。</span><span class="sxs-lookup"><span data-stu-id="808c3-133">If the network interface has multiple IP configurations, the forth command must be done for all these IP configurations before the final Set-AzNetworkInterface command is executed.</span></span> <span data-ttu-id="808c3-134">這可以在第四個命令中執行，但以適當的數位取代 "0"。</span><span class="sxs-lookup"><span data-stu-id="808c3-134">This can be done as in the forth command but by replacing "0" with the appropriate number.</span></span> <span data-ttu-id="808c3-135">如果網路介面有 N IP 組式，則這些命令的 N-1 必須存在。</span><span class="sxs-lookup"><span data-stu-id="808c3-135">If a network interface has N IP configurations, then N-1 of these commands must exist.</span></span>

### <span data-ttu-id="808c3-136">範例 5：將網路安全性群組關聯/解除關聯至網路介面</span><span class="sxs-lookup"><span data-stu-id="808c3-136">Example 5: Associate/Dissociate a Network Security Group to a network interface</span></span>
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nsg = Get-AzNetworkSecurityGroup -ResourceGroupName "ResourceGroup1" -Name "MyNSG"
$nic.NetworkSecurityGroup = $nsg
$nic | Set-AzNetworkInterface
```

<span data-ttu-id="808c3-137">第一個命令會獲得稱為 NetworkInterface1 的現有網路介面，並儲存在$nic變數。</span><span class="sxs-lookup"><span data-stu-id="808c3-137">The first command gets an existing network interface called NetworkInterface1 and stores it in the $nic variable.</span></span> <span data-ttu-id="808c3-138">第二個命令會獲得名為 MyNSG 的現有網路安全性群組，並儲存在 $nsg 變數中。</span><span class="sxs-lookup"><span data-stu-id="808c3-138">The second command gets an existing network security group called MyNSG and stores it in the $nsg variable.</span></span> <span data-ttu-id="808c3-139">第三個命令會$nsg指派$nic。</span><span class="sxs-lookup"><span data-stu-id="808c3-139">The third command assigns the $nsg to the $nic.</span></span> <span data-ttu-id="808c3-140">最後，第四個命令將變更適用于網路介面。</span><span class="sxs-lookup"><span data-stu-id="808c3-140">Finally, the forth command applies the changes to the Network interface.</span></span> <span data-ttu-id="808c3-141">若要將網路安全性群組與網路介面解除關聯，請以 $nsg 取代第三個命令$null。</span><span class="sxs-lookup"><span data-stu-id="808c3-141">To dissociate network security groups from a network interface, simple replace $nsg in the third command with $null.</span></span>

## <span data-ttu-id="808c3-142">參數</span><span class="sxs-lookup"><span data-stu-id="808c3-142">PARAMETERS</span></span>

### <span data-ttu-id="808c3-143">-AsJob</span><span class="sxs-lookup"><span data-stu-id="808c3-143">-AsJob</span></span>
<span data-ttu-id="808c3-144">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="808c3-144">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="808c3-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="808c3-145">-DefaultProfile</span></span>
<span data-ttu-id="808c3-146">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="808c3-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="808c3-147">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="808c3-147">-NetworkInterface</span></span>
<span data-ttu-id="808c3-148">指定代表網路介面應設定之狀態的網路介面物件。</span><span class="sxs-lookup"><span data-stu-id="808c3-148">Specifies a network interface object representing the state to which the network interface should be set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkInterface
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="808c3-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="808c3-149">CommonParameters</span></span>
<span data-ttu-id="808c3-150">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="808c3-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="808c3-151">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="808c3-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="808c3-152">輸入</span><span class="sxs-lookup"><span data-stu-id="808c3-152">INPUTS</span></span>

### <span data-ttu-id="808c3-153">Microsoft.Azure.Commands.Network.models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="808c3-153">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="808c3-154">輸出</span><span class="sxs-lookup"><span data-stu-id="808c3-154">OUTPUTS</span></span>

### <span data-ttu-id="808c3-155">Microsoft.Azure.Commands.Network.models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="808c3-155">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="808c3-156">筆記</span><span class="sxs-lookup"><span data-stu-id="808c3-156">NOTES</span></span>

## <span data-ttu-id="808c3-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="808c3-157">RELATED LINKS</span></span>

[<span data-ttu-id="808c3-158">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="808c3-158">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="808c3-159">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="808c3-159">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="808c3-160">New-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="808c3-160">New-AzNetworkInterface</span></span>](./New-AzNetworkInterface.md)

[<span data-ttu-id="808c3-161">Remove-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="808c3-161">Remove-AzNetworkInterface</span></span>](./Remove-AzNetworkInterface.md)
