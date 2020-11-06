---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 6250EC11-79CF-428B-A72F-9BD72C1751F0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVM.md
ms.openlocfilehash: 8601a7cc6a02211a0264030784485a5ecb4d29fc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447435"
---
# <span data-ttu-id="642cd-101">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="642cd-101">Get-AzureRmVM</span></span>

## <span data-ttu-id="642cd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="642cd-102">SYNOPSIS</span></span>
<span data-ttu-id="642cd-103">取得虛擬機器的屬性。</span><span class="sxs-lookup"><span data-stu-id="642cd-103">Gets the properties of a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="642cd-104">句法</span><span class="sxs-lookup"><span data-stu-id="642cd-104">SYNTAX</span></span>

### <span data-ttu-id="642cd-105">ListAllVirtualMachinesParamSet (預設) </span><span class="sxs-lookup"><span data-stu-id="642cd-105">ListAllVirtualMachinesParamSet (Default)</span></span>
```
Get-AzureRmVM [-Status] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="642cd-106">ListVirtualMachineInResourceGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="642cd-106">ListVirtualMachineInResourceGroupParamSet</span></span>
```
Get-AzureRmVM [-ResourceGroupName] <String> [-Status] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="642cd-107">GetVirtualMachineInResourceGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="642cd-107">GetVirtualMachineInResourceGroupParamSet</span></span>
```
Get-AzureRmVM [-ResourceGroupName] <String> [-Name] <String> [-Status] [-DisplayHint <DisplayHintType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="642cd-108">ListLocationVirtualMachinesParamSet</span><span class="sxs-lookup"><span data-stu-id="642cd-108">ListLocationVirtualMachinesParamSet</span></span>
```
Get-AzureRmVM -Location <String> [-Status] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="642cd-109">ListNextLinkVirtualMachinesParamSet</span><span class="sxs-lookup"><span data-stu-id="642cd-109">ListNextLinkVirtualMachinesParamSet</span></span>
```
Get-AzureRmVM [-Status] [-NextLink] <Uri> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="642cd-110">說明</span><span class="sxs-lookup"><span data-stu-id="642cd-110">DESCRIPTION</span></span>
<span data-ttu-id="642cd-111">**AzureRmVM** Cmdlet 會取得 Azure 虛擬機器的 [模型] 視圖和 [實例] 視圖。</span><span class="sxs-lookup"><span data-stu-id="642cd-111">The **Get-AzureRmVM** cmdlet gets the model view and instance view of an Azure virtual machine.</span></span>
<span data-ttu-id="642cd-112">模型視圖是使用者指定的虛擬機器屬性。</span><span class="sxs-lookup"><span data-stu-id="642cd-112">The model view is the user specified properties of the virtual machine.</span></span>
<span data-ttu-id="642cd-113">[實例] 視圖是虛擬機器的實例層級狀態。</span><span class="sxs-lookup"><span data-stu-id="642cd-113">The instance view is the instance level status of the virtual machine.</span></span>
<span data-ttu-id="642cd-114">指定 *Status* 參數，只取得虛擬機器的 [實例] 視圖。</span><span class="sxs-lookup"><span data-stu-id="642cd-114">Specify the *Status* parameter to get only the instance view of a virtual machine.</span></span>

## <span data-ttu-id="642cd-115">示例</span><span class="sxs-lookup"><span data-stu-id="642cd-115">EXAMPLES</span></span>

### <span data-ttu-id="642cd-116">範例1：取得模型和實例視圖屬性</span><span class="sxs-lookup"><span data-stu-id="642cd-116">Example 1: Get model and instance view properties</span></span>
```
PS C:\> Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="642cd-117">這個命令會取得名為 VirtualMachine07 的虛擬機器的模型視圖和實例視圖屬性。</span><span class="sxs-lookup"><span data-stu-id="642cd-117">This command gets the model view and instance view properties of the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="642cd-118">範例2：取得實例視圖屬性</span><span class="sxs-lookup"><span data-stu-id="642cd-118">Example 2: Get instance view properties</span></span>
```
PS C:\> Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Status
```

<span data-ttu-id="642cd-119">這個命令會取得名為 VirtualMachine07 的虛擬機器的屬性。</span><span class="sxs-lookup"><span data-stu-id="642cd-119">This command gets properties of the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="642cd-120">這個命令會指定 *Status* 參數。</span><span class="sxs-lookup"><span data-stu-id="642cd-120">This command specifies the *Status* parameter.</span></span>
<span data-ttu-id="642cd-121">因此，命令只會取得實例視圖屬性。</span><span class="sxs-lookup"><span data-stu-id="642cd-121">Therefore, the command gets only the instance view properties.</span></span>

### <span data-ttu-id="642cd-122">範例3：取得資源群組中所有虛擬機器的屬性</span><span class="sxs-lookup"><span data-stu-id="642cd-122">Example 3: Get properties for all virtual machines in a resource group</span></span>
```
PS C:\> Get-AzureRmVM -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="642cd-123">這個命令會取得名為 ResourceGroup11 之資源群組中所有虛擬機器的屬性。</span><span class="sxs-lookup"><span data-stu-id="642cd-123">This command gets properties for all the virtual machines in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="642cd-124">範例4：取得您訂閱中的所有虛擬機器</span><span class="sxs-lookup"><span data-stu-id="642cd-124">Example 4: Get all virtual machines in your subscription</span></span>
```
PS C:\> Get-AzureRmVM
```

<span data-ttu-id="642cd-125">這個命令會取得您訂閱中的所有虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="642cd-125">This command gets all the virtual machines in your subscription.</span></span>

### <span data-ttu-id="642cd-126">範例5：取得位置中的所有虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="642cd-126">Example 5: Get all virtual machines in the location.</span></span>
```
PS C:\> Get-AzureRmVM -Location "westus"
```

<span data-ttu-id="642cd-127">這個命令會取得西部美區域中的所有虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="642cd-127">This command gets all the virtual machines in West US region.</span></span>

## <span data-ttu-id="642cd-128">參數</span><span class="sxs-lookup"><span data-stu-id="642cd-128">PARAMETERS</span></span>

### <span data-ttu-id="642cd-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="642cd-129">-DefaultProfile</span></span>
<span data-ttu-id="642cd-130">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="642cd-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="642cd-131">-DisplayHint</span><span class="sxs-lookup"><span data-stu-id="642cd-131">-DisplayHint</span></span>
<span data-ttu-id="642cd-132">決定虛擬機器物件的顯示方式。</span><span class="sxs-lookup"><span data-stu-id="642cd-132">Determines how the virtual machine object is displayed.</span></span>
<span data-ttu-id="642cd-133">有效值為：-精簡：只顯示最上層屬性--展開：顯示所有層級中的所有屬性</span><span class="sxs-lookup"><span data-stu-id="642cd-133">Valid values are: -- Compact: displays only top level properties -- Expand: displays all properties in all levels</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.DisplayHintType
Parameter Sets: GetVirtualMachineInResourceGroupParamSet
Aliases:
Accepted values: Compact, Expand

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="642cd-134">-位置</span><span class="sxs-lookup"><span data-stu-id="642cd-134">-Location</span></span>
<span data-ttu-id="642cd-135">指定虛擬機器的清單位置。</span><span class="sxs-lookup"><span data-stu-id="642cd-135">Specifies a location for the virtual machines to list.</span></span>

```yaml
Type: System.String
Parameter Sets: ListLocationVirtualMachinesParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="642cd-136">-名稱</span><span class="sxs-lookup"><span data-stu-id="642cd-136">-Name</span></span>
<span data-ttu-id="642cd-137">指定要取得的虛擬機器名稱。</span><span class="sxs-lookup"><span data-stu-id="642cd-137">Specifies the name of the virtual machine to get.</span></span>

```yaml
Type: System.String
Parameter Sets: GetVirtualMachineInResourceGroupParamSet
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="642cd-138">-NextLink</span><span class="sxs-lookup"><span data-stu-id="642cd-138">-NextLink</span></span>
<span data-ttu-id="642cd-139">指定 [下一步] 連結。</span><span class="sxs-lookup"><span data-stu-id="642cd-139">Specifies the next link.</span></span>

```yaml
Type: System.Uri
Parameter Sets: ListNextLinkVirtualMachinesParamSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="642cd-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="642cd-140">-ResourceGroupName</span></span>
<span data-ttu-id="642cd-141">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="642cd-141">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ListVirtualMachineInResourceGroupParamSet, GetVirtualMachineInResourceGroupParamSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="642cd-142">-狀態</span><span class="sxs-lookup"><span data-stu-id="642cd-142">-Status</span></span>
<span data-ttu-id="642cd-143">表示此 Cmdlet 只會取得虛擬機器的實例視圖。</span><span class="sxs-lookup"><span data-stu-id="642cd-143">Indicates that this cmdlet gets only the instance view of the virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="642cd-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="642cd-144">CommonParameters</span></span>
<span data-ttu-id="642cd-145">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="642cd-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="642cd-146">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="642cd-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="642cd-147">輸入</span><span class="sxs-lookup"><span data-stu-id="642cd-147">INPUTS</span></span>

### <span data-ttu-id="642cd-148">System.object</span><span class="sxs-lookup"><span data-stu-id="642cd-148">System.String</span></span>

### <span data-ttu-id="642cd-149">系統 Uri</span><span class="sxs-lookup"><span data-stu-id="642cd-149">System.Uri</span></span>

### <span data-ttu-id="642cd-150">DisplayHintType 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="642cd-150">Microsoft.Azure.Commands.Compute.Models.DisplayHintType</span></span>

## <span data-ttu-id="642cd-151">輸出</span><span class="sxs-lookup"><span data-stu-id="642cd-151">OUTPUTS</span></span>

### <span data-ttu-id="642cd-152">PSVirtualMachine 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="642cd-152">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="642cd-153">PSVirtualMachineInstanceView 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="642cd-153">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineInstanceView</span></span>

## <span data-ttu-id="642cd-154">筆記</span><span class="sxs-lookup"><span data-stu-id="642cd-154">NOTES</span></span>

## <span data-ttu-id="642cd-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="642cd-155">RELATED LINKS</span></span>

[<span data-ttu-id="642cd-156">新-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="642cd-156">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="642cd-157">移除-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="642cd-157">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="642cd-158">重新開機-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="642cd-158">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="642cd-159">開始-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="642cd-159">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="642cd-160">停止 AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="642cd-160">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="642cd-161">更新-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="642cd-161">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


