---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: BF80D456-DAB1-4B51-B50F-A75C2C66A472
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVMNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVMNetworkInterface.md
ms.openlocfilehash: 11d2f8226e2cabba5fb431054a0e6c822e33af6e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448766"
---
# <span data-ttu-id="fbde0-101">Add-AzureRmVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="fbde0-101">Add-AzureRmVMNetworkInterface</span></span>

## <span data-ttu-id="fbde0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fbde0-102">SYNOPSIS</span></span>
<span data-ttu-id="fbde0-103">新增網路介面至虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="fbde0-103">Adds a network interface to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fbde0-104">句法</span><span class="sxs-lookup"><span data-stu-id="fbde0-104">SYNTAX</span></span>

### <span data-ttu-id="fbde0-105">GetNicFromNicId (預設) </span><span class="sxs-lookup"><span data-stu-id="fbde0-105">GetNicFromNicId (Default)</span></span>
```
Add-AzureRmVMNetworkInterface [-VM] <PSVirtualMachine> [-Id] <String> [-Primary] [<CommonParameters>]
```

### <span data-ttu-id="fbde0-106">GetNicFromNicObject</span><span class="sxs-lookup"><span data-stu-id="fbde0-106">GetNicFromNicObject</span></span>
```
Add-AzureRmVMNetworkInterface [-VM] <PSVirtualMachine>
 [-NetworkInterface] <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkInterface]>
 [<CommonParameters>]
```

## <span data-ttu-id="fbde0-107">說明</span><span class="sxs-lookup"><span data-stu-id="fbde0-107">DESCRIPTION</span></span>
<span data-ttu-id="fbde0-108">**載入 AzureRmVMNetworkInterface** Cmdlet 會將網路介面新增至虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="fbde0-108">The **Add-AzureRmVMNetworkInterface** cmdlet adds a network interface to a virtual machine.</span></span>
<span data-ttu-id="fbde0-109">您可以在建立虛擬機器或將它新增到現有的虛擬機器中時，新增介面。</span><span class="sxs-lookup"><span data-stu-id="fbde0-109">You can add an interface when you create a virtual machine or add one to an existing virtual machine.</span></span>

## <span data-ttu-id="fbde0-110">示例</span><span class="sxs-lookup"><span data-stu-id="fbde0-110">EXAMPLES</span></span>

### <span data-ttu-id="fbde0-111">範例1：將網路介面新增至新的虛擬機器</span><span class="sxs-lookup"><span data-stu-id="fbde0-111">Example 1: Add a network interface to a new virtual machine</span></span>
```
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" 
PS C:\> Add-AzureRmVMNetworkInterface -VM $VirtualMachine -Id "/subscriptions/46fc8ea4-2de6-4179-8ab1-365da4121af4/resourceGroups/contoso/providers/Microsoft.Network/networkInterfaces/sshNIC"
```

<span data-ttu-id="fbde0-112">第一個命令會建立一個虛擬電腦物件，然後將它儲存在 $VirtualMachine 變數中。</span><span class="sxs-lookup"><span data-stu-id="fbde0-112">The first command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="fbde0-113">該命令會將名稱和大小指派給虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="fbde0-113">The command assigns a name and size to the virtual machine.</span></span>

<span data-ttu-id="fbde0-114">第二個命令會將網路介面新增至儲存在 $VirtualMachine 的虛擬機器中。</span><span class="sxs-lookup"><span data-stu-id="fbde0-114">The second command adds a network interface to the virtual machine stored in $VirtualMachine.</span></span>

### <span data-ttu-id="fbde0-115">範例2：新增網路介面至現有的虛擬機器</span><span class="sxs-lookup"><span data-stu-id="fbde0-115">Example 2: Add a network interface to an existing virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> Add-AzureRmVMNetworkInterface -VM $VirtualMachine -Id "/subscriptions/46fc8ea4-2de6-4179-8ab1-365da4121af4/resourceGroups/contoso/providers/Microsoft.Network/networkInterfaces/sshNIC"
PS C:\> Update-AzureRmVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="fbde0-116">第一個命令會使用 **AzureRmVM** Cmdlet 取得名為 VirtualMachine07 的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="fbde0-116">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzureRmVM** cmdlet.</span></span>
<span data-ttu-id="fbde0-117">該命令會將虛擬機器儲存在 $VirtualMachine 變數中。</span><span class="sxs-lookup"><span data-stu-id="fbde0-117">The command stores the virtual machine in the $VirtualMachine variable.</span></span>

<span data-ttu-id="fbde0-118">第二個命令會將網路介面新增至儲存在 $VirtualMachine 的虛擬機器中。</span><span class="sxs-lookup"><span data-stu-id="fbde0-118">The second command adds a network interface to the virtual machine stored in $VirtualMachine.</span></span>

<span data-ttu-id="fbde0-119">Final 命令會更新儲存在 ResourceGroup11 中 $VirtualMachine 的虛擬機器狀態。</span><span class="sxs-lookup"><span data-stu-id="fbde0-119">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

## <span data-ttu-id="fbde0-120">參數</span><span class="sxs-lookup"><span data-stu-id="fbde0-120">PARAMETERS</span></span>

### <span data-ttu-id="fbde0-121">-識別碼</span><span class="sxs-lookup"><span data-stu-id="fbde0-121">-Id</span></span>
<span data-ttu-id="fbde0-122">指定要新增至虛擬機器的網路介面識別碼。</span><span class="sxs-lookup"><span data-stu-id="fbde0-122">Specifies the ID of a network interface to add to a virtual machine.</span></span>
<span data-ttu-id="fbde0-123">您可以使用 [AzureRmNetworkInterface](/powershell/module/azurerm.network/get-azurermnetworkinterface) Cmdlet 來取得網路介面。</span><span class="sxs-lookup"><span data-stu-id="fbde0-123">You can use the [Get-AzureRmNetworkInterface](/powershell/module/azurerm.network/get-azurermnetworkinterface) cmdlet to obtain a network interface.</span></span>

```yaml
Type: String
Parameter Sets: GetNicFromNicId
Aliases: NicId, NetworkInterfaceId

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbde0-124">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="fbde0-124">-NetworkInterface</span></span>
<span data-ttu-id="fbde0-125">指定網路介面。</span><span class="sxs-lookup"><span data-stu-id="fbde0-125">Specifies the network interface.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkInterface]
Parameter Sets: GetNicFromNicObject
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fbde0-126">-主要</span><span class="sxs-lookup"><span data-stu-id="fbde0-126">-Primary</span></span>
<span data-ttu-id="fbde0-127">表示此 Cmdlet 會將網路介面新增為主要介面。</span><span class="sxs-lookup"><span data-stu-id="fbde0-127">Indicates that this cmdlet adds the network interface as the primary interface.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: GetNicFromNicId
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbde0-128">-VM</span><span class="sxs-lookup"><span data-stu-id="fbde0-128">-VM</span></span>
<span data-ttu-id="fbde0-129">指定要新增網路介面的本機虛擬機器物件。</span><span class="sxs-lookup"><span data-stu-id="fbde0-129">Specifies a local virtual machine object to which to add a network interface.</span></span>
<span data-ttu-id="fbde0-130">若要建立虛擬機器，請使用 **AzureRmVMConfig** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fbde0-130">To create a virtual machine, use the **New-AzureRmVMConfig** cmdlet.</span></span>
<span data-ttu-id="fbde0-131">若要取得現有的虛擬機器，請使用 **AzureRmVM** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fbde0-131">To obtain an existing virtual machine, use the **Get-AzureRmVM** cmdlet.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fbde0-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbde0-132">CommonParameters</span></span>
<span data-ttu-id="fbde0-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fbde0-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbde0-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="fbde0-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbde0-135">輸入</span><span class="sxs-lookup"><span data-stu-id="fbde0-135">INPUTS</span></span>

### <span data-ttu-id="fbde0-136">所有</span><span class="sxs-lookup"><span data-stu-id="fbde0-136">None</span></span>
<span data-ttu-id="fbde0-137">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="fbde0-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fbde0-138">輸出</span><span class="sxs-lookup"><span data-stu-id="fbde0-138">OUTPUTS</span></span>

## <span data-ttu-id="fbde0-139">筆記</span><span class="sxs-lookup"><span data-stu-id="fbde0-139">NOTES</span></span>

## <span data-ttu-id="fbde0-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="fbde0-140">RELATED LINKS</span></span>

[<span data-ttu-id="fbde0-141">新-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="fbde0-141">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)

[<span data-ttu-id="fbde0-142">AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="fbde0-142">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="fbde0-143">AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="fbde0-143">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)