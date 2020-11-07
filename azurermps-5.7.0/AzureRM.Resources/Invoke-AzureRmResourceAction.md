---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 427F7300-0FEB-4F28-9C1D-27592AEBF6A0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/invoke-azurermresourceaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Invoke-AzureRmResourceAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Invoke-AzureRmResourceAction.md
ms.openlocfilehash: 7f2aa8299e3e4dcbdc6d326dfedf76092a65f351
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624679"
---
# <span data-ttu-id="687fb-101">Invoke-AzureRmResourceAction</span><span class="sxs-lookup"><span data-stu-id="687fb-101">Invoke-AzureRmResourceAction</span></span>

## <span data-ttu-id="687fb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="687fb-102">SYNOPSIS</span></span>
<span data-ttu-id="687fb-103">在資源上調用動作。</span><span class="sxs-lookup"><span data-stu-id="687fb-103">Invokes an action on a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="687fb-104">句法</span><span class="sxs-lookup"><span data-stu-id="687fb-104">SYNTAX</span></span>

### <span data-ttu-id="687fb-105">ByResourceId (預設) </span><span class="sxs-lookup"><span data-stu-id="687fb-105">ByResourceId (Default)</span></span>
```
Invoke-AzureRmResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceId <String>
 [-ODataQuery <String>] [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="687fb-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="687fb-106">BySubscriptionLevel</span></span>
```
Invoke-AzureRmResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceName <String>
 -ResourceType <String> [-ExtensionResourceName <String>] [-ExtensionResourceType <String>]
 [-ODataQuery <String>] [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="687fb-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="687fb-107">ByTenantLevel</span></span>
```
Invoke-AzureRmResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceName <String>
 -ResourceType <String> [-ExtensionResourceName <String>] [-ExtensionResourceType <String>]
 [-ODataQuery <String>] [-TenantLevel] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="687fb-108">說明</span><span class="sxs-lookup"><span data-stu-id="687fb-108">DESCRIPTION</span></span>
<span data-ttu-id="687fb-109">**AzureRmResourceAction** Cmdlet 會在指定的 Azure 資源上調用動作。</span><span class="sxs-lookup"><span data-stu-id="687fb-109">The **Invoke-AzureRmResourceAction** cmdlet invokes an action on a specified Azure resource.</span></span>

<span data-ttu-id="687fb-110">若要取得支援的動作清單，請使用 Azure 資源管理器工具。</span><span class="sxs-lookup"><span data-stu-id="687fb-110">To get a list of supported actions, use the Azure Resource Explorer tool.</span></span>

## <span data-ttu-id="687fb-111">示例</span><span class="sxs-lookup"><span data-stu-id="687fb-111">EXAMPLES</span></span>

## <span data-ttu-id="687fb-112">參數</span><span class="sxs-lookup"><span data-stu-id="687fb-112">PARAMETERS</span></span>

### <span data-ttu-id="687fb-113">-動作</span><span class="sxs-lookup"><span data-stu-id="687fb-113">-Action</span></span>
<span data-ttu-id="687fb-114">指定要呼叫之動作的名稱。</span><span class="sxs-lookup"><span data-stu-id="687fb-114">Specifies the name of the action to invoke.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ActionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="687fb-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="687fb-115">-ApiVersion</span></span>
<span data-ttu-id="687fb-116">指定要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="687fb-116">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="687fb-117">如果您沒有指定版本，此 Cmdlet 會使用最新的可用版本。</span><span class="sxs-lookup"><span data-stu-id="687fb-117">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="687fb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="687fb-118">-DefaultProfile</span></span>
<span data-ttu-id="687fb-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="687fb-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="687fb-120">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="687fb-120">-ExtensionResourceName</span></span>
<span data-ttu-id="687fb-121">指定此 Cmdlet 在其上執行動作之資源之延伸資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="687fb-121">Specifies the name of an extension resource for the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="687fb-122">例如，若要指定資料庫，請使用下列格式：</span><span class="sxs-lookup"><span data-stu-id="687fb-122">For instance, to specify a database, use the following format:</span></span> 

<span data-ttu-id="687fb-123">伺服器名稱 `/` 資料庫名稱</span><span class="sxs-lookup"><span data-stu-id="687fb-123">server name`/`database name</span></span>

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

### <span data-ttu-id="687fb-124">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="687fb-124">-ExtensionResourceType</span></span>
<span data-ttu-id="687fb-125">指定延伸資源的類型。</span><span class="sxs-lookup"><span data-stu-id="687fb-125">Specifies the type of the extension resource.</span></span>
<span data-ttu-id="687fb-126">例如：</span><span class="sxs-lookup"><span data-stu-id="687fb-126">For instance:</span></span> 

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

### <span data-ttu-id="687fb-127">-Force</span><span class="sxs-lookup"><span data-stu-id="687fb-127">-Force</span></span>
<span data-ttu-id="687fb-128">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="687fb-128">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="687fb-129">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="687fb-129">-InformationAction</span></span>
<span data-ttu-id="687fb-130">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="687fb-130">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="687fb-131">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="687fb-131">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="687fb-132">持續</span><span class="sxs-lookup"><span data-stu-id="687fb-132">Continue</span></span>
- <span data-ttu-id="687fb-133">理會</span><span class="sxs-lookup"><span data-stu-id="687fb-133">Ignore</span></span>
- <span data-ttu-id="687fb-134">看</span><span class="sxs-lookup"><span data-stu-id="687fb-134">Inquire</span></span>
- <span data-ttu-id="687fb-135">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="687fb-135">SilentlyContinue</span></span>
- <span data-ttu-id="687fb-136">停止</span><span class="sxs-lookup"><span data-stu-id="687fb-136">Stop</span></span>
- <span data-ttu-id="687fb-137">封存</span><span class="sxs-lookup"><span data-stu-id="687fb-137">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="687fb-138">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="687fb-138">-InformationVariable</span></span>
<span data-ttu-id="687fb-139">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="687fb-139">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="687fb-140">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="687fb-140">-ODataQuery</span></span>
<span data-ttu-id="687fb-141">指定 (OData) 樣式篩選的開放式資料通訊協定。</span><span class="sxs-lookup"><span data-stu-id="687fb-141">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="687fb-142">除了任何其他篩選器之外，此 Cmdlet 還會將此值附加到要求中。</span><span class="sxs-lookup"><span data-stu-id="687fb-142">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="687fb-143">-參數</span><span class="sxs-lookup"><span data-stu-id="687fb-143">-Parameters</span></span>
<span data-ttu-id="687fb-144">針對此 Cmdlet 調用的動作指定參數（作為雜湊資料表）。</span><span class="sxs-lookup"><span data-stu-id="687fb-144">Specifies parameters, as a hash table, for the action that this cmdlet invokes.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Object

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="687fb-145">-預先</span><span class="sxs-lookup"><span data-stu-id="687fb-145">-Pre</span></span>
<span data-ttu-id="687fb-146">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="687fb-146">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="687fb-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="687fb-147">-ResourceGroupName</span></span>
<span data-ttu-id="687fb-148">指定此 Cmdlet 在其中調用動作的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="687fb-148">Specifies the name of a resource group in which this cmdlet invokes an action.</span></span>

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

### <span data-ttu-id="687fb-149">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="687fb-149">-ResourceId</span></span>
<span data-ttu-id="687fb-150">指定此 Cmdlet 調用動作之資源的完整限定資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="687fb-150">Specifies the fully qualified resource ID of the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="687fb-151">識別碼包含訂閱，如下列範例所示：</span><span class="sxs-lookup"><span data-stu-id="687fb-151">The ID includes the subscription, as in the following example:</span></span> 

<span data-ttu-id="687fb-152">`/subscriptions/`訂閱識別碼`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="687fb-152">`/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="687fb-153">-CoNtext.resourcename</span><span class="sxs-lookup"><span data-stu-id="687fb-153">-ResourceName</span></span>
<span data-ttu-id="687fb-154">指定此 Cmdlet 在其上執行動作之資源資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="687fb-154">Specifies the name of the resource of the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="687fb-155">例如，若要指定資料庫，請使用下列格式：</span><span class="sxs-lookup"><span data-stu-id="687fb-155">For instance, to specify a database, use the following format:</span></span> 

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

### <span data-ttu-id="687fb-156">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="687fb-156">-ResourceType</span></span>
<span data-ttu-id="687fb-157">指定資源的類型。</span><span class="sxs-lookup"><span data-stu-id="687fb-157">Specifies the type of the resource.</span></span>
<span data-ttu-id="687fb-158">舉例來說，對於資料庫而言，資源類型如下所示：</span><span class="sxs-lookup"><span data-stu-id="687fb-158">For instance, for a database, the resource type is as follows:</span></span> 

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

### <span data-ttu-id="687fb-159">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="687fb-159">-TenantLevel</span></span>
<span data-ttu-id="687fb-160">表示此 Cmdlet 在租使用者層級運作。</span><span class="sxs-lookup"><span data-stu-id="687fb-160">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="687fb-161">-確認</span><span class="sxs-lookup"><span data-stu-id="687fb-161">-Confirm</span></span>
<span data-ttu-id="687fb-162">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="687fb-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="687fb-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="687fb-163">-WhatIf</span></span>
<span data-ttu-id="687fb-164">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="687fb-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="687fb-165">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="687fb-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="687fb-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="687fb-166">CommonParameters</span></span>
<span data-ttu-id="687fb-167">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="687fb-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="687fb-168">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="687fb-168">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="687fb-169">輸入</span><span class="sxs-lookup"><span data-stu-id="687fb-169">INPUTS</span></span>

### <span data-ttu-id="687fb-170">所有</span><span class="sxs-lookup"><span data-stu-id="687fb-170">None</span></span>
<span data-ttu-id="687fb-171">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="687fb-171">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="687fb-172">輸出</span><span class="sxs-lookup"><span data-stu-id="687fb-172">OUTPUTS</span></span>

### <span data-ttu-id="687fb-173">系統管理. PSObject</span><span class="sxs-lookup"><span data-stu-id="687fb-173">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="687fb-174">筆記</span><span class="sxs-lookup"><span data-stu-id="687fb-174">NOTES</span></span>

## <span data-ttu-id="687fb-175">相關連結</span><span class="sxs-lookup"><span data-stu-id="687fb-175">RELATED LINKS</span></span>
