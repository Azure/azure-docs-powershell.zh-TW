---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: BA40BD11-8167-48D7-AC71-72B2FD9924F2
online version: https://docs.microsoft.com/powershell/module/az.resources/new-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicyAssignment.md
ms.openlocfilehash: d1e6b5b2b2e76c4ec807c27922f9ce577d94a7d8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907082"
---
# <span data-ttu-id="dac68-101">New-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="dac68-101">New-AzPolicyAssignment</span></span>

## <span data-ttu-id="dac68-102">簡介</span><span class="sxs-lookup"><span data-stu-id="dac68-102">SYNOPSIS</span></span>
<span data-ttu-id="dac68-103">建立一個策略指派。</span><span class="sxs-lookup"><span data-stu-id="dac68-103">Creates a policy assignment.</span></span>

## <span data-ttu-id="dac68-104">語法</span><span class="sxs-lookup"><span data-stu-id="dac68-104">SYNTAX</span></span>

### <span data-ttu-id="dac68-105">DefaultParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="dac68-105">DefaultParameterSet (Default)</span></span>
```
New-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PsPolicyDefinition>]
 [-PolicySetDefinition <PsPolicySetDefinition>] [-Metadata <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-AssignIdentity] [-Location <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dac68-106">PolicyParameterObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dac68-106">PolicyParameterObjectParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PsPolicyDefinition> [-PolicySetDefinition <PsPolicySetDefinition>]
 -PolicyParameterObject <Hashtable> [-Metadata <String>] [-EnforcementMode <PolicyAssignmentEnforcementMode>]
 [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dac68-107">PolicyParameterStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="dac68-107">PolicyParameterStringParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PsPolicyDefinition> [-PolicySetDefinition <PsPolicySetDefinition>]
 -PolicyParameter <String> [-Metadata <String>] [-EnforcementMode <PolicyAssignmentEnforcementMode>]
 [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dac68-108">PolicySetParameterObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dac68-108">PolicySetParameterObjectParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PsPolicyDefinition>] -PolicySetDefinition <PsPolicySetDefinition>
 -PolicyParameterObject <Hashtable> [-Metadata <String>] [-EnforcementMode <PolicyAssignmentEnforcementMode>]
 [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dac68-109">PolicySetParameterStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="dac68-109">PolicySetParameterStringParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PsPolicyDefinition>] -PolicySetDefinition <PsPolicySetDefinition>
 -PolicyParameter <String> [-Metadata <String>] [-EnforcementMode <PolicyAssignmentEnforcementMode>]
 [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dac68-110">描述</span><span class="sxs-lookup"><span data-stu-id="dac68-110">DESCRIPTION</span></span>
<span data-ttu-id="dac68-111">**New-AzPolicyAssignment** Cmdlet 會建立一個策略指派。</span><span class="sxs-lookup"><span data-stu-id="dac68-111">The **New-AzPolicyAssignment** cmdlet creates a policy assignment.</span></span>
<span data-ttu-id="dac68-112">指定一個策略和範圍。</span><span class="sxs-lookup"><span data-stu-id="dac68-112">Specify a policy and scope.</span></span>

## <span data-ttu-id="dac68-113">例子</span><span class="sxs-lookup"><span data-stu-id="dac68-113">EXAMPLES</span></span>

### <span data-ttu-id="dac68-114">範例 1：訂閱層級的策略指派</span><span class="sxs-lookup"><span data-stu-id="dac68-114">Example 1: Policy assignment at subscription level</span></span>
```
PS C:\> $Subscription = Get-AzSubscription -SubscriptionName 'Subscription01'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope "/subscriptions/$($Subscription.Id)"
```

<span data-ttu-id="dac68-115">第一個命令會使用 Get-AzSubscription Cmdlet 來獲得名為 Subscription01 的訂閱，並儲存在$Subscription變數中。</span><span class="sxs-lookup"><span data-stu-id="dac68-115">The first command gets a subscription named Subscription01 by using the Get-AzSubscription cmdlet and stores it in the $Subscription variable.</span></span>
<span data-ttu-id="dac68-116">第二個命令會使用 Get-AzPolicyDefinition Cmdlet 來獲得名為 VirtualMachinePolicy$Policy定義。</span><span class="sxs-lookup"><span data-stu-id="dac68-116">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="dac68-117">最後一個命令會$Policy訂閱範圍字串所識別的訂閱層級指派該策略。</span><span class="sxs-lookup"><span data-stu-id="dac68-117">The final command assigns the policy in $Policy at the level of the subscription identified by the subscription scope string.</span></span>

### <span data-ttu-id="dac68-118">範例 2：資源群組層級中的策略指派</span><span class="sxs-lookup"><span data-stu-id="dac68-118">Example 2: Policy assignment at resource group level</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId
```

<span data-ttu-id="dac68-119">第一個命令會使用 Get-AzResourceGroup Cmdlet，將資源群組命名為 ResourceGroup11，並儲存在$ResourceGroup變數中。</span><span class="sxs-lookup"><span data-stu-id="dac68-119">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="dac68-120">第二個命令會使用 Get-AzPolicyDefinition Cmdlet 來獲得名為 VirtualMachinePolicy$Policy定義。</span><span class="sxs-lookup"><span data-stu-id="dac68-120">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="dac68-121">最後一個命令會$Policy中由 **resourceId** 屬性識別的資源群組層級指派$ResourceGroup。</span><span class="sxs-lookup"><span data-stu-id="dac68-121">The final command assigns the policy in $Policy at the level of the resource group identified by the **ResourceId** property of $ResourceGroup.</span></span>

### <span data-ttu-id="dac68-122">範例 3：使用策略參數物件在資源群組層級進行策略指派</span><span class="sxs-lookup"><span data-stu-id="dac68-122">Example 3: Policy assignment at resource group level with policy parameter object</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -BuiltIn | Where-Object {$_.Properties.DisplayName -eq 'Allowed locations'}
PS C:\> $Locations = Get-AzLocation | where displayname -like '*east*'
PS C:\> $AllowedLocations = @{'listOfAllowedLocations'=($Locations.location)}
PS C:\> New-AzPolicyAssignment -Name 'RestrictLocationPolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -PolicyParameterObject $AllowedLocations
```

<span data-ttu-id="dac68-123">第一個命令會使用 Get-AzResourceGroup Cmdlet，獲得一個名為 ResourceGroup11 的資源群組。</span><span class="sxs-lookup"><span data-stu-id="dac68-123">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="dac68-124">該命令將該物件儲存在$ResourceGroup變數中。</span><span class="sxs-lookup"><span data-stu-id="dac68-124">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="dac68-125">第二個命令會使用 Cmdlet，為允許的位置Get-AzPolicyDefinition定義。</span><span class="sxs-lookup"><span data-stu-id="dac68-125">The second command gets the built-in policy definition for allowed locations by using the Get-AzPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="dac68-126">該命令將該物件儲存在$Policy變數中。</span><span class="sxs-lookup"><span data-stu-id="dac68-126">The command stores that object in the $Policy variable.</span></span>
<span data-ttu-id="dac68-127">第三個和第四個命令會建立一個物件，其中包含名稱中含有"east"的所有 Azure 區域。</span><span class="sxs-lookup"><span data-stu-id="dac68-127">The third and fourth commands create an object containing all Azure regions with "east" in the name.</span></span>
<span data-ttu-id="dac68-128">命令會將該物件儲存在$AllowedLocations變數中。</span><span class="sxs-lookup"><span data-stu-id="dac68-128">The commands store that object in the $AllowedLocations variable.</span></span>
<span data-ttu-id="dac68-129">最後一個命令會使用 $Policy 中之 policy 參數物件，在資源群組層級指派$AllowedLocations。</span><span class="sxs-lookup"><span data-stu-id="dac68-129">The final command assigns the policy in $Policy at the level of a resource group using the policy parameter object in $AllowedLocations.</span></span>
<span data-ttu-id="dac68-130">資源的 **ResourceId** 屬性$ResourceGroup識別資源群組。</span><span class="sxs-lookup"><span data-stu-id="dac68-130">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

### <span data-ttu-id="dac68-131">範例 4：使用策略參數檔案在資源群組層級進行策略指派</span><span class="sxs-lookup"><span data-stu-id="dac68-131">Example 4: Policy assignment at resource group level with policy parameter file</span></span>
<span data-ttu-id="dac68-132">在具有下列內容的 _AllowedLocations.js_ 建立名為AllowedLocations.js的檔案。</span><span class="sxs-lookup"><span data-stu-id="dac68-132">Create a file called _AllowedLocations.json_ in the local working directory with the following content.</span></span>

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

<span data-ttu-id="dac68-133">第一個命令會使用 Get-AzResourceGroup Cmdlet，將資源群組命名為 ResourceGroup11，並儲存在$ResourceGroup變數中。</span><span class="sxs-lookup"><span data-stu-id="dac68-133">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="dac68-134">第二個命令會使用 Get-AzPolicyDefinition Cmdlet，針對允許的位置獲得內建$Policy定義。</span><span class="sxs-lookup"><span data-stu-id="dac68-134">The second command gets the built-in policy definition for allowed locations by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="dac68-135">最後一個命令會使用$Policy工作目錄上$ResourceGroup之AllowedLocations.js參數檔案，在 $Policy資源群組中指派該策略。</span><span class="sxs-lookup"><span data-stu-id="dac68-135">The final command assigns the policy in $Policy at the resource group identified by the **ResourceId** property of $ResourceGroup using the policy parameter file AllowedLocations.json from the local working directory.</span></span>

### <span data-ttu-id="dac68-136">範例 5：具有受管理身分識別之策略指派</span><span class="sxs-lookup"><span data-stu-id="dac68-136">Example 5: Policy assignment with a managed identity</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -Location 'eastus' -AssignIdentity
```

<span data-ttu-id="dac68-137">第一個命令會使用 Get-AzResourceGroup Cmdlet，將資源群組命名為 ResourceGroup11，並儲存在$ResourceGroup變數中。</span><span class="sxs-lookup"><span data-stu-id="dac68-137">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="dac68-138">第二個命令會使用 Get-AzPolicyDefinition Cmdlet 來獲得名為 VirtualMachinePolicy$Policy定義。</span><span class="sxs-lookup"><span data-stu-id="dac68-138">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="dac68-139">最後一個命令會$Policy資源群組。</span><span class="sxs-lookup"><span data-stu-id="dac68-139">The final command assigns the policy in $Policy to the resource group.</span></span> <span data-ttu-id="dac68-140">系統會自動建立受管理的身分識別，並指派給該策略指派。</span><span class="sxs-lookup"><span data-stu-id="dac68-140">A managed identity is automatically created and assigned to the policy assignment.</span></span>

### <span data-ttu-id="dac68-141">範例 6：具有強制模式屬性的策略指派</span><span class="sxs-lookup"><span data-stu-id="dac68-141">Example 6: Policy assignment with an enforcement mode property</span></span>
```
PS C:\> $Subscription = Get-AzSubscription -SubscriptionName 'Subscription01'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope "/subscriptions/$($Subscription.Id)" -EnforcementMode DoNotEnforce
```

<span data-ttu-id="dac68-142">第一個命令會使用 Get-AzSubscription Cmdlet 來獲得名為 Subscription01 的訂閱，並儲存在$Subscription變數中。</span><span class="sxs-lookup"><span data-stu-id="dac68-142">The first command gets a subscription named Subscription01 by using the Get-AzSubscription cmdlet and stores it in the $Subscription variable.</span></span>
<span data-ttu-id="dac68-143">第二個命令會使用 Get-AzPolicyDefinition Cmdlet 來獲得名為 VirtualMachinePolicy$Policy定義。</span><span class="sxs-lookup"><span data-stu-id="dac68-143">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="dac68-144">最後一個命令會$Policy訂閱範圍字串所識別的訂閱層級指派該策略。</span><span class="sxs-lookup"><span data-stu-id="dac68-144">The final command assigns the policy in $Policy at the level of the subscription identified by the subscription scope string.</span></span> <span data-ttu-id="dac68-145">工作分派設定為 _DoNotEnforce_ 的 EnforcementMode 值，即在建立或更新資源時不會強制執行該政策效果。</span><span class="sxs-lookup"><span data-stu-id="dac68-145">The assignment is set with an EnforcementMode value of _DoNotEnforce_ i.e. the policy effect is not enforced during resource creation or update.</span></span>

## <span data-ttu-id="dac68-146">參數</span><span class="sxs-lookup"><span data-stu-id="dac68-146">PARAMETERS</span></span>

### <span data-ttu-id="dac68-147">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="dac68-147">-ApiVersion</span></span>
<span data-ttu-id="dac68-148">指定要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="dac68-148">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="dac68-149">如果您未指定版本，此 Cmdlet 會使用最新的可用版本。</span><span class="sxs-lookup"><span data-stu-id="dac68-149">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="dac68-150">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="dac68-150">-AssignIdentity</span></span>
<span data-ttu-id="dac68-151">產生並指派此策略指派的 Azure Active Directory 身分識別。</span><span class="sxs-lookup"><span data-stu-id="dac68-151">Generate and assign an Azure Active Directory Identity for this policy assignment.</span></span> <span data-ttu-id="dac68-152">身分識別將用於執行 'deployIfNotExists' 策略的部署。</span><span class="sxs-lookup"><span data-stu-id="dac68-152">The identity will be used when executing deployments for 'deployIfNotExists' policies.</span></span> <span data-ttu-id="dac68-153">指派身分識別時需要位置。</span><span class="sxs-lookup"><span data-stu-id="dac68-153">Location is required when assigning an identity.</span></span>

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

### <span data-ttu-id="dac68-154">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dac68-154">-DefaultProfile</span></span>
<span data-ttu-id="dac68-155">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="dac68-155">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dac68-156">-描述</span><span class="sxs-lookup"><span data-stu-id="dac68-156">-Description</span></span>
<span data-ttu-id="dac68-157">政策指派的描述</span><span class="sxs-lookup"><span data-stu-id="dac68-157">The description for policy assignment</span></span>

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

### <span data-ttu-id="dac68-158">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="dac68-158">-DisplayName</span></span>
<span data-ttu-id="dac68-159">指定策略指派的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="dac68-159">Specifies a display name for the policy assignment.</span></span>

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

### <span data-ttu-id="dac68-160">-EnforcementMode</span><span class="sxs-lookup"><span data-stu-id="dac68-160">-EnforcementMode</span></span>
<span data-ttu-id="dac68-161">策略指派的強制執行模式。</span><span class="sxs-lookup"><span data-stu-id="dac68-161">The enforcement mode for policy assignment.</span></span> <span data-ttu-id="dac68-162">目前，有效的值為 Default、DoNotEnforce。</span><span class="sxs-lookup"><span data-stu-id="dac68-162">Currently, valid values are Default, DoNotEnforce.</span></span>

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

### <span data-ttu-id="dac68-163">-位置</span><span class="sxs-lookup"><span data-stu-id="dac68-163">-Location</span></span>
<span data-ttu-id="dac68-164">策略工作分派的資源身分識別位置。</span><span class="sxs-lookup"><span data-stu-id="dac68-164">The location of the policy assignment's resource identity.</span></span> <span data-ttu-id="dac68-165">使用 -AssignIdentity 切換時，這是必要的。</span><span class="sxs-lookup"><span data-stu-id="dac68-165">This is required when the -AssignIdentity switch is used.</span></span>

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

### <span data-ttu-id="dac68-166">-中繼資料</span><span class="sxs-lookup"><span data-stu-id="dac68-166">-Metadata</span></span>
<span data-ttu-id="dac68-167">新策略指派的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="dac68-167">The metadata for the new policy assignment.</span></span> <span data-ttu-id="dac68-168">這可以是包含中繼資料之檔案名的路徑，或以字串形式表示中繼資料。</span><span class="sxs-lookup"><span data-stu-id="dac68-168">This can either be a path to a file name containing the metadata, or the metadata as a string.</span></span>

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

### <span data-ttu-id="dac68-169">-名稱</span><span class="sxs-lookup"><span data-stu-id="dac68-169">-Name</span></span>
<span data-ttu-id="dac68-170">指定策略工作分派的名稱。</span><span class="sxs-lookup"><span data-stu-id="dac68-170">Specifies a name for the policy assignment.</span></span>

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

### <span data-ttu-id="dac68-171">-NotScope</span><span class="sxs-lookup"><span data-stu-id="dac68-171">-NotScope</span></span>
<span data-ttu-id="dac68-172">非策略工作分派的範圍。</span><span class="sxs-lookup"><span data-stu-id="dac68-172">The not scopes for policy assignment.</span></span>

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

### <span data-ttu-id="dac68-173">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="dac68-173">-PolicyDefinition</span></span>
<span data-ttu-id="dac68-174">指定原則，做為 **包含原則規則的 PsPolicyDefinition** 物件。</span><span class="sxs-lookup"><span data-stu-id="dac68-174">Specifies a policy, as a **PsPolicyDefinition** object that contains the policy rule.</span></span>

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

### <span data-ttu-id="dac68-175">-PolicyParameter</span><span class="sxs-lookup"><span data-stu-id="dac68-175">-PolicyParameter</span></span>
<span data-ttu-id="dac68-176">策略參數檔案路徑或策略參數字串。</span><span class="sxs-lookup"><span data-stu-id="dac68-176">The policy parameter file path or policy parameter string.</span></span>

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

### <span data-ttu-id="dac68-177">-PolicyParameterObject</span><span class="sxs-lookup"><span data-stu-id="dac68-177">-PolicyParameterObject</span></span>
<span data-ttu-id="dac68-178">Policy 參數物件。</span><span class="sxs-lookup"><span data-stu-id="dac68-178">The policy parameter object.</span></span>

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

### <span data-ttu-id="dac68-179">-PolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="dac68-179">-PolicySetDefinition</span></span>
<span data-ttu-id="dac68-180">該策略集定義物件。</span><span class="sxs-lookup"><span data-stu-id="dac68-180">The policy set definition object.</span></span>

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

### <span data-ttu-id="dac68-181">-Pre</span><span class="sxs-lookup"><span data-stu-id="dac68-181">-Pre</span></span>
<span data-ttu-id="dac68-182">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮測試版 API 版本。</span><span class="sxs-lookup"><span data-stu-id="dac68-182">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="dac68-183">-範圍</span><span class="sxs-lookup"><span data-stu-id="dac68-183">-Scope</span></span>
<span data-ttu-id="dac68-184">指定要指派該策略的範圍。</span><span class="sxs-lookup"><span data-stu-id="dac68-184">Specifies the scope at which to assign the policy.</span></span>
<span data-ttu-id="dac68-185">例如，若要將策略指派給資源群組，請指定下列專案： `/subscriptions/` 訂閱識別碼 `/resourcegroups/` 資源組名</span><span class="sxs-lookup"><span data-stu-id="dac68-185">For instance, to assign a policy to a resource group, specify the following: `/subscriptions/`subscription ID`/resourcegroups/`resource group name</span></span>

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

### <span data-ttu-id="dac68-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dac68-186">CommonParameters</span></span>
<span data-ttu-id="dac68-187">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="dac68-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dac68-188">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dac68-188">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dac68-189">輸入</span><span class="sxs-lookup"><span data-stu-id="dac68-189">INPUTS</span></span>

### <span data-ttu-id="dac68-190">System.String</span><span class="sxs-lookup"><span data-stu-id="dac68-190">System.String</span></span>

### <span data-ttu-id="dac68-191">System.String[]</span><span class="sxs-lookup"><span data-stu-id="dac68-191">System.String[]</span></span>

### <span data-ttu-id="dac68-192">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="dac68-192">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="dac68-193">輸出</span><span class="sxs-lookup"><span data-stu-id="dac68-193">OUTPUTS</span></span>

### <span data-ttu-id="dac68-194">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="dac68-194">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="dac68-195">筆記</span><span class="sxs-lookup"><span data-stu-id="dac68-195">NOTES</span></span>

## <span data-ttu-id="dac68-196">相關連結</span><span class="sxs-lookup"><span data-stu-id="dac68-196">RELATED LINKS</span></span>

[<span data-ttu-id="dac68-197">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="dac68-197">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="dac68-198">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="dac68-198">Get-AzPolicyAssignment</span></span>](./Get-AzPolicyAssignment.md)

[<span data-ttu-id="dac68-199">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="dac68-199">Remove-AzPolicyAssignment</span></span>](./Remove-AzPolicyAssignment.md)

[<span data-ttu-id="dac68-200">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="dac68-200">Set-AzPolicyAssignment</span></span>](./Set-AzPolicyAssignment.md)


