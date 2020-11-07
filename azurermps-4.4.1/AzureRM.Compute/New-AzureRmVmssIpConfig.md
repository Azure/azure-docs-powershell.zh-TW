---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 92F192A5-F75E-4EFE-B2D2-B0DF0B78D3B5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVmssIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVmssIpConfig.md
ms.openlocfilehash: 1ea3da37c0844d155f8f837f2a00064fafbf9f1e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626017"
---
# <span data-ttu-id="cc128-101">New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="cc128-101">New-AzureRmVmssIpConfig</span></span>

## <span data-ttu-id="cc128-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cc128-102">SYNOPSIS</span></span>
<span data-ttu-id="cc128-103">為 VMSS 的網路介面建立 IP 配置。</span><span class="sxs-lookup"><span data-stu-id="cc128-103">Creates an IP configuration for a network interface of a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cc128-104">句法</span><span class="sxs-lookup"><span data-stu-id="cc128-104">SYNTAX</span></span>

```
New-AzureRmVmssIpConfig [[-Name] <String>] [[-Id] <String>] [[-SubnetId] <String>]
 [[-ApplicationGatewayBackendAddressPoolsId] <String[]>] [[-LoadBalancerBackendAddressPoolsId] <String[]>]
 [[-LoadBalancerInboundNatPoolsId] <String[]>] [-Primary] [-PrivateIPAddressVersion <String>]
 [-PublicIPAddressConfigurationName <String>] [-PublicIPAddressConfigurationIdleTimeoutInMinutes <Int32>]
 [-DnsSetting <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc128-105">說明</span><span class="sxs-lookup"><span data-stu-id="cc128-105">DESCRIPTION</span></span>
<span data-ttu-id="cc128-106">**新的-AzureRmVmssIpConfig** Cmdlet 會為虛擬機器縮放集 (VMSS) 的網路介面建立 IP 設定物件。</span><span class="sxs-lookup"><span data-stu-id="cc128-106">The **New-AzureRmVmssIpConfig** cmdlet creates an IP configuration object for a network interface of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="cc128-107">將此 Cmdlet 的配置指定為 Add-AzureRmVmssNetworkInterfaceConfiguration Cmdlet 的 *IPConfiguration* 參數。</span><span class="sxs-lookup"><span data-stu-id="cc128-107">Specify the configuration from this cmdlet as the *IPConfiguration* parameter of the Add-AzureRmVmssNetworkInterfaceConfiguration cmdlet.</span></span>

## <span data-ttu-id="cc128-108">示例</span><span class="sxs-lookup"><span data-stu-id="cc128-108">EXAMPLES</span></span>

### <span data-ttu-id="cc128-109">範例1：建立 VMSS 介面的 IP 設定物件</span><span class="sxs-lookup"><span data-stu-id="cc128-109">Example 1: Create an IP configuration object for a VMSS interface</span></span>
```
PS C:\> $IPConfiguration = New-AzureRmVmssIPConfig -Name "ContosoVmssInterface02" -SubnetId $SubnetId
```

<span data-ttu-id="cc128-110">這個命令會建立名為 ContosoVmssInterface02 的 IP 設定物件。</span><span class="sxs-lookup"><span data-stu-id="cc128-110">This command creates an IP configuration object named ContosoVmssInterface02.</span></span>
<span data-ttu-id="cc128-111">此命令會使用 $SubnetId 中儲存的先前定義子網 ID。</span><span class="sxs-lookup"><span data-stu-id="cc128-111">The command uses a previously defined subnet ID stored in $SubnetId.</span></span>
<span data-ttu-id="cc128-112">此命令會將設定設定儲存在 $IPConfiguration 變數中，以便日後與 **AzureRmVmssNetworkInterfaceConfiguration** 搭配使用。</span><span class="sxs-lookup"><span data-stu-id="cc128-112">The command stores the configuration settings in the $IPConfiguration variable for later use with **Add-AzureRmVmssNetworkInterfaceConfiguration**.</span></span>

### <span data-ttu-id="cc128-113">範例2：建立包含 NAT 池設定的 IP 設定物件</span><span class="sxs-lookup"><span data-stu-id="cc128-113">Example 2: Create an IP configuration object that includes NAT pool settings</span></span>
```
PS C:\> $IPConfiguration = New-AzureRmVmssIPConfig -Name "ContosoVmssInterface03" -LoadBalancerInboundNatPoolsId $expectedLb.InboundNatPools[0].Id -LoadBalancerBackendAddressPoolsId $expectedLb.BackendAddressPools[0].Id -SubnetId $SubnetId
```

<span data-ttu-id="cc128-114">這個命令會建立名為 ContosoVmssInterface03 的 IP 設定物件，然後將它儲存在 $IPConfiguration 變數中供日後使用。</span><span class="sxs-lookup"><span data-stu-id="cc128-114">This command creates an IP configuration object named ContosoVmssInterface03, and then stores it in the $IPConfiguration variable for later use.</span></span>
<span data-ttu-id="cc128-115">此命令會使用 $SubnetId 中儲存的先前定義子網 ID。</span><span class="sxs-lookup"><span data-stu-id="cc128-115">The command uses a previously defined subnet ID stored in $SubnetId.</span></span>
<span data-ttu-id="cc128-116">該命令會將設定設定儲存在 $IPConfiguration 變數中，以供日後使用。</span><span class="sxs-lookup"><span data-stu-id="cc128-116">The command stores the configuration settings in the $IPConfiguration variable for later use.</span></span>
<span data-ttu-id="cc128-117">此命令會指定 *LoadBalancerInboundNatPoolsId* 和 *LoadBalancerBackendAddressPoolsId* 參數的值。</span><span class="sxs-lookup"><span data-stu-id="cc128-117">The command specifies values for the *LoadBalancerInboundNatPoolsId* and *LoadBalancerBackendAddressPoolsId* parameters.</span></span>

## <span data-ttu-id="cc128-118">參數</span><span class="sxs-lookup"><span data-stu-id="cc128-118">PARAMETERS</span></span>

### <span data-ttu-id="cc128-119">-ApplicationGatewayBackendAddressPoolsId</span><span class="sxs-lookup"><span data-stu-id="cc128-119">-ApplicationGatewayBackendAddressPoolsId</span></span>
<span data-ttu-id="cc128-120">指定 [負載平衡器] 後端位址集區的參照陣列。</span><span class="sxs-lookup"><span data-stu-id="cc128-120">Specifies an array of references to backend address pools of load balancers.</span></span>
<span data-ttu-id="cc128-121">比例集可以參照一個公用與一個內部負載平衡器的後端位址集區。</span><span class="sxs-lookup"><span data-stu-id="cc128-121">A scale set can reference backend address pools of one public and one internal load balancer.</span></span>
<span data-ttu-id="cc128-122">多個規模集不能使用相同的負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="cc128-122">Multiple scale sets cannot use the same load balancer.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc128-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc128-123">-DefaultProfile</span></span>
<span data-ttu-id="cc128-124">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="cc128-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc128-125">-DnsSetting</span><span class="sxs-lookup"><span data-stu-id="cc128-125">-DnsSetting</span></span>
<span data-ttu-id="cc128-126">要套用於 publicIP 位址的 dns 設定。</span><span class="sxs-lookup"><span data-stu-id="cc128-126">The dns settings to be applied on the publicIP addresses.</span></span>
<span data-ttu-id="cc128-127">要套用於 publicIP 位址的 Dns 設定的功能變數名稱標籤。</span><span class="sxs-lookup"><span data-stu-id="cc128-127">The domain name label of the Dns settings to be applied on the publicIP addresses.</span></span>
<span data-ttu-id="cc128-128">網功能變數名稱稱標籤和 vm 索引的串聯將是將要建立之公用 IP 位址資源的功能變數名稱標籤。</span><span class="sxs-lookup"><span data-stu-id="cc128-128">The concatenation of the domain name label and vm index will be the domain name labels of the Public IP Address resources that will be created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PublicIPAddressDomainNameLabel

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc128-129">-識別碼</span><span class="sxs-lookup"><span data-stu-id="cc128-129">-Id</span></span>
<span data-ttu-id="cc128-130">指定 ID。</span><span class="sxs-lookup"><span data-stu-id="cc128-130">Specifies an ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc128-131">-LoadBalancerBackendAddressPoolsId</span><span class="sxs-lookup"><span data-stu-id="cc128-131">-LoadBalancerBackendAddressPoolsId</span></span>
<span data-ttu-id="cc128-132">指定在負載平衡器) 池的傳入網路位址轉譯 (NAT 的參照陣列。</span><span class="sxs-lookup"><span data-stu-id="cc128-132">Specifies an array of references to incoming network address translation (NAT) pools of the load balancers.</span></span>
<span data-ttu-id="cc128-133">比例集可以參照一個公用與一個內部負載平衡器的傳入 NAT 池。</span><span class="sxs-lookup"><span data-stu-id="cc128-133">A scale set can reference incoming NAT pools of one public and one internal load balancer.</span></span>
<span data-ttu-id="cc128-134">多個規模集不能使用相同的負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="cc128-134">Multiple scale sets cannot use the same load balancer.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc128-135">-LoadBalancerInboundNatPoolsId</span><span class="sxs-lookup"><span data-stu-id="cc128-135">-LoadBalancerInboundNatPoolsId</span></span>
<span data-ttu-id="cc128-136">指定到負載平衡器內傳的 NAT 池的參照陣列。</span><span class="sxs-lookup"><span data-stu-id="cc128-136">Specifies an array of references to incoming NAT pools of the load balancers.</span></span>
<span data-ttu-id="cc128-137">比例集可以參照一個公用與一個內部負載平衡器的傳入 NAT 池。</span><span class="sxs-lookup"><span data-stu-id="cc128-137">A scale set can reference incoming NAT pools of one public and one internal load balancer.</span></span>
<span data-ttu-id="cc128-138">多個規模集不能使用相同的負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="cc128-138">Multiple scale sets cannot use the same load balancer.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc128-139">-名稱</span><span class="sxs-lookup"><span data-stu-id="cc128-139">-Name</span></span>
<span data-ttu-id="cc128-140">指定 IP 配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="cc128-140">Specifies the name of the IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc128-141">-主要</span><span class="sxs-lookup"><span data-stu-id="cc128-141">-Primary</span></span>
<span data-ttu-id="cc128-142">指定當網路介面有一個以上的 IP 配置時的主要 IP 設定。</span><span class="sxs-lookup"><span data-stu-id="cc128-142">Specifies the primary IP Configuration in case the network interface has more than one IP Configuration.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc128-143">-PrivateIPAddressVersion</span><span class="sxs-lookup"><span data-stu-id="cc128-143">-PrivateIPAddressVersion</span></span>
<span data-ttu-id="cc128-144">指定 ip 配置是 IPv4 或 IPv6。</span><span class="sxs-lookup"><span data-stu-id="cc128-144">Specify the ip configuration is either IPv4 or IPv6.</span></span> <span data-ttu-id="cc128-145">預設值會做為 IPv4。</span><span class="sxs-lookup"><span data-stu-id="cc128-145">Default is taken as IPv4.</span></span>  <span data-ttu-id="cc128-146">可能的值為： "IPv4" 和 "IPv6"。</span><span class="sxs-lookup"><span data-stu-id="cc128-146">Possible values are: 'IPv4' and 'IPv6'.</span></span>

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

### <span data-ttu-id="cc128-147">-PublicIPAddressConfigurationIdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="cc128-147">-PublicIPAddressConfigurationIdleTimeoutInMinutes</span></span>
<span data-ttu-id="cc128-148">公用 IP 位址的空閒超時。</span><span class="sxs-lookup"><span data-stu-id="cc128-148">The idle timeout of the public IP address.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: PublicIPAddressIdleTimeoutInMinutes

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc128-149">-PublicIPAddressConfigurationName</span><span class="sxs-lookup"><span data-stu-id="cc128-149">-PublicIPAddressConfigurationName</span></span>
<span data-ttu-id="cc128-150">[PublicIP 位址] 配置名稱。</span><span class="sxs-lookup"><span data-stu-id="cc128-150">The publicIP address configuration name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PublicIPAddressName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc128-151">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="cc128-151">-SubnetId</span></span>
<span data-ttu-id="cc128-152">指定設定在其中建立 VMSS 網路介面的子網 ID。</span><span class="sxs-lookup"><span data-stu-id="cc128-152">Specifies the subnet ID in which the configuration creates  the VMSS network interface.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc128-153">-確認</span><span class="sxs-lookup"><span data-stu-id="cc128-153">-Confirm</span></span>
<span data-ttu-id="cc128-154">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="cc128-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc128-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc128-155">-WhatIf</span></span>
<span data-ttu-id="cc128-156">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cc128-156">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cc128-157">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cc128-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc128-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc128-158">CommonParameters</span></span>
<span data-ttu-id="cc128-159">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cc128-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc128-160">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="cc128-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc128-161">輸入</span><span class="sxs-lookup"><span data-stu-id="cc128-161">INPUTS</span></span>

## <span data-ttu-id="cc128-162">輸出</span><span class="sxs-lookup"><span data-stu-id="cc128-162">OUTPUTS</span></span>

## <span data-ttu-id="cc128-163">筆記</span><span class="sxs-lookup"><span data-stu-id="cc128-163">NOTES</span></span>

## <span data-ttu-id="cc128-164">相關連結</span><span class="sxs-lookup"><span data-stu-id="cc128-164">RELATED LINKS</span></span>

[<span data-ttu-id="cc128-165">附加 AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="cc128-165">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>](./Add-AzureRmVmssNetworkInterfaceConfiguration.md)


