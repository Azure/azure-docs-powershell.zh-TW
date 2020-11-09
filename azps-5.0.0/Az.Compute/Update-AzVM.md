---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 38917534-49C6-47EA-B815-240F794EE655
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVM.md
ms.openlocfilehash: e9ec68d7c3991d7a3eded2566d8e299ddcc36c85
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94284499"
---
# <span data-ttu-id="a7dff-101">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="a7dff-101">Update-AzVM</span></span>

## <span data-ttu-id="a7dff-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a7dff-102">SYNOPSIS</span></span>
<span data-ttu-id="a7dff-103">更新 Azure 虛擬機器的狀態。</span><span class="sxs-lookup"><span data-stu-id="a7dff-103">Updates the state of an Azure virtual machine.</span></span>

## <span data-ttu-id="a7dff-104">句法</span><span class="sxs-lookup"><span data-stu-id="a7dff-104">SYNTAX</span></span>

### <span data-ttu-id="a7dff-105">ResourceGroupNameParameterSetName (預設) </span><span class="sxs-lookup"><span data-stu-id="a7dff-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Update-AzVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>]
 [-OsDiskWriteAccelerator <Boolean>] [-UltraSSDEnabled <Boolean>] [-MaxPrice <Double>]
 [-ProximityPlacementGroupId <String>] [-HostId <String>] [-EncryptionAtHost <Boolean>] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7dff-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="a7dff-106">ExplicitIdentityParameterSet</span></span>
```
Update-AzVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>]
 -IdentityType <ResourceIdentityType> [-IdentityId <String[]>] [-OsDiskWriteAccelerator <Boolean>]
 [-UltraSSDEnabled <Boolean>] [-MaxPrice <Double>] [-ProximityPlacementGroupId <String>] [-HostId <String>]
 [-EncryptionAtHost <Boolean>] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7dff-107">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="a7dff-107">IdParameterSetName</span></span>
```
Update-AzVM [-Id] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>] [-OsDiskWriteAccelerator <Boolean>]
 [-UltraSSDEnabled <Boolean>] [-MaxPrice <Double>] [-ProximityPlacementGroupId <String>] [-HostId <String>]
 [-EncryptionAtHost <Boolean>] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a7dff-108">說明</span><span class="sxs-lookup"><span data-stu-id="a7dff-108">DESCRIPTION</span></span>
<span data-ttu-id="a7dff-109">**AzVM** Cmdlet 會將 Azure 虛擬機器的狀態更新為虛擬機器物件的狀態。</span><span class="sxs-lookup"><span data-stu-id="a7dff-109">The **Update-AzVM** cmdlet updates the state of an Azure virtual machine to the state of a virtual machine object.</span></span>

## <span data-ttu-id="a7dff-110">示例</span><span class="sxs-lookup"><span data-stu-id="a7dff-110">EXAMPLES</span></span>

### <span data-ttu-id="a7dff-111">範例1：更新虛擬機器</span><span class="sxs-lookup"><span data-stu-id="a7dff-111">Example 1: Update a virtual machine</span></span>
```
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="a7dff-112">這個命令會在 ResourceGroup11 中更新虛擬機器，$VirtualMachine。</span><span class="sxs-lookup"><span data-stu-id="a7dff-112">This command updates the virtual machine, $VirtualMachine, in ResourceGroup11.</span></span>
<span data-ttu-id="a7dff-113">此命令會使用儲存在 $VirtualMachine 變數中的虛擬機器物件來更新它。</span><span class="sxs-lookup"><span data-stu-id="a7dff-113">The command updates it by using the virtual machine object stored in the $VirtualMachine variable.</span></span>
<span data-ttu-id="a7dff-114">若要取得虛擬機器物件，請使用 **AzVM** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a7dff-114">To obtain a virtual machine object, use the **Get-AzVM** cmdlet.</span></span>

## <span data-ttu-id="a7dff-115">參數</span><span class="sxs-lookup"><span data-stu-id="a7dff-115">PARAMETERS</span></span>

### <span data-ttu-id="a7dff-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a7dff-116">-AsJob</span></span>
<span data-ttu-id="a7dff-117">在背景中執行 Cmdlet，然後返回作業來追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="a7dff-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="a7dff-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7dff-118">-DefaultProfile</span></span>
<span data-ttu-id="a7dff-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a7dff-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a7dff-120">-HostId</span><span class="sxs-lookup"><span data-stu-id="a7dff-120">-HostId</span></span>
<span data-ttu-id="a7dff-121">主機的識別碼</span><span class="sxs-lookup"><span data-stu-id="a7dff-121">The Id of Host</span></span>

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

### <span data-ttu-id="a7dff-122">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="a7dff-122">-EncryptionAtHost</span></span>
<span data-ttu-id="a7dff-123">使用者可以在要求中使用 EncryptionAtHost 屬性，以啟用或停用虛擬機器或虛擬機器規模設定的主機加密。</span><span class="sxs-lookup"><span data-stu-id="a7dff-123">EncryptionAtHost property can be used by user in the request to enable or disable the Host Encryption for the virtual machine or virtual machine scale set.</span></span> <span data-ttu-id="a7dff-124">這會啟用所有磁片的加密，包括主機本身的資源/Temp 磁片。</span><span class="sxs-lookup"><span data-stu-id="a7dff-124">This will enable the encryption for all the disks including Resource/Temp disk at host itself.</span></span> 

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

### <span data-ttu-id="a7dff-125">-識別碼</span><span class="sxs-lookup"><span data-stu-id="a7dff-125">-Id</span></span>
<span data-ttu-id="a7dff-126">指定虛擬機器的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="a7dff-126">Specifies the resource ID of the virtual machine.</span></span>

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

### <span data-ttu-id="a7dff-127">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="a7dff-127">-IdentityId</span></span>
<span data-ttu-id="a7dff-128">指定與虛擬機器相關聯的使用者識別碼清單。</span><span class="sxs-lookup"><span data-stu-id="a7dff-128">Specifies the list of user identities associated with the virtual machine.</span></span>
<span data-ttu-id="a7dff-129">使用者身分識別參照將是下列形式的 ARM 資源識別碼： '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName} '</span><span class="sxs-lookup"><span data-stu-id="a7dff-129">The user identity references will be ARM resource IDs in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="a7dff-130">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="a7dff-130">-IdentityType</span></span>
<span data-ttu-id="a7dff-131">虛擬機器所用的身分識別類型。</span><span class="sxs-lookup"><span data-stu-id="a7dff-131">The type of identity used for the virtual machine.</span></span> <span data-ttu-id="a7dff-132">有效值為 SystemAssigned、UserAssigned、SystemAssignedUserAssigned 和 None。</span><span class="sxs-lookup"><span data-stu-id="a7dff-132">Valid values are SystemAssigned, UserAssigned, SystemAssignedUserAssigned, and None.</span></span>

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

### <span data-ttu-id="a7dff-133">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="a7dff-133">-MaxPrice</span></span>
<span data-ttu-id="a7dff-134">指定低優先順序 VM/VMSS 要支付的最大價格。</span><span class="sxs-lookup"><span data-stu-id="a7dff-134">Specifies the maximum price you are willing to pay for a low priority VM/VMSS.</span></span> <span data-ttu-id="a7dff-135">這個價格是美元。</span><span class="sxs-lookup"><span data-stu-id="a7dff-135">This price is in US Dollars.</span></span> <span data-ttu-id="a7dff-136">此價格將與 VM 大小的目前低優先順序價格進行比較。</span><span class="sxs-lookup"><span data-stu-id="a7dff-136">This price will be compared with the current low priority price for the VM size.</span></span> <span data-ttu-id="a7dff-137">此外，價格會在建立/更新低優先順序 VM/VMSS 的時間進行比較，而且只有在 maxPrice 大於目前的低優先順序價格時，作業才會成功。</span><span class="sxs-lookup"><span data-stu-id="a7dff-137">Also, the prices are compared at the time of create/update of low priority VM/VMSS and the operation will only succeed if the maxPrice is greater than the current low priority price.</span></span> <span data-ttu-id="a7dff-138">如果在建立 VM/VMSS 之後，目前的低優先順序價格超過 maxPrice，則 maxPrice 也會用於逐出低優先順序 VM/VMSS。</span><span class="sxs-lookup"><span data-stu-id="a7dff-138">The maxPrice will also be used for evicting a low priority VM/VMSS if the current low priority price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="a7dff-139">可能的值為：任何大於零的十進位值。</span><span class="sxs-lookup"><span data-stu-id="a7dff-139">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="a7dff-140">範例：0.01538。</span><span class="sxs-lookup"><span data-stu-id="a7dff-140">Example: 0.01538.</span></span>  <span data-ttu-id="a7dff-141">-1 表示由於價格原因，不應逐出低優先順序 VM/VMSS。</span><span class="sxs-lookup"><span data-stu-id="a7dff-141">-1 indicates that the low priority VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="a7dff-142">此外，如果您沒有提供預設的最大價格，就是-1。</span><span class="sxs-lookup"><span data-stu-id="a7dff-142">Also, the default max price is -1 if it is not provided by you.</span></span>

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

### <span data-ttu-id="a7dff-143">-NoWait</span><span class="sxs-lookup"><span data-stu-id="a7dff-143">-NoWait</span></span>
<span data-ttu-id="a7dff-144">在作業完成之前，立即開始作業並立即返回。</span><span class="sxs-lookup"><span data-stu-id="a7dff-144">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="a7dff-145">若要判斷該作業是否已順利完成，請使用一些其他的機制。</span><span class="sxs-lookup"><span data-stu-id="a7dff-145">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="a7dff-146">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="a7dff-146">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="a7dff-147">指定是否應該在 OS 磁片上啟用或停用 WriteAccelerator。</span><span class="sxs-lookup"><span data-stu-id="a7dff-147">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="a7dff-148">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="a7dff-148">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="a7dff-149">要搭配此虛擬機器使用之鄰近性位置群組的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="a7dff-149">The resource id of the Proximity Placement Group to use with this virtual machine.</span></span>

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

### <span data-ttu-id="a7dff-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7dff-150">-ResourceGroupName</span></span>
<span data-ttu-id="a7dff-151">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a7dff-151">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="a7dff-152">-Tag</span><span class="sxs-lookup"><span data-stu-id="a7dff-152">-Tag</span></span>
<span data-ttu-id="a7dff-153">指定可使用一組名稱值對來標記資源和資源群組。</span><span class="sxs-lookup"><span data-stu-id="a7dff-153">Specifies the resources and resource groups can be tagged with a set of name-value pairs.</span></span>
<span data-ttu-id="a7dff-154">新增標籤至資源之後，您就可以將資源群組集中在不同的資源群組中，以及建立您自己的視圖。</span><span class="sxs-lookup"><span data-stu-id="a7dff-154">Adding tags to resources enables you to group resources together across resource groups and to create your own views.</span></span>
<span data-ttu-id="a7dff-155">每個資源或資源群組最多可以有15個標籤。</span><span class="sxs-lookup"><span data-stu-id="a7dff-155">Each resource or resource group can have a maximum of 15 tags.</span></span>

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

### <span data-ttu-id="a7dff-156">-UltraSSDEnabled</span><span class="sxs-lookup"><span data-stu-id="a7dff-156">-UltraSSDEnabled</span></span>
<span data-ttu-id="a7dff-157">啟用或停用在 VM 上擁有 UltraSSD_LRS 儲存帳戶類型之一或多個受管理資料磁片之功能的標誌。</span><span class="sxs-lookup"><span data-stu-id="a7dff-157">The flag that enables or disables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the VM.</span></span>
<span data-ttu-id="a7dff-158">只有在啟用此屬性時，才能將儲存帳戶類型 UltraSSD_LRS 的受管理磁片新增至虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="a7dff-158">Managed disks with storage account type UltraSSD_LRS can be added to a virtual machine only if this property is enabled.</span></span>

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

### <span data-ttu-id="a7dff-159">-VM</span><span class="sxs-lookup"><span data-stu-id="a7dff-159">-VM</span></span>
<span data-ttu-id="a7dff-160">指定本機虛擬電腦物件。</span><span class="sxs-lookup"><span data-stu-id="a7dff-160">Specifies a local virtual machine object.</span></span>
<span data-ttu-id="a7dff-161">若要取得虛擬機器物件，請使用 Get-AzVM Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a7dff-161">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="a7dff-162">此虛擬機器物件包含虛擬機器的更新狀態。</span><span class="sxs-lookup"><span data-stu-id="a7dff-162">This virtual machine object contains the updated state for the virtual machine.</span></span>

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

### <span data-ttu-id="a7dff-163">-確認</span><span class="sxs-lookup"><span data-stu-id="a7dff-163">-Confirm</span></span>
<span data-ttu-id="a7dff-164">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a7dff-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7dff-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7dff-165">-WhatIf</span></span>
<span data-ttu-id="a7dff-166">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a7dff-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a7dff-167">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a7dff-167">The cmdlet is not run.</span></span>

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


### <span data-ttu-id="a7dff-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7dff-168">CommonParameters</span></span>
<span data-ttu-id="a7dff-169">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a7dff-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7dff-170">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a7dff-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7dff-171">輸入</span><span class="sxs-lookup"><span data-stu-id="a7dff-171">INPUTS</span></span>

### <span data-ttu-id="a7dff-172">System.object</span><span class="sxs-lookup"><span data-stu-id="a7dff-172">System.String</span></span>

### <span data-ttu-id="a7dff-173">PSVirtualMachine 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="a7dff-173">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="a7dff-174">System.object</span><span class="sxs-lookup"><span data-stu-id="a7dff-174">System.Boolean</span></span>

## <span data-ttu-id="a7dff-175">輸出</span><span class="sxs-lookup"><span data-stu-id="a7dff-175">OUTPUTS</span></span>

### <span data-ttu-id="a7dff-176">PSAzureOperationResponse 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="a7dff-176">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="a7dff-177">筆記</span><span class="sxs-lookup"><span data-stu-id="a7dff-177">NOTES</span></span>

## <span data-ttu-id="a7dff-178">相關連結</span><span class="sxs-lookup"><span data-stu-id="a7dff-178">RELATED LINKS</span></span>

[<span data-ttu-id="a7dff-179">AzVM</span><span class="sxs-lookup"><span data-stu-id="a7dff-179">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="a7dff-180">新-AzVM</span><span class="sxs-lookup"><span data-stu-id="a7dff-180">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="a7dff-181">移除-AzVM</span><span class="sxs-lookup"><span data-stu-id="a7dff-181">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="a7dff-182">重新開機-AzVM</span><span class="sxs-lookup"><span data-stu-id="a7dff-182">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="a7dff-183">開始-AzVM</span><span class="sxs-lookup"><span data-stu-id="a7dff-183">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="a7dff-184">停止 AzVM</span><span class="sxs-lookup"><span data-stu-id="a7dff-184">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="a7dff-185">新-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="a7dff-185">New-AzVMConfig</span></span>](./New-AzVMConfig.md)


