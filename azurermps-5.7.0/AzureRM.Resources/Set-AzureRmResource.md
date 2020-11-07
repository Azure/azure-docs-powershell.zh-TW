---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: A00160B9-831F-4A20-8D9D-9E89BC4F5C91
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmResource.md
ms.openlocfilehash: 9b1f12060ca7cc161f4f7fbe7c99948d9ddd10f8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625446"
---
# <span data-ttu-id="7c662-101">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="7c662-101">Set-AzureRmResource</span></span>

## <span data-ttu-id="7c662-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7c662-102">SYNOPSIS</span></span>
<span data-ttu-id="7c662-103">修改資源。</span><span class="sxs-lookup"><span data-stu-id="7c662-103">Modifies a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7c662-104">句法</span><span class="sxs-lookup"><span data-stu-id="7c662-104">SYNTAX</span></span>

### <span data-ttu-id="7c662-105">ByResourceId (預設) </span><span class="sxs-lookup"><span data-stu-id="7c662-105">ByResourceId (Default)</span></span>
```
Set-AzureRmResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] -ResourceId <String> [-ODataQuery <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7c662-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="7c662-106">BySubscriptionLevel</span></span>
```
Set-AzureRmResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>]
 [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c662-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="7c662-107">ByTenantLevel</span></span>
```
Set-AzureRmResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7c662-108">說明</span><span class="sxs-lookup"><span data-stu-id="7c662-108">DESCRIPTION</span></span>
<span data-ttu-id="7c662-109">**AzureRmResource** Cmdlet 會修改現有的 Azure 資源。</span><span class="sxs-lookup"><span data-stu-id="7c662-109">The **Set-AzureRmResource** cmdlet modifies an existing Azure resource.</span></span>
<span data-ttu-id="7c662-110">指定要依名稱和類型或依識別碼來修改的資源。</span><span class="sxs-lookup"><span data-stu-id="7c662-110">Specify a resource to modify by name and type or by ID.</span></span>

## <span data-ttu-id="7c662-111">示例</span><span class="sxs-lookup"><span data-stu-id="7c662-111">EXAMPLES</span></span>

### <span data-ttu-id="7c662-112">範例1：修改資源</span><span class="sxs-lookup"><span data-stu-id="7c662-112">Example 1: Modify a resource</span></span>
```
PS C:\>$Resource = Get-AzureRmResource -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11" -ResourceName "ContosoSite"
PS C:\> $Resource.Properties.Enabled = "False"
PS C:\> $Resource | Set-AzureRmResource -Force
```

<span data-ttu-id="7c662-113">第一個命令會使用 Get-AzureRmResource Cmdlet 來取得名為 ContosoSite 的資源，然後將它儲存在 $Resource 變數中。</span><span class="sxs-lookup"><span data-stu-id="7c662-113">The first command gets the resource named ContosoSite by using the Get-AzureRmResource cmdlet, and then stores it in the $Resource variable.</span></span>

<span data-ttu-id="7c662-114">第二個命令會修改 $Resource 的屬性。</span><span class="sxs-lookup"><span data-stu-id="7c662-114">The second command modifies a property of $Resource.</span></span>

<span data-ttu-id="7c662-115">最後一個命令會更新資源以符合 $Resource。</span><span class="sxs-lookup"><span data-stu-id="7c662-115">The final command updates the resource to match $Resource.</span></span>

## <span data-ttu-id="7c662-116">參數</span><span class="sxs-lookup"><span data-stu-id="7c662-116">PARAMETERS</span></span>

### <span data-ttu-id="7c662-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="7c662-117">-ApiVersion</span></span>
<span data-ttu-id="7c662-118">指定要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="7c662-118">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="7c662-119">如果您沒有指定版本，此 Cmdlet 會使用最新的可用版本。</span><span class="sxs-lookup"><span data-stu-id="7c662-119">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="7c662-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7c662-120">-AsJob</span></span>
<span data-ttu-id="7c662-121">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="7c662-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7c662-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c662-122">-DefaultProfile</span></span>
<span data-ttu-id="7c662-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="7c662-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7c662-124">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="7c662-124">-ExtensionResourceName</span></span>
<span data-ttu-id="7c662-125">指定資源延伸資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="7c662-125">Specifies the name of an extension resource for the resource.</span></span>
<span data-ttu-id="7c662-126">例如，若要指定資料庫，請使用下列格式：</span><span class="sxs-lookup"><span data-stu-id="7c662-126">For instance, to specify a database, use the following format:</span></span>

<span data-ttu-id="7c662-127">伺服器名稱 `/` 資料庫名稱</span><span class="sxs-lookup"><span data-stu-id="7c662-127">server name`/`database name</span></span>

```yaml
Type: String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c662-128">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="7c662-128">-ExtensionResourceType</span></span>
<span data-ttu-id="7c662-129">指定延伸資源的資源類型。</span><span class="sxs-lookup"><span data-stu-id="7c662-129">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="7c662-130">例如，如果延伸資源是資料庫，請指定下列各項：</span><span class="sxs-lookup"><span data-stu-id="7c662-130">For instance, if the extension resource is a database specify the following:</span></span>

`Microsoft.Sql/Servers/Databases`

```yaml
Type: String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c662-131">-Force</span><span class="sxs-lookup"><span data-stu-id="7c662-131">-Force</span></span>
<span data-ttu-id="7c662-132">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="7c662-132">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7c662-133">類型</span><span class="sxs-lookup"><span data-stu-id="7c662-133">-Kind</span></span>
<span data-ttu-id="7c662-134">指定資源的資源類型。</span><span class="sxs-lookup"><span data-stu-id="7c662-134">Specifies the resource kind for the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c662-135">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="7c662-135">-ODataQuery</span></span>
<span data-ttu-id="7c662-136">指定 (OData) 樣式篩選的開放式資料通訊協定。</span><span class="sxs-lookup"><span data-stu-id="7c662-136">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="7c662-137">除了任何其他篩選器之外，此 Cmdlet 還會將此值附加到要求中。</span><span class="sxs-lookup"><span data-stu-id="7c662-137">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="7c662-138">-方案</span><span class="sxs-lookup"><span data-stu-id="7c662-138">-Plan</span></span>
<span data-ttu-id="7c662-139">以雜湊資料表的形式指定資源的資源計劃屬性。</span><span class="sxs-lookup"><span data-stu-id="7c662-139">Specifies resource plan properties, as a hash table, for the resource.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: PlanObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c662-140">-預先</span><span class="sxs-lookup"><span data-stu-id="7c662-140">-Pre</span></span>
<span data-ttu-id="7c662-141">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="7c662-141">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="7c662-142">-屬性</span><span class="sxs-lookup"><span data-stu-id="7c662-142">-Properties</span></span>
<span data-ttu-id="7c662-143">指定資源的資源屬性。</span><span class="sxs-lookup"><span data-stu-id="7c662-143">Specifies resource properties for the resource.</span></span>

```yaml
Type: PSObject
Parameter Sets: (All)
Aliases: PropertyObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c662-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c662-144">-ResourceGroupName</span></span>
<span data-ttu-id="7c662-145">指定此 Cmdlet 修改資源之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="7c662-145">Specifies the name of the resource group where this cmdlet modifies the resource.</span></span>

```yaml
Type: String
Parameter Sets: BySubscriptionLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c662-146">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7c662-146">-ResourceId</span></span>
<span data-ttu-id="7c662-147">指定完全限定的資源識別碼，包括訂閱，如下列範例所示：</span><span class="sxs-lookup"><span data-stu-id="7c662-147">Specifies the fully qualified resource ID, including the subscription, as in the following example:</span></span>

<span data-ttu-id="7c662-148">`/subscriptions/`訂閱識別碼`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="7c662-148">`/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c662-149">-CoNtext.resourcename</span><span class="sxs-lookup"><span data-stu-id="7c662-149">-ResourceName</span></span>
<span data-ttu-id="7c662-150">指定資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="7c662-150">Specifies the name of the resource.</span></span>
<span data-ttu-id="7c662-151">例如，若要指定資料庫，請使用下列格式：</span><span class="sxs-lookup"><span data-stu-id="7c662-151">For instance, to specify a database, use the following format:</span></span>

`ContosoServer/ContosoDatabase`

```yaml
Type: String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c662-152">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="7c662-152">-ResourceType</span></span>
<span data-ttu-id="7c662-153">指定資源的類型。</span><span class="sxs-lookup"><span data-stu-id="7c662-153">Specifies the type of the resource.</span></span>
<span data-ttu-id="7c662-154">舉例來說，對於資料庫而言，資源類型如下所示：</span><span class="sxs-lookup"><span data-stu-id="7c662-154">For instance, for a database, the resource type is as follows:</span></span>

`Microsoft.Sql/Servers/Databases`

```yaml
Type: String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c662-155">-Sku</span><span class="sxs-lookup"><span data-stu-id="7c662-155">-Sku</span></span>
<span data-ttu-id="7c662-156">將資源的 SKU 物件指定為雜湊表。</span><span class="sxs-lookup"><span data-stu-id="7c662-156">Specifies the SKU object of the resource as a hash table.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: SkuObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c662-157">-Tag</span><span class="sxs-lookup"><span data-stu-id="7c662-157">-Tag</span></span>
<span data-ttu-id="7c662-158">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="7c662-158">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="7c662-159">例如：</span><span class="sxs-lookup"><span data-stu-id="7c662-159">For example:</span></span>

<span data-ttu-id="7c662-160">@ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="7c662-160">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c662-161">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="7c662-161">-TenantLevel</span></span>
<span data-ttu-id="7c662-162">表示此 Cmdlet 在租使用者層級運作。</span><span class="sxs-lookup"><span data-stu-id="7c662-162">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c662-163">-UsePatchSemantics</span><span class="sxs-lookup"><span data-stu-id="7c662-163">-UsePatchSemantics</span></span>
<span data-ttu-id="7c662-164">表示此 Cmdlet 使用 HTTP 修補程式來更新物件，而不是 HTTP PUT。</span><span class="sxs-lookup"><span data-stu-id="7c662-164">Indicates that this cmdlet uses an HTTP PATCH to update the object, instead of an HTTP PUT.</span></span>

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

### <span data-ttu-id="7c662-165">-確認</span><span class="sxs-lookup"><span data-stu-id="7c662-165">-Confirm</span></span>
<span data-ttu-id="7c662-166">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7c662-166">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c662-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c662-167">-WhatIf</span></span>
<span data-ttu-id="7c662-168">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7c662-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c662-169">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7c662-169">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c662-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c662-170">CommonParameters</span></span>
<span data-ttu-id="7c662-171">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7c662-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c662-172">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7c662-172">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c662-173">輸入</span><span class="sxs-lookup"><span data-stu-id="7c662-173">INPUTS</span></span>

### <span data-ttu-id="7c662-174">所有</span><span class="sxs-lookup"><span data-stu-id="7c662-174">None</span></span>
<span data-ttu-id="7c662-175">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="7c662-175">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7c662-176">輸出</span><span class="sxs-lookup"><span data-stu-id="7c662-176">OUTPUTS</span></span>

### <span data-ttu-id="7c662-177">系統管理. PSObject</span><span class="sxs-lookup"><span data-stu-id="7c662-177">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="7c662-178">筆記</span><span class="sxs-lookup"><span data-stu-id="7c662-178">NOTES</span></span>

## <span data-ttu-id="7c662-179">相關連結</span><span class="sxs-lookup"><span data-stu-id="7c662-179">RELATED LINKS</span></span>

[<span data-ttu-id="7c662-180">尋找-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="7c662-180">Find-AzureRmResource</span></span>](./Find-AzureRmResource.md)

[<span data-ttu-id="7c662-181">AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="7c662-181">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="7c662-182">移動流覽 AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="7c662-182">Move-AzureRmResource</span></span>](./Move-AzureRmResource.md)

[<span data-ttu-id="7c662-183">新-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="7c662-183">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="7c662-184">移除-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="7c662-184">Remove-AzureRmResource</span></span>](./Remove-AzureRmResource.md)
