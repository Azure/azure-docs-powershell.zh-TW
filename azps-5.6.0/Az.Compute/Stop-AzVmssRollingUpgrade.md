---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/stop-azvmssrollingupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVmssRollingUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVmssRollingUpgrade.md
ms.openlocfilehash: 0371dd5ba008089ff8d8731e0ebb30e6b3caf8fe
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909742"
---
# <span data-ttu-id="666b4-101">Stop-AzVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="666b4-101">Stop-AzVmssRollingUpgrade</span></span>

## <span data-ttu-id="666b4-102">簡介</span><span class="sxs-lookup"><span data-stu-id="666b4-102">SYNOPSIS</span></span>
<span data-ttu-id="666b4-103">取消目前的虛擬機器規模集輪流升級。</span><span class="sxs-lookup"><span data-stu-id="666b4-103">Cancels the current virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="666b4-104">語法</span><span class="sxs-lookup"><span data-stu-id="666b4-104">SYNTAX</span></span>

```
Stop-AzVmssRollingUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="666b4-105">描述</span><span class="sxs-lookup"><span data-stu-id="666b4-105">DESCRIPTION</span></span>
<span data-ttu-id="666b4-106">取消目前的虛擬機器規模集輪流升級。</span><span class="sxs-lookup"><span data-stu-id="666b4-106">Cancels the current virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="666b4-107">例子</span><span class="sxs-lookup"><span data-stu-id="666b4-107">EXAMPLES</span></span>

### <span data-ttu-id="666b4-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="666b4-108">Example 1</span></span>
```
PS C:\> Stop-AzVmssRollingUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="666b4-109">此命令會取消資源群組 "Group001" 中 VM 縮放集 "VMSS001" 的繼續輪流升級。</span><span class="sxs-lookup"><span data-stu-id="666b4-109">This command cancels on-going rolling upgrade of VM scale set "VMSS001" in resource group "Group001".</span></span>

## <span data-ttu-id="666b4-110">參數</span><span class="sxs-lookup"><span data-stu-id="666b4-110">PARAMETERS</span></span>

### <span data-ttu-id="666b4-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="666b4-111">-AsJob</span></span>
<span data-ttu-id="666b4-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="666b4-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="666b4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="666b4-113">-DefaultProfile</span></span>
<span data-ttu-id="666b4-114">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="666b4-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="666b4-115">-強制</span><span class="sxs-lookup"><span data-stu-id="666b4-115">-Force</span></span>
<span data-ttu-id="666b4-116">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="666b4-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="666b4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="666b4-117">-ResourceGroupName</span></span>
<span data-ttu-id="666b4-118">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="666b4-118">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="666b4-119">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="666b4-119">-VMScaleSetName</span></span>
<span data-ttu-id="666b4-120">VM 縮放集的名稱。</span><span class="sxs-lookup"><span data-stu-id="666b4-120">The name of the VM scale set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="666b4-121">-確認</span><span class="sxs-lookup"><span data-stu-id="666b4-121">-Confirm</span></span>
<span data-ttu-id="666b4-122">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="666b4-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="666b4-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="666b4-123">-WhatIf</span></span>
<span data-ttu-id="666b4-124">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="666b4-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="666b4-125">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="666b4-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="666b4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="666b4-126">CommonParameters</span></span>
<span data-ttu-id="666b4-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="666b4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="666b4-128">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="666b4-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="666b4-129">輸入</span><span class="sxs-lookup"><span data-stu-id="666b4-129">INPUTS</span></span>

### <span data-ttu-id="666b4-130">System.String</span><span class="sxs-lookup"><span data-stu-id="666b4-130">System.String</span></span>

## <span data-ttu-id="666b4-131">輸出</span><span class="sxs-lookup"><span data-stu-id="666b4-131">OUTPUTS</span></span>

### <span data-ttu-id="666b4-132">Microsoft.Azure.Commands.Compute.Automation.models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="666b4-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="666b4-133">筆記</span><span class="sxs-lookup"><span data-stu-id="666b4-133">NOTES</span></span>

## <span data-ttu-id="666b4-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="666b4-134">RELATED LINKS</span></span>
