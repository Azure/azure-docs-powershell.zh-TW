---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: BAC2FA68-1D82-411D-A853-FD4EE525B533
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmssnetworkinterfaceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmVmssNetworkInterfaceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmVmssNetworkInterfaceConfiguration.md
ms.openlocfilehash: 6789b2a0f3309e8011cc6e87a27dbf9f28579d05
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449251"
---
# <span data-ttu-id="4307f-101">Add-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="4307f-101">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="4307f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4307f-102">SYNOPSIS</span></span>
<span data-ttu-id="4307f-103">將網路介面設定新增至 VMSS。</span><span class="sxs-lookup"><span data-stu-id="4307f-103">Adds a network interface configuration to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4307f-104">句法</span><span class="sxs-lookup"><span data-stu-id="4307f-104">SYNTAX</span></span>

```
Add-AzureRmVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-Name] <String>] [[-Primary] <Boolean>] [[-Id] <String>]
 [[-IpConfiguration] <VirtualMachineScaleSetIPConfiguration[]>] [-EnableAcceleratedNetworking]
 [-EnableIPForwarding] [-NetworkSecurityGroupId <String>] [-DnsSettingsDnsServer <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4307f-105">說明</span><span class="sxs-lookup"><span data-stu-id="4307f-105">DESCRIPTION</span></span>
<span data-ttu-id="4307f-106">**AzureRmVmssNetworkInterfaceConfiguration** Cmdlet 會將網路介面設定新增到虛擬電腦規模集， (VMSS) 。</span><span class="sxs-lookup"><span data-stu-id="4307f-106">The **Add-AzureRmVmssNetworkInterfaceConfiguration** cmdlet adds a network interface configuration to the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="4307f-107">示例</span><span class="sxs-lookup"><span data-stu-id="4307f-107">EXAMPLES</span></span>

### <span data-ttu-id="4307f-108">範例1：將網路介面設定新增至 VMSS</span><span class="sxs-lookup"><span data-stu-id="4307f-108">Example 1: Add a network interface configuration to the VMSS</span></span>
```
PS C:\> Add-AzureRmVmssNetworkInterfaceConfiguration -VirtualMachineScaleSet $VMSS -Name "Test" -Primary $True -IPConfiguration $IPCfg
```

<span data-ttu-id="4307f-109">這個命令會將網路介面設定新增至 VMSS。</span><span class="sxs-lookup"><span data-stu-id="4307f-109">This command adds a network interface configuration to the VMSS.</span></span>

## <span data-ttu-id="4307f-110">參數</span><span class="sxs-lookup"><span data-stu-id="4307f-110">PARAMETERS</span></span>

### <span data-ttu-id="4307f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4307f-111">-DefaultProfile</span></span>
<span data-ttu-id="4307f-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4307f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4307f-113">-DnsSettingsDnsServer</span><span class="sxs-lookup"><span data-stu-id="4307f-113">-DnsSettingsDnsServer</span></span>
<span data-ttu-id="4307f-114">Dns 設定的 dns 伺服器 IP 位址清單。</span><span class="sxs-lookup"><span data-stu-id="4307f-114">List of dns server IP addresses for dns settings.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: DnsServer

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4307f-115">-EnableAcceleratedNetworking</span><span class="sxs-lookup"><span data-stu-id="4307f-115">-EnableAcceleratedNetworking</span></span>
<span data-ttu-id="4307f-116">指定網路介面是否為已加速網路的功能。</span><span class="sxs-lookup"><span data-stu-id="4307f-116">Specifies whether the network interface is accelerated networking-enabled.</span></span>

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

### <span data-ttu-id="4307f-117">-EnableIPForwarding</span><span class="sxs-lookup"><span data-stu-id="4307f-117">-EnableIPForwarding</span></span>
<span data-ttu-id="4307f-118">指定是否在這個 NIC 上啟用 IP 轉寄。</span><span class="sxs-lookup"><span data-stu-id="4307f-118">Specifies whether IP forwarding enabled on this NIC.</span></span>

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

### <span data-ttu-id="4307f-119">-識別碼</span><span class="sxs-lookup"><span data-stu-id="4307f-119">-Id</span></span>
<span data-ttu-id="4307f-120">指定虛擬機器的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="4307f-120">Specifies the Resource ID of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4307f-121">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="4307f-121">-IpConfiguration</span></span>
<span data-ttu-id="4307f-122">指定網路介面的 IP 配置。</span><span class="sxs-lookup"><span data-stu-id="4307f-122">Specifies the IP configurations of the network interface.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIPConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4307f-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="4307f-123">-Name</span></span>
<span data-ttu-id="4307f-124">指定網路介面配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="4307f-124">Specifies the name of the network interface configuration.</span></span>

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

### <span data-ttu-id="4307f-125">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="4307f-125">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="4307f-126">網路安全性群組的 Id。</span><span class="sxs-lookup"><span data-stu-id="4307f-126">Id of the network security group.</span></span>

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

### <span data-ttu-id="4307f-127">-主要</span><span class="sxs-lookup"><span data-stu-id="4307f-127">-Primary</span></span>
<span data-ttu-id="4307f-128">指出從網路介面設定建立的網路介面是否將是虛擬機器的主要網路資訊中心 (NIC) 。</span><span class="sxs-lookup"><span data-stu-id="4307f-128">Indicates whether network interfaces created from the network interface configuration will be the primary network information center (NIC) of the virtual machine.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4307f-129">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="4307f-129">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="4307f-130">指定 VMSS 物件。</span><span class="sxs-lookup"><span data-stu-id="4307f-130">Specifies the VMSS object.</span></span>
<span data-ttu-id="4307f-131">您可以使用 [新的-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) Cmdlet 來建立物件。</span><span class="sxs-lookup"><span data-stu-id="4307f-131">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create the object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4307f-132">-確認</span><span class="sxs-lookup"><span data-stu-id="4307f-132">-Confirm</span></span>
<span data-ttu-id="4307f-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4307f-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4307f-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4307f-134">-WhatIf</span></span>
<span data-ttu-id="4307f-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4307f-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4307f-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4307f-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4307f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4307f-137">CommonParameters</span></span>
<span data-ttu-id="4307f-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4307f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4307f-139">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4307f-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4307f-140">輸入</span><span class="sxs-lookup"><span data-stu-id="4307f-140">INPUTS</span></span>

### <span data-ttu-id="4307f-141">PSVirtualMachineScaleSet 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="4307f-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="4307f-142">System.object</span><span class="sxs-lookup"><span data-stu-id="4307f-142">System.String</span></span>

### <span data-ttu-id="4307f-143">系統為 Nullable "1 [[System.object，mscorlib，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="4307f-143">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="4307f-144">VirtualMachineScaleSetIPConfiguration [] 的計算模型。</span><span class="sxs-lookup"><span data-stu-id="4307f-144">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIPConfiguration[]</span></span>

### <span data-ttu-id="4307f-145">System.object []</span><span class="sxs-lookup"><span data-stu-id="4307f-145">System.String[]</span></span>

## <span data-ttu-id="4307f-146">輸出</span><span class="sxs-lookup"><span data-stu-id="4307f-146">OUTPUTS</span></span>

### <span data-ttu-id="4307f-147">PSVirtualMachineScaleSet 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="4307f-147">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="4307f-148">筆記</span><span class="sxs-lookup"><span data-stu-id="4307f-148">NOTES</span></span>

## <span data-ttu-id="4307f-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="4307f-149">RELATED LINKS</span></span>

[<span data-ttu-id="4307f-150">新-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="4307f-150">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)