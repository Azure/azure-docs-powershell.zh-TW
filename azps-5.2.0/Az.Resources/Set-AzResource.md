---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: A00160B9-831F-4A20-8D9D-9E89BC4F5C91
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResource.md
ms.openlocfilehash: bf01232939881feb5a60420cde76e0e809cbcb3d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98280478"
---
# <span data-ttu-id="e80b6-101">Set-AzResource</span><span class="sxs-lookup"><span data-stu-id="e80b6-101">Set-AzResource</span></span>

## <span data-ttu-id="e80b6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e80b6-102">SYNOPSIS</span></span>
<span data-ttu-id="e80b6-103">修改資源。</span><span class="sxs-lookup"><span data-stu-id="e80b6-103">Modifies a resource.</span></span>

## <span data-ttu-id="e80b6-104">句法</span><span class="sxs-lookup"><span data-stu-id="e80b6-104">SYNTAX</span></span>

### <span data-ttu-id="e80b6-105">ByResourceId (預設) </span><span class="sxs-lookup"><span data-stu-id="e80b6-105">ByResourceId (Default)</span></span>
```
Set-AzResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] -ResourceId <String> [-ODataQuery <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e80b6-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="e80b6-106">ByInputObject</span></span>
```
Set-AzResource -InputObject <PSResource> [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] [-ODataQuery <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e80b6-107">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="e80b6-107">BySubscriptionLevel</span></span>
```
Set-AzResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>]
 [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e80b6-108">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="e80b6-108">ByTenantLevel</span></span>
```
Set-AzResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e80b6-109">說明</span><span class="sxs-lookup"><span data-stu-id="e80b6-109">DESCRIPTION</span></span>
<span data-ttu-id="e80b6-110">**AzResource** Cmdlet 會修改現有的 Azure 資源。</span><span class="sxs-lookup"><span data-stu-id="e80b6-110">The **Set-AzResource** cmdlet modifies an existing Azure resource.</span></span>
<span data-ttu-id="e80b6-111">指定要依名稱和類型或依識別碼來修改的資源。</span><span class="sxs-lookup"><span data-stu-id="e80b6-111">Specify a resource to modify by name and type or by ID.</span></span>

## <span data-ttu-id="e80b6-112">示例</span><span class="sxs-lookup"><span data-stu-id="e80b6-112">EXAMPLES</span></span>

### <span data-ttu-id="e80b6-113">範例1：修改資源</span><span class="sxs-lookup"><span data-stu-id="e80b6-113">Example 1: Modify a resource</span></span>
```
PS C:\> $Resource = Get-AzResource -ResourceType Microsoft.Web/sites -ResourceGroupName ResourceGroup11 -ResourceName ContosoSite
PS C:\> $Resource.Properties.Enabled = "False"
PS C:\> $Resource | Set-AzResource -Force
```

<span data-ttu-id="e80b6-114">第一個命令會使用 Get-AzResource Cmdlet 來取得名為 ContosoSite 的資源，然後將它儲存在 $Resource 變數中。</span><span class="sxs-lookup"><span data-stu-id="e80b6-114">The first command gets the resource named ContosoSite by using the Get-AzResource cmdlet, and then stores it in the $Resource variable.</span></span>
<span data-ttu-id="e80b6-115">第二個命令會修改 $Resource 的屬性。</span><span class="sxs-lookup"><span data-stu-id="e80b6-115">The second command modifies a property of $Resource.</span></span>
<span data-ttu-id="e80b6-116">最後一個命令會更新資源以符合 $Resource。</span><span class="sxs-lookup"><span data-stu-id="e80b6-116">The final command updates the resource to match $Resource.</span></span>

### <span data-ttu-id="e80b6-117">範例2：修改指定資源群組中的所有資源</span><span class="sxs-lookup"><span data-stu-id="e80b6-117">Example 2: Modify all resources in a given resource group</span></span>
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

<span data-ttu-id="e80b6-118">第一個命令會取得 testrg 資源群組中的資源，然後將它們儲存在 $Resource 變數中。</span><span class="sxs-lookup"><span data-stu-id="e80b6-118">The first command gets the resources in the testrg resource group, and then stores them in the $Resource variable.</span></span>

<span data-ttu-id="e80b6-119">第二個命令會迴圈顯示資源群組中的每一個資源，並將新標記新增到其中。</span><span class="sxs-lookup"><span data-stu-id="e80b6-119">The second command iterates over each of these resources in the resource group and adds a new tag to them.</span></span>

<span data-ttu-id="e80b6-120">最後一個命令會更新這些資源中的每一個。</span><span class="sxs-lookup"><span data-stu-id="e80b6-120">The final command updates each of these resources.</span></span>

## <span data-ttu-id="e80b6-121">參數</span><span class="sxs-lookup"><span data-stu-id="e80b6-121">PARAMETERS</span></span>

### <span data-ttu-id="e80b6-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="e80b6-122">-ApiVersion</span></span>
<span data-ttu-id="e80b6-123">指定要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="e80b6-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="e80b6-124">如果您沒有指定版本，此 Cmdlet 會使用最新的可用版本。</span><span class="sxs-lookup"><span data-stu-id="e80b6-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="e80b6-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e80b6-125">-AsJob</span></span>
<span data-ttu-id="e80b6-126">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e80b6-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e80b6-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e80b6-127">-DefaultProfile</span></span>
<span data-ttu-id="e80b6-128">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="e80b6-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e80b6-129">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="e80b6-129">-ExtensionResourceName</span></span>
<span data-ttu-id="e80b6-130">指定資源延伸資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="e80b6-130">Specifies the name of an extension resource for the resource.</span></span>
<span data-ttu-id="e80b6-131">例如，若要指定資料庫，請使用下列格式：伺服器名稱 `/` 資料庫名稱</span><span class="sxs-lookup"><span data-stu-id="e80b6-131">For instance, to specify a database, use the following format: server name`/`database name</span></span>

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

### <span data-ttu-id="e80b6-132">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="e80b6-132">-ExtensionResourceType</span></span>
<span data-ttu-id="e80b6-133">指定延伸資源的資源類型。</span><span class="sxs-lookup"><span data-stu-id="e80b6-133">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="e80b6-134">例如，如果延伸資源是資料庫，請指定下列各項： `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="e80b6-134">For instance, if the extension resource is a database specify the following: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="e80b6-135">-Force</span><span class="sxs-lookup"><span data-stu-id="e80b6-135">-Force</span></span>
<span data-ttu-id="e80b6-136">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="e80b6-136">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e80b6-137">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e80b6-137">-InputObject</span></span>
<span data-ttu-id="e80b6-138">要更新之資源的物件表示。</span><span class="sxs-lookup"><span data-stu-id="e80b6-138">The object representation of the resource to update.</span></span>

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

### <span data-ttu-id="e80b6-139">類型</span><span class="sxs-lookup"><span data-stu-id="e80b6-139">-Kind</span></span>
<span data-ttu-id="e80b6-140">指定資源的資源類型。</span><span class="sxs-lookup"><span data-stu-id="e80b6-140">Specifies the resource kind for the resource.</span></span>

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

### <span data-ttu-id="e80b6-141">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="e80b6-141">-ODataQuery</span></span>
<span data-ttu-id="e80b6-142">指定 (OData) 樣式篩選的開放式資料通訊協定。</span><span class="sxs-lookup"><span data-stu-id="e80b6-142">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="e80b6-143">除了任何其他篩選器之外，此 Cmdlet 還會將此值附加到要求中。</span><span class="sxs-lookup"><span data-stu-id="e80b6-143">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="e80b6-144">-方案</span><span class="sxs-lookup"><span data-stu-id="e80b6-144">-Plan</span></span>
<span data-ttu-id="e80b6-145">以雜湊資料表的形式指定資源的資源計劃屬性。</span><span class="sxs-lookup"><span data-stu-id="e80b6-145">Specifies resource plan properties, as a hash table, for the resource.</span></span>

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

### <span data-ttu-id="e80b6-146">-預先</span><span class="sxs-lookup"><span data-stu-id="e80b6-146">-Pre</span></span>
<span data-ttu-id="e80b6-147">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="e80b6-147">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="e80b6-148">-屬性</span><span class="sxs-lookup"><span data-stu-id="e80b6-148">-Properties</span></span>
<span data-ttu-id="e80b6-149">指定資源的資源屬性。</span><span class="sxs-lookup"><span data-stu-id="e80b6-149">Specifies resource properties for the resource.</span></span>

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

### <span data-ttu-id="e80b6-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e80b6-150">-ResourceGroupName</span></span>
<span data-ttu-id="e80b6-151">指定此 Cmdlet 修改資源之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e80b6-151">Specifies the name of the resource group where this cmdlet modifies the resource.</span></span>

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

### <span data-ttu-id="e80b6-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e80b6-152">-ResourceId</span></span>
<span data-ttu-id="e80b6-153">指定完全限定的資源識別碼，包括訂閱，如下列範例所示： `/subscriptions/` 訂閱識別碼`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="e80b6-153">Specifies the fully qualified resource ID, including the subscription, as in the following example: `/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="e80b6-154">-CoNtext.resourcename</span><span class="sxs-lookup"><span data-stu-id="e80b6-154">-ResourceName</span></span>
<span data-ttu-id="e80b6-155">指定資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="e80b6-155">Specifies the name of the resource.</span></span>
<span data-ttu-id="e80b6-156">例如，若要指定資料庫，請使用下列格式： `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="e80b6-156">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="e80b6-157">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="e80b6-157">-ResourceType</span></span>
<span data-ttu-id="e80b6-158">指定資源的類型。</span><span class="sxs-lookup"><span data-stu-id="e80b6-158">Specifies the type of the resource.</span></span>
<span data-ttu-id="e80b6-159">舉例來說，對於資料庫而言，資源類型如下所示： `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="e80b6-159">For instance, for a database, the resource type is as follows: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="e80b6-160">-Sku</span><span class="sxs-lookup"><span data-stu-id="e80b6-160">-Sku</span></span>
<span data-ttu-id="e80b6-161">將資源的 SKU 物件指定為雜湊表。</span><span class="sxs-lookup"><span data-stu-id="e80b6-161">Specifies the SKU object of the resource as a hash table.</span></span>

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

### <span data-ttu-id="e80b6-162">-Tag</span><span class="sxs-lookup"><span data-stu-id="e80b6-162">-Tag</span></span>
<span data-ttu-id="e80b6-163">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="e80b6-163">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="e80b6-164">例如： @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="e80b6-164">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="e80b6-165">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="e80b6-165">-TenantLevel</span></span>
<span data-ttu-id="e80b6-166">表示此 Cmdlet 在租使用者層級運作。</span><span class="sxs-lookup"><span data-stu-id="e80b6-166">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="e80b6-167">-UsePatchSemantics</span><span class="sxs-lookup"><span data-stu-id="e80b6-167">-UsePatchSemantics</span></span>
<span data-ttu-id="e80b6-168">表示此 Cmdlet 使用 HTTP 修補程式來更新物件，而不是 HTTP PUT。</span><span class="sxs-lookup"><span data-stu-id="e80b6-168">Indicates that this cmdlet uses an HTTP PATCH to update the object, instead of an HTTP PUT.</span></span>

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

### <span data-ttu-id="e80b6-169">-確認</span><span class="sxs-lookup"><span data-stu-id="e80b6-169">-Confirm</span></span>
<span data-ttu-id="e80b6-170">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e80b6-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e80b6-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e80b6-171">-WhatIf</span></span>
<span data-ttu-id="e80b6-172">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e80b6-172">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e80b6-173">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e80b6-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e80b6-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e80b6-174">CommonParameters</span></span>
<span data-ttu-id="e80b6-175">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e80b6-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e80b6-176">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e80b6-176">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e80b6-177">輸入</span><span class="sxs-lookup"><span data-stu-id="e80b6-177">INPUTS</span></span>

### <span data-ttu-id="e80b6-178">PSResource 中的 SdkModels （）</span><span class="sxs-lookup"><span data-stu-id="e80b6-178">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResource</span></span>

### <span data-ttu-id="e80b6-179">System.object</span><span class="sxs-lookup"><span data-stu-id="e80b6-179">System.String</span></span>

### <span data-ttu-id="e80b6-180">系統管理. PSObject</span><span class="sxs-lookup"><span data-stu-id="e80b6-180">System.Management.Automation.PSObject</span></span>

### <span data-ttu-id="e80b6-181">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="e80b6-181">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e80b6-182">輸出</span><span class="sxs-lookup"><span data-stu-id="e80b6-182">OUTPUTS</span></span>

### <span data-ttu-id="e80b6-183">系統管理. PSObject</span><span class="sxs-lookup"><span data-stu-id="e80b6-183">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="e80b6-184">筆記</span><span class="sxs-lookup"><span data-stu-id="e80b6-184">NOTES</span></span>

## <span data-ttu-id="e80b6-185">相關連結</span><span class="sxs-lookup"><span data-stu-id="e80b6-185">RELATED LINKS</span></span>

[<span data-ttu-id="e80b6-186">AzResource</span><span class="sxs-lookup"><span data-stu-id="e80b6-186">Get-AzResource</span></span>](./Get-AzResource.md)

[<span data-ttu-id="e80b6-187">移動流覽 AzResource</span><span class="sxs-lookup"><span data-stu-id="e80b6-187">Move-AzResource</span></span>](./Move-AzResource.md)

[<span data-ttu-id="e80b6-188">新-AzResource</span><span class="sxs-lookup"><span data-stu-id="e80b6-188">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="e80b6-189">移除-AzResource</span><span class="sxs-lookup"><span data-stu-id="e80b6-189">Remove-AzResource</span></span>](./Remove-AzResource.md)
