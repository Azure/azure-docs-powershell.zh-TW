---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 427F7300-0FEB-4F28-9C1D-27592AEBF6A0
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/invoke-azresourceaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Invoke-AzResourceAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Invoke-AzResourceAction.md
ms.openlocfilehash: 2feb6c48927c1cb5e092414c358b32912892a908
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93959718"
---
# <span data-ttu-id="f6d2f-101">Invoke-AzResourceAction</span><span class="sxs-lookup"><span data-stu-id="f6d2f-101">Invoke-AzResourceAction</span></span>

## <span data-ttu-id="f6d2f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f6d2f-102">SYNOPSIS</span></span>
<span data-ttu-id="f6d2f-103">在資源上調用動作。</span><span class="sxs-lookup"><span data-stu-id="f6d2f-103">Invokes an action on a resource.</span></span>

## <span data-ttu-id="f6d2f-104">句法</span><span class="sxs-lookup"><span data-stu-id="f6d2f-104">SYNTAX</span></span>

### <span data-ttu-id="f6d2f-105">ByResourceId (預設) </span><span class="sxs-lookup"><span data-stu-id="f6d2f-105">ByResourceId (Default)</span></span>
```
Invoke-AzResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceId <String> [-ODataQuery <String>]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f6d2f-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="f6d2f-106">BySubscriptionLevel</span></span>
```
Invoke-AzResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceName <String>
 -ResourceType <String> [-ExtensionResourceName <String>] [-ExtensionResourceType <String>]
 [-ODataQuery <String>] [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6d2f-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="f6d2f-107">ByTenantLevel</span></span>
```
Invoke-AzResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceName <String>
 -ResourceType <String> [-ExtensionResourceName <String>] [-ExtensionResourceType <String>]
 [-ODataQuery <String>] [-TenantLevel] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f6d2f-108">說明</span><span class="sxs-lookup"><span data-stu-id="f6d2f-108">DESCRIPTION</span></span>
<span data-ttu-id="f6d2f-109">**AzResourceAction** Cmdlet 會在指定的 Azure 資源上調用動作。</span><span class="sxs-lookup"><span data-stu-id="f6d2f-109">The **Invoke-AzResourceAction** cmdlet invokes an action on a specified Azure resource.</span></span>
<span data-ttu-id="f6d2f-110">若要取得支援的動作清單，請使用 Azure 資源管理器工具。</span><span class="sxs-lookup"><span data-stu-id="f6d2f-110">To get a list of supported actions, use the Azure Resource Explorer tool.</span></span>

## <span data-ttu-id="f6d2f-111">示例</span><span class="sxs-lookup"><span data-stu-id="f6d2f-111">EXAMPLES</span></span>

### <span data-ttu-id="f6d2f-112">範例1：使用 ResourceId 啟動 VM</span><span class="sxs-lookup"><span data-stu-id="f6d2f-112">Example 1: Invoke starting a VM with ResourceId</span></span>

```powershell
PS C:\>Invoke-AzResourceAction -ResourceId /subscriptions/{subId}/resourceGroups/{rg}/providers/Microsoft.Compute/virtualMachines/testVM -Action start

Confirm
Are you sure you want to invoke the 'start' action on the following resource: /subscriptions/{subId}/resourceGroups/testGroup/providers/Microsoft.Compute/virtualMachines/testVM
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="f6d2f-113">這個命令會以 {ResourceId} 啟動虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="f6d2f-113">This command starts the Virtual Machine with {ResourceId}.</span></span>

### <span data-ttu-id="f6d2f-114">範例2：使用 CoNtext.resourcename 來調用 poweroffing VM</span><span class="sxs-lookup"><span data-stu-id="f6d2f-114">Example 2: Invoke poweroffing a VM with ResourceName</span></span>

```powershell
PS C:\>Invoke-AzResourceAction -ResourceGroupName testGroup -ResourceName testVM -ResourceType Microsoft.Compute/virtualMachines/ -Action Poweroff -Force
```

<span data-ttu-id="f6d2f-115">這個命令會停止使用 {ResourceId} 的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="f6d2f-115">This command stops the Virtual Machine with {ResourceId}.</span></span>
<span data-ttu-id="f6d2f-116">命令會指定 *Force* 參數，因此不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f6d2f-116">The command specifies the *Force* parameter, therefore, it does not prompt you for confirmation.</span></span>

### <span data-ttu-id="f6d2f-117">範例3：使用 ResourceId 註冊資源提供者</span><span class="sxs-lookup"><span data-stu-id="f6d2f-117">Example 3: Invoke registering a resource provider with ResourceId</span></span>

```powershell
PS C:\>Invoke-AzResourceAction -ResourceId /subscriptions/{subId}/providers/Microsoft.Network -action register -Force

id                : /subscriptions/{subId}/providers/Microsoft.Network
namespace         : Microsoft.Network
authorizations    : {…}
resourceTypes     : {@{resourceType=virtualNetworks; locations=System.Object[]; apiVersions=System.Object[]},
                    @{resourceType=publicIPAddresses; locations=System.Object[]; apiVersions=System.Object[]},
                    @{resourceType=networkInterfaces; locations=System.Object[]; apiVersions=System.Object[]},
                    @{resourceType=privateEndpoints; locations=System.Object[]; apiVersions=System.Object[]}…}
registrationState : Registered
```

<span data-ttu-id="f6d2f-118">這個命令會註冊資源提供者 "Microsoft."。</span><span class="sxs-lookup"><span data-stu-id="f6d2f-118">This command registers a resource provider "Microsoft.Network".</span></span>
<span data-ttu-id="f6d2f-119">命令會指定 *Force* 參數，因此不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f6d2f-119">The command specifies the *Force* parameter, therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="f6d2f-120">參數</span><span class="sxs-lookup"><span data-stu-id="f6d2f-120">PARAMETERS</span></span>

### <span data-ttu-id="f6d2f-121">-動作</span><span class="sxs-lookup"><span data-stu-id="f6d2f-121">-Action</span></span>
<span data-ttu-id="f6d2f-122">指定要呼叫之動作的名稱。</span><span class="sxs-lookup"><span data-stu-id="f6d2f-122">Specifies the name of the action to invoke.</span></span>

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

### <span data-ttu-id="f6d2f-123">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="f6d2f-123">-ApiVersion</span></span>
<span data-ttu-id="f6d2f-124">指定要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="f6d2f-124">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="f6d2f-125">如果您沒有指定版本，此 Cmdlet 會使用最新的可用版本。</span><span class="sxs-lookup"><span data-stu-id="f6d2f-125">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="f6d2f-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6d2f-126">-DefaultProfile</span></span>
<span data-ttu-id="f6d2f-127">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="f6d2f-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f6d2f-128">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="f6d2f-128">-ExtensionResourceName</span></span>
<span data-ttu-id="f6d2f-129">指定此 Cmdlet 在其上執行動作之資源之延伸資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="f6d2f-129">Specifies the name of an extension resource for the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="f6d2f-130">例如，若要指定資料庫，請使用下列格式：伺服器名稱 `/` 資料庫名稱</span><span class="sxs-lookup"><span data-stu-id="f6d2f-130">For instance, to specify a database, use the following format: server name`/`database name</span></span>

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

### <span data-ttu-id="f6d2f-131">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="f6d2f-131">-ExtensionResourceType</span></span>
<span data-ttu-id="f6d2f-132">指定延伸資源的類型。</span><span class="sxs-lookup"><span data-stu-id="f6d2f-132">Specifies the type of the extension resource.</span></span>
<span data-ttu-id="f6d2f-133">例如： `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="f6d2f-133">For instance: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="f6d2f-134">-Force</span><span class="sxs-lookup"><span data-stu-id="f6d2f-134">-Force</span></span>
<span data-ttu-id="f6d2f-135">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="f6d2f-135">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f6d2f-136">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="f6d2f-136">-ODataQuery</span></span>
<span data-ttu-id="f6d2f-137">指定 (OData) 樣式篩選的開放式資料通訊協定。</span><span class="sxs-lookup"><span data-stu-id="f6d2f-137">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="f6d2f-138">除了任何其他篩選器之外，此 Cmdlet 還會將此值附加到要求中。</span><span class="sxs-lookup"><span data-stu-id="f6d2f-138">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="f6d2f-139">-參數</span><span class="sxs-lookup"><span data-stu-id="f6d2f-139">-Parameters</span></span>
<span data-ttu-id="f6d2f-140">針對此 Cmdlet 調用的動作指定參數（作為雜湊資料表）。</span><span class="sxs-lookup"><span data-stu-id="f6d2f-140">Specifies parameters, as a hash table, for the action that this cmdlet invokes.</span></span>

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

### <span data-ttu-id="f6d2f-141">-預先</span><span class="sxs-lookup"><span data-stu-id="f6d2f-141">-Pre</span></span>
<span data-ttu-id="f6d2f-142">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="f6d2f-142">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="f6d2f-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6d2f-143">-ResourceGroupName</span></span>
<span data-ttu-id="f6d2f-144">指定此 Cmdlet 在其中調用動作的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f6d2f-144">Specifies the name of a resource group in which this cmdlet invokes an action.</span></span>

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

### <span data-ttu-id="f6d2f-145">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f6d2f-145">-ResourceId</span></span>
<span data-ttu-id="f6d2f-146">指定此 Cmdlet 調用動作之資源的完整限定資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="f6d2f-146">Specifies the fully qualified resource ID of the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="f6d2f-147">識別碼包含訂閱，如下列範例所示： `/subscriptions/` 訂閱識別碼`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="f6d2f-147">The ID includes the subscription, as in the following example: `/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="f6d2f-148">-CoNtext.resourcename</span><span class="sxs-lookup"><span data-stu-id="f6d2f-148">-ResourceName</span></span>
<span data-ttu-id="f6d2f-149">指定此 Cmdlet 在其上執行動作之資源資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="f6d2f-149">Specifies the name of the resource of the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="f6d2f-150">例如，若要指定資料庫，請使用下列格式： `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="f6d2f-150">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="f6d2f-151">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="f6d2f-151">-ResourceType</span></span>
<span data-ttu-id="f6d2f-152">指定資源的類型。</span><span class="sxs-lookup"><span data-stu-id="f6d2f-152">Specifies the type of the resource.</span></span>
<span data-ttu-id="f6d2f-153">舉例來說，對於資料庫而言，資源類型如下所示： `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="f6d2f-153">For instance, for a database, the resource type is as follows: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="f6d2f-154">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="f6d2f-154">-TenantLevel</span></span>
<span data-ttu-id="f6d2f-155">表示此 Cmdlet 在租使用者層級運作。</span><span class="sxs-lookup"><span data-stu-id="f6d2f-155">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="f6d2f-156">-確認</span><span class="sxs-lookup"><span data-stu-id="f6d2f-156">-Confirm</span></span>
<span data-ttu-id="f6d2f-157">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f6d2f-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6d2f-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6d2f-158">-WhatIf</span></span>
<span data-ttu-id="f6d2f-159">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f6d2f-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f6d2f-160">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f6d2f-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6d2f-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6d2f-161">CommonParameters</span></span>
<span data-ttu-id="f6d2f-162">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f6d2f-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6d2f-163">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f6d2f-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6d2f-164">輸入</span><span class="sxs-lookup"><span data-stu-id="f6d2f-164">INPUTS</span></span>

### <span data-ttu-id="f6d2f-165">System.object</span><span class="sxs-lookup"><span data-stu-id="f6d2f-165">System.String</span></span>

## <span data-ttu-id="f6d2f-166">輸出</span><span class="sxs-lookup"><span data-stu-id="f6d2f-166">OUTPUTS</span></span>

### <span data-ttu-id="f6d2f-167">系統管理. PSObject</span><span class="sxs-lookup"><span data-stu-id="f6d2f-167">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="f6d2f-168">筆記</span><span class="sxs-lookup"><span data-stu-id="f6d2f-168">NOTES</span></span>

## <span data-ttu-id="f6d2f-169">相關連結</span><span class="sxs-lookup"><span data-stu-id="f6d2f-169">RELATED LINKS</span></span>
