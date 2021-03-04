---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/powershell/module/az.digitaltwins/new-azdigitaltwinsendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/New-AzDigitalTwinsEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/New-AzDigitalTwinsEndpoint.md
ms.openlocfilehash: 3c59099a2e4440e2c92836ab02b8396b5fc3b207
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910178"
---
# <span data-ttu-id="a9a44-101">New-AzDigitalTwinsEndpoint</span><span class="sxs-lookup"><span data-stu-id="a9a44-101">New-AzDigitalTwinsEndpoint</span></span>

## <span data-ttu-id="a9a44-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a9a44-102">SYNOPSIS</span></span>
<span data-ttu-id="a9a44-103">建立或更新 DigitalTwinsInstance 端點。</span><span class="sxs-lookup"><span data-stu-id="a9a44-103">Create or update DigitalTwinsInstance endpoint.</span></span>

## <span data-ttu-id="a9a44-104">語法</span><span class="sxs-lookup"><span data-stu-id="a9a44-104">SYNTAX</span></span>

### <span data-ttu-id="a9a44-105">EventHub (預設) </span><span class="sxs-lookup"><span data-stu-id="a9a44-105">EventHub (Default)</span></span>
```
New-AzDigitalTwinsEndpoint -EndpointName <String> -ResourceGroupName <String> -ResourceName <String>
 -ConnectionStringPrimaryKey <String> -EndpointType <EndpointType> [-SubscriptionId <String>]
 [-ConnectionStringSecondaryKey <String>] [-DeadLetterSecret <String>]
 [-EndpointDescription <IDigitalTwinsEndpointResource>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a9a44-106">EventGrid</span><span class="sxs-lookup"><span data-stu-id="a9a44-106">EventGrid</span></span>
```
New-AzDigitalTwinsEndpoint -EndpointName <String> -ResourceGroupName <String> -ResourceName <String>
 -AccessKey1 <String> -EndpointType <EndpointType> -TopicEndpoint <String> [-SubscriptionId <String>]
 [-DeadLetterSecret <String>] [-EndpointDescription <IDigitalTwinsEndpointResource>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a9a44-107">ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a9a44-107">ServiceBus</span></span>
```
New-AzDigitalTwinsEndpoint -EndpointName <String> -ResourceGroupName <String> -ResourceName <String>
 -EndpointType <EndpointType> -PrimaryConnectionString <String> [-SubscriptionId <String>]
 [-DeadLetterSecret <String>] [-EndpointDescription <IDigitalTwinsEndpointResource>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a9a44-108">描述</span><span class="sxs-lookup"><span data-stu-id="a9a44-108">DESCRIPTION</span></span>
<span data-ttu-id="a9a44-109">建立或更新 DigitalTwinsInstance 端點。</span><span class="sxs-lookup"><span data-stu-id="a9a44-109">Create or update DigitalTwinsInstance endpoint.</span></span>

## <span data-ttu-id="a9a44-110">例子</span><span class="sxs-lookup"><span data-stu-id="a9a44-110">EXAMPLES</span></span>

### <span data-ttu-id="a9a44-111">範例 1：建立 AzDigitalTwinsEndpoint for Eventhub</span><span class="sxs-lookup"><span data-stu-id="a9a44-111">Example 1: Create an AzDigitalTwinsEndpoint for Eventhub</span></span>
```powershell
PS C:\> New-AzDigitalTwinsEndpoint -EndpointName youriEventHubEndPoint  -EndpointType EventHub -ResourceGroupName youritemp -ResourceName youriDigitalTwins -connectionStringPrimaryKey 'Endpoint=sb://yourieventhubnp.servicebus.windows.net/;SharedAccessKeyName=youriEventhubPolicy;SharedAccessKey=********;EntityPath=yourieventhub'

Name                  Type
----                  ----
youriEventHubEndPoint Microsoft.DigitalTwins/digitalTwinsInstances/endpoints
```

<span data-ttu-id="a9a44-112">使用 connectionStringPrimaryKey 建立 AzDigitalTwinsEndpoint for Eventhub</span><span class="sxs-lookup"><span data-stu-id="a9a44-112">Create an AzDigitalTwinsEndpoint for Eventhub by connectionStringPrimaryKey</span></span>

### <span data-ttu-id="a9a44-113">範例 2：建立 AzDigitalTwinsEndpoint for EventGrid</span><span class="sxs-lookup"><span data-stu-id="a9a44-113">Example 2: Create an AzDigitalTwinsEndpoint for EventGrid</span></span>
```powershell
PS C:\> New-AzDigitalTwinsEndpoint -EndpointName youriEventGridPoint  -EndpointType EventGrid -ResourceGroupName youritemp -ResourceName youriDigitalTwins -TopicEndpoint 'https://yourieventgrid.eastus-1.eventgrid.azure.net/api/events' -AccessKey1 'xxxxxxxxx='

Name                  Type
----                  ----
youriEventGridPoint Microsoft.DigitalTwins/digitalTwinsInstances/endpoints
```

<span data-ttu-id="a9a44-114">使用 TopicEndpoint 和 accessKey1 建立 AzDigitalTwinsEndpoint for Eventhub</span><span class="sxs-lookup"><span data-stu-id="a9a44-114">Create an AzDigitalTwinsEndpoint for Eventhub by TopicEndpoint and accessKey1</span></span>

### <span data-ttu-id="a9a44-115">範例 3：建立 AzDigitalTwinsEndpoint for ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a9a44-115">Example 3: Create an AzDigitalTwinsEndpoint for ServiceBus</span></span>
```powershell
PS C:\> New-AzDigitalTwinsEndpoint -EndpointName youriServiceBusPoint  -EndpointType EventGrid -ResourceGroupName youritemp -ResourceName youriDigitalTwins -PrimaryConnectionString "Endpoint=sb://yourieventhubnp.servicebus.windows.net/;SharedAccessKeyName=******;SharedAccessKey=********;EntityPath=yourieventhub"

Name                  Type
----                  ----
youriServiceBusPoint Microsoft.DigitalTwins/digitalTwinsInstances/endpoints
```

<span data-ttu-id="a9a44-116">建立 AzDigitalTwinsEndpoint for ServicBus by PrimaryConnectionString</span><span class="sxs-lookup"><span data-stu-id="a9a44-116">Create an AzDigitalTwinsEndpoint for ServicBus by PrimaryConnectionString</span></span>

## <span data-ttu-id="a9a44-117">參數</span><span class="sxs-lookup"><span data-stu-id="a9a44-117">PARAMETERS</span></span>

### <span data-ttu-id="a9a44-118">-AccessKey1</span><span class="sxs-lookup"><span data-stu-id="a9a44-118">-AccessKey1</span></span>
<span data-ttu-id="a9a44-119">訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="a9a44-119">The subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: EventGrid
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9a44-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a9a44-120">-AsJob</span></span>
<span data-ttu-id="a9a44-121">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="a9a44-121">Run the command as a job</span></span>

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

### <span data-ttu-id="a9a44-122">-ConnectionStringPrimaryKey</span><span class="sxs-lookup"><span data-stu-id="a9a44-122">-ConnectionStringPrimaryKey</span></span>
<span data-ttu-id="a9a44-123">訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="a9a44-123">The subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: EventHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9a44-124">-ConnectionString中鍵</span><span class="sxs-lookup"><span data-stu-id="a9a44-124">-ConnectionStringSecondaryKey</span></span>
<span data-ttu-id="a9a44-125">訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="a9a44-125">The subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: EventHub
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9a44-126">-DeadLetterSecret</span><span class="sxs-lookup"><span data-stu-id="a9a44-126">-DeadLetterSecret</span></span>
<span data-ttu-id="a9a44-127">已死亡信件儲存空間的秘訣。</span><span class="sxs-lookup"><span data-stu-id="a9a44-127">Dead letter storage secret.</span></span>
<span data-ttu-id="a9a44-128">在閱讀期間會混淆。</span><span class="sxs-lookup"><span data-stu-id="a9a44-128">Will be obfuscated during read.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9a44-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9a44-129">-DefaultProfile</span></span>
<span data-ttu-id="a9a44-130">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a9a44-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9a44-131">-EndpointDescription</span><span class="sxs-lookup"><span data-stu-id="a9a44-131">-EndpointDescription</span></span>
<span data-ttu-id="a9a44-132">DigitalTwinsInstance 端點資源。</span><span class="sxs-lookup"><span data-stu-id="a9a44-132">DigitalTwinsInstance endpoint resource.</span></span>
<span data-ttu-id="a9a44-133">若要建構，請參閱 ENDPOINTDESCRIPTION 屬性的附注區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="a9a44-133">To construct, see NOTES section for ENDPOINTDESCRIPTION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a9a44-134">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="a9a44-134">-EndpointName</span></span>
<span data-ttu-id="a9a44-135">端點資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="a9a44-135">Name of Endpoint Resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9a44-136">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="a9a44-136">-EndpointType</span></span>
<span data-ttu-id="a9a44-137">數位長條端點的類型</span><span class="sxs-lookup"><span data-stu-id="a9a44-137">The type of Digital Twins endpoint</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Support.EndpointType
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9a44-138">-NoWait</span><span class="sxs-lookup"><span data-stu-id="a9a44-138">-NoWait</span></span>
<span data-ttu-id="a9a44-139">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="a9a44-139">Run the command asynchronously</span></span>

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

### <span data-ttu-id="a9a44-140">-PrimaryConnectionString</span><span class="sxs-lookup"><span data-stu-id="a9a44-140">-PrimaryConnectionString</span></span>
<span data-ttu-id="a9a44-141">訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="a9a44-141">The subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceBus
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9a44-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9a44-142">-ResourceGroupName</span></span>
<span data-ttu-id="a9a44-143">包含 DigitalTwinsInstance 的資源組名。</span><span class="sxs-lookup"><span data-stu-id="a9a44-143">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9a44-144">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="a9a44-144">-ResourceName</span></span>
<span data-ttu-id="a9a44-145">DigitalTwinsInstance 的名稱。</span><span class="sxs-lookup"><span data-stu-id="a9a44-145">The name of the DigitalTwinsInstance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9a44-146">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a9a44-146">-SubscriptionId</span></span>
<span data-ttu-id="a9a44-147">訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="a9a44-147">The subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9a44-148">-TopicEndpoint</span><span class="sxs-lookup"><span data-stu-id="a9a44-148">-TopicEndpoint</span></span>
<span data-ttu-id="a9a44-149">訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="a9a44-149">The subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: EventGrid
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9a44-150">-確認</span><span class="sxs-lookup"><span data-stu-id="a9a44-150">-Confirm</span></span>
<span data-ttu-id="a9a44-151">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="a9a44-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9a44-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9a44-152">-WhatIf</span></span>
<span data-ttu-id="a9a44-153">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a9a44-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9a44-154">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a9a44-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9a44-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9a44-155">CommonParameters</span></span>
<span data-ttu-id="a9a44-156">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a9a44-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9a44-157">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a9a44-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9a44-158">輸入</span><span class="sxs-lookup"><span data-stu-id="a9a44-158">INPUTS</span></span>

### <span data-ttu-id="a9a44-159">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span><span class="sxs-lookup"><span data-stu-id="a9a44-159">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span></span>

## <span data-ttu-id="a9a44-160">輸出</span><span class="sxs-lookup"><span data-stu-id="a9a44-160">OUTPUTS</span></span>

### <span data-ttu-id="a9a44-161">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span><span class="sxs-lookup"><span data-stu-id="a9a44-161">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span></span>

## <span data-ttu-id="a9a44-162">筆記</span><span class="sxs-lookup"><span data-stu-id="a9a44-162">NOTES</span></span>

<span data-ttu-id="a9a44-163">別名</span><span class="sxs-lookup"><span data-stu-id="a9a44-163">ALIASES</span></span>

<span data-ttu-id="a9a44-164">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="a9a44-164">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a9a44-165">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="a9a44-165">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a9a44-166">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="a9a44-166">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a9a44-167">ENDPOINTDESCRIPTION <IDigitalTwinsEndpointResource> ：DigitalTwinsInstance 端點資源。</span><span class="sxs-lookup"><span data-stu-id="a9a44-167">ENDPOINTDESCRIPTION <IDigitalTwinsEndpointResource>: DigitalTwinsInstance endpoint resource.</span></span>
  - <span data-ttu-id="a9a44-168">`EndpointType <EndpointType>`：數位星型端點的類型</span><span class="sxs-lookup"><span data-stu-id="a9a44-168">`EndpointType <EndpointType>`: The type of Digital Twins endpoint</span></span>
  - <span data-ttu-id="a9a44-169">`[DeadLetterSecret <String>]`：無信儲存空間的秘訣。</span><span class="sxs-lookup"><span data-stu-id="a9a44-169">`[DeadLetterSecret <String>]`: Dead letter storage secret.</span></span> <span data-ttu-id="a9a44-170">在閱讀期間會混淆。</span><span class="sxs-lookup"><span data-stu-id="a9a44-170">Will be obfuscated during read.</span></span>

## <span data-ttu-id="a9a44-171">相關連結</span><span class="sxs-lookup"><span data-stu-id="a9a44-171">RELATED LINKS</span></span>

