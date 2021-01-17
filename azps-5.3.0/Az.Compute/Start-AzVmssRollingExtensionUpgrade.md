---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/start-azvmssrollingextensionupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVmssRollingExtensionUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVmssRollingExtensionUpgrade.md
ms.openlocfilehash: a98818a855ef7bc75fb27c466dd0ba555d53a10f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98446264"
---
# <span data-ttu-id="1554c-101">Start-AzVmssRollingExtensionUpgrade</span><span class="sxs-lookup"><span data-stu-id="1554c-101">Start-AzVmssRollingExtensionUpgrade</span></span>

## <span data-ttu-id="1554c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1554c-102">SYNOPSIS</span></span>
<span data-ttu-id="1554c-103">這個 Cmdlet 會啟動針對指定的虛擬機器縮放比例設定為最新可用版本的所有延伸的輪流升級。</span><span class="sxs-lookup"><span data-stu-id="1554c-103">This cmdlet starts a rolling upgrade for all extensions on the given Virtual Machine Scale Set to the latest available version.</span></span> 

## <span data-ttu-id="1554c-104">句法</span><span class="sxs-lookup"><span data-stu-id="1554c-104">SYNTAX</span></span>

### <span data-ttu-id="1554c-105">DefaultParameter</span><span class="sxs-lookup"><span data-stu-id="1554c-105">DefaultParameter</span></span>
```
Start-AzVmssRollingExtensionUpgrade -ResourceGroupName <String> -VMScaleSetName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1554c-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="1554c-106">ByInputObject</span></span>
```
Start-AzVmssRollingExtensionUpgrade -VirtualMachineScaleSet <PSVirtualMachineScaleSet> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1554c-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="1554c-107">ByResourceId</span></span>
```
Start-AzVmssRollingExtensionUpgrade -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1554c-108">說明</span><span class="sxs-lookup"><span data-stu-id="1554c-108">DESCRIPTION</span></span>
<span data-ttu-id="1554c-109">啟動 [輪流升級]，將此虛擬機器縮放設定的所有延長線移至最新的可用版本。</span><span class="sxs-lookup"><span data-stu-id="1554c-109">Starts a rolling upgrade to move all extensions on this virtual machine scale set to the latest available version.</span></span>
<span data-ttu-id="1554c-110">已執行最新可用版本的延長線不會受到影響。</span><span class="sxs-lookup"><span data-stu-id="1554c-110">Extensions which are already running the latest available version are not affected.</span></span>

## <span data-ttu-id="1554c-111">示例</span><span class="sxs-lookup"><span data-stu-id="1554c-111">EXAMPLES</span></span>

### <span data-ttu-id="1554c-112">範例1</span><span class="sxs-lookup"><span data-stu-id="1554c-112">Example 1</span></span>
```powershell
PS C:\> $vmss = Get-AzVM -ResourceGroupName "MyResourceGroupName" -VMScaleSetName "MyVmssName";
PS C:\> Add-AzVmssExtension -VirtualMachineScaleSet $vmss -Name "testExtension" -Publisher Microsoft.CPlat.Core -Type "NullWindows" -TypeHandlerVersion "3.0" -AutoUpgradeMinorVersion $True  -Setting "";
PS C:\> Start-AzVmssRollingExtensionUpgrade -ResourceGroupName "MyResourceGroupName" -VMScaleSetName "MyVmssName";
```

<span data-ttu-id="1554c-113">這個範例會取得現有的 VM 比例集 "MyVmssName"，並將延伸加到其中。</span><span class="sxs-lookup"><span data-stu-id="1554c-113">This example gets the existing VM scale set "MyVmssName", and adds an extension to it.</span></span> <span data-ttu-id="1554c-114">最後一個命令會執行延伸輪流升級程式。</span><span class="sxs-lookup"><span data-stu-id="1554c-114">The final command runs the extension rolling upgrade process.</span></span> 

## <span data-ttu-id="1554c-115">參數</span><span class="sxs-lookup"><span data-stu-id="1554c-115">PARAMETERS</span></span>

### <span data-ttu-id="1554c-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1554c-116">-AsJob</span></span>
<span data-ttu-id="1554c-117">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="1554c-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1554c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1554c-118">-DefaultProfile</span></span>
<span data-ttu-id="1554c-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1554c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1554c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1554c-120">-ResourceGroupName</span></span>
<span data-ttu-id="1554c-121">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1554c-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="1554c-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1554c-122">-ResourceId</span></span>
<span data-ttu-id="1554c-123">[VM 比例集] 物件的 [資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="1554c-123">The resource Id of the VM scale set object.</span></span> 

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

### <span data-ttu-id="1554c-124">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="1554c-124">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="1554c-125">VM 比例集物件。</span><span class="sxs-lookup"><span data-stu-id="1554c-125">The VM scale set object.</span></span>

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

### <span data-ttu-id="1554c-126">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="1554c-126">-VMScaleSetName</span></span>
<span data-ttu-id="1554c-127">VM 比例集的名稱。</span><span class="sxs-lookup"><span data-stu-id="1554c-127">The name of the VM scale set.</span></span>

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

### <span data-ttu-id="1554c-128">-確認</span><span class="sxs-lookup"><span data-stu-id="1554c-128">-Confirm</span></span>
<span data-ttu-id="1554c-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1554c-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1554c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1554c-130">-WhatIf</span></span>
<span data-ttu-id="1554c-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1554c-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1554c-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1554c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1554c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1554c-133">CommonParameters</span></span>
<span data-ttu-id="1554c-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1554c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1554c-135">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="1554c-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1554c-136">輸入</span><span class="sxs-lookup"><span data-stu-id="1554c-136">INPUTS</span></span>

### <span data-ttu-id="1554c-137">System.object</span><span class="sxs-lookup"><span data-stu-id="1554c-137">System.String</span></span>

### <span data-ttu-id="1554c-138">PSVirtualMachineScaleSet 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="1554c-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="1554c-139">輸出</span><span class="sxs-lookup"><span data-stu-id="1554c-139">OUTPUTS</span></span>

### <span data-ttu-id="1554c-140">PSOperationStatusResponse 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="1554c-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="1554c-141">筆記</span><span class="sxs-lookup"><span data-stu-id="1554c-141">NOTES</span></span>

## <span data-ttu-id="1554c-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="1554c-142">RELATED LINKS</span></span>
