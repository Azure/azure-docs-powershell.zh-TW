---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdndeliveryruleaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleAction.md
ms.openlocfilehash: a1ebadb47bbde091ca6b430fab86111b35bf34bc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93613529"
---
# <span data-ttu-id="64ab1-101">New-AzCdnDeliveryRuleAction</span><span class="sxs-lookup"><span data-stu-id="64ab1-101">New-AzCdnDeliveryRuleAction</span></span>

## <span data-ttu-id="64ab1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="64ab1-102">SYNOPSIS</span></span>
<span data-ttu-id="64ab1-103">建立傳遞動作。</span><span class="sxs-lookup"><span data-stu-id="64ab1-103">Creates a delivery action.</span></span>

## <span data-ttu-id="64ab1-104">句法</span><span class="sxs-lookup"><span data-stu-id="64ab1-104">SYNTAX</span></span>

### <span data-ttu-id="64ab1-105">CacheExpirationActionParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="64ab1-105">CacheExpirationActionParameterSet (Default)</span></span>
```
New-AzCdnDeliveryRuleAction -CacheBehavior <String> [-CacheDuration <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="64ab1-106">HeaderActionParameterSet</span><span class="sxs-lookup"><span data-stu-id="64ab1-106">HeaderActionParameterSet</span></span>
```
New-AzCdnDeliveryRuleAction -HeaderActionType <String> -Action <String> -HeaderName <String> [-Value <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="64ab1-107">UrlRedirectActionParameterSet</span><span class="sxs-lookup"><span data-stu-id="64ab1-107">UrlRedirectActionParameterSet</span></span>
```
New-AzCdnDeliveryRuleAction -RedirectType <String> [-DestinationProtocol <String>] [-CustomPath <String>]
 [-CustomHostname <String>] [-CustomQueryString <String>] [-CustomFragment <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="64ab1-108">說明</span><span class="sxs-lookup"><span data-stu-id="64ab1-108">DESCRIPTION</span></span>
<span data-ttu-id="64ab1-109">**新的-AzCdnDeliveryRule** Cmdlet 會建立 CDN 端點建立的傳遞規則。</span><span class="sxs-lookup"><span data-stu-id="64ab1-109">The **New-AzCdnDeliveryRule** cmdlet creates a delivery rule for CDN endpoint creation.</span></span>

## <span data-ttu-id="64ab1-110">示例</span><span class="sxs-lookup"><span data-stu-id="64ab1-110">EXAMPLES</span></span>

### <span data-ttu-id="64ab1-111">範例1</span><span class="sxs-lookup"><span data-stu-id="64ab1-111">Example 1</span></span>
```powershell
PS C:\> New-AzCdnDeliveryRuleAction -HeaderActionType ModifyRequestHeader -Action Append -HeaderName "Accept-Encoding" -Value "gzip"

HeaderActionType    Action HeaderName      Value
----------------    ------ ----------      -----
ModifyRequestHeader Append Accept-Encoding gzip
```

<span data-ttu-id="64ab1-112">建立簡單的傳遞規則。</span><span class="sxs-lookup"><span data-stu-id="64ab1-112">Create a simple delivery rule.</span></span>

## <span data-ttu-id="64ab1-113">參數</span><span class="sxs-lookup"><span data-stu-id="64ab1-113">PARAMETERS</span></span>

### <span data-ttu-id="64ab1-114">-動作</span><span class="sxs-lookup"><span data-stu-id="64ab1-114">-Action</span></span>
<span data-ttu-id="64ab1-115">要執行的動作。</span><span class="sxs-lookup"><span data-stu-id="64ab1-115">Action to perform.</span></span>

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

### <span data-ttu-id="64ab1-116">-CacheBehavior</span><span class="sxs-lookup"><span data-stu-id="64ab1-116">-CacheBehavior</span></span>
<span data-ttu-id="64ab1-117">動作的快取行為</span><span class="sxs-lookup"><span data-stu-id="64ab1-117">Caching behavior for the action</span></span>

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

### <span data-ttu-id="64ab1-118">-CacheDuration</span><span class="sxs-lookup"><span data-stu-id="64ab1-118">-CacheDuration</span></span>
<span data-ttu-id="64ab1-119">內容需要緩存的持續時間。</span><span class="sxs-lookup"><span data-stu-id="64ab1-119">The duration for which the content needs to be cached.</span></span>
<span data-ttu-id="64ab1-120">允許的格式為 \[ d。 \]hh： mm： ss</span><span class="sxs-lookup"><span data-stu-id="64ab1-120">Allowed format is \[d.\]hh:mm:ss</span></span>

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

### <span data-ttu-id="64ab1-121">-CustomFragment</span><span class="sxs-lookup"><span data-stu-id="64ab1-121">-CustomFragment</span></span>
<span data-ttu-id="64ab1-122">要新增至重新導向 URL 的片段。</span><span class="sxs-lookup"><span data-stu-id="64ab1-122">Fragment to add to the redirect URL.</span></span>
<span data-ttu-id="64ab1-123">[片段] 是位於 # 之後的 URL 部分。</span><span class="sxs-lookup"><span data-stu-id="64ab1-123">Fragment is the part of the URL that comes after #.</span></span>
<span data-ttu-id="64ab1-124">請勿包含 #。</span><span class="sxs-lookup"><span data-stu-id="64ab1-124">Do not include the #.</span></span>

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

### <span data-ttu-id="64ab1-125">-CustomHostname</span><span class="sxs-lookup"><span data-stu-id="64ab1-125">-CustomHostname</span></span>
<span data-ttu-id="64ab1-126">要重新導向的主機。</span><span class="sxs-lookup"><span data-stu-id="64ab1-126">Host to redirect.</span></span>
<span data-ttu-id="64ab1-127">[留空] 可將傳入主機做為目的地主機。</span><span class="sxs-lookup"><span data-stu-id="64ab1-127">Leave empty to use the incoming host as the destination host.</span></span>

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

### <span data-ttu-id="64ab1-128">-CustomPath</span><span class="sxs-lookup"><span data-stu-id="64ab1-128">-CustomPath</span></span>
<span data-ttu-id="64ab1-129">要重新導向的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="64ab1-129">The full path to redirect.</span></span>
<span data-ttu-id="64ab1-130">Path 不能為空白，且必須以/開頭。</span><span class="sxs-lookup"><span data-stu-id="64ab1-130">Path cannot be empty and must start with /.</span></span>
<span data-ttu-id="64ab1-131">[留空] 可使用傳入路徑做為目的地路徑。</span><span class="sxs-lookup"><span data-stu-id="64ab1-131">Leave empty to use the incoming path as destination path.</span></span>

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

### <span data-ttu-id="64ab1-132">-CustomQueryString</span><span class="sxs-lookup"><span data-stu-id="64ab1-132">-CustomQueryString</span></span>
<span data-ttu-id="64ab1-133">要放在重新導向 URL 中的一組查詢字串。</span><span class="sxs-lookup"><span data-stu-id="64ab1-133">The set of query strings to be placed in the redirect URL.</span></span>
<span data-ttu-id="64ab1-134">設定此值會取代任何現有的查詢字串;保留空白以保留傳入查詢字串。</span><span class="sxs-lookup"><span data-stu-id="64ab1-134">Setting this value would replace any existing query string; leave empty to preserve the incoming query string.</span></span>
<span data-ttu-id="64ab1-135">查詢字串必須是 \< key \> = \< 值 \> 格式。</span><span class="sxs-lookup"><span data-stu-id="64ab1-135">Query string must be in \<key\>=\<value\> format.</span></span>
<span data-ttu-id="64ab1-136">?</span><span class="sxs-lookup"><span data-stu-id="64ab1-136">?</span></span> <span data-ttu-id="64ab1-137">而且 & 將會自動新增，因此不包含它們。</span><span class="sxs-lookup"><span data-stu-id="64ab1-137">and & will be added automatically so do not include them.</span></span>

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

### <span data-ttu-id="64ab1-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64ab1-138">-DefaultProfile</span></span>
<span data-ttu-id="64ab1-139">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="64ab1-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="64ab1-140">-DestinationProtocol</span><span class="sxs-lookup"><span data-stu-id="64ab1-140">-DestinationProtocol</span></span>
<span data-ttu-id="64ab1-141">要用於重新導向的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="64ab1-141">Protocol to use for the redirect.</span></span>
<span data-ttu-id="64ab1-142">預設值為 MatchRequest。</span><span class="sxs-lookup"><span data-stu-id="64ab1-142">The default value is MatchRequest.</span></span>

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

### <span data-ttu-id="64ab1-143">-HeaderActionType</span><span class="sxs-lookup"><span data-stu-id="64ab1-143">-HeaderActionType</span></span>
<span data-ttu-id="64ab1-144">是否修改要求標頭或回應標頭</span><span class="sxs-lookup"><span data-stu-id="64ab1-144">Whether to modify request header or response header</span></span>

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

### <span data-ttu-id="64ab1-145">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="64ab1-145">-HeaderName</span></span>
<span data-ttu-id="64ab1-146">要修改之標頭的名稱。</span><span class="sxs-lookup"><span data-stu-id="64ab1-146">Name of the header to modify.</span></span>

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

### <span data-ttu-id="64ab1-147">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="64ab1-147">-RedirectType</span></span>
<span data-ttu-id="64ab1-148">當您重新導向流量時，規則將使用的重定向類型</span><span class="sxs-lookup"><span data-stu-id="64ab1-148">The redirect type the rule will use when redirecting traffic</span></span>

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

### <span data-ttu-id="64ab1-149">-值</span><span class="sxs-lookup"><span data-stu-id="64ab1-149">-Value</span></span>
<span data-ttu-id="64ab1-150">指定動作的值。</span><span class="sxs-lookup"><span data-stu-id="64ab1-150">Value for the specified action.</span></span>

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

### <span data-ttu-id="64ab1-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64ab1-151">CommonParameters</span></span>
<span data-ttu-id="64ab1-152">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="64ab1-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64ab1-153">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="64ab1-153">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64ab1-154">輸入</span><span class="sxs-lookup"><span data-stu-id="64ab1-154">INPUTS</span></span>

### <span data-ttu-id="64ab1-155">所有</span><span class="sxs-lookup"><span data-stu-id="64ab1-155">None</span></span>

## <span data-ttu-id="64ab1-156">輸出</span><span class="sxs-lookup"><span data-stu-id="64ab1-156">OUTPUTS</span></span>

### <span data-ttu-id="64ab1-157">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleAction</span><span class="sxs-lookup"><span data-stu-id="64ab1-157">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleAction</span></span>

## <span data-ttu-id="64ab1-158">筆記</span><span class="sxs-lookup"><span data-stu-id="64ab1-158">NOTES</span></span>

## <span data-ttu-id="64ab1-159">相關連結</span><span class="sxs-lookup"><span data-stu-id="64ab1-159">RELATED LINKS</span></span>
