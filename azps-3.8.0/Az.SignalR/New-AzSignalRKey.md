---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/new-azsignalrkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/New-AzSignalRKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/New-AzSignalRKey.md
ms.openlocfilehash: 9c27342a073f33a52881376037fc8d3a5d7e8bb1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93957229"
---
# <span data-ttu-id="b72c9-101">New-AzSignalRKey</span><span class="sxs-lookup"><span data-stu-id="b72c9-101">New-AzSignalRKey</span></span>

## <span data-ttu-id="b72c9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b72c9-102">SYNOPSIS</span></span>
<span data-ttu-id="b72c9-103">重新產生 SignalR 服務的便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="b72c9-103">Regenerate an access key for a SignalR service.</span></span>

## <span data-ttu-id="b72c9-104">句法</span><span class="sxs-lookup"><span data-stu-id="b72c9-104">SYNTAX</span></span>

### <span data-ttu-id="b72c9-105">ResourceGroupParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="b72c9-105">ResourceGroupParameterSet (Default)</span></span>
```
New-AzSignalRKey [-ResourceGroupName <String>] [-Name] <String> [-KeyType] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b72c9-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b72c9-106">ResourceIdParameterSet</span></span>
```
New-AzSignalRKey -ResourceId <String> [-KeyType] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b72c9-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b72c9-107">InputObjectParameterSet</span></span>
```
New-AzSignalRKey -InputObject <PSSignalRResource> [-KeyType] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b72c9-108">說明</span><span class="sxs-lookup"><span data-stu-id="b72c9-108">DESCRIPTION</span></span>
<span data-ttu-id="b72c9-109">重新產生 SignalR 服務的便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="b72c9-109">Regenerate an access key for a SignalR service.</span></span>

## <span data-ttu-id="b72c9-110">示例</span><span class="sxs-lookup"><span data-stu-id="b72c9-110">EXAMPLES</span></span>

### <span data-ttu-id="b72c9-111">重新產生主鍵</span><span class="sxs-lookup"><span data-stu-id="b72c9-111">Regenerate the primary key</span></span>
```powershell
PS C:\> New-AzSignalRKey -ResourceGroupName myResourceGroup -Name mysignalr1 -KeyType Primary -PassThru

True
```

## <span data-ttu-id="b72c9-112">參數</span><span class="sxs-lookup"><span data-stu-id="b72c9-112">PARAMETERS</span></span>

### <span data-ttu-id="b72c9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b72c9-113">-DefaultProfile</span></span>
<span data-ttu-id="b72c9-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b72c9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b72c9-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b72c9-115">-InputObject</span></span>
<span data-ttu-id="b72c9-116">SignalR 資源物件。</span><span class="sxs-lookup"><span data-stu-id="b72c9-116">The SignalR resource object.</span></span>

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

### <span data-ttu-id="b72c9-117">-KeyType</span><span class="sxs-lookup"><span data-stu-id="b72c9-117">-KeyType</span></span>
<span data-ttu-id="b72c9-118">金鑰類型，主要是 [主要] 或 [次要]。</span><span class="sxs-lookup"><span data-stu-id="b72c9-118">The key type, either Primary or Secondary.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b72c9-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="b72c9-119">-Name</span></span>
<span data-ttu-id="b72c9-120">SignalR 服務名稱。</span><span class="sxs-lookup"><span data-stu-id="b72c9-120">SignalR service name.</span></span>

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

### <span data-ttu-id="b72c9-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b72c9-121">-PassThru</span></span>
<span data-ttu-id="b72c9-122">如果重新再生已順利完成，則傳回 true。</span><span class="sxs-lookup"><span data-stu-id="b72c9-122">Returns true if the regeneration was completed successfully.</span></span>

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

### <span data-ttu-id="b72c9-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b72c9-123">-ResourceGroupName</span></span>
<span data-ttu-id="b72c9-124">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="b72c9-124">Resource group name.</span></span>

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

### <span data-ttu-id="b72c9-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b72c9-125">-ResourceId</span></span>
<span data-ttu-id="b72c9-126">SignalR 服務資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="b72c9-126">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="b72c9-127">-確認</span><span class="sxs-lookup"><span data-stu-id="b72c9-127">-Confirm</span></span>
<span data-ttu-id="b72c9-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b72c9-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b72c9-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b72c9-129">-WhatIf</span></span>
<span data-ttu-id="b72c9-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b72c9-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b72c9-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b72c9-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b72c9-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b72c9-132">CommonParameters</span></span>
<span data-ttu-id="b72c9-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b72c9-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b72c9-134">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b72c9-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b72c9-135">輸入</span><span class="sxs-lookup"><span data-stu-id="b72c9-135">INPUTS</span></span>

### <span data-ttu-id="b72c9-136">System.object</span><span class="sxs-lookup"><span data-stu-id="b72c9-136">System.String</span></span>
### <span data-ttu-id="b72c9-137">PSSignalRResource 中的 SignalR。</span><span class="sxs-lookup"><span data-stu-id="b72c9-137">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>
## <span data-ttu-id="b72c9-138">輸出</span><span class="sxs-lookup"><span data-stu-id="b72c9-138">OUTPUTS</span></span>

### <span data-ttu-id="b72c9-139">System.object</span><span class="sxs-lookup"><span data-stu-id="b72c9-139">System.Boolean</span></span>
## <span data-ttu-id="b72c9-140">筆記</span><span class="sxs-lookup"><span data-stu-id="b72c9-140">NOTES</span></span>

## <span data-ttu-id="b72c9-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="b72c9-141">RELATED LINKS</span></span>
