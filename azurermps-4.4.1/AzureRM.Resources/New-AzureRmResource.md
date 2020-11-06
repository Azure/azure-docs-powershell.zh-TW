---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: D6FF6BDD-4515-438D-B39D-C0BFC3342F4E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResource.md
ms.openlocfilehash: eb75c1afc0b0fa82c0fee6b734ded951fdfa519f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453291"
---
# <span data-ttu-id="7af7f-101">New-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="7af7f-101">New-AzureRmResource</span></span>

## <span data-ttu-id="7af7f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7af7f-102">SYNOPSIS</span></span>
<span data-ttu-id="7af7f-103">建立資源。</span><span class="sxs-lookup"><span data-stu-id="7af7f-103">Creates a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7af7f-104">句法</span><span class="sxs-lookup"><span data-stu-id="7af7f-104">SYNTAX</span></span>

### <span data-ttu-id="7af7f-105">[資源識別碼] (預設) </span><span class="sxs-lookup"><span data-stu-id="7af7f-105">The resource Id. (Default)</span></span>
```
New-AzureRmResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] -ResourceId <String> [-ODataQuery <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7af7f-106">駐留在訂閱層級的資源。</span><span class="sxs-lookup"><span data-stu-id="7af7f-106">Resource that resides at the subscription level.</span></span>
```
New-AzureRmResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>]
 [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7af7f-107">駐留在租使用者層級的資源。</span><span class="sxs-lookup"><span data-stu-id="7af7f-107">Resource that resides at the tenant level.</span></span>
```
New-AzureRmResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7af7f-108">說明</span><span class="sxs-lookup"><span data-stu-id="7af7f-108">DESCRIPTION</span></span>
<span data-ttu-id="7af7f-109">**新的 AzureRmResource** Cmdlet 會在資源群組中建立 azure 資源，例如網站、Azure SQL database Server 或 Azure SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="7af7f-109">The **New-AzureRmResource** cmdlet creates an Azure resource, such as a website, Azure SQL Database server, or Azure SQL Database, in a resource group.</span></span>

## <span data-ttu-id="7af7f-110">示例</span><span class="sxs-lookup"><span data-stu-id="7af7f-110">EXAMPLES</span></span>

### <span data-ttu-id="7af7f-111">範例1：建立資源</span><span class="sxs-lookup"><span data-stu-id="7af7f-111">Example 1: Create a resource</span></span>
```
PS C:\>New-AzureRmResource -Location "West US" -Properties @{"test"="test"} -ResourceName "TestSite06" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11" -Force
```

<span data-ttu-id="7af7f-112">這個命令會建立 ResourceGroup11 中的網站資源。</span><span class="sxs-lookup"><span data-stu-id="7af7f-112">This command creates a resource that is a website in ResourceGroup11.</span></span>

## <span data-ttu-id="7af7f-113">參數</span><span class="sxs-lookup"><span data-stu-id="7af7f-113">PARAMETERS</span></span>

### <span data-ttu-id="7af7f-114">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="7af7f-114">-ApiVersion</span></span>
<span data-ttu-id="7af7f-115">指定要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="7af7f-115">Specifies the version of the resource provider API to use.</span></span> <span data-ttu-id="7af7f-116">如果您沒有指定版本，此 Cmdlet 會使用最新的可用版本。</span><span class="sxs-lookup"><span data-stu-id="7af7f-116">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="7af7f-117">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="7af7f-117">-ExtensionResourceName</span></span>
<span data-ttu-id="7af7f-118">指定資源延伸資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="7af7f-118">Specifies the name of an extension resource for the resource.</span></span> <span data-ttu-id="7af7f-119">例如，若要指定資料庫，請使用下列格式：</span><span class="sxs-lookup"><span data-stu-id="7af7f-119">For instance, to specify a database, use the following format:</span></span>

<span data-ttu-id="7af7f-120">伺服器名稱 `/` 資料庫名稱</span><span class="sxs-lookup"><span data-stu-id="7af7f-120">server name`/`database name</span></span>

```yaml
Type: System.String
Parameter Sets: Resource that resides at the subscription level., Resource that resides at the tenant level.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7af7f-121">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="7af7f-121">-ExtensionResourceType</span></span>
<span data-ttu-id="7af7f-122">指定延伸資源的資源類型。</span><span class="sxs-lookup"><span data-stu-id="7af7f-122">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="7af7f-123">例如，如果延伸資源是資料庫，請指定下列類型：</span><span class="sxs-lookup"><span data-stu-id="7af7f-123">For instance, if the extension resource is a database, specify the following type:</span></span>

`Microsoft.Sql/Servers/Databases`

```yaml
Type: System.String
Parameter Sets: Resource that resides at the subscription level., Resource that resides at the tenant level.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7af7f-124">-Force</span><span class="sxs-lookup"><span data-stu-id="7af7f-124">-Force</span></span>
<span data-ttu-id="7af7f-125">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="7af7f-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7af7f-126">-IsFullObject</span><span class="sxs-lookup"><span data-stu-id="7af7f-126">-IsFullObject</span></span>
<span data-ttu-id="7af7f-127">指示 *屬性* 參數指定的物件是完整物件。</span><span class="sxs-lookup"><span data-stu-id="7af7f-127">Indicates that the object that the *Properties* parameter specifies is the full object.</span></span>

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

### <span data-ttu-id="7af7f-128">類型</span><span class="sxs-lookup"><span data-stu-id="7af7f-128">-Kind</span></span>
<span data-ttu-id="7af7f-129">指定資源的資源類型。</span><span class="sxs-lookup"><span data-stu-id="7af7f-129">Specifies the resource kind for the resource.</span></span>

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

### <span data-ttu-id="7af7f-130">-位置</span><span class="sxs-lookup"><span data-stu-id="7af7f-130">-Location</span></span>
<span data-ttu-id="7af7f-131">指定資源的位置。</span><span class="sxs-lookup"><span data-stu-id="7af7f-131">Specifies the location of the resource.</span></span>
<span data-ttu-id="7af7f-132">指定資料中心位置，例如 [中北部] 或 [東南部的東南亞]。</span><span class="sxs-lookup"><span data-stu-id="7af7f-132">Specify data center location, such as Central US or Southeast Asia.</span></span>

<span data-ttu-id="7af7f-133">您可以將資源放在支援該類型之資源的任何位置。</span><span class="sxs-lookup"><span data-stu-id="7af7f-133">You can place a resource in any location that supports resources of that type.</span></span> <span data-ttu-id="7af7f-134">資源群組可以包含來自不同位置的資源。</span><span class="sxs-lookup"><span data-stu-id="7af7f-134">Resource groups can contain resources from different locations.</span></span> <span data-ttu-id="7af7f-135">若要判斷哪些位置支援每個資源類型，請使用 Get-AzureLocation Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7af7f-135">To determine which locations support each resource type, use the Get-AzureLocation cmdlet.</span></span>

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

### <span data-ttu-id="7af7f-136">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="7af7f-136">-ODataQuery</span></span>
<span data-ttu-id="7af7f-137">指定 (OData) 樣式篩選的開放式資料通訊協定。</span><span class="sxs-lookup"><span data-stu-id="7af7f-137">Specifies an Open Data Protocol (OData) style filter.</span></span> <span data-ttu-id="7af7f-138">除了任何其他篩選器之外，此 Cmdlet 還會將此值附加到要求中。</span><span class="sxs-lookup"><span data-stu-id="7af7f-138">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="7af7f-139">-方案</span><span class="sxs-lookup"><span data-stu-id="7af7f-139">-Plan</span></span>
<span data-ttu-id="7af7f-140">代表資源規劃屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="7af7f-140">A hash table that represents resource plan properties.</span></span>

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

### <span data-ttu-id="7af7f-141">-預先</span><span class="sxs-lookup"><span data-stu-id="7af7f-141">-Pre</span></span>
<span data-ttu-id="7af7f-142">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="7af7f-142">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="7af7f-143">-屬性</span><span class="sxs-lookup"><span data-stu-id="7af7f-143">-Properties</span></span>
<span data-ttu-id="7af7f-144">指定資源的資源屬性。</span><span class="sxs-lookup"><span data-stu-id="7af7f-144">Specifies resource properties for the resource.</span></span> <span data-ttu-id="7af7f-145">使用此參數來指定資源類型專用屬性的值。</span><span class="sxs-lookup"><span data-stu-id="7af7f-145">Use this parameter to specify the values of properties that are specific to a resource type.</span></span>

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

### <span data-ttu-id="7af7f-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7af7f-146">-ResourceGroupName</span></span>
<span data-ttu-id="7af7f-147">指定此 Cmdlet 建立資源之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="7af7f-147">Specifies the name of the resource group where this cmdlet creates the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Resource that resides at the subscription level.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7af7f-148">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7af7f-148">-ResourceId</span></span>
<span data-ttu-id="7af7f-149">指定完全限定的資源識別碼，包括訂閱，如下列範例所示：</span><span class="sxs-lookup"><span data-stu-id="7af7f-149">Specifies the fully qualified resource ID, including the subscription, as in the following example:</span></span>

<span data-ttu-id="7af7f-150">`/subscriptions/`訂閱識別碼`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="7af7f-150">`/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

```yaml
Type: System.String
Parameter Sets: The resource Id.
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7af7f-151">-CoNtext.resourcename</span><span class="sxs-lookup"><span data-stu-id="7af7f-151">-ResourceName</span></span>
<span data-ttu-id="7af7f-152">指定資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="7af7f-152">Specifies the name of the resource.</span></span> <span data-ttu-id="7af7f-153">例如，若要指定資料庫，請使用下列格式：</span><span class="sxs-lookup"><span data-stu-id="7af7f-153">For instance, to specify a database, use the following format:</span></span>

`ContosoServer/ContosoDatabase`

```yaml
Type: System.String
Parameter Sets: Resource that resides at the subscription level., Resource that resides at the tenant level.
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7af7f-154">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="7af7f-154">-ResourceType</span></span>
<span data-ttu-id="7af7f-155">指定資源的類型。</span><span class="sxs-lookup"><span data-stu-id="7af7f-155">Specifies the type of the resource.</span></span>
<span data-ttu-id="7af7f-156">舉例來說，對於資料庫而言，資源類型如下所示：</span><span class="sxs-lookup"><span data-stu-id="7af7f-156">For instance, for a database, the resource type is as follows:</span></span>

`Microsoft.Sql/Servers/Databases`

```yaml
Type: System.String
Parameter Sets: Resource that resides at the subscription level., Resource that resides at the tenant level.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7af7f-157">-Sku</span><span class="sxs-lookup"><span data-stu-id="7af7f-157">-Sku</span></span>
<span data-ttu-id="7af7f-158">代表 sku 屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="7af7f-158">A hash table that represents sku properties.</span></span>

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

### <span data-ttu-id="7af7f-159">-Tag</span><span class="sxs-lookup"><span data-stu-id="7af7f-159">-Tag</span></span>
<span data-ttu-id="7af7f-160">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="7af7f-160">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="7af7f-161">例如：</span><span class="sxs-lookup"><span data-stu-id="7af7f-161">For example:</span></span>

<span data-ttu-id="7af7f-162">@ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="7af7f-162">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="7af7f-163">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="7af7f-163">-TenantLevel</span></span>
<span data-ttu-id="7af7f-164">表示此 Cmdlet 在租使用者層級運作。</span><span class="sxs-lookup"><span data-stu-id="7af7f-164">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Resource that resides at the tenant level.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7af7f-165">-確認</span><span class="sxs-lookup"><span data-stu-id="7af7f-165">-Confirm</span></span>
<span data-ttu-id="7af7f-166">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7af7f-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7af7f-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7af7f-167">-WhatIf</span></span>
<span data-ttu-id="7af7f-168">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7af7f-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7af7f-169">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7af7f-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7af7f-170">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7af7f-170">-DefaultProfile</span></span>
<span data-ttu-id="7af7f-171">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7af7f-171">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7af7f-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7af7f-172">CommonParameters</span></span>
<span data-ttu-id="7af7f-173">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7af7f-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7af7f-174">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7af7f-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7af7f-175">輸入</span><span class="sxs-lookup"><span data-stu-id="7af7f-175">INPUTS</span></span>

## <span data-ttu-id="7af7f-176">輸出</span><span class="sxs-lookup"><span data-stu-id="7af7f-176">OUTPUTS</span></span>

### <span data-ttu-id="7af7f-177">系統管理. PSObject</span><span class="sxs-lookup"><span data-stu-id="7af7f-177">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="7af7f-178">筆記</span><span class="sxs-lookup"><span data-stu-id="7af7f-178">NOTES</span></span>

## <span data-ttu-id="7af7f-179">相關連結</span><span class="sxs-lookup"><span data-stu-id="7af7f-179">RELATED LINKS</span></span>

[<span data-ttu-id="7af7f-180">尋找-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="7af7f-180">Find-AzureRmResource</span></span>](./Find-AzureRmResource.md)

[<span data-ttu-id="7af7f-181">AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="7af7f-181">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="7af7f-182">移動流覽 AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="7af7f-182">Move-AzureRmResource</span></span>](./Move-AzureRmResource.md)

[<span data-ttu-id="7af7f-183">移除-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="7af7f-183">Remove-AzureRmResource</span></span>](./Remove-AzureRmResource.md)

[<span data-ttu-id="7af7f-184">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="7af7f-184">Set-AzureRmResource</span></span>](./Set-AzureRmResource.md)
