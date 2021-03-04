---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D6FF6BDD-4515-438D-B39D-C0BFC3342F4E
online version: https://docs.microsoft.com/powershell/module/az.resources/new-azresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResource.md
ms.openlocfilehash: 457f5db18ba43d1fd598e255d9ca1fb2e62f3f3f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910669"
---
# <span data-ttu-id="fed81-101">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="fed81-101">New-AzResource</span></span>

## <span data-ttu-id="fed81-102">簡介</span><span class="sxs-lookup"><span data-stu-id="fed81-102">SYNOPSIS</span></span>
<span data-ttu-id="fed81-103">建立資源。</span><span class="sxs-lookup"><span data-stu-id="fed81-103">Creates a resource.</span></span>

## <span data-ttu-id="fed81-104">語法</span><span class="sxs-lookup"><span data-stu-id="fed81-104">SYNTAX</span></span>

### <span data-ttu-id="fed81-105">ByResourceId (預設) </span><span class="sxs-lookup"><span data-stu-id="fed81-105">ByResourceId (Default)</span></span>
```
New-AzResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceId <String> [-ODataQuery <String>]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fed81-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="fed81-106">BySubscriptionLevel</span></span>
```
New-AzResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>]
 [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fed81-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="fed81-107">ByTenantLevel</span></span>
```
New-AzResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fed81-108">描述</span><span class="sxs-lookup"><span data-stu-id="fed81-108">DESCRIPTION</span></span>
<span data-ttu-id="fed81-109">**New-AzResource** Cmdlet 會建立資源群組中的 Azure 資源，例如網站、Azure SQL 資料庫伺服器或 Azure SQL Database。</span><span class="sxs-lookup"><span data-stu-id="fed81-109">The **New-AzResource** cmdlet creates an Azure resource, such as a website, Azure SQL Database server, or Azure SQL Database, in a resource group.</span></span>

## <span data-ttu-id="fed81-110">例子</span><span class="sxs-lookup"><span data-stu-id="fed81-110">EXAMPLES</span></span>

### <span data-ttu-id="fed81-111">範例 1：建立資源</span><span class="sxs-lookup"><span data-stu-id="fed81-111">Example 1: Create a resource</span></span>
```
PS> New-AzResource -Location "West US" -Properties @{test="test"} -ResourceName TestSite06 -ResourceType microsoft.web/sites -ResourceGroupName ResourceGroup11 -Force
```

<span data-ttu-id="fed81-112">此命令會建立資源，該資源是 ResourceGroup11 中的網站。</span><span class="sxs-lookup"><span data-stu-id="fed81-112">This command creates a resource that is a website in ResourceGroup11.</span></span>

### <span data-ttu-id="fed81-113">範例 2：使用 Splatting 建立資源</span><span class="sxs-lookup"><span data-stu-id="fed81-113">Example 2: Create a resource using splatting</span></span>
```
PS> $prop = @{
    Location          = "West US"
    Properties        = @{test = "test"}
    ResourceName      = "TestSite06"
    ResourceType      = "microsoft.web/sites"
    ResourceGroupName = "ResourceGroup11"
    Force             = $true
}

PS> New-AzResource @prop
```

<span data-ttu-id="fed81-114">此命令會建立資源，該資源是 ResourceGroup11 中的網站。</span><span class="sxs-lookup"><span data-stu-id="fed81-114">This command creates a resource that is a website in ResourceGroup11.</span></span>

## <span data-ttu-id="fed81-115">參數</span><span class="sxs-lookup"><span data-stu-id="fed81-115">PARAMETERS</span></span>

### <span data-ttu-id="fed81-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="fed81-116">-ApiVersion</span></span>
<span data-ttu-id="fed81-117">指定要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="fed81-117">Specifies the version of the resource provider API to use.</span></span> <span data-ttu-id="fed81-118">如果您未指定版本，此 Cmdlet 會使用最新的可用版本。</span><span class="sxs-lookup"><span data-stu-id="fed81-118">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="fed81-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fed81-119">-AsJob</span></span>
<span data-ttu-id="fed81-120">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="fed81-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fed81-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fed81-121">-DefaultProfile</span></span>
<span data-ttu-id="fed81-122">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="fed81-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fed81-123">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="fed81-123">-ExtensionResourceName</span></span>
<span data-ttu-id="fed81-124">指定資源的擴充資源名稱。</span><span class="sxs-lookup"><span data-stu-id="fed81-124">Specifies the name of an extension resource for the resource.</span></span> <span data-ttu-id="fed81-125">例如，若要指定資料庫，請使用下列格式：伺服器名稱 `/` 資料庫名稱</span><span class="sxs-lookup"><span data-stu-id="fed81-125">For instance, to specify a database, use the following format: server name`/`database name</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fed81-126">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="fed81-126">-ExtensionResourceType</span></span>
<span data-ttu-id="fed81-127">指定擴充資源的資源類型。</span><span class="sxs-lookup"><span data-stu-id="fed81-127">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="fed81-128">例如，如果擴充資源是資料庫，請指定下列類型： `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="fed81-128">For instance, if the extension resource is a database, specify the following type: `Microsoft.Sql/Servers/Databases`</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fed81-129">-強制</span><span class="sxs-lookup"><span data-stu-id="fed81-129">-Force</span></span>
<span data-ttu-id="fed81-130">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="fed81-130">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="fed81-131">-IsFullObject</span><span class="sxs-lookup"><span data-stu-id="fed81-131">-IsFullObject</span></span>
<span data-ttu-id="fed81-132">表示 Properties 參數指定的物件是完整物件。</span><span class="sxs-lookup"><span data-stu-id="fed81-132">Indicates that the object that the *Properties* parameter specifies is the full object.</span></span>

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

### <span data-ttu-id="fed81-133">-Kind</span><span class="sxs-lookup"><span data-stu-id="fed81-133">-Kind</span></span>
<span data-ttu-id="fed81-134">指定資源的資源類型。</span><span class="sxs-lookup"><span data-stu-id="fed81-134">Specifies the resource kind for the resource.</span></span>

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

### <span data-ttu-id="fed81-135">-位置</span><span class="sxs-lookup"><span data-stu-id="fed81-135">-Location</span></span>
<span data-ttu-id="fed81-136">指定資源的位置。</span><span class="sxs-lookup"><span data-stu-id="fed81-136">Specifies the location of the resource.</span></span>
<span data-ttu-id="fed81-137">指定資料中心位置，例如美國中部或東南亞。</span><span class="sxs-lookup"><span data-stu-id="fed81-137">Specify data center location, such as Central US or Southeast Asia.</span></span>
<span data-ttu-id="fed81-138">您可以將資源放在任何支援該類型資源的位置。</span><span class="sxs-lookup"><span data-stu-id="fed81-138">You can place a resource in any location that supports resources of that type.</span></span> <span data-ttu-id="fed81-139">資源群組可以包含不同位置的資源。</span><span class="sxs-lookup"><span data-stu-id="fed81-139">Resource groups can contain resources from different locations.</span></span> <span data-ttu-id="fed81-140">若要判斷哪些位置支援每種資源類型，請使用 Get-AzLocation Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fed81-140">To determine which locations support each resource type, use the Get-AzLocation cmdlet.</span></span>

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

### <span data-ttu-id="fed81-141">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="fed81-141">-ODataQuery</span></span>
<span data-ttu-id="fed81-142">指定開啟資料通訊協定 (OData) 樣式篩選。</span><span class="sxs-lookup"><span data-stu-id="fed81-142">Specifies an Open Data Protocol (OData) style filter.</span></span> <span data-ttu-id="fed81-143">除了任何其他篩選之外，此 Cmdlet 會附加此值至要求。</span><span class="sxs-lookup"><span data-stu-id="fed81-143">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="fed81-144">-規劃</span><span class="sxs-lookup"><span data-stu-id="fed81-144">-Plan</span></span>
<span data-ttu-id="fed81-145">代表資源計劃屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="fed81-145">A hash table that represents resource plan properties.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: PlanObject

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fed81-146">-Pre</span><span class="sxs-lookup"><span data-stu-id="fed81-146">-Pre</span></span>
<span data-ttu-id="fed81-147">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮測試版 API 版本。</span><span class="sxs-lookup"><span data-stu-id="fed81-147">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="fed81-148">-Properties</span><span class="sxs-lookup"><span data-stu-id="fed81-148">-Properties</span></span>
<span data-ttu-id="fed81-149">指定資源的資源屬性。</span><span class="sxs-lookup"><span data-stu-id="fed81-149">Specifies resource properties for the resource.</span></span> <span data-ttu-id="fed81-150">使用此參數指定資源類型特有的屬性值。</span><span class="sxs-lookup"><span data-stu-id="fed81-150">Use this parameter to specify the values of properties that are specific to a resource type.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: PropertyObject

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fed81-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fed81-151">-ResourceGroupName</span></span>
<span data-ttu-id="fed81-152">指定此 Cmdlet 建立資源的資源組名。</span><span class="sxs-lookup"><span data-stu-id="fed81-152">Specifies the name of the resource group where this cmdlet creates the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fed81-153">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fed81-153">-ResourceId</span></span>
<span data-ttu-id="fed81-154">指定完整資源識別碼，包括訂閱，如下列範例所示： `/subscriptions/` 訂閱識別碼`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="fed81-154">Specifies the fully qualified resource ID, including the subscription, as in the following example: `/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fed81-155">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="fed81-155">-ResourceName</span></span>
<span data-ttu-id="fed81-156">指定資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="fed81-156">Specifies the name of the resource.</span></span> <span data-ttu-id="fed81-157">例如，若要指定資料庫，請使用下列格式： `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="fed81-157">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fed81-158">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="fed81-158">-ResourceType</span></span>
<span data-ttu-id="fed81-159">指定資源的類型。</span><span class="sxs-lookup"><span data-stu-id="fed81-159">Specifies the type of the resource.</span></span>
<span data-ttu-id="fed81-160">例如，對於資料庫，資源類型如下： `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="fed81-160">For instance, for a database, the resource type is as follows: `Microsoft.Sql/Servers/Databases`</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fed81-161">-SKU</span><span class="sxs-lookup"><span data-stu-id="fed81-161">-Sku</span></span>
<span data-ttu-id="fed81-162">代表 SKU 屬性的雜湊表格。</span><span class="sxs-lookup"><span data-stu-id="fed81-162">A hash table that represents sku properties.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: SkuObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fed81-163">-標記</span><span class="sxs-lookup"><span data-stu-id="fed81-163">-Tag</span></span>
<span data-ttu-id="fed81-164">以雜湊表格形式建立索引鍵值組。</span><span class="sxs-lookup"><span data-stu-id="fed81-164">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="fed81-165">例如：@{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="fed81-165">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fed81-166">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="fed81-166">-TenantLevel</span></span>
<span data-ttu-id="fed81-167">表示此 Cmdlet 在租使用者層級運作。</span><span class="sxs-lookup"><span data-stu-id="fed81-167">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fed81-168">-確認</span><span class="sxs-lookup"><span data-stu-id="fed81-168">-Confirm</span></span>
<span data-ttu-id="fed81-169">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="fed81-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fed81-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fed81-170">-WhatIf</span></span>
<span data-ttu-id="fed81-171">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="fed81-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fed81-172">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fed81-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fed81-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fed81-173">CommonParameters</span></span>
<span data-ttu-id="fed81-174">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="fed81-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fed81-175">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fed81-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fed81-176">輸入</span><span class="sxs-lookup"><span data-stu-id="fed81-176">INPUTS</span></span>

### <span data-ttu-id="fed81-177">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="fed81-177">System.Collections.Hashtable</span></span>

### <span data-ttu-id="fed81-178">System.String</span><span class="sxs-lookup"><span data-stu-id="fed81-178">System.String</span></span>

## <span data-ttu-id="fed81-179">輸出</span><span class="sxs-lookup"><span data-stu-id="fed81-179">OUTPUTS</span></span>

### <span data-ttu-id="fed81-180">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="fed81-180">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="fed81-181">筆記</span><span class="sxs-lookup"><span data-stu-id="fed81-181">NOTES</span></span>

## <span data-ttu-id="fed81-182">相關連結</span><span class="sxs-lookup"><span data-stu-id="fed81-182">RELATED LINKS</span></span>

[<span data-ttu-id="fed81-183">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="fed81-183">Get-AzResource</span></span>](./Get-AzResource.md)

[<span data-ttu-id="fed81-184">Move-AzResource</span><span class="sxs-lookup"><span data-stu-id="fed81-184">Move-AzResource</span></span>](./Move-AzResource.md)

[<span data-ttu-id="fed81-185">Remove-AzResource</span><span class="sxs-lookup"><span data-stu-id="fed81-185">Remove-AzResource</span></span>](./Remove-AzResource.md)

[<span data-ttu-id="fed81-186">Set-AzResource</span><span class="sxs-lookup"><span data-stu-id="fed81-186">Set-AzResource</span></span>](./Set-AzResource.md)
