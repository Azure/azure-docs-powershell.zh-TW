---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: BAC2FA68-1D82-411D-A853-FD4EE525B533
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssNetworkInterfaceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssNetworkInterfaceConfiguration.md
ms.openlocfilehash: 651e339de5782d288350535ba1b0527d7a3eb0de
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450848"
---
# <span data-ttu-id="79f04-101">Add-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="79f04-101">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="79f04-102">摘要</span><span class="sxs-lookup"><span data-stu-id="79f04-102">SYNOPSIS</span></span>
<span data-ttu-id="79f04-103">將網路介面設定新增至 VMSS。</span><span class="sxs-lookup"><span data-stu-id="79f04-103">Adds a network interface configuration to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="79f04-104">句法</span><span class="sxs-lookup"><span data-stu-id="79f04-104">SYNTAX</span></span>

```
Add-AzureRmVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-Name] <String>] [[-Primary] <Boolean>] [[-Id] <String>]
 [[-IpConfiguration] <VirtualMachineScaleSetIPConfiguration[]>] [-EnableAcceleratedNetworking]
 [-NetworkSecurityGroupId <String>] [-DnsSettingsDnsServer <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79f04-105">說明</span><span class="sxs-lookup"><span data-stu-id="79f04-105">DESCRIPTION</span></span>
<span data-ttu-id="79f04-106">**AzureRmVmssNetworkInterfaceConfiguration** Cmdlet 會將網路介面設定新增到虛擬電腦規模集， (VMSS) 。</span><span class="sxs-lookup"><span data-stu-id="79f04-106">The **Add-AzureRmVmssNetworkInterfaceConfiguration** cmdlet adds a network interface configuration to the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="79f04-107">示例</span><span class="sxs-lookup"><span data-stu-id="79f04-107">EXAMPLES</span></span>

### <span data-ttu-id="79f04-108">範例1：將網路介面設定新增至 VMSS</span><span class="sxs-lookup"><span data-stu-id="79f04-108">Example 1: Add a network interface configuration to the VMSS</span></span>
```
PS C:\> Add-AzureRmVmssNetworkInterfaceConfiguration -VirtualMachineScaleSet $VMSS -Name "Test" -Primary $True -IPConfiguration $IPCfg
```

<span data-ttu-id="79f04-109">這個命令會將網路介面設定新增至 VMSS。</span><span class="sxs-lookup"><span data-stu-id="79f04-109">This command adds a network interface configuration to the VMSS.</span></span>

## <span data-ttu-id="79f04-110">參數</span><span class="sxs-lookup"><span data-stu-id="79f04-110">PARAMETERS</span></span>

### <span data-ttu-id="79f04-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79f04-111">-DefaultProfile</span></span>
<span data-ttu-id="79f04-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="79f04-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="79f04-113">-DnsSettingsDnsServer</span><span class="sxs-lookup"><span data-stu-id="79f04-113">-DnsSettingsDnsServer</span></span>
<span data-ttu-id="79f04-114">Dns 設定的 dns 伺服器 IP 位址清單。</span><span class="sxs-lookup"><span data-stu-id="79f04-114">List of dns server IP addresses for dns settings.</span></span>

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

### <span data-ttu-id="79f04-115">-EnableAcceleratedNetworking</span><span class="sxs-lookup"><span data-stu-id="79f04-115">-EnableAcceleratedNetworking</span></span>
<span data-ttu-id="79f04-116">指定網路介面是否為已加速網路的功能。</span><span class="sxs-lookup"><span data-stu-id="79f04-116">Specifies whether the network interface is accelerated networking-enabled.</span></span>

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

### <span data-ttu-id="79f04-117">-識別碼</span><span class="sxs-lookup"><span data-stu-id="79f04-117">-Id</span></span>
<span data-ttu-id="79f04-118">指定虛擬機器的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="79f04-118">Specifies the Resource ID of the virtual machine.</span></span>

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

### <span data-ttu-id="79f04-119">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="79f04-119">-IpConfiguration</span></span>
<span data-ttu-id="79f04-120">指定網路介面的 IP 配置。</span><span class="sxs-lookup"><span data-stu-id="79f04-120">Specifies the IP configurations of the network interface.</span></span>

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

### <span data-ttu-id="79f04-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="79f04-121">-Name</span></span>
<span data-ttu-id="79f04-122">指定網路介面配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="79f04-122">Specifies the name of the network interface configuration.</span></span>

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

### <span data-ttu-id="79f04-123">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="79f04-123">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="79f04-124">網路安全性群組的 Id。</span><span class="sxs-lookup"><span data-stu-id="79f04-124">Id of the network security group.</span></span>

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

### <span data-ttu-id="79f04-125">-主要</span><span class="sxs-lookup"><span data-stu-id="79f04-125">-Primary</span></span>
<span data-ttu-id="79f04-126">指出從網路介面設定建立的網路介面是否將是虛擬機器的主要網路資訊中心 (NIC) 。</span><span class="sxs-lookup"><span data-stu-id="79f04-126">Indicates whether network interfaces created from the network interface configuration will be the primary network information center (NIC) of the virtual machine.</span></span>

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

### <span data-ttu-id="79f04-127">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="79f04-127">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="79f04-128">指定 VMSS 物件。</span><span class="sxs-lookup"><span data-stu-id="79f04-128">Specifies the VMSS object.</span></span>
<span data-ttu-id="79f04-129">您可以使用 [新的-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) Cmdlet 來建立物件。</span><span class="sxs-lookup"><span data-stu-id="79f04-129">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="79f04-130">-確認</span><span class="sxs-lookup"><span data-stu-id="79f04-130">-Confirm</span></span>
<span data-ttu-id="79f04-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="79f04-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79f04-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79f04-132">-WhatIf</span></span>
<span data-ttu-id="79f04-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="79f04-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="79f04-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="79f04-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79f04-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79f04-135">CommonParameters</span></span>
<span data-ttu-id="79f04-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="79f04-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79f04-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="79f04-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79f04-138">輸入</span><span class="sxs-lookup"><span data-stu-id="79f04-138">INPUTS</span></span>

## <span data-ttu-id="79f04-139">輸出</span><span class="sxs-lookup"><span data-stu-id="79f04-139">OUTPUTS</span></span>

###  
<span data-ttu-id="79f04-140">這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="79f04-140">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="79f04-141">筆記</span><span class="sxs-lookup"><span data-stu-id="79f04-141">NOTES</span></span>

## <span data-ttu-id="79f04-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="79f04-142">RELATED LINKS</span></span>

[<span data-ttu-id="79f04-143">新-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="79f04-143">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)
