---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridTopic.md
ms.openlocfilehash: 402d781c32b98362d504dd5167024932d82e64fb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94136438"
---
# <span data-ttu-id="d51a0-101">New-AzEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="d51a0-101">New-AzEventGridTopic</span></span>

## <span data-ttu-id="d51a0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d51a0-102">SYNOPSIS</span></span>
<span data-ttu-id="d51a0-103">建立新的 Azure 事件格線主題。</span><span class="sxs-lookup"><span data-stu-id="d51a0-103">Creates a new Azure Event Grid Topic.</span></span>

## <span data-ttu-id="d51a0-104">句法</span><span class="sxs-lookup"><span data-stu-id="d51a0-104">SYNTAX</span></span>

```
New-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Tag <Hashtable>]
 [-InputSchema <String>] [-InputMappingField <Hashtable>] [-InputMappingDefaultValue <Hashtable>]
 [-InboundIpRule <Hashtable>] [-PublicNetworkAccess <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d51a0-105">說明</span><span class="sxs-lookup"><span data-stu-id="d51a0-105">DESCRIPTION</span></span>
<span data-ttu-id="d51a0-106">建立新的 Azure 事件格線主題。</span><span class="sxs-lookup"><span data-stu-id="d51a0-106">Creates a new Azure Event Grid Topic.</span></span> <span data-ttu-id="d51a0-107">建立主題之後，應用程式就可以將事件發佈到主題端點。</span><span class="sxs-lookup"><span data-stu-id="d51a0-107">Once the topic is created, an application can publish events to the topic endpoint.</span></span>

## <span data-ttu-id="d51a0-108">示例</span><span class="sxs-lookup"><span data-stu-id="d51a0-108">EXAMPLES</span></span>

### <span data-ttu-id="d51a0-109">範例1</span><span class="sxs-lookup"><span data-stu-id="d51a0-109">Example 1</span></span>
```powershell
PS C:\> New-AzEventGridTopic -ResourceGroupName MyResourceGroupName -Name Topic1 -Location westus2
```

<span data-ttu-id="d51a0-110">\` \` \` \` 在 [資源群組] MyResourceGroupName 中，在指定的地理位置 Westus2 中 \` \` 建立事件格線主題 Topic1。</span><span class="sxs-lookup"><span data-stu-id="d51a0-110">Creates an Event Grid topic \`Topic1\` in the specified geographic location \`westus2\`, in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="d51a0-111">範例2</span><span class="sxs-lookup"><span data-stu-id="d51a0-111">Example 2</span></span>
```powershell
PS C:\> New-AzEventGridTopic -ResourceGroupName MyResourceGroupName -Name Topic1 -Location westus2 -Tag @{ Department="Finance"; Environment="Test" }
```

<span data-ttu-id="d51a0-112">\` \` \` \` 在資源群組 MyResourceGroupName 中，以 \` 指定的標籤「 \` 部門」和「環境」建立事件格線主題 Topic1 在指定的地理位置 westus2 中。</span><span class="sxs-lookup"><span data-stu-id="d51a0-112">Creates an Event Grid topic \`Topic1\` in the specified geographic location \`westus2\`, in resource group \`MyResourceGroupName\` with the specified tags "Department" and "Environment".</span></span>

## <span data-ttu-id="d51a0-113">參數</span><span class="sxs-lookup"><span data-stu-id="d51a0-113">PARAMETERS</span></span>

### <span data-ttu-id="d51a0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d51a0-114">-DefaultProfile</span></span>
<span data-ttu-id="d51a0-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="d51a0-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d51a0-116">-InboundIpRule</span><span class="sxs-lookup"><span data-stu-id="d51a0-116">-InboundIpRule</span></span>
<span data-ttu-id="d51a0-117">代表入站 IP 規則清單的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="d51a0-117">Hashtable which represents list of inbound IP rules.</span></span> <span data-ttu-id="d51a0-118">每個規則都指定 CIDR 符號中的 IP 位址（例如 10.0.0.0/8），以及根據 IpMask 的 match 或不符合的專案來執行對應的動作。</span><span class="sxs-lookup"><span data-stu-id="d51a0-118">Each rule specifies the IP Address in CIDR notation e.g., 10.0.0.0/8 along with the corresponding Action to be performed based on the match or no match of the IpMask.</span></span> <span data-ttu-id="d51a0-119">可能的動作值包括 [只允許]</span><span class="sxs-lookup"><span data-stu-id="d51a0-119">Possible Action values include Allow only</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d51a0-120">-InputMappingDefaultValue</span><span class="sxs-lookup"><span data-stu-id="d51a0-120">-InputMappingDefaultValue</span></span>
<span data-ttu-id="d51a0-121">Hashtable，該雜湊會以空格分隔的 key = 值格式，以預設值代表輸入對應欄位。</span><span class="sxs-lookup"><span data-stu-id="d51a0-121">Hashtable which represents the input mapping fields with default value in space separated key = value format.</span></span> <span data-ttu-id="d51a0-122">允許的金鑰名稱為： subject、執行應及 dataversion。</span><span class="sxs-lookup"><span data-stu-id="d51a0-122">Allowed key names are: subject, eventtype, and dataversion.</span></span> <span data-ttu-id="d51a0-123">這會在 InputSchemaHelp 僅 customeventschema 時使用。</span><span class="sxs-lookup"><span data-stu-id="d51a0-123">This is used when InputSchemaHelp is customeventschema only.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d51a0-124">-InputMappingField</span><span class="sxs-lookup"><span data-stu-id="d51a0-124">-InputMappingField</span></span>
<span data-ttu-id="d51a0-125">Hashtable，以空格分隔鍵 = 值格式代表輸入對應欄位。</span><span class="sxs-lookup"><span data-stu-id="d51a0-125">Hashtable which represents the input mapping fields in space separated key = value format.</span></span> <span data-ttu-id="d51a0-126">允許的金鑰名稱為： id、主題、eventtime、subject、和 dataversion。</span><span class="sxs-lookup"><span data-stu-id="d51a0-126">Allowed key names are: id, topic, eventtime, subject, eventtype, and dataversion.</span></span> <span data-ttu-id="d51a0-127">這會在 InputSchemaHelp 僅 customeventschema 時使用。</span><span class="sxs-lookup"><span data-stu-id="d51a0-127">This is used when InputSchemaHelp is customeventschema only.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d51a0-128">-InputSchema</span><span class="sxs-lookup"><span data-stu-id="d51a0-128">-InputSchema</span></span>
<span data-ttu-id="d51a0-129">主題輸入事件的架構。</span><span class="sxs-lookup"><span data-stu-id="d51a0-129">The schema of the input events for the topic.</span></span> <span data-ttu-id="d51a0-130">允許的值為： eventgridschema、customeventschema 或 cloudeventv01Schema。</span><span class="sxs-lookup"><span data-stu-id="d51a0-130">Allowed values are: eventgridschema, customeventschema, or cloudeventv01Schema.</span></span> <span data-ttu-id="d51a0-131">預設值為 eventgridschema。</span><span class="sxs-lookup"><span data-stu-id="d51a0-131">Default value is eventgridschema.</span></span> <span data-ttu-id="d51a0-132">請注意，如果已指定 customeventschema，則也必須指定 InputMappingField 或/和 InputMappingDefaultValue 參數。</span><span class="sxs-lookup"><span data-stu-id="d51a0-132">Note that if customeventschema is specified, then InputMappingField or/and InputMappingDefaultValue parameters need to be specified as well.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: EventGridSchema, CustomEventSchema, CloudEventSchemaV1_0

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d51a0-133">-位置</span><span class="sxs-lookup"><span data-stu-id="d51a0-133">-Location</span></span>
<span data-ttu-id="d51a0-134">主題的位置</span><span class="sxs-lookup"><span data-stu-id="d51a0-134">The location of the topic</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d51a0-135">-名稱</span><span class="sxs-lookup"><span data-stu-id="d51a0-135">-Name</span></span>
<span data-ttu-id="d51a0-136">主題的名稱。</span><span class="sxs-lookup"><span data-stu-id="d51a0-136">The name of the topic.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d51a0-137">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="d51a0-137">-PublicNetworkAccess</span></span>
<span data-ttu-id="d51a0-138">這會判斷是否允許透過公用網路進行通訊。</span><span class="sxs-lookup"><span data-stu-id="d51a0-138">This determines if traffic is allowed over public network.</span></span> <span data-ttu-id="d51a0-139">預設為啟用。</span><span class="sxs-lookup"><span data-stu-id="d51a0-139">By default it is enabled.</span></span> <span data-ttu-id="d51a0-140">您可以設定 InboundIpRule 參數，進一步限制特定的 Ip。</span><span class="sxs-lookup"><span data-stu-id="d51a0-140">You can further restrict to specific IPs by configuring InboundIpRule parameters.</span></span> <span data-ttu-id="d51a0-141">允許的值已停用且已啟用。</span><span class="sxs-lookup"><span data-stu-id="d51a0-141">Allowed values are disabled and enabled.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: enabled, disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d51a0-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d51a0-142">-ResourceGroupName</span></span>
<span data-ttu-id="d51a0-143">應該在其中建立主題的資源群組。</span><span class="sxs-lookup"><span data-stu-id="d51a0-143">The resource group in which the topic should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d51a0-144">-Tag</span><span class="sxs-lookup"><span data-stu-id="d51a0-144">-Tag</span></span>
<span data-ttu-id="d51a0-145">代表資源標記的 Hashtables。</span><span class="sxs-lookup"><span data-stu-id="d51a0-145">Hashtables which represents resource Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d51a0-146">-確認</span><span class="sxs-lookup"><span data-stu-id="d51a0-146">-Confirm</span></span>
<span data-ttu-id="d51a0-147">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d51a0-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d51a0-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d51a0-148">-WhatIf</span></span>
<span data-ttu-id="d51a0-149">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d51a0-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d51a0-150">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d51a0-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d51a0-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d51a0-151">CommonParameters</span></span>
<span data-ttu-id="d51a0-152">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d51a0-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d51a0-153">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="d51a0-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d51a0-154">輸入</span><span class="sxs-lookup"><span data-stu-id="d51a0-154">INPUTS</span></span>

### <span data-ttu-id="d51a0-155">System.object</span><span class="sxs-lookup"><span data-stu-id="d51a0-155">System.String</span></span>

### <span data-ttu-id="d51a0-156">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="d51a0-156">System.Collections.Hashtable</span></span>

## <span data-ttu-id="d51a0-157">輸出</span><span class="sxs-lookup"><span data-stu-id="d51a0-157">OUTPUTS</span></span>

### <span data-ttu-id="d51a0-158">PSTopic 中的 EventGrid。</span><span class="sxs-lookup"><span data-stu-id="d51a0-158">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="d51a0-159">筆記</span><span class="sxs-lookup"><span data-stu-id="d51a0-159">NOTES</span></span>

## <span data-ttu-id="d51a0-160">相關連結</span><span class="sxs-lookup"><span data-stu-id="d51a0-160">RELATED LINKS</span></span>
