---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: BAC2FA68-1D82-411D-A853-FD4EE525B533
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmssnetworkinterfaceconfiguration
schema: 2.0.0
ms.openlocfilehash: cda87de466ba3cf3c2a1f73798a2bed21f48206e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93801058"
---
# <span data-ttu-id="1182b-101">Add-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="1182b-101">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="1182b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1182b-102">SYNOPSIS</span></span>
<span data-ttu-id="1182b-103">將網路介面設定新增至 VMSS。</span><span class="sxs-lookup"><span data-stu-id="1182b-103">Adds a network interface configuration to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1182b-104">句法</span><span class="sxs-lookup"><span data-stu-id="1182b-104">SYNTAX</span></span>

```
Add-AzureRmVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-Name] <String>] [[-Primary] <Boolean>] [[-Id] <String>]
 [[-IpConfiguration] <VirtualMachineScaleSetIPConfiguration[]>] [-EnableAcceleratedNetworking]
 [-EnableIPForwarding] [-NetworkSecurityGroupId <String>] [-DnsSettingsDnsServer <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1182b-105">說明</span><span class="sxs-lookup"><span data-stu-id="1182b-105">DESCRIPTION</span></span>
<span data-ttu-id="1182b-106">**AzureRmVmssNetworkInterfaceConfiguration** Cmdlet 會將網路介面設定新增到虛擬電腦規模集， (VMSS) 。</span><span class="sxs-lookup"><span data-stu-id="1182b-106">The **Add-AzureRmVmssNetworkInterfaceConfiguration** cmdlet adds a network interface configuration to the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="1182b-107">示例</span><span class="sxs-lookup"><span data-stu-id="1182b-107">EXAMPLES</span></span>

### <span data-ttu-id="1182b-108">範例1：將網路介面設定新增至 VMSS</span><span class="sxs-lookup"><span data-stu-id="1182b-108">Example 1: Add a network interface configuration to the VMSS</span></span>
```
PS C:\> Add-AzureRmVmssNetworkInterfaceConfiguration -VirtualMachineScaleSet $VMSS -Name "Test" -Primary $True -IPConfiguration $IPCfg
```

<span data-ttu-id="1182b-109">這個命令會將網路介面設定新增至 VMSS。</span><span class="sxs-lookup"><span data-stu-id="1182b-109">This command adds a network interface configuration to the VMSS.</span></span>

## <span data-ttu-id="1182b-110">參數</span><span class="sxs-lookup"><span data-stu-id="1182b-110">PARAMETERS</span></span>

### <span data-ttu-id="1182b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1182b-111">-DefaultProfile</span></span>
<span data-ttu-id="1182b-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1182b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1182b-113">-DnsSettingsDnsServer</span><span class="sxs-lookup"><span data-stu-id="1182b-113">-DnsSettingsDnsServer</span></span>
<span data-ttu-id="1182b-114">Dns 設定的 dns 伺服器 IP 位址清單。</span><span class="sxs-lookup"><span data-stu-id="1182b-114">List of dns server IP addresses for dns settings.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: DnsServer

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1182b-115">-EnableAcceleratedNetworking</span><span class="sxs-lookup"><span data-stu-id="1182b-115">-EnableAcceleratedNetworking</span></span>
<span data-ttu-id="1182b-116">指定網路介面是否為已加速網路的功能。</span><span class="sxs-lookup"><span data-stu-id="1182b-116">Specifies whether the network interface is accelerated networking-enabled.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1182b-117">-EnableIPForwarding</span><span class="sxs-lookup"><span data-stu-id="1182b-117">-EnableIPForwarding</span></span>
<span data-ttu-id="1182b-118">指定是否在這個 NIC 上啟用 IP 轉寄。</span><span class="sxs-lookup"><span data-stu-id="1182b-118">Specifies whether IP forwarding enabled on this NIC.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1182b-119">-識別碼</span><span class="sxs-lookup"><span data-stu-id="1182b-119">-Id</span></span>
<span data-ttu-id="1182b-120">指定虛擬機器的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="1182b-120">Specifies the Resource ID of the virtual machine.</span></span>

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

### <span data-ttu-id="1182b-121">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="1182b-121">-IpConfiguration</span></span>
<span data-ttu-id="1182b-122">指定網路介面的 IP 配置。</span><span class="sxs-lookup"><span data-stu-id="1182b-122">Specifies the IP configurations of the network interface.</span></span>

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

### <span data-ttu-id="1182b-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="1182b-123">-Name</span></span>
<span data-ttu-id="1182b-124">指定網路介面配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="1182b-124">Specifies the name of the network interface configuration.</span></span>

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

### <span data-ttu-id="1182b-125">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="1182b-125">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="1182b-126">網路安全性群組的 Id。</span><span class="sxs-lookup"><span data-stu-id="1182b-126">Id of the network security group.</span></span>

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

### <span data-ttu-id="1182b-127">-主要</span><span class="sxs-lookup"><span data-stu-id="1182b-127">-Primary</span></span>
<span data-ttu-id="1182b-128">指出從網路介面設定建立的網路介面是否將是虛擬機器的主要網路資訊中心 (NIC) 。</span><span class="sxs-lookup"><span data-stu-id="1182b-128">Indicates whether network interfaces created from the network interface configuration will be the primary network information center (NIC) of the virtual machine.</span></span>

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

### <span data-ttu-id="1182b-129">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="1182b-129">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="1182b-130">指定 VMSS 物件。</span><span class="sxs-lookup"><span data-stu-id="1182b-130">Specifies the VMSS object.</span></span>
<span data-ttu-id="1182b-131">您可以使用 [新的-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) Cmdlet 來建立物件。</span><span class="sxs-lookup"><span data-stu-id="1182b-131">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create the object.</span></span>

```yaml
Type: PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1182b-132">-確認</span><span class="sxs-lookup"><span data-stu-id="1182b-132">-Confirm</span></span>
<span data-ttu-id="1182b-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1182b-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1182b-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1182b-134">-WhatIf</span></span>
<span data-ttu-id="1182b-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1182b-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1182b-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1182b-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1182b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1182b-137">CommonParameters</span></span>
<span data-ttu-id="1182b-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1182b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1182b-139">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1182b-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1182b-140">輸入</span><span class="sxs-lookup"><span data-stu-id="1182b-140">INPUTS</span></span>

### <span data-ttu-id="1182b-141">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="1182b-141">VirtualMachineScaleSet</span></span>
<span data-ttu-id="1182b-142">形參 "VirtualMachineScaleSet" 接受管線中 "VirtualMachineScaleSet" 類型的值</span><span class="sxs-lookup"><span data-stu-id="1182b-142">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="1182b-143">輸出</span><span class="sxs-lookup"><span data-stu-id="1182b-143">OUTPUTS</span></span>

###  
<span data-ttu-id="1182b-144">這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="1182b-144">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="1182b-145">筆記</span><span class="sxs-lookup"><span data-stu-id="1182b-145">NOTES</span></span>

## <span data-ttu-id="1182b-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="1182b-146">RELATED LINKS</span></span>

[<span data-ttu-id="1182b-147">新-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="1182b-147">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)
