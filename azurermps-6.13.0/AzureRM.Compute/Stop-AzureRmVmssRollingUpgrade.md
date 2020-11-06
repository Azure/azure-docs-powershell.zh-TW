---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/stop-azurermvmssrollingupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Stop-AzureRmVmssRollingUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Stop-AzureRmVmssRollingUpgrade.md
ms.openlocfilehash: 92a3a98ba5e6743b5d52ad619501fd6ed56c10c6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447403"
---
# <span data-ttu-id="626a2-101">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="626a2-101">Stop-AzureRmVmssRollingUpgrade</span></span>

## <span data-ttu-id="626a2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="626a2-102">SYNOPSIS</span></span>
<span data-ttu-id="626a2-103">取消目前的虛擬機器縮放設定輪流升級。</span><span class="sxs-lookup"><span data-stu-id="626a2-103">Cancels the current virtual machine scale set rolling upgrade.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="626a2-104">句法</span><span class="sxs-lookup"><span data-stu-id="626a2-104">SYNTAX</span></span>

### <span data-ttu-id="626a2-105">DefaultParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="626a2-105">DefaultParameter (Default)</span></span>
```
Stop-AzureRmVmssRollingUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="626a2-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="626a2-106">FriendMethod</span></span>
```
Stop-AzureRmVmssRollingUpgrade [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="626a2-107">說明</span><span class="sxs-lookup"><span data-stu-id="626a2-107">DESCRIPTION</span></span>
<span data-ttu-id="626a2-108">取消目前的虛擬機器縮放設定輪流升級。</span><span class="sxs-lookup"><span data-stu-id="626a2-108">Cancels the current virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="626a2-109">示例</span><span class="sxs-lookup"><span data-stu-id="626a2-109">EXAMPLES</span></span>

### <span data-ttu-id="626a2-110">範例1</span><span class="sxs-lookup"><span data-stu-id="626a2-110">Example 1</span></span>
```
PS C:\> Stop-AzureRmVmssRollingUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="626a2-111">這個命令會在資源群組 "Group001" 中，取消 VM 規模設定為 "VMSS001" 的正在進行中的輪流升級。</span><span class="sxs-lookup"><span data-stu-id="626a2-111">This command cancels on-going rolling upgrade of VM scale set "VMSS001" in resource group "Group001".</span></span>

## <span data-ttu-id="626a2-112">參數</span><span class="sxs-lookup"><span data-stu-id="626a2-112">PARAMETERS</span></span>

### <span data-ttu-id="626a2-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="626a2-113">-AsJob</span></span>
<span data-ttu-id="626a2-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="626a2-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="626a2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="626a2-115">-DefaultProfile</span></span>
<span data-ttu-id="626a2-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="626a2-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="626a2-117">-Force</span><span class="sxs-lookup"><span data-stu-id="626a2-117">-Force</span></span>
<span data-ttu-id="626a2-118">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="626a2-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="626a2-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="626a2-119">-ResourceGroupName</span></span>
<span data-ttu-id="626a2-120">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="626a2-120">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="626a2-121">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="626a2-121">-VMScaleSetName</span></span>
<span data-ttu-id="626a2-122">VM 比例集的名稱。</span><span class="sxs-lookup"><span data-stu-id="626a2-122">The name of the VM scale set.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="626a2-123">-確認</span><span class="sxs-lookup"><span data-stu-id="626a2-123">-Confirm</span></span>
<span data-ttu-id="626a2-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="626a2-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="626a2-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="626a2-125">-WhatIf</span></span>
<span data-ttu-id="626a2-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="626a2-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="626a2-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="626a2-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="626a2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="626a2-128">CommonParameters</span></span>
<span data-ttu-id="626a2-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="626a2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="626a2-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="626a2-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="626a2-131">輸入</span><span class="sxs-lookup"><span data-stu-id="626a2-131">INPUTS</span></span>

### <span data-ttu-id="626a2-132">System.object</span><span class="sxs-lookup"><span data-stu-id="626a2-132">System.String</span></span>

## <span data-ttu-id="626a2-133">輸出</span><span class="sxs-lookup"><span data-stu-id="626a2-133">OUTPUTS</span></span>

### <span data-ttu-id="626a2-134">PSOperationStatusResponse 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="626a2-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="626a2-135">筆記</span><span class="sxs-lookup"><span data-stu-id="626a2-135">NOTES</span></span>

## <span data-ttu-id="626a2-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="626a2-136">RELATED LINKS</span></span>
