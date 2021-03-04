---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/powershell/module/az.signalr/remove-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Remove-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Remove-AzSignalR.md
ms.openlocfilehash: 067dd93f28a5019de96f146a237fe131a9717bfc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902789"
---
# <span data-ttu-id="7bae0-101">Remove-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="7bae0-101">Remove-AzSignalR</span></span>

## <span data-ttu-id="7bae0-102">簡介</span><span class="sxs-lookup"><span data-stu-id="7bae0-102">SYNOPSIS</span></span>
<span data-ttu-id="7bae0-103">移除 SignalR 服務。</span><span class="sxs-lookup"><span data-stu-id="7bae0-103">Remove a SignalR service.</span></span>

## <span data-ttu-id="7bae0-104">語法</span><span class="sxs-lookup"><span data-stu-id="7bae0-104">SYNTAX</span></span>

### <span data-ttu-id="7bae0-105">ResourceGroupParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="7bae0-105">ResourceGroupParameterSet (Default)</span></span>
```
Remove-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7bae0-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7bae0-106">ResourceIdParameterSet</span></span>
```
Remove-AzSignalR -ResourceId <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7bae0-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7bae0-107">InputObjectParameterSet</span></span>
```
Remove-AzSignalR -InputObject <PSSignalRResource> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7bae0-108">描述</span><span class="sxs-lookup"><span data-stu-id="7bae0-108">DESCRIPTION</span></span>
<span data-ttu-id="7bae0-109">移除 SignalR 服務。</span><span class="sxs-lookup"><span data-stu-id="7bae0-109">Remove a SignalR service.</span></span>

## <span data-ttu-id="7bae0-110">例子</span><span class="sxs-lookup"><span data-stu-id="7bae0-110">EXAMPLES</span></span>

### <span data-ttu-id="7bae0-111">移除 SignalR 服務</span><span class="sxs-lookup"><span data-stu-id="7bae0-111">Remove a SignalR service</span></span>
```
PS C:\> Remove-AzSignalR -ResourceGroupName myResourceGroup -Name mysignalr1 -PassThru

True
```

### <span data-ttu-id="7bae0-112">從管道移除所有 SignalR 服務</span><span class="sxs-lookup"><span data-stu-id="7bae0-112">Remove all SignalR service from pipe</span></span>
```
PS C:\> Get-AzSignalR -ResourceGroupName myResourceGroup | Remove-AzSignalR
```

## <span data-ttu-id="7bae0-113">參數</span><span class="sxs-lookup"><span data-stu-id="7bae0-113">PARAMETERS</span></span>

### <span data-ttu-id="7bae0-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7bae0-114">-AsJob</span></span>
<span data-ttu-id="7bae0-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="7bae0-115">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bae0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bae0-116">-DefaultProfile</span></span>
<span data-ttu-id="7bae0-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="7bae0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7bae0-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7bae0-118">-InputObject</span></span>
<span data-ttu-id="7bae0-119">SignalR 資源物件。</span><span class="sxs-lookup"><span data-stu-id="7bae0-119">The SignalR resource object.</span></span>

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

### <span data-ttu-id="7bae0-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="7bae0-120">-Name</span></span>
<span data-ttu-id="7bae0-121">SignalR 服務名稱。</span><span class="sxs-lookup"><span data-stu-id="7bae0-121">SignalR service name.</span></span>

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

### <span data-ttu-id="7bae0-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7bae0-122">-PassThru</span></span>
<span data-ttu-id="7bae0-123">如果移除已完成，則會返回 True。</span><span class="sxs-lookup"><span data-stu-id="7bae0-123">Returns true if the removal was completed successfully.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bae0-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7bae0-124">-ResourceGroupName</span></span>
<span data-ttu-id="7bae0-125">資源組名。</span><span class="sxs-lookup"><span data-stu-id="7bae0-125">Resource group name.</span></span>

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

### <span data-ttu-id="7bae0-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7bae0-126">-ResourceId</span></span>
<span data-ttu-id="7bae0-127">SignalR 服務資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="7bae0-127">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="7bae0-128">-確認</span><span class="sxs-lookup"><span data-stu-id="7bae0-128">-Confirm</span></span>
<span data-ttu-id="7bae0-129">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="7bae0-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7bae0-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7bae0-130">-WhatIf</span></span>
<span data-ttu-id="7bae0-131">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7bae0-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7bae0-132">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7bae0-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7bae0-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bae0-133">CommonParameters</span></span>
<span data-ttu-id="7bae0-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="7bae0-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bae0-135">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7bae0-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bae0-136">輸入</span><span class="sxs-lookup"><span data-stu-id="7bae0-136">INPUTS</span></span>

### <span data-ttu-id="7bae0-137">System.String</span><span class="sxs-lookup"><span data-stu-id="7bae0-137">System.String</span></span>
### <span data-ttu-id="7bae0-138">Microsoft.Azure.Commands.SignalR.models.PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="7bae0-138">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>
## <span data-ttu-id="7bae0-139">輸出</span><span class="sxs-lookup"><span data-stu-id="7bae0-139">OUTPUTS</span></span>

### <span data-ttu-id="7bae0-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7bae0-140">System.Boolean</span></span>
## <span data-ttu-id="7bae0-141">筆記</span><span class="sxs-lookup"><span data-stu-id="7bae0-141">NOTES</span></span>

## <span data-ttu-id="7bae0-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="7bae0-142">RELATED LINKS</span></span>
