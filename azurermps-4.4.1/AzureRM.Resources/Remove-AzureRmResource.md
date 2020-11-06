---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: A262DFD1-8B90-462C-A4E2-ABA0F51173FA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResource.md
ms.openlocfilehash: 92d6fc81536568b2654fb72a1d6462830c05923e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452368"
---
# <span data-ttu-id="ef46e-101">Remove-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="ef46e-101">Remove-AzureRmResource</span></span>

## <span data-ttu-id="ef46e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ef46e-102">SYNOPSIS</span></span>
<span data-ttu-id="ef46e-103">移除資源。</span><span class="sxs-lookup"><span data-stu-id="ef46e-103">Removes a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ef46e-104">句法</span><span class="sxs-lookup"><span data-stu-id="ef46e-104">SYNTAX</span></span>

### <span data-ttu-id="ef46e-105">[資源識別碼] (預設) </span><span class="sxs-lookup"><span data-stu-id="ef46e-105">The resource Id. (Default)</span></span>
```
Remove-AzureRmResource -ResourceId <String> [-ODataQuery <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef46e-106">駐留在訂閱層級的資源。</span><span class="sxs-lookup"><span data-stu-id="ef46e-106">Resource that resides at the subscription level.</span></span>
```
Remove-AzureRmResource -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ODataQuery <String>] [-ResourceGroupName <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ef46e-107">駐留在租使用者層級的資源。</span><span class="sxs-lookup"><span data-stu-id="ef46e-107">Resource that resides at the tenant level.</span></span>
```
Remove-AzureRmResource -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef46e-108">說明</span><span class="sxs-lookup"><span data-stu-id="ef46e-108">DESCRIPTION</span></span>
<span data-ttu-id="ef46e-109">**AzureRmResource** Cmdlet 會移除 Azure 資源。</span><span class="sxs-lookup"><span data-stu-id="ef46e-109">The **Remove-AzureRmResource** cmdlet removes an Azure resource.</span></span>

## <span data-ttu-id="ef46e-110">示例</span><span class="sxs-lookup"><span data-stu-id="ef46e-110">EXAMPLES</span></span>

### <span data-ttu-id="ef46e-111">範例1：移除網站資源</span><span class="sxs-lookup"><span data-stu-id="ef46e-111">Example 1: Remove a website resource</span></span>
```
PS C:\>Remove-AzureRmResource -ResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup11/providers/Microsoft.Web/sites/ContosoSite" -Force
```

<span data-ttu-id="ef46e-112">這個命令會移除名為 ContosoSite 的網站資源。</span><span class="sxs-lookup"><span data-stu-id="ef46e-112">This command removes the website resource named ContosoSite.</span></span>
<span data-ttu-id="ef46e-113">此範例會使用 [訂閱識別碼] 的預留位置值。</span><span class="sxs-lookup"><span data-stu-id="ef46e-113">The example uses a placeholder value for the subscription ID.</span></span>
<span data-ttu-id="ef46e-114">命令會指定 *Force* 參數。</span><span class="sxs-lookup"><span data-stu-id="ef46e-114">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="ef46e-115">因此，它不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ef46e-115">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="ef46e-116">參數</span><span class="sxs-lookup"><span data-stu-id="ef46e-116">PARAMETERS</span></span>

### <span data-ttu-id="ef46e-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="ef46e-117">-ApiVersion</span></span>
<span data-ttu-id="ef46e-118">指定要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="ef46e-118">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="ef46e-119">如果您沒有指定版本，此 Cmdlet 會使用最新的可用版本。</span><span class="sxs-lookup"><span data-stu-id="ef46e-119">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="ef46e-120">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="ef46e-120">-ExtensionResourceName</span></span>
<span data-ttu-id="ef46e-121">指定此 Cmdlet 移除之資源之延伸資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="ef46e-121">Specifies the name of an extension resource of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="ef46e-122">例如，若要指定資料庫，請使用下列格式：</span><span class="sxs-lookup"><span data-stu-id="ef46e-122">For instance, to specify a database, use the following format:</span></span> 

<span data-ttu-id="ef46e-123">伺服器名稱 `/` 資料庫名稱</span><span class="sxs-lookup"><span data-stu-id="ef46e-123">server name`/`database name</span></span>

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

### <span data-ttu-id="ef46e-124">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="ef46e-124">-ExtensionResourceType</span></span>
<span data-ttu-id="ef46e-125">指定延伸資源的資源類型。</span><span class="sxs-lookup"><span data-stu-id="ef46e-125">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="ef46e-126">指定資源的延伸資源類型。</span><span class="sxs-lookup"><span data-stu-id="ef46e-126">Specifies the extension resource type for the resource.</span></span>
<span data-ttu-id="ef46e-127">例如：</span><span class="sxs-lookup"><span data-stu-id="ef46e-127">For instance:</span></span> 

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

### <span data-ttu-id="ef46e-128">-Force</span><span class="sxs-lookup"><span data-stu-id="ef46e-128">-Force</span></span>
<span data-ttu-id="ef46e-129">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="ef46e-129">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ef46e-130">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="ef46e-130">-ODataQuery</span></span>
<span data-ttu-id="ef46e-131">指定 (OData) 樣式篩選的開放式資料通訊協定。</span><span class="sxs-lookup"><span data-stu-id="ef46e-131">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="ef46e-132">除了任何其他篩選器之外，此 Cmdlet 還會將此值附加到要求中。</span><span class="sxs-lookup"><span data-stu-id="ef46e-132">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="ef46e-133">-預先</span><span class="sxs-lookup"><span data-stu-id="ef46e-133">-Pre</span></span>
<span data-ttu-id="ef46e-134">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="ef46e-134">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="ef46e-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef46e-135">-ResourceGroupName</span></span>
<span data-ttu-id="ef46e-136">指定此 Cmdlet 從中移除資源的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ef46e-136">Specifies the name of the resource group from which this cmdlet removes a resource.</span></span>

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

### <span data-ttu-id="ef46e-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ef46e-137">-ResourceId</span></span>
<span data-ttu-id="ef46e-138">指定此 Cmdlet 移除之資源的完整限定資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="ef46e-138">Specifies the fully qualified resource ID of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="ef46e-139">識別碼包含訂閱，如下列範例所示：</span><span class="sxs-lookup"><span data-stu-id="ef46e-139">The ID includes the subscription, as in the following example:</span></span> 

<span data-ttu-id="ef46e-140">`/subscriptions/`訂閱識別碼`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="ef46e-140">`/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="ef46e-141">-CoNtext.resourcename</span><span class="sxs-lookup"><span data-stu-id="ef46e-141">-ResourceName</span></span>
<span data-ttu-id="ef46e-142">指定此 Cmdlet 移除之資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="ef46e-142">Specifies the name of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="ef46e-143">例如，若要指定資料庫，請使用下列格式：</span><span class="sxs-lookup"><span data-stu-id="ef46e-143">For instance, to specify a database, use the following format:</span></span> 

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

### <span data-ttu-id="ef46e-144">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="ef46e-144">-ResourceType</span></span>
<span data-ttu-id="ef46e-145">指定此 Cmdlet 移除的資源類型。</span><span class="sxs-lookup"><span data-stu-id="ef46e-145">Specifies the type of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="ef46e-146">舉例來說，對於資料庫而言，資源類型如下所示：</span><span class="sxs-lookup"><span data-stu-id="ef46e-146">For instance, for a database, the resource type is as follows:</span></span> 

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

### <span data-ttu-id="ef46e-147">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="ef46e-147">-TenantLevel</span></span>
<span data-ttu-id="ef46e-148">表示此 Cmdlet 在租使用者層級運作。</span><span class="sxs-lookup"><span data-stu-id="ef46e-148">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="ef46e-149">-確認</span><span class="sxs-lookup"><span data-stu-id="ef46e-149">-Confirm</span></span>
<span data-ttu-id="ef46e-150">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ef46e-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef46e-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef46e-151">-WhatIf</span></span>
<span data-ttu-id="ef46e-152">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ef46e-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef46e-153">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ef46e-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef46e-154">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef46e-154">-DefaultProfile</span></span>
<span data-ttu-id="ef46e-155">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ef46e-155">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ef46e-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef46e-156">CommonParameters</span></span>
<span data-ttu-id="ef46e-157">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ef46e-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef46e-158">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ef46e-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef46e-159">輸入</span><span class="sxs-lookup"><span data-stu-id="ef46e-159">INPUTS</span></span>

## <span data-ttu-id="ef46e-160">輸出</span><span class="sxs-lookup"><span data-stu-id="ef46e-160">OUTPUTS</span></span>

### <span data-ttu-id="ef46e-161">System.object</span><span class="sxs-lookup"><span data-stu-id="ef46e-161">System.Boolean</span></span>

## <span data-ttu-id="ef46e-162">筆記</span><span class="sxs-lookup"><span data-stu-id="ef46e-162">NOTES</span></span>

## <span data-ttu-id="ef46e-163">相關連結</span><span class="sxs-lookup"><span data-stu-id="ef46e-163">RELATED LINKS</span></span>

[<span data-ttu-id="ef46e-164">尋找-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="ef46e-164">Find-AzureRmResource</span></span>](./Find-AzureRmResource.md)

[<span data-ttu-id="ef46e-165">AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="ef46e-165">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="ef46e-166">移動流覽 AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="ef46e-166">Move-AzureRmResource</span></span>](./Move-AzureRmResource.md)

[<span data-ttu-id="ef46e-167">新-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="ef46e-167">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="ef46e-168">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="ef46e-168">Set-AzureRmResource</span></span>](./Set-AzureRmResource.md)


