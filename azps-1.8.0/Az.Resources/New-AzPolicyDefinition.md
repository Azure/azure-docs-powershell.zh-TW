---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 31F2AF24-488D-4CAF-A9C8-C8DAE76E031F
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicyDefinition.md
ms.openlocfilehash: 07882064fae3cfc4a24899b6106480551f3681a8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93620833"
---
# <span data-ttu-id="42e49-101">New-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="42e49-101">New-AzPolicyDefinition</span></span>

## <span data-ttu-id="42e49-102">摘要</span><span class="sxs-lookup"><span data-stu-id="42e49-102">SYNOPSIS</span></span>
<span data-ttu-id="42e49-103">建立原則定義。</span><span class="sxs-lookup"><span data-stu-id="42e49-103">Creates a policy definition.</span></span>

## <span data-ttu-id="42e49-104">句法</span><span class="sxs-lookup"><span data-stu-id="42e49-104">SYNTAX</span></span>

### <span data-ttu-id="42e49-105">NameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="42e49-105">NameParameterSet (Default)</span></span>
```
New-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] -Policy <String>
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="42e49-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="42e49-106">ManagementGroupNameParameterSet</span></span>
```
New-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] -Policy <String>
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] -ManagementGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="42e49-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="42e49-107">SubscriptionIdParameterSet</span></span>
```
New-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] -Policy <String>
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] -SubscriptionId <Guid> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="42e49-108">說明</span><span class="sxs-lookup"><span data-stu-id="42e49-108">DESCRIPTION</span></span>
<span data-ttu-id="42e49-109">**AzPolicyDefinition** Cmdlet 會建立原則定義，其中包含 JavaScript) 格式 (JSON 物件符號中的原則規則。</span><span class="sxs-lookup"><span data-stu-id="42e49-109">The **New-AzPolicyDefinition** cmdlet creates a policy definition that includes a policy rule in JavaScript Object Notation (JSON) format.</span></span>

## <span data-ttu-id="42e49-110">示例</span><span class="sxs-lookup"><span data-stu-id="42e49-110">EXAMPLES</span></span>

### <span data-ttu-id="42e49-111">範例1：使用原則檔建立原則定義</span><span class="sxs-lookup"><span data-stu-id="42e49-111">Example 1: Create a policy definition by using a policy file</span></span>
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

<span data-ttu-id="42e49-112">這個命令會建立一個名為 LocationDefinition 的原則定義，其中包含 C:\LocationPolicy.json 中指定的原則規則。</span><span class="sxs-lookup"><span data-stu-id="42e49-112">This command creates a policy definition named LocationDefinition that contains the policy rule specified in C:\LocationPolicy.json.</span></span> <span data-ttu-id="42e49-113">上面提供了檔案 LocationPolicy.js的範例內容。</span><span class="sxs-lookup"><span data-stu-id="42e49-113">Example content for the LocationPolicy.json file is provided above.</span></span>

### <span data-ttu-id="42e49-114">範例2：使用內聯參數建立參數化原則定義</span><span class="sxs-lookup"><span data-stu-id="42e49-114">Example 2: Create a parameterized policy definition using inline parameters</span></span>
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

<span data-ttu-id="42e49-115">這個命令會建立一個名為 LocationDefinition 的原則定義，其中包含 C:\LocationPolicy.json 中指定的原則規則。</span><span class="sxs-lookup"><span data-stu-id="42e49-115">This command creates a policy definition named LocationDefinition that contains the policy rule specified in C:\LocationPolicy.json.</span></span> <span data-ttu-id="42e49-116">原則規則的參數定義是內嵌提供的。</span><span class="sxs-lookup"><span data-stu-id="42e49-116">The parameter definition for the policy rule is provided inline.</span></span>

### <span data-ttu-id="42e49-117">範例3：在管理群組中內嵌建立原則定義</span><span class="sxs-lookup"><span data-stu-id="42e49-117">Example 3: Create a policy definition inline in a management group</span></span>
```
PS C:\> New-AzPolicyDefinition -Name 'VMPolicyDefinition' -ManagementGroupName Dept42 -DisplayName 'Virtual Machine policy definition' -Policy '{"if":{"source":"action","equals":"Microsoft.Compute/virtualMachines/write"},"then":{"effect":"deny"}}'
```

<span data-ttu-id="42e49-118">這個命令會在管理群組 Dept42 中建立名為 VMPolicyDefinition 的原則定義。</span><span class="sxs-lookup"><span data-stu-id="42e49-118">This command creates a policy definition named VMPolicyDefinition in management group Dept42.</span></span>
<span data-ttu-id="42e49-119">該命令會將原則指定為有效 JSON 格式的字串。</span><span class="sxs-lookup"><span data-stu-id="42e49-119">The command specifies the policy as a string in valid JSON format.</span></span>

### <span data-ttu-id="42e49-120">範例4：以中繼資料內嵌建立原則定義</span><span class="sxs-lookup"><span data-stu-id="42e49-120">Example 4: Create a policy definition inline with metadata</span></span>
```
PS C:\> New-AzPolicyDefinition -Name 'VMPolicyDefinition' -Metadata '{"Category":"Virtual Machine"}' -Policy '{"if":{"source":"action","equals":"Microsoft.Compute/virtualMachines/write"},"then":{"effect":"deny"}}'


Name               : VMPolicyDefinition
ResourceId         : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policyDefinitions/VMPolicyDefinition
ResourceName       : VMPolicyDefinition
ResourceType       : Microsoft.Authorization/policyDefinitions
SubscriptionId     : 11111111-1111-1111-1111-111111111111
Properties         : @{displayName=VMPolicyDefinition; policyType=Custom; mode=All; metadata=; policyRule=}
PolicyDefinitionId : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policyDefinitions/VMPolicyDefinition
```

<span data-ttu-id="42e49-121">這個命令會建立名為 VMPolicyDefinition 的原則定義，其中繼資料指出其類別是 "虛擬機器"。</span><span class="sxs-lookup"><span data-stu-id="42e49-121">This command creates a policy definition named VMPolicyDefinition with metadata indicating its category is "Virtual Machine".</span></span>
<span data-ttu-id="42e49-122">該命令會將原則指定為有效 JSON 格式的字串。</span><span class="sxs-lookup"><span data-stu-id="42e49-122">The command specifies the policy as a string in valid JSON format.</span></span>

## <span data-ttu-id="42e49-123">參數</span><span class="sxs-lookup"><span data-stu-id="42e49-123">PARAMETERS</span></span>

### <span data-ttu-id="42e49-124">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="42e49-124">-ApiVersion</span></span>
<span data-ttu-id="42e49-125">指定要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="42e49-125">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="42e49-126">如果您沒有指定版本，此 Cmdlet 會使用最新的可用版本。</span><span class="sxs-lookup"><span data-stu-id="42e49-126">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="42e49-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42e49-127">-DefaultProfile</span></span>
<span data-ttu-id="42e49-128">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="42e49-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="42e49-129">-描述</span><span class="sxs-lookup"><span data-stu-id="42e49-129">-Description</span></span>
<span data-ttu-id="42e49-130">指定原則定義的描述。</span><span class="sxs-lookup"><span data-stu-id="42e49-130">Specifies a description for the policy definition.</span></span>

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

### <span data-ttu-id="42e49-131">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="42e49-131">-DisplayName</span></span>
<span data-ttu-id="42e49-132">指定原則定義的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="42e49-132">Specifies a display name for the policy definition.</span></span>

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

### <span data-ttu-id="42e49-133">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="42e49-133">-ManagementGroupName</span></span>
<span data-ttu-id="42e49-134">新原則定義之管理群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="42e49-134">The name of the management group of the new policy definition.</span></span>

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

### <span data-ttu-id="42e49-135">-中繼資料</span><span class="sxs-lookup"><span data-stu-id="42e49-135">-Metadata</span></span>
<span data-ttu-id="42e49-136">原則定義的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="42e49-136">The metadata for policy definition.</span></span> <span data-ttu-id="42e49-137">這可以是包含中繼資料之檔案名的路徑，或以字串形式的中繼資料</span><span class="sxs-lookup"><span data-stu-id="42e49-137">This can either be a path to a file name containing the metadata, or the metadata as string</span></span>

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

### <span data-ttu-id="42e49-138">模式</span><span class="sxs-lookup"><span data-stu-id="42e49-138">-Mode</span></span>
<span data-ttu-id="42e49-139">原則定義的模式</span><span class="sxs-lookup"><span data-stu-id="42e49-139">The mode of the policy definition</span></span>

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

### <span data-ttu-id="42e49-140">-名稱</span><span class="sxs-lookup"><span data-stu-id="42e49-140">-Name</span></span>
<span data-ttu-id="42e49-141">指定原則定義的名稱。</span><span class="sxs-lookup"><span data-stu-id="42e49-141">Specifies a name for the policy definition.</span></span>

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

### <span data-ttu-id="42e49-142">-參數</span><span class="sxs-lookup"><span data-stu-id="42e49-142">-Parameter</span></span>
<span data-ttu-id="42e49-143">原則定義的參數宣告。</span><span class="sxs-lookup"><span data-stu-id="42e49-143">The parameters declaration for policy definition.</span></span> <span data-ttu-id="42e49-144">這可以是包含參數宣告之檔案名的路徑，或是參數宣告（字串）。</span><span class="sxs-lookup"><span data-stu-id="42e49-144">This can either be a path to a file name containing the parameters declaration, or the parameters declaration as string.</span></span>

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

### <span data-ttu-id="42e49-145">-原則</span><span class="sxs-lookup"><span data-stu-id="42e49-145">-Policy</span></span>
<span data-ttu-id="42e49-146">指定原則定義的原則規則。</span><span class="sxs-lookup"><span data-stu-id="42e49-146">Specifies a policy rule for the policy definition.</span></span>
<span data-ttu-id="42e49-147">您可以指定 json 檔案的路徑，或是包含 JSON 格式之原則的字串。</span><span class="sxs-lookup"><span data-stu-id="42e49-147">You can specify the path of a .json file or a string that contains the policy in JSON format.</span></span>

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

### <span data-ttu-id="42e49-148">-預先</span><span class="sxs-lookup"><span data-stu-id="42e49-148">-Pre</span></span>
<span data-ttu-id="42e49-149">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="42e49-149">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="42e49-150">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="42e49-150">-SubscriptionId</span></span>
<span data-ttu-id="42e49-151">新原則定義的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="42e49-151">The subscription ID of the new policy definition.</span></span>

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

### <span data-ttu-id="42e49-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42e49-152">CommonParameters</span></span>
<span data-ttu-id="42e49-153">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="42e49-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42e49-154">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="42e49-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42e49-155">輸入</span><span class="sxs-lookup"><span data-stu-id="42e49-155">INPUTS</span></span>

### <span data-ttu-id="42e49-156">System.object</span><span class="sxs-lookup"><span data-stu-id="42e49-156">System.String</span></span>

### <span data-ttu-id="42e49-157">"CoreLib" 1 [[System. Guid.empty]、[System.] = 4.0.0.0、Culture = 中性、PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="42e49-157">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="42e49-158">輸出</span><span class="sxs-lookup"><span data-stu-id="42e49-158">OUTPUTS</span></span>

### <span data-ttu-id="42e49-159">系統管理. PSObject</span><span class="sxs-lookup"><span data-stu-id="42e49-159">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="42e49-160">筆記</span><span class="sxs-lookup"><span data-stu-id="42e49-160">NOTES</span></span>

## <span data-ttu-id="42e49-161">相關連結</span><span class="sxs-lookup"><span data-stu-id="42e49-161">RELATED LINKS</span></span>

[<span data-ttu-id="42e49-162">AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="42e49-162">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="42e49-163">移除-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="42e49-163">Remove-AzPolicyDefinition</span></span>](./Remove-AzPolicyDefinition.md)

[<span data-ttu-id="42e49-164">Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="42e49-164">Set-AzPolicyDefinition</span></span>](./Set-AzPolicyDefinition.md)


