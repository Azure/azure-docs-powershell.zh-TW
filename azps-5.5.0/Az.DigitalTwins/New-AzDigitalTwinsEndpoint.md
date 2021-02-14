---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/en-us/powershell/module/az.digitaltwins/new-azdigitaltwinsendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/New-AzDigitalTwinsEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/New-AzDigitalTwinsEndpoint.md
ms.openlocfilehash: 6b2c51d21b40745d3dd4dd2db71604fa01a5a6cc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100136239"
---
# <span data-ttu-id="62f38-101">New-AzDigitalTwinsEndpoint</span><span class="sxs-lookup"><span data-stu-id="62f38-101">New-AzDigitalTwinsEndpoint</span></span>

## <span data-ttu-id="62f38-102">摘要</span><span class="sxs-lookup"><span data-stu-id="62f38-102">SYNOPSIS</span></span>
<span data-ttu-id="62f38-103">建立或更新 DigitalTwinsInstance 端點。</span><span class="sxs-lookup"><span data-stu-id="62f38-103">Create or update DigitalTwinsInstance endpoint.</span></span>

## <span data-ttu-id="62f38-104">句法</span><span class="sxs-lookup"><span data-stu-id="62f38-104">SYNTAX</span></span>

### <span data-ttu-id="62f38-105">EventHub (預設) </span><span class="sxs-lookup"><span data-stu-id="62f38-105">EventHub (Default)</span></span>
```
New-AzDigitalTwinsEndpoint -EndpointName <String> -ResourceGroupName <String> -ResourceName <String>
 -ConnectionStringPrimaryKey <String> -EndpointType <EndpointType> [-SubscriptionId <String>]
 [-ConnectionStringSecondaryKey <String>] [-DeadLetterSecret <String>]
 [-EndpointDescription <IDigitalTwinsEndpointResource>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="62f38-106">EventGrid</span><span class="sxs-lookup"><span data-stu-id="62f38-106">EventGrid</span></span>
```
New-AzDigitalTwinsEndpoint -EndpointName <String> -ResourceGroupName <String> -ResourceName <String>
 -AccessKey1 <String> -EndpointType <EndpointType> -TopicEndpoint <String> [-SubscriptionId <String>]
 [-DeadLetterSecret <String>] [-EndpointDescription <IDigitalTwinsEndpointResource>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="62f38-107">"</span><span class="sxs-lookup"><span data-stu-id="62f38-107">ServiceBus</span></span>
```
New-AzDigitalTwinsEndpoint -EndpointName <String> -ResourceGroupName <String> -ResourceName <String>
 -EndpointType <EndpointType> -PrimaryConnectionString <String> [-SubscriptionId <String>]
 [-DeadLetterSecret <String>] [-EndpointDescription <IDigitalTwinsEndpointResource>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="62f38-108">說明</span><span class="sxs-lookup"><span data-stu-id="62f38-108">DESCRIPTION</span></span>
<span data-ttu-id="62f38-109">建立或更新 DigitalTwinsInstance 端點。</span><span class="sxs-lookup"><span data-stu-id="62f38-109">Create or update DigitalTwinsInstance endpoint.</span></span>

## <span data-ttu-id="62f38-110">示例</span><span class="sxs-lookup"><span data-stu-id="62f38-110">EXAMPLES</span></span>

### <span data-ttu-id="62f38-111">範例1：建立 Eventhub 的 AzDigitalTwinsEndpoint</span><span class="sxs-lookup"><span data-stu-id="62f38-111">Example 1: Create an AzDigitalTwinsEndpoint for Eventhub</span></span>
```powershell
PS C:\> New-AzDigitalTwinsEndpoint -EndpointName youriEventHubEndPoint  -EndpointType EventHub -ResourceGroupName youritemp -ResourceName youriDigitalTwins -connectionStringPrimaryKey 'Endpoint=sb://yourieventhubnp.servicebus.windows.net/;SharedAccessKeyName=youriEventhubPolicy;SharedAccessKey=********;EntityPath=yourieventhub'

Name                  Type
----                  ----
youriEventHubEndPoint Microsoft.DigitalTwins/digitalTwinsInstances/endpoints
```

<span data-ttu-id="62f38-112">依 connectionStringPrimaryKey 建立 Eventhub 的 AzDigitalTwinsEndpoint</span><span class="sxs-lookup"><span data-stu-id="62f38-112">Create an AzDigitalTwinsEndpoint for Eventhub by connectionStringPrimaryKey</span></span>

### <span data-ttu-id="62f38-113">範例2：建立 EventGrid 的 AzDigitalTwinsEndpoint</span><span class="sxs-lookup"><span data-stu-id="62f38-113">Example 2: Create an AzDigitalTwinsEndpoint for EventGrid</span></span>
```powershell
PS C:\> New-AzDigitalTwinsEndpoint -EndpointName youriEventGridPoint  -EndpointType EventGrid -ResourceGroupName youritemp -ResourceName youriDigitalTwins -TopicEndpoint 'https://yourieventgrid.eastus-1.eventgrid.azure.net/api/events' -AccessKey1 'xxxxxxxxx='

Name                  Type
----                  ----
youriEventGridPoint Microsoft.DigitalTwins/digitalTwinsInstances/endpoints
```

<span data-ttu-id="62f38-114">依 TopicEndpoint 和 accessKey1 建立 Eventhub 的 AzDigitalTwinsEndpoint</span><span class="sxs-lookup"><span data-stu-id="62f38-114">Create an AzDigitalTwinsEndpoint for Eventhub by TopicEndpoint and accessKey1</span></span>

### <span data-ttu-id="62f38-115">範例3：建立 AzDigitalTwinsEndpoint</span><span class="sxs-lookup"><span data-stu-id="62f38-115">Example 3: Create an AzDigitalTwinsEndpoint for ServiceBus</span></span>
```powershell
PS C:\> New-AzDigitalTwinsEndpoint -EndpointName youriServiceBusPoint  -EndpointType EventGrid -ResourceGroupName youritemp -ResourceName youriDigitalTwins -PrimaryConnectionString "Endpoint=sb://yourieventhubnp.servicebus.windows.net/;SharedAccessKeyName=******;SharedAccessKey=********;EntityPath=yourieventhub"

Name                  Type
----                  ----
youriServiceBusPoint Microsoft.DigitalTwins/digitalTwinsInstances/endpoints
```

<span data-ttu-id="62f38-116">透過 PrimaryConnectionString 建立 ServicBus 的 AzDigitalTwinsEndpoint</span><span class="sxs-lookup"><span data-stu-id="62f38-116">Create an AzDigitalTwinsEndpoint for ServicBus by PrimaryConnectionString</span></span>

## <span data-ttu-id="62f38-117">參數</span><span class="sxs-lookup"><span data-stu-id="62f38-117">PARAMETERS</span></span>

### <span data-ttu-id="62f38-118">-AccessKey1</span><span class="sxs-lookup"><span data-stu-id="62f38-118">-AccessKey1</span></span>
<span data-ttu-id="62f38-119">訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="62f38-119">The subscription identifier.</span></span>

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

### <span data-ttu-id="62f38-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="62f38-120">-AsJob</span></span>
<span data-ttu-id="62f38-121">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="62f38-121">Run the command as a job</span></span>

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

### <span data-ttu-id="62f38-122">-ConnectionStringPrimaryKey</span><span class="sxs-lookup"><span data-stu-id="62f38-122">-ConnectionStringPrimaryKey</span></span>
<span data-ttu-id="62f38-123">訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="62f38-123">The subscription identifier.</span></span>

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

### <span data-ttu-id="62f38-124">-ConnectionStringSecondaryKey</span><span class="sxs-lookup"><span data-stu-id="62f38-124">-ConnectionStringSecondaryKey</span></span>
<span data-ttu-id="62f38-125">訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="62f38-125">The subscription identifier.</span></span>

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

### <span data-ttu-id="62f38-126">-DeadLetterSecret</span><span class="sxs-lookup"><span data-stu-id="62f38-126">-DeadLetterSecret</span></span>
<span data-ttu-id="62f38-127">死信儲存密碼。</span><span class="sxs-lookup"><span data-stu-id="62f38-127">Dead letter storage secret.</span></span>
<span data-ttu-id="62f38-128">在讀取時會被混淆。</span><span class="sxs-lookup"><span data-stu-id="62f38-128">Will be obfuscated during read.</span></span>

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

### <span data-ttu-id="62f38-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62f38-129">-DefaultProfile</span></span>
<span data-ttu-id="62f38-130">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="62f38-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62f38-131">-EndpointDescription</span><span class="sxs-lookup"><span data-stu-id="62f38-131">-EndpointDescription</span></span>
<span data-ttu-id="62f38-132">DigitalTwinsInstance 端點資源。</span><span class="sxs-lookup"><span data-stu-id="62f38-132">DigitalTwinsInstance endpoint resource.</span></span>
<span data-ttu-id="62f38-133">若要建立，請參閱 ENDPOINTDESCRIPTION 屬性和建立雜湊資料表的備忘稿區段。</span><span class="sxs-lookup"><span data-stu-id="62f38-133">To construct, see NOTES section for ENDPOINTDESCRIPTION properties and create a hash table.</span></span>

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

### <span data-ttu-id="62f38-134">-終結點</span><span class="sxs-lookup"><span data-stu-id="62f38-134">-EndpointName</span></span>
<span data-ttu-id="62f38-135">端點資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="62f38-135">Name of Endpoint Resource.</span></span>

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

### <span data-ttu-id="62f38-136">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="62f38-136">-EndpointType</span></span>
<span data-ttu-id="62f38-137">數位 Twins 端點的類型</span><span class="sxs-lookup"><span data-stu-id="62f38-137">The type of Digital Twins endpoint</span></span>

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

### <span data-ttu-id="62f38-138">-NoWait</span><span class="sxs-lookup"><span data-stu-id="62f38-138">-NoWait</span></span>
<span data-ttu-id="62f38-139">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="62f38-139">Run the command asynchronously</span></span>

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

### <span data-ttu-id="62f38-140">-PrimaryConnectionString</span><span class="sxs-lookup"><span data-stu-id="62f38-140">-PrimaryConnectionString</span></span>
<span data-ttu-id="62f38-141">訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="62f38-141">The subscription identifier.</span></span>

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

### <span data-ttu-id="62f38-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62f38-142">-ResourceGroupName</span></span>
<span data-ttu-id="62f38-143">包含 DigitalTwinsInstance 之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="62f38-143">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="62f38-144">-CoNtext.resourcename</span><span class="sxs-lookup"><span data-stu-id="62f38-144">-ResourceName</span></span>
<span data-ttu-id="62f38-145">DigitalTwinsInstance 的名稱。</span><span class="sxs-lookup"><span data-stu-id="62f38-145">The name of the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="62f38-146">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="62f38-146">-SubscriptionId</span></span>
<span data-ttu-id="62f38-147">訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="62f38-147">The subscription identifier.</span></span>

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

### <span data-ttu-id="62f38-148">-TopicEndpoint</span><span class="sxs-lookup"><span data-stu-id="62f38-148">-TopicEndpoint</span></span>
<span data-ttu-id="62f38-149">訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="62f38-149">The subscription identifier.</span></span>

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

### <span data-ttu-id="62f38-150">-確認</span><span class="sxs-lookup"><span data-stu-id="62f38-150">-Confirm</span></span>
<span data-ttu-id="62f38-151">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="62f38-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62f38-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62f38-152">-WhatIf</span></span>
<span data-ttu-id="62f38-153">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="62f38-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62f38-154">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="62f38-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62f38-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62f38-155">CommonParameters</span></span>
<span data-ttu-id="62f38-156">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="62f38-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62f38-157">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="62f38-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62f38-158">輸入</span><span class="sxs-lookup"><span data-stu-id="62f38-158">INPUTS</span></span>

### <span data-ttu-id="62f38-159">IDigitalTwinsEndpointResource （DigitalTwins）。 Api20201031。</span><span class="sxs-lookup"><span data-stu-id="62f38-159">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span></span>

## <span data-ttu-id="62f38-160">輸出</span><span class="sxs-lookup"><span data-stu-id="62f38-160">OUTPUTS</span></span>

### <span data-ttu-id="62f38-161">IDigitalTwinsEndpointResource （DigitalTwins）。 Api20201031。</span><span class="sxs-lookup"><span data-stu-id="62f38-161">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span></span>

## <span data-ttu-id="62f38-162">筆記</span><span class="sxs-lookup"><span data-stu-id="62f38-162">NOTES</span></span>

<span data-ttu-id="62f38-163">別名</span><span class="sxs-lookup"><span data-stu-id="62f38-163">ALIASES</span></span>

<span data-ttu-id="62f38-164">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="62f38-164">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="62f38-165">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="62f38-165">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="62f38-166">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="62f38-166">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="62f38-167">ENDPOINTDESCRIPTION <IDigitalTwinsEndpointResource> ： DigitalTwinsInstance 端點資源。</span><span class="sxs-lookup"><span data-stu-id="62f38-167">ENDPOINTDESCRIPTION <IDigitalTwinsEndpointResource>: DigitalTwinsInstance endpoint resource.</span></span>
  - <span data-ttu-id="62f38-168">`EndpointType <EndpointType>`：數位 Twins 端點的類型</span><span class="sxs-lookup"><span data-stu-id="62f38-168">`EndpointType <EndpointType>`: The type of Digital Twins endpoint</span></span>
  - <span data-ttu-id="62f38-169">`[DeadLetterSecret <String>]`：死信儲存密碼。</span><span class="sxs-lookup"><span data-stu-id="62f38-169">`[DeadLetterSecret <String>]`: Dead letter storage secret.</span></span> <span data-ttu-id="62f38-170">在讀取時會被混淆。</span><span class="sxs-lookup"><span data-stu-id="62f38-170">Will be obfuscated during read.</span></span>

## <span data-ttu-id="62f38-171">相關連結</span><span class="sxs-lookup"><span data-stu-id="62f38-171">RELATED LINKS</span></span>

