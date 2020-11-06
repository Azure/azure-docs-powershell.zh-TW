---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: BB90E6BB-7F53-4441-A7B2-EDA940621D49
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/find-azurermresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Find-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Find-AzureRmResource.md
ms.openlocfilehash: 67389829eb5edc5ea7ac21fcc891cc85787b5e9c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450524"
---
# <span data-ttu-id="49303-101">Find-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="49303-101">Find-AzureRmResource</span></span>

## <span data-ttu-id="49303-102">摘要</span><span class="sxs-lookup"><span data-stu-id="49303-102">SYNOPSIS</span></span>
<span data-ttu-id="49303-103">根據指定的參數搜尋資源。</span><span class="sxs-lookup"><span data-stu-id="49303-103">Searches for resources based on specified parameters.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="49303-104">句法</span><span class="sxs-lookup"><span data-stu-id="49303-104">SYNTAX</span></span>

### <span data-ttu-id="49303-105">GetBySpecifiedScope (預設) </span><span class="sxs-lookup"><span data-stu-id="49303-105">GetBySpecifiedScope (Default)</span></span>
```
Find-AzureRmResource [-ResourceNameContains <String>] [-ResourceNameEquals <String>] [-ResourceType <String>]
 [-ExtensionResourceType <String>] [-Top <Int32>] [-ODataQuery <String>] [-ResourceGroupNameContains <String>]
 [-ResourceGroupNameEquals <String>] [-ExpandProperties] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="49303-106">GetBySpecifiedScopeAtTenantLevel</span><span class="sxs-lookup"><span data-stu-id="49303-106">GetBySpecifiedScopeAtTenantLevel</span></span>
```
Find-AzureRmResource [-ResourceNameContains <String>] [-ResourceNameEquals <String>] -ResourceType <String>
 [-ExtensionResourceType <String>] [-Top <Int32>] [-ODataQuery <String>] [-ExpandProperties] [-TenantLevel]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="49303-107">GetByMultiSubscriptionQuery</span><span class="sxs-lookup"><span data-stu-id="49303-107">GetByMultiSubscriptionQuery</span></span>
```
Find-AzureRmResource [-ResourceNameContains <String>] [-ResourceNameEquals <String>] -ResourceType <String>
 [-ExtensionResourceType <String>] [-Top <Int32>] [-ODataQuery <String>] [-ResourceGroupNameContains <String>]
 [-ResourceGroupNameEquals <String>] [-ExpandProperties] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="49303-108">GetByTagObject</span><span class="sxs-lookup"><span data-stu-id="49303-108">GetByTagObject</span></span>
```
Find-AzureRmResource [-Top <Int32>] [-ODataQuery <String>] [-Tag <Hashtable>] [-ExpandProperties]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="49303-109">GetByTagNameValue</span><span class="sxs-lookup"><span data-stu-id="49303-109">GetByTagNameValue</span></span>
```
Find-AzureRmResource [-Top <Int32>] [-ODataQuery <String>] [-TagName <String>] [-TagValue <String>]
 [-ExpandProperties] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="49303-110">說明</span><span class="sxs-lookup"><span data-stu-id="49303-110">DESCRIPTION</span></span>
<span data-ttu-id="49303-111">**AzureRmResource** Cmdlet 會根據指定的參數搜尋資源。</span><span class="sxs-lookup"><span data-stu-id="49303-111">The **Find-AzureRmResource** cmdlet searches for resources based on specified parameters.</span></span>

## <span data-ttu-id="49303-112">示例</span><span class="sxs-lookup"><span data-stu-id="49303-112">EXAMPLES</span></span>

### <span data-ttu-id="49303-113">範例1：依類型和資源群組名稱搜尋資源</span><span class="sxs-lookup"><span data-stu-id="49303-113">Example 1: Search for resources by type and resource group name</span></span>
```
PS C:\>Find-AzureRmResource -ResourceType "microsoft.web/sites" -ResourceGroupNameContains "ResourceGroup"
```

<span data-ttu-id="49303-114">這個命令會在名稱與字串 ResourceGroup 相符的 [資源群組] 下，搜尋類型為 [microsoft/網站] 的資源。</span><span class="sxs-lookup"><span data-stu-id="49303-114">This command searches for resources of the type microsoft.web/sites under resource groups that have names that match the string ResourceGroup.</span></span>

### <span data-ttu-id="49303-115">範例2：依類型和資源名稱搜尋資源</span><span class="sxs-lookup"><span data-stu-id="49303-115">Example 2: Search for resources by type and resource name</span></span>
```
PS C:\>Find-AzureRmResource -ResourceType "microsoft.web/sites" -ResourceNameContains "test"
```

<span data-ttu-id="49303-116">這個命令會搜尋類型為「microsoft/網站」的資源，且其資源名稱與字串測試相符。</span><span class="sxs-lookup"><span data-stu-id="49303-116">This command searches for resources of the type microsoft.web/sites that have a resource name that matches the string test.</span></span>

## <span data-ttu-id="49303-117">參數</span><span class="sxs-lookup"><span data-stu-id="49303-117">PARAMETERS</span></span>

### <span data-ttu-id="49303-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="49303-118">-ApiVersion</span></span>
<span data-ttu-id="49303-119">指定要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="49303-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="49303-120">如果您沒有指定版本，此 Cmdlet 會使用最新的可用版本。</span><span class="sxs-lookup"><span data-stu-id="49303-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="49303-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49303-121">-DefaultProfile</span></span>
<span data-ttu-id="49303-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="49303-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="49303-123">-ExpandProperties</span><span class="sxs-lookup"><span data-stu-id="49303-123">-ExpandProperties</span></span>
<span data-ttu-id="49303-124">表示此 Cmdlet 會展開資源的屬性。</span><span class="sxs-lookup"><span data-stu-id="49303-124">Indicates that this cmdlet expands the properties of the resource.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49303-125">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="49303-125">-ExtensionResourceType</span></span>
<span data-ttu-id="49303-126">指定此 Cmdlet 搜尋之資源的延伸資源類型。</span><span class="sxs-lookup"><span data-stu-id="49303-126">Specifies the extension resource type for the resources for which this cmdlet searches.</span></span>
<span data-ttu-id="49303-127">例如：</span><span class="sxs-lookup"><span data-stu-id="49303-127">For instance:</span></span>

`Microsoft.Sql/Servers/Databases`

```yaml
Type: String
Parameter Sets: GetBySpecifiedScope, GetBySpecifiedScopeAtTenantLevel, GetByMultiSubscriptionQuery
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49303-128">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="49303-128">-InformationAction</span></span>
<span data-ttu-id="49303-129">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="49303-129">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="49303-130">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="49303-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="49303-131">持續</span><span class="sxs-lookup"><span data-stu-id="49303-131">Continue</span></span>
- <span data-ttu-id="49303-132">理會</span><span class="sxs-lookup"><span data-stu-id="49303-132">Ignore</span></span>
- <span data-ttu-id="49303-133">看</span><span class="sxs-lookup"><span data-stu-id="49303-133">Inquire</span></span>
- <span data-ttu-id="49303-134">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="49303-134">SilentlyContinue</span></span>
- <span data-ttu-id="49303-135">停止</span><span class="sxs-lookup"><span data-stu-id="49303-135">Stop</span></span>
- <span data-ttu-id="49303-136">封存</span><span class="sxs-lookup"><span data-stu-id="49303-136">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49303-137">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="49303-137">-InformationVariable</span></span>
<span data-ttu-id="49303-138">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="49303-138">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49303-139">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="49303-139">-ODataQuery</span></span>
<span data-ttu-id="49303-140">指定 (OData) 樣式篩選的開放式資料通訊協定。</span><span class="sxs-lookup"><span data-stu-id="49303-140">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="49303-141">除了任何其他篩選器之外，此 Cmdlet 還會將此值附加到要求中。</span><span class="sxs-lookup"><span data-stu-id="49303-141">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="49303-142">-預先</span><span class="sxs-lookup"><span data-stu-id="49303-142">-Pre</span></span>
<span data-ttu-id="49303-143">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="49303-143">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49303-144">-ResourceGroupNameContains</span><span class="sxs-lookup"><span data-stu-id="49303-144">-ResourceGroupNameContains</span></span>
<span data-ttu-id="49303-145">指定資源群組的部分名稱。</span><span class="sxs-lookup"><span data-stu-id="49303-145">Specifies a partial name of a resource group.</span></span>
<span data-ttu-id="49303-146">這個 Cmdlet 會與此值為子字串的資源群組相符。</span><span class="sxs-lookup"><span data-stu-id="49303-146">This cmdlet matches resource groups of which this value is a substring.</span></span>
<span data-ttu-id="49303-147">這個 Cmdlet 會搜尋這些資源群組中的資源。</span><span class="sxs-lookup"><span data-stu-id="49303-147">The cmdlet searches for resources in those resource groups.</span></span>

```yaml
Type: String
Parameter Sets: GetBySpecifiedScope, GetByMultiSubscriptionQuery
Aliases: ResourceGroupName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49303-148">-ResourceGroupNameEquals</span><span class="sxs-lookup"><span data-stu-id="49303-148">-ResourceGroupNameEquals</span></span>
<span data-ttu-id="49303-149">完全符合的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="49303-149">The resource group name for a full match.</span></span>

```yaml
Type: String
Parameter Sets: GetBySpecifiedScope, GetByMultiSubscriptionQuery
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49303-150">-ResourceNameContains</span><span class="sxs-lookup"><span data-stu-id="49303-150">-ResourceNameContains</span></span>
<span data-ttu-id="49303-151">指定資源的部分名稱。</span><span class="sxs-lookup"><span data-stu-id="49303-151">Specifies a partial name of a resource.</span></span>
<span data-ttu-id="49303-152">這個 Cmdlet 會搜尋包含此值做為子字串的資源。</span><span class="sxs-lookup"><span data-stu-id="49303-152">The cmdlet searches for resources which contain this value as a substring.</span></span>

```yaml
Type: String
Parameter Sets: GetBySpecifiedScope, GetBySpecifiedScopeAtTenantLevel, GetByMultiSubscriptionQuery
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49303-153">-ResourceNameEquals</span><span class="sxs-lookup"><span data-stu-id="49303-153">-ResourceNameEquals</span></span>
<span data-ttu-id="49303-154">完全符合的資源名稱。</span><span class="sxs-lookup"><span data-stu-id="49303-154">The resource name for a full match.</span></span> <span data-ttu-id="49303-155">例如，如果您的資源名稱是 testResource，您可以指定 testResource。</span><span class="sxs-lookup"><span data-stu-id="49303-155">e.g. if your resource name is testResource, you can specify testResource.</span></span>

```yaml
Type: String
Parameter Sets: GetBySpecifiedScope, GetBySpecifiedScopeAtTenantLevel, GetByMultiSubscriptionQuery
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49303-156">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="49303-156">-ResourceType</span></span>
<span data-ttu-id="49303-157">指定資源的類型。</span><span class="sxs-lookup"><span data-stu-id="49303-157">Specifies the type of a resource.</span></span>
<span data-ttu-id="49303-158">舉例來說，對於資料庫而言，資源類型如下所示：</span><span class="sxs-lookup"><span data-stu-id="49303-158">For instance, for a database, the resource type is as follows:</span></span>

`Microsoft.Sql/Servers/Databases`

<span data-ttu-id="49303-159">這個 Cmdlet 會搜尋指定類型的資源。</span><span class="sxs-lookup"><span data-stu-id="49303-159">This cmdlet searches for resources of the specified type.</span></span>

```yaml
Type: String
Parameter Sets: GetBySpecifiedScope
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetBySpecifiedScopeAtTenantLevel, GetByMultiSubscriptionQuery
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49303-160">-Tag</span><span class="sxs-lookup"><span data-stu-id="49303-160">-Tag</span></span>
<span data-ttu-id="49303-161">OData 查詢的標記篩選器。</span><span class="sxs-lookup"><span data-stu-id="49303-161">The tag filter for the OData query.</span></span> <span data-ttu-id="49303-162">預期格式是 @ {tagName = $null} 或 @ {tagName = ' tagValue '}。</span><span class="sxs-lookup"><span data-stu-id="49303-162">The expected format is @{tagName=$null} or @{tagName = 'tagValue'}.</span></span>

```yaml
Type: Hashtable
Parameter Sets: GetByTagObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49303-163">-TagName</span><span class="sxs-lookup"><span data-stu-id="49303-163">-TagName</span></span>
```yaml
Type: String
Parameter Sets: GetByTagNameValue
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49303-164">-TagValue</span><span class="sxs-lookup"><span data-stu-id="49303-164">-TagValue</span></span>
```yaml
Type: String
Parameter Sets: GetByTagNameValue
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49303-165">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="49303-165">-TenantLevel</span></span>
<span data-ttu-id="49303-166">表示此 Cmdlet 在租使用者層級運作。</span><span class="sxs-lookup"><span data-stu-id="49303-166">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: GetBySpecifiedScopeAtTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49303-167">-上方</span><span class="sxs-lookup"><span data-stu-id="49303-167">-Top</span></span>
<span data-ttu-id="49303-168">指定要檢索的資源數。</span><span class="sxs-lookup"><span data-stu-id="49303-168">Specifies the number of resources to retrieve.</span></span>

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

### <span data-ttu-id="49303-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49303-169">CommonParameters</span></span>
<span data-ttu-id="49303-170">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="49303-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49303-171">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="49303-171">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49303-172">輸入</span><span class="sxs-lookup"><span data-stu-id="49303-172">INPUTS</span></span>

### <span data-ttu-id="49303-173">所有</span><span class="sxs-lookup"><span data-stu-id="49303-173">None</span></span>
<span data-ttu-id="49303-174">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="49303-174">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="49303-175">輸出</span><span class="sxs-lookup"><span data-stu-id="49303-175">OUTPUTS</span></span>

### <span data-ttu-id="49303-176">系統管理. PSObject</span><span class="sxs-lookup"><span data-stu-id="49303-176">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="49303-177">筆記</span><span class="sxs-lookup"><span data-stu-id="49303-177">NOTES</span></span>

## <span data-ttu-id="49303-178">相關連結</span><span class="sxs-lookup"><span data-stu-id="49303-178">RELATED LINKS</span></span>

[<span data-ttu-id="49303-179">AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="49303-179">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="49303-180">移動流覽 AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="49303-180">Move-AzureRmResource</span></span>](./Move-AzureRmResource.md)

[<span data-ttu-id="49303-181">新-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="49303-181">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="49303-182">移除-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="49303-182">Remove-AzureRmResource</span></span>](./Remove-AzureRmResource.md)

[<span data-ttu-id="49303-183">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="49303-183">Set-AzureRmResource</span></span>](./Set-AzureRmResource.md)
