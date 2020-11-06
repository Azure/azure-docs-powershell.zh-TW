---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/remove-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Remove-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Remove-AzSignalR.md
ms.openlocfilehash: 6096bb59622e873d100752646ae6c101b43923e4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93620533"
---
# <span data-ttu-id="c042c-101">Remove-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="c042c-101">Remove-AzSignalR</span></span>

## <span data-ttu-id="c042c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c042c-102">SYNOPSIS</span></span>
<span data-ttu-id="c042c-103">移除 SignalR 服務。</span><span class="sxs-lookup"><span data-stu-id="c042c-103">Remove a SignalR service.</span></span>

## <span data-ttu-id="c042c-104">句法</span><span class="sxs-lookup"><span data-stu-id="c042c-104">SYNTAX</span></span>

### <span data-ttu-id="c042c-105">ResourceGroupParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="c042c-105">ResourceGroupParameterSet (Default)</span></span>
```
Remove-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c042c-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c042c-106">ResourceIdParameterSet</span></span>
```
Remove-AzSignalR -ResourceId <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c042c-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c042c-107">InputObjectParameterSet</span></span>
```
Remove-AzSignalR -InputObject <PSSignalRResource> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c042c-108">說明</span><span class="sxs-lookup"><span data-stu-id="c042c-108">DESCRIPTION</span></span>
<span data-ttu-id="c042c-109">移除 SignalR 服務。</span><span class="sxs-lookup"><span data-stu-id="c042c-109">Remove a SignalR service.</span></span>

## <span data-ttu-id="c042c-110">示例</span><span class="sxs-lookup"><span data-stu-id="c042c-110">EXAMPLES</span></span>

### <span data-ttu-id="c042c-111">移除 SignalR 服務</span><span class="sxs-lookup"><span data-stu-id="c042c-111">Remove a SignalR service</span></span>
```powershell
PS C:\> Remove-AzSignalR -ResourceGroupName myResourceGroup -Name mysignalr1 -PassThru

True
```

### <span data-ttu-id="c042c-112">從管道中移除所有 SignalR 服務</span><span class="sxs-lookup"><span data-stu-id="c042c-112">Remove all SignalR service from pipe</span></span>
```powershell
PS C:\> Get-AzSignalR -ResourceGroupName myResourceGroup | Remove-AzSignalR
```

## <span data-ttu-id="c042c-113">參數</span><span class="sxs-lookup"><span data-stu-id="c042c-113">PARAMETERS</span></span>

### <span data-ttu-id="c042c-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c042c-114">-AsJob</span></span>
<span data-ttu-id="c042c-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c042c-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c042c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c042c-116">-DefaultProfile</span></span>
<span data-ttu-id="c042c-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c042c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c042c-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c042c-118">-InputObject</span></span>
<span data-ttu-id="c042c-119">SignalR 資源物件。</span><span class="sxs-lookup"><span data-stu-id="c042c-119">The SignalR resource object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c042c-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="c042c-120">-Name</span></span>
<span data-ttu-id="c042c-121">SignalR 服務名稱。</span><span class="sxs-lookup"><span data-stu-id="c042c-121">SignalR service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c042c-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c042c-122">-PassThru</span></span>
<span data-ttu-id="c042c-123">如果移除成功完成，則傳回 true。</span><span class="sxs-lookup"><span data-stu-id="c042c-123">Returns true if the removal was completed successfully.</span></span>

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

### <span data-ttu-id="c042c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c042c-124">-ResourceGroupName</span></span>
<span data-ttu-id="c042c-125">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="c042c-125">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c042c-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c042c-126">-ResourceId</span></span>
<span data-ttu-id="c042c-127">SignalR 服務資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="c042c-127">The SignalR service resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c042c-128">-確認</span><span class="sxs-lookup"><span data-stu-id="c042c-128">-Confirm</span></span>
<span data-ttu-id="c042c-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c042c-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c042c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c042c-130">-WhatIf</span></span>
<span data-ttu-id="c042c-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c042c-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c042c-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c042c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c042c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c042c-133">CommonParameters</span></span>
<span data-ttu-id="c042c-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c042c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c042c-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c042c-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c042c-136">輸入</span><span class="sxs-lookup"><span data-stu-id="c042c-136">INPUTS</span></span>

### <span data-ttu-id="c042c-137">System.object</span><span class="sxs-lookup"><span data-stu-id="c042c-137">System.String</span></span>

### <span data-ttu-id="c042c-138">PSSignalRResource 中的 SignalR。</span><span class="sxs-lookup"><span data-stu-id="c042c-138">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="c042c-139">輸出</span><span class="sxs-lookup"><span data-stu-id="c042c-139">OUTPUTS</span></span>

### <span data-ttu-id="c042c-140">System.object</span><span class="sxs-lookup"><span data-stu-id="c042c-140">System.Boolean</span></span>

## <span data-ttu-id="c042c-141">筆記</span><span class="sxs-lookup"><span data-stu-id="c042c-141">NOTES</span></span>

## <span data-ttu-id="c042c-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="c042c-142">RELATED LINKS</span></span>
