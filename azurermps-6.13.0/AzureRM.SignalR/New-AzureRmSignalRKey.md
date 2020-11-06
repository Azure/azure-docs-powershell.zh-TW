---
external help file: Microsoft.Azure.Commands.SignalR.dll-Help.xml
Module Name: AzureRM.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.signalr/new-azurermsignalrkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SignalR/Commands.SignalR/help/New-AzureRmSignalRKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SignalR/Commands.SignalR/help/New-AzureRmSignalRKey.md
ms.openlocfilehash: 4b4f3a416ece999641570a33101a3e7ab201ca3b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449720"
---
# <span data-ttu-id="5b1e7-101">New-AzureRmSignalRKey</span><span class="sxs-lookup"><span data-stu-id="5b1e7-101">New-AzureRmSignalRKey</span></span>

## <span data-ttu-id="5b1e7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5b1e7-102">SYNOPSIS</span></span>
<span data-ttu-id="5b1e7-103">重新產生 SignalR 服務的便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="5b1e7-103">Regenerate an access key for a SignalR service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5b1e7-104">句法</span><span class="sxs-lookup"><span data-stu-id="5b1e7-104">SYNTAX</span></span>

### <span data-ttu-id="5b1e7-105">ResourceGroupParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="5b1e7-105">ResourceGroupParameterSet (Default)</span></span>
```
New-AzureRmSignalRKey [-ResourceGroupName <String>] [-Name] <String> [-KeyType] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b1e7-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5b1e7-106">ResourceIdParameterSet</span></span>
```
New-AzureRmSignalRKey -ResourceId <String> [-KeyType] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b1e7-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5b1e7-107">InputObjectParameterSet</span></span>
```
New-AzureRmSignalRKey -InputObject <PSSignalRResource> [-KeyType] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5b1e7-108">說明</span><span class="sxs-lookup"><span data-stu-id="5b1e7-108">DESCRIPTION</span></span>
<span data-ttu-id="5b1e7-109">重新產生 SignalR 服務的便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="5b1e7-109">Regenerate an access key for a SignalR service.</span></span>

## <span data-ttu-id="5b1e7-110">示例</span><span class="sxs-lookup"><span data-stu-id="5b1e7-110">EXAMPLES</span></span>

### <span data-ttu-id="5b1e7-111">重新產生主鍵</span><span class="sxs-lookup"><span data-stu-id="5b1e7-111">Regenerate the primary key</span></span>
```powershell
PS C:\> New-AzureRmSignalRKey -ResourceGroupName myResourceGroup -Name mysignalr1 -KeyType Primary -PassThru

True
```

## <span data-ttu-id="5b1e7-112">參數</span><span class="sxs-lookup"><span data-stu-id="5b1e7-112">PARAMETERS</span></span>

### <span data-ttu-id="5b1e7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b1e7-113">-DefaultProfile</span></span>
<span data-ttu-id="5b1e7-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5b1e7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b1e7-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5b1e7-115">-InputObject</span></span>
<span data-ttu-id="5b1e7-116">SignalR 資源物件。</span><span class="sxs-lookup"><span data-stu-id="5b1e7-116">The SignalR resource object.</span></span>

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

### <span data-ttu-id="5b1e7-117">-KeyType</span><span class="sxs-lookup"><span data-stu-id="5b1e7-117">-KeyType</span></span>
<span data-ttu-id="5b1e7-118">金鑰類型，主要是 [主要] 或 [次要]。</span><span class="sxs-lookup"><span data-stu-id="5b1e7-118">The key type, either Primary or Secondary.</span></span>

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

### <span data-ttu-id="5b1e7-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="5b1e7-119">-Name</span></span>
<span data-ttu-id="5b1e7-120">SignalR 服務名稱。</span><span class="sxs-lookup"><span data-stu-id="5b1e7-120">SignalR service name.</span></span>

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

### <span data-ttu-id="5b1e7-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5b1e7-121">-PassThru</span></span>
<span data-ttu-id="5b1e7-122">如果重新再生已順利完成，則傳回 true。</span><span class="sxs-lookup"><span data-stu-id="5b1e7-122">Returns true if the regeneration was completed successfully.</span></span>

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

### <span data-ttu-id="5b1e7-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b1e7-123">-ResourceGroupName</span></span>
<span data-ttu-id="5b1e7-124">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="5b1e7-124">Resource group name.</span></span>

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

### <span data-ttu-id="5b1e7-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5b1e7-125">-ResourceId</span></span>
<span data-ttu-id="5b1e7-126">SignalR 服務資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="5b1e7-126">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="5b1e7-127">-確認</span><span class="sxs-lookup"><span data-stu-id="5b1e7-127">-Confirm</span></span>
<span data-ttu-id="5b1e7-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5b1e7-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b1e7-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b1e7-129">-WhatIf</span></span>
<span data-ttu-id="5b1e7-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5b1e7-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5b1e7-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5b1e7-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b1e7-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b1e7-132">CommonParameters</span></span>
<span data-ttu-id="5b1e7-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5b1e7-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b1e7-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5b1e7-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b1e7-135">輸入</span><span class="sxs-lookup"><span data-stu-id="5b1e7-135">INPUTS</span></span>

### <span data-ttu-id="5b1e7-136">System.object</span><span class="sxs-lookup"><span data-stu-id="5b1e7-136">System.String</span></span>
<span data-ttu-id="5b1e7-137">參數： ResourceId (ByValue) </span><span class="sxs-lookup"><span data-stu-id="5b1e7-137">Parameters: ResourceId (ByValue)</span></span>

### <span data-ttu-id="5b1e7-138">PSSignalRResource 中的 SignalR。</span><span class="sxs-lookup"><span data-stu-id="5b1e7-138">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>
<span data-ttu-id="5b1e7-139">參數： InputObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="5b1e7-139">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="5b1e7-140">輸出</span><span class="sxs-lookup"><span data-stu-id="5b1e7-140">OUTPUTS</span></span>

### <span data-ttu-id="5b1e7-141">System.object</span><span class="sxs-lookup"><span data-stu-id="5b1e7-141">System.Boolean</span></span>

## <span data-ttu-id="5b1e7-142">筆記</span><span class="sxs-lookup"><span data-stu-id="5b1e7-142">NOTES</span></span>

## <span data-ttu-id="5b1e7-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="5b1e7-143">RELATED LINKS</span></span>
