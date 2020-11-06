---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 38917534-49C6-47EA-B815-240F794EE655
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmVM.md
ms.openlocfilehash: ad337c07f22b2805002347758f91bf0ea781adad
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450828"
---
# <span data-ttu-id="9c69b-101">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="9c69b-101">Update-AzureRmVM</span></span>

## <span data-ttu-id="9c69b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9c69b-102">SYNOPSIS</span></span>
<span data-ttu-id="9c69b-103">更新 Azure 虛擬機器的狀態。</span><span class="sxs-lookup"><span data-stu-id="9c69b-103">Updates the state of an Azure virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9c69b-104">句法</span><span class="sxs-lookup"><span data-stu-id="9c69b-104">SYNTAX</span></span>

### <span data-ttu-id="9c69b-105">ResourceGroupNameParameterSetName (預設) </span><span class="sxs-lookup"><span data-stu-id="9c69b-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Update-AzureRmVM -VM <PSVirtualMachine> [-Tags <Hashtable>] [-IdentityType <ResourceIdentityType>]
 [-AssignIdentity] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9c69b-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="9c69b-106">IdParameterSetName</span></span>
```
Update-AzureRmVM -VM <PSVirtualMachine> [-Tags <Hashtable>] [-IdentityType <ResourceIdentityType>]
 [-AssignIdentity] [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9c69b-107">說明</span><span class="sxs-lookup"><span data-stu-id="9c69b-107">DESCRIPTION</span></span>
<span data-ttu-id="9c69b-108">**AzureRmVM** Cmdlet 會將 Azure 虛擬機器的狀態更新為虛擬機器物件的狀態。</span><span class="sxs-lookup"><span data-stu-id="9c69b-108">The **Update-AzureRmVM** cmdlet updates the state of an Azure virtual machine to the state of a virtual machine object.</span></span>

## <span data-ttu-id="9c69b-109">示例</span><span class="sxs-lookup"><span data-stu-id="9c69b-109">EXAMPLES</span></span>

### <span data-ttu-id="9c69b-110">範例1：更新虛擬機器</span><span class="sxs-lookup"><span data-stu-id="9c69b-110">Example 1: Update a virtual machine</span></span>
```
PS C:\> Update-AzureRmVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="9c69b-111">這個命令會在 ResourceGroup11 中更新虛擬機器，$VirtualMachine。</span><span class="sxs-lookup"><span data-stu-id="9c69b-111">This command updates the virtual machine, $VirtualMachine, in ResourceGroup11.</span></span>
<span data-ttu-id="9c69b-112">此命令會使用儲存在 $VirtualMachine 變數中的虛擬機器物件來更新它。</span><span class="sxs-lookup"><span data-stu-id="9c69b-112">The command updates it by using the virtual machine object stored in the $VirtualMachine variable.</span></span>
<span data-ttu-id="9c69b-113">若要取得虛擬機器物件，請使用 **AzureRmVM** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9c69b-113">To obtain a virtual machine object, use the **Get-AzureRmVM** cmdlet.</span></span>

## <span data-ttu-id="9c69b-114">參數</span><span class="sxs-lookup"><span data-stu-id="9c69b-114">PARAMETERS</span></span>

### <span data-ttu-id="9c69b-115">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="9c69b-115">-AssignIdentity</span></span>
<span data-ttu-id="9c69b-116">指定系統指派給虛擬機器的身分識別。</span><span class="sxs-lookup"><span data-stu-id="9c69b-116">Specify the system assigned identity for the virtual machine.</span></span>

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

### <span data-ttu-id="9c69b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c69b-117">-DefaultProfile</span></span>
<span data-ttu-id="9c69b-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9c69b-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9c69b-119">-識別碼</span><span class="sxs-lookup"><span data-stu-id="9c69b-119">-Id</span></span>
<span data-ttu-id="9c69b-120">指定虛擬機器的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="9c69b-120">Specifies the Resource ID of the virtual machine.</span></span>

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

### <span data-ttu-id="9c69b-121">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="9c69b-121">-IdentityType</span></span>
<span data-ttu-id="9c69b-122">虛擬機器所用的身分識別類型。</span><span class="sxs-lookup"><span data-stu-id="9c69b-122">The type of identity used for the virtual machine.</span></span> <span data-ttu-id="9c69b-123">目前唯一支援的類型是「SystemAssigned」，它會以隱含方式建立身分識別。</span><span class="sxs-lookup"><span data-stu-id="9c69b-123">Currently, the only supported type is 'SystemAssigned', which implicitly creates an identity.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType]
Parameter Sets: (All)
Aliases: 
Accepted values: SystemAssigned

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c69b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c69b-124">-ResourceGroupName</span></span>
<span data-ttu-id="9c69b-125">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9c69b-125">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c69b-126">-標記</span><span class="sxs-lookup"><span data-stu-id="9c69b-126">-Tags</span></span>
<span data-ttu-id="9c69b-127">指定可使用一組名稱值對來標記資源和資源群組。</span><span class="sxs-lookup"><span data-stu-id="9c69b-127">Specifies the resources and resource groups can be tagged with a set of name-value pairs.</span></span>
<span data-ttu-id="9c69b-128">新增標籤至資源之後，您就可以將資源群組集中在不同的資源群組中，以及建立您自己的視圖。</span><span class="sxs-lookup"><span data-stu-id="9c69b-128">Adding tags to resources enables you to group resources together across resource groups and to create your own views.</span></span>
<span data-ttu-id="9c69b-129">每個資源或資源群組最多可以有15個標籤。</span><span class="sxs-lookup"><span data-stu-id="9c69b-129">Each resource or resource group can have a maximum of 15 tags.</span></span>

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

### <span data-ttu-id="9c69b-130">-VM</span><span class="sxs-lookup"><span data-stu-id="9c69b-130">-VM</span></span>
<span data-ttu-id="9c69b-131">指定本機虛擬電腦物件。</span><span class="sxs-lookup"><span data-stu-id="9c69b-131">Specifies a local virtual machine object.</span></span>
<span data-ttu-id="9c69b-132">若要取得虛擬機器物件，請使用 Get-AzureRmVM Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9c69b-132">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>
<span data-ttu-id="9c69b-133">此虛擬機器物件包含虛擬機器的更新狀態。</span><span class="sxs-lookup"><span data-stu-id="9c69b-133">This virtual machine object contains the updated state for the virtual machine.</span></span>

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

### <span data-ttu-id="9c69b-134">-確認</span><span class="sxs-lookup"><span data-stu-id="9c69b-134">-Confirm</span></span>
<span data-ttu-id="9c69b-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9c69b-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c69b-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c69b-136">-WhatIf</span></span>
<span data-ttu-id="9c69b-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9c69b-137">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="9c69b-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9c69b-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c69b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c69b-139">CommonParameters</span></span>
<span data-ttu-id="9c69b-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9c69b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c69b-141">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9c69b-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c69b-142">輸入</span><span class="sxs-lookup"><span data-stu-id="9c69b-142">INPUTS</span></span>

## <span data-ttu-id="9c69b-143">輸出</span><span class="sxs-lookup"><span data-stu-id="9c69b-143">OUTPUTS</span></span>

## <span data-ttu-id="9c69b-144">筆記</span><span class="sxs-lookup"><span data-stu-id="9c69b-144">NOTES</span></span>

## <span data-ttu-id="9c69b-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="9c69b-145">RELATED LINKS</span></span>

[<span data-ttu-id="9c69b-146">AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="9c69b-146">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="9c69b-147">新-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="9c69b-147">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="9c69b-148">移除-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="9c69b-148">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="9c69b-149">重新開機-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="9c69b-149">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="9c69b-150">開始-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="9c69b-150">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="9c69b-151">停止 AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="9c69b-151">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="9c69b-152">新-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="9c69b-152">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)


