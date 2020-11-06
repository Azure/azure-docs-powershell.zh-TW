---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 6250EC11-79CF-428B-A72F-9BD72C1751F0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvm
schema: 2.0.0
ms.openlocfilehash: 4dbae539d43961d954dba6ea12bd88e08d9616ba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449945"
---
# <span data-ttu-id="2411a-101">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="2411a-101">Get-AzureRmVM</span></span>

## <span data-ttu-id="2411a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2411a-102">SYNOPSIS</span></span>
<span data-ttu-id="2411a-103">取得 Azure 資源管理器 (ARM) 虛擬機器的屬性。</span><span class="sxs-lookup"><span data-stu-id="2411a-103">Gets the properties of an Azure Resource Manager (ARM) virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2411a-104">句法</span><span class="sxs-lookup"><span data-stu-id="2411a-104">SYNTAX</span></span>

### <span data-ttu-id="2411a-105">ListAllVirtualMachinesParamSet (預設) </span><span class="sxs-lookup"><span data-stu-id="2411a-105">ListAllVirtualMachinesParamSet (Default)</span></span>
```
Get-AzureRmVM [-Status] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2411a-106">ListVirtualMachineInResourceGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="2411a-106">ListVirtualMachineInResourceGroupParamSet</span></span>
```
Get-AzureRmVM [-ResourceGroupName] <String> [-Status] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2411a-107">GetVirtualMachineInResourceGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="2411a-107">GetVirtualMachineInResourceGroupParamSet</span></span>
```
Get-AzureRmVM [-ResourceGroupName] <String> [-Name] <String> [-Status] [-DisplayHint <DisplayHintType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2411a-108">ListNextLinkVirtualMachinesParamSet</span><span class="sxs-lookup"><span data-stu-id="2411a-108">ListNextLinkVirtualMachinesParamSet</span></span>
```
Get-AzureRmVM [-Status] [-NextLink] <Uri> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2411a-109">說明</span><span class="sxs-lookup"><span data-stu-id="2411a-109">DESCRIPTION</span></span>
<span data-ttu-id="2411a-110">**AzureRmVM** Cmdlet 會取得 Azure 虛擬機器的 [模型] 視圖和 [實例] 視圖。</span><span class="sxs-lookup"><span data-stu-id="2411a-110">The **Get-AzureRmVM** cmdlet gets the model view and instance view of an Azure virtual machine.</span></span>
<span data-ttu-id="2411a-111">模型視圖是使用者指定的虛擬機器屬性。</span><span class="sxs-lookup"><span data-stu-id="2411a-111">The model view is the user specified properties of the virtual machine.</span></span>
<span data-ttu-id="2411a-112">[實例] 視圖是虛擬機器的實例層級狀態。</span><span class="sxs-lookup"><span data-stu-id="2411a-112">The instance view is the instance level status of the virtual machine.</span></span>
<span data-ttu-id="2411a-113">指定 *Status* 參數，只取得虛擬機器的 [實例] 視圖。</span><span class="sxs-lookup"><span data-stu-id="2411a-113">Specify the *Status* parameter to get only the instance view of a virtual machine.</span></span>

## <span data-ttu-id="2411a-114">示例</span><span class="sxs-lookup"><span data-stu-id="2411a-114">EXAMPLES</span></span>

### <span data-ttu-id="2411a-115">範例1：取得模型和實例視圖屬性</span><span class="sxs-lookup"><span data-stu-id="2411a-115">Example 1: Get model and instance view properties</span></span>
```
PS C:\> Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="2411a-116">這個命令會取得名為 VirtualMachine07 的虛擬機器的模型視圖和實例視圖屬性。</span><span class="sxs-lookup"><span data-stu-id="2411a-116">This command gets the model view and instance view properties of the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="2411a-117">範例2：取得實例視圖屬性</span><span class="sxs-lookup"><span data-stu-id="2411a-117">Example 2: Get instance view properties</span></span>
```
PS C:\> Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Status
```

<span data-ttu-id="2411a-118">這個命令會取得名為 VirtualMachine07 的虛擬機器的屬性。</span><span class="sxs-lookup"><span data-stu-id="2411a-118">This command gets properties of the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="2411a-119">這個命令會指定 *Status* 參數。</span><span class="sxs-lookup"><span data-stu-id="2411a-119">This command specifies the *Status* parameter.</span></span>
<span data-ttu-id="2411a-120">因此，命令只會取得實例視圖屬性。</span><span class="sxs-lookup"><span data-stu-id="2411a-120">Therefore, the command gets only the instance view properties.</span></span>

### <span data-ttu-id="2411a-121">範例3：取得資源群組中所有虛擬機器的屬性</span><span class="sxs-lookup"><span data-stu-id="2411a-121">Example 3: Get properties for all virtual machines in a resource group</span></span>
```
PS C:\> Get-AzureRmVM -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="2411a-122">這個命令會取得名為 ResourceGroup11 之資源群組中所有虛擬機器的屬性。</span><span class="sxs-lookup"><span data-stu-id="2411a-122">This command gets properties for all the virtual machines in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="2411a-123">範例4：取得您訂閱中的所有虛擬機器</span><span class="sxs-lookup"><span data-stu-id="2411a-123">Example 4: Get all virtual machines in your subscription</span></span>
```
PS C:\> Get-AzureRmVM
```

<span data-ttu-id="2411a-124">這個命令會取得您訂閱中的所有虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="2411a-124">This command gets all the virtual machines in your subscription.</span></span>

## <span data-ttu-id="2411a-125">參數</span><span class="sxs-lookup"><span data-stu-id="2411a-125">PARAMETERS</span></span>

### <span data-ttu-id="2411a-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2411a-126">-DefaultProfile</span></span>
<span data-ttu-id="2411a-127">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2411a-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2411a-128">-DisplayHint</span><span class="sxs-lookup"><span data-stu-id="2411a-128">-DisplayHint</span></span>
<span data-ttu-id="2411a-129">決定虛擬機器物件的顯示方式。</span><span class="sxs-lookup"><span data-stu-id="2411a-129">Determines how the virtual machine object is displayed.</span></span>

<span data-ttu-id="2411a-130">有效值為：</span><span class="sxs-lookup"><span data-stu-id="2411a-130">Valid values are:</span></span>

<span data-ttu-id="2411a-131">--精簡：僅顯示最上層屬性</span><span class="sxs-lookup"><span data-stu-id="2411a-131">-- Compact: displays only top level properties</span></span>

<span data-ttu-id="2411a-132">--展開：顯示所有層級中的所有屬性</span><span class="sxs-lookup"><span data-stu-id="2411a-132">-- Expand: displays all properties in all levels</span></span>
```yaml
Type: DisplayHintType
Parameter Sets: GetVirtualMachineInResourceGroupParamSet
Aliases:
Accepted values: Compact, Expand

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2411a-133">-名稱</span><span class="sxs-lookup"><span data-stu-id="2411a-133">-Name</span></span>
<span data-ttu-id="2411a-134">指定要取得的虛擬機器名稱。</span><span class="sxs-lookup"><span data-stu-id="2411a-134">Specifies the name of the virtual machine to get.</span></span>

```yaml
Type: String
Parameter Sets: GetVirtualMachineInResourceGroupParamSet
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2411a-135">-NextLink</span><span class="sxs-lookup"><span data-stu-id="2411a-135">-NextLink</span></span>
<span data-ttu-id="2411a-136">指定 [下一步] 連結。</span><span class="sxs-lookup"><span data-stu-id="2411a-136">Specifies the next link.</span></span>

```yaml
Type: Uri
Parameter Sets: ListNextLinkVirtualMachinesParamSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2411a-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2411a-137">-ResourceGroupName</span></span>
<span data-ttu-id="2411a-138">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2411a-138">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: ListVirtualMachineInResourceGroupParamSet, GetVirtualMachineInResourceGroupParamSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2411a-139">-狀態</span><span class="sxs-lookup"><span data-stu-id="2411a-139">-Status</span></span>
<span data-ttu-id="2411a-140">表示此 Cmdlet 只會取得虛擬機器的實例視圖。</span><span class="sxs-lookup"><span data-stu-id="2411a-140">Indicates that this cmdlet gets only the instance view of the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2411a-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2411a-141">CommonParameters</span></span>
<span data-ttu-id="2411a-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2411a-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2411a-143">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2411a-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2411a-144">輸入</span><span class="sxs-lookup"><span data-stu-id="2411a-144">INPUTS</span></span>

### <span data-ttu-id="2411a-145">所有</span><span class="sxs-lookup"><span data-stu-id="2411a-145">None</span></span>
<span data-ttu-id="2411a-146">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="2411a-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2411a-147">輸出</span><span class="sxs-lookup"><span data-stu-id="2411a-147">OUTPUTS</span></span>

### <span data-ttu-id="2411a-148">PSVirtualMachine 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="2411a-148">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="2411a-149">PSVirtualMachineInstanceView 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="2411a-149">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineInstanceView</span></span>

## <span data-ttu-id="2411a-150">筆記</span><span class="sxs-lookup"><span data-stu-id="2411a-150">NOTES</span></span>

## <span data-ttu-id="2411a-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="2411a-151">RELATED LINKS</span></span>

[<span data-ttu-id="2411a-152">新-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="2411a-152">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="2411a-153">移除-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="2411a-153">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="2411a-154">重新開機-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="2411a-154">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="2411a-155">開始-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="2411a-155">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="2411a-156">停止 AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="2411a-156">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="2411a-157">更新-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="2411a-157">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


