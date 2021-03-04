---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: E1AC7139-786C-4DD6-A898-242723E0D159
online version: https://docs.microsoft.com/powershell/module/az.resources/set-azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyDefinition.md
ms.openlocfilehash: ee3f1ffdb7e95e3c00b30238bf6d35833d99cea6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916894"
---
# <span data-ttu-id="f19f2-101">Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f19f2-101">Set-AzPolicyDefinition</span></span>

## <span data-ttu-id="f19f2-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f19f2-102">SYNOPSIS</span></span>
<span data-ttu-id="f19f2-103">修改策略定義。</span><span class="sxs-lookup"><span data-stu-id="f19f2-103">Modifies a policy definition.</span></span>

## <span data-ttu-id="f19f2-104">語法</span><span class="sxs-lookup"><span data-stu-id="f19f2-104">SYNTAX</span></span>

### <span data-ttu-id="f19f2-105">NameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="f19f2-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f19f2-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f19f2-106">ManagementGroupNameParameterSet</span></span>
```
Set-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] -ManagementGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f19f2-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f19f2-107">SubscriptionIdParameterSet</span></span>
```
Set-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] -SubscriptionId <Guid> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f19f2-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f19f2-108">IdParameterSet</span></span>
```
Set-AzPolicyDefinition -Id <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f19f2-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f19f2-109">InputObjectParameterSet</span></span>
```
Set-AzPolicyDefinition [-DisplayName <String>] [-Description <String>] [-Policy <String>] [-Metadata <String>]
 [-Parameter <String>] [-Mode <String>] -InputObject <PsPolicyDefinition> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f19f2-110">描述</span><span class="sxs-lookup"><span data-stu-id="f19f2-110">DESCRIPTION</span></span>
<span data-ttu-id="f19f2-111">**Set-AzPolicyDefinition** Cmdlet 會修改一個策略定義。</span><span class="sxs-lookup"><span data-stu-id="f19f2-111">The **Set-AzPolicyDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="f19f2-112">例子</span><span class="sxs-lookup"><span data-stu-id="f19f2-112">EXAMPLES</span></span>

### <span data-ttu-id="f19f2-113">範例 1：更新策略定義的描述</span><span class="sxs-lookup"><span data-stu-id="f19f2-113">Example 1: Update the description of a policy definition</span></span>
```
PS C:\> $PolicyDefinition = Get-AzPolicyDefinition -Name 'VMPolicyDefinition'
PS C:\> Set-AzPolicyDefinition -Id $PolicyDefinition.ResourceId -Description 'Updated policy to not allow virtual machine creation'
```

<span data-ttu-id="f19f2-114">第一個命令會使用 Get-AzPolicyDefinition Cmdlet，獲得名為 VMPolicyDefinitionGet-AzPolicyDefinition定義。</span><span class="sxs-lookup"><span data-stu-id="f19f2-114">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="f19f2-115">該命令會儲存該物件在$PolicyDefinition變數中。</span><span class="sxs-lookup"><span data-stu-id="f19f2-115">The command stores that object in the $PolicyDefinition variable.</span></span>
<span data-ttu-id="f19f2-116">第二個命令會更新由 **resourceId** 屬性識別之 $PolicyDefinition。</span><span class="sxs-lookup"><span data-stu-id="f19f2-116">The second command updates the description of the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

### <span data-ttu-id="f19f2-117">範例 2：更新策略定義的模式</span><span class="sxs-lookup"><span data-stu-id="f19f2-117">Example 2: Update the mode of a policy definition</span></span>
```
PS C:\> Set-AzPolicyDefinition -Name 'VMPolicyDefinition' -Mode 'All'
```

<span data-ttu-id="f19f2-118">此命令會使用 Set-AzPolicyDefinition Cmdlet 將 mode 屬性設為 'All'，來更新名為 VMPolicyDefinition 的策略定義。</span><span class="sxs-lookup"><span data-stu-id="f19f2-118">This command updates the policy definition named VMPolicyDefinition by using the Set-AzPolicyDefinition cmdlet to set its mode property to 'All'.</span></span>

### <span data-ttu-id="f19f2-119">範例 3：更新策略定義的中繼資料</span><span class="sxs-lookup"><span data-stu-id="f19f2-119">Example 3: Update the metadata of a policy definition</span></span>
```
PS C:\> Set-AzPolicyDefinition -Name 'VMPolicyDefinition' -Metadata '{"category":"Virtual Machine"}'


Name               : VMPolicyDefinition
ResourceId         : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policyDefinitions/VMPolicyDefinition
ResourceName       : VMPolicyDefinition
ResourceType       : Microsoft.Authorization/policyDefinitions
SubscriptionId     : 11111111-1111-1111-1111-111111111111
Properties         : @{displayName=VMPolicyDefinition; policyType=Custom; mode=All; metadata=; policyRule=}
PolicyDefinitionId : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policyDefinitions/VMPolicyDefinition
```

<span data-ttu-id="f19f2-120">此命令會更新名為 VMPolicyDefinition 之策略定義的中繼資料，指出其類別為「虛擬機器」。</span><span class="sxs-lookup"><span data-stu-id="f19f2-120">This command updates the metadata of a policy definition named VMPolicyDefinition to indicate its category is "Virtual Machine".</span></span>

## <span data-ttu-id="f19f2-121">參數</span><span class="sxs-lookup"><span data-stu-id="f19f2-121">PARAMETERS</span></span>

### <span data-ttu-id="f19f2-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="f19f2-122">-ApiVersion</span></span>
<span data-ttu-id="f19f2-123">指定要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="f19f2-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="f19f2-124">如果您未指定版本，此 Cmdlet 會使用最新的可用版本。</span><span class="sxs-lookup"><span data-stu-id="f19f2-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="f19f2-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f19f2-125">-DefaultProfile</span></span>
<span data-ttu-id="f19f2-126">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="f19f2-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f19f2-127">-描述</span><span class="sxs-lookup"><span data-stu-id="f19f2-127">-Description</span></span>
<span data-ttu-id="f19f2-128">指定新的策略定義描述。</span><span class="sxs-lookup"><span data-stu-id="f19f2-128">Specifies a new description for the policy definition.</span></span>

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

### <span data-ttu-id="f19f2-129">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="f19f2-129">-DisplayName</span></span>
<span data-ttu-id="f19f2-130">指定新的顯示名稱以用於該策略定義。</span><span class="sxs-lookup"><span data-stu-id="f19f2-130">Specifies a new display name for the policy definition.</span></span>

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

### <span data-ttu-id="f19f2-131">-Id</span><span class="sxs-lookup"><span data-stu-id="f19f2-131">-Id</span></span>
<span data-ttu-id="f19f2-132">指定此 Cmdlet 修改之策略定義之完整資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="f19f2-132">Specifies the fully qualified resource ID for the policy definition that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="f19f2-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f19f2-133">-InputObject</span></span>
<span data-ttu-id="f19f2-134">要更新從另一個 Cmdlet 輸出的策略定義物件。</span><span class="sxs-lookup"><span data-stu-id="f19f2-134">The policy definition object to update that was output from another cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.Policy.PsPolicyDefinition
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f19f2-135">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="f19f2-135">-ManagementGroupName</span></span>
<span data-ttu-id="f19f2-136">要更新之策略定義的管理組名。</span><span class="sxs-lookup"><span data-stu-id="f19f2-136">The name of the management group of the policy definition to update.</span></span>

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

### <span data-ttu-id="f19f2-137">-中繼資料</span><span class="sxs-lookup"><span data-stu-id="f19f2-137">-Metadata</span></span>
<span data-ttu-id="f19f2-138">用於定義策略的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="f19f2-138">The metadata for policy definition.</span></span> <span data-ttu-id="f19f2-139">這可以是包含中繼資料之檔案名的路徑，或中繼資料為字串。</span><span class="sxs-lookup"><span data-stu-id="f19f2-139">This can either be a path to a file name containing the metadata, or the metadata as string.</span></span>

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

### <span data-ttu-id="f19f2-140">-模式</span><span class="sxs-lookup"><span data-stu-id="f19f2-140">-Mode</span></span>
<span data-ttu-id="f19f2-141">新策略定義的模式。</span><span class="sxs-lookup"><span data-stu-id="f19f2-141">The mode of the new policy definition.</span></span>

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

### <span data-ttu-id="f19f2-142">-名稱</span><span class="sxs-lookup"><span data-stu-id="f19f2-142">-Name</span></span>
<span data-ttu-id="f19f2-143">指定此 Cmdlet 修改之策略定義的名稱。</span><span class="sxs-lookup"><span data-stu-id="f19f2-143">Specifies the name of the policy definition that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="f19f2-144">-Parameter</span><span class="sxs-lookup"><span data-stu-id="f19f2-144">-Parameter</span></span>
<span data-ttu-id="f19f2-145">原則定義的參數宣告。</span><span class="sxs-lookup"><span data-stu-id="f19f2-145">The parameters declaration for policy definition.</span></span> <span data-ttu-id="f19f2-146">這可以是檔案名或包含參數宣告的 uri 路徑，或參數宣告為字串。</span><span class="sxs-lookup"><span data-stu-id="f19f2-146">This can either be a path to a file name or uri containing the parameters declaration, or the parameters declaration as string.</span></span>

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

### <span data-ttu-id="f19f2-147">-策略</span><span class="sxs-lookup"><span data-stu-id="f19f2-147">-Policy</span></span>
<span data-ttu-id="f19f2-148">指定原則定義的新原則規則。</span><span class="sxs-lookup"><span data-stu-id="f19f2-148">Specifies new policy rule for the policy definition.</span></span>
<span data-ttu-id="f19f2-149">您可以使用 JSON 格式的 JavaScript 物件標記法指定 .json 檔案或包含 (字串) 路徑。</span><span class="sxs-lookup"><span data-stu-id="f19f2-149">You can specify the path of a .json file or a string that contains the policy in JavaScript Object Notation (JSON) format.</span></span>

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

### <span data-ttu-id="f19f2-150">-Pre</span><span class="sxs-lookup"><span data-stu-id="f19f2-150">-Pre</span></span>
<span data-ttu-id="f19f2-151">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮測試版 API 版本。</span><span class="sxs-lookup"><span data-stu-id="f19f2-151">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="f19f2-152">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f19f2-152">-SubscriptionId</span></span>
<span data-ttu-id="f19f2-153">要更新之策略定義的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="f19f2-153">The subscription ID of the policy definition to update.</span></span>

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

### <span data-ttu-id="f19f2-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f19f2-154">CommonParameters</span></span>
<span data-ttu-id="f19f2-155">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f19f2-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f19f2-156">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f19f2-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f19f2-157">輸入</span><span class="sxs-lookup"><span data-stu-id="f19f2-157">INPUTS</span></span>

### <span data-ttu-id="f19f2-158">System.String</span><span class="sxs-lookup"><span data-stu-id="f19f2-158">System.String</span></span>

### <span data-ttu-id="f19f2-159">System.Nullable'1[[System.Guid， System.Private.CoreLib， Version=4.0.0.0， Culture=neutral， PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="f19f2-159">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="f19f2-160">輸出</span><span class="sxs-lookup"><span data-stu-id="f19f2-160">OUTPUTS</span></span>

### <span data-ttu-id="f19f2-161">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="f19f2-161">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="f19f2-162">筆記</span><span class="sxs-lookup"><span data-stu-id="f19f2-162">NOTES</span></span>

## <span data-ttu-id="f19f2-163">相關連結</span><span class="sxs-lookup"><span data-stu-id="f19f2-163">RELATED LINKS</span></span>

[<span data-ttu-id="f19f2-164">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f19f2-164">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="f19f2-165">New-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f19f2-165">New-AzPolicyDefinition</span></span>](./New-AzPolicyDefinition.md)

[<span data-ttu-id="f19f2-166">Remove-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f19f2-166">Remove-AzPolicyDefinition</span></span>](./Remove-AzPolicyDefinition.md)


