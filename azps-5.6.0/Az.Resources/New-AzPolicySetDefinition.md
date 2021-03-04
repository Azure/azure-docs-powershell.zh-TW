---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/new-azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicySetDefinition.md
ms.openlocfilehash: ae1cc96cd617ec74a69fc2c95ec50973e688ebe9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913117"
---
# <span data-ttu-id="f2e50-101">New-AzPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="f2e50-101">New-AzPolicySetDefinition</span></span>

## <span data-ttu-id="f2e50-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f2e50-102">SYNOPSIS</span></span>
<span data-ttu-id="f2e50-103">建立一個策略集定義。</span><span class="sxs-lookup"><span data-stu-id="f2e50-103">Creates a policy set definition.</span></span>

## <span data-ttu-id="f2e50-104">語法</span><span class="sxs-lookup"><span data-stu-id="f2e50-104">SYNTAX</span></span>

### <span data-ttu-id="f2e50-105">NameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="f2e50-105">NameParameterSet (Default)</span></span>
```
New-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Metadata <String>]
 -PolicyDefinition <String> [-Parameter <String>] [-GroupDefinition <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2e50-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f2e50-106">ManagementGroupNameParameterSet</span></span>
```
New-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Metadata <String>]
 -PolicyDefinition <String> [-Parameter <String>] -ManagementGroupName <String> [-GroupDefinition <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f2e50-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f2e50-107">SubscriptionIdParameterSet</span></span>
```
New-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Metadata <String>]
 -PolicyDefinition <String> [-Parameter <String>] -SubscriptionId <Guid> [-GroupDefinition <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f2e50-108">描述</span><span class="sxs-lookup"><span data-stu-id="f2e50-108">DESCRIPTION</span></span>
<span data-ttu-id="f2e50-109">**New-AzPolicySetDefinition** Cmdlet 會建立一個策略集定義。</span><span class="sxs-lookup"><span data-stu-id="f2e50-109">The **New-AzPolicySetDefinition** cmdlet creates a policy set definition.</span></span>

## <span data-ttu-id="f2e50-110">例子</span><span class="sxs-lookup"><span data-stu-id="f2e50-110">EXAMPLES</span></span>

### <span data-ttu-id="f2e50-111">範例 1：使用策略集檔案建立包含中繼資料的組定義</span><span class="sxs-lookup"><span data-stu-id="f2e50-111">Example 1: Create a policy set definition with metadata by using a policy set file</span></span>
```
[
   {
      "policyDefinitionId": "/providers/Microsoft.Authorization/policyDefinitions/2a0e14a6-b0a6-4fab-991a-187a4f81c498",
      "parameters": {
         "tagName": {
            "value": "Business Unit"
         },
         "tagValue": {
            "value": "Finance"
         }
      }
   },
   {
      "policyDefinitionId": "/providers/Microsoft.Authorization/policyDefinitions/464dbb85-3d5f-4a1d-bb09-95a9b5dd19cf"
   }
]
```

```
PS C:\> New-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -Metadata '{"category":"Virtual Machine"}' -PolicyDefinition C:\VMPolicySet.json
```

<span data-ttu-id="f2e50-112">此命令會建立名為 VMPolicySetDefinition 的一個策略集定義，其中中繼資料指出其類別為「虛擬機器」，其中包含 C:\VMPolicy.js中指定的規則定義。</span><span class="sxs-lookup"><span data-stu-id="f2e50-112">This command creates a policy set definition named VMPolicySetDefinition with metadata indicating its category is "Virtual Machine" that contains the policy definitions specified in C:\VMPolicy.json.</span></span> <span data-ttu-id="f2e50-113">上方提供VMPolicy.js的範例內容。</span><span class="sxs-lookup"><span data-stu-id="f2e50-113">Example content of the VMPolicy.json is provided above.</span></span>

### <span data-ttu-id="f2e50-114">範例 2：建立參數化策略集定義</span><span class="sxs-lookup"><span data-stu-id="f2e50-114">Example 2: Create a parameterized policy set definition</span></span>
```
[
   {
      "policyDefinitionId": "/providers/Microsoft.Authorization/policyDefinitions/2a0e14a6-b0a6-4fab-991a-187a4f81c498",
      "parameters": {
         "tagName": {
            "value": "Business Unit"
         },
         "tagValue": {
            "value": "[parameters('buTagValue')]"
         }
      }
   },
   {
      "policyDefinitionId": "/providers/Microsoft.Authorization/policyDefinitions/464dbb85-3d5f-4a1d-bb09-95a9b5dd19cf"
   }
]
```

```
PS C:\> New-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -PolicyDefinition C:\VMPolicySet.json -Parameter '{ "buTagValue": { "type": "string" } }'
```

<span data-ttu-id="f2e50-115">此命令會建立名為 VMPolicySetDefinition 的參數化C:\VMPolicy.js定義。</span><span class="sxs-lookup"><span data-stu-id="f2e50-115">This command creates a parameterized policy set definition named VMPolicySetDefinition that contains the policy definitions specified in C:\VMPolicy.json.</span></span> <span data-ttu-id="f2e50-116">上方提供VMPolicy.js的範例內容。</span><span class="sxs-lookup"><span data-stu-id="f2e50-116">Example content of the VMPolicy.json is provided above.</span></span>

### <span data-ttu-id="f2e50-117">範例 3：使用策略定義群組建立一個策略集定義</span><span class="sxs-lookup"><span data-stu-id="f2e50-117">Example 3: Create a policy set definition with policy definition groups</span></span>
```
[
   {
      "policyDefinitionId": "/providers/Microsoft.Authorization/policyDefinitions/2a0e14a6-b0a6-4fab-991a-187a4f81c498",
      "groupNames": [ "group1" ]
   },
   {
      "policyDefinitionId": "/providers/Microsoft.Authorization/policyDefinitions/464dbb85-3d5f-4a1d-bb09-95a9b5dd19cf",
      "groupNames": [ "group2" ]
   }
]
```

```
$groupsJson = ConvertTo-Json @{ name = "group1" }, @{ name = "group2" }
PS C:\> New-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -GroupDefinition $groupsJson -PolicyDefinition C:\VMPolicySet.json
```

<span data-ttu-id="f2e50-118">此命令會建立一個名為 VMPolicySetDefinition 與群組原則定義組在C:\VMPolicy.js定義。</span><span class="sxs-lookup"><span data-stu-id="f2e50-118">This command creates a policy set definition named VMPolicySetDefinition with grouping of policy definitions specified in C:\VMPolicy.json.</span></span> <span data-ttu-id="f2e50-119">上方提供VMPolicy.js的範例內容。</span><span class="sxs-lookup"><span data-stu-id="f2e50-119">Example content of the VMPolicy.json is provided above.</span></span>

## <span data-ttu-id="f2e50-120">參數</span><span class="sxs-lookup"><span data-stu-id="f2e50-120">PARAMETERS</span></span>

### <span data-ttu-id="f2e50-121">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="f2e50-121">-ApiVersion</span></span>
<span data-ttu-id="f2e50-122">設定時，表示要使用資源提供者 API 的版本。</span><span class="sxs-lookup"><span data-stu-id="f2e50-122">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="f2e50-123">如果未指定，API 版本會自動判斷為最新可用。</span><span class="sxs-lookup"><span data-stu-id="f2e50-123">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="f2e50-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2e50-124">-DefaultProfile</span></span>
<span data-ttu-id="f2e50-125">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="f2e50-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f2e50-126">-描述</span><span class="sxs-lookup"><span data-stu-id="f2e50-126">-Description</span></span>
<span data-ttu-id="f2e50-127">策略集定義的描述。</span><span class="sxs-lookup"><span data-stu-id="f2e50-127">The description for policy set definition.</span></span>

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

### <span data-ttu-id="f2e50-128">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="f2e50-128">-DisplayName</span></span>
<span data-ttu-id="f2e50-129">策略集定義的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="f2e50-129">The display name for policy set definition.</span></span>

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

### <span data-ttu-id="f2e50-130">-GroupDefinition</span><span class="sxs-lookup"><span data-stu-id="f2e50-130">-GroupDefinition</span></span>
<span data-ttu-id="f2e50-131">新策略集定義之策略定義群組。</span><span class="sxs-lookup"><span data-stu-id="f2e50-131">The policy definition groups for the new policy set definition.</span></span> <span data-ttu-id="f2e50-132">這可以是包含群組之檔案的路徑，或群組為 JSON 字串。</span><span class="sxs-lookup"><span data-stu-id="f2e50-132">This can either be a path to a file containing the groups, or the groups as a JSON string.</span></span>

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

### <span data-ttu-id="f2e50-133">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="f2e50-133">-ManagementGroupName</span></span>
<span data-ttu-id="f2e50-134">新策略集定義之管理組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f2e50-134">The name of the management group of the new policy set definition.</span></span>

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

### <span data-ttu-id="f2e50-135">-中繼資料</span><span class="sxs-lookup"><span data-stu-id="f2e50-135">-Metadata</span></span>
<span data-ttu-id="f2e50-136">設定定義之中繼資料。</span><span class="sxs-lookup"><span data-stu-id="f2e50-136">The metadata for policy set definition.</span></span> <span data-ttu-id="f2e50-137">這可以是包含中繼資料之檔案名的路徑，或是 JSON 字串的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="f2e50-137">This can either be a path to a file name containing the metadata, or the metadata as a JSON string.</span></span>

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

### <span data-ttu-id="f2e50-138">-名稱</span><span class="sxs-lookup"><span data-stu-id="f2e50-138">-Name</span></span>
<span data-ttu-id="f2e50-139">該策略集定義名稱。</span><span class="sxs-lookup"><span data-stu-id="f2e50-139">The policy set definition name.</span></span>

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

### <span data-ttu-id="f2e50-140">-Parameter</span><span class="sxs-lookup"><span data-stu-id="f2e50-140">-Parameter</span></span>
<span data-ttu-id="f2e50-141">原則集定義的參數宣告。</span><span class="sxs-lookup"><span data-stu-id="f2e50-141">The parameters declaration for policy set definition.</span></span>
<span data-ttu-id="f2e50-142">這可以是包含參數宣告的檔案名路徑，或參數宣告為 JSON 字串。</span><span class="sxs-lookup"><span data-stu-id="f2e50-142">This can either be a path to a file name containing the parameters declaration, or the parameters declaration as a JSON string.</span></span>

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

### <span data-ttu-id="f2e50-143">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f2e50-143">-PolicyDefinition</span></span>
<span data-ttu-id="f2e50-144">該政策定義。</span><span class="sxs-lookup"><span data-stu-id="f2e50-144">The policy definitions.</span></span> <span data-ttu-id="f2e50-145">這可以是包含策略定義的檔案名路徑，或 JSON 字串中的策略定義。</span><span class="sxs-lookup"><span data-stu-id="f2e50-145">This can either be a path to a file name containing the policy definitions, or the policy definitions as a JSON string.</span></span>

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

### <span data-ttu-id="f2e50-146">-Pre</span><span class="sxs-lookup"><span data-stu-id="f2e50-146">-Pre</span></span>
<span data-ttu-id="f2e50-147">設定之後，表示當系統自動決定要使用哪個版本時，Cmdlet 應該使用測試版 API 版本。</span><span class="sxs-lookup"><span data-stu-id="f2e50-147">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="f2e50-148">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f2e50-148">-SubscriptionId</span></span>
<span data-ttu-id="f2e50-149">新策略集定義的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="f2e50-149">The subscription ID of the new policy set definition.</span></span>

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

### <span data-ttu-id="f2e50-150">-確認</span><span class="sxs-lookup"><span data-stu-id="f2e50-150">-Confirm</span></span>
<span data-ttu-id="f2e50-151">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="f2e50-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2e50-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2e50-152">-WhatIf</span></span>
<span data-ttu-id="f2e50-153">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f2e50-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f2e50-154">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f2e50-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2e50-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2e50-155">CommonParameters</span></span>
<span data-ttu-id="f2e50-156">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f2e50-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2e50-157">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f2e50-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2e50-158">輸入</span><span class="sxs-lookup"><span data-stu-id="f2e50-158">INPUTS</span></span>

### <span data-ttu-id="f2e50-159">System.String</span><span class="sxs-lookup"><span data-stu-id="f2e50-159">System.String</span></span>

### <span data-ttu-id="f2e50-160">System.Nullable'1[[System.Guid， System.Private.CoreLib， Version=4.0.0.0， Culture=neutral， PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="f2e50-160">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="f2e50-161">輸出</span><span class="sxs-lookup"><span data-stu-id="f2e50-161">OUTPUTS</span></span>

### <span data-ttu-id="f2e50-162">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="f2e50-162">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="f2e50-163">筆記</span><span class="sxs-lookup"><span data-stu-id="f2e50-163">NOTES</span></span>

## <span data-ttu-id="f2e50-164">相關連結</span><span class="sxs-lookup"><span data-stu-id="f2e50-164">RELATED LINKS</span></span>
