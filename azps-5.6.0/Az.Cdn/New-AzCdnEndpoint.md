---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: A8C6F3BC-EE93-49A4-BF7B-8420967EEB7B
online version: https://docs.microsoft.com/powershell/module/az.cdn/new-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnEndpoint.md
ms.openlocfilehash: 9c902070ad71048c625115ba2803352a3b1132bd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902925"
---
# <span data-ttu-id="80806-101">New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="80806-101">New-AzCdnEndpoint</span></span>

## <span data-ttu-id="80806-102">簡介</span><span class="sxs-lookup"><span data-stu-id="80806-102">SYNOPSIS</span></span>
<span data-ttu-id="80806-103">建立 CDN 端點。</span><span class="sxs-lookup"><span data-stu-id="80806-103">Creates a CDN endpoint.</span></span>

## <span data-ttu-id="80806-104">語法</span><span class="sxs-lookup"><span data-stu-id="80806-104">SYNTAX</span></span>

### <span data-ttu-id="80806-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="80806-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> -Location <String>
 [-OriginHostHeader <String>] [-OriginPath <String>] [-ContentTypesToCompress <String[]>]
 [-IsCompressionEnabled <Boolean>] [-IsHttpAllowed <Boolean>] [-IsHttpsAllowed <Boolean>]
 [-QueryStringCachingBehavior <PSQueryStringCachingBehavior>] -OriginName <String> -OriginHostName <String>
 [-HttpPort <Int32>] [-HttpsPort <Int32>] [-OptimizationType <String>] [-ProbePath <String>]
 [-GeoFilters <PSGeoFilter[]>] [-DeliveryPolicy <PSDeliveryPolicy>] [-Tag <Hashtable>]
 [-DefaultOriginGroup <String>] [-Priority <Int32>] [-Weight <Int32>] [-PrivateLinkApprovalMessage <String>]
 [-PrivateLinkLocation <String>] [-PrivateLinkResourceId <String>]
 [-OriginId <System.Collections.Generic.List`1[System.String]>] [-OriginGroupName <String>]
 [-OriginGroupProbeIntervalInSeconds <Int32>] [-OriginGroupProbePath <String>]
 [-OriginGroupProbeProtocol <String>] [-OriginGroupProbeRequestType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80806-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="80806-106">ByObjectParameterSet</span></span>
```
New-AzCdnEndpoint -EndpointName <String> -CdnProfile <PSProfile> [-OriginHostHeader <String>]
 [-OriginPath <String>] [-ContentTypesToCompress <String[]>] [-IsCompressionEnabled <Boolean>]
 [-IsHttpAllowed <Boolean>] [-IsHttpsAllowed <Boolean>]
 [-QueryStringCachingBehavior <PSQueryStringCachingBehavior>] -OriginName <String> -OriginHostName <String>
 [-HttpPort <Int32>] [-HttpsPort <Int32>] [-OptimizationType <String>] [-ProbePath <String>]
 [-GeoFilters <PSGeoFilter[]>] [-DeliveryPolicy <PSDeliveryPolicy>] [-Tag <Hashtable>]
 [-DefaultOriginGroup <String>] [-Priority <Int32>] [-Weight <Int32>] [-PrivateLinkApprovalMessage <String>]
 [-PrivateLinkLocation <String>] [-PrivateLinkResourceId <String>]
 [-OriginId <System.Collections.Generic.List`1[System.String]>] [-OriginGroupName <String>]
 [-OriginGroupProbeIntervalInSeconds <Int32>] [-OriginGroupProbePath <String>]
 [-OriginGroupProbeProtocol <String>] [-OriginGroupProbeRequestType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="80806-107">描述</span><span class="sxs-lookup"><span data-stu-id="80806-107">DESCRIPTION</span></span>
<span data-ttu-id="80806-108">**New-AzCdnEndpoint** Cmdlet 會建立 Azure 內容傳遞網路 (CDN) 端點。</span><span class="sxs-lookup"><span data-stu-id="80806-108">The **New-AzCdnEndpoint** cmdlet creates an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="80806-109">例子</span><span class="sxs-lookup"><span data-stu-id="80806-109">EXAMPLES</span></span>

## <span data-ttu-id="80806-110">參數</span><span class="sxs-lookup"><span data-stu-id="80806-110">PARAMETERS</span></span>

### <span data-ttu-id="80806-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="80806-111">-CdnProfile</span></span>
<span data-ttu-id="80806-112">指定新增端點的 CDN 設定檔物件。</span><span class="sxs-lookup"><span data-stu-id="80806-112">Specifies the CDN profile object to which the endpoint is added.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="80806-113">-ContentTypesToCompress</span><span class="sxs-lookup"><span data-stu-id="80806-113">-ContentTypesToCompress</span></span>
<span data-ttu-id="80806-114">指定從邊緣節點壓縮到用戶端的內容類型陣列。</span><span class="sxs-lookup"><span data-stu-id="80806-114">Specifies an array of content types to compress from the edge node to the client.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80806-115">-DefaultOriginGroup</span><span class="sxs-lookup"><span data-stu-id="80806-115">-DefaultOriginGroup</span></span>
<span data-ttu-id="80806-116">預設原始群組。</span><span class="sxs-lookup"><span data-stu-id="80806-116">The default origin group.</span></span>

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

### <span data-ttu-id="80806-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80806-117">-DefaultProfile</span></span>
<span data-ttu-id="80806-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="80806-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="80806-119">-DeliveryPolicy</span><span class="sxs-lookup"><span data-stu-id="80806-119">-DeliveryPolicy</span></span>
<span data-ttu-id="80806-120">此端點的傳遞策略。</span><span class="sxs-lookup"><span data-stu-id="80806-120">The delivery policy for this endpoint.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80806-121">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="80806-121">-EndpointName</span></span>
<span data-ttu-id="80806-122">指定端點的名稱。</span><span class="sxs-lookup"><span data-stu-id="80806-122">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="80806-123">-GeoFilters</span><span class="sxs-lookup"><span data-stu-id="80806-123">-GeoFilters</span></span>
<span data-ttu-id="80806-124">適用于此端點的地理位置篩選清單。</span><span class="sxs-lookup"><span data-stu-id="80806-124">The list of geo filters that applies to this endpoint.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSGeoFilter[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80806-125">-HTTPPort</span><span class="sxs-lookup"><span data-stu-id="80806-125">-HttpPort</span></span>
<span data-ttu-id="80806-126">指定原始伺服器的 HTTP 埠號碼。</span><span class="sxs-lookup"><span data-stu-id="80806-126">Specifies the HTTP port number on the origin server.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80806-127">-HTTPsPort</span><span class="sxs-lookup"><span data-stu-id="80806-127">-HttpsPort</span></span>
<span data-ttu-id="80806-128">指定原始伺服器的 HTTPS 埠號碼。</span><span class="sxs-lookup"><span data-stu-id="80806-128">Specifies the HTTPS port number on the origin server.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80806-129">-IsCompressionEnabled</span><span class="sxs-lookup"><span data-stu-id="80806-129">-IsCompressionEnabled</span></span>
<span data-ttu-id="80806-130">指出端點是否已啟用壓縮。</span><span class="sxs-lookup"><span data-stu-id="80806-130">Indicates whether compression is enabled for the endpoint.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80806-131">-IsHttpAllowed</span><span class="sxs-lookup"><span data-stu-id="80806-131">-IsHttpAllowed</span></span>
<span data-ttu-id="80806-132">指出端點是否啟用 HTTP 流量。</span><span class="sxs-lookup"><span data-stu-id="80806-132">Indicates whether the endpoint enables HTTP traffic.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80806-133">-IsHttpsAllowed</span><span class="sxs-lookup"><span data-stu-id="80806-133">-IsHttpsAllowed</span></span>
<span data-ttu-id="80806-134">指出端點是否啟用 HTTPS 流量。</span><span class="sxs-lookup"><span data-stu-id="80806-134">Indicates whether the endpoint enables HTTPS traffic.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80806-135">-位置</span><span class="sxs-lookup"><span data-stu-id="80806-135">-Location</span></span>
<span data-ttu-id="80806-136">指定端點的資源位置。</span><span class="sxs-lookup"><span data-stu-id="80806-136">Specifies the resource location of the endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80806-137">-優化類型</span><span class="sxs-lookup"><span data-stu-id="80806-137">-OptimizationType</span></span>
<span data-ttu-id="80806-138">指定此端點具有的任何優化。</span><span class="sxs-lookup"><span data-stu-id="80806-138">Specifies any optimization this endpoint has.</span></span>

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

### <span data-ttu-id="80806-139">-OriginGroupName</span><span class="sxs-lookup"><span data-stu-id="80806-139">-OriginGroupName</span></span>
<span data-ttu-id="80806-140">來源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="80806-140">The name of the origin group.</span></span>

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

### <span data-ttu-id="80806-141">-OriginGroupProbeIntervalIn2S</span><span class="sxs-lookup"><span data-stu-id="80806-141">-OriginGroupProbeIntervalInSeconds</span></span>
<span data-ttu-id="80806-142">健康狀態小數之間的秒數。</span><span class="sxs-lookup"><span data-stu-id="80806-142">The number of seconds between health probes.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80806-143">-OriginGroupProbePath</span><span class="sxs-lookup"><span data-stu-id="80806-143">-OriginGroupProbePath</span></span>
<span data-ttu-id="80806-144">這是用來判斷來源健康狀態之來源的相對路徑。</span><span class="sxs-lookup"><span data-stu-id="80806-144">The path relative to the origin that is used to determine the health of the origin.</span></span>

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

### <span data-ttu-id="80806-145">-OriginGroupProbeProtocol</span><span class="sxs-lookup"><span data-stu-id="80806-145">-OriginGroupProbeProtocol</span></span>
<span data-ttu-id="80806-146">用於健康調查的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="80806-146">Protocol to use for health probe.</span></span>

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

### <span data-ttu-id="80806-147">-OriginGroupProbeRequestType</span><span class="sxs-lookup"><span data-stu-id="80806-147">-OriginGroupProbeRequestType</span></span>
<span data-ttu-id="80806-148">已提出健康要求的類型。</span><span class="sxs-lookup"><span data-stu-id="80806-148">The type of health probe request that is made.</span></span>

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

### <span data-ttu-id="80806-149">-OriginHostHeader</span><span class="sxs-lookup"><span data-stu-id="80806-149">-OriginHostHeader</span></span>
<span data-ttu-id="80806-150">指定端點的來源主機頭。</span><span class="sxs-lookup"><span data-stu-id="80806-150">Specifies the origin host head of the endpoint.</span></span>

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

### <span data-ttu-id="80806-151">-OriginHostName</span><span class="sxs-lookup"><span data-stu-id="80806-151">-OriginHostName</span></span>
<span data-ttu-id="80806-152">指定原始伺服器的主機名稱稱。</span><span class="sxs-lookup"><span data-stu-id="80806-152">Specifies the host name of the origin server.</span></span>

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

### <span data-ttu-id="80806-153">-OriginId</span><span class="sxs-lookup"><span data-stu-id="80806-153">-OriginId</span></span>
<span data-ttu-id="80806-154">Azure CDN 來源群組識別碼。</span><span class="sxs-lookup"><span data-stu-id="80806-154">Azure CDN origin group ids.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80806-155">-OriginName</span><span class="sxs-lookup"><span data-stu-id="80806-155">-OriginName</span></span>
<span data-ttu-id="80806-156">指定來源伺服器的資源名稱。</span><span class="sxs-lookup"><span data-stu-id="80806-156">Specifies the resource name of the origin server.</span></span>

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

### <span data-ttu-id="80806-157">-OriginPath</span><span class="sxs-lookup"><span data-stu-id="80806-157">-OriginPath</span></span>
<span data-ttu-id="80806-158">指定原始伺服器的路徑。</span><span class="sxs-lookup"><span data-stu-id="80806-158">Specifies the path of the origin server.</span></span>

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

### <span data-ttu-id="80806-159">-優先順序</span><span class="sxs-lookup"><span data-stu-id="80806-159">-Priority</span></span>
<span data-ttu-id="80806-160">Azure CDN 來源優先順序。</span><span class="sxs-lookup"><span data-stu-id="80806-160">Azure CDN origin priority.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80806-161">-PrivateLinkApprovalMessage</span><span class="sxs-lookup"><span data-stu-id="80806-161">-PrivateLinkApprovalMessage</span></span>
<span data-ttu-id="80806-162">要包含在核准要求中以連結至私人連結的自訂訊息。</span><span class="sxs-lookup"><span data-stu-id="80806-162">A custom message to be included in the approval request to connect to the Private Link.</span></span>

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

### <span data-ttu-id="80806-163">-PrivateLinkLocation</span><span class="sxs-lookup"><span data-stu-id="80806-163">-PrivateLinkLocation</span></span>
<span data-ttu-id="80806-164">Azure CDN 來源私人連結位置。</span><span class="sxs-lookup"><span data-stu-id="80806-164">Azure CDN origin private link location.</span></span>

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

### <span data-ttu-id="80806-165">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="80806-165">-PrivateLinkResourceId</span></span>
<span data-ttu-id="80806-166">Azure CDN 來源私人連結資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="80806-166">Azure CDN origin private link resource id.</span></span>

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

### <span data-ttu-id="80806-167">-PathPath</span><span class="sxs-lookup"><span data-stu-id="80806-167">-ProbePath</span></span>
<span data-ttu-id="80806-168">指定動態網站加速的路徑</span><span class="sxs-lookup"><span data-stu-id="80806-168">Specifies the probe path for Dynamic Site Acceleration</span></span>

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

### <span data-ttu-id="80806-169">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="80806-169">-ProfileName</span></span>
<span data-ttu-id="80806-170">指定設定檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="80806-170">Specifies the name of the profile.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80806-171">-QueryStringCachingBehavior</span><span class="sxs-lookup"><span data-stu-id="80806-171">-QueryStringCachingBehavior</span></span>
<span data-ttu-id="80806-172">指定查詢字串位於要求 URL 時 CDN 端點的行為。</span><span class="sxs-lookup"><span data-stu-id="80806-172">Specifies the behavior of CDN endpoint when a query string is in the request URL.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSQueryStringCachingBehavior]
Parameter Sets: (All)
Aliases:
Accepted values: IgnoreQueryString, BypassCaching, UseQueryString, NotSet

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80806-173">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80806-173">-ResourceGroupName</span></span>
<span data-ttu-id="80806-174">指定此端點所屬的資源組名。</span><span class="sxs-lookup"><span data-stu-id="80806-174">Specifies the name of the resource group to which this endpoint belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80806-175">-標記</span><span class="sxs-lookup"><span data-stu-id="80806-175">-Tag</span></span>
<span data-ttu-id="80806-176">要與 Azure CDN 端點關聯的標記。</span><span class="sxs-lookup"><span data-stu-id="80806-176">The tags to associate with the Azure CDN endpoint.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80806-177">-重量</span><span class="sxs-lookup"><span data-stu-id="80806-177">-Weight</span></span>
<span data-ttu-id="80806-178">Azure CDN 來源粗細。</span><span class="sxs-lookup"><span data-stu-id="80806-178">Azure CDN origin weight.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80806-179">-確認</span><span class="sxs-lookup"><span data-stu-id="80806-179">-Confirm</span></span>
<span data-ttu-id="80806-180">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="80806-180">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80806-181">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80806-181">-WhatIf</span></span>
<span data-ttu-id="80806-182">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="80806-182">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80806-183">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="80806-183">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80806-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80806-184">CommonParameters</span></span>
<span data-ttu-id="80806-185">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="80806-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80806-186">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="80806-186">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80806-187">輸入</span><span class="sxs-lookup"><span data-stu-id="80806-187">INPUTS</span></span>

### <span data-ttu-id="80806-188">Microsoft.Azure.Commands.Cdn.models.Profile.PSProfile</span><span class="sxs-lookup"><span data-stu-id="80806-188">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="80806-189">輸出</span><span class="sxs-lookup"><span data-stu-id="80806-189">OUTPUTS</span></span>

### <span data-ttu-id="80806-190">Microsoft.Azure.Commands.Cdn.models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="80806-190">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="80806-191">筆記</span><span class="sxs-lookup"><span data-stu-id="80806-191">NOTES</span></span>

## <span data-ttu-id="80806-192">相關連結</span><span class="sxs-lookup"><span data-stu-id="80806-192">RELATED LINKS</span></span>

[<span data-ttu-id="80806-193">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="80806-193">Get-AzCdnEndpoint</span></span>](./Get-AzCdnEndpoint.md)

[<span data-ttu-id="80806-194">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="80806-194">Remove-AzCdnEndpoint</span></span>](./Remove-AzCdnEndpoint.md)

[<span data-ttu-id="80806-195">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="80806-195">Set-AzCdnEndpoint</span></span>](./Set-AzCdnEndpoint.md)

[<span data-ttu-id="80806-196">Start-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="80806-196">Start-AzCdnEndpoint</span></span>](./Start-AzCdnEndpoint.md)

[<span data-ttu-id="80806-197">Stop-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="80806-197">Stop-AzCdnEndpoint</span></span>](./Stop-AzCdnEndpoint.md)


