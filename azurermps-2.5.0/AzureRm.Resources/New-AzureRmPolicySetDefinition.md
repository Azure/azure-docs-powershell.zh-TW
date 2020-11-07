---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermpolicysetdefinition
schema: 2.0.0
ms.openlocfilehash: 701c7e11a5b76b2071c5810f8c6948c6024eb1ae
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93801910"
---
# <span data-ttu-id="a8d3f-101">New-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="a8d3f-101">New-AzureRmPolicySetDefinition</span></span>

## <span data-ttu-id="a8d3f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a8d3f-102">SYNOPSIS</span></span>
<span data-ttu-id="a8d3f-103">建立原則集定義。</span><span class="sxs-lookup"><span data-stu-id="a8d3f-103">Creates a policy set definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a8d3f-104">句法</span><span class="sxs-lookup"><span data-stu-id="a8d3f-104">SYNTAX</span></span>

### <span data-ttu-id="a8d3f-105">NameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="a8d3f-105">NameParameterSet (Default)</span></span>
```
New-AzureRmPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] -PolicyDefinition <String> [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8d3f-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a8d3f-106">ManagementGroupNameParameterSet</span></span>
```
New-AzureRmPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] -PolicyDefinition <String> [-Parameter <String>] -ManagementGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a8d3f-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a8d3f-107">SubscriptionIdParameterSet</span></span>
```
New-AzureRmPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] -PolicyDefinition <String> [-Parameter <String>] -SubscriptionId <Guid>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a8d3f-108">說明</span><span class="sxs-lookup"><span data-stu-id="a8d3f-108">DESCRIPTION</span></span>
<span data-ttu-id="a8d3f-109">**新的-AzureRmPolicySetDefinition** Cmdlet 會建立一個策略集定義。</span><span class="sxs-lookup"><span data-stu-id="a8d3f-109">The **New-AzureRmPolicySetDefinition** cmdlet creates a policy set definition.</span></span>

## <span data-ttu-id="a8d3f-110">示例</span><span class="sxs-lookup"><span data-stu-id="a8d3f-110">EXAMPLES</span></span>

### <span data-ttu-id="a8d3f-111">範例1：使用原則集檔案建立原則集定義</span><span class="sxs-lookup"><span data-stu-id="a8d3f-111">Example 1: Create a policy set definition by using a policy set file</span></span>
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
PS C:\> New-AzureRmPolicySetDefinition -Name 'VMPolicyDefinition' -PolicyDefinition C:\VMPolicySet.json
```

<span data-ttu-id="a8d3f-112">這個命令會建立一個名為 VMPolicyDefinition 的原則集定義，其中包含 C:\VMPolicy.json 中指定的原則定義。</span><span class="sxs-lookup"><span data-stu-id="a8d3f-112">This command creates a policy set definition named VMPolicyDefinition that contains the policy definitions specified in C:\VMPolicy.json.</span></span> <span data-ttu-id="a8d3f-113">上面提供了 VMPolicy.js的範例內容。</span><span class="sxs-lookup"><span data-stu-id="a8d3f-113">Example content of the VMPolicy.json is provided above.</span></span>

### <span data-ttu-id="a8d3f-114">範例2：建立參數化原則集定義</span><span class="sxs-lookup"><span data-stu-id="a8d3f-114">Example 2: Create a parameterized policy set definition</span></span>
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
PS C:\> New-AzureRmPolicySetDefinition -Name 'VMPolicyDefinition' -PolicyDefinition C:\VMPolicySet.json -Parameter '{ "buTagValue": { "type": "string" } }'
```

<span data-ttu-id="a8d3f-115">這個命令會建立一個名為 VMPolicyDefinition 的參數化原則集定義，其中包含 C:\VMPolicy.js中指定的原則定義。</span><span class="sxs-lookup"><span data-stu-id="a8d3f-115">This command creates a parameterized policy set definition named VMPolicyDefinition that contains the policy definitions specified in C:\VMPolicy.json.</span></span> <span data-ttu-id="a8d3f-116">上面提供了 VMPolicy.js的範例內容。</span><span class="sxs-lookup"><span data-stu-id="a8d3f-116">Example content of the VMPolicy.json is provided above.</span></span>

## <span data-ttu-id="a8d3f-117">參數</span><span class="sxs-lookup"><span data-stu-id="a8d3f-117">PARAMETERS</span></span>

### <span data-ttu-id="a8d3f-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="a8d3f-118">-ApiVersion</span></span>
<span data-ttu-id="a8d3f-119">設定時，會指出要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="a8d3f-119">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="a8d3f-120">如果未指定，API 版本會自動決定為最新的可用。</span><span class="sxs-lookup"><span data-stu-id="a8d3f-120">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="a8d3f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8d3f-121">-DefaultProfile</span></span>
<span data-ttu-id="a8d3f-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="a8d3f-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a8d3f-123">-描述</span><span class="sxs-lookup"><span data-stu-id="a8d3f-123">-Description</span></span>
<span data-ttu-id="a8d3f-124">原則集定義的描述。</span><span class="sxs-lookup"><span data-stu-id="a8d3f-124">The description for policy set definition.</span></span>

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

### <span data-ttu-id="a8d3f-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="a8d3f-125">-DisplayName</span></span>
<span data-ttu-id="a8d3f-126">原則集定義的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="a8d3f-126">The display name for policy set definition.</span></span>

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

### <span data-ttu-id="a8d3f-127">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="a8d3f-127">-ManagementGroupName</span></span>
<span data-ttu-id="a8d3f-128">新策略集定義之管理群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a8d3f-128">The name of the management group of the new policy set definition.</span></span>

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

### <span data-ttu-id="a8d3f-129">-中繼資料</span><span class="sxs-lookup"><span data-stu-id="a8d3f-129">-Metadata</span></span>
<span data-ttu-id="a8d3f-130">原則集定義的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="a8d3f-130">The metadata for policy set definition.</span></span> <span data-ttu-id="a8d3f-131">這可以是包含中繼資料之檔案名的路徑，或以字串形式的中繼資料</span><span class="sxs-lookup"><span data-stu-id="a8d3f-131">This can either be a path to a file name containing the metadata, or the metadata as string</span></span>

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

### <span data-ttu-id="a8d3f-132">-名稱</span><span class="sxs-lookup"><span data-stu-id="a8d3f-132">-Name</span></span>
<span data-ttu-id="a8d3f-133">原則集定義名稱。</span><span class="sxs-lookup"><span data-stu-id="a8d3f-133">The policy set definition name.</span></span>

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

### <span data-ttu-id="a8d3f-134">-參數</span><span class="sxs-lookup"><span data-stu-id="a8d3f-134">-Parameter</span></span>
<span data-ttu-id="a8d3f-135">原則集定義的參數宣告。</span><span class="sxs-lookup"><span data-stu-id="a8d3f-135">The parameters declaration for policy set definition.</span></span>
<span data-ttu-id="a8d3f-136">這可以是包含參數宣告之檔案名的路徑，或是參數宣告（字串）。</span><span class="sxs-lookup"><span data-stu-id="a8d3f-136">This can either be a path to a file name containing the parameters declaration, or the parameters declaration as string.</span></span>

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

### <span data-ttu-id="a8d3f-137">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="a8d3f-137">-PolicyDefinition</span></span>
<span data-ttu-id="a8d3f-138">原則集定義。</span><span class="sxs-lookup"><span data-stu-id="a8d3f-138">The policy set definition.</span></span> <span data-ttu-id="a8d3f-139">這可以是包含原則定義的檔案名路徑，或原則集定義（字串）。</span><span class="sxs-lookup"><span data-stu-id="a8d3f-139">This can either be a path to a file name containing the policy definitions, or the policy set definition as string.</span></span>

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

### <span data-ttu-id="a8d3f-140">-預先</span><span class="sxs-lookup"><span data-stu-id="a8d3f-140">-Pre</span></span>
<span data-ttu-id="a8d3f-141">設定時，表示 Cmdlet 應該使用預發行 API 版本，以便自動判斷要使用的版本。</span><span class="sxs-lookup"><span data-stu-id="a8d3f-141">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="a8d3f-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a8d3f-142">-SubscriptionId</span></span>
<span data-ttu-id="a8d3f-143">新原則集定義的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="a8d3f-143">The subscription ID of the new policy set definition.</span></span>

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

### <span data-ttu-id="a8d3f-144">-確認</span><span class="sxs-lookup"><span data-stu-id="a8d3f-144">-Confirm</span></span>
<span data-ttu-id="a8d3f-145">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a8d3f-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8d3f-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8d3f-146">-WhatIf</span></span>
<span data-ttu-id="a8d3f-147">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a8d3f-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a8d3f-148">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a8d3f-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8d3f-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8d3f-149">CommonParameters</span></span>
<span data-ttu-id="a8d3f-150">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a8d3f-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8d3f-151">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a8d3f-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8d3f-152">輸入</span><span class="sxs-lookup"><span data-stu-id="a8d3f-152">INPUTS</span></span>

### <span data-ttu-id="a8d3f-153">System.object</span><span class="sxs-lookup"><span data-stu-id="a8d3f-153">System.String</span></span>

### <span data-ttu-id="a8d3f-154">系統. Nullable "1 [[System. Guid，mscorlib，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="a8d3f-154">System.Nullable\`1[[System.Guid, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="a8d3f-155">輸出</span><span class="sxs-lookup"><span data-stu-id="a8d3f-155">OUTPUTS</span></span>

### <span data-ttu-id="a8d3f-156">系統管理. PSObject</span><span class="sxs-lookup"><span data-stu-id="a8d3f-156">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="a8d3f-157">筆記</span><span class="sxs-lookup"><span data-stu-id="a8d3f-157">NOTES</span></span>

## <span data-ttu-id="a8d3f-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="a8d3f-158">RELATED LINKS</span></span>
