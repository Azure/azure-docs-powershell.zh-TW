---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: BAC2FA68-1D82-411D-A853-FD4EE525B533
online version: https://docs.microsoft.com/powershell/module/az.compute/add-azvmssnetworkinterfaceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssNetworkInterfaceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssNetworkInterfaceConfiguration.md
ms.openlocfilehash: c85c4292fcae081e50ba98ff873f967f8e32fbac
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906310"
---
# <span data-ttu-id="e2161-101">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="e2161-101">Add-AzVmssNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="e2161-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e2161-102">SYNOPSIS</span></span>
<span data-ttu-id="e2161-103">新增網路介面組配置至 VMSS。</span><span class="sxs-lookup"><span data-stu-id="e2161-103">Adds a network interface configuration to the VMSS.</span></span>

## <span data-ttu-id="e2161-104">語法</span><span class="sxs-lookup"><span data-stu-id="e2161-104">SYNTAX</span></span>

```
Add-AzVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>]
 [[-Primary] <Boolean>] [[-Id] <String>] [[-IpConfiguration] <VirtualMachineScaleSetIPConfiguration[]>]
 [-EnableAcceleratedNetworking] [-EnableIPForwarding] [-NetworkSecurityGroupId <String>]
 [-DnsSettingsDnsServer <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e2161-105">描述</span><span class="sxs-lookup"><span data-stu-id="e2161-105">DESCRIPTION</span></span>
<span data-ttu-id="e2161-106">**Add-Az VmssNetworkInterfaceConfiguration Cmdlet** 會將網路介面設定新增到虛擬機器縮放集 (VMSS) 。</span><span class="sxs-lookup"><span data-stu-id="e2161-106">The **Add-AzVmssNetworkInterfaceConfiguration** cmdlet adds a network interface configuration to the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="e2161-107">例子</span><span class="sxs-lookup"><span data-stu-id="e2161-107">EXAMPLES</span></span>

### <span data-ttu-id="e2161-108">範例 1：在 VMSS 中新增網路介面組</span><span class="sxs-lookup"><span data-stu-id="e2161-108">Example 1: Add a network interface configuration to the VMSS</span></span>
```
PS C:\> Add-AzVmssNetworkInterfaceConfiguration -VirtualMachineScaleSet $VMSS -Name "Test" -Primary $True -IPConfiguration $IPCfg
```

<span data-ttu-id="e2161-109">此命令會將網路介面組配置新增到 VMSS。</span><span class="sxs-lookup"><span data-stu-id="e2161-109">This command adds a network interface configuration to the VMSS.</span></span>

## <span data-ttu-id="e2161-110">參數</span><span class="sxs-lookup"><span data-stu-id="e2161-110">PARAMETERS</span></span>

### <span data-ttu-id="e2161-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2161-111">-DefaultProfile</span></span>
<span data-ttu-id="e2161-112">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="e2161-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e2161-113">-DnsSettingsDnsServer</span><span class="sxs-lookup"><span data-stu-id="e2161-113">-DnsSettingsDnsServer</span></span>
<span data-ttu-id="e2161-114">dns 設定 dns 伺服器 IP 位址清單。</span><span class="sxs-lookup"><span data-stu-id="e2161-114">List of dns server IP addresses for dns settings.</span></span>

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

### <span data-ttu-id="e2161-115">-EnableAcceworkNetworking</span><span class="sxs-lookup"><span data-stu-id="e2161-115">-EnableAcceleratedNetworking</span></span>
<span data-ttu-id="e2161-116">指定網路介面是否已啟用加速網路功能。</span><span class="sxs-lookup"><span data-stu-id="e2161-116">Specifies whether the network interface is accelerated networking-enabled.</span></span>

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

### <span data-ttu-id="e2161-117">-EnableIPForwarding</span><span class="sxs-lookup"><span data-stu-id="e2161-117">-EnableIPForwarding</span></span>
<span data-ttu-id="e2161-118">指定此 NIC 上是否已啟用 IP 轉轉功能。</span><span class="sxs-lookup"><span data-stu-id="e2161-118">Specifies whether IP forwarding enabled on this NIC.</span></span>

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

### <span data-ttu-id="e2161-119">-Id</span><span class="sxs-lookup"><span data-stu-id="e2161-119">-Id</span></span>
<span data-ttu-id="e2161-120">指定虛擬機器的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="e2161-120">Specifies the Resource ID of the virtual machine.</span></span>

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

### <span data-ttu-id="e2161-121">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="e2161-121">-IpConfiguration</span></span>
<span data-ttu-id="e2161-122">指定網路介面的 IP 群組原則。</span><span class="sxs-lookup"><span data-stu-id="e2161-122">Specifies the IP configurations of the network interface.</span></span>

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

### <span data-ttu-id="e2161-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="e2161-123">-Name</span></span>
<span data-ttu-id="e2161-124">指定網路介面組組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e2161-124">Specifies the name of the network interface configuration.</span></span>

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

### <span data-ttu-id="e2161-125">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="e2161-125">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="e2161-126">網路安全性群組識別碼。</span><span class="sxs-lookup"><span data-stu-id="e2161-126">Id of the network security group.</span></span>

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

### <span data-ttu-id="e2161-127">-主要</span><span class="sxs-lookup"><span data-stu-id="e2161-127">-Primary</span></span>
<span data-ttu-id="e2161-128">指出從網路介面組配置建立的網路介面是否會是虛擬機器 (NIC) 的主要網路資訊中心。</span><span class="sxs-lookup"><span data-stu-id="e2161-128">Indicates whether network interfaces created from the network interface configuration will be the primary network information center (NIC) of the virtual machine.</span></span>

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

### <span data-ttu-id="e2161-129">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="e2161-129">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="e2161-130">指定 VMSS 物件。</span><span class="sxs-lookup"><span data-stu-id="e2161-130">Specifies the VMSS object.</span></span>
<span data-ttu-id="e2161-131">您可以使用 [New-AzEvssConfig](./New-AzVmssConfig.md) Cmdlet 來建立物件。</span><span class="sxs-lookup"><span data-stu-id="e2161-131">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="e2161-132">-確認</span><span class="sxs-lookup"><span data-stu-id="e2161-132">-Confirm</span></span>
<span data-ttu-id="e2161-133">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="e2161-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2161-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2161-134">-WhatIf</span></span>
<span data-ttu-id="e2161-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e2161-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e2161-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e2161-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2161-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2161-137">CommonParameters</span></span>
<span data-ttu-id="e2161-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e2161-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2161-139">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e2161-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2161-140">輸入</span><span class="sxs-lookup"><span data-stu-id="e2161-140">INPUTS</span></span>

### <span data-ttu-id="e2161-141">Microsoft.Azure.Commands.Compute.Automation.models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="e2161-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="e2161-142">System.String</span><span class="sxs-lookup"><span data-stu-id="e2161-142">System.String</span></span>

### <span data-ttu-id="e2161-143">System.Nullable'1[[System.Boolean， System.Private.CoreLib， Version=4.0.0.0， Culture=neutral， PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="e2161-143">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="e2161-144">Microsoft.Azure.management.Compute.models.VirtualMachineScaleSetIPConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="e2161-144">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIPConfiguration[]</span></span>

### <span data-ttu-id="e2161-145">System.String[]</span><span class="sxs-lookup"><span data-stu-id="e2161-145">System.String[]</span></span>

## <span data-ttu-id="e2161-146">輸出</span><span class="sxs-lookup"><span data-stu-id="e2161-146">OUTPUTS</span></span>

### <span data-ttu-id="e2161-147">Microsoft.Azure.Commands.Compute.Automation.models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="e2161-147">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="e2161-148">筆記</span><span class="sxs-lookup"><span data-stu-id="e2161-148">NOTES</span></span>

## <span data-ttu-id="e2161-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="e2161-149">RELATED LINKS</span></span>

[<span data-ttu-id="e2161-150">New-AzEvssConfig</span><span class="sxs-lookup"><span data-stu-id="e2161-150">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)
