---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 427F7300-0FEB-4F28-9C1D-27592AEBF6A0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/invoke-azurermresourceaction
schema: 2.0.0
ms.openlocfilehash: e29dda3fc5d2b62196d0cc5897ba7a7c9b047a8c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93801565"
---
# <span data-ttu-id="18911-101">Invoke-AzureRmResourceAction</span><span class="sxs-lookup"><span data-stu-id="18911-101">Invoke-AzureRmResourceAction</span></span>

## <span data-ttu-id="18911-102">摘要</span><span class="sxs-lookup"><span data-stu-id="18911-102">SYNOPSIS</span></span>
<span data-ttu-id="18911-103">在資源上調用動作。</span><span class="sxs-lookup"><span data-stu-id="18911-103">Invokes an action on a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="18911-104">句法</span><span class="sxs-lookup"><span data-stu-id="18911-104">SYNTAX</span></span>

### <span data-ttu-id="18911-105">ByResourceId (預設) </span><span class="sxs-lookup"><span data-stu-id="18911-105">ByResourceId (Default)</span></span>
```
Invoke-AzureRmResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceId <String>
 [-ODataQuery <String>] [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="18911-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="18911-106">BySubscriptionLevel</span></span>
```
Invoke-AzureRmResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceName <String>
 -ResourceType <String> [-ExtensionResourceName <String>] [-ExtensionResourceType <String>]
 [-ODataQuery <String>] [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18911-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="18911-107">ByTenantLevel</span></span>
```
Invoke-AzureRmResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceName <String>
 -ResourceType <String> [-ExtensionResourceName <String>] [-ExtensionResourceType <String>]
 [-ODataQuery <String>] [-TenantLevel] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="18911-108">說明</span><span class="sxs-lookup"><span data-stu-id="18911-108">DESCRIPTION</span></span>
<span data-ttu-id="18911-109">**AzureRmResourceAction** Cmdlet 會在指定的 Azure 資源上調用動作。</span><span class="sxs-lookup"><span data-stu-id="18911-109">The **Invoke-AzureRmResourceAction** cmdlet invokes an action on a specified Azure resource.</span></span>
<span data-ttu-id="18911-110">若要取得支援的動作清單，請使用 Azure 資源管理器工具。</span><span class="sxs-lookup"><span data-stu-id="18911-110">To get a list of supported actions, use the Azure Resource Explorer tool.</span></span>

## <span data-ttu-id="18911-111">示例</span><span class="sxs-lookup"><span data-stu-id="18911-111">EXAMPLES</span></span>

## <span data-ttu-id="18911-112">參數</span><span class="sxs-lookup"><span data-stu-id="18911-112">PARAMETERS</span></span>

### <span data-ttu-id="18911-113">-動作</span><span class="sxs-lookup"><span data-stu-id="18911-113">-Action</span></span>
<span data-ttu-id="18911-114">指定要呼叫之動作的名稱。</span><span class="sxs-lookup"><span data-stu-id="18911-114">Specifies the name of the action to invoke.</span></span>

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

### <span data-ttu-id="18911-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="18911-115">-ApiVersion</span></span>
<span data-ttu-id="18911-116">指定要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="18911-116">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="18911-117">如果您沒有指定版本，此 Cmdlet 會使用最新的可用版本。</span><span class="sxs-lookup"><span data-stu-id="18911-117">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="18911-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18911-118">-DefaultProfile</span></span>
<span data-ttu-id="18911-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="18911-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="18911-120">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="18911-120">-ExtensionResourceName</span></span>
<span data-ttu-id="18911-121">指定此 Cmdlet 在其上執行動作之資源之延伸資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="18911-121">Specifies the name of an extension resource for the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="18911-122">例如，若要指定資料庫，請使用下列格式：伺服器名稱 `/` 資料庫名稱</span><span class="sxs-lookup"><span data-stu-id="18911-122">For instance, to specify a database, use the following format: server name`/`database name</span></span>

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

### <span data-ttu-id="18911-123">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="18911-123">-ExtensionResourceType</span></span>
<span data-ttu-id="18911-124">指定延伸資源的類型。</span><span class="sxs-lookup"><span data-stu-id="18911-124">Specifies the type of the extension resource.</span></span>
<span data-ttu-id="18911-125">例如： `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="18911-125">For instance: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="18911-126">-Force</span><span class="sxs-lookup"><span data-stu-id="18911-126">-Force</span></span>
<span data-ttu-id="18911-127">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="18911-127">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="18911-128">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="18911-128">-InformationAction</span></span>
<span data-ttu-id="18911-129">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="18911-129">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="18911-130">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="18911-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="18911-131">持續</span><span class="sxs-lookup"><span data-stu-id="18911-131">Continue</span></span>
- <span data-ttu-id="18911-132">理會</span><span class="sxs-lookup"><span data-stu-id="18911-132">Ignore</span></span>
- <span data-ttu-id="18911-133">看</span><span class="sxs-lookup"><span data-stu-id="18911-133">Inquire</span></span>
- <span data-ttu-id="18911-134">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="18911-134">SilentlyContinue</span></span>
- <span data-ttu-id="18911-135">停止</span><span class="sxs-lookup"><span data-stu-id="18911-135">Stop</span></span>
- <span data-ttu-id="18911-136">封存</span><span class="sxs-lookup"><span data-stu-id="18911-136">Suspend</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18911-137">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="18911-137">-InformationVariable</span></span>
<span data-ttu-id="18911-138">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="18911-138">Specifies an information variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18911-139">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="18911-139">-ODataQuery</span></span>
<span data-ttu-id="18911-140">指定 (OData) 樣式篩選的開放式資料通訊協定。</span><span class="sxs-lookup"><span data-stu-id="18911-140">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="18911-141">除了任何其他篩選器之外，此 Cmdlet 還會將此值附加到要求中。</span><span class="sxs-lookup"><span data-stu-id="18911-141">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="18911-142">-參數</span><span class="sxs-lookup"><span data-stu-id="18911-142">-Parameters</span></span>
<span data-ttu-id="18911-143">針對此 Cmdlet 調用的動作指定參數（作為雜湊資料表）。</span><span class="sxs-lookup"><span data-stu-id="18911-143">Specifies parameters, as a hash table, for the action that this cmdlet invokes.</span></span>

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

### <span data-ttu-id="18911-144">-預先</span><span class="sxs-lookup"><span data-stu-id="18911-144">-Pre</span></span>
<span data-ttu-id="18911-145">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="18911-145">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="18911-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18911-146">-ResourceGroupName</span></span>
<span data-ttu-id="18911-147">指定此 Cmdlet 在其中調用動作的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="18911-147">Specifies the name of a resource group in which this cmdlet invokes an action.</span></span>

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

### <span data-ttu-id="18911-148">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="18911-148">-ResourceId</span></span>
<span data-ttu-id="18911-149">指定此 Cmdlet 調用動作之資源的完整限定資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="18911-149">Specifies the fully qualified resource ID of the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="18911-150">識別碼包含訂閱，如下列範例所示： `/subscriptions/` 訂閱識別碼`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="18911-150">The ID includes the subscription, as in the following example: `/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="18911-151">-CoNtext.resourcename</span><span class="sxs-lookup"><span data-stu-id="18911-151">-ResourceName</span></span>
<span data-ttu-id="18911-152">指定此 Cmdlet 在其上執行動作之資源資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="18911-152">Specifies the name of the resource of the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="18911-153">例如，若要指定資料庫，請使用下列格式： `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="18911-153">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="18911-154">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="18911-154">-ResourceType</span></span>
<span data-ttu-id="18911-155">指定資源的類型。</span><span class="sxs-lookup"><span data-stu-id="18911-155">Specifies the type of the resource.</span></span>
<span data-ttu-id="18911-156">舉例來說，對於資料庫而言，資源類型如下所示： `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="18911-156">For instance, for a database, the resource type is as follows: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="18911-157">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="18911-157">-TenantLevel</span></span>
<span data-ttu-id="18911-158">表示此 Cmdlet 在租使用者層級運作。</span><span class="sxs-lookup"><span data-stu-id="18911-158">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="18911-159">-確認</span><span class="sxs-lookup"><span data-stu-id="18911-159">-Confirm</span></span>
<span data-ttu-id="18911-160">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="18911-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18911-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18911-161">-WhatIf</span></span>
<span data-ttu-id="18911-162">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="18911-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="18911-163">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="18911-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="18911-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18911-164">CommonParameters</span></span>
<span data-ttu-id="18911-165">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="18911-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18911-166">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="18911-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18911-167">輸入</span><span class="sxs-lookup"><span data-stu-id="18911-167">INPUTS</span></span>

## <span data-ttu-id="18911-168">輸出</span><span class="sxs-lookup"><span data-stu-id="18911-168">OUTPUTS</span></span>

## <span data-ttu-id="18911-169">筆記</span><span class="sxs-lookup"><span data-stu-id="18911-169">NOTES</span></span>

## <span data-ttu-id="18911-170">相關連結</span><span class="sxs-lookup"><span data-stu-id="18911-170">RELATED LINKS</span></span>
