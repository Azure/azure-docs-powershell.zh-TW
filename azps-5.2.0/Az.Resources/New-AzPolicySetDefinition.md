---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicySetDefinition.md
ms.openlocfilehash: 1a4a2579b05c60133fa1b0f7ab057be602965eaa
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98281484"
---
# <span data-ttu-id="66180-101">New-AzPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="66180-101">New-AzPolicySetDefinition</span></span>

## <span data-ttu-id="66180-102">摘要</span><span class="sxs-lookup"><span data-stu-id="66180-102">SYNOPSIS</span></span>
<span data-ttu-id="66180-103">建立原則集定義。</span><span class="sxs-lookup"><span data-stu-id="66180-103">Creates a policy set definition.</span></span>

## <span data-ttu-id="66180-104">句法</span><span class="sxs-lookup"><span data-stu-id="66180-104">SYNTAX</span></span>

### <span data-ttu-id="66180-105">NameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="66180-105">NameParameterSet (Default)</span></span>
```
New-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Metadata <String>]
 -PolicyDefinition <String> [-Parameter <String>] [-GroupDefinition <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66180-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="66180-106">ManagementGroupNameParameterSet</span></span>
```
New-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Metadata <String>]
 -PolicyDefinition <String> [-Parameter <String>] -ManagementGroupName <String> [-GroupDefinition <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="66180-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="66180-107">SubscriptionIdParameterSet</span></span>
```
New-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Metadata <String>]
 -PolicyDefinition <String> [-Parameter <String>] -SubscriptionId <Guid> [-GroupDefinition <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="66180-108">說明</span><span class="sxs-lookup"><span data-stu-id="66180-108">DESCRIPTION</span></span>
<span data-ttu-id="66180-109">**新的-AzPolicySetDefinition** Cmdlet 會建立一個策略集定義。</span><span class="sxs-lookup"><span data-stu-id="66180-109">The **New-AzPolicySetDefinition** cmdlet creates a policy set definition.</span></span>

## <span data-ttu-id="66180-110">示例</span><span class="sxs-lookup"><span data-stu-id="66180-110">EXAMPLES</span></span>

### <span data-ttu-id="66180-111">範例1：使用原則集檔案建立含中繼資料的原則集定義</span><span class="sxs-lookup"><span data-stu-id="66180-111">Example 1: Create a policy set definition with metadata by using a policy set file</span></span>
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

<span data-ttu-id="66180-112">這個命令會建立一個名為 VMPolicySetDefinition 的原則集定義，其中繼資料指出其類別是「虛擬機器」，其中包含 C:\VMPolicy.js的中所指定的原則定義。</span><span class="sxs-lookup"><span data-stu-id="66180-112">This command creates a policy set definition named VMPolicySetDefinition with metadata indicating its category is "Virtual Machine" that contains the policy definitions specified in C:\VMPolicy.json.</span></span> <span data-ttu-id="66180-113">上面提供了 VMPolicy.js的範例內容。</span><span class="sxs-lookup"><span data-stu-id="66180-113">Example content of the VMPolicy.json is provided above.</span></span>

### <span data-ttu-id="66180-114">範例2：建立參數化原則集定義</span><span class="sxs-lookup"><span data-stu-id="66180-114">Example 2: Create a parameterized policy set definition</span></span>
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

<span data-ttu-id="66180-115">這個命令會建立一個名為 VMPolicySetDefinition 的參數化原則集定義，其中包含 C:\VMPolicy.js中指定的原則定義。</span><span class="sxs-lookup"><span data-stu-id="66180-115">This command creates a parameterized policy set definition named VMPolicySetDefinition that contains the policy definitions specified in C:\VMPolicy.json.</span></span> <span data-ttu-id="66180-116">上面提供了 VMPolicy.js的範例內容。</span><span class="sxs-lookup"><span data-stu-id="66180-116">Example content of the VMPolicy.json is provided above.</span></span>

### <span data-ttu-id="66180-117">範例3：使用原則定義群組建立原則集定義</span><span class="sxs-lookup"><span data-stu-id="66180-117">Example 3: Create a policy set definition with policy definition groups</span></span>
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

<span data-ttu-id="66180-118">這個命令會建立一個名為 VMPolicySetDefinition 的原則集定義，並將原則定義分組，並在 C:\VMPolicy.json] 上指定。</span><span class="sxs-lookup"><span data-stu-id="66180-118">This command creates a policy set definition named VMPolicySetDefinition with grouping of policy definitions specified in C:\VMPolicy.json.</span></span> <span data-ttu-id="66180-119">上面提供了 VMPolicy.js的範例內容。</span><span class="sxs-lookup"><span data-stu-id="66180-119">Example content of the VMPolicy.json is provided above.</span></span>

## <span data-ttu-id="66180-120">參數</span><span class="sxs-lookup"><span data-stu-id="66180-120">PARAMETERS</span></span>

### <span data-ttu-id="66180-121">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="66180-121">-ApiVersion</span></span>
<span data-ttu-id="66180-122">設定時，會指出要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="66180-122">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="66180-123">如果未指定，API 版本會自動決定為最新的可用。</span><span class="sxs-lookup"><span data-stu-id="66180-123">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="66180-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66180-124">-DefaultProfile</span></span>
<span data-ttu-id="66180-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="66180-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="66180-126">-描述</span><span class="sxs-lookup"><span data-stu-id="66180-126">-Description</span></span>
<span data-ttu-id="66180-127">原則集定義的描述。</span><span class="sxs-lookup"><span data-stu-id="66180-127">The description for policy set definition.</span></span>

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

### <span data-ttu-id="66180-128">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="66180-128">-DisplayName</span></span>
<span data-ttu-id="66180-129">原則集定義的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="66180-129">The display name for policy set definition.</span></span>

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

### <span data-ttu-id="66180-130">-GroupDefinition</span><span class="sxs-lookup"><span data-stu-id="66180-130">-GroupDefinition</span></span>
<span data-ttu-id="66180-131">新原則集定義的原則定義群組。</span><span class="sxs-lookup"><span data-stu-id="66180-131">The policy definition groups for the new policy set definition.</span></span> <span data-ttu-id="66180-132">這可以是包含群組之檔案的路徑，或作為 JSON 字串的群組。</span><span class="sxs-lookup"><span data-stu-id="66180-132">This can either be a path to a file containing the groups, or the groups as a JSON string.</span></span>

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

### <span data-ttu-id="66180-133">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="66180-133">-ManagementGroupName</span></span>
<span data-ttu-id="66180-134">新策略集定義之管理群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="66180-134">The name of the management group of the new policy set definition.</span></span>

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

### <span data-ttu-id="66180-135">-中繼資料</span><span class="sxs-lookup"><span data-stu-id="66180-135">-Metadata</span></span>
<span data-ttu-id="66180-136">原則集定義的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="66180-136">The metadata for policy set definition.</span></span> <span data-ttu-id="66180-137">這可以是包含中繼資料之檔案名的路徑，或作為 JSON 字串的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="66180-137">This can either be a path to a file name containing the metadata, or the metadata as a JSON string.</span></span>

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

### <span data-ttu-id="66180-138">-名稱</span><span class="sxs-lookup"><span data-stu-id="66180-138">-Name</span></span>
<span data-ttu-id="66180-139">原則集定義名稱。</span><span class="sxs-lookup"><span data-stu-id="66180-139">The policy set definition name.</span></span>

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

### <span data-ttu-id="66180-140">-參數</span><span class="sxs-lookup"><span data-stu-id="66180-140">-Parameter</span></span>
<span data-ttu-id="66180-141">原則集定義的參數宣告。</span><span class="sxs-lookup"><span data-stu-id="66180-141">The parameters declaration for policy set definition.</span></span>
<span data-ttu-id="66180-142">這可以是包含參數宣告之檔案名的路徑，或作為 JSON 字串的參數宣告。</span><span class="sxs-lookup"><span data-stu-id="66180-142">This can either be a path to a file name containing the parameters declaration, or the parameters declaration as a JSON string.</span></span>

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

### <span data-ttu-id="66180-143">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="66180-143">-PolicyDefinition</span></span>
<span data-ttu-id="66180-144">原則定義。</span><span class="sxs-lookup"><span data-stu-id="66180-144">The policy definitions.</span></span> <span data-ttu-id="66180-145">這可以是包含原則定義的檔案名路徑，或原則定義（JSON 字串）。</span><span class="sxs-lookup"><span data-stu-id="66180-145">This can either be a path to a file name containing the policy definitions, or the policy definitions as a JSON string.</span></span>

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

### <span data-ttu-id="66180-146">-預先</span><span class="sxs-lookup"><span data-stu-id="66180-146">-Pre</span></span>
<span data-ttu-id="66180-147">設定時，表示 Cmdlet 應該使用預發行 API 版本，以便自動判斷要使用的版本。</span><span class="sxs-lookup"><span data-stu-id="66180-147">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="66180-148">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="66180-148">-SubscriptionId</span></span>
<span data-ttu-id="66180-149">新原則集定義的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="66180-149">The subscription ID of the new policy set definition.</span></span>

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

### <span data-ttu-id="66180-150">-確認</span><span class="sxs-lookup"><span data-stu-id="66180-150">-Confirm</span></span>
<span data-ttu-id="66180-151">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="66180-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66180-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66180-152">-WhatIf</span></span>
<span data-ttu-id="66180-153">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="66180-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="66180-154">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="66180-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66180-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66180-155">CommonParameters</span></span>
<span data-ttu-id="66180-156">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="66180-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66180-157">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="66180-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66180-158">輸入</span><span class="sxs-lookup"><span data-stu-id="66180-158">INPUTS</span></span>

### <span data-ttu-id="66180-159">System.object</span><span class="sxs-lookup"><span data-stu-id="66180-159">System.String</span></span>

### <span data-ttu-id="66180-160">"CoreLib" 1 [[System. Guid.empty]、[System.] = 4.0.0.0、Culture = 中性、PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="66180-160">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="66180-161">輸出</span><span class="sxs-lookup"><span data-stu-id="66180-161">OUTPUTS</span></span>

### <span data-ttu-id="66180-162">系統管理. PSObject</span><span class="sxs-lookup"><span data-stu-id="66180-162">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="66180-163">筆記</span><span class="sxs-lookup"><span data-stu-id="66180-163">NOTES</span></span>

## <span data-ttu-id="66180-164">相關連結</span><span class="sxs-lookup"><span data-stu-id="66180-164">RELATED LINKS</span></span>
