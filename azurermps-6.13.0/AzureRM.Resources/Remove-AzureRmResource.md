---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: A262DFD1-8B90-462C-A4E2-ABA0F51173FA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResource.md
ms.openlocfilehash: cbe72ac0c1b62a11b48113bd9043118f3750f37b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625567"
---
# <span data-ttu-id="c492b-101">Remove-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="c492b-101">Remove-AzureRmResource</span></span>

## <span data-ttu-id="c492b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c492b-102">SYNOPSIS</span></span>
<span data-ttu-id="c492b-103">移除資源。</span><span class="sxs-lookup"><span data-stu-id="c492b-103">Removes a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c492b-104">句法</span><span class="sxs-lookup"><span data-stu-id="c492b-104">SYNTAX</span></span>

### <span data-ttu-id="c492b-105">ByResourceId (預設) </span><span class="sxs-lookup"><span data-stu-id="c492b-105">ByResourceId (Default)</span></span>
```
Remove-AzureRmResource [-AsJob] -ResourceId <String> [-ODataQuery <String>] [-Force] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c492b-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="c492b-106">BySubscriptionLevel</span></span>
```
Remove-AzureRmResource [-AsJob] -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ODataQuery <String>] [-ResourceGroupName <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c492b-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="c492b-107">ByTenantLevel</span></span>
```
Remove-AzureRmResource [-AsJob] -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c492b-108">說明</span><span class="sxs-lookup"><span data-stu-id="c492b-108">DESCRIPTION</span></span>
<span data-ttu-id="c492b-109">**AzureRmResource** Cmdlet 會移除 Azure 資源。</span><span class="sxs-lookup"><span data-stu-id="c492b-109">The **Remove-AzureRmResource** cmdlet removes an Azure resource.</span></span>

## <span data-ttu-id="c492b-110">示例</span><span class="sxs-lookup"><span data-stu-id="c492b-110">EXAMPLES</span></span>

### <span data-ttu-id="c492b-111">範例1：移除網站資源</span><span class="sxs-lookup"><span data-stu-id="c492b-111">Example 1: Remove a website resource</span></span>
```
PS C:\>Remove-AzureRmResource -ResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup11/providers/Microsoft.Web/sites/ContosoSite" -Force
```

<span data-ttu-id="c492b-112">這個命令會移除名為 ContosoSite 的網站資源。</span><span class="sxs-lookup"><span data-stu-id="c492b-112">This command removes the website resource named ContosoSite.</span></span>
<span data-ttu-id="c492b-113">此範例會使用 [訂閱識別碼] 的預留位置值。</span><span class="sxs-lookup"><span data-stu-id="c492b-113">The example uses a placeholder value for the subscription ID.</span></span>
<span data-ttu-id="c492b-114">命令會指定 *Force* 參數。</span><span class="sxs-lookup"><span data-stu-id="c492b-114">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="c492b-115">因此，它不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c492b-115">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="c492b-116">參數</span><span class="sxs-lookup"><span data-stu-id="c492b-116">PARAMETERS</span></span>

### <span data-ttu-id="c492b-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="c492b-117">-ApiVersion</span></span>
<span data-ttu-id="c492b-118">指定要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="c492b-118">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="c492b-119">如果您沒有指定版本，此 Cmdlet 會使用最新的可用版本。</span><span class="sxs-lookup"><span data-stu-id="c492b-119">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="c492b-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c492b-120">-AsJob</span></span>
<span data-ttu-id="c492b-121">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c492b-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c492b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c492b-122">-DefaultProfile</span></span>
<span data-ttu-id="c492b-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="c492b-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c492b-124">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="c492b-124">-ExtensionResourceName</span></span>
<span data-ttu-id="c492b-125">指定此 Cmdlet 移除之資源之延伸資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="c492b-125">Specifies the name of an extension resource of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="c492b-126">例如，若要指定資料庫，請使用下列格式：伺服器名稱 `/` 資料庫名稱</span><span class="sxs-lookup"><span data-stu-id="c492b-126">For instance, to specify a database, use the following format: server name`/`database name</span></span>

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

### <span data-ttu-id="c492b-127">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="c492b-127">-ExtensionResourceType</span></span>
<span data-ttu-id="c492b-128">指定延伸資源的資源類型。</span><span class="sxs-lookup"><span data-stu-id="c492b-128">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="c492b-129">指定資源的延伸資源類型。</span><span class="sxs-lookup"><span data-stu-id="c492b-129">Specifies the extension resource type for the resource.</span></span>
<span data-ttu-id="c492b-130">例如： `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="c492b-130">For instance: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="c492b-131">-Force</span><span class="sxs-lookup"><span data-stu-id="c492b-131">-Force</span></span>
<span data-ttu-id="c492b-132">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="c492b-132">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c492b-133">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="c492b-133">-ODataQuery</span></span>
<span data-ttu-id="c492b-134">指定 (OData) 樣式篩選的開放式資料通訊協定。</span><span class="sxs-lookup"><span data-stu-id="c492b-134">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="c492b-135">除了任何其他篩選器之外，此 Cmdlet 還會將此值附加到要求中。</span><span class="sxs-lookup"><span data-stu-id="c492b-135">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="c492b-136">-預先</span><span class="sxs-lookup"><span data-stu-id="c492b-136">-Pre</span></span>
<span data-ttu-id="c492b-137">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="c492b-137">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="c492b-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c492b-138">-ResourceGroupName</span></span>
<span data-ttu-id="c492b-139">指定此 Cmdlet 從中移除資源的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c492b-139">Specifies the name of the resource group from which this cmdlet removes a resource.</span></span>

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

### <span data-ttu-id="c492b-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c492b-140">-ResourceId</span></span>
<span data-ttu-id="c492b-141">指定此 Cmdlet 移除之資源的完整限定資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="c492b-141">Specifies the fully qualified resource ID of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="c492b-142">識別碼包含訂閱，如下列範例所示： `/subscriptions/` 訂閱識別碼`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="c492b-142">The ID includes the subscription, as in the following example: `/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="c492b-143">-CoNtext.resourcename</span><span class="sxs-lookup"><span data-stu-id="c492b-143">-ResourceName</span></span>
<span data-ttu-id="c492b-144">指定此 Cmdlet 移除之資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="c492b-144">Specifies the name of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="c492b-145">例如，若要指定資料庫，請使用下列格式： `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="c492b-145">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="c492b-146">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="c492b-146">-ResourceType</span></span>
<span data-ttu-id="c492b-147">指定此 Cmdlet 移除的資源類型。</span><span class="sxs-lookup"><span data-stu-id="c492b-147">Specifies the type of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="c492b-148">舉例來說，對於資料庫而言，資源類型如下所示： `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="c492b-148">For instance, for a database, the resource type is as follows: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="c492b-149">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="c492b-149">-TenantLevel</span></span>
<span data-ttu-id="c492b-150">表示此 Cmdlet 在租使用者層級運作。</span><span class="sxs-lookup"><span data-stu-id="c492b-150">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="c492b-151">-確認</span><span class="sxs-lookup"><span data-stu-id="c492b-151">-Confirm</span></span>
<span data-ttu-id="c492b-152">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c492b-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c492b-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c492b-153">-WhatIf</span></span>
<span data-ttu-id="c492b-154">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c492b-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c492b-155">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c492b-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c492b-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c492b-156">CommonParameters</span></span>
<span data-ttu-id="c492b-157">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c492b-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c492b-158">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c492b-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c492b-159">輸入</span><span class="sxs-lookup"><span data-stu-id="c492b-159">INPUTS</span></span>

### <span data-ttu-id="c492b-160">所有</span><span class="sxs-lookup"><span data-stu-id="c492b-160">None</span></span>

## <span data-ttu-id="c492b-161">輸出</span><span class="sxs-lookup"><span data-stu-id="c492b-161">OUTPUTS</span></span>

### <span data-ttu-id="c492b-162">System.object</span><span class="sxs-lookup"><span data-stu-id="c492b-162">System.Boolean</span></span>

## <span data-ttu-id="c492b-163">筆記</span><span class="sxs-lookup"><span data-stu-id="c492b-163">NOTES</span></span>

## <span data-ttu-id="c492b-164">相關連結</span><span class="sxs-lookup"><span data-stu-id="c492b-164">RELATED LINKS</span></span>

[<span data-ttu-id="c492b-165">尋找-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="c492b-165">Find-AzureRmResource</span></span>](./Find-AzureRmResource.md)

[<span data-ttu-id="c492b-166">AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="c492b-166">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="c492b-167">移動流覽 AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="c492b-167">Move-AzureRmResource</span></span>](./Move-AzureRmResource.md)

[<span data-ttu-id="c492b-168">新-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="c492b-168">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="c492b-169">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="c492b-169">Set-AzureRmResource</span></span>](./Set-AzureRmResource.md)


