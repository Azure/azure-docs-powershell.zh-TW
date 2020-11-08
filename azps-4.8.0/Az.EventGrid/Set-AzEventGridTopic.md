---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/set-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Set-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Set-AzEventGridTopic.md
ms.openlocfilehash: 6a6b373fcbe38aac7e4e8d3972206955942eb18e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94136422"
---
# <span data-ttu-id="8da60-101">Set-AzEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="8da60-101">Set-AzEventGridTopic</span></span>

## <span data-ttu-id="8da60-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8da60-102">SYNOPSIS</span></span>
<span data-ttu-id="8da60-103">設定事件格線主題的屬性。</span><span class="sxs-lookup"><span data-stu-id="8da60-103">Sets the properties of an Event Grid topic.</span></span>

## <span data-ttu-id="8da60-104">句法</span><span class="sxs-lookup"><span data-stu-id="8da60-104">SYNTAX</span></span>

### <span data-ttu-id="8da60-105">TopicNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="8da60-105">TopicNameParameterSet (Default)</span></span>
```
Set-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-Tag] <Hashtable>
 [-InboundIpRule] <Hashtable> [-PublicNetworkAccess] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8da60-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="8da60-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Set-AzEventGridTopic [-ResourceId] <String> [-Tag] <Hashtable> [-InboundIpRule] <Hashtable>
 [-PublicNetworkAccess] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8da60-107">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8da60-107">TopicInputObjectParameterSet</span></span>
```
Set-AzEventGridTopic [-InputObject] <PSTopic> [[-Tag] <Hashtable>] [[-InboundIpRule] <Hashtable>]
 [[-PublicNetworkAccess] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8da60-108">說明</span><span class="sxs-lookup"><span data-stu-id="8da60-108">DESCRIPTION</span></span>
<span data-ttu-id="8da60-109">設定事件格線主題的屬性。</span><span class="sxs-lookup"><span data-stu-id="8da60-109">Sets the properties of an Event Grid topic.</span></span> <span data-ttu-id="8da60-110">這可以用來取代事件格線主題的標記。</span><span class="sxs-lookup"><span data-stu-id="8da60-110">This can be used to replace the tags of an Event Grid topic.</span></span>

## <span data-ttu-id="8da60-111">示例</span><span class="sxs-lookup"><span data-stu-id="8da60-111">EXAMPLES</span></span>

### <span data-ttu-id="8da60-112">範例1</span><span class="sxs-lookup"><span data-stu-id="8da60-112">Example 1</span></span>
```powershell
PS C:\> Set-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 -Tag @{ Department="Finance"; Environment="Test" }
```

<span data-ttu-id="8da60-113">設定 [資源群組 MyResourceGroupName] 中 Topic1 事件格線主題的屬性 \` \` \` \` ，以使用指定的標記「部門」和「環境」取代標記。</span><span class="sxs-lookup"><span data-stu-id="8da60-113">Sets the properties of the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\` to replace the tags with the specified tags "Department" and "Environment".</span></span>

## <span data-ttu-id="8da60-114">參數</span><span class="sxs-lookup"><span data-stu-id="8da60-114">PARAMETERS</span></span>

### <span data-ttu-id="8da60-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8da60-115">-DefaultProfile</span></span>
<span data-ttu-id="8da60-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="8da60-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8da60-117">-InboundIpRule</span><span class="sxs-lookup"><span data-stu-id="8da60-117">-InboundIpRule</span></span>
<span data-ttu-id="8da60-118">代表入站 IP 規則清單的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="8da60-118">Hashtable which represents list of inbound IP rules.</span></span> <span data-ttu-id="8da60-119">每個規則都指定 CIDR 符號中的 IP 位址（例如 10.0.0.0/8），以及根據 IpMask 的 match 或不符合的專案來執行對應的動作。</span><span class="sxs-lookup"><span data-stu-id="8da60-119">Each rule specifies the IP Address in CIDR notation e.g., 10.0.0.0/8 along with the corresponding Action to be performed based on the match or no match of the IpMask.</span></span> <span data-ttu-id="8da60-120">可能的動作值包括 [只允許]</span><span class="sxs-lookup"><span data-stu-id="8da60-120">Possible Action values include Allow only</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: TopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Hashtable
Parameter Sets: TopicInputObjectParameterSet
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8da60-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8da60-121">-InputObject</span></span>
<span data-ttu-id="8da60-122">EventGrid 主題物件。</span><span class="sxs-lookup"><span data-stu-id="8da60-122">EventGrid Topic object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSTopic
Parameter Sets: TopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8da60-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="8da60-123">-Name</span></span>
<span data-ttu-id="8da60-124">EventGrid 主題名稱。</span><span class="sxs-lookup"><span data-stu-id="8da60-124">EventGrid Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: TopicName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8da60-125">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="8da60-125">-PublicNetworkAccess</span></span>
<span data-ttu-id="8da60-126">這會判斷是否允許透過公用網路進行通訊。</span><span class="sxs-lookup"><span data-stu-id="8da60-126">This determines if traffic is allowed over public network.</span></span> <span data-ttu-id="8da60-127">預設為啟用。</span><span class="sxs-lookup"><span data-stu-id="8da60-127">By default it is enabled.</span></span> <span data-ttu-id="8da60-128">您可以設定 InboundIpRule 參數，進一步限制特定的 Ip。</span><span class="sxs-lookup"><span data-stu-id="8da60-128">You can further restrict to specific IPs by configuring InboundIpRule parameters.</span></span> <span data-ttu-id="8da60-129">允許的值已停用且已啟用。</span><span class="sxs-lookup"><span data-stu-id="8da60-129">Allowed values are disabled and enabled.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:
Accepted values: enabled, disabled

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: TopicInputObjectParameterSet
Aliases:
Accepted values: enabled, disabled

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8da60-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8da60-130">-ResourceGroupName</span></span>
<span data-ttu-id="8da60-131">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="8da60-131">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8da60-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8da60-132">-ResourceId</span></span>
<span data-ttu-id="8da60-133">EventGrid 主題 ResourceID。</span><span class="sxs-lookup"><span data-stu-id="8da60-133">EventGrid Topic ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8da60-134">-Tag</span><span class="sxs-lookup"><span data-stu-id="8da60-134">-Tag</span></span>
<span data-ttu-id="8da60-135">代表資源標記的 Hashtables。</span><span class="sxs-lookup"><span data-stu-id="8da60-135">Hashtables which represents resource Tag.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: TopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Hashtable
Parameter Sets: TopicInputObjectParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8da60-136">-確認</span><span class="sxs-lookup"><span data-stu-id="8da60-136">-Confirm</span></span>
<span data-ttu-id="8da60-137">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8da60-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8da60-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8da60-138">-WhatIf</span></span>
<span data-ttu-id="8da60-139">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8da60-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8da60-140">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8da60-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8da60-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8da60-141">CommonParameters</span></span>
<span data-ttu-id="8da60-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8da60-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8da60-143">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="8da60-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8da60-144">輸入</span><span class="sxs-lookup"><span data-stu-id="8da60-144">INPUTS</span></span>

### <span data-ttu-id="8da60-145">System.object</span><span class="sxs-lookup"><span data-stu-id="8da60-145">System.String</span></span>

### <span data-ttu-id="8da60-146">PSTopic 中的 EventGrid。</span><span class="sxs-lookup"><span data-stu-id="8da60-146">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="8da60-147">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="8da60-147">System.Collections.Hashtable</span></span>

## <span data-ttu-id="8da60-148">輸出</span><span class="sxs-lookup"><span data-stu-id="8da60-148">OUTPUTS</span></span>

### <span data-ttu-id="8da60-149">PSTopic 中的 EventGrid。</span><span class="sxs-lookup"><span data-stu-id="8da60-149">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="8da60-150">筆記</span><span class="sxs-lookup"><span data-stu-id="8da60-150">NOTES</span></span>

## <span data-ttu-id="8da60-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="8da60-151">RELATED LINKS</span></span>
