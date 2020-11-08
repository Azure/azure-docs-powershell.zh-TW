---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicySetDefinition.md
ms.openlocfilehash: cd8bc24a0cedac91ef18e19a80e1662fdcbac297
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94127349"
---
# <span data-ttu-id="52369-101">Set-AzPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="52369-101">Set-AzPolicySetDefinition</span></span>

## <span data-ttu-id="52369-102">摘要</span><span class="sxs-lookup"><span data-stu-id="52369-102">SYNOPSIS</span></span>
<span data-ttu-id="52369-103">修改原則集定義</span><span class="sxs-lookup"><span data-stu-id="52369-103">Modifies a policy set definition</span></span>

## <span data-ttu-id="52369-104">句法</span><span class="sxs-lookup"><span data-stu-id="52369-104">SYNTAX</span></span>

### <span data-ttu-id="52369-105">NameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="52369-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] [-GroupDefinition <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="52369-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="52369-106">ManagementGroupNameParameterSet</span></span>
```
Set-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] -ManagementGroupName <String>
 [-GroupDefinition <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52369-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="52369-107">SubscriptionIdParameterSet</span></span>
```
Set-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] -SubscriptionId <Guid>
 [-GroupDefinition <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52369-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="52369-108">IdParameterSet</span></span>
```
Set-AzPolicySetDefinition -Id <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] [-GroupDefinition <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="52369-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="52369-109">InputObjectParameterSet</span></span>
```
Set-AzPolicySetDefinition [-DisplayName <String>] [-Description <String>] [-PolicyDefinition <String>]
 [-Metadata <String>] [-Parameter <String>] -InputObject <PsPolicySetDefinition> [-GroupDefinition <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="52369-110">說明</span><span class="sxs-lookup"><span data-stu-id="52369-110">DESCRIPTION</span></span>
<span data-ttu-id="52369-111">**AzPolicySetDefinition** Cmdlet 會修改原則定義。</span><span class="sxs-lookup"><span data-stu-id="52369-111">The **Set-AzPolicySetDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="52369-112">示例</span><span class="sxs-lookup"><span data-stu-id="52369-112">EXAMPLES</span></span>

### <span data-ttu-id="52369-113">範例1：更新原則集定義的描述</span><span class="sxs-lookup"><span data-stu-id="52369-113">Example 1: Update the description of a policy set definition</span></span>
```
PS C:\> $PolicySetDefinition = Get-AzPolicySetDefinition -ResourceId '/subscriptions/mySub/Microsoft.Authorization/policySetDefinitions/myPSSetDefinition'
PS C:\> Set-AzPolicySetDefinition -Id $PolicySetDefinition.ResourceId -Description 'Updated policy to not allow virtual machine creation'
```

<span data-ttu-id="52369-114">第一個命令會使用 Get-AzPolicySetDefinition Cmdlet 來取得原則集定義。</span><span class="sxs-lookup"><span data-stu-id="52369-114">The first command gets a policy set definition by using the Get-AzPolicySetDefinition cmdlet.</span></span>
<span data-ttu-id="52369-115">該命令會將該物件儲存在 $PolicySetDefinition 變數中。</span><span class="sxs-lookup"><span data-stu-id="52369-115">The command stores that object in the $PolicySetDefinition variable.</span></span>
<span data-ttu-id="52369-116">第二個命令會更新由 $PolicySetDefinition 的 **ResourceId** 屬性所識別之原則集定義的描述。</span><span class="sxs-lookup"><span data-stu-id="52369-116">The second command updates the description of the policy set definition identified by the **ResourceId** property of $PolicySetDefinition.</span></span>

### <span data-ttu-id="52369-117">範例2：更新原則集定義的中繼資料</span><span class="sxs-lookup"><span data-stu-id="52369-117">Example 2: Update the metadata of a policy set definition</span></span>
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

<span data-ttu-id="52369-118">這個命令會更新名為 VMPolicySetDefinition 的原則集定義中繼資料，以指出其類別是「虛擬機器」。</span><span class="sxs-lookup"><span data-stu-id="52369-118">This command updates the metadata of a policy set definition named VMPolicySetDefinition to indicate its category is "Virtual Machine".</span></span>

### <span data-ttu-id="52369-119">範例3：更新原則集定義的群組</span><span class="sxs-lookup"><span data-stu-id="52369-119">Example 3: Update the groups of a policy set definition</span></span>
```
PS C:\> Set-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -GroupDefinition '[{ "name": "group1", "displayName": "Virtual Machine Security" }, { "name": "group2" }]'
```

<span data-ttu-id="52369-120">這個命令會更新名為 VMPolicySetDefinition 的原則集定義群組。</span><span class="sxs-lookup"><span data-stu-id="52369-120">This command updates the groups of a policy set definition named VMPolicySetDefinition.</span></span>

### <span data-ttu-id="52369-121">範例4：使用雜湊資料表更新原則集定義的群組</span><span class="sxs-lookup"><span data-stu-id="52369-121">Example 4: Update the groups of a policy set definition using a hash table</span></span>
```
$groupsJson = ConvertTo-Json @{ name = "group1", displayName = "Virtual Machine Security" }, @{ name = "group2" }
PS C:\> Set-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -GroupDefinition $groupsJson
```

<span data-ttu-id="52369-122">這個命令會使用雜湊資料表來構造群組，以更新名為 VMPolicySetDefinition 的原則集定義群組。</span><span class="sxs-lookup"><span data-stu-id="52369-122">This command updates the groups of a policy set definition named VMPolicySetDefinition using a hash table to construct the groups.</span></span>

## <span data-ttu-id="52369-123">參數</span><span class="sxs-lookup"><span data-stu-id="52369-123">PARAMETERS</span></span>

### <span data-ttu-id="52369-124">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="52369-124">-ApiVersion</span></span>
<span data-ttu-id="52369-125">設定時，會指出要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="52369-125">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="52369-126">如果未指定，API 版本會自動決定為最新的可用。</span><span class="sxs-lookup"><span data-stu-id="52369-126">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="52369-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52369-127">-DefaultProfile</span></span>
<span data-ttu-id="52369-128">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="52369-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="52369-129">-描述</span><span class="sxs-lookup"><span data-stu-id="52369-129">-Description</span></span>
<span data-ttu-id="52369-130">原則集定義的描述。</span><span class="sxs-lookup"><span data-stu-id="52369-130">The description for policy set definition.</span></span>

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

### <span data-ttu-id="52369-131">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="52369-131">-DisplayName</span></span>
<span data-ttu-id="52369-132">原則集定義的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="52369-132">The display name for policy set definition.</span></span>

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

### <span data-ttu-id="52369-133">-GroupDefinition</span><span class="sxs-lookup"><span data-stu-id="52369-133">-GroupDefinition</span></span>
<span data-ttu-id="52369-134">更新之原則集定義的原則定義群組。</span><span class="sxs-lookup"><span data-stu-id="52369-134">The policy definition groups of the updated policy set definition.</span></span> <span data-ttu-id="52369-135">這可以是包含群組之檔案的路徑，或作為 JSON 字串的群組。</span><span class="sxs-lookup"><span data-stu-id="52369-135">This can either be a path to a file containing the groups, or the groups as a JSON string.</span></span>

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

### <span data-ttu-id="52369-136">-識別碼</span><span class="sxs-lookup"><span data-stu-id="52369-136">-Id</span></span>
<span data-ttu-id="52369-137">完全合格的原則定義識別碼，包括訂閱。</span><span class="sxs-lookup"><span data-stu-id="52369-137">The fully qualified policy definition Id, including the subscription.</span></span>
<span data-ttu-id="52369-138">例如/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="52369-138">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="52369-139">-InputObject</span><span class="sxs-lookup"><span data-stu-id="52369-139">-InputObject</span></span>
<span data-ttu-id="52369-140">從另一個 Cmdlet 輸出的要更新的原則集定義物件。</span><span class="sxs-lookup"><span data-stu-id="52369-140">The policy set definition object to update that was output from another cmdlet.</span></span>

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

### <span data-ttu-id="52369-141">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="52369-141">-ManagementGroupName</span></span>
<span data-ttu-id="52369-142">要更新之原則集定義之管理群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="52369-142">The name of the management group of the policy set definition to update.</span></span>

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

### <span data-ttu-id="52369-143">-中繼資料</span><span class="sxs-lookup"><span data-stu-id="52369-143">-Metadata</span></span>
<span data-ttu-id="52369-144">更新之原則集定義的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="52369-144">The metadata of the updated policy set definition.</span></span> <span data-ttu-id="52369-145">這可以是包含中繼資料之檔案名的路徑，或作為 JSON 字串的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="52369-145">This can either be a path to a file name containing the metadata, or the metadata as a JSON string.</span></span>

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

### <span data-ttu-id="52369-146">-名稱</span><span class="sxs-lookup"><span data-stu-id="52369-146">-Name</span></span>
<span data-ttu-id="52369-147">原則集定義名稱。</span><span class="sxs-lookup"><span data-stu-id="52369-147">The policy set definition name.</span></span>

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

### <span data-ttu-id="52369-148">-參數</span><span class="sxs-lookup"><span data-stu-id="52369-148">-Parameter</span></span>
<span data-ttu-id="52369-149">更新之原則集定義的參數宣告。</span><span class="sxs-lookup"><span data-stu-id="52369-149">The parameters declaration of the updated policy set definition.</span></span> <span data-ttu-id="52369-150">這可以是包含參數宣告之檔案名或 uri 的路徑，或作為 JSON 字串的參數宣告。</span><span class="sxs-lookup"><span data-stu-id="52369-150">This can either be a path to a file name or uri containing the parameters declaration, or the parameters declaration as a JSON string.</span></span>

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

### <span data-ttu-id="52369-151">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="52369-151">-PolicyDefinition</span></span>
<span data-ttu-id="52369-152">原則定義。</span><span class="sxs-lookup"><span data-stu-id="52369-152">The policy definitions.</span></span> <span data-ttu-id="52369-153">這可以是包含原則定義的檔案名路徑，或原則定義（JSON 字串）。</span><span class="sxs-lookup"><span data-stu-id="52369-153">This can either be a path to a file name containing the policy definitions, or the policy definitions as a JSON string.</span></span>

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

### <span data-ttu-id="52369-154">-預先</span><span class="sxs-lookup"><span data-stu-id="52369-154">-Pre</span></span>
<span data-ttu-id="52369-155">設定時，表示 Cmdlet 應該使用預發行 API 版本，以便自動判斷要使用的版本。</span><span class="sxs-lookup"><span data-stu-id="52369-155">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="52369-156">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="52369-156">-SubscriptionId</span></span>
<span data-ttu-id="52369-157">要更新之原則集定義的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="52369-157">The subscription ID of the policy set definition to update.</span></span>

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

### <span data-ttu-id="52369-158">-確認</span><span class="sxs-lookup"><span data-stu-id="52369-158">-Confirm</span></span>
<span data-ttu-id="52369-159">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="52369-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52369-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52369-160">-WhatIf</span></span>
<span data-ttu-id="52369-161">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="52369-161">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="52369-162">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="52369-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52369-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52369-163">CommonParameters</span></span>
<span data-ttu-id="52369-164">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="52369-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52369-165">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="52369-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52369-166">輸入</span><span class="sxs-lookup"><span data-stu-id="52369-166">INPUTS</span></span>

### <span data-ttu-id="52369-167">System.object</span><span class="sxs-lookup"><span data-stu-id="52369-167">System.String</span></span>

### <span data-ttu-id="52369-168">"CoreLib" 1 [[System. Guid.empty]、[System.] = 4.0.0.0、Culture = 中性、PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="52369-168">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="52369-169">輸出</span><span class="sxs-lookup"><span data-stu-id="52369-169">OUTPUTS</span></span>

### <span data-ttu-id="52369-170">系統管理. PSObject</span><span class="sxs-lookup"><span data-stu-id="52369-170">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="52369-171">筆記</span><span class="sxs-lookup"><span data-stu-id="52369-171">NOTES</span></span>

## <span data-ttu-id="52369-172">相關連結</span><span class="sxs-lookup"><span data-stu-id="52369-172">RELATED LINKS</span></span>
