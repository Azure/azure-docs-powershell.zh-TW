---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 92F192A5-F75E-4EFE-B2D2-B0DF0B78D3B5
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azvmssipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssIpConfig.md
ms.openlocfilehash: 30dbe52805017a00f24cc95c832386545ae036e0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905182"
---
# <span data-ttu-id="a787c-101">New-AzVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="a787c-101">New-AzVmssIpConfig</span></span>

## <span data-ttu-id="a787c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a787c-102">SYNOPSIS</span></span>
<span data-ttu-id="a787c-103">為 VMSS 的網路介面建立 IP 組。</span><span class="sxs-lookup"><span data-stu-id="a787c-103">Creates an IP configuration for a network interface of a VMSS.</span></span>

## <span data-ttu-id="a787c-104">語法</span><span class="sxs-lookup"><span data-stu-id="a787c-104">SYNTAX</span></span>

```
New-AzVmssIpConfig [[-Name] <String>] [[-Id] <String>] [[-SubnetId] <String>]
 [[-ApplicationGatewayBackendAddressPoolsId] <String[]>] [[-LoadBalancerBackendAddressPoolsId] <String[]>]
 [[-LoadBalancerInboundNatPoolsId] <String[]>] [-Primary] [-PrivateIPAddressVersion <String>]
 [-PublicIPAddressConfigurationName <String>] [-PublicIPAddressConfigurationIdleTimeoutInMinutes <Int32>]
 [-DnsSetting <String>] [-IpTag <VirtualMachineScaleSetIpTag[]>] [-PublicIPPrefix <String>]
 [-PublicIPAddressVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a787c-105">描述</span><span class="sxs-lookup"><span data-stu-id="a787c-105">DESCRIPTION</span></span>
<span data-ttu-id="a787c-106">**New-Az VmssIpConfig** Cmdlet 會為虛擬機器規模集 (VMSS) 的網路介面建立 IP 設定) 。</span><span class="sxs-lookup"><span data-stu-id="a787c-106">The **New-AzVmssIpConfig** cmdlet creates an IP configuration object for a network interface of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="a787c-107">指定此 Cmdlet 的設定為 Add-AzVmssNetworkInterfaceConfiguration Cmdlet 的 *IPConfiguration* 參數。</span><span class="sxs-lookup"><span data-stu-id="a787c-107">Specify the configuration from this cmdlet as the *IPConfiguration* parameter of the Add-AzVmssNetworkInterfaceConfiguration cmdlet.</span></span>

## <span data-ttu-id="a787c-108">例子</span><span class="sxs-lookup"><span data-stu-id="a787c-108">EXAMPLES</span></span>

### <span data-ttu-id="a787c-109">範例 1：為 VMSS 介面建立 IP 組組物件</span><span class="sxs-lookup"><span data-stu-id="a787c-109">Example 1: Create an IP configuration object for a VMSS interface</span></span>
```
PS C:\> $IPConfiguration = New-AzVmssIPConfig -Name "ContosoVmssInterface02" -SubnetId $SubnetId
```

<span data-ttu-id="a787c-110">此命令會建立一個名為 ContosoEvsInterface02 的 IP 組式物件。</span><span class="sxs-lookup"><span data-stu-id="a787c-110">This command creates an IP configuration object named ContosoVmssInterface02.</span></span>
<span data-ttu-id="a787c-111">該命令使用先前定義的子網識別碼，儲存在 $SubnetId。</span><span class="sxs-lookup"><span data-stu-id="a787c-111">The command uses a previously defined subnet ID stored in $SubnetId.</span></span>
<span data-ttu-id="a787c-112">命令會儲存 $IPConfiguration 變數中的設定，供日後與 **Add-AzEvssNetworkInterfaceConfiguration 一起使用**。</span><span class="sxs-lookup"><span data-stu-id="a787c-112">The command stores the configuration settings in the $IPConfiguration variable for later use with **Add-AzVmssNetworkInterfaceConfiguration**.</span></span>

### <span data-ttu-id="a787c-113">範例 2：建立包含 NAT 區設定之 IP 設定物件</span><span class="sxs-lookup"><span data-stu-id="a787c-113">Example 2: Create an IP configuration object that includes NAT pool settings</span></span>
```
PS C:\> $IPConfiguration = New-AzVmssIPConfig -Name "ContosoVmssInterface03" -LoadBalancerInboundNatPoolsId $expectedLb.InboundNatPools[0].Id -LoadBalancerBackendAddressPoolsId $expectedLb.BackendAddressPools[0].Id -SubnetId $SubnetId
```

<span data-ttu-id="a787c-114">此命令會建立一個名為 ContosoEvsInterface03 的 IP 組$IPConfiguration，供日後使用。</span><span class="sxs-lookup"><span data-stu-id="a787c-114">This command creates an IP configuration object named ContosoVmssInterface03, and then stores it in the $IPConfiguration variable for later use.</span></span>
<span data-ttu-id="a787c-115">該命令使用先前定義的子網識別碼，儲存在 $SubnetId。</span><span class="sxs-lookup"><span data-stu-id="a787c-115">The command uses a previously defined subnet ID stored in $SubnetId.</span></span>
<span data-ttu-id="a787c-116">命令會儲存設定設定$IPConfiguration變數中，供日後使用。</span><span class="sxs-lookup"><span data-stu-id="a787c-116">The command stores the configuration settings in the $IPConfiguration variable for later use.</span></span>
<span data-ttu-id="a787c-117">該命令會指定 *LoadBalancerInboundNatPoolsId* 和 *LoadBalancerBackendAddressPoolsId 參數* 的值。</span><span class="sxs-lookup"><span data-stu-id="a787c-117">The command specifies values for the *LoadBalancerInboundNatPoolsId* and *LoadBalancerBackendAddressPoolsId* parameters.</span></span>

## <span data-ttu-id="a787c-118">參數</span><span class="sxs-lookup"><span data-stu-id="a787c-118">PARAMETERS</span></span>

### <span data-ttu-id="a787c-119">-ApplicationGatewayBackendAddressPoolsId</span><span class="sxs-lookup"><span data-stu-id="a787c-119">-ApplicationGatewayBackendAddressPoolsId</span></span>
<span data-ttu-id="a787c-120">指定負載平衡器後端位址資料庫的參照陣列。</span><span class="sxs-lookup"><span data-stu-id="a787c-120">Specifies an array of references to backend address pools of load balancers.</span></span>
<span data-ttu-id="a787c-121">縮放集可參照一個公用和一個內部負載平衡器後端位址集區。</span><span class="sxs-lookup"><span data-stu-id="a787c-121">A scale set can reference backend address pools of one public and one internal load balancer.</span></span>
<span data-ttu-id="a787c-122">多個縮放比例集無法使用相同的負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="a787c-122">Multiple scale sets cannot use the same load balancer.</span></span>

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

### <span data-ttu-id="a787c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a787c-123">-DefaultProfile</span></span>
<span data-ttu-id="a787c-124">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a787c-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a787c-125">-DnsSetting</span><span class="sxs-lookup"><span data-stu-id="a787c-125">-DnsSetting</span></span>
<span data-ttu-id="a787c-126">要用於公用IP 位址的 dns 設定。</span><span class="sxs-lookup"><span data-stu-id="a787c-126">The dns settings to be applied on the publicIP addresses.</span></span>
<span data-ttu-id="a787c-127">要用於公用IP 位址的 Dns 設定功能變數名稱標籤。</span><span class="sxs-lookup"><span data-stu-id="a787c-127">The domain name label of the Dns settings to be applied on the publicIP addresses.</span></span>
<span data-ttu-id="a787c-128">功能變數名稱標籤和 vm 索引的連系將會是所建立之公用 IP 位址資源的功能變數名稱標籤。</span><span class="sxs-lookup"><span data-stu-id="a787c-128">The concatenation of the domain name label and vm index will be the domain name labels of the Public IP Address resources that will be created.</span></span>

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

### <span data-ttu-id="a787c-129">-Id</span><span class="sxs-lookup"><span data-stu-id="a787c-129">-Id</span></span>
<span data-ttu-id="a787c-130">指定識別碼。</span><span class="sxs-lookup"><span data-stu-id="a787c-130">Specifies an ID.</span></span>

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

### <span data-ttu-id="a787c-131">-IpTag</span><span class="sxs-lookup"><span data-stu-id="a787c-131">-IpTag</span></span>
<span data-ttu-id="a787c-132">指定 Ip Tag 物件的陣列。</span><span class="sxs-lookup"><span data-stu-id="a787c-132">Specifies an array of Ip Tag objects.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIpTag[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a787c-133">-LoadBalancerBackendAddressPoolsId</span><span class="sxs-lookup"><span data-stu-id="a787c-133">-LoadBalancerBackendAddressPoolsId</span></span>
<span data-ttu-id="a787c-134">指定呼叫負載平衡器之 NAT (NAT) 傳入網路位址轉譯的陣列。</span><span class="sxs-lookup"><span data-stu-id="a787c-134">Specifies an array of references to incoming network address translation (NAT) pools of the load balancers.</span></span>
<span data-ttu-id="a787c-135">縮放集可參照一個公用和一個內部負載平衡器的內部 NAT 集區。</span><span class="sxs-lookup"><span data-stu-id="a787c-135">A scale set can reference incoming NAT pools of one public and one internal load balancer.</span></span>
<span data-ttu-id="a787c-136">多個縮放比例集無法使用相同的負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="a787c-136">Multiple scale sets cannot use the same load balancer.</span></span>

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

### <span data-ttu-id="a787c-137">-LoadBalancerInboundNatPoolsId</span><span class="sxs-lookup"><span data-stu-id="a787c-137">-LoadBalancerInboundNatPoolsId</span></span>
<span data-ttu-id="a787c-138">指定負載平衡器傳入 NAT 資料庫的參照陣列。</span><span class="sxs-lookup"><span data-stu-id="a787c-138">Specifies an array of references to incoming NAT pools of the load balancers.</span></span>
<span data-ttu-id="a787c-139">縮放集可參照一個公用和一個內部負載平衡器的內部 NAT 集區。</span><span class="sxs-lookup"><span data-stu-id="a787c-139">A scale set can reference incoming NAT pools of one public and one internal load balancer.</span></span>
<span data-ttu-id="a787c-140">多個縮放比例集無法使用相同的負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="a787c-140">Multiple scale sets cannot use the same load balancer.</span></span>

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

### <span data-ttu-id="a787c-141">-名稱</span><span class="sxs-lookup"><span data-stu-id="a787c-141">-Name</span></span>
<span data-ttu-id="a787c-142">指定 IP 組名。</span><span class="sxs-lookup"><span data-stu-id="a787c-142">Specifies the name of the IP configuration.</span></span>

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

### <span data-ttu-id="a787c-143">-主要</span><span class="sxs-lookup"><span data-stu-id="a787c-143">-Primary</span></span>
<span data-ttu-id="a787c-144">指定主要 IP 群組原則，以防網路介面具有多個 IP 群組原則。</span><span class="sxs-lookup"><span data-stu-id="a787c-144">Specifies the primary IP Configuration in case the network interface has more than one IP Configuration.</span></span>

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

### <span data-ttu-id="a787c-145">-PrivateIPAddressVersion</span><span class="sxs-lookup"><span data-stu-id="a787c-145">-PrivateIPAddressVersion</span></span>
<span data-ttu-id="a787c-146">指定私人 IP 位址的 IP 群組原則。</span><span class="sxs-lookup"><span data-stu-id="a787c-146">Specify the IP configuration for private IP address.</span></span>  <span data-ttu-id="a787c-147">預設值會視為 IPv4。</span><span class="sxs-lookup"><span data-stu-id="a787c-147">Default is taken as IPv4.</span></span>  <span data-ttu-id="a787c-148">可能的值為：'IPv4' 和 'IPv6'。</span><span class="sxs-lookup"><span data-stu-id="a787c-148">Possible values are: 'IPv4' and 'IPv6'.</span></span>

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

### <span data-ttu-id="a787c-149">-PublicIPAddressConfigurationIdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="a787c-149">-PublicIPAddressConfigurationIdleTimeoutInMinutes</span></span>
<span data-ttu-id="a787c-150">公用 IP 位址的閒置超時。</span><span class="sxs-lookup"><span data-stu-id="a787c-150">The idle timeout of the public IP address.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: PublicIPAddressIdleTimeoutInMinutes

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a787c-151">-PublicIPAddressConfigurationName</span><span class="sxs-lookup"><span data-stu-id="a787c-151">-PublicIPAddressConfigurationName</span></span>
<span data-ttu-id="a787c-152">公用IP 位址組組名稱。</span><span class="sxs-lookup"><span data-stu-id="a787c-152">The publicIP address configuration name.</span></span>

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

### <span data-ttu-id="a787c-153">-PublicIPAddressVersion</span><span class="sxs-lookup"><span data-stu-id="a787c-153">-PublicIPAddressVersion</span></span>
<span data-ttu-id="a787c-154">指定公用 IP 位址的 IP 群組原則。</span><span class="sxs-lookup"><span data-stu-id="a787c-154">Specify the IP configuration for public IP address.</span></span>  <span data-ttu-id="a787c-155">預設值會視為 IPv4。</span><span class="sxs-lookup"><span data-stu-id="a787c-155">Default is taken as IPv4.</span></span>  <span data-ttu-id="a787c-156">可能的值為：'IPv4' 和 'IPv6'。</span><span class="sxs-lookup"><span data-stu-id="a787c-156">Possible values are: 'IPv4' and 'IPv6'.</span></span>

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

### <span data-ttu-id="a787c-157">-PublicIPPrefix</span><span class="sxs-lookup"><span data-stu-id="a787c-157">-PublicIPPrefix</span></span>
<span data-ttu-id="a787c-158">公用 IP 首碼的識別碼</span><span class="sxs-lookup"><span data-stu-id="a787c-158">The ID of Public IP Prefix</span></span>

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

### <span data-ttu-id="a787c-159">-子網Id</span><span class="sxs-lookup"><span data-stu-id="a787c-159">-SubnetId</span></span>
<span data-ttu-id="a787c-160">指定群組原則建立 VMSS 網路介面的子網識別碼。</span><span class="sxs-lookup"><span data-stu-id="a787c-160">Specifies the subnet ID in which the configuration creates  the VMSS network interface.</span></span>

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

### <span data-ttu-id="a787c-161">-確認</span><span class="sxs-lookup"><span data-stu-id="a787c-161">-Confirm</span></span>
<span data-ttu-id="a787c-162">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="a787c-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a787c-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a787c-163">-WhatIf</span></span>
<span data-ttu-id="a787c-164">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a787c-164">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a787c-165">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a787c-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a787c-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a787c-166">CommonParameters</span></span>
<span data-ttu-id="a787c-167">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a787c-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a787c-168">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a787c-168">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a787c-169">輸入</span><span class="sxs-lookup"><span data-stu-id="a787c-169">INPUTS</span></span>

### <span data-ttu-id="a787c-170">System.String</span><span class="sxs-lookup"><span data-stu-id="a787c-170">System.String</span></span>

### <span data-ttu-id="a787c-171">System.String[]</span><span class="sxs-lookup"><span data-stu-id="a787c-171">System.String[]</span></span>

### <span data-ttu-id="a787c-172">System.Int32</span><span class="sxs-lookup"><span data-stu-id="a787c-172">System.Int32</span></span>

### <span data-ttu-id="a787c-173">Microsoft.Azure.management.Compute.models.VirtualMachineScaleSetipTag[]</span><span class="sxs-lookup"><span data-stu-id="a787c-173">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIpTag[]</span></span>

## <span data-ttu-id="a787c-174">輸出</span><span class="sxs-lookup"><span data-stu-id="a787c-174">OUTPUTS</span></span>

### <span data-ttu-id="a787c-175">Microsoft.Azure.management.Compute.models.VirtualMachineScaleSetIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="a787c-175">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIPConfiguration</span></span>

## <span data-ttu-id="a787c-176">筆記</span><span class="sxs-lookup"><span data-stu-id="a787c-176">NOTES</span></span>

## <span data-ttu-id="a787c-177">相關連結</span><span class="sxs-lookup"><span data-stu-id="a787c-177">RELATED LINKS</span></span>

[<span data-ttu-id="a787c-178">Add-AzEvssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="a787c-178">Add-AzVmssNetworkInterfaceConfiguration</span></span>](./Add-AzVmssNetworkInterfaceConfiguration.md)


