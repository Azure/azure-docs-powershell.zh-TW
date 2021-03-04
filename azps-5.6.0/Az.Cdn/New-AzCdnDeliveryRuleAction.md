---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/powershell/module/az.cdn/new-azcdndeliveryruleaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleAction.md
ms.openlocfilehash: 127c73a34b030a991b5875f141ea8dd850a4f0a1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916582"
---
# <span data-ttu-id="feb1f-101">New-AzCdnDeliveryRuleAction</span><span class="sxs-lookup"><span data-stu-id="feb1f-101">New-AzCdnDeliveryRuleAction</span></span>

## <span data-ttu-id="feb1f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="feb1f-102">SYNOPSIS</span></span>
<span data-ttu-id="feb1f-103">建立傳遞動作。</span><span class="sxs-lookup"><span data-stu-id="feb1f-103">Creates a delivery action.</span></span>

## <span data-ttu-id="feb1f-104">語法</span><span class="sxs-lookup"><span data-stu-id="feb1f-104">SYNTAX</span></span>

### <span data-ttu-id="feb1f-105">CacheExpirationActionParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="feb1f-105">CacheExpirationActionParameterSet (Default)</span></span>
```
New-AzCdnDeliveryRuleAction -CacheBehavior <String> [-CacheDuration <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="feb1f-106">HeaderActionParameterSet</span><span class="sxs-lookup"><span data-stu-id="feb1f-106">HeaderActionParameterSet</span></span>
```
New-AzCdnDeliveryRuleAction -HeaderActionType <String> -Action <String> -HeaderName <String> [-Value <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="feb1f-107">UrlRedirectActionParameterSet</span><span class="sxs-lookup"><span data-stu-id="feb1f-107">UrlRedirectActionParameterSet</span></span>
```
New-AzCdnDeliveryRuleAction -RedirectType <String> [-DestinationProtocol <String>] [-CustomPath <String>]
 [-CustomHostname <String>] [-CustomQueryString <String>] [-CustomFragment <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="feb1f-108">CacheKeyQueryStringActionParameterSet</span><span class="sxs-lookup"><span data-stu-id="feb1f-108">CacheKeyQueryStringActionParameterSet</span></span>
```
New-AzCdnDeliveryRuleAction -QueryStringBehavior <String> [-QueryParameter <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="feb1f-109">UrlRewriteActionParameterSet</span><span class="sxs-lookup"><span data-stu-id="feb1f-109">UrlRewriteActionParameterSet</span></span>
```
New-AzCdnDeliveryRuleAction -SourcePattern <String> -Destination <String> [-PreservePath]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="feb1f-110">描述</span><span class="sxs-lookup"><span data-stu-id="feb1f-110">DESCRIPTION</span></span>
<span data-ttu-id="feb1f-111">**New-AzCdnDeliveryRule** Cmdlet 會建立 CDN 端點的建立傳遞規則。</span><span class="sxs-lookup"><span data-stu-id="feb1f-111">The **New-AzCdnDeliveryRule** cmdlet creates a delivery rule for CDN endpoint creation.</span></span>

## <span data-ttu-id="feb1f-112">例子</span><span class="sxs-lookup"><span data-stu-id="feb1f-112">EXAMPLES</span></span>

### <span data-ttu-id="feb1f-113">範例 1</span><span class="sxs-lookup"><span data-stu-id="feb1f-113">Example 1</span></span>
```powershell
PS C:\> New-AzCdnDeliveryRuleAction -HeaderActionType ModifyRequestHeader -Action Append -HeaderName "Accept-Encoding" -Value "gzip"

HeaderActionType    Action HeaderName      Value
----------------    ------ ----------      -----
ModifyRequestHeader Append Accept-Encoding gzip
```

<span data-ttu-id="feb1f-114">建立簡單的傳遞規則。</span><span class="sxs-lookup"><span data-stu-id="feb1f-114">Create a simple delivery rule.</span></span>

## <span data-ttu-id="feb1f-115">參數</span><span class="sxs-lookup"><span data-stu-id="feb1f-115">PARAMETERS</span></span>

### <span data-ttu-id="feb1f-116">-動作</span><span class="sxs-lookup"><span data-stu-id="feb1f-116">-Action</span></span>
<span data-ttu-id="feb1f-117">要執行的動作。</span><span class="sxs-lookup"><span data-stu-id="feb1f-117">Action to perform.</span></span>

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

### <span data-ttu-id="feb1f-118">-CacheBehavior</span><span class="sxs-lookup"><span data-stu-id="feb1f-118">-CacheBehavior</span></span>
<span data-ttu-id="feb1f-119">動作的緩存行為</span><span class="sxs-lookup"><span data-stu-id="feb1f-119">Caching behavior for the action</span></span>

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

### <span data-ttu-id="feb1f-120">-CacheDuration</span><span class="sxs-lookup"><span data-stu-id="feb1f-120">-CacheDuration</span></span>
<span data-ttu-id="feb1f-121">需要緩存內容的持續時間。</span><span class="sxs-lookup"><span data-stu-id="feb1f-121">The duration for which the content needs to be cached.</span></span>
<span data-ttu-id="feb1f-122">允許的格式 \[ 為 d。 \]hh：mm：ss</span><span class="sxs-lookup"><span data-stu-id="feb1f-122">Allowed format is \[d.\]hh:mm:ss</span></span>

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

### <span data-ttu-id="feb1f-123">-CustomFragment</span><span class="sxs-lookup"><span data-stu-id="feb1f-123">-CustomFragment</span></span>
<span data-ttu-id="feb1f-124">要新加入重新導向 URL 的片段。</span><span class="sxs-lookup"><span data-stu-id="feb1f-124">Fragment to add to the redirect URL.</span></span>
<span data-ttu-id="feb1f-125">片段是 #之後 URL 的一部分。</span><span class="sxs-lookup"><span data-stu-id="feb1f-125">Fragment is the part of the URL that comes after #.</span></span>
<span data-ttu-id="feb1f-126">請勿包含 #。</span><span class="sxs-lookup"><span data-stu-id="feb1f-126">Do not include the #.</span></span>

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

### <span data-ttu-id="feb1f-127">-CustomHostname</span><span class="sxs-lookup"><span data-stu-id="feb1f-127">-CustomHostname</span></span>
<span data-ttu-id="feb1f-128">要重新導向的主機。</span><span class="sxs-lookup"><span data-stu-id="feb1f-128">Host to redirect.</span></span>
<span data-ttu-id="feb1f-129">保留空白，以使用內接主機做為目的地主機。</span><span class="sxs-lookup"><span data-stu-id="feb1f-129">Leave empty to use the incoming host as the destination host.</span></span>

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

### <span data-ttu-id="feb1f-130">-CustomPath</span><span class="sxs-lookup"><span data-stu-id="feb1f-130">-CustomPath</span></span>
<span data-ttu-id="feb1f-131">重新導向的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="feb1f-131">The full path to redirect.</span></span>
<span data-ttu-id="feb1f-132">路徑不能是空白的，必須以 /開始。</span><span class="sxs-lookup"><span data-stu-id="feb1f-132">Path cannot be empty and must start with /.</span></span>
<span data-ttu-id="feb1f-133">保留空白，以使用內入路徑做為目的地路徑。</span><span class="sxs-lookup"><span data-stu-id="feb1f-133">Leave empty to use the incoming path as destination path.</span></span>

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

### <span data-ttu-id="feb1f-134">-CustomQueryString</span><span class="sxs-lookup"><span data-stu-id="feb1f-134">-CustomQueryString</span></span>
<span data-ttu-id="feb1f-135">這是要放在重新導向 URL 中的查詢字串集。</span><span class="sxs-lookup"><span data-stu-id="feb1f-135">The set of query strings to be placed in the redirect URL.</span></span>
<span data-ttu-id="feb1f-136">設定此值會取代任何現有的查詢字串;保留空白以保留傳入查詢字串。</span><span class="sxs-lookup"><span data-stu-id="feb1f-136">Setting this value would replace any existing query string; leave empty to preserve the incoming query string.</span></span>
<span data-ttu-id="feb1f-137">查詢字串必須採用 \<key\> = \<value\> 格式。</span><span class="sxs-lookup"><span data-stu-id="feb1f-137">Query string must be in \<key\>=\<value\> format.</span></span>
<span data-ttu-id="feb1f-138">?</span><span class="sxs-lookup"><span data-stu-id="feb1f-138">?</span></span> <span data-ttu-id="feb1f-139">並且&自動新增，因此請勿包含它們。</span><span class="sxs-lookup"><span data-stu-id="feb1f-139">and & will be added automatically so do not include them.</span></span>

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

### <span data-ttu-id="feb1f-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="feb1f-140">-DefaultProfile</span></span>
<span data-ttu-id="feb1f-141">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="feb1f-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="feb1f-142">-目的地</span><span class="sxs-lookup"><span data-stu-id="feb1f-142">-Destination</span></span>
<span data-ttu-id="feb1f-143">定義將重寫上述要求的相對 URL。</span><span class="sxs-lookup"><span data-stu-id="feb1f-143">Define the relative URL to which the above requests will be rewritten by.</span></span>

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

### <span data-ttu-id="feb1f-144">-DestinationProtocol</span><span class="sxs-lookup"><span data-stu-id="feb1f-144">-DestinationProtocol</span></span>
<span data-ttu-id="feb1f-145">用於重新導向的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="feb1f-145">Protocol to use for the redirect.</span></span>
<span data-ttu-id="feb1f-146">預設值為 MatchRequest。</span><span class="sxs-lookup"><span data-stu-id="feb1f-146">The default value is MatchRequest.</span></span>

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

### <span data-ttu-id="feb1f-147">-HeaderActionType</span><span class="sxs-lookup"><span data-stu-id="feb1f-147">-HeaderActionType</span></span>
<span data-ttu-id="feb1f-148">是否要修改要求標題或回應標頭</span><span class="sxs-lookup"><span data-stu-id="feb1f-148">Whether to modify request header or response header</span></span>

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

### <span data-ttu-id="feb1f-149">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="feb1f-149">-HeaderName</span></span>
<span data-ttu-id="feb1f-150">要修改的標題名稱。</span><span class="sxs-lookup"><span data-stu-id="feb1f-150">Name of the header to modify.</span></span>

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

### <span data-ttu-id="feb1f-151">-PreservePath</span><span class="sxs-lookup"><span data-stu-id="feb1f-151">-PreservePath</span></span>
<span data-ttu-id="feb1f-152">是否要保留不一樣的路徑。</span><span class="sxs-lookup"><span data-stu-id="feb1f-152">Whether to preserve unmatched path.</span></span>

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

### <span data-ttu-id="feb1f-153">-QueryParameter</span><span class="sxs-lookup"><span data-stu-id="feb1f-153">-QueryParameter</span></span>
<span data-ttu-id="feb1f-154">要包含或排除逗號分隔 (的查詢) 。</span><span class="sxs-lookup"><span data-stu-id="feb1f-154">Query parameters to include or exclude (comma separated).</span></span>

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

### <span data-ttu-id="feb1f-155">-QueryStringBehavior</span><span class="sxs-lookup"><span data-stu-id="feb1f-155">-QueryStringBehavior</span></span>
<span data-ttu-id="feb1f-156">要求查詢字串行為</span><span class="sxs-lookup"><span data-stu-id="feb1f-156">QueryString behavior for the requests</span></span>

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

### <span data-ttu-id="feb1f-157">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="feb1f-157">-RedirectType</span></span>
<span data-ttu-id="feb1f-158">重新導向流量時，規則會使用的重新導向類型</span><span class="sxs-lookup"><span data-stu-id="feb1f-158">The redirect type the rule will use when redirecting traffic</span></span>

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

### <span data-ttu-id="feb1f-159">-SourcePattern</span><span class="sxs-lookup"><span data-stu-id="feb1f-159">-SourcePattern</span></span>
<span data-ttu-id="feb1f-160">定義可識別可重寫之要求類型的要求 URI 模式。</span><span class="sxs-lookup"><span data-stu-id="feb1f-160">Define a request URI pattern that identifies the type of requests that may be rewritten.</span></span> <span data-ttu-id="feb1f-161">如果值為空白，則所有字串都相符。</span><span class="sxs-lookup"><span data-stu-id="feb1f-161">If value is blank, all strings are matched.</span></span>

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

### <span data-ttu-id="feb1f-162">-值</span><span class="sxs-lookup"><span data-stu-id="feb1f-162">-Value</span></span>
<span data-ttu-id="feb1f-163">指定動作的值。</span><span class="sxs-lookup"><span data-stu-id="feb1f-163">Value for the specified action.</span></span>

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

### <span data-ttu-id="feb1f-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="feb1f-164">CommonParameters</span></span>
<span data-ttu-id="feb1f-165">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="feb1f-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="feb1f-166">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="feb1f-166">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="feb1f-167">輸入</span><span class="sxs-lookup"><span data-stu-id="feb1f-167">INPUTS</span></span>

### <span data-ttu-id="feb1f-168">沒有</span><span class="sxs-lookup"><span data-stu-id="feb1f-168">None</span></span>

## <span data-ttu-id="feb1f-169">輸出</span><span class="sxs-lookup"><span data-stu-id="feb1f-169">OUTPUTS</span></span>

### <span data-ttu-id="feb1f-170">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSD力RuleAction</span><span class="sxs-lookup"><span data-stu-id="feb1f-170">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleAction</span></span>

## <span data-ttu-id="feb1f-171">筆記</span><span class="sxs-lookup"><span data-stu-id="feb1f-171">NOTES</span></span>

## <span data-ttu-id="feb1f-172">相關連結</span><span class="sxs-lookup"><span data-stu-id="feb1f-172">RELATED LINKS</span></span>
