---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: A00160B9-831F-4A20-8D9D-9E89BC4F5C91
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResource.md
ms.openlocfilehash: 82e06a4736a613111efac452eb1fced2713dc470
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100415745"
---
# <span data-ttu-id="459d4-101">Set-AzResource</span><span class="sxs-lookup"><span data-stu-id="459d4-101">Set-AzResource</span></span>

## <span data-ttu-id="459d4-102">簡介</span><span class="sxs-lookup"><span data-stu-id="459d4-102">SYNOPSIS</span></span>
<span data-ttu-id="459d4-103">修改資源。</span><span class="sxs-lookup"><span data-stu-id="459d4-103">Modifies a resource.</span></span>

## <span data-ttu-id="459d4-104">語法</span><span class="sxs-lookup"><span data-stu-id="459d4-104">SYNTAX</span></span>

### <span data-ttu-id="459d4-105">ByResourceId (預設) </span><span class="sxs-lookup"><span data-stu-id="459d4-105">ByResourceId (Default)</span></span>
```
Set-AzResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] -ResourceId <String> [-ODataQuery <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="459d4-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="459d4-106">ByInputObject</span></span>
```
Set-AzResource -InputObject <PSResource> [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] [-ODataQuery <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="459d4-107">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="459d4-107">BySubscriptionLevel</span></span>
```
Set-AzResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>]
 [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="459d4-108">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="459d4-108">ByTenantLevel</span></span>
```
Set-AzResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="459d4-109">描述</span><span class="sxs-lookup"><span data-stu-id="459d4-109">DESCRIPTION</span></span>
<span data-ttu-id="459d4-110">**Set-AzResource** Cmdlet 會修改現有的 Azure 資源。</span><span class="sxs-lookup"><span data-stu-id="459d4-110">The **Set-AzResource** cmdlet modifies an existing Azure resource.</span></span>
<span data-ttu-id="459d4-111">指定要根據名稱和類型或識別碼修改的資源。</span><span class="sxs-lookup"><span data-stu-id="459d4-111">Specify a resource to modify by name and type or by ID.</span></span>

## <span data-ttu-id="459d4-112">例子</span><span class="sxs-lookup"><span data-stu-id="459d4-112">EXAMPLES</span></span>

### <span data-ttu-id="459d4-113">範例 1：修改資源</span><span class="sxs-lookup"><span data-stu-id="459d4-113">Example 1: Modify a resource</span></span>
```
PS C:\> $Resource = Get-AzResource -ResourceType Microsoft.Web/sites -ResourceGroupName ResourceGroup11 -ResourceName ContosoSite
PS C:\> $Resource.Properties.Enabled = "False"
PS C:\> $Resource | Set-AzResource -Force
```

<span data-ttu-id="459d4-114">第一個命令會使用 Get-AzResource Cmdlet 來獲得名為 ContosoSite 的資源，然後將它儲存在$Resource變數中。</span><span class="sxs-lookup"><span data-stu-id="459d4-114">The first command gets the resource named ContosoSite by using the Get-AzResource cmdlet, and then stores it in the $Resource variable.</span></span>
<span data-ttu-id="459d4-115">第二個命令會修改 $Resource。</span><span class="sxs-lookup"><span data-stu-id="459d4-115">The second command modifies a property of $Resource.</span></span>
<span data-ttu-id="459d4-116">最後一個命令會更新資源以與$Resource。</span><span class="sxs-lookup"><span data-stu-id="459d4-116">The final command updates the resource to match $Resource.</span></span>

### <span data-ttu-id="459d4-117">範例 2：修改給定資源群組中所有資源</span><span class="sxs-lookup"><span data-stu-id="459d4-117">Example 2: Modify all resources in a given resource group</span></span>
```
PS C:\> $Resource = Get-AzResource -ResourceGroupName testrg
PS C:\> $Resource | ForEach-Object { $_.Tags.Add("testkey", "testval") }
PS C:\> $Resource | Set-AzResource -Force

Name              : kv-test
ResourceId        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.KeyVault/vaults/kv-test
ResourceName      : kv-test
ResourceType      : Microsoft.KeyVault/vaults
ResourceGroupName : testrg
Location          : westus
SubscriptionId    : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Tags              : {testrgkey, key}
Properties        : @{}

Name              : testresource
ResourceId        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Providers.Test/statefulResources/testresource
ResourceName      : testresource
ResourceType      : Providers.Test/statefulResources
ResourceGroupName : testrg
Location          : West US 2
SubscriptionId    : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Tags              : {testrgkey, anothertesttag}
Properties        : @{key=value}
Sku               : @{name=A0}
```

<span data-ttu-id="459d4-118">第一個命令會獲得 testrg 資源群組中的資源，然後將資源儲存在$Resource變數中。</span><span class="sxs-lookup"><span data-stu-id="459d4-118">The first command gets the resources in the testrg resource group, and then stores them in the $Resource variable.</span></span>

<span data-ttu-id="459d4-119">第二個命令會在每個資源群組中執行，並新增標記給他們。</span><span class="sxs-lookup"><span data-stu-id="459d4-119">The second command iterates over each of these resources in the resource group and adds a new tag to them.</span></span>

<span data-ttu-id="459d4-120">最後一個命令會更新這些資源。</span><span class="sxs-lookup"><span data-stu-id="459d4-120">The final command updates each of these resources.</span></span>

## <span data-ttu-id="459d4-121">參數</span><span class="sxs-lookup"><span data-stu-id="459d4-121">PARAMETERS</span></span>

### <span data-ttu-id="459d4-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="459d4-122">-ApiVersion</span></span>
<span data-ttu-id="459d4-123">指定要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="459d4-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="459d4-124">如果您未指定版本，此 Cmdlet 會使用最新的可用版本。</span><span class="sxs-lookup"><span data-stu-id="459d4-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="459d4-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="459d4-125">-AsJob</span></span>
<span data-ttu-id="459d4-126">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="459d4-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="459d4-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="459d4-127">-DefaultProfile</span></span>
<span data-ttu-id="459d4-128">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="459d4-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="459d4-129">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="459d4-129">-ExtensionResourceName</span></span>
<span data-ttu-id="459d4-130">指定資源的擴充資源名稱。</span><span class="sxs-lookup"><span data-stu-id="459d4-130">Specifies the name of an extension resource for the resource.</span></span>
<span data-ttu-id="459d4-131">例如，若要指定資料庫，請使用下列格式：伺服器名稱 `/` 資料庫名稱</span><span class="sxs-lookup"><span data-stu-id="459d4-131">For instance, to specify a database, use the following format: server name`/`database name</span></span>

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

### <span data-ttu-id="459d4-132">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="459d4-132">-ExtensionResourceType</span></span>
<span data-ttu-id="459d4-133">指定擴充資源的資源類型。</span><span class="sxs-lookup"><span data-stu-id="459d4-133">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="459d4-134">例如，如果擴充資源是資料庫，請指定下列專案： `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="459d4-134">For instance, if the extension resource is a database specify the following: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="459d4-135">-強制</span><span class="sxs-lookup"><span data-stu-id="459d4-135">-Force</span></span>
<span data-ttu-id="459d4-136">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="459d4-136">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="459d4-137">-InputObject</span><span class="sxs-lookup"><span data-stu-id="459d4-137">-InputObject</span></span>
<span data-ttu-id="459d4-138">要更新之資源的物件標記法。</span><span class="sxs-lookup"><span data-stu-id="459d4-138">The object representation of the resource to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResource
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="459d4-139">-Kind</span><span class="sxs-lookup"><span data-stu-id="459d4-139">-Kind</span></span>
<span data-ttu-id="459d4-140">指定資源的資源類型。</span><span class="sxs-lookup"><span data-stu-id="459d4-140">Specifies the resource kind for the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="459d4-141">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="459d4-141">-ODataQuery</span></span>
<span data-ttu-id="459d4-142">指定開啟資料通訊協定 (OData) 樣式篩選。</span><span class="sxs-lookup"><span data-stu-id="459d4-142">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="459d4-143">除了任何其他篩選之外，此 Cmdlet 會附加此值至要求。</span><span class="sxs-lookup"><span data-stu-id="459d4-143">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="459d4-144">-規劃</span><span class="sxs-lookup"><span data-stu-id="459d4-144">-Plan</span></span>
<span data-ttu-id="459d4-145">指定資源的資源計劃屬性 #A0 為雜湊資料表 #A1。</span><span class="sxs-lookup"><span data-stu-id="459d4-145">Specifies resource plan properties, as a hash table, for the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: PlanObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="459d4-146">-Pre</span><span class="sxs-lookup"><span data-stu-id="459d4-146">-Pre</span></span>
<span data-ttu-id="459d4-147">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮測試版 API 版本。</span><span class="sxs-lookup"><span data-stu-id="459d4-147">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="459d4-148">-Properties</span><span class="sxs-lookup"><span data-stu-id="459d4-148">-Properties</span></span>
<span data-ttu-id="459d4-149">指定資源的資源屬性。</span><span class="sxs-lookup"><span data-stu-id="459d4-149">Specifies resource properties for the resource.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: PropertyObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="459d4-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="459d4-150">-ResourceGroupName</span></span>
<span data-ttu-id="459d4-151">指定此 Cmdlet 修改資源的資源組名。</span><span class="sxs-lookup"><span data-stu-id="459d4-151">Specifies the name of the resource group where this cmdlet modifies the resource.</span></span>

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

### <span data-ttu-id="459d4-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="459d4-152">-ResourceId</span></span>
<span data-ttu-id="459d4-153">指定完整資源識別碼，包括訂閱，如下列範例所示： `/subscriptions/` 訂閱識別碼`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="459d4-153">Specifies the fully qualified resource ID, including the subscription, as in the following example: `/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="459d4-154">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="459d4-154">-ResourceName</span></span>
<span data-ttu-id="459d4-155">指定資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="459d4-155">Specifies the name of the resource.</span></span>
<span data-ttu-id="459d4-156">例如，若要指定資料庫，請使用下列格式： `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="459d4-156">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="459d4-157">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="459d4-157">-ResourceType</span></span>
<span data-ttu-id="459d4-158">指定資源的類型。</span><span class="sxs-lookup"><span data-stu-id="459d4-158">Specifies the type of the resource.</span></span>
<span data-ttu-id="459d4-159">例如，對於資料庫，資源類型如下： `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="459d4-159">For instance, for a database, the resource type is as follows: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="459d4-160">-SKU</span><span class="sxs-lookup"><span data-stu-id="459d4-160">-Sku</span></span>
<span data-ttu-id="459d4-161">指定資源的 SKU 物件做為雜湊表格。</span><span class="sxs-lookup"><span data-stu-id="459d4-161">Specifies the SKU object of the resource as a hash table.</span></span>

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

### <span data-ttu-id="459d4-162">-標記</span><span class="sxs-lookup"><span data-stu-id="459d4-162">-Tag</span></span>
<span data-ttu-id="459d4-163">以雜湊表格形式建立索引鍵值組。</span><span class="sxs-lookup"><span data-stu-id="459d4-163">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="459d4-164">例如：@{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="459d4-164">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="459d4-165">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="459d4-165">-TenantLevel</span></span>
<span data-ttu-id="459d4-166">表示此 Cmdlet 在租使用者層級運作。</span><span class="sxs-lookup"><span data-stu-id="459d4-166">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="459d4-167">-UsePatchSemantics</span><span class="sxs-lookup"><span data-stu-id="459d4-167">-UsePatchSemantics</span></span>
<span data-ttu-id="459d4-168">表示此 Cmdlet 使用 HTTP 修補程式來更新物件，而不是 HTTP PUT。</span><span class="sxs-lookup"><span data-stu-id="459d4-168">Indicates that this cmdlet uses an HTTP PATCH to update the object, instead of an HTTP PUT.</span></span>

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

### <span data-ttu-id="459d4-169">-確認</span><span class="sxs-lookup"><span data-stu-id="459d4-169">-Confirm</span></span>
<span data-ttu-id="459d4-170">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="459d4-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="459d4-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="459d4-171">-WhatIf</span></span>
<span data-ttu-id="459d4-172">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="459d4-172">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="459d4-173">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="459d4-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="459d4-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="459d4-174">CommonParameters</span></span>
<span data-ttu-id="459d4-175">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="459d4-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="459d4-176">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="459d4-176">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="459d4-177">輸入</span><span class="sxs-lookup"><span data-stu-id="459d4-177">INPUTS</span></span>

### <span data-ttu-id="459d4-178">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResource</span><span class="sxs-lookup"><span data-stu-id="459d4-178">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResource</span></span>

### <span data-ttu-id="459d4-179">System.String</span><span class="sxs-lookup"><span data-stu-id="459d4-179">System.String</span></span>

### <span data-ttu-id="459d4-180">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="459d4-180">System.Management.Automation.PSObject</span></span>

### <span data-ttu-id="459d4-181">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="459d4-181">System.Collections.Hashtable</span></span>

## <span data-ttu-id="459d4-182">輸出</span><span class="sxs-lookup"><span data-stu-id="459d4-182">OUTPUTS</span></span>

### <span data-ttu-id="459d4-183">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="459d4-183">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="459d4-184">筆記</span><span class="sxs-lookup"><span data-stu-id="459d4-184">NOTES</span></span>

## <span data-ttu-id="459d4-185">相關連結</span><span class="sxs-lookup"><span data-stu-id="459d4-185">RELATED LINKS</span></span>


[<span data-ttu-id="459d4-186">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="459d4-186">Get-AzResource</span></span>](./Get-AzResource.md)

[<span data-ttu-id="459d4-187">Move-AzResource</span><span class="sxs-lookup"><span data-stu-id="459d4-187">Move-AzResource</span></span>](./Move-AzResource.md)

[<span data-ttu-id="459d4-188">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="459d4-188">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="459d4-189">Remove-AzResource</span><span class="sxs-lookup"><span data-stu-id="459d4-189">Remove-AzResource</span></span>](./Remove-AzResource.md)
