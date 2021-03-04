---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 31F2AF24-488D-4CAF-A9C8-C8DAE76E031F
online version: https://docs.microsoft.com/powershell/module/az.resources/new-azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicyDefinition.md
ms.openlocfilehash: 259b0abd120fb27eee1ca80da61266f4c890423f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907070"
---
# <span data-ttu-id="f37b6-101">New-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f37b6-101">New-AzPolicyDefinition</span></span>

## <span data-ttu-id="f37b6-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f37b6-102">SYNOPSIS</span></span>
<span data-ttu-id="f37b6-103">建立一個策略定義。</span><span class="sxs-lookup"><span data-stu-id="f37b6-103">Creates a policy definition.</span></span>

## <span data-ttu-id="f37b6-104">語法</span><span class="sxs-lookup"><span data-stu-id="f37b6-104">SYNTAX</span></span>

### <span data-ttu-id="f37b6-105">NameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="f37b6-105">NameParameterSet (Default)</span></span>
```
New-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] -Policy <String>
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f37b6-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f37b6-106">ManagementGroupNameParameterSet</span></span>
```
New-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] -Policy <String>
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] -ManagementGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f37b6-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f37b6-107">SubscriptionIdParameterSet</span></span>
```
New-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] -Policy <String>
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] -SubscriptionId <Guid> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f37b6-108">描述</span><span class="sxs-lookup"><span data-stu-id="f37b6-108">DESCRIPTION</span></span>
<span data-ttu-id="f37b6-109">**New-AzPolicyDefinition** Cmdlet 會建立一個原則定義，其中包含 JavaScript 物件標記法和 JSON 格式 (原則規則) 規則。</span><span class="sxs-lookup"><span data-stu-id="f37b6-109">The **New-AzPolicyDefinition** cmdlet creates a policy definition that includes a policy rule in JavaScript Object Notation (JSON) format.</span></span>

## <span data-ttu-id="f37b6-110">例子</span><span class="sxs-lookup"><span data-stu-id="f37b6-110">EXAMPLES</span></span>

### <span data-ttu-id="f37b6-111">範例 1：使用策略檔案建立策略定義</span><span class="sxs-lookup"><span data-stu-id="f37b6-111">Example 1: Create a policy definition by using a policy file</span></span>
```
{
   "if": {
      "field": "location",
      "notIn": ["eastus", "westus", "centralus"]
   },
   "then": {
      "effect": "audit"
   }
}
```

```
PS C:\> New-AzPolicyDefinition -Name 'LocationDefinition' -Policy C:\LocationPolicy.json
```

<span data-ttu-id="f37b6-112">此命令會建立名為 LocationDefinition 原則定義，其中包含在 C:\LocationPolicy.js中指定的原則規則。</span><span class="sxs-lookup"><span data-stu-id="f37b6-112">This command creates a policy definition named LocationDefinition that contains the policy rule specified in C:\LocationPolicy.json.</span></span> <span data-ttu-id="f37b6-113">上方提供檔案LocationPolicy.js範例內容。</span><span class="sxs-lookup"><span data-stu-id="f37b6-113">Example content for the LocationPolicy.json file is provided above.</span></span>

### <span data-ttu-id="f37b6-114">範例 2：使用內嵌參數建立參數化政策定義</span><span class="sxs-lookup"><span data-stu-id="f37b6-114">Example 2: Create a parameterized policy definition using inline parameters</span></span>
```
{
   "if": {
      "field": "location",
      "notIn": "[parameters('listOfAllowedLocations')]"
   },
   "then": {
      "effect": "audit"
   }
}
```

```
PS C:\> New-AzPolicyDefinition -Name 'LocationDefinition' -Policy C:\LocationPolicy.json -Parameter '{ "listOfAllowedLocations": { "type": "array" } }'
```

<span data-ttu-id="f37b6-115">此命令會建立名為 LocationDefinition 原則定義，其中包含在 C:\LocationPolicy.js中指定的原則規則。</span><span class="sxs-lookup"><span data-stu-id="f37b6-115">This command creates a policy definition named LocationDefinition that contains the policy rule specified in C:\LocationPolicy.json.</span></span> <span data-ttu-id="f37b6-116">原則規則的參數定義是內嵌提供。</span><span class="sxs-lookup"><span data-stu-id="f37b6-116">The parameter definition for the policy rule is provided inline.</span></span>

### <span data-ttu-id="f37b6-117">範例 3：在管理群組中建立內嵌策略定義</span><span class="sxs-lookup"><span data-stu-id="f37b6-117">Example 3: Create a policy definition inline in a management group</span></span>
```
PS C:\> New-AzPolicyDefinition -Name 'VMPolicyDefinition' -ManagementGroupName Dept42 -DisplayName 'Virtual Machine policy definition' -Policy '{"if":{"field":"type","equals":"Microsoft.Compute/virtualMachines"},"then":{"effect":"deny"}}'
```

<span data-ttu-id="f37b6-118">此命令在管理群組 Dept42 中建立名為 VMPolicyDefinition 的策略定義。</span><span class="sxs-lookup"><span data-stu-id="f37b6-118">This command creates a policy definition named VMPolicyDefinition in management group Dept42.</span></span>
<span data-ttu-id="f37b6-119">命令會以有效的 JSON 格式將規則指定為字串。</span><span class="sxs-lookup"><span data-stu-id="f37b6-119">The command specifies the policy as a string in valid JSON format.</span></span>

### <span data-ttu-id="f37b6-120">範例 4：使用中繼資料內嵌建立策略定義</span><span class="sxs-lookup"><span data-stu-id="f37b6-120">Example 4: Create a policy definition inline with metadata</span></span>
```
PS C:\> New-AzPolicyDefinition -Name 'VMPolicyDefinition' -Metadata '{"category":"Virtual Machine"}' -Policy '{"if":{"field":"type","equals":"Microsoft.Compute/virtualMachines"},"then":{"effect":"deny"}}'


Name               : VMPolicyDefinition
ResourceId         : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policyDefinitions/VMPolicyDefinition
ResourceName       : VMPolicyDefinition
ResourceType       : Microsoft.Authorization/policyDefinitions
SubscriptionId     : 11111111-1111-1111-1111-111111111111
Properties         : @{displayName=VMPolicyDefinition; policyType=Custom; mode=All; metadata=; policyRule=}
PolicyDefinitionId : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policyDefinitions/VMPolicyDefinition
```

<span data-ttu-id="f37b6-121">此命令會建立名為 VMPolicyDefinition 的一個策略定義，其中繼資料指出其類別為「虛擬機器」。</span><span class="sxs-lookup"><span data-stu-id="f37b6-121">This command creates a policy definition named VMPolicyDefinition with metadata indicating its category is "Virtual Machine".</span></span>
<span data-ttu-id="f37b6-122">命令會以有效的 JSON 格式將規則指定為字串。</span><span class="sxs-lookup"><span data-stu-id="f37b6-122">The command specifies the policy as a string in valid JSON format.</span></span>

### <span data-ttu-id="f37b6-123">範例 5：使用模式內嵌建立策略定義</span><span class="sxs-lookup"><span data-stu-id="f37b6-123">Example 5: Create a policy definition inline with mode</span></span>
```
PS C:\> New-AzPolicyDefinition -Name 'TagsPolicyDefinition' -Policy '{"if":{"value":"[less(length(field(''tags'')), 3)]","equals":true},"then":{"effect":"deny"}}' -Mode Indexed


Name               : TagsPolicyDefinition
ResourceId         : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policyDefinitions/TagsPolicyDefinition
ResourceName       : TagsPolicyDefinition
ResourceType       : Microsoft.Authorization/policyDefinitions
SubscriptionId     : 11111111-1111-1111-1111-111111111111
Properties         : @{displayName=TagsPolicyDefinition; policyType=Custom; mode=Indexed; metadata=; parameters=; policyRule=}
PolicyDefinitionId : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policyDefinitions/TagsPolicyDefinition
```

<span data-ttu-id="f37b6-124">此命令會建立名為 TagsPolicyDefinition 且模式 「已編制索引」，指出僅應針對支援標記和位置的資源類型評估該策略。</span><span class="sxs-lookup"><span data-stu-id="f37b6-124">This command creates a policy definition named TagsPolicyDefinition with mode "Indexed" indicating the policy should be evaluated only for resource types that support tags and location.</span></span>

## <span data-ttu-id="f37b6-125">參數</span><span class="sxs-lookup"><span data-stu-id="f37b6-125">PARAMETERS</span></span>

### <span data-ttu-id="f37b6-126">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="f37b6-126">-ApiVersion</span></span>
<span data-ttu-id="f37b6-127">指定要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="f37b6-127">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="f37b6-128">如果您未指定版本，此 Cmdlet 會使用最新的可用版本。</span><span class="sxs-lookup"><span data-stu-id="f37b6-128">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="f37b6-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f37b6-129">-DefaultProfile</span></span>
<span data-ttu-id="f37b6-130">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="f37b6-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f37b6-131">-描述</span><span class="sxs-lookup"><span data-stu-id="f37b6-131">-Description</span></span>
<span data-ttu-id="f37b6-132">指定策略定義的描述。</span><span class="sxs-lookup"><span data-stu-id="f37b6-132">Specifies a description for the policy definition.</span></span>

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

### <span data-ttu-id="f37b6-133">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="f37b6-133">-DisplayName</span></span>
<span data-ttu-id="f37b6-134">指定策略定義的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="f37b6-134">Specifies a display name for the policy definition.</span></span>

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

### <span data-ttu-id="f37b6-135">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="f37b6-135">-ManagementGroupName</span></span>
<span data-ttu-id="f37b6-136">新策略定義的管理組名。</span><span class="sxs-lookup"><span data-stu-id="f37b6-136">The name of the management group of the new policy definition.</span></span>

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

### <span data-ttu-id="f37b6-137">-中繼資料</span><span class="sxs-lookup"><span data-stu-id="f37b6-137">-Metadata</span></span>
<span data-ttu-id="f37b6-138">用於定義策略的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="f37b6-138">The metadata for policy definition.</span></span> <span data-ttu-id="f37b6-139">這可以是包含中繼資料之檔案名的路徑，或中繼資料為字串</span><span class="sxs-lookup"><span data-stu-id="f37b6-139">This can either be a path to a file name containing the metadata, or the metadata as string</span></span>

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

### <span data-ttu-id="f37b6-140">-模式</span><span class="sxs-lookup"><span data-stu-id="f37b6-140">-Mode</span></span>
<span data-ttu-id="f37b6-141">策略定義的模式</span><span class="sxs-lookup"><span data-stu-id="f37b6-141">The mode of the policy definition</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: All
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f37b6-142">-名稱</span><span class="sxs-lookup"><span data-stu-id="f37b6-142">-Name</span></span>
<span data-ttu-id="f37b6-143">指定策略定義的名稱。</span><span class="sxs-lookup"><span data-stu-id="f37b6-143">Specifies a name for the policy definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f37b6-144">-Parameter</span><span class="sxs-lookup"><span data-stu-id="f37b6-144">-Parameter</span></span>
<span data-ttu-id="f37b6-145">原則定義的參數宣告。</span><span class="sxs-lookup"><span data-stu-id="f37b6-145">The parameters declaration for policy definition.</span></span> <span data-ttu-id="f37b6-146">這可以是包含參數宣告的檔案名路徑，或參數宣告為字串。</span><span class="sxs-lookup"><span data-stu-id="f37b6-146">This can either be a path to a file name containing the parameters declaration, or the parameters declaration as string.</span></span>

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

### <span data-ttu-id="f37b6-147">-策略</span><span class="sxs-lookup"><span data-stu-id="f37b6-147">-Policy</span></span>
<span data-ttu-id="f37b6-148">指定原則定義原則規則。</span><span class="sxs-lookup"><span data-stu-id="f37b6-148">Specifies a policy rule for the policy definition.</span></span>
<span data-ttu-id="f37b6-149">您可以指定 .json 檔案的路徑或包含 JSON 格式之策略的字串。</span><span class="sxs-lookup"><span data-stu-id="f37b6-149">You can specify the path of a .json file or a string that contains the policy in JSON format.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f37b6-150">-Pre</span><span class="sxs-lookup"><span data-stu-id="f37b6-150">-Pre</span></span>
<span data-ttu-id="f37b6-151">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮測試版 API 版本。</span><span class="sxs-lookup"><span data-stu-id="f37b6-151">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="f37b6-152">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f37b6-152">-SubscriptionId</span></span>
<span data-ttu-id="f37b6-153">新政策定義的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="f37b6-153">The subscription ID of the new policy definition.</span></span>

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

### <span data-ttu-id="f37b6-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f37b6-154">CommonParameters</span></span>
<span data-ttu-id="f37b6-155">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f37b6-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f37b6-156">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f37b6-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f37b6-157">輸入</span><span class="sxs-lookup"><span data-stu-id="f37b6-157">INPUTS</span></span>

### <span data-ttu-id="f37b6-158">System.String</span><span class="sxs-lookup"><span data-stu-id="f37b6-158">System.String</span></span>

### <span data-ttu-id="f37b6-159">System.Nullable'1[[System.Guid， System.Private.CoreLib， Version=4.0.0.0， Culture=neutral， PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="f37b6-159">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="f37b6-160">輸出</span><span class="sxs-lookup"><span data-stu-id="f37b6-160">OUTPUTS</span></span>

### <span data-ttu-id="f37b6-161">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="f37b6-161">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="f37b6-162">筆記</span><span class="sxs-lookup"><span data-stu-id="f37b6-162">NOTES</span></span>

## <span data-ttu-id="f37b6-163">相關連結</span><span class="sxs-lookup"><span data-stu-id="f37b6-163">RELATED LINKS</span></span>

[<span data-ttu-id="f37b6-164">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f37b6-164">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="f37b6-165">Remove-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f37b6-165">Remove-AzPolicyDefinition</span></span>](./Remove-AzPolicyDefinition.md)

[<span data-ttu-id="f37b6-166">Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f37b6-166">Set-AzPolicyDefinition</span></span>](./Set-AzPolicyDefinition.md)


