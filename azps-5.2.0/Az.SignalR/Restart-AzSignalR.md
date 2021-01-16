---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/restart-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Restart-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Restart-AzSignalR.md
ms.openlocfilehash: ea5de8ddd36d315381d4f60ee0fa1ce7dc49adc2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98278598"
---
# <span data-ttu-id="ae83e-101">Restart-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="ae83e-101">Restart-AzSignalR</span></span>

## <span data-ttu-id="ae83e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ae83e-102">SYNOPSIS</span></span>
<span data-ttu-id="ae83e-103">重新開機 SignalR 服務。</span><span class="sxs-lookup"><span data-stu-id="ae83e-103">Restart a SignalR service.</span></span>

## <span data-ttu-id="ae83e-104">句法</span><span class="sxs-lookup"><span data-stu-id="ae83e-104">SYNTAX</span></span>

### <span data-ttu-id="ae83e-105">ResourceGroupParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="ae83e-105">ResourceGroupParameterSet (Default)</span></span>
```
Restart-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae83e-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ae83e-106">ResourceIdParameterSet</span></span>
```
Restart-AzSignalR -ResourceId <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae83e-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ae83e-107">InputObjectParameterSet</span></span>
```
Restart-AzSignalR -InputObject <PSSignalRResource> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae83e-108">說明</span><span class="sxs-lookup"><span data-stu-id="ae83e-108">DESCRIPTION</span></span>
<span data-ttu-id="ae83e-109">重新開機 SignalR 服務。</span><span class="sxs-lookup"><span data-stu-id="ae83e-109">Restart a SignalR service.</span></span>

## <span data-ttu-id="ae83e-110">示例</span><span class="sxs-lookup"><span data-stu-id="ae83e-110">EXAMPLES</span></span>

### <span data-ttu-id="ae83e-111">重新開機特定的 SignalR 服務</span><span class="sxs-lookup"><span data-stu-id="ae83e-111">Restart a specific SignalR service</span></span>
```powershell
PS C:\> Restart-AzSignalR -ResourceGroupName myResourceGroup -Name mysignalr1 -PassThru

True
```

<span data-ttu-id="ae83e-112">預設的資源群組可以由 \` AzDefault-ResourceGroupName myResourceGroup 進行設定 \` 。</span><span class="sxs-lookup"><span data-stu-id="ae83e-112">The default resource group can be set by \`Set-AzDefault -ResourceGroupName myResourceGroup\`.</span></span>

## <span data-ttu-id="ae83e-113">參數</span><span class="sxs-lookup"><span data-stu-id="ae83e-113">PARAMETERS</span></span>

### <span data-ttu-id="ae83e-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ae83e-114">-AsJob</span></span>
<span data-ttu-id="ae83e-115">在背景作業中執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ae83e-115">Run the cmdlet in background job.</span></span>

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

### <span data-ttu-id="ae83e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae83e-116">-DefaultProfile</span></span>
<span data-ttu-id="ae83e-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ae83e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae83e-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ae83e-118">-InputObject</span></span>
<span data-ttu-id="ae83e-119">SignalR 資源物件。</span><span class="sxs-lookup"><span data-stu-id="ae83e-119">The SignalR resource object.</span></span>

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

### <span data-ttu-id="ae83e-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="ae83e-120">-Name</span></span>
<span data-ttu-id="ae83e-121">SignalR 服務名稱。</span><span class="sxs-lookup"><span data-stu-id="ae83e-121">The SignalR service name.</span></span>

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

### <span data-ttu-id="ae83e-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ae83e-122">-PassThru</span></span>
<span data-ttu-id="ae83e-123">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="ae83e-123">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="ae83e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae83e-124">-ResourceGroupName</span></span>
<span data-ttu-id="ae83e-125">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ae83e-125">The resource group name.</span></span>
<span data-ttu-id="ae83e-126">如果沒有指定，則會使用預設值。</span><span class="sxs-lookup"><span data-stu-id="ae83e-126">The default one will be used if not specified.</span></span>

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

### <span data-ttu-id="ae83e-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ae83e-127">-ResourceId</span></span>
<span data-ttu-id="ae83e-128">SignalR 服務資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="ae83e-128">The SignalR service resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae83e-129">-確認</span><span class="sxs-lookup"><span data-stu-id="ae83e-129">-Confirm</span></span>
<span data-ttu-id="ae83e-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ae83e-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae83e-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae83e-131">-WhatIf</span></span>
<span data-ttu-id="ae83e-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ae83e-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae83e-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ae83e-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae83e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae83e-134">CommonParameters</span></span>
<span data-ttu-id="ae83e-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ae83e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae83e-136">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ae83e-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae83e-137">輸入</span><span class="sxs-lookup"><span data-stu-id="ae83e-137">INPUTS</span></span>

### <span data-ttu-id="ae83e-138">System.object</span><span class="sxs-lookup"><span data-stu-id="ae83e-138">System.String</span></span>

### <span data-ttu-id="ae83e-139">PSSignalRResource 中的 SignalR。</span><span class="sxs-lookup"><span data-stu-id="ae83e-139">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="ae83e-140">輸出</span><span class="sxs-lookup"><span data-stu-id="ae83e-140">OUTPUTS</span></span>

### <span data-ttu-id="ae83e-141">System.object</span><span class="sxs-lookup"><span data-stu-id="ae83e-141">System.Boolean</span></span>

## <span data-ttu-id="ae83e-142">筆記</span><span class="sxs-lookup"><span data-stu-id="ae83e-142">NOTES</span></span>

## <span data-ttu-id="ae83e-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="ae83e-143">RELATED LINKS</span></span>
