---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 38917534-49C6-47EA-B815-240F794EE655
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Update-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Update-AzVM.md
ms.openlocfilehash: 8dd18c97a1636e4b6422d58fa7aca28d8798001b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794818"
---
# <span data-ttu-id="29ab0-101">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="29ab0-101">Update-AzVM</span></span>

## <span data-ttu-id="29ab0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="29ab0-102">SYNOPSIS</span></span>
<span data-ttu-id="29ab0-103">更新 Azure 虛擬機器的狀態。</span><span class="sxs-lookup"><span data-stu-id="29ab0-103">Updates the state of an Azure virtual machine.</span></span>

## <span data-ttu-id="29ab0-104">句法</span><span class="sxs-lookup"><span data-stu-id="29ab0-104">SYNTAX</span></span>

### <span data-ttu-id="29ab0-105">ResourceGroupNameParameterSetName (預設) </span><span class="sxs-lookup"><span data-stu-id="29ab0-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Update-AzVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>]
 [-OsDiskWriteAccelerator <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="29ab0-106">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="29ab0-106">AssignIdentityParameterSet</span></span>
```
Update-AzVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>] [-AssignIdentity]
 [-OsDiskWriteAccelerator <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="29ab0-107">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="29ab0-107">ExplicitIdentityParameterSet</span></span>
```
Update-AzVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>]
 -IdentityType <ResourceIdentityType> [-IdentityId <String[]>] [-OsDiskWriteAccelerator <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29ab0-108">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="29ab0-108">IdParameterSetName</span></span>
```
Update-AzVM [-Id] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>] [-OsDiskWriteAccelerator <Boolean>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29ab0-109">說明</span><span class="sxs-lookup"><span data-stu-id="29ab0-109">DESCRIPTION</span></span>
<span data-ttu-id="29ab0-110">**AzVM** Cmdlet 會將 Azure 虛擬機器的狀態更新為虛擬機器物件的狀態。</span><span class="sxs-lookup"><span data-stu-id="29ab0-110">The **Update-AzVM** cmdlet updates the state of an Azure virtual machine to the state of a virtual machine object.</span></span>

## <span data-ttu-id="29ab0-111">示例</span><span class="sxs-lookup"><span data-stu-id="29ab0-111">EXAMPLES</span></span>

### <span data-ttu-id="29ab0-112">範例1：更新虛擬機器</span><span class="sxs-lookup"><span data-stu-id="29ab0-112">Example 1: Update a virtual machine</span></span>
```
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="29ab0-113">這個命令會在 ResourceGroup11 中更新虛擬機器，$VirtualMachine。</span><span class="sxs-lookup"><span data-stu-id="29ab0-113">This command updates the virtual machine, $VirtualMachine, in ResourceGroup11.</span></span>
<span data-ttu-id="29ab0-114">此命令會使用儲存在 $VirtualMachine 變數中的虛擬機器物件來更新它。</span><span class="sxs-lookup"><span data-stu-id="29ab0-114">The command updates it by using the virtual machine object stored in the $VirtualMachine variable.</span></span>
<span data-ttu-id="29ab0-115">若要取得虛擬機器物件，請使用 **AzVM** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="29ab0-115">To obtain a virtual machine object, use the **Get-AzVM** cmdlet.</span></span>

## <span data-ttu-id="29ab0-116">參數</span><span class="sxs-lookup"><span data-stu-id="29ab0-116">PARAMETERS</span></span>

### <span data-ttu-id="29ab0-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="29ab0-117">-AsJob</span></span>
<span data-ttu-id="29ab0-118">在背景中執行 Cmdlet，然後返回作業來追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="29ab0-118">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="29ab0-119">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="29ab0-119">-AssignIdentity</span></span>
<span data-ttu-id="29ab0-120">指定系統指派給虛擬機器的身分識別。</span><span class="sxs-lookup"><span data-stu-id="29ab0-120">Specify the system assigned identity for the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AssignIdentityParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29ab0-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29ab0-121">-DefaultProfile</span></span>
<span data-ttu-id="29ab0-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="29ab0-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="29ab0-123">-識別碼</span><span class="sxs-lookup"><span data-stu-id="29ab0-123">-Id</span></span>
<span data-ttu-id="29ab0-124">指定虛擬機器的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="29ab0-124">Specifies the Resource ID of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: IdParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29ab0-125">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="29ab0-125">-IdentityId</span></span>
<span data-ttu-id="29ab0-126">指定與虛擬機器小性集相關聯的使用者識別碼清單。</span><span class="sxs-lookup"><span data-stu-id="29ab0-126">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="29ab0-127">使用者身分識別參照將是下列形式的 ARM 資源識別碼： '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName} '</span><span class="sxs-lookup"><span data-stu-id="29ab0-127">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

```yaml
Type: String[]
Parameter Sets: ExplicitIdentityParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29ab0-128">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="29ab0-128">-IdentityType</span></span>
<span data-ttu-id="29ab0-129">虛擬機器所用的身分識別類型。</span><span class="sxs-lookup"><span data-stu-id="29ab0-129">The type of identity used for the virtual machine.</span></span> <span data-ttu-id="29ab0-130">目前唯一支援的類型是「SystemAssigned」，它會以隱含方式建立身分識別。</span><span class="sxs-lookup"><span data-stu-id="29ab0-130">Currently, the only supported type is 'SystemAssigned', which implicitly creates an identity.</span></span>

```yaml
Type: ResourceIdentityType
Parameter Sets: ExplicitIdentityParameterSet
Aliases: 
Accepted values: SystemAssigned, UserAssigned, SystemAssignedUserAssigned, None

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29ab0-131">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="29ab0-131">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="29ab0-132">指定是否應該在 OS 磁片上啟用或停用 WriteAccelerator。</span><span class="sxs-lookup"><span data-stu-id="29ab0-132">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29ab0-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29ab0-133">-ResourceGroupName</span></span>
<span data-ttu-id="29ab0-134">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="29ab0-134">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupNameParameterSetName, AssignIdentityParameterSet, ExplicitIdentityParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29ab0-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="29ab0-135">-Tag</span></span>
<span data-ttu-id="29ab0-136">指定可使用一組名稱值對來標記資源和資源群組。</span><span class="sxs-lookup"><span data-stu-id="29ab0-136">Specifies the resources and resource groups can be tagged with a set of name-value pairs.</span></span>
<span data-ttu-id="29ab0-137">新增標籤至資源之後，您就可以將資源群組集中在不同的資源群組中，以及建立您自己的視圖。</span><span class="sxs-lookup"><span data-stu-id="29ab0-137">Adding tags to resources enables you to group resources together across resource groups and to create your own views.</span></span>
<span data-ttu-id="29ab0-138">每個資源或資源群組最多可以有15個標籤。</span><span class="sxs-lookup"><span data-stu-id="29ab0-138">Each resource or resource group can have a maximum of 15 tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29ab0-139">-VM</span><span class="sxs-lookup"><span data-stu-id="29ab0-139">-VM</span></span>
<span data-ttu-id="29ab0-140">指定本機虛擬電腦物件。</span><span class="sxs-lookup"><span data-stu-id="29ab0-140">Specifies a local virtual machine object.</span></span>
<span data-ttu-id="29ab0-141">若要取得虛擬機器物件，請使用 Get-AzVM Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="29ab0-141">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="29ab0-142">此虛擬機器物件包含虛擬機器的更新狀態。</span><span class="sxs-lookup"><span data-stu-id="29ab0-142">This virtual machine object contains the updated state for the virtual machine.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="29ab0-143">-確認</span><span class="sxs-lookup"><span data-stu-id="29ab0-143">-Confirm</span></span>
<span data-ttu-id="29ab0-144">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="29ab0-144">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29ab0-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29ab0-145">-WhatIf</span></span>
<span data-ttu-id="29ab0-146">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="29ab0-146">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="29ab0-147">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="29ab0-147">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29ab0-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29ab0-148">CommonParameters</span></span>
<span data-ttu-id="29ab0-149">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="29ab0-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29ab0-150">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="29ab0-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29ab0-151">輸入</span><span class="sxs-lookup"><span data-stu-id="29ab0-151">INPUTS</span></span>

### <span data-ttu-id="29ab0-152">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="29ab0-152">PSVirtualMachine</span></span>
<span data-ttu-id="29ab0-153">[VM "參數從管線接受類型 ' PSVirtualMachine」的值</span><span class="sxs-lookup"><span data-stu-id="29ab0-153">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="29ab0-154">輸出</span><span class="sxs-lookup"><span data-stu-id="29ab0-154">OUTPUTS</span></span>

### <span data-ttu-id="29ab0-155">PSAzureOperationResponse 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="29ab0-155">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="29ab0-156">筆記</span><span class="sxs-lookup"><span data-stu-id="29ab0-156">NOTES</span></span>

## <span data-ttu-id="29ab0-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="29ab0-157">RELATED LINKS</span></span>

[<span data-ttu-id="29ab0-158">AzVM</span><span class="sxs-lookup"><span data-stu-id="29ab0-158">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="29ab0-159">新-AzVM</span><span class="sxs-lookup"><span data-stu-id="29ab0-159">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="29ab0-160">移除-AzVM</span><span class="sxs-lookup"><span data-stu-id="29ab0-160">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="29ab0-161">重新開機-AzVM</span><span class="sxs-lookup"><span data-stu-id="29ab0-161">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="29ab0-162">開始-AzVM</span><span class="sxs-lookup"><span data-stu-id="29ab0-162">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="29ab0-163">停止 AzVM</span><span class="sxs-lookup"><span data-stu-id="29ab0-163">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="29ab0-164">新-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="29ab0-164">New-AzVMConfig</span></span>](./New-AzVMConfig.md)


