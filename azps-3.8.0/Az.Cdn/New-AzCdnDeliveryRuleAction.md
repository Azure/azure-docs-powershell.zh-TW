---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdndeliveryruleaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleAction.md
ms.openlocfilehash: d893850105656a9f599870e2ef17a6b195254ad6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93958789"
---
# <span data-ttu-id="2ca63-101">New-AzCdnDeliveryRuleAction</span><span class="sxs-lookup"><span data-stu-id="2ca63-101">New-AzCdnDeliveryRuleAction</span></span>

## <span data-ttu-id="2ca63-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2ca63-102">SYNOPSIS</span></span>
<span data-ttu-id="2ca63-103">建立傳遞動作。</span><span class="sxs-lookup"><span data-stu-id="2ca63-103">Creates a delivery action.</span></span>

## <span data-ttu-id="2ca63-104">句法</span><span class="sxs-lookup"><span data-stu-id="2ca63-104">SYNTAX</span></span>

### <span data-ttu-id="2ca63-105">CacheExpirationActionParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="2ca63-105">CacheExpirationActionParameterSet (Default)</span></span>
```
New-AzCdnDeliveryRuleAction -CacheBehavior <String> [-CacheDuration <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2ca63-106">HeaderActionParameterSet</span><span class="sxs-lookup"><span data-stu-id="2ca63-106">HeaderActionParameterSet</span></span>
```
New-AzCdnDeliveryRuleAction -HeaderActionType <String> -Action <String> -HeaderName <String> [-Value <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2ca63-107">UrlRedirectActionParameterSet</span><span class="sxs-lookup"><span data-stu-id="2ca63-107">UrlRedirectActionParameterSet</span></span>
```
New-AzCdnDeliveryRuleAction -RedirectType <String> [-DestinationProtocol <String>] [-CustomPath <String>]
 [-CustomHostname <String>] [-CustomQueryString <String>] [-CustomFragment <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2ca63-108">CacheKeyQueryStringActionParameterSet</span><span class="sxs-lookup"><span data-stu-id="2ca63-108">CacheKeyQueryStringActionParameterSet</span></span>
```
New-AzCdnDeliveryRuleAction -QueryStringBehavior <String> [-QueryParameter <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2ca63-109">UrlRewriteActionParameterSet</span><span class="sxs-lookup"><span data-stu-id="2ca63-109">UrlRewriteActionParameterSet</span></span>
```
New-AzCdnDeliveryRuleAction -SourcePattern <String> -Destination <String> [-PreservePath]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2ca63-110">說明</span><span class="sxs-lookup"><span data-stu-id="2ca63-110">DESCRIPTION</span></span>
<span data-ttu-id="2ca63-111">**新的-AzCdnDeliveryRule** Cmdlet 會建立 CDN 端點建立的傳遞規則。</span><span class="sxs-lookup"><span data-stu-id="2ca63-111">The **New-AzCdnDeliveryRule** cmdlet creates a delivery rule for CDN endpoint creation.</span></span>

## <span data-ttu-id="2ca63-112">示例</span><span class="sxs-lookup"><span data-stu-id="2ca63-112">EXAMPLES</span></span>

### <span data-ttu-id="2ca63-113">範例1</span><span class="sxs-lookup"><span data-stu-id="2ca63-113">Example 1</span></span>
```powershell
PS C:\> New-AzCdnDeliveryRuleAction -HeaderActionType ModifyRequestHeader -Action Append -HeaderName "Accept-Encoding" -Value "gzip"

HeaderActionType    Action HeaderName      Value
----------------    ------ ----------      -----
ModifyRequestHeader Append Accept-Encoding gzip
```

<span data-ttu-id="2ca63-114">建立簡單的傳遞規則。</span><span class="sxs-lookup"><span data-stu-id="2ca63-114">Create a simple delivery rule.</span></span>

## <span data-ttu-id="2ca63-115">參數</span><span class="sxs-lookup"><span data-stu-id="2ca63-115">PARAMETERS</span></span>

### <span data-ttu-id="2ca63-116">-動作</span><span class="sxs-lookup"><span data-stu-id="2ca63-116">-Action</span></span>
<span data-ttu-id="2ca63-117">要執行的動作。</span><span class="sxs-lookup"><span data-stu-id="2ca63-117">Action to perform.</span></span>

```yaml
Type: System.String
Parameter Sets: HeaderActionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ca63-118">-CacheBehavior</span><span class="sxs-lookup"><span data-stu-id="2ca63-118">-CacheBehavior</span></span>
<span data-ttu-id="2ca63-119">動作的快取行為</span><span class="sxs-lookup"><span data-stu-id="2ca63-119">Caching behavior for the action</span></span>

```yaml
Type: System.String
Parameter Sets: CacheExpirationActionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ca63-120">-CacheDuration</span><span class="sxs-lookup"><span data-stu-id="2ca63-120">-CacheDuration</span></span>
<span data-ttu-id="2ca63-121">內容需要緩存的持續時間。</span><span class="sxs-lookup"><span data-stu-id="2ca63-121">The duration for which the content needs to be cached.</span></span>
<span data-ttu-id="2ca63-122">允許的格式為 \[ d。 \]hh： mm： ss</span><span class="sxs-lookup"><span data-stu-id="2ca63-122">Allowed format is \[d.\]hh:mm:ss</span></span>

```yaml
Type: System.String
Parameter Sets: CacheExpirationActionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ca63-123">-CustomFragment</span><span class="sxs-lookup"><span data-stu-id="2ca63-123">-CustomFragment</span></span>
<span data-ttu-id="2ca63-124">要新增至重新導向 URL 的片段。</span><span class="sxs-lookup"><span data-stu-id="2ca63-124">Fragment to add to the redirect URL.</span></span>
<span data-ttu-id="2ca63-125">[片段] 是位於 # 之後的 URL 部分。</span><span class="sxs-lookup"><span data-stu-id="2ca63-125">Fragment is the part of the URL that comes after #.</span></span>
<span data-ttu-id="2ca63-126">請勿包含 #。</span><span class="sxs-lookup"><span data-stu-id="2ca63-126">Do not include the #.</span></span>

```yaml
Type: System.String
Parameter Sets: UrlRedirectActionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ca63-127">-CustomHostname</span><span class="sxs-lookup"><span data-stu-id="2ca63-127">-CustomHostname</span></span>
<span data-ttu-id="2ca63-128">要重新導向的主機。</span><span class="sxs-lookup"><span data-stu-id="2ca63-128">Host to redirect.</span></span>
<span data-ttu-id="2ca63-129">[留空] 可將傳入主機做為目的地主機。</span><span class="sxs-lookup"><span data-stu-id="2ca63-129">Leave empty to use the incoming host as the destination host.</span></span>

```yaml
Type: System.String
Parameter Sets: UrlRedirectActionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ca63-130">-CustomPath</span><span class="sxs-lookup"><span data-stu-id="2ca63-130">-CustomPath</span></span>
<span data-ttu-id="2ca63-131">要重新導向的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="2ca63-131">The full path to redirect.</span></span>
<span data-ttu-id="2ca63-132">Path 不能為空白，且必須以/開頭。</span><span class="sxs-lookup"><span data-stu-id="2ca63-132">Path cannot be empty and must start with /.</span></span>
<span data-ttu-id="2ca63-133">[留空] 可使用傳入路徑做為目的地路徑。</span><span class="sxs-lookup"><span data-stu-id="2ca63-133">Leave empty to use the incoming path as destination path.</span></span>

```yaml
Type: System.String
Parameter Sets: UrlRedirectActionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ca63-134">-CustomQueryString</span><span class="sxs-lookup"><span data-stu-id="2ca63-134">-CustomQueryString</span></span>
<span data-ttu-id="2ca63-135">要放在重新導向 URL 中的一組查詢字串。</span><span class="sxs-lookup"><span data-stu-id="2ca63-135">The set of query strings to be placed in the redirect URL.</span></span>
<span data-ttu-id="2ca63-136">設定此值會取代任何現有的查詢字串;保留空白以保留傳入查詢字串。</span><span class="sxs-lookup"><span data-stu-id="2ca63-136">Setting this value would replace any existing query string; leave empty to preserve the incoming query string.</span></span>
<span data-ttu-id="2ca63-137">查詢字串必須是 \< key \> = \< 值 \> 格式。</span><span class="sxs-lookup"><span data-stu-id="2ca63-137">Query string must be in \<key\>=\<value\> format.</span></span>
<span data-ttu-id="2ca63-138">?</span><span class="sxs-lookup"><span data-stu-id="2ca63-138">?</span></span> <span data-ttu-id="2ca63-139">而且 & 將會自動新增，因此不包含它們。</span><span class="sxs-lookup"><span data-stu-id="2ca63-139">and & will be added automatically so do not include them.</span></span>

```yaml
Type: System.String
Parameter Sets: UrlRedirectActionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ca63-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ca63-140">-DefaultProfile</span></span>
<span data-ttu-id="2ca63-141">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2ca63-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ca63-142">-目的地</span><span class="sxs-lookup"><span data-stu-id="2ca63-142">-Destination</span></span>
<span data-ttu-id="2ca63-143">定義上述要求將會重新寫入的相對 URL。</span><span class="sxs-lookup"><span data-stu-id="2ca63-143">Define the relative URL to which the above requests will be rewritten by.</span></span>

```yaml
Type: System.String
Parameter Sets: UrlRewriteActionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ca63-144">-DestinationProtocol</span><span class="sxs-lookup"><span data-stu-id="2ca63-144">-DestinationProtocol</span></span>
<span data-ttu-id="2ca63-145">要用於重新導向的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="2ca63-145">Protocol to use for the redirect.</span></span>
<span data-ttu-id="2ca63-146">預設值為 MatchRequest。</span><span class="sxs-lookup"><span data-stu-id="2ca63-146">The default value is MatchRequest.</span></span>

```yaml
Type: System.String
Parameter Sets: UrlRedirectActionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ca63-147">-HeaderActionType</span><span class="sxs-lookup"><span data-stu-id="2ca63-147">-HeaderActionType</span></span>
<span data-ttu-id="2ca63-148">是否修改要求標頭或回應標頭</span><span class="sxs-lookup"><span data-stu-id="2ca63-148">Whether to modify request header or response header</span></span>

```yaml
Type: System.String
Parameter Sets: HeaderActionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ca63-149">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="2ca63-149">-HeaderName</span></span>
<span data-ttu-id="2ca63-150">要修改之標頭的名稱。</span><span class="sxs-lookup"><span data-stu-id="2ca63-150">Name of the header to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: HeaderActionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ca63-151">-PreservePath</span><span class="sxs-lookup"><span data-stu-id="2ca63-151">-PreservePath</span></span>
<span data-ttu-id="2ca63-152">是否保留不成對的路徑。</span><span class="sxs-lookup"><span data-stu-id="2ca63-152">Whether to preserve unmatched path.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UrlRewriteActionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ca63-153">-QueryParameter</span><span class="sxs-lookup"><span data-stu-id="2ca63-153">-QueryParameter</span></span>
<span data-ttu-id="2ca63-154">包含或排除 (逗號分隔) 的查詢參數。</span><span class="sxs-lookup"><span data-stu-id="2ca63-154">Query parameters to include or exclude (comma separated).</span></span>

```yaml
Type: System.String[]
Parameter Sets: CacheKeyQueryStringActionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ca63-155">-QueryStringBehavior</span><span class="sxs-lookup"><span data-stu-id="2ca63-155">-QueryStringBehavior</span></span>
<span data-ttu-id="2ca63-156">要求的 QueryString 行為</span><span class="sxs-lookup"><span data-stu-id="2ca63-156">QueryString behavior for the requests</span></span>

```yaml
Type: System.String
Parameter Sets: CacheKeyQueryStringActionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ca63-157">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="2ca63-157">-RedirectType</span></span>
<span data-ttu-id="2ca63-158">當您重新導向流量時，規則將使用的重定向類型</span><span class="sxs-lookup"><span data-stu-id="2ca63-158">The redirect type the rule will use when redirecting traffic</span></span>

```yaml
Type: System.String
Parameter Sets: UrlRedirectActionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ca63-159">-SourcePattern</span><span class="sxs-lookup"><span data-stu-id="2ca63-159">-SourcePattern</span></span>
<span data-ttu-id="2ca63-160">定義標識可能要重新寫入之要求類型的要求 URI 模式。</span><span class="sxs-lookup"><span data-stu-id="2ca63-160">Define a request URI pattern that identifies the type of requests that may be rewritten.</span></span> <span data-ttu-id="2ca63-161">如果 value 為空白，則會與所有字串相符。</span><span class="sxs-lookup"><span data-stu-id="2ca63-161">If value is blank, all strings are matched.</span></span>

```yaml
Type: System.String
Parameter Sets: UrlRewriteActionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ca63-162">-值</span><span class="sxs-lookup"><span data-stu-id="2ca63-162">-Value</span></span>
<span data-ttu-id="2ca63-163">指定動作的值。</span><span class="sxs-lookup"><span data-stu-id="2ca63-163">Value for the specified action.</span></span>

```yaml
Type: System.String
Parameter Sets: HeaderActionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ca63-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ca63-164">CommonParameters</span></span>
<span data-ttu-id="2ca63-165">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2ca63-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ca63-166">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="2ca63-166">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ca63-167">輸入</span><span class="sxs-lookup"><span data-stu-id="2ca63-167">INPUTS</span></span>

### <span data-ttu-id="2ca63-168">所有</span><span class="sxs-lookup"><span data-stu-id="2ca63-168">None</span></span>

## <span data-ttu-id="2ca63-169">輸出</span><span class="sxs-lookup"><span data-stu-id="2ca63-169">OUTPUTS</span></span>

### <span data-ttu-id="2ca63-170">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleAction</span><span class="sxs-lookup"><span data-stu-id="2ca63-170">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleAction</span></span>

## <span data-ttu-id="2ca63-171">筆記</span><span class="sxs-lookup"><span data-stu-id="2ca63-171">NOTES</span></span>

## <span data-ttu-id="2ca63-172">相關連結</span><span class="sxs-lookup"><span data-stu-id="2ca63-172">RELATED LINKS</span></span>