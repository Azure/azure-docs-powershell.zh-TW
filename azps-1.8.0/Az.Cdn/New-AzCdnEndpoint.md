---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: A8C6F3BC-EE93-49A4-BF7B-8420967EEB7B
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnEndpoint.md
ms.openlocfilehash: 9d8704abaeb5fd320a871b7b15720af3bbb0c472
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93788641"
---
# <span data-ttu-id="daf49-101">New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="daf49-101">New-AzCdnEndpoint</span></span>

## <span data-ttu-id="daf49-102">摘要</span><span class="sxs-lookup"><span data-stu-id="daf49-102">SYNOPSIS</span></span>
<span data-ttu-id="daf49-103">建立 CDN 端點。</span><span class="sxs-lookup"><span data-stu-id="daf49-103">Creates a CDN endpoint.</span></span>

## <span data-ttu-id="daf49-104">句法</span><span class="sxs-lookup"><span data-stu-id="daf49-104">SYNTAX</span></span>

### <span data-ttu-id="daf49-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="daf49-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> -Location <String>
 [-OriginHostHeader <String>] [-OriginPath <String>] [-ContentTypesToCompress <String[]>]
 [-IsCompressionEnabled <Boolean>] [-IsHttpAllowed <Boolean>] [-IsHttpsAllowed <Boolean>]
 [-QueryStringCachingBehavior <PSQueryStringCachingBehavior>] -OriginName <String> -OriginHostName <String>
 [-HttpPort <Int32>] [-HttpsPort <Int32>] [-OptimizationType <String>] [-ProbePath <String>]
 [-GeoFilters <PSGeoFilter[]>] [-DeliveryPolicy <PSDeliveryPolicy>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="daf49-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="daf49-106">ByObjectParameterSet</span></span>
```
New-AzCdnEndpoint -EndpointName <String> -CdnProfile <PSProfile> [-OriginHostHeader <String>]
 [-OriginPath <String>] [-ContentTypesToCompress <String[]>] [-IsCompressionEnabled <Boolean>]
 [-IsHttpAllowed <Boolean>] [-IsHttpsAllowed <Boolean>]
 [-QueryStringCachingBehavior <PSQueryStringCachingBehavior>] -OriginName <String> -OriginHostName <String>
 [-HttpPort <Int32>] [-HttpsPort <Int32>] [-OptimizationType <String>] [-ProbePath <String>]
 [-GeoFilters <PSGeoFilter[]>] [-DeliveryPolicy <PSDeliveryPolicy>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="daf49-107">說明</span><span class="sxs-lookup"><span data-stu-id="daf49-107">DESCRIPTION</span></span>
<span data-ttu-id="daf49-108">**新的-AzCdnEndpoint** Cmdlet 會在 (CDN) 端點上建立 Azure 內容傳遞網路。</span><span class="sxs-lookup"><span data-stu-id="daf49-108">The **New-AzCdnEndpoint** cmdlet creates an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="daf49-109">示例</span><span class="sxs-lookup"><span data-stu-id="daf49-109">EXAMPLES</span></span>

## <span data-ttu-id="daf49-110">參數</span><span class="sxs-lookup"><span data-stu-id="daf49-110">PARAMETERS</span></span>

### <span data-ttu-id="daf49-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="daf49-111">-CdnProfile</span></span>
<span data-ttu-id="daf49-112">指定要新增端點的 CDN 設定檔物件。</span><span class="sxs-lookup"><span data-stu-id="daf49-112">Specifies the CDN profile object to which the endpoint is added.</span></span>

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

### <span data-ttu-id="daf49-113">-ContentTypesToCompress</span><span class="sxs-lookup"><span data-stu-id="daf49-113">-ContentTypesToCompress</span></span>
<span data-ttu-id="daf49-114">指定要從 edge 節點壓縮至用戶端的內容類型陣列。</span><span class="sxs-lookup"><span data-stu-id="daf49-114">Specifies an array of content types to compress from the edge node to the client.</span></span>

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

### <span data-ttu-id="daf49-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="daf49-115">-DefaultProfile</span></span>
<span data-ttu-id="daf49-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="daf49-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="daf49-117">-DeliveryPolicy</span><span class="sxs-lookup"><span data-stu-id="daf49-117">-DeliveryPolicy</span></span>
<span data-ttu-id="daf49-118">此端點的傳遞原則。</span><span class="sxs-lookup"><span data-stu-id="daf49-118">The delivery policy for this endpoint.</span></span>

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

### <span data-ttu-id="daf49-119">-終結點</span><span class="sxs-lookup"><span data-stu-id="daf49-119">-EndpointName</span></span>
<span data-ttu-id="daf49-120">指定端點的名稱。</span><span class="sxs-lookup"><span data-stu-id="daf49-120">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="daf49-121">-GeoFilters</span><span class="sxs-lookup"><span data-stu-id="daf49-121">-GeoFilters</span></span>
<span data-ttu-id="daf49-122">適用于此端點的地區篩選清單。</span><span class="sxs-lookup"><span data-stu-id="daf49-122">The list of geo filters that applies to this endpoint.</span></span>

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

### <span data-ttu-id="daf49-123">-HttpPort</span><span class="sxs-lookup"><span data-stu-id="daf49-123">-HttpPort</span></span>
<span data-ttu-id="daf49-124">指定原始伺服器上的 HTTP 埠號碼。</span><span class="sxs-lookup"><span data-stu-id="daf49-124">Specifies the HTTP port number on the origin server.</span></span>

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

### <span data-ttu-id="daf49-125">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="daf49-125">-HttpsPort</span></span>
<span data-ttu-id="daf49-126">指定原始伺服器上的 HTTPS 埠號碼。</span><span class="sxs-lookup"><span data-stu-id="daf49-126">Specifies the HTTPS port number on the origin server.</span></span>

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

### <span data-ttu-id="daf49-127">-IsCompressionEnabled</span><span class="sxs-lookup"><span data-stu-id="daf49-127">-IsCompressionEnabled</span></span>
<span data-ttu-id="daf49-128">指出是否已針對端點啟用壓縮。</span><span class="sxs-lookup"><span data-stu-id="daf49-128">Indicates whether compression is enabled for the endpoint.</span></span>

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

### <span data-ttu-id="daf49-129">-IsHttpAllowed</span><span class="sxs-lookup"><span data-stu-id="daf49-129">-IsHttpAllowed</span></span>
<span data-ttu-id="daf49-130">指示端點是否啟用 HTTP 流量。</span><span class="sxs-lookup"><span data-stu-id="daf49-130">Indicates whether the endpoint enables HTTP traffic.</span></span>

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

### <span data-ttu-id="daf49-131">-IsHttpsAllowed</span><span class="sxs-lookup"><span data-stu-id="daf49-131">-IsHttpsAllowed</span></span>
<span data-ttu-id="daf49-132">指示端點是否啟用 HTTPS 流量。</span><span class="sxs-lookup"><span data-stu-id="daf49-132">Indicates whether the endpoint enables HTTPS traffic.</span></span>

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

### <span data-ttu-id="daf49-133">-位置</span><span class="sxs-lookup"><span data-stu-id="daf49-133">-Location</span></span>
<span data-ttu-id="daf49-134">指定端點的資源位置。</span><span class="sxs-lookup"><span data-stu-id="daf49-134">Specifies the resource location of the endpoint.</span></span>

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

### <span data-ttu-id="daf49-135">-OptimizationType</span><span class="sxs-lookup"><span data-stu-id="daf49-135">-OptimizationType</span></span>
<span data-ttu-id="daf49-136">指定此端點所擁有的任何優化。</span><span class="sxs-lookup"><span data-stu-id="daf49-136">Specifies any optimization this endpoint has.</span></span>

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

### <span data-ttu-id="daf49-137">-OriginHostHeader</span><span class="sxs-lookup"><span data-stu-id="daf49-137">-OriginHostHeader</span></span>
<span data-ttu-id="daf49-138">指定端點的原始主機頭。</span><span class="sxs-lookup"><span data-stu-id="daf49-138">Specifies the origin host head of the endpoint.</span></span>

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

### <span data-ttu-id="daf49-139">-OriginHostName</span><span class="sxs-lookup"><span data-stu-id="daf49-139">-OriginHostName</span></span>
<span data-ttu-id="daf49-140">指定原始伺服器的主機名稱。</span><span class="sxs-lookup"><span data-stu-id="daf49-140">Specifies the host name of the origin server.</span></span>

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

### <span data-ttu-id="daf49-141">-OriginName</span><span class="sxs-lookup"><span data-stu-id="daf49-141">-OriginName</span></span>
<span data-ttu-id="daf49-142">指定原始伺服器的資源名稱。</span><span class="sxs-lookup"><span data-stu-id="daf49-142">Specifies the resource name of the origin server.</span></span>

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

### <span data-ttu-id="daf49-143">-OriginPath</span><span class="sxs-lookup"><span data-stu-id="daf49-143">-OriginPath</span></span>
<span data-ttu-id="daf49-144">指定原始伺服器的路徑。</span><span class="sxs-lookup"><span data-stu-id="daf49-144">Specifies the path of the origin server.</span></span>

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

### <span data-ttu-id="daf49-145">-ProbePath</span><span class="sxs-lookup"><span data-stu-id="daf49-145">-ProbePath</span></span>
<span data-ttu-id="daf49-146">指定動態網站加速的探測路徑</span><span class="sxs-lookup"><span data-stu-id="daf49-146">Specifies the probe path for Dynamic Site Acceleration</span></span>

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

### <span data-ttu-id="daf49-147">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="daf49-147">-ProfileName</span></span>
<span data-ttu-id="daf49-148">指定設定檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="daf49-148">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="daf49-149">-QueryStringCachingBehavior</span><span class="sxs-lookup"><span data-stu-id="daf49-149">-QueryStringCachingBehavior</span></span>
<span data-ttu-id="daf49-150">指定當查詢字串位於要求 URL 中時，CDN 端點的行為。</span><span class="sxs-lookup"><span data-stu-id="daf49-150">Specifies the behavior of CDN endpoint when a query string is in the request URL.</span></span>

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

### <span data-ttu-id="daf49-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="daf49-151">-ResourceGroupName</span></span>
<span data-ttu-id="daf49-152">指定此端點所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="daf49-152">Specifies the name of the resource group to which this endpoint belongs.</span></span>

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

### <span data-ttu-id="daf49-153">-Tag</span><span class="sxs-lookup"><span data-stu-id="daf49-153">-Tag</span></span>
<span data-ttu-id="daf49-154">要與 Azure CDN 端點建立關聯的標籤。</span><span class="sxs-lookup"><span data-stu-id="daf49-154">The tags to associate with the Azure CDN endpoint.</span></span>

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

### <span data-ttu-id="daf49-155">-確認</span><span class="sxs-lookup"><span data-stu-id="daf49-155">-Confirm</span></span>
<span data-ttu-id="daf49-156">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="daf49-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="daf49-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="daf49-157">-WhatIf</span></span>
<span data-ttu-id="daf49-158">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="daf49-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="daf49-159">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="daf49-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="daf49-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="daf49-160">CommonParameters</span></span>
<span data-ttu-id="daf49-161">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="daf49-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="daf49-162">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="daf49-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="daf49-163">輸入</span><span class="sxs-lookup"><span data-stu-id="daf49-163">INPUTS</span></span>

### <span data-ttu-id="daf49-164">PSProfile 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="daf49-164">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="daf49-165">輸出</span><span class="sxs-lookup"><span data-stu-id="daf49-165">OUTPUTS</span></span>

### <span data-ttu-id="daf49-166">[PSEndpoint] 的 [Cdn] 命令</span><span class="sxs-lookup"><span data-stu-id="daf49-166">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="daf49-167">筆記</span><span class="sxs-lookup"><span data-stu-id="daf49-167">NOTES</span></span>

## <span data-ttu-id="daf49-168">相關連結</span><span class="sxs-lookup"><span data-stu-id="daf49-168">RELATED LINKS</span></span>

[<span data-ttu-id="daf49-169">AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="daf49-169">Get-AzCdnEndpoint</span></span>](./Get-AzCdnEndpoint.md)

[<span data-ttu-id="daf49-170">移除-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="daf49-170">Remove-AzCdnEndpoint</span></span>](./Remove-AzCdnEndpoint.md)

[<span data-ttu-id="daf49-171">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="daf49-171">Set-AzCdnEndpoint</span></span>](./Set-AzCdnEndpoint.md)

[<span data-ttu-id="daf49-172">開始-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="daf49-172">Start-AzCdnEndpoint</span></span>](./Start-AzCdnEndpoint.md)

[<span data-ttu-id="daf49-173">停止 AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="daf49-173">Stop-AzCdnEndpoint</span></span>](./Stop-AzCdnEndpoint.md)


