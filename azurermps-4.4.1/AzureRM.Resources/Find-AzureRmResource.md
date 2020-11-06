---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: BB90E6BB-7F53-4441-A7B2-EDA940621D49
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Find-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Find-AzureRmResource.md
ms.openlocfilehash: e626a57088a9c726bfe9040f76157f0b011a6405
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448010"
---
# <span data-ttu-id="037e7-101">Find-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="037e7-101">Find-AzureRmResource</span></span>

## <span data-ttu-id="037e7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="037e7-102">SYNOPSIS</span></span>
<span data-ttu-id="037e7-103">根據指定的參數搜尋資源。</span><span class="sxs-lookup"><span data-stu-id="037e7-103">Searches for resources based on specified parameters.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="037e7-104">句法</span><span class="sxs-lookup"><span data-stu-id="037e7-104">SYNTAX</span></span>

### <span data-ttu-id="037e7-105">根據指定的範圍列出資源。</span><span class="sxs-lookup"><span data-stu-id="037e7-105">Lists the resources based on the specified scope.</span></span> <span data-ttu-id="037e7-106"> (預設) </span><span class="sxs-lookup"><span data-stu-id="037e7-106">(Default)</span></span>
```
Find-AzureRmResource [-ResourceNameContains <String>] [-ResourceNameEquals <String>] [-ResourceType <String>]
 [-ExtensionResourceType <String>] [-Top <Int32>] [-ODataQuery <String>] [-ResourceGroupNameContains <String>]
 [-ResourceGroupNameEquals <String>] [-ExpandProperties] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="037e7-107">根據租使用者層級的指定範圍列出資源。</span><span class="sxs-lookup"><span data-stu-id="037e7-107">Lists the resources based on the specified scope at the tenant level.</span></span>
```
Find-AzureRmResource [-ResourceNameContains <String>] [-ResourceNameEquals <String>] -ResourceType <String>
 [-ExtensionResourceType <String>] [-Top <Int32>] [-ODataQuery <String>] [-ExpandProperties] [-TenantLevel]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="037e7-108">使用多重訂閱查詢取得資源。</span><span class="sxs-lookup"><span data-stu-id="037e7-108">Get a resources using a multi-subscription query.</span></span>
```
Find-AzureRmResource [-ResourceNameContains <String>] [-ResourceNameEquals <String>] -ResourceType <String>
 [-ExtensionResourceType <String>] [-Top <Int32>] [-ODataQuery <String>] [-ResourceGroupNameContains <String>]
 [-ResourceGroupNameEquals <String>] [-ExpandProperties] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="037e7-109">依指定為 hashset 的標記物件列出資源。</span><span class="sxs-lookup"><span data-stu-id="037e7-109">Lists resources by a tag object specified as a hashset.</span></span>
```
Find-AzureRmResource [-Top <Int32>] [-ODataQuery <String>] [-Tag <Hashtable>] [-ExpandProperties]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="037e7-110">依指定為個別名稱和值參數的標記列出資源。</span><span class="sxs-lookup"><span data-stu-id="037e7-110">Lists resources by a tag specified as a individual name and value parameters.</span></span>
```
Find-AzureRmResource [-Top <Int32>] [-ODataQuery <String>] [-TagName <String>] [-TagValue <String>]
 [-ExpandProperties] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="037e7-111">說明</span><span class="sxs-lookup"><span data-stu-id="037e7-111">DESCRIPTION</span></span>
<span data-ttu-id="037e7-112">**AzureRmResource** Cmdlet 會根據指定的參數搜尋資源。</span><span class="sxs-lookup"><span data-stu-id="037e7-112">The **Find-AzureRmResource** cmdlet searches for resources based on specified parameters.</span></span>

## <span data-ttu-id="037e7-113">示例</span><span class="sxs-lookup"><span data-stu-id="037e7-113">EXAMPLES</span></span>

### <span data-ttu-id="037e7-114">範例1：依類型和資源群組名稱搜尋資源</span><span class="sxs-lookup"><span data-stu-id="037e7-114">Example 1: Search for resources by type and resource group name</span></span>
```
PS C:\>Find-AzureRmResource -ResourceType "microsoft.web/sites" -ResourceGroupNameContains "ResourceGroup"
```

<span data-ttu-id="037e7-115">這個命令會在名稱與字串 ResourceGroup 相符的 [資源群組] 下，搜尋類型為 [microsoft/網站] 的資源。</span><span class="sxs-lookup"><span data-stu-id="037e7-115">This command searches for resources of the type microsoft.web/sites under resource groups that have names that match the string ResourceGroup.</span></span>

### <span data-ttu-id="037e7-116">範例2：依類型和資源名稱搜尋資源</span><span class="sxs-lookup"><span data-stu-id="037e7-116">Example 2: Search for resources by type and resource name</span></span>
```
PS C:\>Find-AzureRmResource -ResourceType "microsoft.web/sites" -ResourceNameContains "test"
```

<span data-ttu-id="037e7-117">這個命令會搜尋類型為「microsoft/網站」的資源，且其資源名稱與字串測試相符。</span><span class="sxs-lookup"><span data-stu-id="037e7-117">This command searches for resources of the type microsoft.web/sites that have a resource name that matches the string test.</span></span>

## <span data-ttu-id="037e7-118">參數</span><span class="sxs-lookup"><span data-stu-id="037e7-118">PARAMETERS</span></span>

### <span data-ttu-id="037e7-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="037e7-119">-ApiVersion</span></span>
<span data-ttu-id="037e7-120">指定要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="037e7-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="037e7-121">如果您沒有指定版本，此 Cmdlet 會使用最新的可用版本。</span><span class="sxs-lookup"><span data-stu-id="037e7-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="037e7-122">-ExpandProperties</span><span class="sxs-lookup"><span data-stu-id="037e7-122">-ExpandProperties</span></span>
<span data-ttu-id="037e7-123">表示此 Cmdlet 會展開資源的屬性。</span><span class="sxs-lookup"><span data-stu-id="037e7-123">Indicates that this cmdlet expands the properties of the resource.</span></span>

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

### <span data-ttu-id="037e7-124">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="037e7-124">-ExtensionResourceType</span></span>
<span data-ttu-id="037e7-125">指定此 Cmdlet 搜尋之資源的延伸資源類型。</span><span class="sxs-lookup"><span data-stu-id="037e7-125">Specifies the extension resource type for the resources for which this cmdlet searches.</span></span>
<span data-ttu-id="037e7-126">例如：</span><span class="sxs-lookup"><span data-stu-id="037e7-126">For instance:</span></span>

`Microsoft.Sql/Servers/Databases`

```yaml
Type: System.String
Parameter Sets: Lists the resources based on the specified scope., Lists the resources based on the specified scope at the tenant level., Get a resources using a multi-subscription query.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="037e7-127">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="037e7-127">-InformationAction</span></span>
<span data-ttu-id="037e7-128">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="037e7-128">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="037e7-129">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="037e7-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="037e7-130">持續</span><span class="sxs-lookup"><span data-stu-id="037e7-130">Continue</span></span>
- <span data-ttu-id="037e7-131">理會</span><span class="sxs-lookup"><span data-stu-id="037e7-131">Ignore</span></span>
- <span data-ttu-id="037e7-132">看</span><span class="sxs-lookup"><span data-stu-id="037e7-132">Inquire</span></span>
- <span data-ttu-id="037e7-133">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="037e7-133">SilentlyContinue</span></span>
- <span data-ttu-id="037e7-134">停止</span><span class="sxs-lookup"><span data-stu-id="037e7-134">Stop</span></span>
- <span data-ttu-id="037e7-135">封存</span><span class="sxs-lookup"><span data-stu-id="037e7-135">Suspend</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="037e7-136">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="037e7-136">-InformationVariable</span></span>
<span data-ttu-id="037e7-137">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="037e7-137">Specifies an information variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="037e7-138">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="037e7-138">-ODataQuery</span></span>
<span data-ttu-id="037e7-139">指定 (OData) 樣式篩選的開放式資料通訊協定。</span><span class="sxs-lookup"><span data-stu-id="037e7-139">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="037e7-140">除了任何其他篩選器之外，此 Cmdlet 還會將此值附加到要求中。</span><span class="sxs-lookup"><span data-stu-id="037e7-140">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="037e7-141">-預先</span><span class="sxs-lookup"><span data-stu-id="037e7-141">-Pre</span></span>
<span data-ttu-id="037e7-142">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="037e7-142">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="037e7-143">-ResourceGroupNameContains</span><span class="sxs-lookup"><span data-stu-id="037e7-143">-ResourceGroupNameContains</span></span>
<span data-ttu-id="037e7-144">指定資源群組的部分名稱。</span><span class="sxs-lookup"><span data-stu-id="037e7-144">Specifies a partial name of a resource group.</span></span>
<span data-ttu-id="037e7-145">這個 Cmdlet 會與此值為子字串的資源群組相符。</span><span class="sxs-lookup"><span data-stu-id="037e7-145">This cmdlet matches resource groups of which this value is a substring.</span></span>
<span data-ttu-id="037e7-146">這個 Cmdlet 會搜尋這些資源群組中的資源。</span><span class="sxs-lookup"><span data-stu-id="037e7-146">The cmdlet searches for resources in those resource groups.</span></span>

```yaml
Type: System.String
Parameter Sets: Lists the resources based on the specified scope., Get a resources using a multi-subscription query.
Aliases: ResourceGroupName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="037e7-147">-ResourceGroupNameEquals</span><span class="sxs-lookup"><span data-stu-id="037e7-147">-ResourceGroupNameEquals</span></span>
<span data-ttu-id="037e7-148">完全符合的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="037e7-148">The resource group name for a full match.</span></span>

```yaml
Type: System.String
Parameter Sets: Lists the resources based on the specified scope., Get a resources using a multi-subscription query.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="037e7-149">-ResourceNameContains</span><span class="sxs-lookup"><span data-stu-id="037e7-149">-ResourceNameContains</span></span>
<span data-ttu-id="037e7-150">指定資源的部分名稱。</span><span class="sxs-lookup"><span data-stu-id="037e7-150">Specifies a partial name of a resource.</span></span>
<span data-ttu-id="037e7-151">這個 Cmdlet 會搜尋包含此值做為子字串的資源。</span><span class="sxs-lookup"><span data-stu-id="037e7-151">The cmdlet searches for resources which contain this value as a substring.</span></span>

```yaml
Type: System.String
Parameter Sets: Lists the resources based on the specified scope., Lists the resources based on the specified scope at the tenant level., Get a resources using a multi-subscription query.
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="037e7-152">-ResourceNameEquals</span><span class="sxs-lookup"><span data-stu-id="037e7-152">-ResourceNameEquals</span></span>
<span data-ttu-id="037e7-153">完全符合的資源名稱。</span><span class="sxs-lookup"><span data-stu-id="037e7-153">The resource name for a full match.</span></span> <span data-ttu-id="037e7-154">例如，如果您的資源名稱是 testResource，您可以指定 testResource。</span><span class="sxs-lookup"><span data-stu-id="037e7-154">e.g. if your resource name is testResource, you can specify testResource.</span></span>

```yaml
Type: System.String
Parameter Sets: Lists the resources based on the specified scope., Lists the resources based on the specified scope at the tenant level., Get a resources using a multi-subscription query.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="037e7-155">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="037e7-155">-ResourceType</span></span>
<span data-ttu-id="037e7-156">指定資源的類型。</span><span class="sxs-lookup"><span data-stu-id="037e7-156">Specifies the type of a resource.</span></span>
<span data-ttu-id="037e7-157">舉例來說，對於資料庫而言，資源類型如下所示：</span><span class="sxs-lookup"><span data-stu-id="037e7-157">For instance, for a database, the resource type is as follows:</span></span>

`Microsoft.Sql/Servers/Databases`

<span data-ttu-id="037e7-158">這個 Cmdlet 會搜尋指定類型的資源。</span><span class="sxs-lookup"><span data-stu-id="037e7-158">This cmdlet searches for resources of the specified type.</span></span>

```yaml
Type: System.String
Parameter Sets: Lists the resources based on the specified scope.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Lists the resources based on the specified scope at the tenant level., Get a resources using a multi-subscription query.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="037e7-159">-Tag</span><span class="sxs-lookup"><span data-stu-id="037e7-159">-Tag</span></span>
<span data-ttu-id="037e7-160">OData 查詢的標記篩選器。</span><span class="sxs-lookup"><span data-stu-id="037e7-160">The tag filter for the OData query.</span></span> <span data-ttu-id="037e7-161">預期格式是 @ {tagName = $null} 或 @ {tagName = ' tagValue '}。</span><span class="sxs-lookup"><span data-stu-id="037e7-161">The expected format is @{tagName=$null} or @{tagName = 'tagValue'}.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Lists resources by a tag object specified as a hashset.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="037e7-162">-TagName</span><span class="sxs-lookup"><span data-stu-id="037e7-162">-TagName</span></span>
```yaml
Type: System.String
Parameter Sets: Lists resources by a tag specified as a individual name and value parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="037e7-163">-TagValue</span><span class="sxs-lookup"><span data-stu-id="037e7-163">-TagValue</span></span>
```yaml
Type: System.String
Parameter Sets: Lists resources by a tag specified as a individual name and value parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="037e7-164">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="037e7-164">-TenantLevel</span></span>
<span data-ttu-id="037e7-165">表示此 Cmdlet 在租使用者層級運作。</span><span class="sxs-lookup"><span data-stu-id="037e7-165">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Lists the resources based on the specified scope at the tenant level.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="037e7-166">-上方</span><span class="sxs-lookup"><span data-stu-id="037e7-166">-Top</span></span>
<span data-ttu-id="037e7-167">指定要檢索的資源數。</span><span class="sxs-lookup"><span data-stu-id="037e7-167">Specifies the number of resources to retrieve.</span></span>

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

### <span data-ttu-id="037e7-168">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="037e7-168">-DefaultProfile</span></span>
<span data-ttu-id="037e7-169">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="037e7-169">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="037e7-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="037e7-170">CommonParameters</span></span>
<span data-ttu-id="037e7-171">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="037e7-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="037e7-172">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="037e7-172">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="037e7-173">輸入</span><span class="sxs-lookup"><span data-stu-id="037e7-173">INPUTS</span></span>

## <span data-ttu-id="037e7-174">輸出</span><span class="sxs-lookup"><span data-stu-id="037e7-174">OUTPUTS</span></span>

### <span data-ttu-id="037e7-175">系統管理. PSObject</span><span class="sxs-lookup"><span data-stu-id="037e7-175">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="037e7-176">筆記</span><span class="sxs-lookup"><span data-stu-id="037e7-176">NOTES</span></span>

## <span data-ttu-id="037e7-177">相關連結</span><span class="sxs-lookup"><span data-stu-id="037e7-177">RELATED LINKS</span></span>

[<span data-ttu-id="037e7-178">AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="037e7-178">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="037e7-179">移動流覽 AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="037e7-179">Move-AzureRmResource</span></span>](./Move-AzureRmResource.md)

[<span data-ttu-id="037e7-180">新-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="037e7-180">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="037e7-181">移除-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="037e7-181">Remove-AzureRmResource</span></span>](./Remove-AzureRmResource.md)

[<span data-ttu-id="037e7-182">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="037e7-182">Set-AzureRmResource</span></span>](./Set-AzureRmResource.md)
