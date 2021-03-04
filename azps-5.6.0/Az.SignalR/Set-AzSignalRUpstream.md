---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/powershell/module/az.signalr/set-azsignalrupstream
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Set-AzSignalRUpstream.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Set-AzSignalRUpstream.md
ms.openlocfilehash: 7fde7a8f40efaee9cbf3011e844ee8a48e3949a4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902765"
---
# <span data-ttu-id="a56c0-101">Set-AzSignalRUpstream</span><span class="sxs-lookup"><span data-stu-id="a56c0-101">Set-AzSignalRUpstream</span></span>

## <span data-ttu-id="a56c0-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a56c0-102">SYNOPSIS</span></span>
<span data-ttu-id="a56c0-103">設定 SignalR 服務的行流設定。</span><span class="sxs-lookup"><span data-stu-id="a56c0-103">Set the upstream settings of a SignalR service.</span></span>

## <span data-ttu-id="a56c0-104">語法</span><span class="sxs-lookup"><span data-stu-id="a56c0-104">SYNTAX</span></span>

### <span data-ttu-id="a56c0-105">ResourceGroupParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="a56c0-105">ResourceGroupParameterSet (Default)</span></span>
```
Set-AzSignalRUpstream [-ResourceGroupName <String>] [-Name] <String> [-AsJob]
 [-Template <PSUpstreamTemplate[]>] [-Clear] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a56c0-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a56c0-106">ResourceIdParameterSet</span></span>
```
Set-AzSignalRUpstream -ResourceId <String> [-AsJob] [-Template <PSUpstreamTemplate[]>] [-Clear]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a56c0-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a56c0-107">InputObjectParameterSet</span></span>
```
Set-AzSignalRUpstream -InputObject <PSSignalRResource> [-AsJob] [-Template <PSUpstreamTemplate[]>] [-Clear]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a56c0-108">描述</span><span class="sxs-lookup"><span data-stu-id="a56c0-108">DESCRIPTION</span></span>
<span data-ttu-id="a56c0-109">設定 SignalR 服務的行流設定。</span><span class="sxs-lookup"><span data-stu-id="a56c0-109">Set the upstream settings of a SignalR service.</span></span>

## <span data-ttu-id="a56c0-110">例子</span><span class="sxs-lookup"><span data-stu-id="a56c0-110">EXAMPLES</span></span>

### <span data-ttu-id="a56c0-111">設定兩個排序的下游範本</span><span class="sxs-lookup"><span data-stu-id="a56c0-111">Set two ordered upstream templates</span></span>
```powershell
PS C:\>  Set-AzSignalRUpstream -name pssignalr -ResourceGroupName test_resource_group -Template @{UrlTemplate='http://host-connections1.com'; HubPattern='chat';EventPattern='broadcast' }, @{UrlTemplate='http://host-connections2.com'}

Templates
---------
{Microsoft.Azure.Commands.SignalR.Models.PSUpstreamTemplate, Microsoft.Azure.Commands.SignalR.Models.PSUpstreamTemplat…
```

<span data-ttu-id="a56c0-112">下列 JSON 代表實際樣板集。</span><span class="sxs-lookup"><span data-stu-id="a56c0-112">The following JSON represents the actual templates set.</span></span> 

 `
{
    "hubPattern": "chat",
    "eventPattern": "broadcast",
    "categoryPattern": "*",
    "urlTemplate": "http://host-connections1.com"
},
{
    "hubPattern": "*",
    "eventPattern": "*",
    "categoryPattern": "*",
    "urlTemplate": "http://host-connections2.com"
}
`

### <span data-ttu-id="a56c0-113">清除所有上流設定</span><span class="sxs-lookup"><span data-stu-id="a56c0-113">Clear all the upstream settings</span></span>
```powershell
PS C:\>  Set-AzSignalRUpstream -name pssignalr -ResourceGroupName test_resource_group -Clear

Templates
---------
{}
```

## <span data-ttu-id="a56c0-114">參數</span><span class="sxs-lookup"><span data-stu-id="a56c0-114">PARAMETERS</span></span>

### <span data-ttu-id="a56c0-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a56c0-115">-AsJob</span></span>
<span data-ttu-id="a56c0-116">在背景工作中執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a56c0-116">Run the cmdlet in background job.</span></span>

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

### <span data-ttu-id="a56c0-117">-清除</span><span class="sxs-lookup"><span data-stu-id="a56c0-117">-Clear</span></span>
<span data-ttu-id="a56c0-118">清除所有上流設定。</span><span class="sxs-lookup"><span data-stu-id="a56c0-118">Clear all the upstream settings.</span></span>

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

### <span data-ttu-id="a56c0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a56c0-119">-DefaultProfile</span></span>
<span data-ttu-id="a56c0-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a56c0-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a56c0-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a56c0-121">-InputObject</span></span>
<span data-ttu-id="a56c0-122">SignalR 資源物件。</span><span class="sxs-lookup"><span data-stu-id="a56c0-122">The SignalR resource object.</span></span>

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

### <span data-ttu-id="a56c0-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="a56c0-123">-Name</span></span>
<span data-ttu-id="a56c0-124">SignalR 服務名稱。</span><span class="sxs-lookup"><span data-stu-id="a56c0-124">The SignalR service name.</span></span>

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

### <span data-ttu-id="a56c0-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a56c0-125">-ResourceGroupName</span></span>
<span data-ttu-id="a56c0-126">資源組名。</span><span class="sxs-lookup"><span data-stu-id="a56c0-126">The resource group name.</span></span>
<span data-ttu-id="a56c0-127">如果沒有指定，將會使用預設選項。</span><span class="sxs-lookup"><span data-stu-id="a56c0-127">The default one will be used if not specified.</span></span>

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

### <span data-ttu-id="a56c0-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a56c0-128">-ResourceId</span></span>
<span data-ttu-id="a56c0-129">SignalR 服務資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="a56c0-129">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="a56c0-130">-範本</span><span class="sxs-lookup"><span data-stu-id="a56c0-130">-Template</span></span>
<span data-ttu-id="a56c0-131">範本專案 () 設定。</span><span class="sxs-lookup"><span data-stu-id="a56c0-131">Template item(s) for upstream settings.</span></span>
<span data-ttu-id="a56c0-132">必要的金鑰：UrlTemplate。</span><span class="sxs-lookup"><span data-stu-id="a56c0-132">Required key: UrlTemplate.</span></span>
<span data-ttu-id="a56c0-133">選擇性鍵：HubPattern、EventPattern、CategoryPattern。</span><span class="sxs-lookup"><span data-stu-id="a56c0-133">Optional keys: HubPattern, EventPattern, CategoryPattern.</span></span>
<span data-ttu-id="a56c0-134">使用 splatting 語法傳遞 templates 參數的範例：@{UrlTemplate=' http://host-connections1.com '， HubPattern= 'chat';EventPattern='broadcast' }，@{UrlTemplate=' http://host-connections2.com '}</span><span class="sxs-lookup"><span data-stu-id="a56c0-134">Example using splatting syntax to pass templates parameter: @{UrlTemplate='http://host-connections1.com', HubPattern= 'chat';EventPattern='broadcast' },@{UrlTemplate='http://host-connections2.com'}</span></span>

```yaml
Type: Microsoft.Azure.Commands.SignalR.Models.PSUpstreamTemplate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a56c0-135">-確認</span><span class="sxs-lookup"><span data-stu-id="a56c0-135">-Confirm</span></span>
<span data-ttu-id="a56c0-136">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="a56c0-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a56c0-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a56c0-137">-WhatIf</span></span>
<span data-ttu-id="a56c0-138">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a56c0-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a56c0-139">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a56c0-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a56c0-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a56c0-140">CommonParameters</span></span>
<span data-ttu-id="a56c0-141">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a56c0-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a56c0-142">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a56c0-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a56c0-143">輸入</span><span class="sxs-lookup"><span data-stu-id="a56c0-143">INPUTS</span></span>

### <span data-ttu-id="a56c0-144">System.String</span><span class="sxs-lookup"><span data-stu-id="a56c0-144">System.String</span></span>

## <span data-ttu-id="a56c0-145">輸出</span><span class="sxs-lookup"><span data-stu-id="a56c0-145">OUTPUTS</span></span>

### <span data-ttu-id="a56c0-146">Microsoft.Azure.Commands.SignalR.models.PSServerlessUpstreamSettings</span><span class="sxs-lookup"><span data-stu-id="a56c0-146">Microsoft.Azure.Commands.SignalR.Models.PSServerlessUpstreamSettings</span></span>

## <span data-ttu-id="a56c0-147">筆記</span><span class="sxs-lookup"><span data-stu-id="a56c0-147">NOTES</span></span>

## <span data-ttu-id="a56c0-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="a56c0-148">RELATED LINKS</span></span>

[<span data-ttu-id="a56c0-149">如何使用 Splatting 將參數傳遞到 PowerShell 中的命令</span><span class="sxs-lookup"><span data-stu-id="a56c0-149">How to use splatting to pass parameters to commands in PowerShell</span></span>](https://docs.microsoft.com/powershell/module/microsoft.powershell.core/about/about_splatting?view=powershell-7)
