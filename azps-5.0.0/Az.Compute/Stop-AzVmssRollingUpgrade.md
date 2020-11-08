---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/stop-azvmssrollingupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVmssRollingUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVmssRollingUpgrade.md
ms.openlocfilehash: 331f390890e6349c5a48f9b57c3d0e99fa972532
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94138217"
---
# <span data-ttu-id="afe1c-101">Stop-AzVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="afe1c-101">Stop-AzVmssRollingUpgrade</span></span>

## <span data-ttu-id="afe1c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="afe1c-102">SYNOPSIS</span></span>
<span data-ttu-id="afe1c-103">取消目前的虛擬機器縮放設定輪流升級。</span><span class="sxs-lookup"><span data-stu-id="afe1c-103">Cancels the current virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="afe1c-104">句法</span><span class="sxs-lookup"><span data-stu-id="afe1c-104">SYNTAX</span></span>

```
Stop-AzVmssRollingUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="afe1c-105">說明</span><span class="sxs-lookup"><span data-stu-id="afe1c-105">DESCRIPTION</span></span>
<span data-ttu-id="afe1c-106">取消目前的虛擬機器縮放設定輪流升級。</span><span class="sxs-lookup"><span data-stu-id="afe1c-106">Cancels the current virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="afe1c-107">示例</span><span class="sxs-lookup"><span data-stu-id="afe1c-107">EXAMPLES</span></span>

### <span data-ttu-id="afe1c-108">範例1</span><span class="sxs-lookup"><span data-stu-id="afe1c-108">Example 1</span></span>
```
PS C:\> Stop-AzVmssRollingUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="afe1c-109">這個命令會在資源群組 "Group001" 中，取消 VM 規模設定為 "VMSS001" 的正在進行中的輪流升級。</span><span class="sxs-lookup"><span data-stu-id="afe1c-109">This command cancels on-going rolling upgrade of VM scale set "VMSS001" in resource group "Group001".</span></span>

## <span data-ttu-id="afe1c-110">參數</span><span class="sxs-lookup"><span data-stu-id="afe1c-110">PARAMETERS</span></span>

### <span data-ttu-id="afe1c-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="afe1c-111">-AsJob</span></span>
<span data-ttu-id="afe1c-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="afe1c-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="afe1c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afe1c-113">-DefaultProfile</span></span>
<span data-ttu-id="afe1c-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="afe1c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="afe1c-115">-Force</span><span class="sxs-lookup"><span data-stu-id="afe1c-115">-Force</span></span>
<span data-ttu-id="afe1c-116">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="afe1c-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="afe1c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="afe1c-117">-ResourceGroupName</span></span>
<span data-ttu-id="afe1c-118">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="afe1c-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="afe1c-119">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="afe1c-119">-VMScaleSetName</span></span>
<span data-ttu-id="afe1c-120">VM 比例集的名稱。</span><span class="sxs-lookup"><span data-stu-id="afe1c-120">The name of the VM scale set.</span></span>

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

### <span data-ttu-id="afe1c-121">-確認</span><span class="sxs-lookup"><span data-stu-id="afe1c-121">-Confirm</span></span>
<span data-ttu-id="afe1c-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="afe1c-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="afe1c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="afe1c-123">-WhatIf</span></span>
<span data-ttu-id="afe1c-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="afe1c-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="afe1c-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="afe1c-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="afe1c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afe1c-126">CommonParameters</span></span>
<span data-ttu-id="afe1c-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="afe1c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afe1c-128">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="afe1c-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afe1c-129">輸入</span><span class="sxs-lookup"><span data-stu-id="afe1c-129">INPUTS</span></span>

### <span data-ttu-id="afe1c-130">System.object</span><span class="sxs-lookup"><span data-stu-id="afe1c-130">System.String</span></span>

## <span data-ttu-id="afe1c-131">輸出</span><span class="sxs-lookup"><span data-stu-id="afe1c-131">OUTPUTS</span></span>

### <span data-ttu-id="afe1c-132">PSOperationStatusResponse 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="afe1c-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="afe1c-133">筆記</span><span class="sxs-lookup"><span data-stu-id="afe1c-133">NOTES</span></span>

## <span data-ttu-id="afe1c-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="afe1c-134">RELATED LINKS</span></span>
