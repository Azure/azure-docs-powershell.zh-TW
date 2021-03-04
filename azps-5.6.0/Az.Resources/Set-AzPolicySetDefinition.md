---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/set-azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicySetDefinition.md
ms.openlocfilehash: fab07b94c565a37d2884c5074de9f23692878df4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916893"
---
# <span data-ttu-id="1ba25-101">Set-AzPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="1ba25-101">Set-AzPolicySetDefinition</span></span>

## <span data-ttu-id="1ba25-102">簡介</span><span class="sxs-lookup"><span data-stu-id="1ba25-102">SYNOPSIS</span></span>
<span data-ttu-id="1ba25-103">修改策略集定義</span><span class="sxs-lookup"><span data-stu-id="1ba25-103">Modifies a policy set definition</span></span>

## <span data-ttu-id="1ba25-104">語法</span><span class="sxs-lookup"><span data-stu-id="1ba25-104">SYNTAX</span></span>

### <span data-ttu-id="1ba25-105">NameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="1ba25-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] [-GroupDefinition <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1ba25-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="1ba25-106">ManagementGroupNameParameterSet</span></span>
```
Set-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] -ManagementGroupName <String>
 [-GroupDefinition <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ba25-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1ba25-107">SubscriptionIdParameterSet</span></span>
```
Set-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] -SubscriptionId <Guid>
 [-GroupDefinition <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ba25-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1ba25-108">IdParameterSet</span></span>
```
Set-AzPolicySetDefinition -Id <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] [-GroupDefinition <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1ba25-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1ba25-109">InputObjectParameterSet</span></span>
```
Set-AzPolicySetDefinition [-DisplayName <String>] [-Description <String>] [-PolicyDefinition <String>]
 [-Metadata <String>] [-Parameter <String>] -InputObject <PsPolicySetDefinition> [-GroupDefinition <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1ba25-110">描述</span><span class="sxs-lookup"><span data-stu-id="1ba25-110">DESCRIPTION</span></span>
<span data-ttu-id="1ba25-111">**Set-AzPolicySetDefinition** Cmdlet 會修改一個策略定義。</span><span class="sxs-lookup"><span data-stu-id="1ba25-111">The **Set-AzPolicySetDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="1ba25-112">例子</span><span class="sxs-lookup"><span data-stu-id="1ba25-112">EXAMPLES</span></span>

### <span data-ttu-id="1ba25-113">範例 1：更新策略集定義的描述</span><span class="sxs-lookup"><span data-stu-id="1ba25-113">Example 1: Update the description of a policy set definition</span></span>
```
PS C:\> $PolicySetDefinition = Get-AzPolicySetDefinition -ResourceId '/subscriptions/mySub/Microsoft.Authorization/policySetDefinitions/myPSSetDefinition'
PS C:\> Set-AzPolicySetDefinition -Id $PolicySetDefinition.ResourceId -Description 'Updated policy to not allow virtual machine creation'
```

<span data-ttu-id="1ba25-114">第一個命令會使用 Cmdlet Get-AzPolicySetDefinition定義。</span><span class="sxs-lookup"><span data-stu-id="1ba25-114">The first command gets a policy set definition by using the Get-AzPolicySetDefinition cmdlet.</span></span>
<span data-ttu-id="1ba25-115">該命令會儲存該物件在$PolicySetDefinition變數中。</span><span class="sxs-lookup"><span data-stu-id="1ba25-115">The command stores that object in the $PolicySetDefinition variable.</span></span>
<span data-ttu-id="1ba25-116">第二個命令會更新由 **resourceId** 屬性識別之 $PolicySetDefinition。</span><span class="sxs-lookup"><span data-stu-id="1ba25-116">The second command updates the description of the policy set definition identified by the **ResourceId** property of $PolicySetDefinition.</span></span>

### <span data-ttu-id="1ba25-117">範例 2：更新策略集定義的中繼資料</span><span class="sxs-lookup"><span data-stu-id="1ba25-117">Example 2: Update the metadata of a policy set definition</span></span>
```
PS C:\> Set-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -Metadata '{"category":"Virtual Machine"}'


Name                  : VMPolicySetDefinition
ResourceId            : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policySetDefinitions/VMPolicySetDefinition
ResourceName          : VMPolicySetDefinition
ResourceType          : Microsoft.Authorization/policySetDefinitions
SubscriptionId        : 11111111-1111-1111-1111-111111111111
Properties            : @{displayName=VMPolicySetDefinition; policyType=Custom; metadata=; parameters=; policyDefinitions=System.Object[]}
PolicySetDefinitionId : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policySetDefinitions/VMPolicySetDefinition
```

<span data-ttu-id="1ba25-118">此命令會更新名為 VMPolicySetDefinition 之策略集定義的中繼資料，指出其類別為「虛擬機器」。</span><span class="sxs-lookup"><span data-stu-id="1ba25-118">This command updates the metadata of a policy set definition named VMPolicySetDefinition to indicate its category is "Virtual Machine".</span></span>

### <span data-ttu-id="1ba25-119">範例 3：更新策略集定義的群組</span><span class="sxs-lookup"><span data-stu-id="1ba25-119">Example 3: Update the groups of a policy set definition</span></span>
```
PS C:\> Set-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -GroupDefinition '[{ "name": "group1", "displayName": "Virtual Machine Security" }, { "name": "group2" }]'
```

<span data-ttu-id="1ba25-120">此命令會更新名為 VMPolicySetDefinition 之策略集定義的群組。</span><span class="sxs-lookup"><span data-stu-id="1ba25-120">This command updates the groups of a policy set definition named VMPolicySetDefinition.</span></span>

### <span data-ttu-id="1ba25-121">範例 4：使用雜湊表更新策略集定義的群組</span><span class="sxs-lookup"><span data-stu-id="1ba25-121">Example 4: Update the groups of a policy set definition using a hash table</span></span>
```
$groupsJson = ConvertTo-Json @{ name = "group1", displayName = "Virtual Machine Security" }, @{ name = "group2" }
PS C:\> Set-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -GroupDefinition $groupsJson
```

<span data-ttu-id="1ba25-122">此命令會使用雜湊表更新名為 VMPolicySetDefinition 之策略集定義的群組，以建構群組。</span><span class="sxs-lookup"><span data-stu-id="1ba25-122">This command updates the groups of a policy set definition named VMPolicySetDefinition using a hash table to construct the groups.</span></span>

## <span data-ttu-id="1ba25-123">參數</span><span class="sxs-lookup"><span data-stu-id="1ba25-123">PARAMETERS</span></span>

### <span data-ttu-id="1ba25-124">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="1ba25-124">-ApiVersion</span></span>
<span data-ttu-id="1ba25-125">設定時，表示要使用資源提供者 API 的版本。</span><span class="sxs-lookup"><span data-stu-id="1ba25-125">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="1ba25-126">如果未指定，API 版本會自動判斷為最新可用。</span><span class="sxs-lookup"><span data-stu-id="1ba25-126">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="1ba25-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ba25-127">-DefaultProfile</span></span>
<span data-ttu-id="1ba25-128">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="1ba25-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1ba25-129">-描述</span><span class="sxs-lookup"><span data-stu-id="1ba25-129">-Description</span></span>
<span data-ttu-id="1ba25-130">策略集定義的描述。</span><span class="sxs-lookup"><span data-stu-id="1ba25-130">The description for policy set definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ba25-131">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="1ba25-131">-DisplayName</span></span>
<span data-ttu-id="1ba25-132">策略集定義的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="1ba25-132">The display name for policy set definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ba25-133">-GroupDefinition</span><span class="sxs-lookup"><span data-stu-id="1ba25-133">-GroupDefinition</span></span>
<span data-ttu-id="1ba25-134">已更新之策略集定義之策略定義群組。</span><span class="sxs-lookup"><span data-stu-id="1ba25-134">The policy definition groups of the updated policy set definition.</span></span> <span data-ttu-id="1ba25-135">這可以是包含群組之檔案的路徑，或群組為 JSON 字串。</span><span class="sxs-lookup"><span data-stu-id="1ba25-135">This can either be a path to a file containing the groups, or the groups as a JSON string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ba25-136">-Id</span><span class="sxs-lookup"><span data-stu-id="1ba25-136">-Id</span></span>
<span data-ttu-id="1ba25-137">完整規定定義識別碼，包括訂閱。</span><span class="sxs-lookup"><span data-stu-id="1ba25-137">The fully qualified policy definition Id, including the subscription.</span></span>
<span data-ttu-id="1ba25-138">例如/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="1ba25-138">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ba25-139">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1ba25-139">-InputObject</span></span>
<span data-ttu-id="1ba25-140">此策略會設定定義物件，以更新從另一個 Cmdlet 輸出的結果。</span><span class="sxs-lookup"><span data-stu-id="1ba25-140">The policy set definition object to update that was output from another cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.Policy.PsPolicySetDefinition
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1ba25-141">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="1ba25-141">-ManagementGroupName</span></span>
<span data-ttu-id="1ba25-142">要更新之組定義之管理組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1ba25-142">The name of the management group of the policy set definition to update.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagementGroupNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ba25-143">-中繼資料</span><span class="sxs-lookup"><span data-stu-id="1ba25-143">-Metadata</span></span>
<span data-ttu-id="1ba25-144">更新之策略集定義的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="1ba25-144">The metadata of the updated policy set definition.</span></span> <span data-ttu-id="1ba25-145">這可以是包含中繼資料之檔案名的路徑，或是 JSON 字串的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="1ba25-145">This can either be a path to a file name containing the metadata, or the metadata as a JSON string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ba25-146">-名稱</span><span class="sxs-lookup"><span data-stu-id="1ba25-146">-Name</span></span>
<span data-ttu-id="1ba25-147">該策略集定義名稱。</span><span class="sxs-lookup"><span data-stu-id="1ba25-147">The policy set definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet, ManagementGroupNameParameterSet, SubscriptionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ba25-148">-Parameter</span><span class="sxs-lookup"><span data-stu-id="1ba25-148">-Parameter</span></span>
<span data-ttu-id="1ba25-149">更新原則集定義的參數宣告。</span><span class="sxs-lookup"><span data-stu-id="1ba25-149">The parameters declaration of the updated policy set definition.</span></span> <span data-ttu-id="1ba25-150">這可以是檔案名或包含參數宣告的 uri 路徑，或參數宣告為 JSON 字串。</span><span class="sxs-lookup"><span data-stu-id="1ba25-150">This can either be a path to a file name or uri containing the parameters declaration, or the parameters declaration as a JSON string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ba25-151">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="1ba25-151">-PolicyDefinition</span></span>
<span data-ttu-id="1ba25-152">該政策定義。</span><span class="sxs-lookup"><span data-stu-id="1ba25-152">The policy definitions.</span></span> <span data-ttu-id="1ba25-153">這可以是包含策略定義的檔案名路徑，或 JSON 字串中的策略定義。</span><span class="sxs-lookup"><span data-stu-id="1ba25-153">This can either be a path to a file name containing the policy definitions, or the policy definitions as a JSON string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ba25-154">-Pre</span><span class="sxs-lookup"><span data-stu-id="1ba25-154">-Pre</span></span>
<span data-ttu-id="1ba25-155">設定之後，表示當系統自動決定要使用哪個版本時，Cmdlet 應該使用測試版 API 版本。</span><span class="sxs-lookup"><span data-stu-id="1ba25-155">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="1ba25-156">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1ba25-156">-SubscriptionId</span></span>
<span data-ttu-id="1ba25-157">要更新之策略集定義的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="1ba25-157">The subscription ID of the policy set definition to update.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: SubscriptionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ba25-158">-確認</span><span class="sxs-lookup"><span data-stu-id="1ba25-158">-Confirm</span></span>
<span data-ttu-id="1ba25-159">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="1ba25-159">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ba25-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ba25-160">-WhatIf</span></span>
<span data-ttu-id="1ba25-161">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1ba25-161">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1ba25-162">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1ba25-162">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ba25-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ba25-163">CommonParameters</span></span>
<span data-ttu-id="1ba25-164">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="1ba25-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ba25-165">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1ba25-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ba25-166">輸入</span><span class="sxs-lookup"><span data-stu-id="1ba25-166">INPUTS</span></span>

### <span data-ttu-id="1ba25-167">System.String</span><span class="sxs-lookup"><span data-stu-id="1ba25-167">System.String</span></span>

### <span data-ttu-id="1ba25-168">System.Nullable'1[[System.Guid， System.Private.CoreLib， Version=4.0.0.0， Culture=neutral， PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="1ba25-168">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="1ba25-169">輸出</span><span class="sxs-lookup"><span data-stu-id="1ba25-169">OUTPUTS</span></span>

### <span data-ttu-id="1ba25-170">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="1ba25-170">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="1ba25-171">筆記</span><span class="sxs-lookup"><span data-stu-id="1ba25-171">NOTES</span></span>

## <span data-ttu-id="1ba25-172">相關連結</span><span class="sxs-lookup"><span data-stu-id="1ba25-172">RELATED LINKS</span></span>
