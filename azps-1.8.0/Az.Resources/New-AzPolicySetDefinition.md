---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicySetDefinition.md
ms.openlocfilehash: cf1f1993c58e9c87c36538199555e5ebd7c2175a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93620827"
---
# <span data-ttu-id="d70d5-101">New-AzPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="d70d5-101">New-AzPolicySetDefinition</span></span>

## <span data-ttu-id="d70d5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d70d5-102">SYNOPSIS</span></span>
<span data-ttu-id="d70d5-103">建立原則集定義。</span><span class="sxs-lookup"><span data-stu-id="d70d5-103">Creates a policy set definition.</span></span>

## <span data-ttu-id="d70d5-104">句法</span><span class="sxs-lookup"><span data-stu-id="d70d5-104">SYNTAX</span></span>

### <span data-ttu-id="d70d5-105">NameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="d70d5-105">NameParameterSet (Default)</span></span>
```
New-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Metadata <String>]
 -PolicyDefinition <String> [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d70d5-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d70d5-106">ManagementGroupNameParameterSet</span></span>
```
New-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Metadata <String>]
 -PolicyDefinition <String> [-Parameter <String>] -ManagementGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d70d5-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d70d5-107">SubscriptionIdParameterSet</span></span>
```
New-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Metadata <String>]
 -PolicyDefinition <String> [-Parameter <String>] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d70d5-108">說明</span><span class="sxs-lookup"><span data-stu-id="d70d5-108">DESCRIPTION</span></span>
<span data-ttu-id="d70d5-109">**新的-AzPolicySetDefinition** Cmdlet 會建立一個策略集定義。</span><span class="sxs-lookup"><span data-stu-id="d70d5-109">The **New-AzPolicySetDefinition** cmdlet creates a policy set definition.</span></span>

## <span data-ttu-id="d70d5-110">示例</span><span class="sxs-lookup"><span data-stu-id="d70d5-110">EXAMPLES</span></span>

### <span data-ttu-id="d70d5-111">範例1：使用原則集檔案建立原則集定義</span><span class="sxs-lookup"><span data-stu-id="d70d5-111">Example 1: Create a policy set definition by using a policy set file</span></span>
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
PS C:\> New-AzPolicySetDefinition -Name 'VMPolicyDefinition' -PolicyDefinition C:\VMPolicySet.json
```

<span data-ttu-id="d70d5-112">這個命令會建立一個名為 VMPolicyDefinition 的原則集定義，其中包含 C:\VMPolicy.json 中指定的原則定義。</span><span class="sxs-lookup"><span data-stu-id="d70d5-112">This command creates a policy set definition named VMPolicyDefinition that contains the policy definitions specified in C:\VMPolicy.json.</span></span> <span data-ttu-id="d70d5-113">上面提供了 VMPolicy.js的範例內容。</span><span class="sxs-lookup"><span data-stu-id="d70d5-113">Example content of the VMPolicy.json is provided above.</span></span>

### <span data-ttu-id="d70d5-114">範例2：建立參數化原則集定義</span><span class="sxs-lookup"><span data-stu-id="d70d5-114">Example 2: Create a parameterized policy set definition</span></span>
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
PS C:\> New-AzPolicySetDefinition -Name 'VMPolicyDefinition' -PolicyDefinition C:\VMPolicySet.json -Parameter '{ "buTagValue": { "type": "string" } }'
```

<span data-ttu-id="d70d5-115">這個命令會建立一個名為 VMPolicyDefinition 的參數化原則集定義，其中包含 C:\VMPolicy.js中指定的原則定義。</span><span class="sxs-lookup"><span data-stu-id="d70d5-115">This command creates a parameterized policy set definition named VMPolicyDefinition that contains the policy definitions specified in C:\VMPolicy.json.</span></span> <span data-ttu-id="d70d5-116">上面提供了 VMPolicy.js的範例內容。</span><span class="sxs-lookup"><span data-stu-id="d70d5-116">Example content of the VMPolicy.json is provided above.</span></span>

## <span data-ttu-id="d70d5-117">參數</span><span class="sxs-lookup"><span data-stu-id="d70d5-117">PARAMETERS</span></span>

### <span data-ttu-id="d70d5-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="d70d5-118">-ApiVersion</span></span>
<span data-ttu-id="d70d5-119">設定時，會指出要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="d70d5-119">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="d70d5-120">如果未指定，API 版本會自動決定為最新的可用。</span><span class="sxs-lookup"><span data-stu-id="d70d5-120">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="d70d5-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d70d5-121">-DefaultProfile</span></span>
<span data-ttu-id="d70d5-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="d70d5-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d70d5-123">-描述</span><span class="sxs-lookup"><span data-stu-id="d70d5-123">-Description</span></span>
<span data-ttu-id="d70d5-124">原則集定義的描述。</span><span class="sxs-lookup"><span data-stu-id="d70d5-124">The description for policy set definition.</span></span>

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

### <span data-ttu-id="d70d5-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="d70d5-125">-DisplayName</span></span>
<span data-ttu-id="d70d5-126">原則集定義的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="d70d5-126">The display name for policy set definition.</span></span>

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

### <span data-ttu-id="d70d5-127">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="d70d5-127">-ManagementGroupName</span></span>
<span data-ttu-id="d70d5-128">新策略集定義之管理群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d70d5-128">The name of the management group of the new policy set definition.</span></span>

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

### <span data-ttu-id="d70d5-129">-中繼資料</span><span class="sxs-lookup"><span data-stu-id="d70d5-129">-Metadata</span></span>
<span data-ttu-id="d70d5-130">原則集定義的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="d70d5-130">The metadata for policy set definition.</span></span> <span data-ttu-id="d70d5-131">這可以是包含中繼資料之檔案名的路徑，或以字串形式的中繼資料</span><span class="sxs-lookup"><span data-stu-id="d70d5-131">This can either be a path to a file name containing the metadata, or the metadata as string</span></span>

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

### <span data-ttu-id="d70d5-132">-名稱</span><span class="sxs-lookup"><span data-stu-id="d70d5-132">-Name</span></span>
<span data-ttu-id="d70d5-133">原則集定義名稱。</span><span class="sxs-lookup"><span data-stu-id="d70d5-133">The policy set definition name.</span></span>

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

### <span data-ttu-id="d70d5-134">-參數</span><span class="sxs-lookup"><span data-stu-id="d70d5-134">-Parameter</span></span>
<span data-ttu-id="d70d5-135">原則集定義的參數宣告。</span><span class="sxs-lookup"><span data-stu-id="d70d5-135">The parameters declaration for policy set definition.</span></span>
<span data-ttu-id="d70d5-136">這可以是包含參數宣告之檔案名的路徑，或是參數宣告（字串）。</span><span class="sxs-lookup"><span data-stu-id="d70d5-136">This can either be a path to a file name containing the parameters declaration, or the parameters declaration as string.</span></span>

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

### <span data-ttu-id="d70d5-137">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="d70d5-137">-PolicyDefinition</span></span>
<span data-ttu-id="d70d5-138">原則集定義。</span><span class="sxs-lookup"><span data-stu-id="d70d5-138">The policy set definition.</span></span> <span data-ttu-id="d70d5-139">這可以是包含原則定義的檔案名路徑，或原則集定義（字串）。</span><span class="sxs-lookup"><span data-stu-id="d70d5-139">This can either be a path to a file name containing the policy definitions, or the policy set definition as string.</span></span>

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

### <span data-ttu-id="d70d5-140">-預先</span><span class="sxs-lookup"><span data-stu-id="d70d5-140">-Pre</span></span>
<span data-ttu-id="d70d5-141">設定時，表示 Cmdlet 應該使用預發行 API 版本，以便自動判斷要使用的版本。</span><span class="sxs-lookup"><span data-stu-id="d70d5-141">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="d70d5-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d70d5-142">-SubscriptionId</span></span>
<span data-ttu-id="d70d5-143">新原則集定義的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="d70d5-143">The subscription ID of the new policy set definition.</span></span>

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

### <span data-ttu-id="d70d5-144">-確認</span><span class="sxs-lookup"><span data-stu-id="d70d5-144">-Confirm</span></span>
<span data-ttu-id="d70d5-145">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d70d5-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d70d5-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d70d5-146">-WhatIf</span></span>
<span data-ttu-id="d70d5-147">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d70d5-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d70d5-148">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d70d5-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d70d5-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d70d5-149">CommonParameters</span></span>
<span data-ttu-id="d70d5-150">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d70d5-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d70d5-151">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d70d5-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d70d5-152">輸入</span><span class="sxs-lookup"><span data-stu-id="d70d5-152">INPUTS</span></span>

### <span data-ttu-id="d70d5-153">System.object</span><span class="sxs-lookup"><span data-stu-id="d70d5-153">System.String</span></span>

### <span data-ttu-id="d70d5-154">"CoreLib" 1 [[System. Guid.empty]、[System.] = 4.0.0.0、Culture = 中性、PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="d70d5-154">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="d70d5-155">輸出</span><span class="sxs-lookup"><span data-stu-id="d70d5-155">OUTPUTS</span></span>

### <span data-ttu-id="d70d5-156">系統管理. PSObject</span><span class="sxs-lookup"><span data-stu-id="d70d5-156">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="d70d5-157">筆記</span><span class="sxs-lookup"><span data-stu-id="d70d5-157">NOTES</span></span>

## <span data-ttu-id="d70d5-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="d70d5-158">RELATED LINKS</span></span>
