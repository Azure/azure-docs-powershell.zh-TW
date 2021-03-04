---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/powershell/module/az.signalr/new-azsignalrkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/New-AzSignalRKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/New-AzSignalRKey.md
ms.openlocfilehash: a17f8e6457cc62799fdef3d3606e04962774fdac
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902790"
---
# <span data-ttu-id="4000a-101">New-AzSignalRKey</span><span class="sxs-lookup"><span data-stu-id="4000a-101">New-AzSignalRKey</span></span>

## <span data-ttu-id="4000a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="4000a-102">SYNOPSIS</span></span>
<span data-ttu-id="4000a-103">重新產生 SignalR 服務的便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="4000a-103">Regenerate an access key for a SignalR service.</span></span>

## <span data-ttu-id="4000a-104">語法</span><span class="sxs-lookup"><span data-stu-id="4000a-104">SYNTAX</span></span>

### <span data-ttu-id="4000a-105">ResourceGroupParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="4000a-105">ResourceGroupParameterSet (Default)</span></span>
```
New-AzSignalRKey [-ResourceGroupName <String>] [-Name] <String> [-KeyType] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4000a-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4000a-106">ResourceIdParameterSet</span></span>
```
New-AzSignalRKey -ResourceId <String> [-KeyType] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4000a-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4000a-107">InputObjectParameterSet</span></span>
```
New-AzSignalRKey -InputObject <PSSignalRResource> [-KeyType] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4000a-108">描述</span><span class="sxs-lookup"><span data-stu-id="4000a-108">DESCRIPTION</span></span>
<span data-ttu-id="4000a-109">重新產生 SignalR 服務的便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="4000a-109">Regenerate an access key for a SignalR service.</span></span>

## <span data-ttu-id="4000a-110">例子</span><span class="sxs-lookup"><span data-stu-id="4000a-110">EXAMPLES</span></span>

### <span data-ttu-id="4000a-111">重新產生主鍵</span><span class="sxs-lookup"><span data-stu-id="4000a-111">Regenerate the primary key</span></span>
```powershell
PS C:\> New-AzSignalRKey -ResourceGroupName myResourceGroup -Name mysignalr1 -KeyType Primary -PassThru

True
```

## <span data-ttu-id="4000a-112">參數</span><span class="sxs-lookup"><span data-stu-id="4000a-112">PARAMETERS</span></span>

### <span data-ttu-id="4000a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4000a-113">-DefaultProfile</span></span>
<span data-ttu-id="4000a-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="4000a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4000a-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4000a-115">-InputObject</span></span>
<span data-ttu-id="4000a-116">SignalR 資源物件。</span><span class="sxs-lookup"><span data-stu-id="4000a-116">The SignalR resource object.</span></span>

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

### <span data-ttu-id="4000a-117">-KeyType</span><span class="sxs-lookup"><span data-stu-id="4000a-117">-KeyType</span></span>
<span data-ttu-id="4000a-118">主鍵類型或次要鍵類型。</span><span class="sxs-lookup"><span data-stu-id="4000a-118">The key type, either Primary or Secondary.</span></span>

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

### <span data-ttu-id="4000a-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="4000a-119">-Name</span></span>
<span data-ttu-id="4000a-120">SignalR 服務名稱。</span><span class="sxs-lookup"><span data-stu-id="4000a-120">SignalR service name.</span></span>

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

### <span data-ttu-id="4000a-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4000a-121">-PassThru</span></span>
<span data-ttu-id="4000a-122">如果成功完成更新，則會返回 True。</span><span class="sxs-lookup"><span data-stu-id="4000a-122">Returns true if the regeneration was completed successfully.</span></span>

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

### <span data-ttu-id="4000a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4000a-123">-ResourceGroupName</span></span>
<span data-ttu-id="4000a-124">資源組名。</span><span class="sxs-lookup"><span data-stu-id="4000a-124">Resource group name.</span></span>

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

### <span data-ttu-id="4000a-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4000a-125">-ResourceId</span></span>
<span data-ttu-id="4000a-126">SignalR 服務資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="4000a-126">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="4000a-127">-確認</span><span class="sxs-lookup"><span data-stu-id="4000a-127">-Confirm</span></span>
<span data-ttu-id="4000a-128">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="4000a-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4000a-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4000a-129">-WhatIf</span></span>
<span data-ttu-id="4000a-130">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4000a-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4000a-131">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4000a-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4000a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4000a-132">CommonParameters</span></span>
<span data-ttu-id="4000a-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="4000a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4000a-134">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4000a-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4000a-135">輸入</span><span class="sxs-lookup"><span data-stu-id="4000a-135">INPUTS</span></span>

### <span data-ttu-id="4000a-136">System.String</span><span class="sxs-lookup"><span data-stu-id="4000a-136">System.String</span></span>
### <span data-ttu-id="4000a-137">Microsoft.Azure.Commands.SignalR.models.PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="4000a-137">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>
## <span data-ttu-id="4000a-138">輸出</span><span class="sxs-lookup"><span data-stu-id="4000a-138">OUTPUTS</span></span>

### <span data-ttu-id="4000a-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4000a-139">System.Boolean</span></span>
## <span data-ttu-id="4000a-140">筆記</span><span class="sxs-lookup"><span data-stu-id="4000a-140">NOTES</span></span>

## <span data-ttu-id="4000a-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="4000a-141">RELATED LINKS</span></span>
