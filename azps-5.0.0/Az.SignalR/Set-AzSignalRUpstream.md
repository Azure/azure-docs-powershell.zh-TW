---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/set-azsignalrupstream
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Set-AzSignalRUpstream.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Set-AzSignalRUpstream.md
ms.openlocfilehash: e04e87067f86f529117512e7443118f308b20547
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94287211"
---
# <span data-ttu-id="52d9a-101">Set-AzSignalRUpstream</span><span class="sxs-lookup"><span data-stu-id="52d9a-101">Set-AzSignalRUpstream</span></span>

## <span data-ttu-id="52d9a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="52d9a-102">SYNOPSIS</span></span>
<span data-ttu-id="52d9a-103">設定 SignalR 服務的上游設定。</span><span class="sxs-lookup"><span data-stu-id="52d9a-103">Set the upstream settings of a SignalR service.</span></span>

## <span data-ttu-id="52d9a-104">句法</span><span class="sxs-lookup"><span data-stu-id="52d9a-104">SYNTAX</span></span>

### <span data-ttu-id="52d9a-105">ResourceGroupParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="52d9a-105">ResourceGroupParameterSet (Default)</span></span>
```
Set-AzSignalRUpstream [-ResourceGroupName <String>] [-Name] <String> [-AsJob]
 [-Template <PSUpstreamTemplate[]>] [-Clear] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="52d9a-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="52d9a-106">ResourceIdParameterSet</span></span>
```
Set-AzSignalRUpstream -ResourceId <String> [-AsJob] [-Template <PSUpstreamTemplate[]>] [-Clear]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52d9a-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="52d9a-107">InputObjectParameterSet</span></span>
```
Set-AzSignalRUpstream -InputObject <PSSignalRResource> [-AsJob] [-Template <PSUpstreamTemplate[]>] [-Clear]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52d9a-108">說明</span><span class="sxs-lookup"><span data-stu-id="52d9a-108">DESCRIPTION</span></span>
<span data-ttu-id="52d9a-109">設定 SignalR 服務的上游設定。</span><span class="sxs-lookup"><span data-stu-id="52d9a-109">Set the upstream settings of a SignalR service.</span></span>

## <span data-ttu-id="52d9a-110">示例</span><span class="sxs-lookup"><span data-stu-id="52d9a-110">EXAMPLES</span></span>

### <span data-ttu-id="52d9a-111">設定兩個已排序的上游範本</span><span class="sxs-lookup"><span data-stu-id="52d9a-111">Set two ordered upstream templates</span></span>
```powershell
PS C:\>  Set-AzSignalRUpstream -name pssignalr -ResourceGroupName test_resource_group -Template @{UrlTemplate='http://host-connections1.com'; HubPattern='chat';EventPattern='broadcast' }, @{UrlTemplate='http://host-connections2.com'}

Templates
---------
{Microsoft.Azure.Commands.SignalR.Models.PSUpstreamTemplate, Microsoft.Azure.Commands.SignalR.Models.PSUpstreamTemplat…
```

<span data-ttu-id="52d9a-112">下列 JSON 代表實際的樣板集。</span><span class="sxs-lookup"><span data-stu-id="52d9a-112">The following JSON represents the actual templates set.</span></span> 

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

### <span data-ttu-id="52d9a-113">清除所有上游設定</span><span class="sxs-lookup"><span data-stu-id="52d9a-113">Clear all the upstream settings</span></span>
```powershell
PS C:\>  Set-AzSignalRUpstream -name pssignalr -ResourceGroupName test_resource_group -Clear

Templates
---------
{}
```

## <span data-ttu-id="52d9a-114">參數</span><span class="sxs-lookup"><span data-stu-id="52d9a-114">PARAMETERS</span></span>

### <span data-ttu-id="52d9a-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="52d9a-115">-AsJob</span></span>
<span data-ttu-id="52d9a-116">在背景作業中執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="52d9a-116">Run the cmdlet in background job.</span></span>

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

### <span data-ttu-id="52d9a-117">-Clear</span><span class="sxs-lookup"><span data-stu-id="52d9a-117">-Clear</span></span>
<span data-ttu-id="52d9a-118">清除所有上游設定。</span><span class="sxs-lookup"><span data-stu-id="52d9a-118">Clear all the upstream settings.</span></span>

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

### <span data-ttu-id="52d9a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52d9a-119">-DefaultProfile</span></span>
<span data-ttu-id="52d9a-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="52d9a-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52d9a-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="52d9a-121">-InputObject</span></span>
<span data-ttu-id="52d9a-122">SignalR 資源物件。</span><span class="sxs-lookup"><span data-stu-id="52d9a-122">The SignalR resource object.</span></span>

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

### <span data-ttu-id="52d9a-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="52d9a-123">-Name</span></span>
<span data-ttu-id="52d9a-124">SignalR 服務名稱。</span><span class="sxs-lookup"><span data-stu-id="52d9a-124">The SignalR service name.</span></span>

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

### <span data-ttu-id="52d9a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52d9a-125">-ResourceGroupName</span></span>
<span data-ttu-id="52d9a-126">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="52d9a-126">The resource group name.</span></span>
<span data-ttu-id="52d9a-127">如果沒有指定，則會使用預設值。</span><span class="sxs-lookup"><span data-stu-id="52d9a-127">The default one will be used if not specified.</span></span>

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

### <span data-ttu-id="52d9a-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="52d9a-128">-ResourceId</span></span>
<span data-ttu-id="52d9a-129">SignalR 服務資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="52d9a-129">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="52d9a-130">-範本</span><span class="sxs-lookup"><span data-stu-id="52d9a-130">-Template</span></span>
<span data-ttu-id="52d9a-131"> (s) 的 [上游設定] 範本專案。</span><span class="sxs-lookup"><span data-stu-id="52d9a-131">Template item(s) for upstream settings.</span></span>
<span data-ttu-id="52d9a-132">必要的金鑰： UrlTemplate。</span><span class="sxs-lookup"><span data-stu-id="52d9a-132">Required key: UrlTemplate.</span></span>
<span data-ttu-id="52d9a-133">選擇性鍵： HubPattern、EventPattern、CategoryPattern。</span><span class="sxs-lookup"><span data-stu-id="52d9a-133">Optional keys: HubPattern, EventPattern, CategoryPattern.</span></span>
<span data-ttu-id="52d9a-134">使用 splatting 語法來傳遞範本參數的範例： @ {UrlTemplate = ' http://host-connections1.com '，HubPattern = 「聊天」;EventPattern = "廣播"}，@ {UrlTemplate = ' http://host-connections2.com "}</span><span class="sxs-lookup"><span data-stu-id="52d9a-134">Example using splatting syntax to pass templates parameter: @{UrlTemplate='http://host-connections1.com', HubPattern= 'chat';EventPattern='broadcast' },@{UrlTemplate='http://host-connections2.com'}</span></span>

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

### <span data-ttu-id="52d9a-135">-確認</span><span class="sxs-lookup"><span data-stu-id="52d9a-135">-Confirm</span></span>
<span data-ttu-id="52d9a-136">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="52d9a-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52d9a-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52d9a-137">-WhatIf</span></span>
<span data-ttu-id="52d9a-138">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="52d9a-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52d9a-139">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="52d9a-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52d9a-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52d9a-140">CommonParameters</span></span>
<span data-ttu-id="52d9a-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="52d9a-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52d9a-142">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="52d9a-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52d9a-143">輸入</span><span class="sxs-lookup"><span data-stu-id="52d9a-143">INPUTS</span></span>

### <span data-ttu-id="52d9a-144">System.object</span><span class="sxs-lookup"><span data-stu-id="52d9a-144">System.String</span></span>

## <span data-ttu-id="52d9a-145">輸出</span><span class="sxs-lookup"><span data-stu-id="52d9a-145">OUTPUTS</span></span>

### <span data-ttu-id="52d9a-146">PSServerlessUpstreamSettings 中的 SignalR。</span><span class="sxs-lookup"><span data-stu-id="52d9a-146">Microsoft.Azure.Commands.SignalR.Models.PSServerlessUpstreamSettings</span></span>

## <span data-ttu-id="52d9a-147">筆記</span><span class="sxs-lookup"><span data-stu-id="52d9a-147">NOTES</span></span>

## <span data-ttu-id="52d9a-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="52d9a-148">RELATED LINKS</span></span>

[<span data-ttu-id="52d9a-149">如何在 PowerShell 中使用 splatting 將參數傳遞到命令</span><span class="sxs-lookup"><span data-stu-id="52d9a-149">How to use splatting to pass parameters to commands in PowerShell</span></span>](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.core/about/about_splatting?view=powershell-7)
