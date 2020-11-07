---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: BAC2FA68-1D82-411D-A853-FD4EE525B533
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssNetworkInterfaceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssNetworkInterfaceConfiguration.md
ms.openlocfilehash: 0b21b5fa3b5b605ee3092a61eaf67a2c63c4346b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623483"
---
# <span data-ttu-id="5ce8d-101">Add-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="5ce8d-101">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="5ce8d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5ce8d-102">SYNOPSIS</span></span>
<span data-ttu-id="5ce8d-103">將網路介面設定新增至 VMSS。</span><span class="sxs-lookup"><span data-stu-id="5ce8d-103">Adds a network interface configuration to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5ce8d-104">句法</span><span class="sxs-lookup"><span data-stu-id="5ce8d-104">SYNTAX</span></span>

```
Add-AzureRmVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <VirtualMachineScaleSet>
 [[-Name] <String>] [[-Primary] <Boolean>] [[-Id] <String>]
 [[-IpConfiguration] <VirtualMachineScaleSetIPConfiguration[]>] [-NetworkSecurityGroupId <String>]
 [-DnsSettingsDnsServer <String[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ce8d-105">說明</span><span class="sxs-lookup"><span data-stu-id="5ce8d-105">DESCRIPTION</span></span>
<span data-ttu-id="5ce8d-106">**AzureRmVmssNetworkInterfaceConfiguration** Cmdlet 會將網路介面設定新增到虛擬電腦規模集， (VMSS) 。</span><span class="sxs-lookup"><span data-stu-id="5ce8d-106">The **Add-AzureRmVmssNetworkInterfaceConfiguration** cmdlet adds a network interface configuration to the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="5ce8d-107">示例</span><span class="sxs-lookup"><span data-stu-id="5ce8d-107">EXAMPLES</span></span>

### <span data-ttu-id="5ce8d-108">範例1：將網路介面設定新增至 VMSS</span><span class="sxs-lookup"><span data-stu-id="5ce8d-108">Example 1: Add a network interface configuration to the VMSS</span></span>
```
PS C:\> Add-AzureRmVmssNetworkInterfaceConfiguration -VirtualMachineScaleSet $VMSS -Name "Test" -Primary $True -IPConfiguration $IPCfg
```

<span data-ttu-id="5ce8d-109">這個命令會將網路介面設定新增至 VMSS。</span><span class="sxs-lookup"><span data-stu-id="5ce8d-109">This command adds a network interface configuration to the VMSS.</span></span>

## <span data-ttu-id="5ce8d-110">參數</span><span class="sxs-lookup"><span data-stu-id="5ce8d-110">PARAMETERS</span></span>

### <span data-ttu-id="5ce8d-111">-DnsSettingsDnsServer</span><span class="sxs-lookup"><span data-stu-id="5ce8d-111">-DnsSettingsDnsServer</span></span>
<span data-ttu-id="5ce8d-112">Dns 設定的 dns 伺服器 IP 位址清單。</span><span class="sxs-lookup"><span data-stu-id="5ce8d-112">List of dns server IP addresses for dns settings.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ce8d-113">-識別碼</span><span class="sxs-lookup"><span data-stu-id="5ce8d-113">-Id</span></span>
<span data-ttu-id="5ce8d-114">指定虛擬機器的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="5ce8d-114">Specifies the Resource ID of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ce8d-115">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="5ce8d-115">-IpConfiguration</span></span>
<span data-ttu-id="5ce8d-116">指定網路介面的 IP 配置。</span><span class="sxs-lookup"><span data-stu-id="5ce8d-116">Specifies the IP configurations of the network interface.</span></span>

```yaml
Type: VirtualMachineScaleSetIPConfiguration[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ce8d-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="5ce8d-117">-Name</span></span>
<span data-ttu-id="5ce8d-118">指定網路介面配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="5ce8d-118">Specifies the name of the network interface configuration.</span></span>

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

### <span data-ttu-id="5ce8d-119">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="5ce8d-119">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="5ce8d-120">網路安全性群組的 Id。</span><span class="sxs-lookup"><span data-stu-id="5ce8d-120">Id of the network security group.</span></span>

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

### <span data-ttu-id="5ce8d-121">-主要</span><span class="sxs-lookup"><span data-stu-id="5ce8d-121">-Primary</span></span>
<span data-ttu-id="5ce8d-122">指出從網路介面設定建立的網路介面是否將是虛擬機器的主要網路資訊中心 (NIC) 。</span><span class="sxs-lookup"><span data-stu-id="5ce8d-122">Indicates whether network interfaces created from the network interface configuration will be the primary network information center (NIC) of the virtual machine.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ce8d-123">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="5ce8d-123">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="5ce8d-124">指定 VMSS 物件。</span><span class="sxs-lookup"><span data-stu-id="5ce8d-124">Specifies the VMSS object.</span></span>
<span data-ttu-id="5ce8d-125">您可以使用 [新的-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) Cmdlet 來建立物件。</span><span class="sxs-lookup"><span data-stu-id="5ce8d-125">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create the object.</span></span>

```yaml
Type: VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5ce8d-126">-確認</span><span class="sxs-lookup"><span data-stu-id="5ce8d-126">-Confirm</span></span>
<span data-ttu-id="5ce8d-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5ce8d-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ce8d-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ce8d-128">-WhatIf</span></span>
<span data-ttu-id="5ce8d-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5ce8d-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5ce8d-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5ce8d-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ce8d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ce8d-131">CommonParameters</span></span>
<span data-ttu-id="5ce8d-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5ce8d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ce8d-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5ce8d-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ce8d-134">輸入</span><span class="sxs-lookup"><span data-stu-id="5ce8d-134">INPUTS</span></span>

### <span data-ttu-id="5ce8d-135">所有</span><span class="sxs-lookup"><span data-stu-id="5ce8d-135">None</span></span>
<span data-ttu-id="5ce8d-136">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="5ce8d-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5ce8d-137">輸出</span><span class="sxs-lookup"><span data-stu-id="5ce8d-137">OUTPUTS</span></span>

###  
<span data-ttu-id="5ce8d-138">這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="5ce8d-138">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="5ce8d-139">筆記</span><span class="sxs-lookup"><span data-stu-id="5ce8d-139">NOTES</span></span>

## <span data-ttu-id="5ce8d-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="5ce8d-140">RELATED LINKS</span></span>

[<span data-ttu-id="5ce8d-141">新-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="5ce8d-141">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)
