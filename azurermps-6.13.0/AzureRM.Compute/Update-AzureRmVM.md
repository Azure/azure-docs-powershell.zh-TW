---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 38917534-49C6-47EA-B815-240F794EE655
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/update-azurermvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmVM.md
ms.openlocfilehash: e29eb849dfd7ec3417daaea1b0cae447d20f1322
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451307"
---
# <span data-ttu-id="a4f84-101">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="a4f84-101">Update-AzureRmVM</span></span>

## <span data-ttu-id="a4f84-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a4f84-102">SYNOPSIS</span></span>
<span data-ttu-id="a4f84-103">更新 Azure 虛擬機器的狀態。</span><span class="sxs-lookup"><span data-stu-id="a4f84-103">Updates the state of an Azure virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a4f84-104">句法</span><span class="sxs-lookup"><span data-stu-id="a4f84-104">SYNTAX</span></span>

### <span data-ttu-id="a4f84-105">ResourceGroupNameParameterSetName (預設) </span><span class="sxs-lookup"><span data-stu-id="a4f84-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Update-AzureRmVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>]
 [-OsDiskWriteAccelerator <Boolean>] [-UltraSSDEnabled <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4f84-106">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="a4f84-106">AssignIdentityParameterSet</span></span>
```
Update-AzureRmVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>] [-AssignIdentity]
 [-OsDiskWriteAccelerator <Boolean>] [-UltraSSDEnabled <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4f84-107">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="a4f84-107">ExplicitIdentityParameterSet</span></span>
```
Update-AzureRmVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>]
 -IdentityType <ResourceIdentityType> [-IdentityId <String[]>] [-OsDiskWriteAccelerator <Boolean>]
 [-UltraSSDEnabled <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a4f84-108">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="a4f84-108">IdParameterSetName</span></span>
```
Update-AzureRmVM [-Id] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>] [-OsDiskWriteAccelerator <Boolean>]
 [-UltraSSDEnabled <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a4f84-109">說明</span><span class="sxs-lookup"><span data-stu-id="a4f84-109">DESCRIPTION</span></span>
<span data-ttu-id="a4f84-110">**AzureRmVM** Cmdlet 會將 Azure 虛擬機器的狀態更新為虛擬機器物件的狀態。</span><span class="sxs-lookup"><span data-stu-id="a4f84-110">The **Update-AzureRmVM** cmdlet updates the state of an Azure virtual machine to the state of a virtual machine object.</span></span>

## <span data-ttu-id="a4f84-111">示例</span><span class="sxs-lookup"><span data-stu-id="a4f84-111">EXAMPLES</span></span>

### <span data-ttu-id="a4f84-112">範例1：更新虛擬機器</span><span class="sxs-lookup"><span data-stu-id="a4f84-112">Example 1: Update a virtual machine</span></span>
```
PS C:\> Update-AzureRmVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="a4f84-113">這個命令會在 ResourceGroup11 中更新虛擬機器，$VirtualMachine。</span><span class="sxs-lookup"><span data-stu-id="a4f84-113">This command updates the virtual machine, $VirtualMachine, in ResourceGroup11.</span></span>
<span data-ttu-id="a4f84-114">此命令會使用儲存在 $VirtualMachine 變數中的虛擬機器物件來更新它。</span><span class="sxs-lookup"><span data-stu-id="a4f84-114">The command updates it by using the virtual machine object stored in the $VirtualMachine variable.</span></span>
<span data-ttu-id="a4f84-115">若要取得虛擬機器物件，請使用 **AzureRmVM** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a4f84-115">To obtain a virtual machine object, use the **Get-AzureRmVM** cmdlet.</span></span>

## <span data-ttu-id="a4f84-116">參數</span><span class="sxs-lookup"><span data-stu-id="a4f84-116">PARAMETERS</span></span>

### <span data-ttu-id="a4f84-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a4f84-117">-AsJob</span></span>
<span data-ttu-id="a4f84-118">在背景中執行 Cmdlet，然後返回作業來追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="a4f84-118">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="a4f84-119">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="a4f84-119">-AssignIdentity</span></span>
<span data-ttu-id="a4f84-120">指定系統指派給虛擬機器的身分識別。</span><span class="sxs-lookup"><span data-stu-id="a4f84-120">Specify the system assigned identity for the virtual machine.</span></span>

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

### <span data-ttu-id="a4f84-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4f84-121">-DefaultProfile</span></span>
<span data-ttu-id="a4f84-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a4f84-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a4f84-123">-識別碼</span><span class="sxs-lookup"><span data-stu-id="a4f84-123">-Id</span></span>
<span data-ttu-id="a4f84-124">指定虛擬機器的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="a4f84-124">Specifies the Resource ID of the virtual machine.</span></span>

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

### <span data-ttu-id="a4f84-125">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="a4f84-125">-IdentityId</span></span>
<span data-ttu-id="a4f84-126">指定與虛擬機器小性集相關聯的使用者識別碼清單。</span><span class="sxs-lookup"><span data-stu-id="a4f84-126">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="a4f84-127">使用者身分識別參照將是下列形式的 ARM 資源識別碼： '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName} '</span><span class="sxs-lookup"><span data-stu-id="a4f84-127">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="a4f84-128">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="a4f84-128">-IdentityType</span></span>
<span data-ttu-id="a4f84-129">虛擬機器所用的身分識別類型。</span><span class="sxs-lookup"><span data-stu-id="a4f84-129">The type of identity used for the virtual machine.</span></span> <span data-ttu-id="a4f84-130">目前唯一支援的類型是「SystemAssigned」，它會以隱含方式建立身分識別。</span><span class="sxs-lookup"><span data-stu-id="a4f84-130">Currently, the only supported type is 'SystemAssigned', which implicitly creates an identity.</span></span>

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

### <span data-ttu-id="a4f84-131">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="a4f84-131">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="a4f84-132">指定是否應該在 OS 磁片上啟用或停用 WriteAccelerator。</span><span class="sxs-lookup"><span data-stu-id="a4f84-132">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="a4f84-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4f84-133">-ResourceGroupName</span></span>
<span data-ttu-id="a4f84-134">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a4f84-134">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="a4f84-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="a4f84-135">-Tag</span></span>
<span data-ttu-id="a4f84-136">指定可使用一組名稱值對來標記資源和資源群組。</span><span class="sxs-lookup"><span data-stu-id="a4f84-136">Specifies the resources and resource groups can be tagged with a set of name-value pairs.</span></span>
<span data-ttu-id="a4f84-137">新增標籤至資源之後，您就可以將資源群組集中在不同的資源群組中，以及建立您自己的視圖。</span><span class="sxs-lookup"><span data-stu-id="a4f84-137">Adding tags to resources enables you to group resources together across resource groups and to create your own views.</span></span>
<span data-ttu-id="a4f84-138">每個資源或資源群組最多可以有15個標籤。</span><span class="sxs-lookup"><span data-stu-id="a4f84-138">Each resource or resource group can have a maximum of 15 tags.</span></span>

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

### <span data-ttu-id="a4f84-139">-UltraSSDEnabled</span><span class="sxs-lookup"><span data-stu-id="a4f84-139">-UltraSSDEnabled</span></span>
<span data-ttu-id="a4f84-140">啟用或停用在 VM 上擁有 UltraSSD_LRS 儲存帳戶類型之一或多個受管理資料磁片之功能的標誌。</span><span class="sxs-lookup"><span data-stu-id="a4f84-140">The flag that enables or disables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the VM.</span></span>
<span data-ttu-id="a4f84-141">只有在啟用此屬性時，才能將儲存帳戶類型 UltraSSD_LRS 的受管理磁片新增至虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="a4f84-141">Managed disks with storage account type UltraSSD_LRS can be added to a virtual machine only if this property is enabled.</span></span>

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

### <span data-ttu-id="a4f84-142">-VM</span><span class="sxs-lookup"><span data-stu-id="a4f84-142">-VM</span></span>
<span data-ttu-id="a4f84-143">指定本機虛擬電腦物件。</span><span class="sxs-lookup"><span data-stu-id="a4f84-143">Specifies a local virtual machine object.</span></span>
<span data-ttu-id="a4f84-144">若要取得虛擬機器物件，請使用 Get-AzureRmVM Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a4f84-144">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>
<span data-ttu-id="a4f84-145">此虛擬機器物件包含虛擬機器的更新狀態。</span><span class="sxs-lookup"><span data-stu-id="a4f84-145">This virtual machine object contains the updated state for the virtual machine.</span></span>

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

### <span data-ttu-id="a4f84-146">-確認</span><span class="sxs-lookup"><span data-stu-id="a4f84-146">-Confirm</span></span>
<span data-ttu-id="a4f84-147">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a4f84-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4f84-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4f84-148">-WhatIf</span></span>
<span data-ttu-id="a4f84-149">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a4f84-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4f84-150">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a4f84-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4f84-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4f84-151">CommonParameters</span></span>
<span data-ttu-id="a4f84-152">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a4f84-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4f84-153">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a4f84-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4f84-154">輸入</span><span class="sxs-lookup"><span data-stu-id="a4f84-154">INPUTS</span></span>

### <span data-ttu-id="a4f84-155">System.object</span><span class="sxs-lookup"><span data-stu-id="a4f84-155">System.String</span></span>

### <span data-ttu-id="a4f84-156">PSVirtualMachine 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="a4f84-156">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="a4f84-157">輸出</span><span class="sxs-lookup"><span data-stu-id="a4f84-157">OUTPUTS</span></span>

### <span data-ttu-id="a4f84-158">PSAzureOperationResponse 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="a4f84-158">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="a4f84-159">筆記</span><span class="sxs-lookup"><span data-stu-id="a4f84-159">NOTES</span></span>

## <span data-ttu-id="a4f84-160">相關連結</span><span class="sxs-lookup"><span data-stu-id="a4f84-160">RELATED LINKS</span></span>

[<span data-ttu-id="a4f84-161">AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="a4f84-161">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="a4f84-162">新-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="a4f84-162">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="a4f84-163">移除-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="a4f84-163">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="a4f84-164">重新開機-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="a4f84-164">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="a4f84-165">開始-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="a4f84-165">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="a4f84-166">停止 AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="a4f84-166">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="a4f84-167">新-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="a4f84-167">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)


