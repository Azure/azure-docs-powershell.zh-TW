---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DDB38A77-E5C0-47DD-BADD-94488F661CD5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterface.md
ms.openlocfilehash: 9b851bcbaa545dee99628dc066956854181df7f7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94136219"
---
# <span data-ttu-id="7dd50-101">Set-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="7dd50-101">Set-AzNetworkInterface</span></span>

## <span data-ttu-id="7dd50-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7dd50-102">SYNOPSIS</span></span>
<span data-ttu-id="7dd50-103">更新網路介面。</span><span class="sxs-lookup"><span data-stu-id="7dd50-103">Updates a network interface.</span></span>

## <span data-ttu-id="7dd50-104">句法</span><span class="sxs-lookup"><span data-stu-id="7dd50-104">SYNTAX</span></span>

```
Set-AzNetworkInterface -NetworkInterface <PSNetworkInterface> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7dd50-105">說明</span><span class="sxs-lookup"><span data-stu-id="7dd50-105">DESCRIPTION</span></span>
<span data-ttu-id="7dd50-106">**AzNetworkInterface** 會更新網路介面。</span><span class="sxs-lookup"><span data-stu-id="7dd50-106">The **Set-AzNetworkInterface** updates a network interface.</span></span>

## <span data-ttu-id="7dd50-107">示例</span><span class="sxs-lookup"><span data-stu-id="7dd50-107">EXAMPLES</span></span>

### <span data-ttu-id="7dd50-108">範例1：設定網路介面</span><span class="sxs-lookup"><span data-stu-id="7dd50-108">Example 1: Configure a network interface</span></span>
```
$Nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$Nic.IpConfigurations[0].PrivateIpAddress = "10.0.1.20"
$Nic.IpConfigurations[0].PrivateIpAllocationMethod = "Static"
$Nic.Tag = @{Name = "Name"; Value = "Value"}
Set-AzNetworkInterface -NetworkInterface $Nic
```

<span data-ttu-id="7dd50-109">這個範例會設定網路介面。</span><span class="sxs-lookup"><span data-stu-id="7dd50-109">This example configures a network interface.</span></span>
<span data-ttu-id="7dd50-110">第一個命令會在資源群組 ResourceGroup1 中取得名為 NetworkInterface1 的網路介面。</span><span class="sxs-lookup"><span data-stu-id="7dd50-110">The first command gets a network interface named NetworkInterface1 in resource group ResourceGroup1.</span></span>
<span data-ttu-id="7dd50-111">第二個命令會設定 IP 配置的私人 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="7dd50-111">The second command sets the private IP address of the IP configuration.</span></span>
<span data-ttu-id="7dd50-112">第三個命令會將專用 IP 配置方法設定為 Static。</span><span class="sxs-lookup"><span data-stu-id="7dd50-112">The third command sets the private IP allocation method to Static.</span></span>
<span data-ttu-id="7dd50-113">第四個命令會在網路介面上設定標記。</span><span class="sxs-lookup"><span data-stu-id="7dd50-113">The fourth command sets a tag on the network interface.</span></span>
<span data-ttu-id="7dd50-114">第五個命令使用儲存在 $Nic 變數中的資訊來設定網路介面。</span><span class="sxs-lookup"><span data-stu-id="7dd50-114">The fifth command uses the information stored in the $Nic variable to set the network interface.</span></span>

### <span data-ttu-id="7dd50-115">範例2：變更網路介面上的 DNS 設定</span><span class="sxs-lookup"><span data-stu-id="7dd50-115">Example 2: Change DNS settings on a network interface</span></span>
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nic.DnsSettings.DnsServers.Add("192.168.1.100")
$nic | Set-AzNetworkInterface
```

<span data-ttu-id="7dd50-116">第一個命令會取得名為 NetworkInterface1 的網路介面，該網路介面存在於資源群組 ResourceGroup1 中。</span><span class="sxs-lookup"><span data-stu-id="7dd50-116">The first command gets a network interface named NetworkInterface1 that exists within resource group ResourceGroup1.</span></span> <span data-ttu-id="7dd50-117">第二個命令會將 DNS 伺服器192.168.1.100 新增到這個介面。</span><span class="sxs-lookup"><span data-stu-id="7dd50-117">The second command adds DNS server 192.168.1.100 to this interface.</span></span> <span data-ttu-id="7dd50-118">第三個命令會將這些變更套用至網路介面。</span><span class="sxs-lookup"><span data-stu-id="7dd50-118">The third command applies these changes to the network interface.</span></span> <span data-ttu-id="7dd50-119">若要移除 DNS 伺服器，請遵循上面所列的命令，但要取代 "。新增 "with"。第二個命令中的 [移除]。</span><span class="sxs-lookup"><span data-stu-id="7dd50-119">To remove a DNS server, follow the commands listed above, but replace ".Add" with ".Remove" in the second command.</span></span>

### <span data-ttu-id="7dd50-120">範例3：在網路介面上啟用 IP 轉寄</span><span class="sxs-lookup"><span data-stu-id="7dd50-120">Example 3: Enable IP forwarding on a network interface</span></span>
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nic.EnableIPForwarding = 1
$nic | Set-AzNetworkInterface
```

<span data-ttu-id="7dd50-121">第一個命令會取得名為 NetworkInterface1 的現有網路介面，並將它儲存在 $nic 變數中。</span><span class="sxs-lookup"><span data-stu-id="7dd50-121">The first command gets an existing network interface called NetworkInterface1 and stores it in the $nic variable.</span></span> <span data-ttu-id="7dd50-122">第二個命令會將 IP 轉寄值變更為 true。</span><span class="sxs-lookup"><span data-stu-id="7dd50-122">The second command changes the IP forwarding value to true.</span></span> <span data-ttu-id="7dd50-123">最後，第三個命令會將變更套用至網路介面。</span><span class="sxs-lookup"><span data-stu-id="7dd50-123">Finally, the third command applies the changes to the network interface.</span></span> <span data-ttu-id="7dd50-124">若要在網路介面上停用 IP 轉寄功能，請遵循範例範例，但務必將第二個命令改為「$nic。EnableIPForwarding = 0 "。</span><span class="sxs-lookup"><span data-stu-id="7dd50-124">To disable IP forwarding on a network interface, follow the sample example, but be sure to change the second command to "$nic.EnableIPForwarding = 0".</span></span>

### <span data-ttu-id="7dd50-125">範例4：變更網路介面的子網</span><span class="sxs-lookup"><span data-stu-id="7dd50-125">Example 4: Change the subnet of a network interface</span></span>
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$vnet = Get-AzVirtualNetwork -Name VNet1 -ResourceGroupName crosssubcrossversionpeering
$subnet2 = Get-AzVirtualNetworkSubnetConfig -Name Subnet2 -VirtualNetwork $vnet
$nic.IpConfigurations[0].Subnet.Id = $subnet2.Id
$nic | Set-AzNetworkInterface
```

<span data-ttu-id="7dd50-126">第一個命令會取得網路介面 NetworkInterface1，並將它儲存在 $nic 變數中。</span><span class="sxs-lookup"><span data-stu-id="7dd50-126">The first command gets the network interface NetworkInterface1 and stores it in the $nic variable.</span></span> <span data-ttu-id="7dd50-127">第二個命令會取得與網路介面將要關聯之子網相關聯的虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="7dd50-127">The second command gets the virtual network associated with the subnet that the network interface is going to be associated with.</span></span> <span data-ttu-id="7dd50-128">第二個命令會取得子網，並將它儲存在 $subnet 2 變數中。</span><span class="sxs-lookup"><span data-stu-id="7dd50-128">The second command gets the subnet and stores it in the $subnet2 variable.</span></span> <span data-ttu-id="7dd50-129">第三個命令會將網路介面的主要私人 IP 位址與新的子網相關聯。</span><span class="sxs-lookup"><span data-stu-id="7dd50-129">The third command associated the primary private IP address of the network interface with the new subnet.</span></span> <span data-ttu-id="7dd50-130">最後，最後一個命令會在網路介面上套用這些變更。</span><span class="sxs-lookup"><span data-stu-id="7dd50-130">Finally the last command applied these changes on the network interface.</span></span>
>[!NOTE] 
><span data-ttu-id="7dd50-131">您必須先動態使用 IP 設定，才能變更子網。</span><span class="sxs-lookup"><span data-stu-id="7dd50-131">The IP configurations must be dynamic before you can change the subnet.</span></span> <span data-ttu-id="7dd50-132">如果您有靜態 IP 設定，請先將它變更為 [動態]，然後再繼續進行。</span><span class="sxs-lookup"><span data-stu-id="7dd50-132">If you have static IP configurations, change then to dynamic before proceeding.</span></span> 
>[!NOTE]
><span data-ttu-id="7dd50-133">如果網路介面有多個 IP 設定，則在執行最後一個 Set-AzNetworkInterface 命令之前，必須完成所有這些 IP 設定的第四個命令。</span><span class="sxs-lookup"><span data-stu-id="7dd50-133">If the network interface has multiple IP configurations, the forth command must be done for all these IP configurations before the final Set-AzNetworkInterface command is executed.</span></span> <span data-ttu-id="7dd50-134">您可以在第四個命令中完成，但將 "0" 取代為適當的數位。</span><span class="sxs-lookup"><span data-stu-id="7dd50-134">This can be done as in the forth command but by replacing "0" with the appropriate number.</span></span> <span data-ttu-id="7dd50-135">如果網路介面具有 N 個 IP 配置，則必須存在這些命令的 N-1。</span><span class="sxs-lookup"><span data-stu-id="7dd50-135">If a network interface has N IP configurations, then N-1 of these commands must exist.</span></span>

### <span data-ttu-id="7dd50-136">範例5：將網路安全群組關聯/取消關聯至網路介面</span><span class="sxs-lookup"><span data-stu-id="7dd50-136">Example 5: Associate/Dissociate a Network Security Group to a network interface</span></span>
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nsg = Get-AzNetworkSecurityGroup -ResourceGroupName "ResourceGroup1" -Name "MyNSG"
$nic.NetworkSecurityGroup = $nsg
$nic | Set-AzNetworkInterface
```

<span data-ttu-id="7dd50-137">第一個命令會取得名為 NetworkInterface1 的現有網路介面，並將它儲存在 $nic 變數中。</span><span class="sxs-lookup"><span data-stu-id="7dd50-137">The first command gets an existing network interface called NetworkInterface1 and stores it in the $nic variable.</span></span> <span data-ttu-id="7dd50-138">第二個命令會取得一個名為 MyNSG 的現有網路安全性群組，並將它儲存在 $nsg 變數中。</span><span class="sxs-lookup"><span data-stu-id="7dd50-138">The second command gets an existing network security group called MyNSG and stores it in the $nsg variable.</span></span> <span data-ttu-id="7dd50-139">第三個命令會將 $nsg 指派給 $nic。</span><span class="sxs-lookup"><span data-stu-id="7dd50-139">The third command assigns the $nsg to the $nic.</span></span> <span data-ttu-id="7dd50-140">最後，第四個命令會將變更套用至網路介面。</span><span class="sxs-lookup"><span data-stu-id="7dd50-140">Finally, the forth command applies the changes to the Network interface.</span></span> <span data-ttu-id="7dd50-141">若要將網路安全群組與網路介面取消關聯，請在第三個命令中使用 $null 簡單地取代 $nsg。</span><span class="sxs-lookup"><span data-stu-id="7dd50-141">To dissociate network security groups from a network interface, simple replace $nsg in the third command with $null.</span></span>

## <span data-ttu-id="7dd50-142">參數</span><span class="sxs-lookup"><span data-stu-id="7dd50-142">PARAMETERS</span></span>

### <span data-ttu-id="7dd50-143">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7dd50-143">-AsJob</span></span>
<span data-ttu-id="7dd50-144">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="7dd50-144">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7dd50-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7dd50-145">-DefaultProfile</span></span>
<span data-ttu-id="7dd50-146">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7dd50-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7dd50-147">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="7dd50-147">-NetworkInterface</span></span>
<span data-ttu-id="7dd50-148">指定代表要設定網路介面之狀態的網路介面物件。</span><span class="sxs-lookup"><span data-stu-id="7dd50-148">Specifies a network interface object representing the state to which the network interface should be set.</span></span>

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

### <span data-ttu-id="7dd50-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7dd50-149">CommonParameters</span></span>
<span data-ttu-id="7dd50-150">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7dd50-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7dd50-151">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7dd50-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7dd50-152">輸入</span><span class="sxs-lookup"><span data-stu-id="7dd50-152">INPUTS</span></span>

### <span data-ttu-id="7dd50-153">PSNetworkInterface 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="7dd50-153">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="7dd50-154">輸出</span><span class="sxs-lookup"><span data-stu-id="7dd50-154">OUTPUTS</span></span>

### <span data-ttu-id="7dd50-155">PSNetworkInterface 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="7dd50-155">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="7dd50-156">筆記</span><span class="sxs-lookup"><span data-stu-id="7dd50-156">NOTES</span></span>

## <span data-ttu-id="7dd50-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="7dd50-157">RELATED LINKS</span></span>

[<span data-ttu-id="7dd50-158">AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="7dd50-158">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="7dd50-159">AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="7dd50-159">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="7dd50-160">新-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="7dd50-160">New-AzNetworkInterface</span></span>](./New-AzNetworkInterface.md)

[<span data-ttu-id="7dd50-161">移除-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="7dd50-161">Remove-AzNetworkInterface</span></span>](./Remove-AzNetworkInterface.md)
