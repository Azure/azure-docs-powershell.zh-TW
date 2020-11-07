---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D6FF6BDD-4515-438D-B39D-C0BFC3342F4E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-Azresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzResource.md
ms.openlocfilehash: 7ae512f7992392bf12b17775a505313621ec3096
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/08/2020
ms.locfileid: "93968823"
---
# <span data-ttu-id="76b07-101">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="76b07-101">New-AzResource</span></span>

## <span data-ttu-id="76b07-102">摘要</span><span class="sxs-lookup"><span data-stu-id="76b07-102">SYNOPSIS</span></span>
<span data-ttu-id="76b07-103">建立資源。</span><span class="sxs-lookup"><span data-stu-id="76b07-103">Creates a resource.</span></span>

## <span data-ttu-id="76b07-104">句法</span><span class="sxs-lookup"><span data-stu-id="76b07-104">SYNTAX</span></span>

### <span data-ttu-id="76b07-105">ByResourceId (預設) </span><span class="sxs-lookup"><span data-stu-id="76b07-105">ByResourceId (Default)</span></span>
```
New-AzResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceId <String> [-ODataQuery <String>]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="76b07-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="76b07-106">BySubscriptionLevel</span></span>
```
New-AzResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>]
 [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76b07-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="76b07-107">ByTenantLevel</span></span>
```
New-AzResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="76b07-108">說明</span><span class="sxs-lookup"><span data-stu-id="76b07-108">DESCRIPTION</span></span>
<span data-ttu-id="76b07-109">**新的 AzResource** Cmdlet 會在資源群組中建立 azure 資源，例如網站、Azure SQL database Server 或 Azure SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="76b07-109">The **New-AzResource** cmdlet creates an Azure resource, such as a website, Azure SQL Database server, or Azure SQL Database, in a resource group.</span></span>

## <span data-ttu-id="76b07-110">示例</span><span class="sxs-lookup"><span data-stu-id="76b07-110">EXAMPLES</span></span>

### <span data-ttu-id="76b07-111">範例1：建立資源</span><span class="sxs-lookup"><span data-stu-id="76b07-111">Example 1: Create a resource</span></span>
```
PS> New-AzResource -Location "West US" -Properties @{test="test"} -ResourceName TestSite06 -ResourceType microsoft.web/sites -ResourceGroupName ResourceGroup11 -Force
```

<span data-ttu-id="76b07-112">這個命令會建立 ResourceGroup11 中的網站資源。</span><span class="sxs-lookup"><span data-stu-id="76b07-112">This command creates a resource that is a website in ResourceGroup11.</span></span>

### <span data-ttu-id="76b07-113">範例2：使用 splatting 建立資源</span><span class="sxs-lookup"><span data-stu-id="76b07-113">Example 2: Create a resource using splatting</span></span>
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

<span data-ttu-id="76b07-114">這個命令會建立 ResourceGroup11 中的網站資源。</span><span class="sxs-lookup"><span data-stu-id="76b07-114">This command creates a resource that is a website in ResourceGroup11.</span></span>

## <span data-ttu-id="76b07-115">參數</span><span class="sxs-lookup"><span data-stu-id="76b07-115">PARAMETERS</span></span>

### <span data-ttu-id="76b07-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="76b07-116">-ApiVersion</span></span>
<span data-ttu-id="76b07-117">指定要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="76b07-117">Specifies the version of the resource provider API to use.</span></span> <span data-ttu-id="76b07-118">如果您沒有指定版本，此 Cmdlet 會使用最新的可用版本。</span><span class="sxs-lookup"><span data-stu-id="76b07-118">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="76b07-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="76b07-119">-AsJob</span></span>
<span data-ttu-id="76b07-120">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="76b07-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="76b07-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76b07-121">-DefaultProfile</span></span>
<span data-ttu-id="76b07-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="76b07-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76b07-123">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="76b07-123">-ExtensionResourceName</span></span>
<span data-ttu-id="76b07-124">指定資源延伸資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="76b07-124">Specifies the name of an extension resource for the resource.</span></span> <span data-ttu-id="76b07-125">例如，若要指定資料庫，請使用下列格式：伺服器名稱 `/` 資料庫名稱</span><span class="sxs-lookup"><span data-stu-id="76b07-125">For instance, to specify a database, use the following format: server name`/`database name</span></span>

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

### <span data-ttu-id="76b07-126">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="76b07-126">-ExtensionResourceType</span></span>
<span data-ttu-id="76b07-127">指定延伸資源的資源類型。</span><span class="sxs-lookup"><span data-stu-id="76b07-127">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="76b07-128">例如，如果延伸資源是資料庫，請指定下列類型： `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="76b07-128">For instance, if the extension resource is a database, specify the following type: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="76b07-129">-Force</span><span class="sxs-lookup"><span data-stu-id="76b07-129">-Force</span></span>
<span data-ttu-id="76b07-130">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="76b07-130">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="76b07-131">-IsFullObject</span><span class="sxs-lookup"><span data-stu-id="76b07-131">-IsFullObject</span></span>
<span data-ttu-id="76b07-132">指示 *屬性* 參數指定的物件是完整物件。</span><span class="sxs-lookup"><span data-stu-id="76b07-132">Indicates that the object that the *Properties* parameter specifies is the full object.</span></span>

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

### <span data-ttu-id="76b07-133">類型</span><span class="sxs-lookup"><span data-stu-id="76b07-133">-Kind</span></span>
<span data-ttu-id="76b07-134">指定資源的資源類型。</span><span class="sxs-lookup"><span data-stu-id="76b07-134">Specifies the resource kind for the resource.</span></span>

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

### <span data-ttu-id="76b07-135">-位置</span><span class="sxs-lookup"><span data-stu-id="76b07-135">-Location</span></span>
<span data-ttu-id="76b07-136">指定資源的位置。</span><span class="sxs-lookup"><span data-stu-id="76b07-136">Specifies the location of the resource.</span></span>
<span data-ttu-id="76b07-137">指定資料中心位置，例如 [中北部] 或 [東南部的東南亞]。</span><span class="sxs-lookup"><span data-stu-id="76b07-137">Specify data center location, such as Central US or Southeast Asia.</span></span>
<span data-ttu-id="76b07-138">您可以將資源放在支援該類型之資源的任何位置。</span><span class="sxs-lookup"><span data-stu-id="76b07-138">You can place a resource in any location that supports resources of that type.</span></span> <span data-ttu-id="76b07-139">資源群組可以包含來自不同位置的資源。</span><span class="sxs-lookup"><span data-stu-id="76b07-139">Resource groups can contain resources from different locations.</span></span> <span data-ttu-id="76b07-140">若要判斷哪些位置支援每個資源類型，請使用 Get-AzureLocation Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="76b07-140">To determine which locations support each resource type, use the Get-AzureLocation cmdlet.</span></span>

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

### <span data-ttu-id="76b07-141">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="76b07-141">-ODataQuery</span></span>
<span data-ttu-id="76b07-142">指定 (OData) 樣式篩選的開放式資料通訊協定。</span><span class="sxs-lookup"><span data-stu-id="76b07-142">Specifies an Open Data Protocol (OData) style filter.</span></span> <span data-ttu-id="76b07-143">除了任何其他篩選器之外，此 Cmdlet 還會將此值附加到要求中。</span><span class="sxs-lookup"><span data-stu-id="76b07-143">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="76b07-144">-方案</span><span class="sxs-lookup"><span data-stu-id="76b07-144">-Plan</span></span>
<span data-ttu-id="76b07-145">代表資源規劃屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="76b07-145">A hash table that represents resource plan properties.</span></span>

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

### <span data-ttu-id="76b07-146">-預先</span><span class="sxs-lookup"><span data-stu-id="76b07-146">-Pre</span></span>
<span data-ttu-id="76b07-147">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="76b07-147">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="76b07-148">-屬性</span><span class="sxs-lookup"><span data-stu-id="76b07-148">-Properties</span></span>
<span data-ttu-id="76b07-149">指定資源的資源屬性。</span><span class="sxs-lookup"><span data-stu-id="76b07-149">Specifies resource properties for the resource.</span></span> <span data-ttu-id="76b07-150">使用此參數來指定資源類型專用屬性的值。</span><span class="sxs-lookup"><span data-stu-id="76b07-150">Use this parameter to specify the values of properties that are specific to a resource type.</span></span>

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

### <span data-ttu-id="76b07-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76b07-151">-ResourceGroupName</span></span>
<span data-ttu-id="76b07-152">指定此 Cmdlet 建立資源之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="76b07-152">Specifies the name of the resource group where this cmdlet creates the resource.</span></span>

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

### <span data-ttu-id="76b07-153">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="76b07-153">-ResourceId</span></span>
<span data-ttu-id="76b07-154">指定完全限定的資源識別碼，包括訂閱，如下列範例所示： `/subscriptions/` 訂閱識別碼`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="76b07-154">Specifies the fully qualified resource ID, including the subscription, as in the following example: `/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="76b07-155">-CoNtext.resourcename</span><span class="sxs-lookup"><span data-stu-id="76b07-155">-ResourceName</span></span>
<span data-ttu-id="76b07-156">指定資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="76b07-156">Specifies the name of the resource.</span></span> <span data-ttu-id="76b07-157">例如，若要指定資料庫，請使用下列格式： `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="76b07-157">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="76b07-158">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="76b07-158">-ResourceType</span></span>
<span data-ttu-id="76b07-159">指定資源的類型。</span><span class="sxs-lookup"><span data-stu-id="76b07-159">Specifies the type of the resource.</span></span>
<span data-ttu-id="76b07-160">舉例來說，對於資料庫而言，資源類型如下所示： `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="76b07-160">For instance, for a database, the resource type is as follows: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="76b07-161">-Sku</span><span class="sxs-lookup"><span data-stu-id="76b07-161">-Sku</span></span>
<span data-ttu-id="76b07-162">代表 sku 屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="76b07-162">A hash table that represents sku properties.</span></span>

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

### <span data-ttu-id="76b07-163">-Tag</span><span class="sxs-lookup"><span data-stu-id="76b07-163">-Tag</span></span>
<span data-ttu-id="76b07-164">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="76b07-164">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="76b07-165">例如： @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="76b07-165">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="76b07-166">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="76b07-166">-TenantLevel</span></span>
<span data-ttu-id="76b07-167">表示此 Cmdlet 在租使用者層級運作。</span><span class="sxs-lookup"><span data-stu-id="76b07-167">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="76b07-168">-確認</span><span class="sxs-lookup"><span data-stu-id="76b07-168">-Confirm</span></span>
<span data-ttu-id="76b07-169">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="76b07-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76b07-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76b07-170">-WhatIf</span></span>
<span data-ttu-id="76b07-171">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="76b07-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76b07-172">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="76b07-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76b07-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76b07-173">CommonParameters</span></span>
<span data-ttu-id="76b07-174">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="76b07-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76b07-175">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="76b07-175">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76b07-176">輸入</span><span class="sxs-lookup"><span data-stu-id="76b07-176">INPUTS</span></span>

### <span data-ttu-id="76b07-177">所有</span><span class="sxs-lookup"><span data-stu-id="76b07-177">None</span></span>

## <span data-ttu-id="76b07-178">輸出</span><span class="sxs-lookup"><span data-stu-id="76b07-178">OUTPUTS</span></span>

### <span data-ttu-id="76b07-179">PSResource 中的 ResourceManagement。</span><span class="sxs-lookup"><span data-stu-id="76b07-179">Microsoft.Azure.Commands.ResourceManagement.Models.PSResource</span></span>

## <span data-ttu-id="76b07-180">筆記</span><span class="sxs-lookup"><span data-stu-id="76b07-180">NOTES</span></span>

## <span data-ttu-id="76b07-181">相關連結</span><span class="sxs-lookup"><span data-stu-id="76b07-181">RELATED LINKS</span></span>

[<span data-ttu-id="76b07-182">AzResource</span><span class="sxs-lookup"><span data-stu-id="76b07-182">Get-AzResource</span></span>](./Get-AzResource.md)

[<span data-ttu-id="76b07-183">移動流覽 AzResource</span><span class="sxs-lookup"><span data-stu-id="76b07-183">Move-AzResource</span></span>](./Move-AzResource.md)

[<span data-ttu-id="76b07-184">移除-AzResource</span><span class="sxs-lookup"><span data-stu-id="76b07-184">Remove-AzResource</span></span>](./Remove-AzResource.md)

[<span data-ttu-id="76b07-185">Set-AzResource</span><span class="sxs-lookup"><span data-stu-id="76b07-185">Set-AzResource</span></span>](./Set-AzResource.md)
