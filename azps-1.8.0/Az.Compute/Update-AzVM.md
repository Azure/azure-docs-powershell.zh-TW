---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 38917534-49C6-47EA-B815-240F794EE655
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVM.md
ms.openlocfilehash: e87536a524766ac86b80d790ee1372336fedba17
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93788249"
---
# <span data-ttu-id="6e3bd-101">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="6e3bd-101">Update-AzVM</span></span>

## <span data-ttu-id="6e3bd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6e3bd-102">SYNOPSIS</span></span>
<span data-ttu-id="6e3bd-103">更新 Azure 虛擬機器的狀態。</span><span class="sxs-lookup"><span data-stu-id="6e3bd-103">Updates the state of an Azure virtual machine.</span></span>

## <span data-ttu-id="6e3bd-104">句法</span><span class="sxs-lookup"><span data-stu-id="6e3bd-104">SYNTAX</span></span>

### <span data-ttu-id="6e3bd-105">ResourceGroupNameParameterSetName (預設) </span><span class="sxs-lookup"><span data-stu-id="6e3bd-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Update-AzVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>]
 [-OsDiskWriteAccelerator <Boolean>] [-UltraSSDEnabled <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e3bd-106">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="6e3bd-106">AssignIdentityParameterSet</span></span>
```
Update-AzVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>] [-AssignIdentity]
 [-OsDiskWriteAccelerator <Boolean>] [-UltraSSDEnabled <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e3bd-107">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="6e3bd-107">ExplicitIdentityParameterSet</span></span>
```
Update-AzVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>]
 -IdentityType <ResourceIdentityType> [-IdentityId <String[]>] [-OsDiskWriteAccelerator <Boolean>]
 [-UltraSSDEnabled <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6e3bd-108">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="6e3bd-108">IdParameterSetName</span></span>
```
Update-AzVM [-Id] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>] [-OsDiskWriteAccelerator <Boolean>]
 [-UltraSSDEnabled <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6e3bd-109">說明</span><span class="sxs-lookup"><span data-stu-id="6e3bd-109">DESCRIPTION</span></span>
<span data-ttu-id="6e3bd-110">**AzVM** Cmdlet 會將 Azure 虛擬機器的狀態更新為虛擬機器物件的狀態。</span><span class="sxs-lookup"><span data-stu-id="6e3bd-110">The **Update-AzVM** cmdlet updates the state of an Azure virtual machine to the state of a virtual machine object.</span></span>

## <span data-ttu-id="6e3bd-111">示例</span><span class="sxs-lookup"><span data-stu-id="6e3bd-111">EXAMPLES</span></span>

### <span data-ttu-id="6e3bd-112">範例1：更新虛擬機器</span><span class="sxs-lookup"><span data-stu-id="6e3bd-112">Example 1: Update a virtual machine</span></span>
```
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="6e3bd-113">這個命令會在 ResourceGroup11 中更新虛擬機器，$VirtualMachine。</span><span class="sxs-lookup"><span data-stu-id="6e3bd-113">This command updates the virtual machine, $VirtualMachine, in ResourceGroup11.</span></span>
<span data-ttu-id="6e3bd-114">此命令會使用儲存在 $VirtualMachine 變數中的虛擬機器物件來更新它。</span><span class="sxs-lookup"><span data-stu-id="6e3bd-114">The command updates it by using the virtual machine object stored in the $VirtualMachine variable.</span></span>
<span data-ttu-id="6e3bd-115">若要取得虛擬機器物件，請使用 **AzVM** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6e3bd-115">To obtain a virtual machine object, use the **Get-AzVM** cmdlet.</span></span>

## <span data-ttu-id="6e3bd-116">參數</span><span class="sxs-lookup"><span data-stu-id="6e3bd-116">PARAMETERS</span></span>

### <span data-ttu-id="6e3bd-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6e3bd-117">-AsJob</span></span>
<span data-ttu-id="6e3bd-118">在背景中執行 Cmdlet，然後返回作業來追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="6e3bd-118">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="6e3bd-119">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="6e3bd-119">-AssignIdentity</span></span>
<span data-ttu-id="6e3bd-120">指定虛擬機器的系統指派身分識別。</span><span class="sxs-lookup"><span data-stu-id="6e3bd-120">Specify the system-assigned identity for the virtual machine.</span></span>

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

### <span data-ttu-id="6e3bd-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e3bd-121">-DefaultProfile</span></span>
<span data-ttu-id="6e3bd-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6e3bd-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e3bd-123">-識別碼</span><span class="sxs-lookup"><span data-stu-id="6e3bd-123">-Id</span></span>
<span data-ttu-id="6e3bd-124">指定虛擬機器的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="6e3bd-124">Specifies the resource ID of the virtual machine.</span></span>

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

### <span data-ttu-id="6e3bd-125">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="6e3bd-125">-IdentityId</span></span>
<span data-ttu-id="6e3bd-126">指定與虛擬機器相關聯的使用者識別碼清單。</span><span class="sxs-lookup"><span data-stu-id="6e3bd-126">Specifies the list of user identities associated with the virtual machine.</span></span>
<span data-ttu-id="6e3bd-127">使用者身分識別參照將是下列形式的 ARM 資源識別碼： '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName} '</span><span class="sxs-lookup"><span data-stu-id="6e3bd-127">The user identity references will be ARM resource IDs in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="6e3bd-128">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="6e3bd-128">-IdentityType</span></span>
<span data-ttu-id="6e3bd-129">虛擬機器所用的身分識別類型。</span><span class="sxs-lookup"><span data-stu-id="6e3bd-129">The type of identity used for the virtual machine.</span></span> <span data-ttu-id="6e3bd-130">有效值為 SystemAssigned、UserAssigned、SystemAssignedUserAssigned 和 None。</span><span class="sxs-lookup"><span data-stu-id="6e3bd-130">Valid values are SystemAssigned, UserAssigned, SystemAssignedUserAssigned, and None.</span></span>

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

### <span data-ttu-id="6e3bd-131">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="6e3bd-131">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="6e3bd-132">指定是否應該在 OS 磁片上啟用或停用 WriteAccelerator。</span><span class="sxs-lookup"><span data-stu-id="6e3bd-132">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="6e3bd-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e3bd-133">-ResourceGroupName</span></span>
<span data-ttu-id="6e3bd-134">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6e3bd-134">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="6e3bd-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="6e3bd-135">-Tag</span></span>
<span data-ttu-id="6e3bd-136">指定可使用一組名稱值對來標記資源和資源群組。</span><span class="sxs-lookup"><span data-stu-id="6e3bd-136">Specifies the resources and resource groups can be tagged with a set of name-value pairs.</span></span>
<span data-ttu-id="6e3bd-137">新增標籤至資源之後，您就可以將資源群組集中在不同的資源群組中，以及建立您自己的視圖。</span><span class="sxs-lookup"><span data-stu-id="6e3bd-137">Adding tags to resources enables you to group resources together across resource groups and to create your own views.</span></span>
<span data-ttu-id="6e3bd-138">每個資源或資源群組最多可以有15個標籤。</span><span class="sxs-lookup"><span data-stu-id="6e3bd-138">Each resource or resource group can have a maximum of 15 tags.</span></span>

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

### <span data-ttu-id="6e3bd-139">-UltraSSDEnabled</span><span class="sxs-lookup"><span data-stu-id="6e3bd-139">-UltraSSDEnabled</span></span>
<span data-ttu-id="6e3bd-140">啟用或停用在 VM 上擁有 UltraSSD_LRS 儲存帳戶類型之一或多個受管理資料磁片之功能的標誌。</span><span class="sxs-lookup"><span data-stu-id="6e3bd-140">The flag that enables or disables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the VM.</span></span>
<span data-ttu-id="6e3bd-141">只有在啟用此屬性時，才能將儲存帳戶類型 UltraSSD_LRS 的受管理磁片新增至虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="6e3bd-141">Managed disks with storage account type UltraSSD_LRS can be added to a virtual machine only if this property is enabled.</span></span>

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

### <span data-ttu-id="6e3bd-142">-VM</span><span class="sxs-lookup"><span data-stu-id="6e3bd-142">-VM</span></span>
<span data-ttu-id="6e3bd-143">指定本機虛擬電腦物件。</span><span class="sxs-lookup"><span data-stu-id="6e3bd-143">Specifies a local virtual machine object.</span></span>
<span data-ttu-id="6e3bd-144">若要取得虛擬機器物件，請使用 Get-AzVM Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6e3bd-144">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="6e3bd-145">此虛擬機器物件包含虛擬機器的更新狀態。</span><span class="sxs-lookup"><span data-stu-id="6e3bd-145">This virtual machine object contains the updated state for the virtual machine.</span></span>

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

### <span data-ttu-id="6e3bd-146">-確認</span><span class="sxs-lookup"><span data-stu-id="6e3bd-146">-Confirm</span></span>
<span data-ttu-id="6e3bd-147">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6e3bd-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6e3bd-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e3bd-148">-WhatIf</span></span>
<span data-ttu-id="6e3bd-149">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6e3bd-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6e3bd-150">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6e3bd-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6e3bd-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e3bd-151">CommonParameters</span></span>
<span data-ttu-id="6e3bd-152">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6e3bd-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e3bd-153">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6e3bd-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e3bd-154">輸入</span><span class="sxs-lookup"><span data-stu-id="6e3bd-154">INPUTS</span></span>

### <span data-ttu-id="6e3bd-155">System.object</span><span class="sxs-lookup"><span data-stu-id="6e3bd-155">System.String</span></span>

### <span data-ttu-id="6e3bd-156">PSVirtualMachine 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="6e3bd-156">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="6e3bd-157">System.object</span><span class="sxs-lookup"><span data-stu-id="6e3bd-157">System.Boolean</span></span>

## <span data-ttu-id="6e3bd-158">輸出</span><span class="sxs-lookup"><span data-stu-id="6e3bd-158">OUTPUTS</span></span>

### <span data-ttu-id="6e3bd-159">PSAzureOperationResponse 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="6e3bd-159">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="6e3bd-160">筆記</span><span class="sxs-lookup"><span data-stu-id="6e3bd-160">NOTES</span></span>

## <span data-ttu-id="6e3bd-161">相關連結</span><span class="sxs-lookup"><span data-stu-id="6e3bd-161">RELATED LINKS</span></span>

[<span data-ttu-id="6e3bd-162">AzVM</span><span class="sxs-lookup"><span data-stu-id="6e3bd-162">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="6e3bd-163">新-AzVM</span><span class="sxs-lookup"><span data-stu-id="6e3bd-163">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="6e3bd-164">移除-AzVM</span><span class="sxs-lookup"><span data-stu-id="6e3bd-164">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="6e3bd-165">重新開機-AzVM</span><span class="sxs-lookup"><span data-stu-id="6e3bd-165">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="6e3bd-166">開始-AzVM</span><span class="sxs-lookup"><span data-stu-id="6e3bd-166">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="6e3bd-167">停止 AzVM</span><span class="sxs-lookup"><span data-stu-id="6e3bd-167">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="6e3bd-168">新-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="6e3bd-168">New-AzVMConfig</span></span>](./New-AzVMConfig.md)


