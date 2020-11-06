---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 427F7300-0FEB-4F28-9C1D-27592AEBF6A0
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/invoke-azresourceaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Invoke-AzResourceAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Invoke-AzResourceAction.md
ms.openlocfilehash: 9a971618c205380a4ca2b049563fc8ee4542e681
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93620855"
---
# <span data-ttu-id="c5fd3-101">Invoke-AzResourceAction</span><span class="sxs-lookup"><span data-stu-id="c5fd3-101">Invoke-AzResourceAction</span></span>

## <span data-ttu-id="c5fd3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c5fd3-102">SYNOPSIS</span></span>
<span data-ttu-id="c5fd3-103">在資源上調用動作。</span><span class="sxs-lookup"><span data-stu-id="c5fd3-103">Invokes an action on a resource.</span></span>

## <span data-ttu-id="c5fd3-104">句法</span><span class="sxs-lookup"><span data-stu-id="c5fd3-104">SYNTAX</span></span>

### <span data-ttu-id="c5fd3-105">ByResourceId (預設) </span><span class="sxs-lookup"><span data-stu-id="c5fd3-105">ByResourceId (Default)</span></span>
```
Invoke-AzResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceId <String> [-ODataQuery <String>]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c5fd3-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="c5fd3-106">BySubscriptionLevel</span></span>
```
Invoke-AzResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceName <String>
 -ResourceType <String> [-ExtensionResourceName <String>] [-ExtensionResourceType <String>]
 [-ODataQuery <String>] [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5fd3-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="c5fd3-107">ByTenantLevel</span></span>
```
Invoke-AzResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceName <String>
 -ResourceType <String> [-ExtensionResourceName <String>] [-ExtensionResourceType <String>]
 [-ODataQuery <String>] [-TenantLevel] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c5fd3-108">說明</span><span class="sxs-lookup"><span data-stu-id="c5fd3-108">DESCRIPTION</span></span>
<span data-ttu-id="c5fd3-109">**AzResourceAction** Cmdlet 會在指定的 Azure 資源上調用動作。</span><span class="sxs-lookup"><span data-stu-id="c5fd3-109">The **Invoke-AzResourceAction** cmdlet invokes an action on a specified Azure resource.</span></span>
<span data-ttu-id="c5fd3-110">若要取得支援的動作清單，請使用 Azure 資源管理器工具。</span><span class="sxs-lookup"><span data-stu-id="c5fd3-110">To get a list of supported actions, use the Azure Resource Explorer tool.</span></span>

## <span data-ttu-id="c5fd3-111">示例</span><span class="sxs-lookup"><span data-stu-id="c5fd3-111">EXAMPLES</span></span>

## <span data-ttu-id="c5fd3-112">參數</span><span class="sxs-lookup"><span data-stu-id="c5fd3-112">PARAMETERS</span></span>

### <span data-ttu-id="c5fd3-113">-動作</span><span class="sxs-lookup"><span data-stu-id="c5fd3-113">-Action</span></span>
<span data-ttu-id="c5fd3-114">指定要呼叫之動作的名稱。</span><span class="sxs-lookup"><span data-stu-id="c5fd3-114">Specifies the name of the action to invoke.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ActionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5fd3-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="c5fd3-115">-ApiVersion</span></span>
<span data-ttu-id="c5fd3-116">指定要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="c5fd3-116">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="c5fd3-117">如果您沒有指定版本，此 Cmdlet 會使用最新的可用版本。</span><span class="sxs-lookup"><span data-stu-id="c5fd3-117">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="c5fd3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5fd3-118">-DefaultProfile</span></span>
<span data-ttu-id="c5fd3-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="c5fd3-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c5fd3-120">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="c5fd3-120">-ExtensionResourceName</span></span>
<span data-ttu-id="c5fd3-121">指定此 Cmdlet 在其上執行動作之資源之延伸資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="c5fd3-121">Specifies the name of an extension resource for the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="c5fd3-122">例如，若要指定資料庫，請使用下列格式：伺服器名稱 `/` 資料庫名稱</span><span class="sxs-lookup"><span data-stu-id="c5fd3-122">For instance, to specify a database, use the following format: server name`/`database name</span></span>

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

### <span data-ttu-id="c5fd3-123">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="c5fd3-123">-ExtensionResourceType</span></span>
<span data-ttu-id="c5fd3-124">指定延伸資源的類型。</span><span class="sxs-lookup"><span data-stu-id="c5fd3-124">Specifies the type of the extension resource.</span></span>
<span data-ttu-id="c5fd3-125">例如： `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="c5fd3-125">For instance: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="c5fd3-126">-Force</span><span class="sxs-lookup"><span data-stu-id="c5fd3-126">-Force</span></span>
<span data-ttu-id="c5fd3-127">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="c5fd3-127">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c5fd3-128">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="c5fd3-128">-ODataQuery</span></span>
<span data-ttu-id="c5fd3-129">指定 (OData) 樣式篩選的開放式資料通訊協定。</span><span class="sxs-lookup"><span data-stu-id="c5fd3-129">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="c5fd3-130">除了任何其他篩選器之外，此 Cmdlet 還會將此值附加到要求中。</span><span class="sxs-lookup"><span data-stu-id="c5fd3-130">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="c5fd3-131">-參數</span><span class="sxs-lookup"><span data-stu-id="c5fd3-131">-Parameters</span></span>
<span data-ttu-id="c5fd3-132">針對此 Cmdlet 調用的動作指定參數（作為雜湊資料表）。</span><span class="sxs-lookup"><span data-stu-id="c5fd3-132">Specifies parameters, as a hash table, for the action that this cmdlet invokes.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Object

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5fd3-133">-預先</span><span class="sxs-lookup"><span data-stu-id="c5fd3-133">-Pre</span></span>
<span data-ttu-id="c5fd3-134">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="c5fd3-134">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="c5fd3-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5fd3-135">-ResourceGroupName</span></span>
<span data-ttu-id="c5fd3-136">指定此 Cmdlet 在其中調用動作的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c5fd3-136">Specifies the name of a resource group in which this cmdlet invokes an action.</span></span>

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

### <span data-ttu-id="c5fd3-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c5fd3-137">-ResourceId</span></span>
<span data-ttu-id="c5fd3-138">指定此 Cmdlet 調用動作之資源的完整限定資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="c5fd3-138">Specifies the fully qualified resource ID of the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="c5fd3-139">識別碼包含訂閱，如下列範例所示： `/subscriptions/` 訂閱識別碼`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="c5fd3-139">The ID includes the subscription, as in the following example: `/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="c5fd3-140">-CoNtext.resourcename</span><span class="sxs-lookup"><span data-stu-id="c5fd3-140">-ResourceName</span></span>
<span data-ttu-id="c5fd3-141">指定此 Cmdlet 在其上執行動作之資源資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="c5fd3-141">Specifies the name of the resource of the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="c5fd3-142">例如，若要指定資料庫，請使用下列格式： `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="c5fd3-142">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="c5fd3-143">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="c5fd3-143">-ResourceType</span></span>
<span data-ttu-id="c5fd3-144">指定資源的類型。</span><span class="sxs-lookup"><span data-stu-id="c5fd3-144">Specifies the type of the resource.</span></span>
<span data-ttu-id="c5fd3-145">舉例來說，對於資料庫而言，資源類型如下所示： `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="c5fd3-145">For instance, for a database, the resource type is as follows: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="c5fd3-146">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="c5fd3-146">-TenantLevel</span></span>
<span data-ttu-id="c5fd3-147">表示此 Cmdlet 在租使用者層級運作。</span><span class="sxs-lookup"><span data-stu-id="c5fd3-147">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="c5fd3-148">-確認</span><span class="sxs-lookup"><span data-stu-id="c5fd3-148">-Confirm</span></span>
<span data-ttu-id="c5fd3-149">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c5fd3-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5fd3-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5fd3-150">-WhatIf</span></span>
<span data-ttu-id="c5fd3-151">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c5fd3-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c5fd3-152">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c5fd3-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5fd3-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5fd3-153">CommonParameters</span></span>
<span data-ttu-id="c5fd3-154">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c5fd3-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5fd3-155">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c5fd3-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5fd3-156">輸入</span><span class="sxs-lookup"><span data-stu-id="c5fd3-156">INPUTS</span></span>

### <span data-ttu-id="c5fd3-157">System.object</span><span class="sxs-lookup"><span data-stu-id="c5fd3-157">System.String</span></span>

## <span data-ttu-id="c5fd3-158">輸出</span><span class="sxs-lookup"><span data-stu-id="c5fd3-158">OUTPUTS</span></span>

### <span data-ttu-id="c5fd3-159">系統管理. PSObject</span><span class="sxs-lookup"><span data-stu-id="c5fd3-159">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="c5fd3-160">筆記</span><span class="sxs-lookup"><span data-stu-id="c5fd3-160">NOTES</span></span>

## <span data-ttu-id="c5fd3-161">相關連結</span><span class="sxs-lookup"><span data-stu-id="c5fd3-161">RELATED LINKS</span></span>