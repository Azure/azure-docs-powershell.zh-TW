---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: A262DFD1-8B90-462C-A4E2-ABA0F51173FA
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResource.md
ms.openlocfilehash: ef81674d75ee2f5f79988875e70764df91d23d2c
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/08/2020
ms.locfileid: "93802666"
---
# <span data-ttu-id="5c06d-101">Remove-AzResource</span><span class="sxs-lookup"><span data-stu-id="5c06d-101">Remove-AzResource</span></span>

## <span data-ttu-id="5c06d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5c06d-102">SYNOPSIS</span></span>
<span data-ttu-id="5c06d-103">移除資源。</span><span class="sxs-lookup"><span data-stu-id="5c06d-103">Removes a resource.</span></span>

## <span data-ttu-id="5c06d-104">句法</span><span class="sxs-lookup"><span data-stu-id="5c06d-104">SYNTAX</span></span>

### <span data-ttu-id="5c06d-105">ByResourceId (預設) </span><span class="sxs-lookup"><span data-stu-id="5c06d-105">ByResourceId (Default)</span></span>
```
Remove-AzResource [-AsJob] -ResourceId <String> [-ODataQuery <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c06d-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="5c06d-106">BySubscriptionLevel</span></span>
```
Remove-AzResource [-AsJob] -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ODataQuery <String>] [-ResourceGroupName <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5c06d-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="5c06d-107">ByTenantLevel</span></span>
```
Remove-AzResource [-AsJob] -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5c06d-108">說明</span><span class="sxs-lookup"><span data-stu-id="5c06d-108">DESCRIPTION</span></span>
<span data-ttu-id="5c06d-109">**AzResource** Cmdlet 會移除 Azure 資源。</span><span class="sxs-lookup"><span data-stu-id="5c06d-109">The **Remove-AzResource** cmdlet removes an Azure resource.</span></span>

## <span data-ttu-id="5c06d-110">示例</span><span class="sxs-lookup"><span data-stu-id="5c06d-110">EXAMPLES</span></span>

### <span data-ttu-id="5c06d-111">範例1：移除網站資源</span><span class="sxs-lookup"><span data-stu-id="5c06d-111">Example 1: Remove a website resource</span></span>
```
PS C:\>Remove-AzResource -ResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup11/providers/Microsoft.Web/sites/ContosoSite" -Force
```

<span data-ttu-id="5c06d-112">這個命令會移除名為 ContosoSite 的網站資源。</span><span class="sxs-lookup"><span data-stu-id="5c06d-112">This command removes the website resource named ContosoSite.</span></span>
<span data-ttu-id="5c06d-113">此範例會使用 [訂閱識別碼] 的預留位置值。</span><span class="sxs-lookup"><span data-stu-id="5c06d-113">The example uses a placeholder value for the subscription ID.</span></span>
<span data-ttu-id="5c06d-114">命令會指定 *Force* 參數。</span><span class="sxs-lookup"><span data-stu-id="5c06d-114">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="5c06d-115">因此，它不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5c06d-115">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="5c06d-116">參數</span><span class="sxs-lookup"><span data-stu-id="5c06d-116">PARAMETERS</span></span>

### <span data-ttu-id="5c06d-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="5c06d-117">-ApiVersion</span></span>
<span data-ttu-id="5c06d-118">指定要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="5c06d-118">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="5c06d-119">如果您沒有指定版本，此 Cmdlet 會使用最新的可用版本。</span><span class="sxs-lookup"><span data-stu-id="5c06d-119">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="5c06d-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5c06d-120">-AsJob</span></span>
<span data-ttu-id="5c06d-121">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5c06d-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5c06d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c06d-122">-DefaultProfile</span></span>
<span data-ttu-id="5c06d-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="5c06d-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5c06d-124">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="5c06d-124">-ExtensionResourceName</span></span>
<span data-ttu-id="5c06d-125">指定此 Cmdlet 移除之資源之延伸資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="5c06d-125">Specifies the name of an extension resource of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="5c06d-126">例如，若要指定資料庫，請使用下列格式：伺服器名稱 `/` 資料庫名稱</span><span class="sxs-lookup"><span data-stu-id="5c06d-126">For instance, to specify a database, use the following format: server name`/`database name</span></span>

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

### <span data-ttu-id="5c06d-127">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="5c06d-127">-ExtensionResourceType</span></span>
<span data-ttu-id="5c06d-128">指定延伸資源的資源類型。</span><span class="sxs-lookup"><span data-stu-id="5c06d-128">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="5c06d-129">指定資源的延伸資源類型。</span><span class="sxs-lookup"><span data-stu-id="5c06d-129">Specifies the extension resource type for the resource.</span></span>
<span data-ttu-id="5c06d-130">例如： `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="5c06d-130">For instance: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="5c06d-131">-Force</span><span class="sxs-lookup"><span data-stu-id="5c06d-131">-Force</span></span>
<span data-ttu-id="5c06d-132">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="5c06d-132">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5c06d-133">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="5c06d-133">-ODataQuery</span></span>
<span data-ttu-id="5c06d-134">指定 (OData) 樣式篩選的開放式資料通訊協定。</span><span class="sxs-lookup"><span data-stu-id="5c06d-134">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="5c06d-135">除了任何其他篩選器之外，此 Cmdlet 還會將此值附加到要求中。</span><span class="sxs-lookup"><span data-stu-id="5c06d-135">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="5c06d-136">-預先</span><span class="sxs-lookup"><span data-stu-id="5c06d-136">-Pre</span></span>
<span data-ttu-id="5c06d-137">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="5c06d-137">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="5c06d-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c06d-138">-ResourceGroupName</span></span>
<span data-ttu-id="5c06d-139">指定此 Cmdlet 從中移除資源的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5c06d-139">Specifies the name of the resource group from which this cmdlet removes a resource.</span></span>

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

### <span data-ttu-id="5c06d-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5c06d-140">-ResourceId</span></span>
<span data-ttu-id="5c06d-141">指定此 Cmdlet 移除之資源的完整限定資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="5c06d-141">Specifies the fully qualified resource ID of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="5c06d-142">識別碼包含訂閱，如下列範例所示： `/subscriptions/` 訂閱識別碼`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="5c06d-142">The ID includes the subscription, as in the following example: `/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="5c06d-143">-CoNtext.resourcename</span><span class="sxs-lookup"><span data-stu-id="5c06d-143">-ResourceName</span></span>
<span data-ttu-id="5c06d-144">指定此 Cmdlet 移除之資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="5c06d-144">Specifies the name of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="5c06d-145">例如，若要指定資料庫，請使用下列格式： `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="5c06d-145">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="5c06d-146">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="5c06d-146">-ResourceType</span></span>
<span data-ttu-id="5c06d-147">指定此 Cmdlet 移除的資源類型。</span><span class="sxs-lookup"><span data-stu-id="5c06d-147">Specifies the type of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="5c06d-148">舉例來說，對於資料庫而言，資源類型如下所示： `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="5c06d-148">For instance, for a database, the resource type is as follows: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="5c06d-149">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="5c06d-149">-TenantLevel</span></span>
<span data-ttu-id="5c06d-150">表示此 Cmdlet 在租使用者層級運作。</span><span class="sxs-lookup"><span data-stu-id="5c06d-150">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="5c06d-151">-確認</span><span class="sxs-lookup"><span data-stu-id="5c06d-151">-Confirm</span></span>
<span data-ttu-id="5c06d-152">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5c06d-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c06d-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c06d-153">-WhatIf</span></span>
<span data-ttu-id="5c06d-154">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5c06d-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5c06d-155">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5c06d-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c06d-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c06d-156">CommonParameters</span></span>
<span data-ttu-id="5c06d-157">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5c06d-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c06d-158">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5c06d-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c06d-159">輸入</span><span class="sxs-lookup"><span data-stu-id="5c06d-159">INPUTS</span></span>

### <span data-ttu-id="5c06d-160">System.object</span><span class="sxs-lookup"><span data-stu-id="5c06d-160">System.String</span></span>

## <span data-ttu-id="5c06d-161">輸出</span><span class="sxs-lookup"><span data-stu-id="5c06d-161">OUTPUTS</span></span>

### <span data-ttu-id="5c06d-162">System.object</span><span class="sxs-lookup"><span data-stu-id="5c06d-162">System.Boolean</span></span>

## <span data-ttu-id="5c06d-163">筆記</span><span class="sxs-lookup"><span data-stu-id="5c06d-163">NOTES</span></span>

## <span data-ttu-id="5c06d-164">相關連結</span><span class="sxs-lookup"><span data-stu-id="5c06d-164">RELATED LINKS</span></span>

[<span data-ttu-id="5c06d-165">AzResource</span><span class="sxs-lookup"><span data-stu-id="5c06d-165">Get-AzResource</span></span>](./Get-AzResource.md)

[<span data-ttu-id="5c06d-166">移動流覽 AzResource</span><span class="sxs-lookup"><span data-stu-id="5c06d-166">Move-AzResource</span></span>](./Move-AzResource.md)

[<span data-ttu-id="5c06d-167">新-AzResource</span><span class="sxs-lookup"><span data-stu-id="5c06d-167">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="5c06d-168">Set-AzResource</span><span class="sxs-lookup"><span data-stu-id="5c06d-168">Set-AzResource</span></span>](./Set-AzResource.md)


