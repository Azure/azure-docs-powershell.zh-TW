---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: D6FF6BDD-4515-438D-B39D-C0BFC3342F4E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResource.md
ms.openlocfilehash: 57e4bd86ad3f5205749579e190960ea4f8e70588
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623539"
---
# <span data-ttu-id="5a178-101">New-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="5a178-101">New-AzureRmResource</span></span>

## <span data-ttu-id="5a178-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5a178-102">SYNOPSIS</span></span>
<span data-ttu-id="5a178-103">建立資源。</span><span class="sxs-lookup"><span data-stu-id="5a178-103">Creates a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5a178-104">句法</span><span class="sxs-lookup"><span data-stu-id="5a178-104">SYNTAX</span></span>

### <span data-ttu-id="5a178-105">ByResourceId (預設) </span><span class="sxs-lookup"><span data-stu-id="5a178-105">ByResourceId (Default)</span></span>
```
New-AzureRmResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceId <String> [-ODataQuery <String>]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5a178-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="5a178-106">BySubscriptionLevel</span></span>
```
New-AzureRmResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>]
 [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a178-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="5a178-107">ByTenantLevel</span></span>
```
New-AzureRmResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5a178-108">說明</span><span class="sxs-lookup"><span data-stu-id="5a178-108">DESCRIPTION</span></span>
<span data-ttu-id="5a178-109">**新的 AzureRmResource** Cmdlet 會在資源群組中建立 azure 資源，例如網站、Azure SQL database Server 或 Azure SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="5a178-109">The **New-AzureRmResource** cmdlet creates an Azure resource, such as a website, Azure SQL Database server, or Azure SQL Database, in a resource group.</span></span>

## <span data-ttu-id="5a178-110">示例</span><span class="sxs-lookup"><span data-stu-id="5a178-110">EXAMPLES</span></span>

### <span data-ttu-id="5a178-111">範例1：建立資源</span><span class="sxs-lookup"><span data-stu-id="5a178-111">Example 1: Create a resource</span></span>
```
PS> New-AzureRmResource -Location "West US" -Properties @{test="test"} -ResourceName TestSite06 -ResourceType microsoft.web/sites -ResourceGroupName ResourceGroup11 -Force
```

<span data-ttu-id="5a178-112">這個命令會建立 ResourceGroup11 中的網站資源。</span><span class="sxs-lookup"><span data-stu-id="5a178-112">This command creates a resource that is a website in ResourceGroup11.</span></span>

### <span data-ttu-id="5a178-113">範例2：使用 splatting 建立資源</span><span class="sxs-lookup"><span data-stu-id="5a178-113">Example 2: Create a resource using splatting</span></span>
```
PS> $prop = @{
    Location          = "West US" 
    Properties        = @{test = "test"} 
    ResourceName      = "TestSite06" 
    ResourceType      = "microsoft.web/sites" 
    ResourceGroupName = "ResourceGroup11" 
    Force             = $true
}

PS> New-AzureRmResource @prop
```

<span data-ttu-id="5a178-114">這個命令會建立 ResourceGroup11 中的網站資源。</span><span class="sxs-lookup"><span data-stu-id="5a178-114">This command creates a resource that is a website in ResourceGroup11.</span></span>

## <span data-ttu-id="5a178-115">參數</span><span class="sxs-lookup"><span data-stu-id="5a178-115">PARAMETERS</span></span>

### <span data-ttu-id="5a178-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="5a178-116">-ApiVersion</span></span>
<span data-ttu-id="5a178-117">指定要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="5a178-117">Specifies the version of the resource provider API to use.</span></span> <span data-ttu-id="5a178-118">如果您沒有指定版本，此 Cmdlet 會使用最新的可用版本。</span><span class="sxs-lookup"><span data-stu-id="5a178-118">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="5a178-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5a178-119">-AsJob</span></span>
<span data-ttu-id="5a178-120">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5a178-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5a178-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a178-121">-DefaultProfile</span></span>
<span data-ttu-id="5a178-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="5a178-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5a178-123">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="5a178-123">-ExtensionResourceName</span></span>
<span data-ttu-id="5a178-124">指定資源延伸資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="5a178-124">Specifies the name of an extension resource for the resource.</span></span> <span data-ttu-id="5a178-125">例如，若要指定資料庫，請使用下列格式：伺服器名稱 `/` 資料庫名稱</span><span class="sxs-lookup"><span data-stu-id="5a178-125">For instance, to specify a database, use the following format: server name`/`database name</span></span>

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

### <span data-ttu-id="5a178-126">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="5a178-126">-ExtensionResourceType</span></span>
<span data-ttu-id="5a178-127">指定延伸資源的資源類型。</span><span class="sxs-lookup"><span data-stu-id="5a178-127">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="5a178-128">例如，如果延伸資源是資料庫，請指定下列類型： `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="5a178-128">For instance, if the extension resource is a database, specify the following type: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="5a178-129">-Force</span><span class="sxs-lookup"><span data-stu-id="5a178-129">-Force</span></span>
<span data-ttu-id="5a178-130">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="5a178-130">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5a178-131">-IsFullObject</span><span class="sxs-lookup"><span data-stu-id="5a178-131">-IsFullObject</span></span>
<span data-ttu-id="5a178-132">指示 *屬性* 參數指定的物件是完整物件。</span><span class="sxs-lookup"><span data-stu-id="5a178-132">Indicates that the object that the *Properties* parameter specifies is the full object.</span></span>

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

### <span data-ttu-id="5a178-133">類型</span><span class="sxs-lookup"><span data-stu-id="5a178-133">-Kind</span></span>
<span data-ttu-id="5a178-134">指定資源的資源類型。</span><span class="sxs-lookup"><span data-stu-id="5a178-134">Specifies the resource kind for the resource.</span></span>

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

### <span data-ttu-id="5a178-135">-位置</span><span class="sxs-lookup"><span data-stu-id="5a178-135">-Location</span></span>
<span data-ttu-id="5a178-136">指定資源的位置。</span><span class="sxs-lookup"><span data-stu-id="5a178-136">Specifies the location of the resource.</span></span>
<span data-ttu-id="5a178-137">指定資料中心位置，例如 [中北部] 或 [東南部的東南亞]。</span><span class="sxs-lookup"><span data-stu-id="5a178-137">Specify data center location, such as Central US or Southeast Asia.</span></span>
<span data-ttu-id="5a178-138">您可以將資源放在支援該類型之資源的任何位置。</span><span class="sxs-lookup"><span data-stu-id="5a178-138">You can place a resource in any location that supports resources of that type.</span></span> <span data-ttu-id="5a178-139">資源群組可以包含來自不同位置的資源。</span><span class="sxs-lookup"><span data-stu-id="5a178-139">Resource groups can contain resources from different locations.</span></span> <span data-ttu-id="5a178-140">若要判斷哪些位置支援每個資源類型，請使用 Get-AzureLocation Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5a178-140">To determine which locations support each resource type, use the Get-AzureLocation cmdlet.</span></span>

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

### <span data-ttu-id="5a178-141">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="5a178-141">-ODataQuery</span></span>
<span data-ttu-id="5a178-142">指定 (OData) 樣式篩選的開放式資料通訊協定。</span><span class="sxs-lookup"><span data-stu-id="5a178-142">Specifies an Open Data Protocol (OData) style filter.</span></span> <span data-ttu-id="5a178-143">除了任何其他篩選器之外，此 Cmdlet 還會將此值附加到要求中。</span><span class="sxs-lookup"><span data-stu-id="5a178-143">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="5a178-144">-方案</span><span class="sxs-lookup"><span data-stu-id="5a178-144">-Plan</span></span>
<span data-ttu-id="5a178-145">代表資源規劃屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="5a178-145">A hash table that represents resource plan properties.</span></span>

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

### <span data-ttu-id="5a178-146">-預先</span><span class="sxs-lookup"><span data-stu-id="5a178-146">-Pre</span></span>
<span data-ttu-id="5a178-147">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="5a178-147">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="5a178-148">-屬性</span><span class="sxs-lookup"><span data-stu-id="5a178-148">-Properties</span></span>
<span data-ttu-id="5a178-149">指定資源的資源屬性。</span><span class="sxs-lookup"><span data-stu-id="5a178-149">Specifies resource properties for the resource.</span></span> <span data-ttu-id="5a178-150">使用此參數來指定資源類型專用屬性的值。</span><span class="sxs-lookup"><span data-stu-id="5a178-150">Use this parameter to specify the values of properties that are specific to a resource type.</span></span>

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

### <span data-ttu-id="5a178-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a178-151">-ResourceGroupName</span></span>
<span data-ttu-id="5a178-152">指定此 Cmdlet 建立資源之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5a178-152">Specifies the name of the resource group where this cmdlet creates the resource.</span></span>

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

### <span data-ttu-id="5a178-153">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5a178-153">-ResourceId</span></span>
<span data-ttu-id="5a178-154">指定完全限定的資源識別碼，包括訂閱，如下列範例所示： `/subscriptions/` 訂閱識別碼`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="5a178-154">Specifies the fully qualified resource ID, including the subscription, as in the following example: `/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="5a178-155">-CoNtext.resourcename</span><span class="sxs-lookup"><span data-stu-id="5a178-155">-ResourceName</span></span>
<span data-ttu-id="5a178-156">指定資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="5a178-156">Specifies the name of the resource.</span></span> <span data-ttu-id="5a178-157">例如，若要指定資料庫，請使用下列格式： `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="5a178-157">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="5a178-158">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="5a178-158">-ResourceType</span></span>
<span data-ttu-id="5a178-159">指定資源的類型。</span><span class="sxs-lookup"><span data-stu-id="5a178-159">Specifies the type of the resource.</span></span>
<span data-ttu-id="5a178-160">舉例來說，對於資料庫而言，資源類型如下所示： `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="5a178-160">For instance, for a database, the resource type is as follows: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="5a178-161">-Sku</span><span class="sxs-lookup"><span data-stu-id="5a178-161">-Sku</span></span>
<span data-ttu-id="5a178-162">代表 sku 屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="5a178-162">A hash table that represents sku properties.</span></span>

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

### <span data-ttu-id="5a178-163">-Tag</span><span class="sxs-lookup"><span data-stu-id="5a178-163">-Tag</span></span>
<span data-ttu-id="5a178-164">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="5a178-164">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="5a178-165">例如： @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="5a178-165">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="5a178-166">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="5a178-166">-TenantLevel</span></span>
<span data-ttu-id="5a178-167">表示此 Cmdlet 在租使用者層級運作。</span><span class="sxs-lookup"><span data-stu-id="5a178-167">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="5a178-168">-確認</span><span class="sxs-lookup"><span data-stu-id="5a178-168">-Confirm</span></span>
<span data-ttu-id="5a178-169">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5a178-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a178-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a178-170">-WhatIf</span></span>
<span data-ttu-id="5a178-171">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5a178-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a178-172">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5a178-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a178-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a178-173">CommonParameters</span></span>
<span data-ttu-id="5a178-174">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5a178-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a178-175">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5a178-175">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a178-176">輸入</span><span class="sxs-lookup"><span data-stu-id="5a178-176">INPUTS</span></span>

### <span data-ttu-id="5a178-177">所有</span><span class="sxs-lookup"><span data-stu-id="5a178-177">None</span></span>

## <span data-ttu-id="5a178-178">輸出</span><span class="sxs-lookup"><span data-stu-id="5a178-178">OUTPUTS</span></span>

### <span data-ttu-id="5a178-179">PSResource 中的 ResourceManagement。</span><span class="sxs-lookup"><span data-stu-id="5a178-179">Microsoft.Azure.Commands.ResourceManagement.Models.PSResource</span></span>

## <span data-ttu-id="5a178-180">筆記</span><span class="sxs-lookup"><span data-stu-id="5a178-180">NOTES</span></span>

## <span data-ttu-id="5a178-181">相關連結</span><span class="sxs-lookup"><span data-stu-id="5a178-181">RELATED LINKS</span></span>

[<span data-ttu-id="5a178-182">尋找-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="5a178-182">Find-AzureRmResource</span></span>](./Find-AzureRmResource.md)

[<span data-ttu-id="5a178-183">AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="5a178-183">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="5a178-184">移動流覽 AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="5a178-184">Move-AzureRmResource</span></span>](./Move-AzureRmResource.md)

[<span data-ttu-id="5a178-185">移除-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="5a178-185">Remove-AzureRmResource</span></span>](./Remove-AzureRmResource.md)

[<span data-ttu-id="5a178-186">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="5a178-186">Set-AzureRmResource</span></span>](./Set-AzureRmResource.md)
