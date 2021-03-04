---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/start-azvmssrollingosupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVmssRollingOSUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVmssRollingOSUpgrade.md
ms.openlocfilehash: fb3d6f08eaa540e208830a15563b8edd8c2432ee
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904534"
---
# <span data-ttu-id="00ff3-101">Start-AzVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="00ff3-101">Start-AzVmssRollingOSUpgrade</span></span>

## <span data-ttu-id="00ff3-102">簡介</span><span class="sxs-lookup"><span data-stu-id="00ff3-102">SYNOPSIS</span></span>
<span data-ttu-id="00ff3-103">開始進行輪流升級，以將所有虛擬機器縮放比例集實例移至最新可用的平臺映射作業系統版本。</span><span class="sxs-lookup"><span data-stu-id="00ff3-103">Starts a rolling upgrade to move all virtual machine scale set instances to the latest available Platform Image OS version.</span></span>

## <span data-ttu-id="00ff3-104">語法</span><span class="sxs-lookup"><span data-stu-id="00ff3-104">SYNTAX</span></span>

```
Start-AzVmssRollingOSUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="00ff3-105">描述</span><span class="sxs-lookup"><span data-stu-id="00ff3-105">DESCRIPTION</span></span>
<span data-ttu-id="00ff3-106">開始進行輪流升級，以將所有虛擬機器縮放比例集實例移至最新可用的平臺映射作業系統版本。</span><span class="sxs-lookup"><span data-stu-id="00ff3-106">Starts a rolling upgrade to move all virtual machine scale set instances to the latest available Platform Image OS version.</span></span>
<span data-ttu-id="00ff3-107">已使用最新可用作業系統版本的實例不會受到影響。</span><span class="sxs-lookup"><span data-stu-id="00ff3-107">Instances which are already running the latest available OS version are not affected.</span></span>

## <span data-ttu-id="00ff3-108">例子</span><span class="sxs-lookup"><span data-stu-id="00ff3-108">EXAMPLES</span></span>

### <span data-ttu-id="00ff3-109">範例 1</span><span class="sxs-lookup"><span data-stu-id="00ff3-109">Example 1</span></span>
```
PS C:\> Start-AzVmssRollingOSUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="00ff3-110">此命令會開始對資源群組 "Group001" 中 VM 縮放集 "VMSS001" 的所有 vm 實例進行輪流升級。</span><span class="sxs-lookup"><span data-stu-id="00ff3-110">This command starts a rolling upgrade of all vm instances of VM scale set "VMSS001" in resource group "Group001".</span></span>

## <span data-ttu-id="00ff3-111">參數</span><span class="sxs-lookup"><span data-stu-id="00ff3-111">PARAMETERS</span></span>

### <span data-ttu-id="00ff3-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="00ff3-112">-AsJob</span></span>
<span data-ttu-id="00ff3-113">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="00ff3-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="00ff3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00ff3-114">-DefaultProfile</span></span>
<span data-ttu-id="00ff3-115">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="00ff3-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="00ff3-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00ff3-116">-ResourceGroupName</span></span>
<span data-ttu-id="00ff3-117">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="00ff3-117">The name of the resource group.</span></span>

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

### <span data-ttu-id="00ff3-118">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="00ff3-118">-VMScaleSetName</span></span>
<span data-ttu-id="00ff3-119">VM 縮放集的名稱。</span><span class="sxs-lookup"><span data-stu-id="00ff3-119">The name of the VM scale set.</span></span>

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

### <span data-ttu-id="00ff3-120">-確認</span><span class="sxs-lookup"><span data-stu-id="00ff3-120">-Confirm</span></span>
<span data-ttu-id="00ff3-121">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="00ff3-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00ff3-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00ff3-122">-WhatIf</span></span>
<span data-ttu-id="00ff3-123">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="00ff3-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="00ff3-124">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="00ff3-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="00ff3-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00ff3-125">CommonParameters</span></span>
<span data-ttu-id="00ff3-126">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="00ff3-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00ff3-127">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="00ff3-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00ff3-128">輸入</span><span class="sxs-lookup"><span data-stu-id="00ff3-128">INPUTS</span></span>

### <span data-ttu-id="00ff3-129">System.String</span><span class="sxs-lookup"><span data-stu-id="00ff3-129">System.String</span></span>

## <span data-ttu-id="00ff3-130">輸出</span><span class="sxs-lookup"><span data-stu-id="00ff3-130">OUTPUTS</span></span>

### <span data-ttu-id="00ff3-131">Microsoft.Azure.Commands.Compute.Automation.models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="00ff3-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="00ff3-132">筆記</span><span class="sxs-lookup"><span data-stu-id="00ff3-132">NOTES</span></span>

## <span data-ttu-id="00ff3-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="00ff3-133">RELATED LINKS</span></span>
