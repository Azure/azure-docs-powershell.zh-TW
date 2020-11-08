---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: E1AC7139-786C-4DD6-A898-242723E0D159
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyDefinition.md
ms.openlocfilehash: 3aed403965bc48a26044b930fdf5cc9e9a93bbbe
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94127352"
---
# <span data-ttu-id="d3f93-101">Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="d3f93-101">Set-AzPolicyDefinition</span></span>

## <span data-ttu-id="d3f93-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d3f93-102">SYNOPSIS</span></span>
<span data-ttu-id="d3f93-103">修改原則定義。</span><span class="sxs-lookup"><span data-stu-id="d3f93-103">Modifies a policy definition.</span></span>

## <span data-ttu-id="d3f93-104">句法</span><span class="sxs-lookup"><span data-stu-id="d3f93-104">SYNTAX</span></span>

### <span data-ttu-id="d3f93-105">NameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="d3f93-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d3f93-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d3f93-106">ManagementGroupNameParameterSet</span></span>
```
Set-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] -ManagementGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d3f93-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d3f93-107">SubscriptionIdParameterSet</span></span>
```
Set-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] -SubscriptionId <Guid> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d3f93-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d3f93-108">IdParameterSet</span></span>
```
Set-AzPolicyDefinition -Id <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d3f93-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d3f93-109">InputObjectParameterSet</span></span>
```
Set-AzPolicyDefinition [-DisplayName <String>] [-Description <String>] [-Policy <String>] [-Metadata <String>]
 [-Parameter <String>] [-Mode <String>] -InputObject <PsPolicyDefinition> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d3f93-110">說明</span><span class="sxs-lookup"><span data-stu-id="d3f93-110">DESCRIPTION</span></span>
<span data-ttu-id="d3f93-111">**AzPolicyDefinition** Cmdlet 會修改原則定義。</span><span class="sxs-lookup"><span data-stu-id="d3f93-111">The **Set-AzPolicyDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="d3f93-112">示例</span><span class="sxs-lookup"><span data-stu-id="d3f93-112">EXAMPLES</span></span>

### <span data-ttu-id="d3f93-113">範例1：更新原則定義的描述</span><span class="sxs-lookup"><span data-stu-id="d3f93-113">Example 1: Update the description of a policy definition</span></span>
```
PS C:\> $PolicyDefinition = Get-AzPolicyDefinition -Name 'VMPolicyDefinition'
PS C:\> Set-AzPolicyDefinition -Id $PolicyDefinition.ResourceId -Description 'Updated policy to not allow virtual machine creation'
```

<span data-ttu-id="d3f93-114">第一個命令會使用 Get-AzPolicyDefinition Cmdlet 來取得名為 VMPolicyDefinition 的原則定義。</span><span class="sxs-lookup"><span data-stu-id="d3f93-114">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="d3f93-115">該命令會將該物件儲存在 $PolicyDefinition 變數中。</span><span class="sxs-lookup"><span data-stu-id="d3f93-115">The command stores that object in the $PolicyDefinition variable.</span></span>
<span data-ttu-id="d3f93-116">第二個命令會更新 $PolicyDefinition 的 **ResourceId** 屬性所識別之原則定義的描述。</span><span class="sxs-lookup"><span data-stu-id="d3f93-116">The second command updates the description of the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

### <span data-ttu-id="d3f93-117">範例2：更新原則定義的模式</span><span class="sxs-lookup"><span data-stu-id="d3f93-117">Example 2: Update the mode of a policy definition</span></span>
```
PS C:\> Set-AzPolicyDefinition -Name 'VMPolicyDefinition' -Mode 'All'
```

<span data-ttu-id="d3f93-118">這個命令會使用 Set-AzPolicyDefinition Cmdlet 來更新名為 VMPolicyDefinition 的原則定義，將其 mode 屬性設定為 ' All」。</span><span class="sxs-lookup"><span data-stu-id="d3f93-118">This command updates the policy definition named VMPolicyDefinition by using the Set-AzPolicyDefinition cmdlet to set its mode property to 'All'.</span></span>

### <span data-ttu-id="d3f93-119">範例3：更新原則定義的中繼資料</span><span class="sxs-lookup"><span data-stu-id="d3f93-119">Example 3: Update the metadata of a policy definition</span></span>
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

<span data-ttu-id="d3f93-120">這個命令會更新名為 VMPolicyDefinition 的原則定義中繼資料，以指出其類別是「虛擬機器」。</span><span class="sxs-lookup"><span data-stu-id="d3f93-120">This command updates the metadata of a policy definition named VMPolicyDefinition to indicate its category is "Virtual Machine".</span></span>

## <span data-ttu-id="d3f93-121">參數</span><span class="sxs-lookup"><span data-stu-id="d3f93-121">PARAMETERS</span></span>

### <span data-ttu-id="d3f93-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="d3f93-122">-ApiVersion</span></span>
<span data-ttu-id="d3f93-123">指定要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="d3f93-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="d3f93-124">如果您沒有指定版本，此 Cmdlet 會使用最新的可用版本。</span><span class="sxs-lookup"><span data-stu-id="d3f93-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="d3f93-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3f93-125">-DefaultProfile</span></span>
<span data-ttu-id="d3f93-126">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="d3f93-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d3f93-127">-描述</span><span class="sxs-lookup"><span data-stu-id="d3f93-127">-Description</span></span>
<span data-ttu-id="d3f93-128">指定原則定義的新描述。</span><span class="sxs-lookup"><span data-stu-id="d3f93-128">Specifies a new description for the policy definition.</span></span>

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

### <span data-ttu-id="d3f93-129">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="d3f93-129">-DisplayName</span></span>
<span data-ttu-id="d3f93-130">指定原則定義的新顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="d3f93-130">Specifies a new display name for the policy definition.</span></span>

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

### <span data-ttu-id="d3f93-131">-識別碼</span><span class="sxs-lookup"><span data-stu-id="d3f93-131">-Id</span></span>
<span data-ttu-id="d3f93-132">指定此 Cmdlet 所修改之原則定義的完全限定資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="d3f93-132">Specifies the fully qualified resource ID for the policy definition that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="d3f93-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d3f93-133">-InputObject</span></span>
<span data-ttu-id="d3f93-134">從另一個 Cmdlet 輸出的要更新的原則定義物件。</span><span class="sxs-lookup"><span data-stu-id="d3f93-134">The policy definition object to update that was output from another cmdlet.</span></span>

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

### <span data-ttu-id="d3f93-135">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="d3f93-135">-ManagementGroupName</span></span>
<span data-ttu-id="d3f93-136">要更新之原則定義之管理群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d3f93-136">The name of the management group of the policy definition to update.</span></span>

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

### <span data-ttu-id="d3f93-137">-中繼資料</span><span class="sxs-lookup"><span data-stu-id="d3f93-137">-Metadata</span></span>
<span data-ttu-id="d3f93-138">原則定義的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="d3f93-138">The metadata for policy definition.</span></span> <span data-ttu-id="d3f93-139">這可以是包含中繼資料之檔案名的路徑，或以字串形式的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="d3f93-139">This can either be a path to a file name containing the metadata, or the metadata as string.</span></span>

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

### <span data-ttu-id="d3f93-140">模式</span><span class="sxs-lookup"><span data-stu-id="d3f93-140">-Mode</span></span>
<span data-ttu-id="d3f93-141">新原則定義的模式。</span><span class="sxs-lookup"><span data-stu-id="d3f93-141">The mode of the new policy definition.</span></span>

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

### <span data-ttu-id="d3f93-142">-名稱</span><span class="sxs-lookup"><span data-stu-id="d3f93-142">-Name</span></span>
<span data-ttu-id="d3f93-143">指定此 Cmdlet 所修改之原則定義的名稱。</span><span class="sxs-lookup"><span data-stu-id="d3f93-143">Specifies the name of the policy definition that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="d3f93-144">-參數</span><span class="sxs-lookup"><span data-stu-id="d3f93-144">-Parameter</span></span>
<span data-ttu-id="d3f93-145">原則定義的參數宣告。</span><span class="sxs-lookup"><span data-stu-id="d3f93-145">The parameters declaration for policy definition.</span></span> <span data-ttu-id="d3f93-146">這可以是包含參數宣告之檔案名或 uri 的路徑，或是參數宣告（字串）。</span><span class="sxs-lookup"><span data-stu-id="d3f93-146">This can either be a path to a file name or uri containing the parameters declaration, or the parameters declaration as string.</span></span>

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

### <span data-ttu-id="d3f93-147">-原則</span><span class="sxs-lookup"><span data-stu-id="d3f93-147">-Policy</span></span>
<span data-ttu-id="d3f93-148">指定原則定義的新原則規則。</span><span class="sxs-lookup"><span data-stu-id="d3f93-148">Specifies new policy rule for the policy definition.</span></span>
<span data-ttu-id="d3f93-149">您可以指定 json 檔案的路徑，或是包含 JavaScript 物件符號 (JSON) 格式之原則的字串。</span><span class="sxs-lookup"><span data-stu-id="d3f93-149">You can specify the path of a .json file or a string that contains the policy in JavaScript Object Notation (JSON) format.</span></span>

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

### <span data-ttu-id="d3f93-150">-預先</span><span class="sxs-lookup"><span data-stu-id="d3f93-150">-Pre</span></span>
<span data-ttu-id="d3f93-151">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="d3f93-151">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="d3f93-152">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d3f93-152">-SubscriptionId</span></span>
<span data-ttu-id="d3f93-153">要更新之原則定義的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="d3f93-153">The subscription ID of the policy definition to update.</span></span>

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

### <span data-ttu-id="d3f93-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3f93-154">CommonParameters</span></span>
<span data-ttu-id="d3f93-155">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d3f93-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3f93-156">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="d3f93-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3f93-157">輸入</span><span class="sxs-lookup"><span data-stu-id="d3f93-157">INPUTS</span></span>

### <span data-ttu-id="d3f93-158">System.object</span><span class="sxs-lookup"><span data-stu-id="d3f93-158">System.String</span></span>

### <span data-ttu-id="d3f93-159">"CoreLib" 1 [[System. Guid.empty]、[System.] = 4.0.0.0、Culture = 中性、PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="d3f93-159">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="d3f93-160">輸出</span><span class="sxs-lookup"><span data-stu-id="d3f93-160">OUTPUTS</span></span>

### <span data-ttu-id="d3f93-161">系統管理. PSObject</span><span class="sxs-lookup"><span data-stu-id="d3f93-161">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="d3f93-162">筆記</span><span class="sxs-lookup"><span data-stu-id="d3f93-162">NOTES</span></span>

## <span data-ttu-id="d3f93-163">相關連結</span><span class="sxs-lookup"><span data-stu-id="d3f93-163">RELATED LINKS</span></span>

[<span data-ttu-id="d3f93-164">AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="d3f93-164">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="d3f93-165">新-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="d3f93-165">New-AzPolicyDefinition</span></span>](./New-AzPolicyDefinition.md)

[<span data-ttu-id="d3f93-166">移除-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="d3f93-166">Remove-AzPolicyDefinition</span></span>](./Remove-AzPolicyDefinition.md)


