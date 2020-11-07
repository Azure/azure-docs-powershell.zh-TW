---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 31F2AF24-488D-4CAF-A9C8-C8DAE76E031F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermpolicydefinition
schema: 2.0.0
ms.openlocfilehash: 844c4d6af4d5ea0b11f0ae3e662bd2ba91957c1d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93801913"
---
# <span data-ttu-id="74b42-101">New-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="74b42-101">New-AzureRmPolicyDefinition</span></span>

## <span data-ttu-id="74b42-102">摘要</span><span class="sxs-lookup"><span data-stu-id="74b42-102">SYNOPSIS</span></span>
<span data-ttu-id="74b42-103">建立原則定義。</span><span class="sxs-lookup"><span data-stu-id="74b42-103">Creates a policy definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="74b42-104">句法</span><span class="sxs-lookup"><span data-stu-id="74b42-104">SYNTAX</span></span>

### <span data-ttu-id="74b42-105">NameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="74b42-105">NameParameterSet (Default)</span></span>
```
New-AzureRmPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] -Policy <String>
 [-Metadata <String>] [-Parameter <String>] [-Mode <PolicyDefinitionMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="74b42-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="74b42-106">ManagementGroupNameParameterSet</span></span>
```
New-AzureRmPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] -Policy <String>
 [-Metadata <String>] [-Parameter <String>] [-Mode <PolicyDefinitionMode>] -ManagementGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="74b42-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="74b42-107">SubscriptionIdParameterSet</span></span>
```
New-AzureRmPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] -Policy <String>
 [-Metadata <String>] [-Parameter <String>] [-Mode <PolicyDefinitionMode>] -SubscriptionId <Guid>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="74b42-108">說明</span><span class="sxs-lookup"><span data-stu-id="74b42-108">DESCRIPTION</span></span>
<span data-ttu-id="74b42-109">**AzureRmPolicyDefinition** Cmdlet 會建立原則定義，其中包含 JavaScript) 格式 (JSON 物件符號中的原則規則。</span><span class="sxs-lookup"><span data-stu-id="74b42-109">The **New-AzureRmPolicyDefinition** cmdlet creates a policy definition that includes a policy rule in JavaScript Object Notation (JSON) format.</span></span>

## <span data-ttu-id="74b42-110">示例</span><span class="sxs-lookup"><span data-stu-id="74b42-110">EXAMPLES</span></span>

### <span data-ttu-id="74b42-111">範例1：使用原則檔建立原則定義</span><span class="sxs-lookup"><span data-stu-id="74b42-111">Example 1: Create a policy definition by using a policy file</span></span>
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
PS C:\> New-AzureRmPolicyDefinition -Name 'LocationDefinition' -Policy C:\LocationPolicy.json
```

<span data-ttu-id="74b42-112">這個命令會建立一個名為 LocationDefinition 的原則定義，其中包含 C:\LocationPolicy.json 中指定的原則規則。</span><span class="sxs-lookup"><span data-stu-id="74b42-112">This command creates a policy definition named LocationDefinition that contains the policy rule specified in C:\LocationPolicy.json.</span></span> <span data-ttu-id="74b42-113">上面提供了檔案 LocationPolicy.js的範例內容。</span><span class="sxs-lookup"><span data-stu-id="74b42-113">Example content for the LocationPolicy.json file is provided above.</span></span>

### <span data-ttu-id="74b42-114">範例2：使用內聯參數建立參數化原則定義</span><span class="sxs-lookup"><span data-stu-id="74b42-114">Example 2: Create a parameterized policy definition using inline parameters</span></span>
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
PS C:\> New-AzureRmPolicyDefinition -Name 'LocationDefinition' -Policy C:\LocationPolicy.json -Parameter '{ "listOfAllowedLocations": { "type": "array" } }'
```

<span data-ttu-id="74b42-115">這個命令會建立一個名為 LocationDefinition 的原則定義，其中包含 C:\LocationPolicy.json 中指定的原則規則。</span><span class="sxs-lookup"><span data-stu-id="74b42-115">This command creates a policy definition named LocationDefinition that contains the policy rule specified in C:\LocationPolicy.json.</span></span> <span data-ttu-id="74b42-116">原則規則的參數定義是內嵌提供的。</span><span class="sxs-lookup"><span data-stu-id="74b42-116">The parameter definition for the policy rule is provided inline.</span></span>

### <span data-ttu-id="74b42-117">範例3：在管理群組中內嵌建立原則定義</span><span class="sxs-lookup"><span data-stu-id="74b42-117">Example 3: Create a policy definition inline in a management group</span></span>
```
PS C:\> New-AzureRmPolicyDefinition -Name 'VMPolicyDefinition' -ManagementGroupName Dept42 -DisplayName 'Virtual Machine policy definition' -Policy '{"if":{"source":"action","equals":"Microsoft.Compute/virtualMachines/write"},"then":{"effect":"deny"}}'
```

<span data-ttu-id="74b42-118">這個命令會在管理群組 Dept42 中建立名為 VMPolicyDefinition 的原則定義。</span><span class="sxs-lookup"><span data-stu-id="74b42-118">This command creates a policy definition named VMPolicyDefinition in management group Dept42.</span></span>
<span data-ttu-id="74b42-119">該命令會將原則指定為有效 JSON 格式的字串。</span><span class="sxs-lookup"><span data-stu-id="74b42-119">The command specifies the policy as a string in valid JSON format.</span></span>

### <span data-ttu-id="74b42-120">範例4：以中繼資料內嵌建立原則定義</span><span class="sxs-lookup"><span data-stu-id="74b42-120">Example 4: Create a policy definition inline with metadata</span></span>
```
PS C:\> New-AzureRmPolicyDefinition -Name 'VMPolicyDefinition' -Metadata '{"Category":"Virtual Machine"}' -Policy '{"if":{"source":"action","equals":"Microsoft.Compute/virtualMachines/write"},"then":{"effect":"deny"}}'


Name               : VMPolicyDefinition
ResourceId         : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policyDefinitions/VMPolicyDefinition
ResourceName       : VMPolicyDefinition
ResourceType       : Microsoft.Authorization/policyDefinitions
SubscriptionId     : 11111111-1111-1111-1111-111111111111
Properties         : @{displayName=VMPolicyDefinition; policyType=Custom; mode=All; metadata=; policyRule=}
PolicyDefinitionId : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policyDefinitions/VMPolicyDefinition
```

<span data-ttu-id="74b42-121">這個命令會建立名為 VMPolicyDefinition 的原則定義，其中繼資料指出其類別是 "虛擬機器"。</span><span class="sxs-lookup"><span data-stu-id="74b42-121">This command creates a policy definition named VMPolicyDefinition with metadata indicating its category is "Virtual Machine".</span></span>
<span data-ttu-id="74b42-122">該命令會將原則指定為有效 JSON 格式的字串。</span><span class="sxs-lookup"><span data-stu-id="74b42-122">The command specifies the policy as a string in valid JSON format.</span></span>

## <span data-ttu-id="74b42-123">參數</span><span class="sxs-lookup"><span data-stu-id="74b42-123">PARAMETERS</span></span>

### <span data-ttu-id="74b42-124">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="74b42-124">-ApiVersion</span></span>
<span data-ttu-id="74b42-125">指定要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="74b42-125">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="74b42-126">如果您沒有指定版本，此 Cmdlet 會使用最新的可用版本。</span><span class="sxs-lookup"><span data-stu-id="74b42-126">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="74b42-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74b42-127">-DefaultProfile</span></span>
<span data-ttu-id="74b42-128">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="74b42-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="74b42-129">-描述</span><span class="sxs-lookup"><span data-stu-id="74b42-129">-Description</span></span>
<span data-ttu-id="74b42-130">指定原則定義的描述。</span><span class="sxs-lookup"><span data-stu-id="74b42-130">Specifies a description for the policy definition.</span></span>

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

### <span data-ttu-id="74b42-131">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="74b42-131">-DisplayName</span></span>
<span data-ttu-id="74b42-132">指定原則定義的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="74b42-132">Specifies a display name for the policy definition.</span></span>

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

### <span data-ttu-id="74b42-133">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="74b42-133">-InformationAction</span></span>
<span data-ttu-id="74b42-134">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="74b42-134">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="74b42-135">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="74b42-135">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="74b42-136">持續</span><span class="sxs-lookup"><span data-stu-id="74b42-136">Continue</span></span>
- <span data-ttu-id="74b42-137">理會</span><span class="sxs-lookup"><span data-stu-id="74b42-137">Ignore</span></span>
- <span data-ttu-id="74b42-138">看</span><span class="sxs-lookup"><span data-stu-id="74b42-138">Inquire</span></span>
- <span data-ttu-id="74b42-139">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="74b42-139">SilentlyContinue</span></span>
- <span data-ttu-id="74b42-140">停止</span><span class="sxs-lookup"><span data-stu-id="74b42-140">Stop</span></span>
- <span data-ttu-id="74b42-141">封存</span><span class="sxs-lookup"><span data-stu-id="74b42-141">Suspend</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74b42-142">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="74b42-142">-InformationVariable</span></span>
<span data-ttu-id="74b42-143">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="74b42-143">Specifies an information variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74b42-144">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="74b42-144">-ManagementGroupName</span></span>
<span data-ttu-id="74b42-145">新原則定義之管理群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="74b42-145">The name of the management group of the new policy definition.</span></span>

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

### <span data-ttu-id="74b42-146">-中繼資料</span><span class="sxs-lookup"><span data-stu-id="74b42-146">-Metadata</span></span>
<span data-ttu-id="74b42-147">原則定義的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="74b42-147">The metadata for policy definition.</span></span> <span data-ttu-id="74b42-148">這可以是包含中繼資料之檔案名的路徑，或以字串形式的中繼資料</span><span class="sxs-lookup"><span data-stu-id="74b42-148">This can either be a path to a file name containing the metadata, or the metadata as string</span></span>

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

### <span data-ttu-id="74b42-149">模式</span><span class="sxs-lookup"><span data-stu-id="74b42-149">-Mode</span></span>
<span data-ttu-id="74b42-150">原則定義的模式</span><span class="sxs-lookup"><span data-stu-id="74b42-150">The mode of the policy definition</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Policy.PolicyDefinitionMode]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74b42-151">-名稱</span><span class="sxs-lookup"><span data-stu-id="74b42-151">-Name</span></span>
<span data-ttu-id="74b42-152">指定原則定義的名稱。</span><span class="sxs-lookup"><span data-stu-id="74b42-152">Specifies a name for the policy definition.</span></span>

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

### <span data-ttu-id="74b42-153">-參數</span><span class="sxs-lookup"><span data-stu-id="74b42-153">-Parameter</span></span>
<span data-ttu-id="74b42-154">原則定義的參數宣告。</span><span class="sxs-lookup"><span data-stu-id="74b42-154">The parameters declaration for policy definition.</span></span> <span data-ttu-id="74b42-155">這可以是包含參數宣告之檔案名的路徑，或是參數宣告（字串）。</span><span class="sxs-lookup"><span data-stu-id="74b42-155">This can either be a path to a file name containing the parameters declaration, or the parameters declaration as string.</span></span>

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

### <span data-ttu-id="74b42-156">-原則</span><span class="sxs-lookup"><span data-stu-id="74b42-156">-Policy</span></span>
<span data-ttu-id="74b42-157">指定原則定義的原則規則。</span><span class="sxs-lookup"><span data-stu-id="74b42-157">Specifies a policy rule for the policy definition.</span></span>
<span data-ttu-id="74b42-158">您可以指定 json 檔案的路徑，或是包含 JSON 格式之原則的字串。</span><span class="sxs-lookup"><span data-stu-id="74b42-158">You can specify the path of a .json file or a string that contains the policy in JSON format.</span></span>

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

### <span data-ttu-id="74b42-159">-預先</span><span class="sxs-lookup"><span data-stu-id="74b42-159">-Pre</span></span>
<span data-ttu-id="74b42-160">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="74b42-160">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="74b42-161">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="74b42-161">-SubscriptionId</span></span>
<span data-ttu-id="74b42-162">新原則定義的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="74b42-162">The subscription ID of the new policy definition.</span></span>

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

### <span data-ttu-id="74b42-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74b42-163">CommonParameters</span></span>
<span data-ttu-id="74b42-164">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="74b42-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74b42-165">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="74b42-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74b42-166">輸入</span><span class="sxs-lookup"><span data-stu-id="74b42-166">INPUTS</span></span>

## <span data-ttu-id="74b42-167">輸出</span><span class="sxs-lookup"><span data-stu-id="74b42-167">OUTPUTS</span></span>

## <span data-ttu-id="74b42-168">筆記</span><span class="sxs-lookup"><span data-stu-id="74b42-168">NOTES</span></span>

## <span data-ttu-id="74b42-169">相關連結</span><span class="sxs-lookup"><span data-stu-id="74b42-169">RELATED LINKS</span></span>

[<span data-ttu-id="74b42-170">AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="74b42-170">Get-AzureRmPolicyDefinition</span></span>](./Get-AzureRmPolicyDefinition.md)

[<span data-ttu-id="74b42-171">移除-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="74b42-171">Remove-AzureRmPolicyDefinition</span></span>](./Remove-AzureRmPolicyDefinition.md)

[<span data-ttu-id="74b42-172">Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="74b42-172">Set-AzureRmPolicyDefinition</span></span>](./Set-AzureRmPolicyDefinition.md)


