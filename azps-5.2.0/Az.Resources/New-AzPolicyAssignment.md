---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: BA40BD11-8167-48D7-AC71-72B2FD9924F2
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicyAssignment.md
ms.openlocfilehash: 63efc580cf47274363f04750dc6a3f8da93b6665
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98281485"
---
# <span data-ttu-id="11407-101">New-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="11407-101">New-AzPolicyAssignment</span></span>

## <span data-ttu-id="11407-102">摘要</span><span class="sxs-lookup"><span data-stu-id="11407-102">SYNOPSIS</span></span>
<span data-ttu-id="11407-103">建立原則指派。</span><span class="sxs-lookup"><span data-stu-id="11407-103">Creates a policy assignment.</span></span>

## <span data-ttu-id="11407-104">句法</span><span class="sxs-lookup"><span data-stu-id="11407-104">SYNTAX</span></span>

### <span data-ttu-id="11407-105">DefaultParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="11407-105">DefaultParameterSet (Default)</span></span>
```
New-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PsPolicyDefinition>]
 [-PolicySetDefinition <PsPolicySetDefinition>] [-Metadata <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-AssignIdentity] [-Location <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="11407-106">PolicyParameterObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="11407-106">PolicyParameterObjectParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PsPolicyDefinition> [-PolicySetDefinition <PsPolicySetDefinition>]
 -PolicyParameterObject <Hashtable> [-Metadata <String>] [-EnforcementMode <PolicyAssignmentEnforcementMode>]
 [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="11407-107">PolicyParameterStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="11407-107">PolicyParameterStringParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PsPolicyDefinition> [-PolicySetDefinition <PsPolicySetDefinition>]
 -PolicyParameter <String> [-Metadata <String>] [-EnforcementMode <PolicyAssignmentEnforcementMode>]
 [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="11407-108">PolicySetParameterObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="11407-108">PolicySetParameterObjectParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PsPolicyDefinition>] -PolicySetDefinition <PsPolicySetDefinition>
 -PolicyParameterObject <Hashtable> [-Metadata <String>] [-EnforcementMode <PolicyAssignmentEnforcementMode>]
 [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="11407-109">PolicySetParameterStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="11407-109">PolicySetParameterStringParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PsPolicyDefinition>] -PolicySetDefinition <PsPolicySetDefinition>
 -PolicyParameter <String> [-Metadata <String>] [-EnforcementMode <PolicyAssignmentEnforcementMode>]
 [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="11407-110">說明</span><span class="sxs-lookup"><span data-stu-id="11407-110">DESCRIPTION</span></span>
<span data-ttu-id="11407-111">**新的-AzPolicyAssignment** Cmdlet 會建立原則指派。</span><span class="sxs-lookup"><span data-stu-id="11407-111">The **New-AzPolicyAssignment** cmdlet creates a policy assignment.</span></span>
<span data-ttu-id="11407-112">指定原則與範圍。</span><span class="sxs-lookup"><span data-stu-id="11407-112">Specify a policy and scope.</span></span>

## <span data-ttu-id="11407-113">示例</span><span class="sxs-lookup"><span data-stu-id="11407-113">EXAMPLES</span></span>

### <span data-ttu-id="11407-114">範例1：訂閱層級的原則指派</span><span class="sxs-lookup"><span data-stu-id="11407-114">Example 1: Policy assignment at subscription level</span></span>
```
PS C:\> $Subscription = Get-AzSubscription -SubscriptionName 'Subscription01'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope "/subscriptions/$($Subscription.Id)"
```

<span data-ttu-id="11407-115">第一個命令會使用 Get-AzSubscription Cmdlet 來取得名為 Subscription01 的訂閱，並將其儲存在 $Subscription 變數中。</span><span class="sxs-lookup"><span data-stu-id="11407-115">The first command gets a subscription named Subscription01 by using the Get-AzSubscription cmdlet and stores it in the $Subscription variable.</span></span>
<span data-ttu-id="11407-116">第二個命令會使用 Get-AzPolicyDefinition Cmdlet 來取得名為 VirtualMachinePolicy 的原則定義，並將它儲存在 $Policy 變數中。</span><span class="sxs-lookup"><span data-stu-id="11407-116">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="11407-117">最終命令會將原則指派給訂閱範圍字串所識別之訂閱層級的 $Policy。</span><span class="sxs-lookup"><span data-stu-id="11407-117">The final command assigns the policy in $Policy at the level of the subscription identified by the subscription scope string.</span></span>

### <span data-ttu-id="11407-118">範例2：資源群組層級的原則指派</span><span class="sxs-lookup"><span data-stu-id="11407-118">Example 2: Policy assignment at resource group level</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId
```

<span data-ttu-id="11407-119">第一個命令會使用 Get-AzResourceGroup Cmdlet 來取得名為 ResourceGroup11 的資源群組，並將它儲存在 $ResourceGroup 變數中。</span><span class="sxs-lookup"><span data-stu-id="11407-119">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="11407-120">第二個命令會使用 Get-AzPolicyDefinition Cmdlet 來取得名為 VirtualMachinePolicy 的原則定義，並將它儲存在 $Policy 變數中。</span><span class="sxs-lookup"><span data-stu-id="11407-120">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="11407-121">最後一個命令會將原則指派給 $Policy，該資源群組由 $ResourceGroup 的 **ResourceId** 屬性所識別。</span><span class="sxs-lookup"><span data-stu-id="11407-121">The final command assigns the policy in $Policy at the level of the resource group identified by the **ResourceId** property of $ResourceGroup.</span></span>

### <span data-ttu-id="11407-122">範例3：資源群組層級與 policy 參數物件的原則指派</span><span class="sxs-lookup"><span data-stu-id="11407-122">Example 3: Policy assignment at resource group level with policy parameter object</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -BuiltIn | Where-Object {$_.Properties.DisplayName -eq 'Allowed locations'}
PS C:\> $Locations = Get-AzLocation | where displayname -like '*east*'
PS C:\> $AllowedLocations = @{'listOfAllowedLocations'=($Locations.location)}
PS C:\> New-AzPolicyAssignment -Name 'RestrictLocationPolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -PolicyParameterObject $AllowedLocations
```

<span data-ttu-id="11407-123">第一個命令會使用 Get-AzResourceGroup Cmdlet 來取得名為 ResourceGroup11 的資源群組。</span><span class="sxs-lookup"><span data-stu-id="11407-123">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="11407-124">該命令會將該物件儲存在 $ResourceGroup 變數中。</span><span class="sxs-lookup"><span data-stu-id="11407-124">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="11407-125">第二個命令會使用 Get-AzPolicyDefinition Cmdlet 來取得允許位置的內建原則定義。</span><span class="sxs-lookup"><span data-stu-id="11407-125">The second command gets the built-in policy definition for allowed locations by using the Get-AzPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="11407-126">該命令會將該物件儲存在 $Policy 變數中。</span><span class="sxs-lookup"><span data-stu-id="11407-126">The command stores that object in the $Policy variable.</span></span>
<span data-ttu-id="11407-127">第三個和第四個命令會建立一個物件，其中包含名稱中含 "東" 的所有 Azure 區域。</span><span class="sxs-lookup"><span data-stu-id="11407-127">The third and fourth commands create an object containing all Azure regions with "east" in the name.</span></span>
<span data-ttu-id="11407-128">命令會將該物件儲存在 $AllowedLocations 變數中。</span><span class="sxs-lookup"><span data-stu-id="11407-128">The commands store that object in the $AllowedLocations variable.</span></span>
<span data-ttu-id="11407-129">Final 命令會在 $AllowedLocations 中使用 policy 參數物件的資源群組層次 $Policy 指派原則。</span><span class="sxs-lookup"><span data-stu-id="11407-129">The final command assigns the policy in $Policy at the level of a resource group using the policy parameter object in $AllowedLocations.</span></span>
<span data-ttu-id="11407-130">$ResourceGroup 的 **ResourceId** 屬性會識別資源群組。</span><span class="sxs-lookup"><span data-stu-id="11407-130">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

### <span data-ttu-id="11407-131">範例4：資源群組層級的原則指派（含原則參數檔案）</span><span class="sxs-lookup"><span data-stu-id="11407-131">Example 4: Policy assignment at resource group level with policy parameter file</span></span>
<span data-ttu-id="11407-132">在本機工作目錄中，使用下列內容來建立名為 _AllowedLocations.js_ 的檔案。</span><span class="sxs-lookup"><span data-stu-id="11407-132">Create a file called _AllowedLocations.json_ in the local working directory with the following content.</span></span>

```
{
    "listOfAllowedLocations":  {
      "value": [
        "westus",
        "westeurope",
        "japanwest"
      ]
    }
}
```

```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -BuiltIn | Where-Object {$_.Properties.DisplayName -eq 'Allowed locations'}
PS C:\> New-AzPolicyAssignment -Name 'RestrictLocationPolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -PolicyParameter .\AllowedLocations.json
```

<span data-ttu-id="11407-133">第一個命令會使用 Get-AzResourceGroup Cmdlet 來取得名為 ResourceGroup11 的資源群組，並將它儲存在 $ResourceGroup 變數中。</span><span class="sxs-lookup"><span data-stu-id="11407-133">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="11407-134">第二個命令會使用 Get-AzPolicyDefinition Cmdlet 來取得允許位置的內建原則定義，並將它儲存在 $Policy 變數中。</span><span class="sxs-lookup"><span data-stu-id="11407-134">The second command gets the built-in policy definition for allowed locations by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="11407-135">Final 命令會在 $Policy 的資源群組中，指派由 $ResourceGroup 的 **ResourceId** 屬性所識別的資源群組的原則，該資源組是從本機工作目錄 AllowedLocations.js。</span><span class="sxs-lookup"><span data-stu-id="11407-135">The final command assigns the policy in $Policy at the resource group identified by the **ResourceId** property of $ResourceGroup using the policy parameter file AllowedLocations.json from the local working directory.</span></span>

### <span data-ttu-id="11407-136">範例5：具有受管理身分識別的原則指派</span><span class="sxs-lookup"><span data-stu-id="11407-136">Example 5: Policy assignment with a managed identity</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -Location 'eastus' -AssignIdentity
```

<span data-ttu-id="11407-137">第一個命令會使用 Get-AzResourceGroup Cmdlet 來取得名為 ResourceGroup11 的資源群組，並將它儲存在 $ResourceGroup 變數中。</span><span class="sxs-lookup"><span data-stu-id="11407-137">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="11407-138">第二個命令會使用 Get-AzPolicyDefinition Cmdlet 來取得名為 VirtualMachinePolicy 的原則定義，並將它儲存在 $Policy 變數中。</span><span class="sxs-lookup"><span data-stu-id="11407-138">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="11407-139">最終命令會將 $Policy 的原則指派給資源群組。</span><span class="sxs-lookup"><span data-stu-id="11407-139">The final command assigns the policy in $Policy to the resource group.</span></span> <span data-ttu-id="11407-140">系統會自動建立受管理的身分識別，並指派給原則指派。</span><span class="sxs-lookup"><span data-stu-id="11407-140">A managed identity is automatically created and assigned to the policy assignment.</span></span>

### <span data-ttu-id="11407-141">範例6：具有 [強制模式] 屬性的原則指派</span><span class="sxs-lookup"><span data-stu-id="11407-141">Example 6: Policy assignment with an enforcement mode property</span></span>
```
PS C:\> $Subscription = Get-AzSubscription -SubscriptionName 'Subscription01'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope "/subscriptions/$($Subscription.Id)" -EnforcementMode DoNotEnforce
```

<span data-ttu-id="11407-142">第一個命令會使用 Get-AzSubscription Cmdlet 來取得名為 Subscription01 的訂閱，並將其儲存在 $Subscription 變數中。</span><span class="sxs-lookup"><span data-stu-id="11407-142">The first command gets a subscription named Subscription01 by using the Get-AzSubscription cmdlet and stores it in the $Subscription variable.</span></span>
<span data-ttu-id="11407-143">第二個命令會使用 Get-AzPolicyDefinition Cmdlet 來取得名為 VirtualMachinePolicy 的原則定義，並將它儲存在 $Policy 變數中。</span><span class="sxs-lookup"><span data-stu-id="11407-143">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="11407-144">最終命令會將原則指派給訂閱範圍字串所識別之訂閱層級的 $Policy。</span><span class="sxs-lookup"><span data-stu-id="11407-144">The final command assigns the policy in $Policy at the level of the subscription identified by the subscription scope string.</span></span> <span data-ttu-id="11407-145">作業是使用 _DoNotEnforce_ 的 EnforcementMode 值來設定，亦即在建立或更新資源期間未強制執行原則效果。</span><span class="sxs-lookup"><span data-stu-id="11407-145">The assignment is set with an EnforcementMode value of _DoNotEnforce_ i.e. the policy effect is not enforced during resource creation or update.</span></span>

## <span data-ttu-id="11407-146">參數</span><span class="sxs-lookup"><span data-stu-id="11407-146">PARAMETERS</span></span>

### <span data-ttu-id="11407-147">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="11407-147">-ApiVersion</span></span>
<span data-ttu-id="11407-148">指定要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="11407-148">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="11407-149">如果您沒有指定版本，此 Cmdlet 會使用最新的可用版本。</span><span class="sxs-lookup"><span data-stu-id="11407-149">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="11407-150">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="11407-150">-AssignIdentity</span></span>
<span data-ttu-id="11407-151">針對此原則指派產生並指派 Azure Active Directory 身分識別。</span><span class="sxs-lookup"><span data-stu-id="11407-151">Generate and assign an Azure Active Directory Identity for this policy assignment.</span></span> <span data-ttu-id="11407-152">在執行「deployIfNotExists」原則的部署時，就會使用該身分識別。</span><span class="sxs-lookup"><span data-stu-id="11407-152">The identity will be used when executing deployments for 'deployIfNotExists' policies.</span></span> <span data-ttu-id="11407-153">指派身分識別時，位置是必要的。</span><span class="sxs-lookup"><span data-stu-id="11407-153">Location is required when assigning an identity.</span></span>

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

### <span data-ttu-id="11407-154">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11407-154">-DefaultProfile</span></span>
<span data-ttu-id="11407-155">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="11407-155">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="11407-156">-描述</span><span class="sxs-lookup"><span data-stu-id="11407-156">-Description</span></span>
<span data-ttu-id="11407-157">原則指派的描述</span><span class="sxs-lookup"><span data-stu-id="11407-157">The description for policy assignment</span></span>

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

### <span data-ttu-id="11407-158">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="11407-158">-DisplayName</span></span>
<span data-ttu-id="11407-159">指定原則指派的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="11407-159">Specifies a display name for the policy assignment.</span></span>

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

### <span data-ttu-id="11407-160">-EnforcementMode</span><span class="sxs-lookup"><span data-stu-id="11407-160">-EnforcementMode</span></span>
<span data-ttu-id="11407-161">原則指派的強制模式。</span><span class="sxs-lookup"><span data-stu-id="11407-161">The enforcement mode for policy assignment.</span></span> <span data-ttu-id="11407-162">目前，有效值為預設值，DoNotEnforce。</span><span class="sxs-lookup"><span data-stu-id="11407-162">Currently, valid values are Default, DoNotEnforce.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Policy.PolicyAssignmentEnforcementMode]
Parameter Sets: (All)
Aliases:
Accepted values: Default, DoNotEnforce

Required: False
Position: Named
Default value: Default
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11407-163">-位置</span><span class="sxs-lookup"><span data-stu-id="11407-163">-Location</span></span>
<span data-ttu-id="11407-164">原則指派資源身分識別的位置。</span><span class="sxs-lookup"><span data-stu-id="11407-164">The location of the policy assignment's resource identity.</span></span> <span data-ttu-id="11407-165">使用-AssignIdentity 切換時，這是必要的。</span><span class="sxs-lookup"><span data-stu-id="11407-165">This is required when the -AssignIdentity switch is used.</span></span>

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

### <span data-ttu-id="11407-166">-中繼資料</span><span class="sxs-lookup"><span data-stu-id="11407-166">-Metadata</span></span>
<span data-ttu-id="11407-167">新原則指派的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="11407-167">The metadata for the new policy assignment.</span></span> <span data-ttu-id="11407-168">這可以是包含中繼資料之檔案名的路徑，或是中繼資料作為字串。</span><span class="sxs-lookup"><span data-stu-id="11407-168">This can either be a path to a file name containing the metadata, or the metadata as a string.</span></span>

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

### <span data-ttu-id="11407-169">-名稱</span><span class="sxs-lookup"><span data-stu-id="11407-169">-Name</span></span>
<span data-ttu-id="11407-170">指定原則指派的名稱。</span><span class="sxs-lookup"><span data-stu-id="11407-170">Specifies a name for the policy assignment.</span></span>

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

### <span data-ttu-id="11407-171">-NotScope</span><span class="sxs-lookup"><span data-stu-id="11407-171">-NotScope</span></span>
<span data-ttu-id="11407-172">原則指派的 not 作用中。</span><span class="sxs-lookup"><span data-stu-id="11407-172">The not scopes for policy assignment.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11407-173">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="11407-173">-PolicyDefinition</span></span>
<span data-ttu-id="11407-174">指定原則，做為包含原則規則的 **PsPolicyDefinition** 物件。</span><span class="sxs-lookup"><span data-stu-id="11407-174">Specifies a policy, as a **PsPolicyDefinition** object that contains the policy rule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.Policy.PsPolicyDefinition
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.Policy.PsPolicyDefinition
Parameter Sets: PolicyParameterObjectParameterSet, PolicyParameterStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.Policy.PsPolicyDefinition
Parameter Sets: PolicySetParameterObjectParameterSet, PolicySetParameterStringParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11407-175">-PolicyParameter</span><span class="sxs-lookup"><span data-stu-id="11407-175">-PolicyParameter</span></span>
<span data-ttu-id="11407-176">原則參數檔案路徑或原則參數字串。</span><span class="sxs-lookup"><span data-stu-id="11407-176">The policy parameter file path or policy parameter string.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyParameterStringParameterSet, PolicySetParameterStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11407-177">-PolicyParameterObject</span><span class="sxs-lookup"><span data-stu-id="11407-177">-PolicyParameterObject</span></span>
<span data-ttu-id="11407-178">原則參數物件。</span><span class="sxs-lookup"><span data-stu-id="11407-178">The policy parameter object.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: PolicyParameterObjectParameterSet, PolicySetParameterObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11407-179">-PolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="11407-179">-PolicySetDefinition</span></span>
<span data-ttu-id="11407-180">原則集定義物件。</span><span class="sxs-lookup"><span data-stu-id="11407-180">The policy set definition object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.Policy.PsPolicySetDefinition
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.Policy.PsPolicySetDefinition
Parameter Sets: PolicyParameterObjectParameterSet, PolicyParameterStringParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.Policy.PsPolicySetDefinition
Parameter Sets: PolicySetParameterObjectParameterSet, PolicySetParameterStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11407-181">-預先</span><span class="sxs-lookup"><span data-stu-id="11407-181">-Pre</span></span>
<span data-ttu-id="11407-182">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="11407-182">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="11407-183">-範圍</span><span class="sxs-lookup"><span data-stu-id="11407-183">-Scope</span></span>
<span data-ttu-id="11407-184">指定指派原則的範圍。</span><span class="sxs-lookup"><span data-stu-id="11407-184">Specifies the scope at which to assign the policy.</span></span>
<span data-ttu-id="11407-185">例如，若要將原則指派給資源群組，請指定下列專案： `/subscriptions/` 訂閱識別碼 `/resourcegroups/` 資源組名稱</span><span class="sxs-lookup"><span data-stu-id="11407-185">For instance, to assign a policy to a resource group, specify the following: `/subscriptions/`subscription ID`/resourcegroups/`resource group name</span></span>

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

### <span data-ttu-id="11407-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11407-186">CommonParameters</span></span>
<span data-ttu-id="11407-187">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="11407-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11407-188">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="11407-188">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11407-189">輸入</span><span class="sxs-lookup"><span data-stu-id="11407-189">INPUTS</span></span>

### <span data-ttu-id="11407-190">System.object</span><span class="sxs-lookup"><span data-stu-id="11407-190">System.String</span></span>

### <span data-ttu-id="11407-191">System.object []</span><span class="sxs-lookup"><span data-stu-id="11407-191">System.String[]</span></span>

### <span data-ttu-id="11407-192">系統管理. PSObject</span><span class="sxs-lookup"><span data-stu-id="11407-192">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="11407-193">輸出</span><span class="sxs-lookup"><span data-stu-id="11407-193">OUTPUTS</span></span>

### <span data-ttu-id="11407-194">系統管理. PSObject</span><span class="sxs-lookup"><span data-stu-id="11407-194">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="11407-195">筆記</span><span class="sxs-lookup"><span data-stu-id="11407-195">NOTES</span></span>

## <span data-ttu-id="11407-196">相關連結</span><span class="sxs-lookup"><span data-stu-id="11407-196">RELATED LINKS</span></span>

[<span data-ttu-id="11407-197">AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="11407-197">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="11407-198">AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="11407-198">Get-AzPolicyAssignment</span></span>](./Get-AzPolicyAssignment.md)

[<span data-ttu-id="11407-199">移除-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="11407-199">Remove-AzPolicyAssignment</span></span>](./Remove-AzPolicyAssignment.md)

[<span data-ttu-id="11407-200">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="11407-200">Set-AzPolicyAssignment</span></span>](./Set-AzPolicyAssignment.md)


