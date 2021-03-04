---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/powershell/module/az.signalr/restart-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Restart-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Restart-AzSignalR.md
ms.openlocfilehash: c98b716f37fcf9aafafacdefad4c51b0451cf12d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902786"
---
# <span data-ttu-id="a8ff2-101">Restart-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="a8ff2-101">Restart-AzSignalR</span></span>

## <span data-ttu-id="a8ff2-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a8ff2-102">SYNOPSIS</span></span>
<span data-ttu-id="a8ff2-103">重新開機 SignalR 服務。</span><span class="sxs-lookup"><span data-stu-id="a8ff2-103">Restart a SignalR service.</span></span>

## <span data-ttu-id="a8ff2-104">語法</span><span class="sxs-lookup"><span data-stu-id="a8ff2-104">SYNTAX</span></span>

### <span data-ttu-id="a8ff2-105">ResourceGroupParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="a8ff2-105">ResourceGroupParameterSet (Default)</span></span>
```
Restart-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8ff2-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a8ff2-106">ResourceIdParameterSet</span></span>
```
Restart-AzSignalR -ResourceId <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8ff2-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a8ff2-107">InputObjectParameterSet</span></span>
```
Restart-AzSignalR -InputObject <PSSignalRResource> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a8ff2-108">描述</span><span class="sxs-lookup"><span data-stu-id="a8ff2-108">DESCRIPTION</span></span>
<span data-ttu-id="a8ff2-109">重新開機 SignalR 服務。</span><span class="sxs-lookup"><span data-stu-id="a8ff2-109">Restart a SignalR service.</span></span>

## <span data-ttu-id="a8ff2-110">例子</span><span class="sxs-lookup"><span data-stu-id="a8ff2-110">EXAMPLES</span></span>

### <span data-ttu-id="a8ff2-111">重新開機特定的 SignalR 服務</span><span class="sxs-lookup"><span data-stu-id="a8ff2-111">Restart a specific SignalR service</span></span>
```powershell
PS C:\> Restart-AzSignalR -ResourceGroupName myResourceGroup -Name mysignalr1 -PassThru

True
```

<span data-ttu-id="a8ff2-112">預設資源群組可以設定為 \` Set-AzDefault -ResourceGroupName myResourceGroup。 \`</span><span class="sxs-lookup"><span data-stu-id="a8ff2-112">The default resource group can be set by \`Set-AzDefault -ResourceGroupName myResourceGroup\`.</span></span>

## <span data-ttu-id="a8ff2-113">參數</span><span class="sxs-lookup"><span data-stu-id="a8ff2-113">PARAMETERS</span></span>

### <span data-ttu-id="a8ff2-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a8ff2-114">-AsJob</span></span>
<span data-ttu-id="a8ff2-115">在背景工作中執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a8ff2-115">Run the cmdlet in background job.</span></span>

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

### <span data-ttu-id="a8ff2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8ff2-116">-DefaultProfile</span></span>
<span data-ttu-id="a8ff2-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a8ff2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a8ff2-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a8ff2-118">-InputObject</span></span>
<span data-ttu-id="a8ff2-119">SignalR 資源物件。</span><span class="sxs-lookup"><span data-stu-id="a8ff2-119">The SignalR resource object.</span></span>

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

### <span data-ttu-id="a8ff2-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="a8ff2-120">-Name</span></span>
<span data-ttu-id="a8ff2-121">SignalR 服務名稱。</span><span class="sxs-lookup"><span data-stu-id="a8ff2-121">The SignalR service name.</span></span>

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

### <span data-ttu-id="a8ff2-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a8ff2-122">-PassThru</span></span>
<span data-ttu-id="a8ff2-123">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="a8ff2-123">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="a8ff2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8ff2-124">-ResourceGroupName</span></span>
<span data-ttu-id="a8ff2-125">資源組名。</span><span class="sxs-lookup"><span data-stu-id="a8ff2-125">The resource group name.</span></span>
<span data-ttu-id="a8ff2-126">如果沒有指定，將會使用預設選項。</span><span class="sxs-lookup"><span data-stu-id="a8ff2-126">The default one will be used if not specified.</span></span>

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

### <span data-ttu-id="a8ff2-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a8ff2-127">-ResourceId</span></span>
<span data-ttu-id="a8ff2-128">SignalR 服務資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="a8ff2-128">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="a8ff2-129">-確認</span><span class="sxs-lookup"><span data-stu-id="a8ff2-129">-Confirm</span></span>
<span data-ttu-id="a8ff2-130">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="a8ff2-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8ff2-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8ff2-131">-WhatIf</span></span>
<span data-ttu-id="a8ff2-132">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a8ff2-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8ff2-133">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a8ff2-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8ff2-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8ff2-134">CommonParameters</span></span>
<span data-ttu-id="a8ff2-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a8ff2-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8ff2-136">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a8ff2-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8ff2-137">輸入</span><span class="sxs-lookup"><span data-stu-id="a8ff2-137">INPUTS</span></span>

### <span data-ttu-id="a8ff2-138">System.String</span><span class="sxs-lookup"><span data-stu-id="a8ff2-138">System.String</span></span>

### <span data-ttu-id="a8ff2-139">Microsoft.Azure.Commands.SignalR.models.PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="a8ff2-139">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="a8ff2-140">輸出</span><span class="sxs-lookup"><span data-stu-id="a8ff2-140">OUTPUTS</span></span>

### <span data-ttu-id="a8ff2-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a8ff2-141">System.Boolean</span></span>

## <span data-ttu-id="a8ff2-142">筆記</span><span class="sxs-lookup"><span data-stu-id="a8ff2-142">NOTES</span></span>

## <span data-ttu-id="a8ff2-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="a8ff2-143">RELATED LINKS</span></span>
