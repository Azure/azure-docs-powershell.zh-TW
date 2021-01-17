---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 5F135E64-9432-4D08-961F-4604410378A3
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmssdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssDiagnosticsExtension.md
ms.openlocfilehash: 0bf685f9efbe47271fddcc842c1237dd86e8a298
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98449736"
---
# <span data-ttu-id="e8132-101">Remove-AzVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="e8132-101">Remove-AzVmssDiagnosticsExtension</span></span>

## <span data-ttu-id="e8132-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e8132-102">SYNOPSIS</span></span>
<span data-ttu-id="e8132-103">從 VMSS 移除診斷延伸。</span><span class="sxs-lookup"><span data-stu-id="e8132-103">Removes a diagnostics extension from the VMSS.</span></span>

## <span data-ttu-id="e8132-104">句法</span><span class="sxs-lookup"><span data-stu-id="e8132-104">SYNTAX</span></span>

```
Remove-AzVmssDiagnosticsExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8132-105">說明</span><span class="sxs-lookup"><span data-stu-id="e8132-105">DESCRIPTION</span></span>
<span data-ttu-id="e8132-106">**AzVmssDiagnosticsExtension** Cmdlet 會從虛擬機器縮放集 (VMSS) 中移除診斷延伸。</span><span class="sxs-lookup"><span data-stu-id="e8132-106">The **Remove-AzVmssDiagnosticsExtension** cmdlet removes a diagnostics extension from the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="e8132-107">示例</span><span class="sxs-lookup"><span data-stu-id="e8132-107">EXAMPLES</span></span>

### <span data-ttu-id="e8132-108">範例1：從 VMSS 移除診斷延伸</span><span class="sxs-lookup"><span data-stu-id="e8132-108">Example 1: Remove a diagnostics extension from the VMSS</span></span>
```
PS C:\> Remove-AzVmssDiagnosticsExtension -VirtualMachineScaleSet $VMSS -Name $extName
```

<span data-ttu-id="e8132-109">這個命令會從 VMSS 中移除診斷延伸。</span><span class="sxs-lookup"><span data-stu-id="e8132-109">This command removes diagnostics extension from the VMSS.</span></span>

## <span data-ttu-id="e8132-110">參數</span><span class="sxs-lookup"><span data-stu-id="e8132-110">PARAMETERS</span></span>

### <span data-ttu-id="e8132-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8132-111">-DefaultProfile</span></span>
<span data-ttu-id="e8132-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e8132-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e8132-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="e8132-113">-Name</span></span>
<span data-ttu-id="e8132-114">指定此 Cmdlet 從 VMSS 中移除之延伸的名稱。</span><span class="sxs-lookup"><span data-stu-id="e8132-114">Specifies the name of the extension that this cmdlet removes from the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8132-115">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="e8132-115">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="e8132-116">指定要移除延伸的 VMSS。</span><span class="sxs-lookup"><span data-stu-id="e8132-116">Specifies the VMSS from which to remove the extension.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e8132-117">-確認</span><span class="sxs-lookup"><span data-stu-id="e8132-117">-Confirm</span></span>
<span data-ttu-id="e8132-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e8132-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8132-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8132-119">-WhatIf</span></span>
<span data-ttu-id="e8132-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e8132-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8132-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e8132-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8132-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8132-122">CommonParameters</span></span>
<span data-ttu-id="e8132-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e8132-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8132-124">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e8132-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8132-125">輸入</span><span class="sxs-lookup"><span data-stu-id="e8132-125">INPUTS</span></span>

### <span data-ttu-id="e8132-126">PSVirtualMachineScaleSet 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="e8132-126">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="e8132-127">System.object</span><span class="sxs-lookup"><span data-stu-id="e8132-127">System.String</span></span>

## <span data-ttu-id="e8132-128">輸出</span><span class="sxs-lookup"><span data-stu-id="e8132-128">OUTPUTS</span></span>

### <span data-ttu-id="e8132-129">PSVirtualMachineScaleSet 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="e8132-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="e8132-130">筆記</span><span class="sxs-lookup"><span data-stu-id="e8132-130">NOTES</span></span>

## <span data-ttu-id="e8132-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="e8132-131">RELATED LINKS</span></span>

[<span data-ttu-id="e8132-132">附加 AzVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="e8132-132">Add-AzVmssDiagnosticsExtension</span></span>](./Add-AzVmssDiagnosticsExtension.md)

[<span data-ttu-id="e8132-133">移除-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="e8132-133">Remove-AzVMDiagnosticsExtension</span></span>](./Remove-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="e8132-134">移除-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="e8132-134">Remove-AzVmssExtension</span></span>](./Remove-AzVmssExtension.md)


