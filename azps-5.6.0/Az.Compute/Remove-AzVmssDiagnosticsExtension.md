---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 5F135E64-9432-4D08-961F-4604410378A3
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azvmssdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssDiagnosticsExtension.md
ms.openlocfilehash: 233423f6c9515263bfa457d3bd456415b5a389e2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917094"
---
# <span data-ttu-id="56edb-101">Remove-AzVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="56edb-101">Remove-AzVmssDiagnosticsExtension</span></span>

## <span data-ttu-id="56edb-102">簡介</span><span class="sxs-lookup"><span data-stu-id="56edb-102">SYNOPSIS</span></span>
<span data-ttu-id="56edb-103">從 VMSS 移除診斷擴充功能。</span><span class="sxs-lookup"><span data-stu-id="56edb-103">Removes a diagnostics extension from the VMSS.</span></span>

## <span data-ttu-id="56edb-104">語法</span><span class="sxs-lookup"><span data-stu-id="56edb-104">SYNTAX</span></span>

```
Remove-AzVmssDiagnosticsExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="56edb-105">描述</span><span class="sxs-lookup"><span data-stu-id="56edb-105">DESCRIPTION</span></span>
<span data-ttu-id="56edb-106">**Remove-Az VmssDiagnosticsExtension** Cmdlet 會從虛擬機器縮放集 (VMSS) 移除診斷副檔名。</span><span class="sxs-lookup"><span data-stu-id="56edb-106">The **Remove-AzVmssDiagnosticsExtension** cmdlet removes a diagnostics extension from the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="56edb-107">例子</span><span class="sxs-lookup"><span data-stu-id="56edb-107">EXAMPLES</span></span>

### <span data-ttu-id="56edb-108">範例 1：從 VMSS 移除診斷擴充功能</span><span class="sxs-lookup"><span data-stu-id="56edb-108">Example 1: Remove a diagnostics extension from the VMSS</span></span>
```
PS C:\> Remove-AzVmssDiagnosticsExtension -VirtualMachineScaleSet $VMSS -Name $extName
```

<span data-ttu-id="56edb-109">此命令會從 VMSS 移除診斷擴充功能。</span><span class="sxs-lookup"><span data-stu-id="56edb-109">This command removes diagnostics extension from the VMSS.</span></span>

## <span data-ttu-id="56edb-110">參數</span><span class="sxs-lookup"><span data-stu-id="56edb-110">PARAMETERS</span></span>

### <span data-ttu-id="56edb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56edb-111">-DefaultProfile</span></span>
<span data-ttu-id="56edb-112">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="56edb-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="56edb-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="56edb-113">-Name</span></span>
<span data-ttu-id="56edb-114">指定此 Cmdlet 從 VMSS 移除的副檔名。</span><span class="sxs-lookup"><span data-stu-id="56edb-114">Specifies the name of the extension that this cmdlet removes from the VMSS.</span></span>

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

### <span data-ttu-id="56edb-115">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="56edb-115">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="56edb-116">指定要移除副檔名的 VMSS。</span><span class="sxs-lookup"><span data-stu-id="56edb-116">Specifies the VMSS from which to remove the extension.</span></span>

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

### <span data-ttu-id="56edb-117">-確認</span><span class="sxs-lookup"><span data-stu-id="56edb-117">-Confirm</span></span>
<span data-ttu-id="56edb-118">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="56edb-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56edb-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56edb-119">-WhatIf</span></span>
<span data-ttu-id="56edb-120">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="56edb-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="56edb-121">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="56edb-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56edb-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56edb-122">CommonParameters</span></span>
<span data-ttu-id="56edb-123">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="56edb-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56edb-124">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="56edb-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56edb-125">輸入</span><span class="sxs-lookup"><span data-stu-id="56edb-125">INPUTS</span></span>

### <span data-ttu-id="56edb-126">Microsoft.Azure.Commands.Compute.Automation.models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="56edb-126">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="56edb-127">System.String</span><span class="sxs-lookup"><span data-stu-id="56edb-127">System.String</span></span>

## <span data-ttu-id="56edb-128">輸出</span><span class="sxs-lookup"><span data-stu-id="56edb-128">OUTPUTS</span></span>

### <span data-ttu-id="56edb-129">Microsoft.Azure.Commands.Compute.Automation.models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="56edb-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="56edb-130">筆記</span><span class="sxs-lookup"><span data-stu-id="56edb-130">NOTES</span></span>

## <span data-ttu-id="56edb-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="56edb-131">RELATED LINKS</span></span>

[<span data-ttu-id="56edb-132">Add-AzEvssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="56edb-132">Add-AzVmssDiagnosticsExtension</span></span>](./Add-AzVmssDiagnosticsExtension.md)

[<span data-ttu-id="56edb-133">Remove-AzMSDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="56edb-133">Remove-AzVMDiagnosticsExtension</span></span>](./Remove-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="56edb-134">Remove-AzEvssExtension</span><span class="sxs-lookup"><span data-stu-id="56edb-134">Remove-AzVmssExtension</span></span>](./Remove-AzVmssExtension.md)


