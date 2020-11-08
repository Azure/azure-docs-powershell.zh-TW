---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: A8C6F3BC-EE93-49A4-BF7B-8420967EEB7B
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnEndpoint.md
ms.openlocfilehash: 9e0b8ee74ff89f4a5903df1c73dc7b289b0371c4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94137712"
---
# <span data-ttu-id="29bbd-101">New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="29bbd-101">New-AzCdnEndpoint</span></span>

## <span data-ttu-id="29bbd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="29bbd-102">SYNOPSIS</span></span>
<span data-ttu-id="29bbd-103">建立 CDN 端點。</span><span class="sxs-lookup"><span data-stu-id="29bbd-103">Creates a CDN endpoint.</span></span>

## <span data-ttu-id="29bbd-104">句法</span><span class="sxs-lookup"><span data-stu-id="29bbd-104">SYNTAX</span></span>

### <span data-ttu-id="29bbd-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="29bbd-105">ByFieldsParameterSet (Default)</span></span>
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

### <span data-ttu-id="29bbd-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="29bbd-106">ByObjectParameterSet</span></span>
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

## <span data-ttu-id="29bbd-107">說明</span><span class="sxs-lookup"><span data-stu-id="29bbd-107">DESCRIPTION</span></span>
<span data-ttu-id="29bbd-108">**新的-AzCdnEndpoint** Cmdlet 會在 (CDN) 端點上建立 Azure 內容傳遞網路。</span><span class="sxs-lookup"><span data-stu-id="29bbd-108">The **New-AzCdnEndpoint** cmdlet creates an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="29bbd-109">示例</span><span class="sxs-lookup"><span data-stu-id="29bbd-109">EXAMPLES</span></span>

## <span data-ttu-id="29bbd-110">參數</span><span class="sxs-lookup"><span data-stu-id="29bbd-110">PARAMETERS</span></span>

### <span data-ttu-id="29bbd-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="29bbd-111">-CdnProfile</span></span>
<span data-ttu-id="29bbd-112">指定要新增端點的 CDN 設定檔物件。</span><span class="sxs-lookup"><span data-stu-id="29bbd-112">Specifies the CDN profile object to which the endpoint is added.</span></span>

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

### <span data-ttu-id="29bbd-113">-ContentTypesToCompress</span><span class="sxs-lookup"><span data-stu-id="29bbd-113">-ContentTypesToCompress</span></span>
<span data-ttu-id="29bbd-114">指定要從 edge 節點壓縮至用戶端的內容類型陣列。</span><span class="sxs-lookup"><span data-stu-id="29bbd-114">Specifies an array of content types to compress from the edge node to the client.</span></span>

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

### <span data-ttu-id="29bbd-115">-DefaultOriginGroup</span><span class="sxs-lookup"><span data-stu-id="29bbd-115">-DefaultOriginGroup</span></span>
<span data-ttu-id="29bbd-116">[預設原點] 群組。</span><span class="sxs-lookup"><span data-stu-id="29bbd-116">The default origin group.</span></span>

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

### <span data-ttu-id="29bbd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29bbd-117">-DefaultProfile</span></span>
<span data-ttu-id="29bbd-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="29bbd-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="29bbd-119">-DeliveryPolicy</span><span class="sxs-lookup"><span data-stu-id="29bbd-119">-DeliveryPolicy</span></span>
<span data-ttu-id="29bbd-120">此端點的傳遞原則。</span><span class="sxs-lookup"><span data-stu-id="29bbd-120">The delivery policy for this endpoint.</span></span>

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

### <span data-ttu-id="29bbd-121">-終結點</span><span class="sxs-lookup"><span data-stu-id="29bbd-121">-EndpointName</span></span>
<span data-ttu-id="29bbd-122">指定端點的名稱。</span><span class="sxs-lookup"><span data-stu-id="29bbd-122">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="29bbd-123">-GeoFilters</span><span class="sxs-lookup"><span data-stu-id="29bbd-123">-GeoFilters</span></span>
<span data-ttu-id="29bbd-124">適用于此端點的地區篩選清單。</span><span class="sxs-lookup"><span data-stu-id="29bbd-124">The list of geo filters that applies to this endpoint.</span></span>

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

### <span data-ttu-id="29bbd-125">-HttpPort</span><span class="sxs-lookup"><span data-stu-id="29bbd-125">-HttpPort</span></span>
<span data-ttu-id="29bbd-126">指定原始伺服器上的 HTTP 埠號碼。</span><span class="sxs-lookup"><span data-stu-id="29bbd-126">Specifies the HTTP port number on the origin server.</span></span>

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

### <span data-ttu-id="29bbd-127">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="29bbd-127">-HttpsPort</span></span>
<span data-ttu-id="29bbd-128">指定原始伺服器上的 HTTPS 埠號碼。</span><span class="sxs-lookup"><span data-stu-id="29bbd-128">Specifies the HTTPS port number on the origin server.</span></span>

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

### <span data-ttu-id="29bbd-129">-IsCompressionEnabled</span><span class="sxs-lookup"><span data-stu-id="29bbd-129">-IsCompressionEnabled</span></span>
<span data-ttu-id="29bbd-130">指出是否已針對端點啟用壓縮。</span><span class="sxs-lookup"><span data-stu-id="29bbd-130">Indicates whether compression is enabled for the endpoint.</span></span>

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

### <span data-ttu-id="29bbd-131">-IsHttpAllowed</span><span class="sxs-lookup"><span data-stu-id="29bbd-131">-IsHttpAllowed</span></span>
<span data-ttu-id="29bbd-132">指示端點是否啟用 HTTP 流量。</span><span class="sxs-lookup"><span data-stu-id="29bbd-132">Indicates whether the endpoint enables HTTP traffic.</span></span>

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

### <span data-ttu-id="29bbd-133">-IsHttpsAllowed</span><span class="sxs-lookup"><span data-stu-id="29bbd-133">-IsHttpsAllowed</span></span>
<span data-ttu-id="29bbd-134">指示端點是否啟用 HTTPS 流量。</span><span class="sxs-lookup"><span data-stu-id="29bbd-134">Indicates whether the endpoint enables HTTPS traffic.</span></span>

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

### <span data-ttu-id="29bbd-135">-位置</span><span class="sxs-lookup"><span data-stu-id="29bbd-135">-Location</span></span>
<span data-ttu-id="29bbd-136">指定端點的資源位置。</span><span class="sxs-lookup"><span data-stu-id="29bbd-136">Specifies the resource location of the endpoint.</span></span>

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

### <span data-ttu-id="29bbd-137">-OptimizationType</span><span class="sxs-lookup"><span data-stu-id="29bbd-137">-OptimizationType</span></span>
<span data-ttu-id="29bbd-138">指定此端點所擁有的任何優化。</span><span class="sxs-lookup"><span data-stu-id="29bbd-138">Specifies any optimization this endpoint has.</span></span>

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

### <span data-ttu-id="29bbd-139">-OriginGroupName</span><span class="sxs-lookup"><span data-stu-id="29bbd-139">-OriginGroupName</span></span>
<span data-ttu-id="29bbd-140">來源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="29bbd-140">The name of the origin group.</span></span>

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

### <span data-ttu-id="29bbd-141">-OriginGroupProbeIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="29bbd-141">-OriginGroupProbeIntervalInSeconds</span></span>
<span data-ttu-id="29bbd-142">Health 探測之間的秒數。</span><span class="sxs-lookup"><span data-stu-id="29bbd-142">The number of seconds between health probes.</span></span>

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

### <span data-ttu-id="29bbd-143">-OriginGroupProbePath</span><span class="sxs-lookup"><span data-stu-id="29bbd-143">-OriginGroupProbePath</span></span>
<span data-ttu-id="29bbd-144">相對於用於判斷原點健康情況之來源的路徑。</span><span class="sxs-lookup"><span data-stu-id="29bbd-144">The path relative to the origin that is used to determine the health of the origin.</span></span>

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

### <span data-ttu-id="29bbd-145">-OriginGroupProbeProtocol</span><span class="sxs-lookup"><span data-stu-id="29bbd-145">-OriginGroupProbeProtocol</span></span>
<span data-ttu-id="29bbd-146">要用於 health 探測的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="29bbd-146">Protocol to use for health probe.</span></span>

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

### <span data-ttu-id="29bbd-147">-OriginGroupProbeRequestType</span><span class="sxs-lookup"><span data-stu-id="29bbd-147">-OriginGroupProbeRequestType</span></span>
<span data-ttu-id="29bbd-148">所進行的健康情況探測要求類型。</span><span class="sxs-lookup"><span data-stu-id="29bbd-148">The type of health probe request that is made.</span></span>

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

### <span data-ttu-id="29bbd-149">-OriginHostHeader</span><span class="sxs-lookup"><span data-stu-id="29bbd-149">-OriginHostHeader</span></span>
<span data-ttu-id="29bbd-150">指定端點的原始主機頭。</span><span class="sxs-lookup"><span data-stu-id="29bbd-150">Specifies the origin host head of the endpoint.</span></span>

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

### <span data-ttu-id="29bbd-151">-OriginHostName</span><span class="sxs-lookup"><span data-stu-id="29bbd-151">-OriginHostName</span></span>
<span data-ttu-id="29bbd-152">指定原始伺服器的主機名稱。</span><span class="sxs-lookup"><span data-stu-id="29bbd-152">Specifies the host name of the origin server.</span></span>

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

### <span data-ttu-id="29bbd-153">-OriginId</span><span class="sxs-lookup"><span data-stu-id="29bbd-153">-OriginId</span></span>
<span data-ttu-id="29bbd-154">Azure CDN 原始群組識別碼。</span><span class="sxs-lookup"><span data-stu-id="29bbd-154">Azure CDN origin group ids.</span></span>

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

### <span data-ttu-id="29bbd-155">-OriginName</span><span class="sxs-lookup"><span data-stu-id="29bbd-155">-OriginName</span></span>
<span data-ttu-id="29bbd-156">指定原始伺服器的資源名稱。</span><span class="sxs-lookup"><span data-stu-id="29bbd-156">Specifies the resource name of the origin server.</span></span>

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

### <span data-ttu-id="29bbd-157">-OriginPath</span><span class="sxs-lookup"><span data-stu-id="29bbd-157">-OriginPath</span></span>
<span data-ttu-id="29bbd-158">指定原始伺服器的路徑。</span><span class="sxs-lookup"><span data-stu-id="29bbd-158">Specifies the path of the origin server.</span></span>

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

### <span data-ttu-id="29bbd-159">-優先順序</span><span class="sxs-lookup"><span data-stu-id="29bbd-159">-Priority</span></span>
<span data-ttu-id="29bbd-160">Azure CDN 原始優先順序。</span><span class="sxs-lookup"><span data-stu-id="29bbd-160">Azure CDN origin priority.</span></span>

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

### <span data-ttu-id="29bbd-161">-PrivateLinkApprovalMessage</span><span class="sxs-lookup"><span data-stu-id="29bbd-161">-PrivateLinkApprovalMessage</span></span>
<span data-ttu-id="29bbd-162">要包含在要連線到私人連結之核准要求中的自訂訊息。</span><span class="sxs-lookup"><span data-stu-id="29bbd-162">A custom message to be included in the approval request to connect to the Private Link.</span></span>

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

### <span data-ttu-id="29bbd-163">-PrivateLinkLocation</span><span class="sxs-lookup"><span data-stu-id="29bbd-163">-PrivateLinkLocation</span></span>
<span data-ttu-id="29bbd-164">Azure CDN 來源私人連結位置。</span><span class="sxs-lookup"><span data-stu-id="29bbd-164">Azure CDN origin private link location.</span></span>

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

### <span data-ttu-id="29bbd-165">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="29bbd-165">-PrivateLinkResourceId</span></span>
<span data-ttu-id="29bbd-166">Azure CDN 來源私人連結資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="29bbd-166">Azure CDN origin private link resource id.</span></span>

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

### <span data-ttu-id="29bbd-167">-ProbePath</span><span class="sxs-lookup"><span data-stu-id="29bbd-167">-ProbePath</span></span>
<span data-ttu-id="29bbd-168">指定動態網站加速的探測路徑</span><span class="sxs-lookup"><span data-stu-id="29bbd-168">Specifies the probe path for Dynamic Site Acceleration</span></span>

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

### <span data-ttu-id="29bbd-169">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="29bbd-169">-ProfileName</span></span>
<span data-ttu-id="29bbd-170">指定設定檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="29bbd-170">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="29bbd-171">-QueryStringCachingBehavior</span><span class="sxs-lookup"><span data-stu-id="29bbd-171">-QueryStringCachingBehavior</span></span>
<span data-ttu-id="29bbd-172">指定當查詢字串位於要求 URL 中時，CDN 端點的行為。</span><span class="sxs-lookup"><span data-stu-id="29bbd-172">Specifies the behavior of CDN endpoint when a query string is in the request URL.</span></span>

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

### <span data-ttu-id="29bbd-173">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29bbd-173">-ResourceGroupName</span></span>
<span data-ttu-id="29bbd-174">指定此端點所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="29bbd-174">Specifies the name of the resource group to which this endpoint belongs.</span></span>

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

### <span data-ttu-id="29bbd-175">-Tag</span><span class="sxs-lookup"><span data-stu-id="29bbd-175">-Tag</span></span>
<span data-ttu-id="29bbd-176">要與 Azure CDN 端點建立關聯的標籤。</span><span class="sxs-lookup"><span data-stu-id="29bbd-176">The tags to associate with the Azure CDN endpoint.</span></span>

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

### <span data-ttu-id="29bbd-177">寬度</span><span class="sxs-lookup"><span data-stu-id="29bbd-177">-Weight</span></span>
<span data-ttu-id="29bbd-178">Azure CDN 原始重量。</span><span class="sxs-lookup"><span data-stu-id="29bbd-178">Azure CDN origin weight.</span></span>

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

### <span data-ttu-id="29bbd-179">-確認</span><span class="sxs-lookup"><span data-stu-id="29bbd-179">-Confirm</span></span>
<span data-ttu-id="29bbd-180">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="29bbd-180">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29bbd-181">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29bbd-181">-WhatIf</span></span>
<span data-ttu-id="29bbd-182">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="29bbd-182">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29bbd-183">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="29bbd-183">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29bbd-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29bbd-184">CommonParameters</span></span>
<span data-ttu-id="29bbd-185">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="29bbd-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29bbd-186">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="29bbd-186">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29bbd-187">輸入</span><span class="sxs-lookup"><span data-stu-id="29bbd-187">INPUTS</span></span>

### <span data-ttu-id="29bbd-188">PSProfile 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="29bbd-188">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="29bbd-189">輸出</span><span class="sxs-lookup"><span data-stu-id="29bbd-189">OUTPUTS</span></span>

### <span data-ttu-id="29bbd-190">[PSEndpoint] 的 [Cdn] 命令</span><span class="sxs-lookup"><span data-stu-id="29bbd-190">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="29bbd-191">筆記</span><span class="sxs-lookup"><span data-stu-id="29bbd-191">NOTES</span></span>

## <span data-ttu-id="29bbd-192">相關連結</span><span class="sxs-lookup"><span data-stu-id="29bbd-192">RELATED LINKS</span></span>

[<span data-ttu-id="29bbd-193">AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="29bbd-193">Get-AzCdnEndpoint</span></span>](./Get-AzCdnEndpoint.md)

[<span data-ttu-id="29bbd-194">移除-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="29bbd-194">Remove-AzCdnEndpoint</span></span>](./Remove-AzCdnEndpoint.md)

[<span data-ttu-id="29bbd-195">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="29bbd-195">Set-AzCdnEndpoint</span></span>](./Set-AzCdnEndpoint.md)

[<span data-ttu-id="29bbd-196">開始-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="29bbd-196">Start-AzCdnEndpoint</span></span>](./Start-AzCdnEndpoint.md)

[<span data-ttu-id="29bbd-197">停止 AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="29bbd-197">Stop-AzCdnEndpoint</span></span>](./Stop-AzCdnEndpoint.md)


