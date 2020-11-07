---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: BF80D456-DAB1-4B51-B50F-A75C2C66A472
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmnetworkinterface
schema: 2.0.0
ms.openlocfilehash: 112403f4cb742c5df39538eb2d8d8fac629d3379
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93801826"
---
# <span data-ttu-id="45806-101">Add-AzureRmVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="45806-101">Add-AzureRmVMNetworkInterface</span></span>

## <span data-ttu-id="45806-102">摘要</span><span class="sxs-lookup"><span data-stu-id="45806-102">SYNOPSIS</span></span>
<span data-ttu-id="45806-103">新增網路介面至虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="45806-103">Adds a network interface to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="45806-104">句法</span><span class="sxs-lookup"><span data-stu-id="45806-104">SYNTAX</span></span>

### <span data-ttu-id="45806-105">GetNicFromNicId (預設) </span><span class="sxs-lookup"><span data-stu-id="45806-105">GetNicFromNicId (Default)</span></span>
```
Add-AzureRmVMNetworkInterface [-VM] <PSVirtualMachine> [-Id] <String> [-Primary]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="45806-106">GetNicFromNicObject</span><span class="sxs-lookup"><span data-stu-id="45806-106">GetNicFromNicObject</span></span>
```
Add-AzureRmVMNetworkInterface [-VM] <PSVirtualMachine>
 [-NetworkInterface] <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.INetworkInterfaceReference]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="45806-107">說明</span><span class="sxs-lookup"><span data-stu-id="45806-107">DESCRIPTION</span></span>
<span data-ttu-id="45806-108">**載入 AzureRmVMNetworkInterface** Cmdlet 會將網路介面新增至虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="45806-108">The **Add-AzureRmVMNetworkInterface** cmdlet adds a network interface to a virtual machine.</span></span>
<span data-ttu-id="45806-109">您可以在建立虛擬機器或將它新增到現有的虛擬機器中時，新增介面。</span><span class="sxs-lookup"><span data-stu-id="45806-109">You can add an interface when you create a virtual machine or add one to an existing virtual machine.</span></span>

## <span data-ttu-id="45806-110">示例</span><span class="sxs-lookup"><span data-stu-id="45806-110">EXAMPLES</span></span>

### <span data-ttu-id="45806-111">範例1：將網路介面新增至新的虛擬機器</span><span class="sxs-lookup"><span data-stu-id="45806-111">Example 1: Add a network interface to a new virtual machine</span></span>
```
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> Add-AzureRmVMNetworkInterface -VM $VirtualMachine -Id "/subscriptions/46fc8ea4-2de6-4179-8ab1-365da4121af4/resourceGroups/contoso/providers/Microsoft.Network/networkInterfaces/sshNIC"
```

<span data-ttu-id="45806-112">第一個命令會建立一個虛擬電腦物件，然後將它儲存在 $VirtualMachine 變數中。</span><span class="sxs-lookup"><span data-stu-id="45806-112">The first command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="45806-113">該命令會將名稱和大小指派給虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="45806-113">The command assigns a name and size to the virtual machine.</span></span>

<span data-ttu-id="45806-114">第二個命令會將網路介面新增至儲存在 $VirtualMachine 的虛擬機器中。</span><span class="sxs-lookup"><span data-stu-id="45806-114">The second command adds a network interface to the virtual machine stored in $VirtualMachine.</span></span>

### <span data-ttu-id="45806-115">範例2：新增網路介面至現有的虛擬機器</span><span class="sxs-lookup"><span data-stu-id="45806-115">Example 2: Add a network interface to an existing virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> Add-AzureRmVMNetworkInterface -VM $VirtualMachine -Id "/subscriptions/46fc8ea4-2de6-4179-8ab1-365da4121af4/resourceGroups/contoso/providers/Microsoft.Network/networkInterfaces/sshNIC"
PS C:\> Update-AzureRmVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="45806-116">第一個命令會使用 **AzureRmVM** Cmdlet 取得名為 VirtualMachine07 的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="45806-116">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzureRmVM** cmdlet.</span></span>
<span data-ttu-id="45806-117">該命令會將虛擬機器儲存在 $VirtualMachine 變數中。</span><span class="sxs-lookup"><span data-stu-id="45806-117">The command stores the virtual machine in the $VirtualMachine variable.</span></span>

<span data-ttu-id="45806-118">第二個命令會將網路介面新增至儲存在 $VirtualMachine 的虛擬機器中。</span><span class="sxs-lookup"><span data-stu-id="45806-118">The second command adds a network interface to the virtual machine stored in $VirtualMachine.</span></span>

<span data-ttu-id="45806-119">Final 命令會更新儲存在 ResourceGroup11 中 $VirtualMachine 的虛擬機器狀態。</span><span class="sxs-lookup"><span data-stu-id="45806-119">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

## <span data-ttu-id="45806-120">參數</span><span class="sxs-lookup"><span data-stu-id="45806-120">PARAMETERS</span></span>

### <span data-ttu-id="45806-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45806-121">-DefaultProfile</span></span>
<span data-ttu-id="45806-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="45806-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="45806-123">-識別碼</span><span class="sxs-lookup"><span data-stu-id="45806-123">-Id</span></span>
<span data-ttu-id="45806-124">指定要新增至虛擬機器的網路介面識別碼。</span><span class="sxs-lookup"><span data-stu-id="45806-124">Specifies the ID of a network interface to add to a virtual machine.</span></span>
<span data-ttu-id="45806-125">您可以使用 [AzureRmNetworkInterface](/powershell/module/azurerm.network/get-azurermnetworkinterface) Cmdlet 來取得網路介面。</span><span class="sxs-lookup"><span data-stu-id="45806-125">You can use the [Get-AzureRmNetworkInterface](/powershell/module/azurerm.network/get-azurermnetworkinterface) cmdlet to obtain a network interface.</span></span>

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

### <span data-ttu-id="45806-126">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="45806-126">-NetworkInterface</span></span>
<span data-ttu-id="45806-127">指定網路介面。</span><span class="sxs-lookup"><span data-stu-id="45806-127">Specifies the network interface.</span></span>

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

### <span data-ttu-id="45806-128">-主要</span><span class="sxs-lookup"><span data-stu-id="45806-128">-Primary</span></span>
<span data-ttu-id="45806-129">表示此 Cmdlet 會將網路介面新增為主要介面。</span><span class="sxs-lookup"><span data-stu-id="45806-129">Indicates that this cmdlet adds the network interface as the primary interface.</span></span>

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

### <span data-ttu-id="45806-130">-VM</span><span class="sxs-lookup"><span data-stu-id="45806-130">-VM</span></span>
<span data-ttu-id="45806-131">指定要新增網路介面的本機虛擬機器物件。</span><span class="sxs-lookup"><span data-stu-id="45806-131">Specifies a local virtual machine object to which to add a network interface.</span></span>
<span data-ttu-id="45806-132">若要建立虛擬機器，請使用 **AzureRmVMConfig** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="45806-132">To create a virtual machine, use the **New-AzureRmVMConfig** cmdlet.</span></span>
<span data-ttu-id="45806-133">若要取得現有的虛擬機器，請使用 **AzureRmVM** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="45806-133">To obtain an existing virtual machine, use the **Get-AzureRmVM** cmdlet.</span></span>

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

### <span data-ttu-id="45806-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45806-134">CommonParameters</span></span>
<span data-ttu-id="45806-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="45806-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45806-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="45806-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45806-137">輸入</span><span class="sxs-lookup"><span data-stu-id="45806-137">INPUTS</span></span>

### <span data-ttu-id="45806-138">[System.object]。清單 ' 1 [PSNetworkInterface] （）</span><span class="sxs-lookup"><span data-stu-id="45806-138">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.Network.Models.PSNetworkInterface]</span></span>
<span data-ttu-id="45806-139">"NetworkInterface" 參數接受來自管線的 "System.object" 類型的值。清單 ' 1 [PSNetworkInterface]」的值</span><span class="sxs-lookup"><span data-stu-id="45806-139">Parameter 'NetworkInterface' accepts value of type 'System.Collections.Generic.List\`1[Microsoft.Azure.Commands.Network.Models.PSNetworkInterface]' from the pipeline</span></span>

### <span data-ttu-id="45806-140">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="45806-140">PSVirtualMachine</span></span>
<span data-ttu-id="45806-141">[VM "參數從管線接受類型 ' PSVirtualMachine」的值</span><span class="sxs-lookup"><span data-stu-id="45806-141">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="45806-142">輸出</span><span class="sxs-lookup"><span data-stu-id="45806-142">OUTPUTS</span></span>

### <span data-ttu-id="45806-143">PSVirtualMachine 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="45806-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="45806-144">筆記</span><span class="sxs-lookup"><span data-stu-id="45806-144">NOTES</span></span>

## <span data-ttu-id="45806-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="45806-145">RELATED LINKS</span></span>

[<span data-ttu-id="45806-146">新-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="45806-146">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)

[<span data-ttu-id="45806-147">AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="45806-147">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="45806-148">AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="45806-148">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)
