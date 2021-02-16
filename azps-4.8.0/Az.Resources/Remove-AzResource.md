---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: A262DFD1-8B90-462C-A4E2-ABA0F51173FA
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResource.md
ms.openlocfilehash: 9e8eea48238bd177f3a8556691db48686a57dd99
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100414861"
---
# <span data-ttu-id="b3d3c-101">Remove-AzResource</span><span class="sxs-lookup"><span data-stu-id="b3d3c-101">Remove-AzResource</span></span>

## <span data-ttu-id="b3d3c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b3d3c-102">SYNOPSIS</span></span>
<span data-ttu-id="b3d3c-103">移除資源。</span><span class="sxs-lookup"><span data-stu-id="b3d3c-103">Removes a resource.</span></span>

## <span data-ttu-id="b3d3c-104">語法</span><span class="sxs-lookup"><span data-stu-id="b3d3c-104">SYNTAX</span></span>

### <span data-ttu-id="b3d3c-105">ByResourceId (預設) </span><span class="sxs-lookup"><span data-stu-id="b3d3c-105">ByResourceId (Default)</span></span>
```
Remove-AzResource [-AsJob] -ResourceId <String> [-ODataQuery <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3d3c-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="b3d3c-106">BySubscriptionLevel</span></span>
```
Remove-AzResource [-AsJob] -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ODataQuery <String>] [-ResourceGroupName <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b3d3c-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="b3d3c-107">ByTenantLevel</span></span>
```
Remove-AzResource [-AsJob] -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3d3c-108">描述</span><span class="sxs-lookup"><span data-stu-id="b3d3c-108">DESCRIPTION</span></span>
<span data-ttu-id="b3d3c-109">**Remove-AzResource** Cmdlet 會移除 Azure 資源。</span><span class="sxs-lookup"><span data-stu-id="b3d3c-109">The **Remove-AzResource** cmdlet removes an Azure resource.</span></span>

## <span data-ttu-id="b3d3c-110">例子</span><span class="sxs-lookup"><span data-stu-id="b3d3c-110">EXAMPLES</span></span>

### <span data-ttu-id="b3d3c-111">範例 1：移除網站資源</span><span class="sxs-lookup"><span data-stu-id="b3d3c-111">Example 1: Remove a website resource</span></span>
```
PS C:\>Remove-AzResource -ResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup11/providers/Microsoft.Web/sites/ContosoSite" -Force
```

<span data-ttu-id="b3d3c-112">此命令會移除名為 ContosoSite 的網站資源。</span><span class="sxs-lookup"><span data-stu-id="b3d3c-112">This command removes the website resource named ContosoSite.</span></span>
<span data-ttu-id="b3d3c-113">此範例使用訂閱識別碼的預留位置值。</span><span class="sxs-lookup"><span data-stu-id="b3d3c-113">The example uses a placeholder value for the subscription ID.</span></span>
<span data-ttu-id="b3d3c-114">命令會指定 *Force* 參數。</span><span class="sxs-lookup"><span data-stu-id="b3d3c-114">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="b3d3c-115">因此，它不會提示您確認。</span><span class="sxs-lookup"><span data-stu-id="b3d3c-115">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="b3d3c-116">參數</span><span class="sxs-lookup"><span data-stu-id="b3d3c-116">PARAMETERS</span></span>

### <span data-ttu-id="b3d3c-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="b3d3c-117">-ApiVersion</span></span>
<span data-ttu-id="b3d3c-118">指定要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="b3d3c-118">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="b3d3c-119">如果您未指定版本，此 Cmdlet 會使用最新的可用版本。</span><span class="sxs-lookup"><span data-stu-id="b3d3c-119">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="b3d3c-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b3d3c-120">-AsJob</span></span>
<span data-ttu-id="b3d3c-121">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b3d3c-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b3d3c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3d3c-122">-DefaultProfile</span></span>
<span data-ttu-id="b3d3c-123">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="b3d3c-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b3d3c-124">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="b3d3c-124">-ExtensionResourceName</span></span>
<span data-ttu-id="b3d3c-125">指定此 Cmdlet 移除之資源的延伸資源名稱。</span><span class="sxs-lookup"><span data-stu-id="b3d3c-125">Specifies the name of an extension resource of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="b3d3c-126">例如，若要指定資料庫，請使用下列格式：伺服器名稱 `/` 資料庫名稱</span><span class="sxs-lookup"><span data-stu-id="b3d3c-126">For instance, to specify a database, use the following format: server name`/`database name</span></span>

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

### <span data-ttu-id="b3d3c-127">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="b3d3c-127">-ExtensionResourceType</span></span>
<span data-ttu-id="b3d3c-128">指定擴充資源的資源類型。</span><span class="sxs-lookup"><span data-stu-id="b3d3c-128">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="b3d3c-129">指定資源的擴充資源類型。</span><span class="sxs-lookup"><span data-stu-id="b3d3c-129">Specifies the extension resource type for the resource.</span></span>
<span data-ttu-id="b3d3c-130">例如： `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="b3d3c-130">For instance: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="b3d3c-131">-強制</span><span class="sxs-lookup"><span data-stu-id="b3d3c-131">-Force</span></span>
<span data-ttu-id="b3d3c-132">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="b3d3c-132">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b3d3c-133">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="b3d3c-133">-ODataQuery</span></span>
<span data-ttu-id="b3d3c-134">指定開啟資料通訊協定 (OData) 樣式篩選。</span><span class="sxs-lookup"><span data-stu-id="b3d3c-134">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="b3d3c-135">除了任何其他篩選之外，此 Cmdlet 會附加此值至要求。</span><span class="sxs-lookup"><span data-stu-id="b3d3c-135">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="b3d3c-136">-Pre</span><span class="sxs-lookup"><span data-stu-id="b3d3c-136">-Pre</span></span>
<span data-ttu-id="b3d3c-137">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮測試版 API 版本。</span><span class="sxs-lookup"><span data-stu-id="b3d3c-137">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="b3d3c-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3d3c-138">-ResourceGroupName</span></span>
<span data-ttu-id="b3d3c-139">指定此 Cmdlet 從其中移除資源的資源組名。</span><span class="sxs-lookup"><span data-stu-id="b3d3c-139">Specifies the name of the resource group from which this cmdlet removes a resource.</span></span>

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

### <span data-ttu-id="b3d3c-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b3d3c-140">-ResourceId</span></span>
<span data-ttu-id="b3d3c-141">指定此 Cmdlet 移除之資源之完整資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="b3d3c-141">Specifies the fully qualified resource ID of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="b3d3c-142">識別碼包含訂閱，如下列範例所示： `/subscriptions/` 訂閱識別碼`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="b3d3c-142">The ID includes the subscription, as in the following example: `/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="b3d3c-143">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="b3d3c-143">-ResourceName</span></span>
<span data-ttu-id="b3d3c-144">指定此 Cmdlet 移除的資源名稱。</span><span class="sxs-lookup"><span data-stu-id="b3d3c-144">Specifies the name of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="b3d3c-145">例如，若要指定資料庫，請使用下列格式： `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="b3d3c-145">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="b3d3c-146">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="b3d3c-146">-ResourceType</span></span>
<span data-ttu-id="b3d3c-147">指定此 Cmdlet 移除的資源類型。</span><span class="sxs-lookup"><span data-stu-id="b3d3c-147">Specifies the type of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="b3d3c-148">例如，對於資料庫，資源類型如下所示： `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="b3d3c-148">For instance, for a database, the resource type is as follows: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="b3d3c-149">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="b3d3c-149">-TenantLevel</span></span>
<span data-ttu-id="b3d3c-150">表示此 Cmdlet 在租使用者層級運作。</span><span class="sxs-lookup"><span data-stu-id="b3d3c-150">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="b3d3c-151">-確認</span><span class="sxs-lookup"><span data-stu-id="b3d3c-151">-Confirm</span></span>
<span data-ttu-id="b3d3c-152">執行 Cmdlet 之前，系統會提示您確認。</span><span class="sxs-lookup"><span data-stu-id="b3d3c-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3d3c-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3d3c-153">-WhatIf</span></span>
<span data-ttu-id="b3d3c-154">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b3d3c-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3d3c-155">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b3d3c-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3d3c-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3d3c-156">CommonParameters</span></span>
<span data-ttu-id="b3d3c-157">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b3d3c-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3d3c-158">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b3d3c-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3d3c-159">輸入</span><span class="sxs-lookup"><span data-stu-id="b3d3c-159">INPUTS</span></span>

### <span data-ttu-id="b3d3c-160">System.String</span><span class="sxs-lookup"><span data-stu-id="b3d3c-160">System.String</span></span>

## <span data-ttu-id="b3d3c-161">輸出</span><span class="sxs-lookup"><span data-stu-id="b3d3c-161">OUTPUTS</span></span>

### <span data-ttu-id="b3d3c-162">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b3d3c-162">System.Boolean</span></span>

## <span data-ttu-id="b3d3c-163">筆記</span><span class="sxs-lookup"><span data-stu-id="b3d3c-163">NOTES</span></span>

## <span data-ttu-id="b3d3c-164">相關連結</span><span class="sxs-lookup"><span data-stu-id="b3d3c-164">RELATED LINKS</span></span>


[<span data-ttu-id="b3d3c-165">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="b3d3c-165">Get-AzResource</span></span>](./Get-AzResource.md)

[<span data-ttu-id="b3d3c-166">Move-AzResource</span><span class="sxs-lookup"><span data-stu-id="b3d3c-166">Move-AzResource</span></span>](./Move-AzResource.md)

[<span data-ttu-id="b3d3c-167">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="b3d3c-167">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="b3d3c-168">Set-AzResource</span><span class="sxs-lookup"><span data-stu-id="b3d3c-168">Set-AzResource</span></span>](./Set-AzResource.md)


