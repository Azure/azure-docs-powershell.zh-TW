---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: A262DFD1-8B90-462C-A4E2-ABA0F51173FA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResource.md
ms.openlocfilehash: 0cf65c33ca5af99be30f7bfa85ad4ad80ff62735
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450503"
---
# <span data-ttu-id="f302d-101">Remove-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="f302d-101">Remove-AzureRmResource</span></span>

## <span data-ttu-id="f302d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f302d-102">SYNOPSIS</span></span>
<span data-ttu-id="f302d-103">移除資源。</span><span class="sxs-lookup"><span data-stu-id="f302d-103">Removes a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f302d-104">句法</span><span class="sxs-lookup"><span data-stu-id="f302d-104">SYNTAX</span></span>

### <span data-ttu-id="f302d-105">ByResourceId (預設) </span><span class="sxs-lookup"><span data-stu-id="f302d-105">ByResourceId (Default)</span></span>
```
Remove-AzureRmResource [-AsJob] -ResourceId <String> [-ODataQuery <String>] [-Force] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f302d-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="f302d-106">BySubscriptionLevel</span></span>
```
Remove-AzureRmResource [-AsJob] -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ODataQuery <String>] [-ResourceGroupName <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f302d-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="f302d-107">ByTenantLevel</span></span>
```
Remove-AzureRmResource [-AsJob] -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f302d-108">說明</span><span class="sxs-lookup"><span data-stu-id="f302d-108">DESCRIPTION</span></span>
<span data-ttu-id="f302d-109">**AzureRmResource** Cmdlet 會移除 Azure 資源。</span><span class="sxs-lookup"><span data-stu-id="f302d-109">The **Remove-AzureRmResource** cmdlet removes an Azure resource.</span></span>

## <span data-ttu-id="f302d-110">示例</span><span class="sxs-lookup"><span data-stu-id="f302d-110">EXAMPLES</span></span>

### <span data-ttu-id="f302d-111">範例1：移除網站資源</span><span class="sxs-lookup"><span data-stu-id="f302d-111">Example 1: Remove a website resource</span></span>
```
PS C:\>Remove-AzureRmResource -ResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup11/providers/Microsoft.Web/sites/ContosoSite" -Force
```

<span data-ttu-id="f302d-112">這個命令會移除名為 ContosoSite 的網站資源。</span><span class="sxs-lookup"><span data-stu-id="f302d-112">This command removes the website resource named ContosoSite.</span></span>
<span data-ttu-id="f302d-113">此範例會使用 [訂閱識別碼] 的預留位置值。</span><span class="sxs-lookup"><span data-stu-id="f302d-113">The example uses a placeholder value for the subscription ID.</span></span>
<span data-ttu-id="f302d-114">命令會指定 *Force* 參數。</span><span class="sxs-lookup"><span data-stu-id="f302d-114">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="f302d-115">因此，它不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f302d-115">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="f302d-116">參數</span><span class="sxs-lookup"><span data-stu-id="f302d-116">PARAMETERS</span></span>

### <span data-ttu-id="f302d-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="f302d-117">-ApiVersion</span></span>
<span data-ttu-id="f302d-118">指定要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="f302d-118">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="f302d-119">如果您沒有指定版本，此 Cmdlet 會使用最新的可用版本。</span><span class="sxs-lookup"><span data-stu-id="f302d-119">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="f302d-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f302d-120">-AsJob</span></span>
<span data-ttu-id="f302d-121">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f302d-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f302d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f302d-122">-DefaultProfile</span></span>
<span data-ttu-id="f302d-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="f302d-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f302d-124">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="f302d-124">-ExtensionResourceName</span></span>
<span data-ttu-id="f302d-125">指定此 Cmdlet 移除之資源之延伸資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="f302d-125">Specifies the name of an extension resource of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="f302d-126">例如，若要指定資料庫，請使用下列格式：</span><span class="sxs-lookup"><span data-stu-id="f302d-126">For instance, to specify a database, use the following format:</span></span> 

<span data-ttu-id="f302d-127">伺服器名稱 `/` 資料庫名稱</span><span class="sxs-lookup"><span data-stu-id="f302d-127">server name`/`database name</span></span>

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

### <span data-ttu-id="f302d-128">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="f302d-128">-ExtensionResourceType</span></span>
<span data-ttu-id="f302d-129">指定延伸資源的資源類型。</span><span class="sxs-lookup"><span data-stu-id="f302d-129">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="f302d-130">指定資源的延伸資源類型。</span><span class="sxs-lookup"><span data-stu-id="f302d-130">Specifies the extension resource type for the resource.</span></span>
<span data-ttu-id="f302d-131">例如：</span><span class="sxs-lookup"><span data-stu-id="f302d-131">For instance:</span></span> 

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

### <span data-ttu-id="f302d-132">-Force</span><span class="sxs-lookup"><span data-stu-id="f302d-132">-Force</span></span>
<span data-ttu-id="f302d-133">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="f302d-133">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f302d-134">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="f302d-134">-ODataQuery</span></span>
<span data-ttu-id="f302d-135">指定 (OData) 樣式篩選的開放式資料通訊協定。</span><span class="sxs-lookup"><span data-stu-id="f302d-135">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="f302d-136">除了任何其他篩選器之外，此 Cmdlet 還會將此值附加到要求中。</span><span class="sxs-lookup"><span data-stu-id="f302d-136">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="f302d-137">-預先</span><span class="sxs-lookup"><span data-stu-id="f302d-137">-Pre</span></span>
<span data-ttu-id="f302d-138">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="f302d-138">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="f302d-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f302d-139">-ResourceGroupName</span></span>
<span data-ttu-id="f302d-140">指定此 Cmdlet 從中移除資源的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f302d-140">Specifies the name of the resource group from which this cmdlet removes a resource.</span></span>

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

### <span data-ttu-id="f302d-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f302d-141">-ResourceId</span></span>
<span data-ttu-id="f302d-142">指定此 Cmdlet 移除之資源的完整限定資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="f302d-142">Specifies the fully qualified resource ID of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="f302d-143">識別碼包含訂閱，如下列範例所示：</span><span class="sxs-lookup"><span data-stu-id="f302d-143">The ID includes the subscription, as in the following example:</span></span> 

<span data-ttu-id="f302d-144">`/subscriptions/`訂閱識別碼`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="f302d-144">`/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="f302d-145">-CoNtext.resourcename</span><span class="sxs-lookup"><span data-stu-id="f302d-145">-ResourceName</span></span>
<span data-ttu-id="f302d-146">指定此 Cmdlet 移除之資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="f302d-146">Specifies the name of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="f302d-147">例如，若要指定資料庫，請使用下列格式：</span><span class="sxs-lookup"><span data-stu-id="f302d-147">For instance, to specify a database, use the following format:</span></span> 

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

### <span data-ttu-id="f302d-148">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="f302d-148">-ResourceType</span></span>
<span data-ttu-id="f302d-149">指定此 Cmdlet 移除的資源類型。</span><span class="sxs-lookup"><span data-stu-id="f302d-149">Specifies the type of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="f302d-150">舉例來說，對於資料庫而言，資源類型如下所示：</span><span class="sxs-lookup"><span data-stu-id="f302d-150">For instance, for a database, the resource type is as follows:</span></span> 

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

### <span data-ttu-id="f302d-151">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="f302d-151">-TenantLevel</span></span>
<span data-ttu-id="f302d-152">表示此 Cmdlet 在租使用者層級運作。</span><span class="sxs-lookup"><span data-stu-id="f302d-152">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="f302d-153">-確認</span><span class="sxs-lookup"><span data-stu-id="f302d-153">-Confirm</span></span>
<span data-ttu-id="f302d-154">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f302d-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f302d-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f302d-155">-WhatIf</span></span>
<span data-ttu-id="f302d-156">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f302d-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f302d-157">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f302d-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f302d-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f302d-158">CommonParameters</span></span>
<span data-ttu-id="f302d-159">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f302d-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f302d-160">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f302d-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f302d-161">輸入</span><span class="sxs-lookup"><span data-stu-id="f302d-161">INPUTS</span></span>

### <span data-ttu-id="f302d-162">所有</span><span class="sxs-lookup"><span data-stu-id="f302d-162">None</span></span>
<span data-ttu-id="f302d-163">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="f302d-163">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f302d-164">輸出</span><span class="sxs-lookup"><span data-stu-id="f302d-164">OUTPUTS</span></span>

### <span data-ttu-id="f302d-165">System.object</span><span class="sxs-lookup"><span data-stu-id="f302d-165">System.Boolean</span></span>

## <span data-ttu-id="f302d-166">筆記</span><span class="sxs-lookup"><span data-stu-id="f302d-166">NOTES</span></span>

## <span data-ttu-id="f302d-167">相關連結</span><span class="sxs-lookup"><span data-stu-id="f302d-167">RELATED LINKS</span></span>

[<span data-ttu-id="f302d-168">尋找-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="f302d-168">Find-AzureRmResource</span></span>](./Find-AzureRmResource.md)

[<span data-ttu-id="f302d-169">AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="f302d-169">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="f302d-170">移動流覽 AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="f302d-170">Move-AzureRmResource</span></span>](./Move-AzureRmResource.md)

[<span data-ttu-id="f302d-171">新-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="f302d-171">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="f302d-172">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="f302d-172">Set-AzureRmResource</span></span>](./Set-AzureRmResource.md)


