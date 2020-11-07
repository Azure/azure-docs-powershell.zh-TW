---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicySetDefinition.md
ms.openlocfilehash: 8a8559058b0bb5e1b33d93451bed35182a44783b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93957676"
---
# <span data-ttu-id="81a46-101">Set-AzPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="81a46-101">Set-AzPolicySetDefinition</span></span>

## <span data-ttu-id="81a46-102">摘要</span><span class="sxs-lookup"><span data-stu-id="81a46-102">SYNOPSIS</span></span>
<span data-ttu-id="81a46-103">修改原則集定義</span><span class="sxs-lookup"><span data-stu-id="81a46-103">Modifies a policy set definition</span></span>

## <span data-ttu-id="81a46-104">句法</span><span class="sxs-lookup"><span data-stu-id="81a46-104">SYNTAX</span></span>

### <span data-ttu-id="81a46-105">NameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="81a46-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] [-GroupDefinition <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="81a46-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="81a46-106">ManagementGroupNameParameterSet</span></span>
```
Set-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] -ManagementGroupName <String>
 [-GroupDefinition <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81a46-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="81a46-107">SubscriptionIdParameterSet</span></span>
```
Set-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] -SubscriptionId <Guid>
 [-GroupDefinition <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81a46-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="81a46-108">IdParameterSet</span></span>
```
Set-AzPolicySetDefinition -Id <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] [-GroupDefinition <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="81a46-109">說明</span><span class="sxs-lookup"><span data-stu-id="81a46-109">DESCRIPTION</span></span>
<span data-ttu-id="81a46-110">**AzPolicySetDefinition** Cmdlet 會修改原則定義。</span><span class="sxs-lookup"><span data-stu-id="81a46-110">The **Set-AzPolicySetDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="81a46-111">示例</span><span class="sxs-lookup"><span data-stu-id="81a46-111">EXAMPLES</span></span>

### <span data-ttu-id="81a46-112">範例1：更新原則集定義的描述</span><span class="sxs-lookup"><span data-stu-id="81a46-112">Example 1: Update the description of a policy set definition</span></span>
```
PS C:\> $PolicySetDefinition = Get-AzPolicySetDefinition -ResourceId '/subscriptions/mySub/Microsoft.Authorization/policySetDefinitions/myPSSetDefinition'
PS C:\> Set-AzPolicySetDefinition -Id $PolicySetDefinition.ResourceId -Description 'Updated policy to not allow virtual machine creation'
```

<span data-ttu-id="81a46-113">第一個命令會使用 Get-AzPolicySetDefinition Cmdlet 來取得原則集定義。</span><span class="sxs-lookup"><span data-stu-id="81a46-113">The first command gets a policy set definition by using the Get-AzPolicySetDefinition cmdlet.</span></span>
<span data-ttu-id="81a46-114">該命令會將該物件儲存在 $PolicySetDefinition 變數中。</span><span class="sxs-lookup"><span data-stu-id="81a46-114">The command stores that object in the $PolicySetDefinition variable.</span></span>
<span data-ttu-id="81a46-115">第二個命令會更新由 $PolicySetDefinition 的 **ResourceId** 屬性所識別之原則集定義的描述。</span><span class="sxs-lookup"><span data-stu-id="81a46-115">The second command updates the description of the policy set definition identified by the **ResourceId** property of $PolicySetDefinition.</span></span>

### <span data-ttu-id="81a46-116">範例2：更新原則集定義的中繼資料</span><span class="sxs-lookup"><span data-stu-id="81a46-116">Example 2: Update the metadata of a policy set definition</span></span>
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

<span data-ttu-id="81a46-117">這個命令會更新名為 VMPolicySetDefinition 的原則集定義中繼資料，以指出其類別是「虛擬機器」。</span><span class="sxs-lookup"><span data-stu-id="81a46-117">This command updates the metadata of a policy set definition named VMPolicySetDefinition to indicate its category is "Virtual Machine".</span></span>

### <span data-ttu-id="81a46-118">範例3：更新原則集定義的群組</span><span class="sxs-lookup"><span data-stu-id="81a46-118">Example 3: Update the groups of a policy set definition</span></span>
```
PS C:\> Set-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -GroupDefinition '[{ "name": "group1", "displayName": "Virtual Machine Security" }, { "name": "group2" }]'
```

<span data-ttu-id="81a46-119">這個命令會更新名為 VMPolicySetDefinition 的原則集定義群組。</span><span class="sxs-lookup"><span data-stu-id="81a46-119">This command updates the groups of a policy set definition named VMPolicySetDefinition.</span></span>

### <span data-ttu-id="81a46-120">範例4：使用雜湊資料表更新原則集定義的群組</span><span class="sxs-lookup"><span data-stu-id="81a46-120">Example 4: Update the groups of a policy set definition using a hash table</span></span>
```
$groupsJson = ConvertTo-Json @{ name = "group1", displayName = "Virtual Machine Security" }, @{ name = "group2" }
PS C:\> Set-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -GroupDefinition $groupsJson
```

<span data-ttu-id="81a46-121">這個命令會使用雜湊資料表來構造群組，以更新名為 VMPolicySetDefinition 的原則集定義群組。</span><span class="sxs-lookup"><span data-stu-id="81a46-121">This command updates the groups of a policy set definition named VMPolicySetDefinition using a hash table to construct the groups.</span></span>

## <span data-ttu-id="81a46-122">參數</span><span class="sxs-lookup"><span data-stu-id="81a46-122">PARAMETERS</span></span>

### <span data-ttu-id="81a46-123">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="81a46-123">-ApiVersion</span></span>
<span data-ttu-id="81a46-124">設定時，會指出要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="81a46-124">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="81a46-125">如果未指定，API 版本會自動決定為最新的可用。</span><span class="sxs-lookup"><span data-stu-id="81a46-125">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="81a46-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81a46-126">-DefaultProfile</span></span>
<span data-ttu-id="81a46-127">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="81a46-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="81a46-128">-描述</span><span class="sxs-lookup"><span data-stu-id="81a46-128">-Description</span></span>
<span data-ttu-id="81a46-129">原則集定義的描述。</span><span class="sxs-lookup"><span data-stu-id="81a46-129">The description for policy set definition.</span></span>

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

### <span data-ttu-id="81a46-130">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="81a46-130">-DisplayName</span></span>
<span data-ttu-id="81a46-131">原則集定義的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="81a46-131">The display name for policy set definition.</span></span>

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

### <span data-ttu-id="81a46-132">-GroupDefinition</span><span class="sxs-lookup"><span data-stu-id="81a46-132">-GroupDefinition</span></span>
<span data-ttu-id="81a46-133">更新之原則集定義的原則定義群組。</span><span class="sxs-lookup"><span data-stu-id="81a46-133">The policy definition groups of the updated policy set definition.</span></span> <span data-ttu-id="81a46-134">這可以是包含群組之檔案的路徑，或作為 JSON 字串的群組。</span><span class="sxs-lookup"><span data-stu-id="81a46-134">This can either be a path to a file containing the groups, or the groups as a JSON string.</span></span>

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

### <span data-ttu-id="81a46-135">-識別碼</span><span class="sxs-lookup"><span data-stu-id="81a46-135">-Id</span></span>
<span data-ttu-id="81a46-136">完全合格的原則定義識別碼，包括訂閱。</span><span class="sxs-lookup"><span data-stu-id="81a46-136">The fully qualified policy definition Id, including the subscription.</span></span>
<span data-ttu-id="81a46-137">例如/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="81a46-137">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="81a46-138">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="81a46-138">-ManagementGroupName</span></span>
<span data-ttu-id="81a46-139">要更新之原則集定義之管理群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="81a46-139">The name of the management group of the policy set definition to update.</span></span>

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

### <span data-ttu-id="81a46-140">-中繼資料</span><span class="sxs-lookup"><span data-stu-id="81a46-140">-Metadata</span></span>
<span data-ttu-id="81a46-141">更新之原則集定義的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="81a46-141">The metadata of the updated policy set definition.</span></span> <span data-ttu-id="81a46-142">這可以是包含中繼資料之檔案名的路徑，或作為 JSON 字串的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="81a46-142">This can either be a path to a file name containing the metadata, or the metadata as a JSON string.</span></span>

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

### <span data-ttu-id="81a46-143">-名稱</span><span class="sxs-lookup"><span data-stu-id="81a46-143">-Name</span></span>
<span data-ttu-id="81a46-144">原則集定義名稱。</span><span class="sxs-lookup"><span data-stu-id="81a46-144">The policy set definition name.</span></span>

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

### <span data-ttu-id="81a46-145">-參數</span><span class="sxs-lookup"><span data-stu-id="81a46-145">-Parameter</span></span>
<span data-ttu-id="81a46-146">更新之原則集定義的參數宣告。</span><span class="sxs-lookup"><span data-stu-id="81a46-146">The parameters declaration of the updated policy set definition.</span></span> <span data-ttu-id="81a46-147">這可以是包含參數宣告之檔案名或 uri 的路徑，或作為 JSON 字串的參數宣告。</span><span class="sxs-lookup"><span data-stu-id="81a46-147">This can either be a path to a file name or uri containing the parameters declaration, or the parameters declaration as a JSON string.</span></span>

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

### <span data-ttu-id="81a46-148">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="81a46-148">-PolicyDefinition</span></span>
<span data-ttu-id="81a46-149">原則定義。</span><span class="sxs-lookup"><span data-stu-id="81a46-149">The policy definitions.</span></span> <span data-ttu-id="81a46-150">這可以是包含原則定義的檔案名路徑，或原則定義（JSON 字串）。</span><span class="sxs-lookup"><span data-stu-id="81a46-150">This can either be a path to a file name containing the policy definitions, or the policy definitions as a JSON string.</span></span>

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

### <span data-ttu-id="81a46-151">-預先</span><span class="sxs-lookup"><span data-stu-id="81a46-151">-Pre</span></span>
<span data-ttu-id="81a46-152">設定時，表示 Cmdlet 應該使用預發行 API 版本，以便自動判斷要使用的版本。</span><span class="sxs-lookup"><span data-stu-id="81a46-152">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="81a46-153">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="81a46-153">-SubscriptionId</span></span>
<span data-ttu-id="81a46-154">要更新之原則集定義的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="81a46-154">The subscription ID of the policy set definition to update.</span></span>

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

### <span data-ttu-id="81a46-155">-確認</span><span class="sxs-lookup"><span data-stu-id="81a46-155">-Confirm</span></span>
<span data-ttu-id="81a46-156">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="81a46-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81a46-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81a46-157">-WhatIf</span></span>
<span data-ttu-id="81a46-158">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="81a46-158">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="81a46-159">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="81a46-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81a46-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81a46-160">CommonParameters</span></span>
<span data-ttu-id="81a46-161">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="81a46-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81a46-162">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="81a46-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81a46-163">輸入</span><span class="sxs-lookup"><span data-stu-id="81a46-163">INPUTS</span></span>

### <span data-ttu-id="81a46-164">System.object</span><span class="sxs-lookup"><span data-stu-id="81a46-164">System.String</span></span>

### <span data-ttu-id="81a46-165">"CoreLib" 1 [[System. Guid.empty]、[System.] = 4.0.0.0、Culture = 中性、PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="81a46-165">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="81a46-166">輸出</span><span class="sxs-lookup"><span data-stu-id="81a46-166">OUTPUTS</span></span>

### <span data-ttu-id="81a46-167">系統管理. PSObject</span><span class="sxs-lookup"><span data-stu-id="81a46-167">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="81a46-168">筆記</span><span class="sxs-lookup"><span data-stu-id="81a46-168">NOTES</span></span>

## <span data-ttu-id="81a46-169">相關連結</span><span class="sxs-lookup"><span data-stu-id="81a46-169">RELATED LINKS</span></span>
