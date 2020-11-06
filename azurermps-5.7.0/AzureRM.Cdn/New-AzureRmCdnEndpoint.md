---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: A8C6F3BC-EE93-49A4-BF7B-8420967EEB7B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/new-azurermcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/New-AzureRmCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/New-AzureRmCdnEndpoint.md
ms.openlocfilehash: 682c12270608f9c75e86cea742fd411e0eb657a7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446436"
---
# <span data-ttu-id="5ad61-101">New-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="5ad61-101">New-AzureRmCdnEndpoint</span></span>

## <span data-ttu-id="5ad61-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5ad61-102">SYNOPSIS</span></span>
<span data-ttu-id="5ad61-103">建立 CDN 端點。</span><span class="sxs-lookup"><span data-stu-id="5ad61-103">Creates a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5ad61-104">句法</span><span class="sxs-lookup"><span data-stu-id="5ad61-104">SYNTAX</span></span>

### <span data-ttu-id="5ad61-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="5ad61-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzureRmCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -Location <String> [-OriginHostHeader <String>] [-OriginPath <String>] [-ContentTypesToCompress <String[]>]
 [-IsCompressionEnabled <Boolean>] [-IsHttpAllowed <Boolean>] [-IsHttpsAllowed <Boolean>]
 [-QueryStringCachingBehavior <PSQueryStringCachingBehavior>] -OriginName <String> -OriginHostName <String>
 [-HttpPort <Int32>] [-HttpsPort <Int32>] [-OptimizationType <String>] [-GeoFilters <PSGeoFilter[]>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ad61-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5ad61-106">ByObjectParameterSet</span></span>
```
New-AzureRmCdnEndpoint -EndpointName <String> -CdnProfile <PSProfile> [-OriginHostHeader <String>]
 [-OriginPath <String>] [-ContentTypesToCompress <String[]>] [-IsCompressionEnabled <Boolean>]
 [-IsHttpAllowed <Boolean>] [-IsHttpsAllowed <Boolean>]
 [-QueryStringCachingBehavior <PSQueryStringCachingBehavior>] -OriginName <String> -OriginHostName <String>
 [-HttpPort <Int32>] [-HttpsPort <Int32>] [-OptimizationType <String>] [-GeoFilters <PSGeoFilter[]>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ad61-107">說明</span><span class="sxs-lookup"><span data-stu-id="5ad61-107">DESCRIPTION</span></span>
<span data-ttu-id="5ad61-108">**新的-AzureRmCdnEndpoint** Cmdlet 會在 (CDN) 端點上建立 Azure 內容傳遞網路。</span><span class="sxs-lookup"><span data-stu-id="5ad61-108">The **New-AzureRmCdnEndpoint** cmdlet creates an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="5ad61-109">示例</span><span class="sxs-lookup"><span data-stu-id="5ad61-109">EXAMPLES</span></span>

## <span data-ttu-id="5ad61-110">參數</span><span class="sxs-lookup"><span data-stu-id="5ad61-110">PARAMETERS</span></span>

### <span data-ttu-id="5ad61-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="5ad61-111">-CdnProfile</span></span>
<span data-ttu-id="5ad61-112">指定要新增端點的 CDN 設定檔物件。</span><span class="sxs-lookup"><span data-stu-id="5ad61-112">Specifies the CDN profile object to which the endpoint is added.</span></span>

```yaml
Type: PSProfile
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5ad61-113">-ContentTypesToCompress</span><span class="sxs-lookup"><span data-stu-id="5ad61-113">-ContentTypesToCompress</span></span>
<span data-ttu-id="5ad61-114">指定要從 edge 節點壓縮至用戶端的內容類型陣列。</span><span class="sxs-lookup"><span data-stu-id="5ad61-114">Specifies an array of content types to compress from the edge node to the client.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ad61-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ad61-115">-DefaultProfile</span></span>
<span data-ttu-id="5ad61-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="5ad61-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ad61-117">-終結點</span><span class="sxs-lookup"><span data-stu-id="5ad61-117">-EndpointName</span></span>
<span data-ttu-id="5ad61-118">指定端點的名稱。</span><span class="sxs-lookup"><span data-stu-id="5ad61-118">Specifies the name of the endpoint.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ad61-119">-GeoFilters</span><span class="sxs-lookup"><span data-stu-id="5ad61-119">-GeoFilters</span></span>
<span data-ttu-id="5ad61-120">適用于此端點的地區篩選清單。</span><span class="sxs-lookup"><span data-stu-id="5ad61-120">The list of geo filters that applies to this endpoint.</span></span>

```yaml
Type: PSGeoFilter[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ad61-121">-HttpPort</span><span class="sxs-lookup"><span data-stu-id="5ad61-121">-HttpPort</span></span>
<span data-ttu-id="5ad61-122">指定原始伺服器上的 HTTP 埠號碼。</span><span class="sxs-lookup"><span data-stu-id="5ad61-122">Specifies the HTTP port number on the origin server.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ad61-123">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="5ad61-123">-HttpsPort</span></span>
<span data-ttu-id="5ad61-124">指定原始伺服器上的 HTTPS 埠號碼。</span><span class="sxs-lookup"><span data-stu-id="5ad61-124">Specifies the HTTPS port number on the origin server.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ad61-125">-IsCompressionEnabled</span><span class="sxs-lookup"><span data-stu-id="5ad61-125">-IsCompressionEnabled</span></span>
<span data-ttu-id="5ad61-126">指出是否已針對端點啟用壓縮。</span><span class="sxs-lookup"><span data-stu-id="5ad61-126">Indicates whether compression is enabled for the endpoint.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ad61-127">-IsHttpAllowed</span><span class="sxs-lookup"><span data-stu-id="5ad61-127">-IsHttpAllowed</span></span>
<span data-ttu-id="5ad61-128">指示端點是否啟用 HTTP 流量。</span><span class="sxs-lookup"><span data-stu-id="5ad61-128">Indicates whether the endpoint enables HTTP traffic.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ad61-129">-IsHttpsAllowed</span><span class="sxs-lookup"><span data-stu-id="5ad61-129">-IsHttpsAllowed</span></span>
<span data-ttu-id="5ad61-130">指示端點是否啟用 HTTPS 流量。</span><span class="sxs-lookup"><span data-stu-id="5ad61-130">Indicates whether the endpoint enables HTTPS traffic.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ad61-131">-位置</span><span class="sxs-lookup"><span data-stu-id="5ad61-131">-Location</span></span>
<span data-ttu-id="5ad61-132">指定端點的資源位置。</span><span class="sxs-lookup"><span data-stu-id="5ad61-132">Specifies the resource location of the endpoint.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ad61-133">-OptimizationType</span><span class="sxs-lookup"><span data-stu-id="5ad61-133">-OptimizationType</span></span>
<span data-ttu-id="5ad61-134">指定此端點所擁有的任何優化。</span><span class="sxs-lookup"><span data-stu-id="5ad61-134">Specifies any optimization this endpoint has.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ad61-135">-OriginHostHeader</span><span class="sxs-lookup"><span data-stu-id="5ad61-135">-OriginHostHeader</span></span>
<span data-ttu-id="5ad61-136">指定端點的原始主機頭。</span><span class="sxs-lookup"><span data-stu-id="5ad61-136">Specifies the origin host head of the endpoint.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ad61-137">-OriginHostName</span><span class="sxs-lookup"><span data-stu-id="5ad61-137">-OriginHostName</span></span>
<span data-ttu-id="5ad61-138">指定原始伺服器的主機名稱。</span><span class="sxs-lookup"><span data-stu-id="5ad61-138">Specifies the host name of the origin server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ad61-139">-OriginName</span><span class="sxs-lookup"><span data-stu-id="5ad61-139">-OriginName</span></span>
<span data-ttu-id="5ad61-140">指定原始伺服器的資源名稱。</span><span class="sxs-lookup"><span data-stu-id="5ad61-140">Specifies the resource name of the origin server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ad61-141">-OriginPath</span><span class="sxs-lookup"><span data-stu-id="5ad61-141">-OriginPath</span></span>
<span data-ttu-id="5ad61-142">指定原始伺服器的路徑。</span><span class="sxs-lookup"><span data-stu-id="5ad61-142">Specifies the path of the origin server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ad61-143">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="5ad61-143">-ProfileName</span></span>
<span data-ttu-id="5ad61-144">指定設定檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="5ad61-144">Specifies the name of the profile.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ad61-145">-QueryStringCachingBehavior</span><span class="sxs-lookup"><span data-stu-id="5ad61-145">-QueryStringCachingBehavior</span></span>
<span data-ttu-id="5ad61-146">指定當查詢字串位於要求 URL 中時，CDN 端點的行為。</span><span class="sxs-lookup"><span data-stu-id="5ad61-146">Specifies the behavior of CDN endpoint when a query string is in the request URL.</span></span>

```yaml
Type: PSQueryStringCachingBehavior
Parameter Sets: (All)
Aliases:
Accepted values: IgnoreQueryString, BypassCaching, UseQueryString, NotSet

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ad61-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ad61-147">-ResourceGroupName</span></span>
<span data-ttu-id="5ad61-148">指定此端點所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5ad61-148">Specifies the name of the resource group to which this endpoint belongs.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ad61-149">-Tag</span><span class="sxs-lookup"><span data-stu-id="5ad61-149">-Tag</span></span>
<span data-ttu-id="5ad61-150">要與 Azure CDN 端點建立關聯的標籤。</span><span class="sxs-lookup"><span data-stu-id="5ad61-150">The tags to associate with the Azure CDN endpoint.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ad61-151">-確認</span><span class="sxs-lookup"><span data-stu-id="5ad61-151">-Confirm</span></span>
<span data-ttu-id="5ad61-152">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5ad61-152">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ad61-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ad61-153">-WhatIf</span></span>
<span data-ttu-id="5ad61-154">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5ad61-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ad61-155">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5ad61-155">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ad61-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ad61-156">CommonParameters</span></span>
<span data-ttu-id="5ad61-157">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5ad61-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ad61-158">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5ad61-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ad61-159">輸入</span><span class="sxs-lookup"><span data-stu-id="5ad61-159">INPUTS</span></span>

### <span data-ttu-id="5ad61-160">PSProfile</span><span class="sxs-lookup"><span data-stu-id="5ad61-160">PSProfile</span></span>
<span data-ttu-id="5ad61-161">形參 "CdnProfile" 接受管線中 "PSProfile" 類型的值</span><span class="sxs-lookup"><span data-stu-id="5ad61-161">Parameter 'CdnProfile' accepts value of type 'PSProfile' from the pipeline</span></span>

## <span data-ttu-id="5ad61-162">輸出</span><span class="sxs-lookup"><span data-stu-id="5ad61-162">OUTPUTS</span></span>

### <span data-ttu-id="5ad61-163">[PSEndpoint] 的 [Cdn] 命令</span><span class="sxs-lookup"><span data-stu-id="5ad61-163">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="5ad61-164">筆記</span><span class="sxs-lookup"><span data-stu-id="5ad61-164">NOTES</span></span>

## <span data-ttu-id="5ad61-165">相關連結</span><span class="sxs-lookup"><span data-stu-id="5ad61-165">RELATED LINKS</span></span>

[<span data-ttu-id="5ad61-166">AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="5ad61-166">Get-AzureRmCdnEndpoint</span></span>](./Get-AzureRmCdnEndpoint.md)

[<span data-ttu-id="5ad61-167">移除-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="5ad61-167">Remove-AzureRmCdnEndpoint</span></span>](./Remove-AzureRmCdnEndpoint.md)

[<span data-ttu-id="5ad61-168">Set-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="5ad61-168">Set-AzureRmCdnEndpoint</span></span>](./Set-AzureRmCdnEndpoint.md)

[<span data-ttu-id="5ad61-169">開始-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="5ad61-169">Start-AzureRmCdnEndpoint</span></span>](./Start-AzureRmCdnEndpoint.md)

[<span data-ttu-id="5ad61-170">停止 AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="5ad61-170">Stop-AzureRmCdnEndpoint</span></span>](./Stop-AzureRmCdnEndpoint.md)


