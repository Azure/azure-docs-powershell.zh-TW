---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 63D48BA4-EE80-4740-90B9-0EE05B3F6536
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmssvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssVM.md
ms.openlocfilehash: d7eb7d8dd6fd8bb9f9071a00aef6a90057b81d02
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93788474"
---
# <span data-ttu-id="52e2e-101">Get-AzVmssVM</span><span class="sxs-lookup"><span data-stu-id="52e2e-101">Get-AzVmssVM</span></span>

## <span data-ttu-id="52e2e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="52e2e-102">SYNOPSIS</span></span>
<span data-ttu-id="52e2e-103">取得 VMSS 虛擬機器的屬性。</span><span class="sxs-lookup"><span data-stu-id="52e2e-103">Gets the properties of a VMSS virtual machine.</span></span>

## <span data-ttu-id="52e2e-104">句法</span><span class="sxs-lookup"><span data-stu-id="52e2e-104">SYNTAX</span></span>

### <span data-ttu-id="52e2e-105">DefaultParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="52e2e-105">DefaultParameter (Default)</span></span>
```
Get-AzVmssVM [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [[-InstanceId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="52e2e-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="52e2e-106">FriendMethod</span></span>
```
Get-AzVmssVM [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [[-InstanceId] <String>]
 [-InstanceView] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="52e2e-107">說明</span><span class="sxs-lookup"><span data-stu-id="52e2e-107">DESCRIPTION</span></span>
<span data-ttu-id="52e2e-108">**AzVmssVM** Cmdlet 會取得虛擬機器規模集的模型視圖和實例視圖， (VMSS) 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="52e2e-108">The **Get-AzVmssVM** cmdlet gets the model view and instance view of a Virtual Machine Scale Set (VMSS) virtual machine.</span></span>
<span data-ttu-id="52e2e-109">模型視圖是使用者指定的虛擬機器屬性。</span><span class="sxs-lookup"><span data-stu-id="52e2e-109">The model view is the user specified properties of the virtual machine.</span></span>
<span data-ttu-id="52e2e-110">[實例] 視圖是虛擬機器的實例層級狀態。</span><span class="sxs-lookup"><span data-stu-id="52e2e-110">The instance view is the instance level status of the virtual machine.</span></span>
<span data-ttu-id="52e2e-111">指定 *Status* 參數，只取得虛擬機器的 [實例] 視圖。</span><span class="sxs-lookup"><span data-stu-id="52e2e-111">Specify the *Status* parameter to get only the instance view of a virtual machine.</span></span>

## <span data-ttu-id="52e2e-112">示例</span><span class="sxs-lookup"><span data-stu-id="52e2e-112">EXAMPLES</span></span>

### <span data-ttu-id="52e2e-113">範例1：取得 VMSS 虛擬機器的屬性</span><span class="sxs-lookup"><span data-stu-id="52e2e-113">Example 1: Get the properties of a VMSS virtual machine</span></span>
```
PS C:\> Get-AzVmssVM -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="52e2e-114">這個命令會取得名為 VMSS001 的 VMSS 虛擬電腦的屬性，該虛擬機器屬於名為 Group001 的資源群組。</span><span class="sxs-lookup"><span data-stu-id="52e2e-114">This command gets the properties of the VMSS virtual machine named VMSS001 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="52e2e-115">由於命令不會指定 *InstanceView* 切換參數，因此 Cmdlet 會取得虛擬機器的模型視圖。</span><span class="sxs-lookup"><span data-stu-id="52e2e-115">Since the command does not specify the *InstanceView* switch parameter, the cmdlet gets the model view of the virtual machine.</span></span>

### <span data-ttu-id="52e2e-116">範例2：取得 VMSS 虛擬機器的模型視圖屬性</span><span class="sxs-lookup"><span data-stu-id="52e2e-116">Example 2: Get the model view properties of a VMSS virtual machine</span></span>
```
PS C:\> Get-AzVmssVM -ResourceGroupName "Group002" -VMScaleSetName "VMSS004" -InstanceId $ID
```

<span data-ttu-id="52e2e-117">這個命令會取得名為 VMSS004 的 VMSS 虛擬電腦的屬性，該虛擬機器屬於名為 Group002 的資源群組。</span><span class="sxs-lookup"><span data-stu-id="52e2e-117">This command gets the properties of the VMSS virtual machine named VMSS004 that belongs to the resource group named Group002.</span></span>
<span data-ttu-id="52e2e-118">命令會取得儲存在變數 $ID 中的實例識別碼，以取得模型視圖。</span><span class="sxs-lookup"><span data-stu-id="52e2e-118">The command gets the instance ID stored in the variable $ID for which to get the model view.</span></span>

### <span data-ttu-id="52e2e-119">範例3：取得 VMSS 虛擬機器的實例視圖屬性</span><span class="sxs-lookup"><span data-stu-id="52e2e-119">Example 3: Get the instance view properties of a VMSS virtual machine</span></span>
```
PS C:\> Get-AzVmssVM -InstanceView  -ResourceGroupName $rgname  -VMScaleSetName $vmssName -InstanceId $ID
```

<span data-ttu-id="52e2e-120">這個命令會取得名為 VMSS004 的 VMSS 虛擬電腦的屬性，該虛擬機器屬於名為 Group002 的資源群組。</span><span class="sxs-lookup"><span data-stu-id="52e2e-120">This command gets the properties of the VMSS virtual machine named VMSS004 that belongs to the resource group named Group002.</span></span>
<span data-ttu-id="52e2e-121">由於命令會指定 *InstanceView* 切換參數，因此 Cmdlet 會取得虛擬機器的實例視圖。</span><span class="sxs-lookup"><span data-stu-id="52e2e-121">Since the command specifies the *InstanceView* switch parameter, the cmdlet gets the instance view of the virtual machine.</span></span>
<span data-ttu-id="52e2e-122">命令會取得儲存在變數 $ID 中的實例識別碼，以取得實例視圖。</span><span class="sxs-lookup"><span data-stu-id="52e2e-122">The command gets the instance ID stored in the variable $ID for which to get the instance view.</span></span>

## <span data-ttu-id="52e2e-123">參數</span><span class="sxs-lookup"><span data-stu-id="52e2e-123">PARAMETERS</span></span>

### <span data-ttu-id="52e2e-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52e2e-124">-DefaultProfile</span></span>
<span data-ttu-id="52e2e-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="52e2e-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="52e2e-126">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="52e2e-126">-InstanceId</span></span>
<span data-ttu-id="52e2e-127">指定要取得模型視圖的實例識別碼。</span><span class="sxs-lookup"><span data-stu-id="52e2e-127">Specifies the instance ID for which to get the model view.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52e2e-128">-InstanceView</span><span class="sxs-lookup"><span data-stu-id="52e2e-128">-InstanceView</span></span>
<span data-ttu-id="52e2e-129">表示此 Cmdlet 只會取得虛擬機器的實例視圖。</span><span class="sxs-lookup"><span data-stu-id="52e2e-129">Indicates that this cmdlet gets only the instance view of the virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FriendMethod
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52e2e-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52e2e-130">-ResourceGroupName</span></span>
<span data-ttu-id="52e2e-131">指定 VMSS 之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="52e2e-131">Specifies the name of the Resource Group of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52e2e-132">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="52e2e-132">-VMScaleSetName</span></span>
<span data-ttu-id="52e2e-133">Species VMSS 的名稱。</span><span class="sxs-lookup"><span data-stu-id="52e2e-133">Species the name of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52e2e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52e2e-134">CommonParameters</span></span>
<span data-ttu-id="52e2e-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="52e2e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52e2e-136">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="52e2e-136">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52e2e-137">輸入</span><span class="sxs-lookup"><span data-stu-id="52e2e-137">INPUTS</span></span>

### <span data-ttu-id="52e2e-138">System.object</span><span class="sxs-lookup"><span data-stu-id="52e2e-138">System.String</span></span>

## <span data-ttu-id="52e2e-139">輸出</span><span class="sxs-lookup"><span data-stu-id="52e2e-139">OUTPUTS</span></span>

### <span data-ttu-id="52e2e-140">PSVirtualMachineScaleSetVM 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="52e2e-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="52e2e-141">筆記</span><span class="sxs-lookup"><span data-stu-id="52e2e-141">NOTES</span></span>

## <span data-ttu-id="52e2e-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="52e2e-142">RELATED LINKS</span></span>

[<span data-ttu-id="52e2e-143">Set-AzVmssVM</span><span class="sxs-lookup"><span data-stu-id="52e2e-143">Set-AzVmssVM</span></span>](./Set-AzVmssVM.md)

[<span data-ttu-id="52e2e-144">AzVmss</span><span class="sxs-lookup"><span data-stu-id="52e2e-144">Get-AzVmss</span></span>](./Get-AzVmss.md)

