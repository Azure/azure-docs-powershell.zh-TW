---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/powershell/module/az.eventgrid/new-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridTopic.md
ms.openlocfilehash: df81f976f571a59f68d51ef734f1bc3ea5536015
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911981"
---
# <span data-ttu-id="a68dd-101">New-AzEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="a68dd-101">New-AzEventGridTopic</span></span>

## <span data-ttu-id="a68dd-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a68dd-102">SYNOPSIS</span></span>
<span data-ttu-id="a68dd-103">建立新 Azure 事件格線主題。</span><span class="sxs-lookup"><span data-stu-id="a68dd-103">Creates a new Azure Event Grid Topic.</span></span>

## <span data-ttu-id="a68dd-104">語法</span><span class="sxs-lookup"><span data-stu-id="a68dd-104">SYNTAX</span></span>

```
New-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Tag <Hashtable>]
 [-InputSchema <String>] [-InputMappingField <Hashtable>] [-InputMappingDefaultValue <Hashtable>]
 [-InboundIpRule <Hashtable>] [-PublicNetworkAccess <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a68dd-105">描述</span><span class="sxs-lookup"><span data-stu-id="a68dd-105">DESCRIPTION</span></span>
<span data-ttu-id="a68dd-106">建立新 Azure 事件格線主題。</span><span class="sxs-lookup"><span data-stu-id="a68dd-106">Creates a new Azure Event Grid Topic.</span></span> <span data-ttu-id="a68dd-107">建立主題後，應用程式可以將事件發佈至主題端點。</span><span class="sxs-lookup"><span data-stu-id="a68dd-107">Once the topic is created, an application can publish events to the topic endpoint.</span></span>

## <span data-ttu-id="a68dd-108">例子</span><span class="sxs-lookup"><span data-stu-id="a68dd-108">EXAMPLES</span></span>

### <span data-ttu-id="a68dd-109">範例 1</span><span class="sxs-lookup"><span data-stu-id="a68dd-109">Example 1</span></span>
```powershell
PS C:\> New-AzEventGridTopic -ResourceGroupName MyResourceGroupName -Name Topic1 -Location westus2
```

<span data-ttu-id="a68dd-110">在資源群組 \` \` MyResourceGroupName 中，于指定的地理位置 \` westus2 \` 中建立事件網格 \` 線主題主題 \` 1。</span><span class="sxs-lookup"><span data-stu-id="a68dd-110">Creates an Event Grid topic \`Topic1\` in the specified geographic location \`westus2\`, in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="a68dd-111">範例 2</span><span class="sxs-lookup"><span data-stu-id="a68dd-111">Example 2</span></span>
```powershell
PS C:\> New-AzEventGridTopic -ResourceGroupName MyResourceGroupName -Name Topic1 -Location westus2 -Tag @{ Department="Finance"; Environment="Test" }
```

<span data-ttu-id="a68dd-112">在資源群組 \` \` \` \` \` MyResourceGroupName 中，于指定的地理位置 westus2 建立事件格線主題 Topic1，並指定標記「部門」和 \` 「環境」。</span><span class="sxs-lookup"><span data-stu-id="a68dd-112">Creates an Event Grid topic \`Topic1\` in the specified geographic location \`westus2\`, in resource group \`MyResourceGroupName\` with the specified tags "Department" and "Environment".</span></span>

## <span data-ttu-id="a68dd-113">參數</span><span class="sxs-lookup"><span data-stu-id="a68dd-113">PARAMETERS</span></span>

### <span data-ttu-id="a68dd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a68dd-114">-DefaultProfile</span></span>
<span data-ttu-id="a68dd-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="a68dd-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a68dd-116">-InboundIpRule</span><span class="sxs-lookup"><span data-stu-id="a68dd-116">-InboundIpRule</span></span>
<span data-ttu-id="a68dd-117">代表內入 IP 規則清單的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="a68dd-117">Hashtable which represents list of inbound IP rules.</span></span> <span data-ttu-id="a68dd-118">每個規則都指定 CIDR 標記法中的 IP 位址，例如 10.0.0.0/8，以及根據 IpMask 相符或不相符時要執行的對應動作。</span><span class="sxs-lookup"><span data-stu-id="a68dd-118">Each rule specifies the IP Address in CIDR notation e.g., 10.0.0.0/8 along with the corresponding Action to be performed based on the match or no match of the IpMask.</span></span> <span data-ttu-id="a68dd-119">可能的動作值包括僅允許</span><span class="sxs-lookup"><span data-stu-id="a68dd-119">Possible Action values include Allow only</span></span>

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

### <span data-ttu-id="a68dd-120">-InputMappingDefaultValue</span><span class="sxs-lookup"><span data-stu-id="a68dd-120">-InputMappingDefaultValue</span></span>
<span data-ttu-id="a68dd-121">代表以空格分隔鍵 = 值格式預設值之輸入地圖欄位的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="a68dd-121">Hashtable which represents the input mapping fields with default value in space separated key = value format.</span></span> <span data-ttu-id="a68dd-122">允許的金鑰名稱為：subject、eventtype 和資料version。</span><span class="sxs-lookup"><span data-stu-id="a68dd-122">Allowed key names are: subject, eventtype, and dataversion.</span></span> <span data-ttu-id="a68dd-123">只有在 InputSchemaHelp 為 customeventschema 時，會使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="a68dd-123">This is used when InputSchemaHelp is customeventschema only.</span></span>

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

### <span data-ttu-id="a68dd-124">-InputMappingField</span><span class="sxs-lookup"><span data-stu-id="a68dd-124">-InputMappingField</span></span>
<span data-ttu-id="a68dd-125">代表空格分隔鍵 = 值格式之輸入地圖欄位的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="a68dd-125">Hashtable which represents the input mapping fields in space separated key = value format.</span></span> <span data-ttu-id="a68dd-126">允許的金鑰名稱為：id、topic、eventtime、subject、eventtype 和資料version。</span><span class="sxs-lookup"><span data-stu-id="a68dd-126">Allowed key names are: id, topic, eventtime, subject, eventtype, and dataversion.</span></span> <span data-ttu-id="a68dd-127">只有在 InputSchemaHelp 為 customeventschema 時，會使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="a68dd-127">This is used when InputSchemaHelp is customeventschema only.</span></span>

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

### <span data-ttu-id="a68dd-128">-InputSchema</span><span class="sxs-lookup"><span data-stu-id="a68dd-128">-InputSchema</span></span>
<span data-ttu-id="a68dd-129">主題之輸入事件的架構。</span><span class="sxs-lookup"><span data-stu-id="a68dd-129">The schema of the input events for the topic.</span></span> <span data-ttu-id="a68dd-130">允許的值為：eventgridschema、customeventschema 或 cloudeventv01Schema。</span><span class="sxs-lookup"><span data-stu-id="a68dd-130">Allowed values are: eventgridschema, customeventschema, or cloudeventv01Schema.</span></span> <span data-ttu-id="a68dd-131">預設值為 eventgridschema。</span><span class="sxs-lookup"><span data-stu-id="a68dd-131">Default value is eventgridschema.</span></span> <span data-ttu-id="a68dd-132">請注意，如果已指定 customeventschema，則 InputMappingField 或/和 InputMappingDefaultValue 參數也需要指定。</span><span class="sxs-lookup"><span data-stu-id="a68dd-132">Note that if customeventschema is specified, then InputMappingField or/and InputMappingDefaultValue parameters need to be specified as well.</span></span>

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

### <span data-ttu-id="a68dd-133">-位置</span><span class="sxs-lookup"><span data-stu-id="a68dd-133">-Location</span></span>
<span data-ttu-id="a68dd-134">主題的位置</span><span class="sxs-lookup"><span data-stu-id="a68dd-134">The location of the topic</span></span>

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

### <span data-ttu-id="a68dd-135">-名稱</span><span class="sxs-lookup"><span data-stu-id="a68dd-135">-Name</span></span>
<span data-ttu-id="a68dd-136">主題的名稱。</span><span class="sxs-lookup"><span data-stu-id="a68dd-136">The name of the topic.</span></span>

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

### <span data-ttu-id="a68dd-137">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="a68dd-137">-PublicNetworkAccess</span></span>
<span data-ttu-id="a68dd-138">這會決定是否允許流量通過公用網路。</span><span class="sxs-lookup"><span data-stu-id="a68dd-138">This determines if traffic is allowed over public network.</span></span> <span data-ttu-id="a68dd-139">根據預設，此功能會啟用。</span><span class="sxs-lookup"><span data-stu-id="a68dd-139">By default it is enabled.</span></span> <span data-ttu-id="a68dd-140">您可以設定 InboundIpRule 參數，進一步限制特定 IP。</span><span class="sxs-lookup"><span data-stu-id="a68dd-140">You can further restrict to specific IPs by configuring InboundIpRule parameters.</span></span> <span data-ttu-id="a68dd-141">允許的值會停用並啟用。</span><span class="sxs-lookup"><span data-stu-id="a68dd-141">Allowed values are disabled and enabled.</span></span>

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

### <span data-ttu-id="a68dd-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a68dd-142">-ResourceGroupName</span></span>
<span data-ttu-id="a68dd-143">應建立主題的資源群組。</span><span class="sxs-lookup"><span data-stu-id="a68dd-143">The resource group in which the topic should be created.</span></span>

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

### <span data-ttu-id="a68dd-144">-標記</span><span class="sxs-lookup"><span data-stu-id="a68dd-144">-Tag</span></span>
<span data-ttu-id="a68dd-145">代表資源標記的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="a68dd-145">Hashtables which represents resource Tags.</span></span>

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

### <span data-ttu-id="a68dd-146">-確認</span><span class="sxs-lookup"><span data-stu-id="a68dd-146">-Confirm</span></span>
<span data-ttu-id="a68dd-147">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="a68dd-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a68dd-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a68dd-148">-WhatIf</span></span>
<span data-ttu-id="a68dd-149">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a68dd-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a68dd-150">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a68dd-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a68dd-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a68dd-151">CommonParameters</span></span>
<span data-ttu-id="a68dd-152">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a68dd-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a68dd-153">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a68dd-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a68dd-154">輸入</span><span class="sxs-lookup"><span data-stu-id="a68dd-154">INPUTS</span></span>

### <span data-ttu-id="a68dd-155">System.String</span><span class="sxs-lookup"><span data-stu-id="a68dd-155">System.String</span></span>

### <span data-ttu-id="a68dd-156">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="a68dd-156">System.Collections.Hashtable</span></span>

## <span data-ttu-id="a68dd-157">輸出</span><span class="sxs-lookup"><span data-stu-id="a68dd-157">OUTPUTS</span></span>

### <span data-ttu-id="a68dd-158">Microsoft.Azure.Commands.EventGrid.models.PSTopic</span><span class="sxs-lookup"><span data-stu-id="a68dd-158">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="a68dd-159">筆記</span><span class="sxs-lookup"><span data-stu-id="a68dd-159">NOTES</span></span>

## <span data-ttu-id="a68dd-160">相關連結</span><span class="sxs-lookup"><span data-stu-id="a68dd-160">RELATED LINKS</span></span>
