---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: BF80D456-DAB1-4B51-B50F-A75C2C66A472
online version: https://docs.microsoft.com/powershell/module/az.compute/add-azvmnetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMNetworkInterface.md
ms.openlocfilehash: efe587cf01fa2adf16e4b6beaaa319312f3c9fa5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906314"
---
# <span data-ttu-id="08866-101">Add-AzVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="08866-101">Add-AzVMNetworkInterface</span></span>

## <span data-ttu-id="08866-102">簡介</span><span class="sxs-lookup"><span data-stu-id="08866-102">SYNOPSIS</span></span>
<span data-ttu-id="08866-103">新增網路介面至虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="08866-103">Adds a network interface to a virtual machine.</span></span>

## <span data-ttu-id="08866-104">語法</span><span class="sxs-lookup"><span data-stu-id="08866-104">SYNTAX</span></span>

### <span data-ttu-id="08866-105">GetNicFromNicId (預設) </span><span class="sxs-lookup"><span data-stu-id="08866-105">GetNicFromNicId (Default)</span></span>
```
Add-AzVMNetworkInterface [-VM] <PSVirtualMachine> [-Id] <String> [-Primary]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="08866-106">GetNicFromNicObject</span><span class="sxs-lookup"><span data-stu-id="08866-106">GetNicFromNicObject</span></span>
```
Add-AzVMNetworkInterface [-VM] <PSVirtualMachine>
 [-NetworkInterface] <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.INetworkInterfaceReference]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="08866-107">描述</span><span class="sxs-lookup"><span data-stu-id="08866-107">DESCRIPTION</span></span>
<span data-ttu-id="08866-108">**Add-Az VIRTUALNetworkInterface** Cmdlet 會新增網路介面至虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="08866-108">The **Add-AzVMNetworkInterface** cmdlet adds a network interface to a virtual machine.</span></span>
<span data-ttu-id="08866-109">您可以在建立虛擬機器時新增介面，或新增一個至現有的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="08866-109">You can add an interface when you create a virtual machine or add one to an existing virtual machine.</span></span>

## <span data-ttu-id="08866-110">例子</span><span class="sxs-lookup"><span data-stu-id="08866-110">EXAMPLES</span></span>

### <span data-ttu-id="08866-111">範例 1：新增網路介面至新的虛擬機器</span><span class="sxs-lookup"><span data-stu-id="08866-111">Example 1: Add a network interface to a new virtual machine</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> Add-AzVMNetworkInterface -VM $VirtualMachine -Id "/subscriptions/46fc8ea4-2de6-4179-8ab1-365da4121af4/resourceGroups/contoso/providers/Microsoft.Network/networkInterfaces/sshNIC"
```

<span data-ttu-id="08866-112">第一個命令會建立虛擬機器物件，然後將它儲存在$VirtualMachine變數中。</span><span class="sxs-lookup"><span data-stu-id="08866-112">The first command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="08866-113">該命令會為虛擬機器指定名稱和大小。</span><span class="sxs-lookup"><span data-stu-id="08866-113">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="08866-114">第二個命令會將網路介面新增到儲存在 $VirtualMachine 中的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="08866-114">The second command adds a network interface to the virtual machine stored in $VirtualMachine.</span></span>

### <span data-ttu-id="08866-115">範例 2：新增網路介面至現有的虛擬機器</span><span class="sxs-lookup"><span data-stu-id="08866-115">Example 2: Add a network interface to an existing virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> Add-AzVMNetworkInterface -VM $VirtualMachine -Id "/subscriptions/46fc8ea4-2de6-4179-8ab1-365da4121af4/resourceGroups/contoso/providers/Microsoft.Network/networkInterfaces/sshNIC"
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="08866-116">第一個命令會使用 **Get-Az VIRTUAL** Cmdlet 取得名為 VirtualMachine07 的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="08866-116">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzVM** cmdlet.</span></span>
<span data-ttu-id="08866-117">該命令將虛擬機器儲存在 $VirtualMachine 變數中。</span><span class="sxs-lookup"><span data-stu-id="08866-117">The command stores the virtual machine in the $VirtualMachine variable.</span></span>
<span data-ttu-id="08866-118">第二個命令會將網路介面新增到儲存在 $VirtualMachine 中的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="08866-118">The second command adds a network interface to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="08866-119">最後一個命令會更新儲存在 ResourceGroup11 $VirtualMachine的狀態。</span><span class="sxs-lookup"><span data-stu-id="08866-119">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

## <span data-ttu-id="08866-120">參數</span><span class="sxs-lookup"><span data-stu-id="08866-120">PARAMETERS</span></span>

### <span data-ttu-id="08866-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08866-121">-DefaultProfile</span></span>
<span data-ttu-id="08866-122">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="08866-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="08866-123">-Id</span><span class="sxs-lookup"><span data-stu-id="08866-123">-Id</span></span>
<span data-ttu-id="08866-124">指定要新加入虛擬機器的網路介面識別碼。</span><span class="sxs-lookup"><span data-stu-id="08866-124">Specifies the ID of a network interface to add to a virtual machine.</span></span>
<span data-ttu-id="08866-125">您可以使用 [Get-AzNetworkInterface](/powershell/module/az.network/get-aznetworkinterface) Cmdlet 取得網路介面。</span><span class="sxs-lookup"><span data-stu-id="08866-125">You can use the [Get-AzNetworkInterface](/powershell/module/az.network/get-aznetworkinterface) cmdlet to obtain a network interface.</span></span>

```yaml
Type: System.String
Parameter Sets: GetNicFromNicId
Aliases: NicId, NetworkInterfaceId

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08866-126">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="08866-126">-NetworkInterface</span></span>
<span data-ttu-id="08866-127">指定網路介面。</span><span class="sxs-lookup"><span data-stu-id="08866-127">Specifies the network interface.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.INetworkInterfaceReference]
Parameter Sets: GetNicFromNicObject
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="08866-128">-主要</span><span class="sxs-lookup"><span data-stu-id="08866-128">-Primary</span></span>
<span data-ttu-id="08866-129">表示此 Cmdlet 將網路介面新增為主要介面。</span><span class="sxs-lookup"><span data-stu-id="08866-129">Indicates that this cmdlet adds the network interface as the primary interface.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetNicFromNicId
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08866-130">-VM</span><span class="sxs-lookup"><span data-stu-id="08866-130">-VM</span></span>
<span data-ttu-id="08866-131">指定要新增網路介面的本機虛擬機器物件。</span><span class="sxs-lookup"><span data-stu-id="08866-131">Specifies a local virtual machine object to which to add a network interface.</span></span>
<span data-ttu-id="08866-132">若要建立虛擬機器，請使用 **New-AzMSConfig** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="08866-132">To create a virtual machine, use the **New-AzVMConfig** cmdlet.</span></span>
<span data-ttu-id="08866-133">若要取得現有的虛擬機器，請使用 **Get-Az%。CMdlet。**</span><span class="sxs-lookup"><span data-stu-id="08866-133">To obtain an existing virtual machine, use the **Get-AzVM** cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="08866-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08866-134">CommonParameters</span></span>
<span data-ttu-id="08866-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="08866-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08866-136">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="08866-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08866-137">輸入</span><span class="sxs-lookup"><span data-stu-id="08866-137">INPUTS</span></span>

### <span data-ttu-id="08866-138">Microsoft.Azure.Commands.Compute.models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="08866-138">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="08866-139">System.String</span><span class="sxs-lookup"><span data-stu-id="08866-139">System.String</span></span>

### <span data-ttu-id="08866-140">System.Collections.generic.List'1[[Microsoft.Azure.management.Internal.Network.Common.INetworkInterfaceReference，Microsoft.Azure.PowerShell.Clients.Network，Version=1.0.0.0，Culture=neutral，PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="08866-140">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Internal.Network.Common.INetworkInterfaceReference, Microsoft.Azure.PowerShell.Clients.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="08866-141">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="08866-141">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="08866-142">輸出</span><span class="sxs-lookup"><span data-stu-id="08866-142">OUTPUTS</span></span>

### <span data-ttu-id="08866-143">Microsoft.Azure.Commands.Compute.models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="08866-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="08866-144">筆記</span><span class="sxs-lookup"><span data-stu-id="08866-144">NOTES</span></span>

## <span data-ttu-id="08866-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="08866-145">RELATED LINKS</span></span>

[<span data-ttu-id="08866-146">New-AzMSCONFIG</span><span class="sxs-lookup"><span data-stu-id="08866-146">New-AzVMConfig</span></span>](./New-AzVMConfig.md)

[<span data-ttu-id="08866-147">Get-AzMS</span><span class="sxs-lookup"><span data-stu-id="08866-147">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="08866-148">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="08866-148">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)
