---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/start-azvmssrollingosupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Start-AzVmssRollingOSUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Start-AzVmssRollingOSUpgrade.md
ms.openlocfilehash: f3ebb13438d88a65e763d81936704db859bc1e97
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794842"
---
# <span data-ttu-id="79ab7-101">Start-AzVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="79ab7-101">Start-AzVmssRollingOSUpgrade</span></span>

## <span data-ttu-id="79ab7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="79ab7-102">SYNOPSIS</span></span>
<span data-ttu-id="79ab7-103">啟動 [輪流升級]，將所有虛擬機器規模集實例移至最新的可用平臺影像 OS 版本。</span><span class="sxs-lookup"><span data-stu-id="79ab7-103">Starts a rolling upgrade to move all virtual machine scale set instances to the latest available Platform Image OS version.</span></span>

## <span data-ttu-id="79ab7-104">句法</span><span class="sxs-lookup"><span data-stu-id="79ab7-104">SYNTAX</span></span>

```
Start-AzVmssRollingOSUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79ab7-105">說明</span><span class="sxs-lookup"><span data-stu-id="79ab7-105">DESCRIPTION</span></span>
<span data-ttu-id="79ab7-106">啟動 [輪流升級]，將所有虛擬機器規模集實例移至最新的可用平臺影像 OS 版本。</span><span class="sxs-lookup"><span data-stu-id="79ab7-106">Starts a rolling upgrade to move all virtual machine scale set instances to the latest available Platform Image OS version.</span></span>
<span data-ttu-id="79ab7-107">已執行最新可用 OS 版本的實例不會受到影響。</span><span class="sxs-lookup"><span data-stu-id="79ab7-107">Instances which are already running the latest available OS version are not affected.</span></span>

## <span data-ttu-id="79ab7-108">示例</span><span class="sxs-lookup"><span data-stu-id="79ab7-108">EXAMPLES</span></span>

### <span data-ttu-id="79ab7-109">範例1</span><span class="sxs-lookup"><span data-stu-id="79ab7-109">Example 1</span></span>
```
PS C:\> Start-AzVmssRollingOSUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="79ab7-110">這個命令會在資源群組 "Group001" 中啟動 VM 規模集 "VMSS001" 的所有 vm 實例的輪流升級。</span><span class="sxs-lookup"><span data-stu-id="79ab7-110">This command starts a rolling upgrade of all vm instances of VM scale set "VMSS001" in resource group "Group001".</span></span>

## <span data-ttu-id="79ab7-111">參數</span><span class="sxs-lookup"><span data-stu-id="79ab7-111">PARAMETERS</span></span>

### <span data-ttu-id="79ab7-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="79ab7-112">-AsJob</span></span>
<span data-ttu-id="79ab7-113">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="79ab7-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="79ab7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79ab7-114">-DefaultProfile</span></span>
<span data-ttu-id="79ab7-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="79ab7-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="79ab7-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79ab7-116">-ResourceGroupName</span></span>
<span data-ttu-id="79ab7-117">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="79ab7-117">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79ab7-118">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="79ab7-118">-VMScaleSetName</span></span>
<span data-ttu-id="79ab7-119">VM 比例集的名稱。</span><span class="sxs-lookup"><span data-stu-id="79ab7-119">The name of the VM scale set.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79ab7-120">-確認</span><span class="sxs-lookup"><span data-stu-id="79ab7-120">-Confirm</span></span>
<span data-ttu-id="79ab7-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="79ab7-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79ab7-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79ab7-122">-WhatIf</span></span>
<span data-ttu-id="79ab7-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="79ab7-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79ab7-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="79ab7-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79ab7-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79ab7-125">CommonParameters</span></span>
<span data-ttu-id="79ab7-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="79ab7-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79ab7-127">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="79ab7-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79ab7-128">輸入</span><span class="sxs-lookup"><span data-stu-id="79ab7-128">INPUTS</span></span>

### <span data-ttu-id="79ab7-129">System.object</span><span class="sxs-lookup"><span data-stu-id="79ab7-129">System.String</span></span>

## <span data-ttu-id="79ab7-130">輸出</span><span class="sxs-lookup"><span data-stu-id="79ab7-130">OUTPUTS</span></span>

### <span data-ttu-id="79ab7-131">PSOperationStatusResponse 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="79ab7-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="79ab7-132">筆記</span><span class="sxs-lookup"><span data-stu-id="79ab7-132">NOTES</span></span>

## <span data-ttu-id="79ab7-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="79ab7-133">RELATED LINKS</span></span>

