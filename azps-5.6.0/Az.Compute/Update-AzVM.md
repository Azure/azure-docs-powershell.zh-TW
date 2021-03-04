---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 38917534-49C6-47EA-B815-240F794EE655
online version: https://docs.microsoft.com/powershell/module/az.compute/update-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVM.md
ms.openlocfilehash: e7a86b191687f72cb538fb017a904890e4958d50
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902914"
---
# <span data-ttu-id="3c63c-101">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="3c63c-101">Update-AzVM</span></span>

## <span data-ttu-id="3c63c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="3c63c-102">SYNOPSIS</span></span>
<span data-ttu-id="3c63c-103">更新 Azure 虛擬機器的狀態。</span><span class="sxs-lookup"><span data-stu-id="3c63c-103">Updates the state of an Azure virtual machine.</span></span>

## <span data-ttu-id="3c63c-104">語法</span><span class="sxs-lookup"><span data-stu-id="3c63c-104">SYNTAX</span></span>

### <span data-ttu-id="3c63c-105">ResourceGroupNameParameterSetName (預設) </span><span class="sxs-lookup"><span data-stu-id="3c63c-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Update-AzVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>]
 [-OsDiskWriteAccelerator <Boolean>] [-UltraSSDEnabled <Boolean>] [-MaxPrice <Double>]
 [-ProximityPlacementGroupId <String>] [-HostId <String>] [-EncryptionAtHost <Boolean>] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c63c-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="3c63c-106">ExplicitIdentityParameterSet</span></span>
```
Update-AzVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>]
 -IdentityType <ResourceIdentityType> [-IdentityId <String[]>] [-OsDiskWriteAccelerator <Boolean>]
 [-UltraSSDEnabled <Boolean>] [-MaxPrice <Double>] [-ProximityPlacementGroupId <String>] [-HostId <String>]
 [-EncryptionAtHost <Boolean>] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c63c-107">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="3c63c-107">IdParameterSetName</span></span>
```
Update-AzVM [-Id] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>] [-OsDiskWriteAccelerator <Boolean>]
 [-UltraSSDEnabled <Boolean>] [-MaxPrice <Double>] [-ProximityPlacementGroupId <String>] [-HostId <String>]
 [-EncryptionAtHost <Boolean>] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3c63c-108">描述</span><span class="sxs-lookup"><span data-stu-id="3c63c-108">DESCRIPTION</span></span>
<span data-ttu-id="3c63c-109">**Update-AzMS** Cmdlet 將 Azure 虛擬機器的狀態更新為虛擬機器物件的狀態。</span><span class="sxs-lookup"><span data-stu-id="3c63c-109">The **Update-AzVM** cmdlet updates the state of an Azure virtual machine to the state of a virtual machine object.</span></span>

## <span data-ttu-id="3c63c-110">例子</span><span class="sxs-lookup"><span data-stu-id="3c63c-110">EXAMPLES</span></span>

### <span data-ttu-id="3c63c-111">範例 1：更新虛擬機器</span><span class="sxs-lookup"><span data-stu-id="3c63c-111">Example 1: Update a virtual machine</span></span>
```
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="3c63c-112">此命令會更新 ResourceGroup11 $VirtualMachine的虛擬機器 。.</span><span class="sxs-lookup"><span data-stu-id="3c63c-112">This command updates the virtual machine, $VirtualMachine, in ResourceGroup11.</span></span>
<span data-ttu-id="3c63c-113">命令會使用儲存在變數中的虛擬機器$VirtualMachine更新。</span><span class="sxs-lookup"><span data-stu-id="3c63c-113">The command updates it by using the virtual machine object stored in the $VirtualMachine variable.</span></span>
<span data-ttu-id="3c63c-114">若要取得虛擬機器物件，請使用 **Get-Az%。CMdlet。**</span><span class="sxs-lookup"><span data-stu-id="3c63c-114">To obtain a virtual machine object, use the **Get-AzVM** cmdlet.</span></span>

## <span data-ttu-id="3c63c-115">參數</span><span class="sxs-lookup"><span data-stu-id="3c63c-115">PARAMETERS</span></span>

### <span data-ttu-id="3c63c-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3c63c-116">-AsJob</span></span>
<span data-ttu-id="3c63c-117">在背景中執行 Cmdlet 並返回工作以追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="3c63c-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="3c63c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c63c-118">-DefaultProfile</span></span>
<span data-ttu-id="3c63c-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="3c63c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3c63c-120">-HostId</span><span class="sxs-lookup"><span data-stu-id="3c63c-120">-HostId</span></span>
<span data-ttu-id="3c63c-121">主機名稱</span><span class="sxs-lookup"><span data-stu-id="3c63c-121">The Id of Host</span></span>

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

### <span data-ttu-id="3c63c-122">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="3c63c-122">-EncryptionAtHost</span></span>
<span data-ttu-id="3c63c-123">使用者可在要求中使用 EncryptionAtHost 屬性，以啟用或停用虛擬機器或虛擬機器縮放集的主機加密。</span><span class="sxs-lookup"><span data-stu-id="3c63c-123">EncryptionAtHost property can be used by user in the request to enable or disable the Host Encryption for the virtual machine or virtual machine scale set.</span></span> <span data-ttu-id="3c63c-124">這會啟用所有磁片的加密，包括主機本身的資源/Temp 磁片。</span><span class="sxs-lookup"><span data-stu-id="3c63c-124">This will enable the encryption for all the disks including Resource/Temp disk at host itself.</span></span> 

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c63c-125">-Id</span><span class="sxs-lookup"><span data-stu-id="3c63c-125">-Id</span></span>
<span data-ttu-id="3c63c-126">指定虛擬機器的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="3c63c-126">Specifies the resource ID of the virtual machine.</span></span>

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

### <span data-ttu-id="3c63c-127">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="3c63c-127">-IdentityId</span></span>
<span data-ttu-id="3c63c-128">指定與虛擬機器相關聯的使用者身分清單。</span><span class="sxs-lookup"><span data-stu-id="3c63c-128">Specifies the list of user identities associated with the virtual machine.</span></span>
<span data-ttu-id="3c63c-129">使用者身分識別參照為表單中的 ARM 資源識別碼：'/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identityies/{identityName}'</span><span class="sxs-lookup"><span data-stu-id="3c63c-129">The user identity references will be ARM resource IDs in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="3c63c-130">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="3c63c-130">-IdentityType</span></span>
<span data-ttu-id="3c63c-131">用於虛擬機器的身分識別類型。</span><span class="sxs-lookup"><span data-stu-id="3c63c-131">The type of identity used for the virtual machine.</span></span> <span data-ttu-id="3c63c-132">有效的值為 SystemAssigned、UserAssigned、SystemAssignedUserAssigned 和 None。</span><span class="sxs-lookup"><span data-stu-id="3c63c-132">Valid values are SystemAssigned, UserAssigned, SystemAssignedUserAssigned, and None.</span></span>

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

### <span data-ttu-id="3c63c-133">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="3c63c-133">-MaxPrice</span></span>
<span data-ttu-id="3c63c-134">指定您願意為低優先順序 VM/VMSS 支付的最高價格。</span><span class="sxs-lookup"><span data-stu-id="3c63c-134">Specifies the maximum price you are willing to pay for a low priority VM/VMSS.</span></span> <span data-ttu-id="3c63c-135">此價格為美元。</span><span class="sxs-lookup"><span data-stu-id="3c63c-135">This price is in US Dollars.</span></span> <span data-ttu-id="3c63c-136">此價格會與 VM 大小目前低優先順序價格進行比較。</span><span class="sxs-lookup"><span data-stu-id="3c63c-136">This price will be compared with the current low priority price for the VM size.</span></span> <span data-ttu-id="3c63c-137">此外，在建立/更新低優先順序 VM/VMSS 時，會比較價格，且只有在 maxPrice 大於目前低優先順序價格時，作業才能成功。</span><span class="sxs-lookup"><span data-stu-id="3c63c-137">Also, the prices are compared at the time of create/update of low priority VM/VMSS and the operation will only succeed if the maxPrice is greater than the current low priority price.</span></span> <span data-ttu-id="3c63c-138">如果建立 VM/VMSS 之後，目前的低優先順序價格超出 maxPrice，maxPrice 也會用於評估低優先順序的 VM/VMSS。</span><span class="sxs-lookup"><span data-stu-id="3c63c-138">The maxPrice will also be used for evicting a low priority VM/VMSS if the current low priority price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="3c63c-139">可能的值為：任何大於零的十進位值。</span><span class="sxs-lookup"><span data-stu-id="3c63c-139">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="3c63c-140">範例：0.01538。</span><span class="sxs-lookup"><span data-stu-id="3c63c-140">Example: 0.01538.</span></span>  <span data-ttu-id="3c63c-141">-1 表示基於價格考慮，不應將低優先順序的 VM/VMSS 從上而退出。</span><span class="sxs-lookup"><span data-stu-id="3c63c-141">-1 indicates that the low priority VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="3c63c-142">此外，如果您未提供，預設最高價格為 -1。</span><span class="sxs-lookup"><span data-stu-id="3c63c-142">Also, the default max price is -1 if it is not provided by you.</span></span>

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

### <span data-ttu-id="3c63c-143">-NoWait</span><span class="sxs-lookup"><span data-stu-id="3c63c-143">-NoWait</span></span>
<span data-ttu-id="3c63c-144">啟動作業，並立即在作業完成之前返回。</span><span class="sxs-lookup"><span data-stu-id="3c63c-144">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="3c63c-145">若要判斷作業是否成功完成，請使用一些其他機制。</span><span class="sxs-lookup"><span data-stu-id="3c63c-145">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="3c63c-146">-OsRiteWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="3c63c-146">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="3c63c-147">指定作業系統磁片上是否應該啟用或停用 WriteAccelerator。</span><span class="sxs-lookup"><span data-stu-id="3c63c-147">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="3c63c-148">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="3c63c-148">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="3c63c-149">要用於此虛擬機器的鄰近位置群組資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="3c63c-149">The resource id of the Proximity Placement Group to use with this virtual machine.</span></span>

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

### <span data-ttu-id="3c63c-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c63c-150">-ResourceGroupName</span></span>
<span data-ttu-id="3c63c-151">指定虛擬機器的資源組名。</span><span class="sxs-lookup"><span data-stu-id="3c63c-151">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName, ExplicitIdentityParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c63c-152">-標記</span><span class="sxs-lookup"><span data-stu-id="3c63c-152">-Tag</span></span>
<span data-ttu-id="3c63c-153">指定可以使用一組名稱值組標記資源和資源群組。</span><span class="sxs-lookup"><span data-stu-id="3c63c-153">Specifies the resources and resource groups can be tagged with a set of name-value pairs.</span></span>
<span data-ttu-id="3c63c-154">將標記新增到資源，可讓您跨資源群組將資源分組，以及建立您自己的視圖。</span><span class="sxs-lookup"><span data-stu-id="3c63c-154">Adding tags to resources enables you to group resources together across resource groups and to create your own views.</span></span>
<span data-ttu-id="3c63c-155">每個資源或資源群組最多可以有 15 個標記。</span><span class="sxs-lookup"><span data-stu-id="3c63c-155">Each resource or resource group can have a maximum of 15 tags.</span></span>

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

### <span data-ttu-id="3c63c-156">-UltraSSDEnabled</span><span class="sxs-lookup"><span data-stu-id="3c63c-156">-UltraSSDEnabled</span></span>
<span data-ttu-id="3c63c-157">可啟用或停用一或多個受管理資料磁片的標UltraSSD_LRS在 VM 上儲存帳戶類型。</span><span class="sxs-lookup"><span data-stu-id="3c63c-157">The flag that enables or disables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the VM.</span></span>
<span data-ttu-id="3c63c-158">只有啟用此屬性UltraSSD_LRS才能將具有儲存帳戶類型的受管理磁片新增到虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="3c63c-158">Managed disks with storage account type UltraSSD_LRS can be added to a virtual machine only if this property is enabled.</span></span>

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

### <span data-ttu-id="3c63c-159">-VM</span><span class="sxs-lookup"><span data-stu-id="3c63c-159">-VM</span></span>
<span data-ttu-id="3c63c-160">指定本機虛擬機器物件。</span><span class="sxs-lookup"><span data-stu-id="3c63c-160">Specifies a local virtual machine object.</span></span>
<span data-ttu-id="3c63c-161">若要取得虛擬機器物件，請使用 Get-AzVM Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3c63c-161">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="3c63c-162">此虛擬機器物件包含虛擬機器的更新狀態。</span><span class="sxs-lookup"><span data-stu-id="3c63c-162">This virtual machine object contains the updated state for the virtual machine.</span></span>

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

### <span data-ttu-id="3c63c-163">-確認</span><span class="sxs-lookup"><span data-stu-id="3c63c-163">-Confirm</span></span>
<span data-ttu-id="3c63c-164">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="3c63c-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c63c-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c63c-165">-WhatIf</span></span>
<span data-ttu-id="3c63c-166">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3c63c-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c63c-167">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3c63c-167">The cmdlet is not run.</span></span>

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


### <span data-ttu-id="3c63c-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c63c-168">CommonParameters</span></span>
<span data-ttu-id="3c63c-169">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="3c63c-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c63c-170">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3c63c-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c63c-171">輸入</span><span class="sxs-lookup"><span data-stu-id="3c63c-171">INPUTS</span></span>

### <span data-ttu-id="3c63c-172">System.String</span><span class="sxs-lookup"><span data-stu-id="3c63c-172">System.String</span></span>

### <span data-ttu-id="3c63c-173">Microsoft.Azure.Commands.Compute.models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="3c63c-173">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="3c63c-174">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3c63c-174">System.Boolean</span></span>

## <span data-ttu-id="3c63c-175">輸出</span><span class="sxs-lookup"><span data-stu-id="3c63c-175">OUTPUTS</span></span>

### <span data-ttu-id="3c63c-176">Microsoft.Azure.Commands.Compute.models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="3c63c-176">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="3c63c-177">筆記</span><span class="sxs-lookup"><span data-stu-id="3c63c-177">NOTES</span></span>

## <span data-ttu-id="3c63c-178">相關連結</span><span class="sxs-lookup"><span data-stu-id="3c63c-178">RELATED LINKS</span></span>

[<span data-ttu-id="3c63c-179">Get-AzMS</span><span class="sxs-lookup"><span data-stu-id="3c63c-179">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="3c63c-180">New-AzMS</span><span class="sxs-lookup"><span data-stu-id="3c63c-180">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="3c63c-181">Remove-AzMS</span><span class="sxs-lookup"><span data-stu-id="3c63c-181">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="3c63c-182">Restart-AzMS</span><span class="sxs-lookup"><span data-stu-id="3c63c-182">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="3c63c-183">Start-AzMS</span><span class="sxs-lookup"><span data-stu-id="3c63c-183">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="3c63c-184">Stop-AzMS</span><span class="sxs-lookup"><span data-stu-id="3c63c-184">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="3c63c-185">New-AzMSCONFIG</span><span class="sxs-lookup"><span data-stu-id="3c63c-185">New-AzVMConfig</span></span>](./New-AzVMConfig.md)


