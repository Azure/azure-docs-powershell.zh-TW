---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/stop-azurermvmssrollingupgrade
schema: 2.0.0
ms.openlocfilehash: 8893f5fc8f6bf798635fdfd5e9a16bc4179815e7
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93802542"
---
# <span data-ttu-id="2af2c-101">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="2af2c-101">Stop-AzureRmVmssRollingUpgrade</span></span>

## <span data-ttu-id="2af2c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2af2c-102">SYNOPSIS</span></span>
<span data-ttu-id="2af2c-103">取消目前的虛擬機器縮放設定輪流升級。</span><span class="sxs-lookup"><span data-stu-id="2af2c-103">Cancels the current virtual machine scale set rolling upgrade.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2af2c-104">句法</span><span class="sxs-lookup"><span data-stu-id="2af2c-104">SYNTAX</span></span>

### <span data-ttu-id="2af2c-105">DefaultParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="2af2c-105">DefaultParameter (Default)</span></span>
```
Stop-AzureRmVmssRollingUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2af2c-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="2af2c-106">FriendMethod</span></span>
```
Stop-AzureRmVmssRollingUpgrade [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2af2c-107">說明</span><span class="sxs-lookup"><span data-stu-id="2af2c-107">DESCRIPTION</span></span>
<span data-ttu-id="2af2c-108">取消目前的虛擬機器縮放設定輪流升級。</span><span class="sxs-lookup"><span data-stu-id="2af2c-108">Cancels the current virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="2af2c-109">示例</span><span class="sxs-lookup"><span data-stu-id="2af2c-109">EXAMPLES</span></span>

### <span data-ttu-id="2af2c-110">範例1</span><span class="sxs-lookup"><span data-stu-id="2af2c-110">Example 1</span></span>
```
PS C:\> Stop-AzureRmVmssRollingUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="2af2c-111">這個命令會在資源群組 "Group001" 中，取消 VM 規模設定為 "VMSS001" 的正在進行中的輪流升級。</span><span class="sxs-lookup"><span data-stu-id="2af2c-111">This command cancels on-going rolling upgrade of VM scale set "VMSS001" in resource group "Group001".</span></span>

## <span data-ttu-id="2af2c-112">參數</span><span class="sxs-lookup"><span data-stu-id="2af2c-112">PARAMETERS</span></span>

### <span data-ttu-id="2af2c-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2af2c-113">-AsJob</span></span>
<span data-ttu-id="2af2c-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="2af2c-114">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2af2c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2af2c-115">-DefaultProfile</span></span>
<span data-ttu-id="2af2c-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2af2c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2af2c-117">-Force</span><span class="sxs-lookup"><span data-stu-id="2af2c-117">-Force</span></span>
<span data-ttu-id="2af2c-118">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="2af2c-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2af2c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2af2c-119">-ResourceGroupName</span></span>
<span data-ttu-id="2af2c-120">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2af2c-120">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2af2c-121">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="2af2c-121">-VMScaleSetName</span></span>
<span data-ttu-id="2af2c-122">VM 比例集的名稱。</span><span class="sxs-lookup"><span data-stu-id="2af2c-122">The name of the VM scale set.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2af2c-123">-確認</span><span class="sxs-lookup"><span data-stu-id="2af2c-123">-Confirm</span></span>
<span data-ttu-id="2af2c-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2af2c-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2af2c-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2af2c-125">-WhatIf</span></span>
<span data-ttu-id="2af2c-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2af2c-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2af2c-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2af2c-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2af2c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2af2c-128">CommonParameters</span></span>
<span data-ttu-id="2af2c-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2af2c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2af2c-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2af2c-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2af2c-131">輸入</span><span class="sxs-lookup"><span data-stu-id="2af2c-131">INPUTS</span></span>

### <span data-ttu-id="2af2c-132">System.object</span><span class="sxs-lookup"><span data-stu-id="2af2c-132">System.String</span></span>

## <span data-ttu-id="2af2c-133">輸出</span><span class="sxs-lookup"><span data-stu-id="2af2c-133">OUTPUTS</span></span>

### <span data-ttu-id="2af2c-134">PSOperationStatusResponse 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="2af2c-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="2af2c-135">筆記</span><span class="sxs-lookup"><span data-stu-id="2af2c-135">NOTES</span></span>

## <span data-ttu-id="2af2c-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="2af2c-136">RELATED LINKS</span></span>

