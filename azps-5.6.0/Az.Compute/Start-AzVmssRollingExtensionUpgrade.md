---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/start-azvmssrollingextensionupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVmssRollingExtensionUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVmssRollingExtensionUpgrade.md
ms.openlocfilehash: 2816f34c8a6148d67a5bed397e573b07fa2e7004
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910742"
---
# <span data-ttu-id="6b3f6-101">Start-AzVmssRollingExtensionUpgrade</span><span class="sxs-lookup"><span data-stu-id="6b3f6-101">Start-AzVmssRollingExtensionUpgrade</span></span>

## <span data-ttu-id="6b3f6-102">簡介</span><span class="sxs-lookup"><span data-stu-id="6b3f6-102">SYNOPSIS</span></span>
<span data-ttu-id="6b3f6-103">此 Cmdlet 會針對所設定為最新可用版本之虛擬機器縮放比例上的所有擴充功能開始進行輪流升級。</span><span class="sxs-lookup"><span data-stu-id="6b3f6-103">This cmdlet starts a rolling upgrade for all extensions on the given Virtual Machine Scale Set to the latest available version.</span></span> 

## <span data-ttu-id="6b3f6-104">語法</span><span class="sxs-lookup"><span data-stu-id="6b3f6-104">SYNTAX</span></span>

### <span data-ttu-id="6b3f6-105">DefaultParameter</span><span class="sxs-lookup"><span data-stu-id="6b3f6-105">DefaultParameter</span></span>
```
Start-AzVmssRollingExtensionUpgrade -ResourceGroupName <String> -VMScaleSetName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b3f6-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="6b3f6-106">ByInputObject</span></span>
```
Start-AzVmssRollingExtensionUpgrade -VirtualMachineScaleSet <PSVirtualMachineScaleSet> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b3f6-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="6b3f6-107">ByResourceId</span></span>
```
Start-AzVmssRollingExtensionUpgrade -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b3f6-108">描述</span><span class="sxs-lookup"><span data-stu-id="6b3f6-108">DESCRIPTION</span></span>
<span data-ttu-id="6b3f6-109">開始進行輪流升級，將此虛擬機器規模上的所有擴充功能移至最新可用版本。</span><span class="sxs-lookup"><span data-stu-id="6b3f6-109">Starts a rolling upgrade to move all extensions on this virtual machine scale set to the latest available version.</span></span>
<span data-ttu-id="6b3f6-110">已使用最新可用版本的擴充功能不受影響。</span><span class="sxs-lookup"><span data-stu-id="6b3f6-110">Extensions which are already running the latest available version are not affected.</span></span>

## <span data-ttu-id="6b3f6-111">例子</span><span class="sxs-lookup"><span data-stu-id="6b3f6-111">EXAMPLES</span></span>

### <span data-ttu-id="6b3f6-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="6b3f6-112">Example 1</span></span>
```powershell
PS C:\> $vmss = Get-AzVM -ResourceGroupName "MyResourceGroupName" -VMScaleSetName "MyVmssName";
PS C:\> Add-AzVmssExtension -VirtualMachineScaleSet $vmss -Name "testExtension" -Publisher Microsoft.CPlat.Core -Type "NullWindows" -TypeHandlerVersion "3.0" -AutoUpgradeMinorVersion $True  -Setting "";
PS C:\> Start-AzVmssRollingExtensionUpgrade -ResourceGroupName "MyResourceGroupName" -VMScaleSetName "MyVmssName";
```

<span data-ttu-id="6b3f6-113">此範例會獲得現有的 VM 縮放集 "My VmssName"，並新增擴充功能。</span><span class="sxs-lookup"><span data-stu-id="6b3f6-113">This example gets the existing VM scale set "MyVmssName", and adds an extension to it.</span></span> <span data-ttu-id="6b3f6-114">最後一個命令會執行擴充功能輪流升級程式。</span><span class="sxs-lookup"><span data-stu-id="6b3f6-114">The final command runs the extension rolling upgrade process.</span></span> 

## <span data-ttu-id="6b3f6-115">參數</span><span class="sxs-lookup"><span data-stu-id="6b3f6-115">PARAMETERS</span></span>

### <span data-ttu-id="6b3f6-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6b3f6-116">-AsJob</span></span>
<span data-ttu-id="6b3f6-117">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6b3f6-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6b3f6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b3f6-118">-DefaultProfile</span></span>
<span data-ttu-id="6b3f6-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="6b3f6-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6b3f6-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b3f6-120">-ResourceGroupName</span></span>
<span data-ttu-id="6b3f6-121">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6b3f6-121">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b3f6-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6b3f6-122">-ResourceId</span></span>
<span data-ttu-id="6b3f6-123">VM 縮放集物件的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="6b3f6-123">The resource Id of the VM scale set object.</span></span> 

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6b3f6-124">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="6b3f6-124">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="6b3f6-125">VM 縮放集物件。</span><span class="sxs-lookup"><span data-stu-id="6b3f6-125">The VM scale set object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6b3f6-126">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="6b3f6-126">-VMScaleSetName</span></span>
<span data-ttu-id="6b3f6-127">VM 縮放集的名稱。</span><span class="sxs-lookup"><span data-stu-id="6b3f6-127">The name of the VM scale set.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b3f6-128">-確認</span><span class="sxs-lookup"><span data-stu-id="6b3f6-128">-Confirm</span></span>
<span data-ttu-id="6b3f6-129">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="6b3f6-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b3f6-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b3f6-130">-WhatIf</span></span>
<span data-ttu-id="6b3f6-131">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6b3f6-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b3f6-132">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6b3f6-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b3f6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b3f6-133">CommonParameters</span></span>
<span data-ttu-id="6b3f6-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="6b3f6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b3f6-135">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6b3f6-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b3f6-136">輸入</span><span class="sxs-lookup"><span data-stu-id="6b3f6-136">INPUTS</span></span>

### <span data-ttu-id="6b3f6-137">System.String</span><span class="sxs-lookup"><span data-stu-id="6b3f6-137">System.String</span></span>

### <span data-ttu-id="6b3f6-138">Microsoft.Azure.Commands.Compute.Automation.models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="6b3f6-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="6b3f6-139">輸出</span><span class="sxs-lookup"><span data-stu-id="6b3f6-139">OUTPUTS</span></span>

### <span data-ttu-id="6b3f6-140">Microsoft.Azure.Commands.Compute.Automation.models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="6b3f6-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="6b3f6-141">筆記</span><span class="sxs-lookup"><span data-stu-id="6b3f6-141">NOTES</span></span>

## <span data-ttu-id="6b3f6-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="6b3f6-142">RELATED LINKS</span></span>
