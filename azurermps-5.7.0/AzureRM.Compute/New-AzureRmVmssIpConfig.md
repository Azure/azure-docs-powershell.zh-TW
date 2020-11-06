---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 92F192A5-F75E-4EFE-B2D2-B0DF0B78D3B5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVmssIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVmssIpConfig.md
ms.openlocfilehash: 448f6236f5c9545ff1a1194c8103463f78a8fefd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448746"
---
# <span data-ttu-id="8dc18-101">New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="8dc18-101">New-AzureRmVmssIpConfig</span></span>

## <span data-ttu-id="8dc18-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8dc18-102">SYNOPSIS</span></span>
<span data-ttu-id="8dc18-103">為 VMSS 的網路介面建立 IP 配置。</span><span class="sxs-lookup"><span data-stu-id="8dc18-103">Creates an IP configuration for a network interface of a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8dc18-104">句法</span><span class="sxs-lookup"><span data-stu-id="8dc18-104">SYNTAX</span></span>

```
New-AzureRmVmssIpConfig [[-Name] <String>] [[-Id] <String>] [[-SubnetId] <String>]
 [[-ApplicationGatewayBackendAddressPoolsId] <String[]>] [[-LoadBalancerBackendAddressPoolsId] <String[]>]
 [[-LoadBalancerInboundNatPoolsId] <String[]>] [-PrivateIPAddressVersion <String>]
 [-PublicIPAddressConfigurationName <String>] [-PublicIPAddressConfigurationIdleTimeoutInMinutes <Int32>]
 [-DnsSetting <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8dc18-105">說明</span><span class="sxs-lookup"><span data-stu-id="8dc18-105">DESCRIPTION</span></span>
<span data-ttu-id="8dc18-106">**新的-AzureRmVmssIpConfig** Cmdlet 會為虛擬機器縮放集 (VMSS) 的網路介面建立 IP 設定物件。</span><span class="sxs-lookup"><span data-stu-id="8dc18-106">The **New-AzureRmVmssIpConfig** cmdlet creates an IP configuration object for a network interface of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="8dc18-107">將此 Cmdlet 的配置指定為 Add-AzureRmVmssNetworkInterfaceConfiguration Cmdlet 的 *IPConfiguration* 參數。</span><span class="sxs-lookup"><span data-stu-id="8dc18-107">Specify the configuration from this cmdlet as the *IPConfiguration* parameter of the Add-AzureRmVmssNetworkInterfaceConfiguration cmdlet.</span></span>

## <span data-ttu-id="8dc18-108">示例</span><span class="sxs-lookup"><span data-stu-id="8dc18-108">EXAMPLES</span></span>

### <span data-ttu-id="8dc18-109">範例1：建立 VMSS 介面的 IP 設定物件</span><span class="sxs-lookup"><span data-stu-id="8dc18-109">Example 1: Create an IP configuration object for a VMSS interface</span></span>
```
PS C:\> $IPConfiguration = New-AzureRmVmssIPConfig -Name "ContosoVmssInterface02" -SubnetId $SubnetId
```

<span data-ttu-id="8dc18-110">這個命令會建立名為 ContosoVmssInterface02 的 IP 設定物件。</span><span class="sxs-lookup"><span data-stu-id="8dc18-110">This command creates an IP configuration object named ContosoVmssInterface02.</span></span>
<span data-ttu-id="8dc18-111">此命令會使用 $SubnetId 中儲存的先前定義子網 ID。</span><span class="sxs-lookup"><span data-stu-id="8dc18-111">The command uses a previously defined subnet ID stored in $SubnetId.</span></span>
<span data-ttu-id="8dc18-112">此命令會將設定設定儲存在 $IPConfiguration 變數中，以便日後與 **AzureRmVmssNetworkInterfaceConfiguration** 搭配使用。</span><span class="sxs-lookup"><span data-stu-id="8dc18-112">The command stores the configuration settings in the $IPConfiguration variable for later use with **Add-AzureRmVmssNetworkInterfaceConfiguration**.</span></span>

### <span data-ttu-id="8dc18-113">範例2：建立包含 NAT 池設定的 IP 設定物件</span><span class="sxs-lookup"><span data-stu-id="8dc18-113">Example 2: Create an IP configuration object that includes NAT pool settings</span></span>
```
PS C:\> $IPConfiguration = New-AzureRmVmssIPConfig -Name "ContosoVmssInterface03" -LoadBalancerInboundNatPoolsId $expectedLb.InboundNatPools[0].Id -LoadBalancerBackendAddressPoolsId $expectedLb.BackendAddressPools[0].Id -SubnetId $SubnetId
```

<span data-ttu-id="8dc18-114">這個命令會建立名為 ContosoVmssInterface03 的 IP 設定物件，然後將它儲存在 $IPConfiguration 變數中供日後使用。</span><span class="sxs-lookup"><span data-stu-id="8dc18-114">This command creates an IP configuration object named ContosoVmssInterface03, and then stores it in the $IPConfiguration variable for later use.</span></span>
<span data-ttu-id="8dc18-115">此命令會使用 $SubnetId 中儲存的先前定義子網 ID。</span><span class="sxs-lookup"><span data-stu-id="8dc18-115">The command uses a previously defined subnet ID stored in $SubnetId.</span></span>
<span data-ttu-id="8dc18-116">該命令會將設定設定儲存在 $IPConfiguration 變數中，以供日後使用。</span><span class="sxs-lookup"><span data-stu-id="8dc18-116">The command stores the configuration settings in the $IPConfiguration variable for later use.</span></span>
<span data-ttu-id="8dc18-117">此命令會指定 *LoadBalancerInboundNatPoolsId* 和 *LoadBalancerBackendAddressPoolsId* 參數的值。</span><span class="sxs-lookup"><span data-stu-id="8dc18-117">The command specifies values for the *LoadBalancerInboundNatPoolsId* and *LoadBalancerBackendAddressPoolsId* parameters.</span></span>

## <span data-ttu-id="8dc18-118">參數</span><span class="sxs-lookup"><span data-stu-id="8dc18-118">PARAMETERS</span></span>

### <span data-ttu-id="8dc18-119">-ApplicationGatewayBackendAddressPoolsId</span><span class="sxs-lookup"><span data-stu-id="8dc18-119">-ApplicationGatewayBackendAddressPoolsId</span></span>
<span data-ttu-id="8dc18-120">指定 [負載平衡器] 後端位址集區的參照陣列。</span><span class="sxs-lookup"><span data-stu-id="8dc18-120">Specifies an array of references to backend address pools of load balancers.</span></span>
<span data-ttu-id="8dc18-121">比例集可以參照一個公用與一個內部負載平衡器的後端位址集區。</span><span class="sxs-lookup"><span data-stu-id="8dc18-121">A scale set can reference backend address pools of one public and one internal load balancer.</span></span>
<span data-ttu-id="8dc18-122">多個規模集不能使用相同的負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="8dc18-122">Multiple scale sets cannot use the same load balancer.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8dc18-123">-DnsSetting</span><span class="sxs-lookup"><span data-stu-id="8dc18-123">-DnsSetting</span></span>
<span data-ttu-id="8dc18-124">要套用於 publicIP 位址的 dns 設定。</span><span class="sxs-lookup"><span data-stu-id="8dc18-124">The dns settings to be applied on the publicIP addresses.</span></span>
<span data-ttu-id="8dc18-125">要套用於 publicIP 位址的 Dns 設定的功能變數名稱標籤。</span><span class="sxs-lookup"><span data-stu-id="8dc18-125">The domain name label of the Dns settings to be applied on the publicIP addresses.</span></span>
<span data-ttu-id="8dc18-126">網功能變數名稱稱標籤和 vm 索引的串聯將是將要建立之公用 IP 位址資源的功能變數名稱標籤。</span><span class="sxs-lookup"><span data-stu-id="8dc18-126">The concatenation of the domain name label and vm index will be the domain name labels of the Public IP Address resources that will be created.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8dc18-127">-識別碼</span><span class="sxs-lookup"><span data-stu-id="8dc18-127">-Id</span></span>
<span data-ttu-id="8dc18-128">指定 ID。</span><span class="sxs-lookup"><span data-stu-id="8dc18-128">Specifies an ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8dc18-129">-LoadBalancerBackendAddressPoolsId</span><span class="sxs-lookup"><span data-stu-id="8dc18-129">-LoadBalancerBackendAddressPoolsId</span></span>
<span data-ttu-id="8dc18-130">指定在負載平衡器) 池的傳入網路位址轉譯 (NAT 的參照陣列。</span><span class="sxs-lookup"><span data-stu-id="8dc18-130">Specifies an array of references to incoming network address translation (NAT) pools of the load balancers.</span></span>
<span data-ttu-id="8dc18-131">比例集可以參照一個公用與一個內部負載平衡器的傳入 NAT 池。</span><span class="sxs-lookup"><span data-stu-id="8dc18-131">A scale set can reference incoming NAT pools of one public and one internal load balancer.</span></span>
<span data-ttu-id="8dc18-132">多個規模集不能使用相同的負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="8dc18-132">Multiple scale sets cannot use the same load balancer.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8dc18-133">-LoadBalancerInboundNatPoolsId</span><span class="sxs-lookup"><span data-stu-id="8dc18-133">-LoadBalancerInboundNatPoolsId</span></span>
<span data-ttu-id="8dc18-134">指定到負載平衡器內傳的 NAT 池的參照陣列。</span><span class="sxs-lookup"><span data-stu-id="8dc18-134">Specifies an array of references to incoming NAT pools of the load balancers.</span></span>
<span data-ttu-id="8dc18-135">比例集可以參照一個公用與一個內部負載平衡器的傳入 NAT 池。</span><span class="sxs-lookup"><span data-stu-id="8dc18-135">A scale set can reference incoming NAT pools of one public and one internal load balancer.</span></span>
<span data-ttu-id="8dc18-136">多個規模集不能使用相同的負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="8dc18-136">Multiple scale sets cannot use the same load balancer.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8dc18-137">-名稱</span><span class="sxs-lookup"><span data-stu-id="8dc18-137">-Name</span></span>
<span data-ttu-id="8dc18-138">指定 IP 配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="8dc18-138">Specifies the name of the IP configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8dc18-139">-PrivateIPAddressVersion</span><span class="sxs-lookup"><span data-stu-id="8dc18-139">-PrivateIPAddressVersion</span></span>
<span data-ttu-id="8dc18-140">指定 ip 配置是 IPv4 或 IPv6。</span><span class="sxs-lookup"><span data-stu-id="8dc18-140">Specify the ip configuration is either IPv4 or IPv6.</span></span> <span data-ttu-id="8dc18-141">預設值會做為 IPv4。</span><span class="sxs-lookup"><span data-stu-id="8dc18-141">Default is taken as IPv4.</span></span>  <span data-ttu-id="8dc18-142">可能的值為： "IPv4" 和 "IPv6"。</span><span class="sxs-lookup"><span data-stu-id="8dc18-142">Possible values are: 'IPv4' and 'IPv6'.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8dc18-143">-PublicIPAddressConfigurationIdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="8dc18-143">-PublicIPAddressConfigurationIdleTimeoutInMinutes</span></span>
<span data-ttu-id="8dc18-144">公用 IP 位址的空閒超時。</span><span class="sxs-lookup"><span data-stu-id="8dc18-144">The idle timeout of the public IP address.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8dc18-145">-PublicIPAddressConfigurationName</span><span class="sxs-lookup"><span data-stu-id="8dc18-145">-PublicIPAddressConfigurationName</span></span>
<span data-ttu-id="8dc18-146">[PublicIP 位址] 配置名稱。</span><span class="sxs-lookup"><span data-stu-id="8dc18-146">The publicIP address configuration name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8dc18-147">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="8dc18-147">-SubnetId</span></span>
<span data-ttu-id="8dc18-148">指定設定在其中建立 VMSS 網路介面的子網 ID。</span><span class="sxs-lookup"><span data-stu-id="8dc18-148">Specifies the subnet ID in which the configuration creates  the VMSS network interface.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8dc18-149">-確認</span><span class="sxs-lookup"><span data-stu-id="8dc18-149">-Confirm</span></span>
<span data-ttu-id="8dc18-150">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8dc18-150">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dc18-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8dc18-151">-WhatIf</span></span>
<span data-ttu-id="8dc18-152">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8dc18-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8dc18-153">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8dc18-153">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dc18-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8dc18-154">CommonParameters</span></span>
<span data-ttu-id="8dc18-155">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8dc18-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8dc18-156">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8dc18-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8dc18-157">輸入</span><span class="sxs-lookup"><span data-stu-id="8dc18-157">INPUTS</span></span>

### <span data-ttu-id="8dc18-158">所有</span><span class="sxs-lookup"><span data-stu-id="8dc18-158">None</span></span>
<span data-ttu-id="8dc18-159">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="8dc18-159">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8dc18-160">輸出</span><span class="sxs-lookup"><span data-stu-id="8dc18-160">OUTPUTS</span></span>

## <span data-ttu-id="8dc18-161">筆記</span><span class="sxs-lookup"><span data-stu-id="8dc18-161">NOTES</span></span>

## <span data-ttu-id="8dc18-162">相關連結</span><span class="sxs-lookup"><span data-stu-id="8dc18-162">RELATED LINKS</span></span>

[<span data-ttu-id="8dc18-163">附加 AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="8dc18-163">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>](./Add-AzureRmVmssNetworkInterfaceConfiguration.md)


