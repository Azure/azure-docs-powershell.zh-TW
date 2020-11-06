---
external help file: Microsoft.Azure.Commands.SignalR.dll-Help.xml
Module Name: AzureRM.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.signalr/new-azurermsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SignalR/Commands.SignalR/help/Remove-AzureRmSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SignalR/Commands.SignalR/help/Remove-AzureRmSignalR.md
ms.openlocfilehash: 5fcf62e592ed1e842c3dc6f4be21462170c4f83b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449718"
---
# <span data-ttu-id="5b5da-101">Remove-AzureRmSignalR</span><span class="sxs-lookup"><span data-stu-id="5b5da-101">Remove-AzureRmSignalR</span></span>

## <span data-ttu-id="5b5da-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5b5da-102">SYNOPSIS</span></span>
<span data-ttu-id="5b5da-103">移除 SignalR 服務。</span><span class="sxs-lookup"><span data-stu-id="5b5da-103">Remove a SignalR service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5b5da-104">句法</span><span class="sxs-lookup"><span data-stu-id="5b5da-104">SYNTAX</span></span>

### <span data-ttu-id="5b5da-105">ResourceGroupParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="5b5da-105">ResourceGroupParameterSet (Default)</span></span>
```
Remove-AzureRmSignalR [-ResourceGroupName <String>] [-Name] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b5da-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5b5da-106">ResourceIdParameterSet</span></span>
```
Remove-AzureRmSignalR -ResourceId <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b5da-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5b5da-107">InputObjectParameterSet</span></span>
```
Remove-AzureRmSignalR -InputObject <PSSignalRResource> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5b5da-108">說明</span><span class="sxs-lookup"><span data-stu-id="5b5da-108">DESCRIPTION</span></span>
<span data-ttu-id="5b5da-109">移除 SignalR 服務。</span><span class="sxs-lookup"><span data-stu-id="5b5da-109">Remove a SignalR service.</span></span>

## <span data-ttu-id="5b5da-110">示例</span><span class="sxs-lookup"><span data-stu-id="5b5da-110">EXAMPLES</span></span>

### <span data-ttu-id="5b5da-111">移除 SignalR 服務</span><span class="sxs-lookup"><span data-stu-id="5b5da-111">Remove a SignalR service</span></span>
```powershell
PS C:\> Remove-AzureRmSignalR -ResourceGroupName myResourceGroup -Name mysignalr1 -PassThru

True
```

### <span data-ttu-id="5b5da-112">從管道中移除所有 SignalR 服務</span><span class="sxs-lookup"><span data-stu-id="5b5da-112">Remove all SignalR service from pipe</span></span>
```powershell
PS C:\> Get-AzureRmSignalR -ResourceGroupName myResourceGroup | Remove-AzureRmSignalR
```

## <span data-ttu-id="5b5da-113">參數</span><span class="sxs-lookup"><span data-stu-id="5b5da-113">PARAMETERS</span></span>

### <span data-ttu-id="5b5da-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5b5da-114">-AsJob</span></span>
<span data-ttu-id="5b5da-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5b5da-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5b5da-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b5da-116">-DefaultProfile</span></span>
<span data-ttu-id="5b5da-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5b5da-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b5da-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5b5da-118">-InputObject</span></span>
<span data-ttu-id="5b5da-119">SignalR 資源物件。</span><span class="sxs-lookup"><span data-stu-id="5b5da-119">The SignalR resource object.</span></span>

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

### <span data-ttu-id="5b5da-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="5b5da-120">-Name</span></span>
<span data-ttu-id="5b5da-121">SignalR 服務名稱。</span><span class="sxs-lookup"><span data-stu-id="5b5da-121">SignalR service name.</span></span>

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

### <span data-ttu-id="5b5da-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5b5da-122">-PassThru</span></span>
<span data-ttu-id="5b5da-123">如果移除成功完成，則傳回 true。</span><span class="sxs-lookup"><span data-stu-id="5b5da-123">Returns true if the removal was completed successfully.</span></span>

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

### <span data-ttu-id="5b5da-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b5da-124">-ResourceGroupName</span></span>
<span data-ttu-id="5b5da-125">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="5b5da-125">Resource group name.</span></span>

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

### <span data-ttu-id="5b5da-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5b5da-126">-ResourceId</span></span>
<span data-ttu-id="5b5da-127">SignalR 服務資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="5b5da-127">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="5b5da-128">-確認</span><span class="sxs-lookup"><span data-stu-id="5b5da-128">-Confirm</span></span>
<span data-ttu-id="5b5da-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5b5da-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b5da-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b5da-130">-WhatIf</span></span>
<span data-ttu-id="5b5da-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5b5da-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5b5da-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5b5da-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b5da-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b5da-133">CommonParameters</span></span>
<span data-ttu-id="5b5da-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5b5da-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b5da-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5b5da-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b5da-136">輸入</span><span class="sxs-lookup"><span data-stu-id="5b5da-136">INPUTS</span></span>

### <span data-ttu-id="5b5da-137">System.object</span><span class="sxs-lookup"><span data-stu-id="5b5da-137">System.String</span></span>
<span data-ttu-id="5b5da-138">參數： ResourceId (ByValue) </span><span class="sxs-lookup"><span data-stu-id="5b5da-138">Parameters: ResourceId (ByValue)</span></span>

### <span data-ttu-id="5b5da-139">PSSignalRResource 中的 SignalR。</span><span class="sxs-lookup"><span data-stu-id="5b5da-139">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>
<span data-ttu-id="5b5da-140">參數： InputObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="5b5da-140">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="5b5da-141">輸出</span><span class="sxs-lookup"><span data-stu-id="5b5da-141">OUTPUTS</span></span>

### <span data-ttu-id="5b5da-142">System.object</span><span class="sxs-lookup"><span data-stu-id="5b5da-142">System.Boolean</span></span>

## <span data-ttu-id="5b5da-143">筆記</span><span class="sxs-lookup"><span data-stu-id="5b5da-143">NOTES</span></span>

## <span data-ttu-id="5b5da-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="5b5da-144">RELATED LINKS</span></span>