---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 38917534-49C6-47EA-B815-240F794EE655
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVM.md
ms.openlocfilehash: 6be4e505dfdacdc95e6ab3c9f7229fa4d1e470f1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93958506"
---
# <span data-ttu-id="1de96-101">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="1de96-101">Update-AzVM</span></span>

## <span data-ttu-id="1de96-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1de96-102">SYNOPSIS</span></span>
<span data-ttu-id="1de96-103">更新 Azure 虛擬機器的狀態。</span><span class="sxs-lookup"><span data-stu-id="1de96-103">Updates the state of an Azure virtual machine.</span></span>

## <span data-ttu-id="1de96-104">句法</span><span class="sxs-lookup"><span data-stu-id="1de96-104">SYNTAX</span></span>

### <span data-ttu-id="1de96-105">ResourceGroupNameParameterSetName (預設) </span><span class="sxs-lookup"><span data-stu-id="1de96-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Update-AzVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>]
 [-OsDiskWriteAccelerator <Boolean>] [-UltraSSDEnabled <Boolean>] [-MaxPrice <Double>]
 [-ProximityPlacementGroupId <String>] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1de96-106">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="1de96-106">AssignIdentityParameterSet</span></span>
```
Update-AzVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>] [-AssignIdentity]
 [-OsDiskWriteAccelerator <Boolean>] [-UltraSSDEnabled <Boolean>] [-MaxPrice <Double>]
 [-ProximityPlacementGroupId <String>] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1de96-107">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="1de96-107">ExplicitIdentityParameterSet</span></span>
```
Update-AzVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>]
 -IdentityType <ResourceIdentityType> [-IdentityId <String[]>] [-OsDiskWriteAccelerator <Boolean>]
 [-UltraSSDEnabled <Boolean>] [-MaxPrice <Double>] [-ProximityPlacementGroupId <String>] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1de96-108">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="1de96-108">IdParameterSetName</span></span>
```
Update-AzVM [-Id] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>] [-OsDiskWriteAccelerator <Boolean>]
 [-UltraSSDEnabled <Boolean>] [-MaxPrice <Double>] [-ProximityPlacementGroupId <String>] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1de96-109">說明</span><span class="sxs-lookup"><span data-stu-id="1de96-109">DESCRIPTION</span></span>
<span data-ttu-id="1de96-110">**AzVM** Cmdlet 會將 Azure 虛擬機器的狀態更新為虛擬機器物件的狀態。</span><span class="sxs-lookup"><span data-stu-id="1de96-110">The **Update-AzVM** cmdlet updates the state of an Azure virtual machine to the state of a virtual machine object.</span></span>

## <span data-ttu-id="1de96-111">示例</span><span class="sxs-lookup"><span data-stu-id="1de96-111">EXAMPLES</span></span>

### <span data-ttu-id="1de96-112">範例1：更新虛擬機器</span><span class="sxs-lookup"><span data-stu-id="1de96-112">Example 1: Update a virtual machine</span></span>
```
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="1de96-113">這個命令會在 ResourceGroup11 中更新虛擬機器，$VirtualMachine。</span><span class="sxs-lookup"><span data-stu-id="1de96-113">This command updates the virtual machine, $VirtualMachine, in ResourceGroup11.</span></span>
<span data-ttu-id="1de96-114">此命令會使用儲存在 $VirtualMachine 變數中的虛擬機器物件來更新它。</span><span class="sxs-lookup"><span data-stu-id="1de96-114">The command updates it by using the virtual machine object stored in the $VirtualMachine variable.</span></span>
<span data-ttu-id="1de96-115">若要取得虛擬機器物件，請使用 **AzVM** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1de96-115">To obtain a virtual machine object, use the **Get-AzVM** cmdlet.</span></span>

## <span data-ttu-id="1de96-116">參數</span><span class="sxs-lookup"><span data-stu-id="1de96-116">PARAMETERS</span></span>

### <span data-ttu-id="1de96-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1de96-117">-AsJob</span></span>
<span data-ttu-id="1de96-118">在背景中執行 Cmdlet，然後返回作業來追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="1de96-118">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="1de96-119">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="1de96-119">-AssignIdentity</span></span>
<span data-ttu-id="1de96-120">指定虛擬機器的系統指派身分識別。</span><span class="sxs-lookup"><span data-stu-id="1de96-120">Specify the system-assigned identity for the virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AssignIdentityParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1de96-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1de96-121">-DefaultProfile</span></span>
<span data-ttu-id="1de96-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1de96-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1de96-123">-識別碼</span><span class="sxs-lookup"><span data-stu-id="1de96-123">-Id</span></span>
<span data-ttu-id="1de96-124">指定虛擬機器的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="1de96-124">Specifies the resource ID of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1de96-125">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="1de96-125">-IdentityId</span></span>
<span data-ttu-id="1de96-126">指定與虛擬機器相關聯的使用者識別碼清單。</span><span class="sxs-lookup"><span data-stu-id="1de96-126">Specifies the list of user identities associated with the virtual machine.</span></span>
<span data-ttu-id="1de96-127">使用者身分識別參照將是下列形式的 ARM 資源識別碼： '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName} '</span><span class="sxs-lookup"><span data-stu-id="1de96-127">The user identity references will be ARM resource IDs in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

```yaml
Type: System.String[]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1de96-128">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="1de96-128">-IdentityType</span></span>
<span data-ttu-id="1de96-129">虛擬機器所用的身分識別類型。</span><span class="sxs-lookup"><span data-stu-id="1de96-129">The type of identity used for the virtual machine.</span></span> <span data-ttu-id="1de96-130">有效值為 SystemAssigned、UserAssigned、SystemAssignedUserAssigned 和 None。</span><span class="sxs-lookup"><span data-stu-id="1de96-130">Valid values are SystemAssigned, UserAssigned, SystemAssignedUserAssigned, and None.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:
Accepted values: SystemAssigned, UserAssigned, SystemAssignedUserAssigned, None

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1de96-131">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="1de96-131">-MaxPrice</span></span>
<span data-ttu-id="1de96-132">指定低優先順序 VM/VMSS 要支付的最大價格。</span><span class="sxs-lookup"><span data-stu-id="1de96-132">Specifies the maximum price you are willing to pay for a low priority VM/VMSS.</span></span> <span data-ttu-id="1de96-133">這個價格是美元。</span><span class="sxs-lookup"><span data-stu-id="1de96-133">This price is in US Dollars.</span></span> <span data-ttu-id="1de96-134">此價格將與 VM 大小的目前低優先順序價格進行比較。</span><span class="sxs-lookup"><span data-stu-id="1de96-134">This price will be compared with the current low priority price for the VM size.</span></span> <span data-ttu-id="1de96-135">此外，價格會在建立/更新低優先順序 VM/VMSS 的時間進行比較，而且只有在 maxPrice 大於目前的低優先順序價格時，作業才會成功。</span><span class="sxs-lookup"><span data-stu-id="1de96-135">Also, the prices are compared at the time of create/update of low priority VM/VMSS and the operation will only succeed if the maxPrice is greater than the current low priority price.</span></span> <span data-ttu-id="1de96-136">如果在建立 VM/VMSS 之後，目前的低優先順序價格超過 maxPrice，則 maxPrice 也會用於逐出低優先順序 VM/VMSS。</span><span class="sxs-lookup"><span data-stu-id="1de96-136">The maxPrice will also be used for evicting a low priority VM/VMSS if the current low priority price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="1de96-137">可能的值為：任何大於零的十進位值。</span><span class="sxs-lookup"><span data-stu-id="1de96-137">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="1de96-138">範例：0.01538。</span><span class="sxs-lookup"><span data-stu-id="1de96-138">Example: 0.01538.</span></span>  <span data-ttu-id="1de96-139">-1 表示由於價格原因，不應逐出低優先順序 VM/VMSS。</span><span class="sxs-lookup"><span data-stu-id="1de96-139">-1 indicates that the low priority VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="1de96-140">此外，如果您沒有提供預設的最大價格，就是-1。</span><span class="sxs-lookup"><span data-stu-id="1de96-140">Also, the default max price is -1 if it is not provided by you.</span></span>

```yaml
Type: System.Double
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1de96-141">-NoWait</span><span class="sxs-lookup"><span data-stu-id="1de96-141">-NoWait</span></span>
<span data-ttu-id="1de96-142">在作業完成之前，立即開始作業並立即返回。</span><span class="sxs-lookup"><span data-stu-id="1de96-142">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="1de96-143">若要判斷該作業是否已順利完成，請使用一些其他的機制。</span><span class="sxs-lookup"><span data-stu-id="1de96-143">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="1de96-144">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="1de96-144">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="1de96-145">指定是否應該在 OS 磁片上啟用或停用 WriteAccelerator。</span><span class="sxs-lookup"><span data-stu-id="1de96-145">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1de96-146">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="1de96-146">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="1de96-147">要搭配此虛擬機器使用之鄰近性位置群組的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="1de96-147">The resource id of the Proximity Placement Group to use with this virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1de96-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1de96-148">-ResourceGroupName</span></span>
<span data-ttu-id="1de96-149">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1de96-149">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName, AssignIdentityParameterSet, ExplicitIdentityParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1de96-150">-Tag</span><span class="sxs-lookup"><span data-stu-id="1de96-150">-Tag</span></span>
<span data-ttu-id="1de96-151">指定可使用一組名稱值對來標記資源和資源群組。</span><span class="sxs-lookup"><span data-stu-id="1de96-151">Specifies the resources and resource groups can be tagged with a set of name-value pairs.</span></span>
<span data-ttu-id="1de96-152">新增標籤至資源之後，您就可以將資源群組集中在不同的資源群組中，以及建立您自己的視圖。</span><span class="sxs-lookup"><span data-stu-id="1de96-152">Adding tags to resources enables you to group resources together across resource groups and to create your own views.</span></span>
<span data-ttu-id="1de96-153">每個資源或資源群組最多可以有15個標籤。</span><span class="sxs-lookup"><span data-stu-id="1de96-153">Each resource or resource group can have a maximum of 15 tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1de96-154">-UltraSSDEnabled</span><span class="sxs-lookup"><span data-stu-id="1de96-154">-UltraSSDEnabled</span></span>
<span data-ttu-id="1de96-155">啟用或停用在 VM 上擁有 UltraSSD_LRS 儲存帳戶類型之一或多個受管理資料磁片之功能的標誌。</span><span class="sxs-lookup"><span data-stu-id="1de96-155">The flag that enables or disables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the VM.</span></span>
<span data-ttu-id="1de96-156">只有在啟用此屬性時，才能將儲存帳戶類型 UltraSSD_LRS 的受管理磁片新增至虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="1de96-156">Managed disks with storage account type UltraSSD_LRS can be added to a virtual machine only if this property is enabled.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1de96-157">-VM</span><span class="sxs-lookup"><span data-stu-id="1de96-157">-VM</span></span>
<span data-ttu-id="1de96-158">指定本機虛擬電腦物件。</span><span class="sxs-lookup"><span data-stu-id="1de96-158">Specifies a local virtual machine object.</span></span>
<span data-ttu-id="1de96-159">若要取得虛擬機器物件，請使用 Get-AzVM Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1de96-159">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="1de96-160">此虛擬機器物件包含虛擬機器的更新狀態。</span><span class="sxs-lookup"><span data-stu-id="1de96-160">This virtual machine object contains the updated state for the virtual machine.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1de96-161">-確認</span><span class="sxs-lookup"><span data-stu-id="1de96-161">-Confirm</span></span>
<span data-ttu-id="1de96-162">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1de96-162">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1de96-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1de96-163">-WhatIf</span></span>
<span data-ttu-id="1de96-164">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1de96-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1de96-165">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1de96-165">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1de96-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1de96-166">CommonParameters</span></span>
<span data-ttu-id="1de96-167">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1de96-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1de96-168">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="1de96-168">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1de96-169">輸入</span><span class="sxs-lookup"><span data-stu-id="1de96-169">INPUTS</span></span>

### <span data-ttu-id="1de96-170">System.object</span><span class="sxs-lookup"><span data-stu-id="1de96-170">System.String</span></span>

### <span data-ttu-id="1de96-171">PSVirtualMachine 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="1de96-171">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="1de96-172">System.object</span><span class="sxs-lookup"><span data-stu-id="1de96-172">System.Boolean</span></span>

## <span data-ttu-id="1de96-173">輸出</span><span class="sxs-lookup"><span data-stu-id="1de96-173">OUTPUTS</span></span>

### <span data-ttu-id="1de96-174">PSAzureOperationResponse 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="1de96-174">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="1de96-175">筆記</span><span class="sxs-lookup"><span data-stu-id="1de96-175">NOTES</span></span>

## <span data-ttu-id="1de96-176">相關連結</span><span class="sxs-lookup"><span data-stu-id="1de96-176">RELATED LINKS</span></span>

[<span data-ttu-id="1de96-177">AzVM</span><span class="sxs-lookup"><span data-stu-id="1de96-177">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="1de96-178">新-AzVM</span><span class="sxs-lookup"><span data-stu-id="1de96-178">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="1de96-179">移除-AzVM</span><span class="sxs-lookup"><span data-stu-id="1de96-179">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="1de96-180">重新開機-AzVM</span><span class="sxs-lookup"><span data-stu-id="1de96-180">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="1de96-181">開始-AzVM</span><span class="sxs-lookup"><span data-stu-id="1de96-181">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="1de96-182">停止 AzVM</span><span class="sxs-lookup"><span data-stu-id="1de96-182">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="1de96-183">新-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="1de96-183">New-AzVMConfig</span></span>](./New-AzVMConfig.md)


