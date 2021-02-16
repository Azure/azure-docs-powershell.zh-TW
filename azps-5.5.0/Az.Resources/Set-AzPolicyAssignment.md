---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C3B2C33F-8BD4-4E31-9450-EF6A3A6A5325
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyAssignment.md
ms.openlocfilehash: 8efda1a15546a09f0946506f3bc7fd27462b3c03
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100139923"
---
# <span data-ttu-id="0a055-101">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="0a055-101">Set-AzPolicyAssignment</span></span>

## <span data-ttu-id="0a055-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0a055-102">SYNOPSIS</span></span>
<span data-ttu-id="0a055-103">修改原則分派。</span><span class="sxs-lookup"><span data-stu-id="0a055-103">Modifies a policy assignment.</span></span>

## <span data-ttu-id="0a055-104">句法</span><span class="sxs-lookup"><span data-stu-id="0a055-104">SYNTAX</span></span>

### <span data-ttu-id="0a055-105">NameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="0a055-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Metadata <String>] [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0a055-106">PolicyParameterNameObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0a055-106">PolicyParameterNameObjectParameterSet</span></span>
```
Set-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Metadata <String>] -PolicyParameterObject <Hashtable> [-AssignIdentity]
 [-Location <String>] [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0a055-107">PolicyParameterNameStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="0a055-107">PolicyParameterNameStringParameterSet</span></span>
```
Set-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Metadata <String>] -PolicyParameter <String> [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0a055-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0a055-108">IdParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] -Id <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0a055-109">PolicyParameterIdObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0a055-109">PolicyParameterIdObjectParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] -Id <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] -PolicyParameterObject <Hashtable> [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0a055-110">PolicyParameterIdStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="0a055-110">PolicyParameterIdStringParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] -Id <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] -PolicyParameter <String> [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0a055-111">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0a055-111">InputObjectParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] -InputObject <PsPolicyAssignment> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0a055-112">說明</span><span class="sxs-lookup"><span data-stu-id="0a055-112">DESCRIPTION</span></span>
<span data-ttu-id="0a055-113">**AzPolicyAssignment** Cmdlet 會修改原則指派。</span><span class="sxs-lookup"><span data-stu-id="0a055-113">The **Set-AzPolicyAssignment** cmdlet modifies a policy assignment.</span></span>
<span data-ttu-id="0a055-114">依識別碼或名稱和範圍指定作業。</span><span class="sxs-lookup"><span data-stu-id="0a055-114">Specify an assignment by ID or by name and scope.</span></span>

## <span data-ttu-id="0a055-115">示例</span><span class="sxs-lookup"><span data-stu-id="0a055-115">EXAMPLES</span></span>

### <span data-ttu-id="0a055-116">範例1：更新顯示名稱</span><span class="sxs-lookup"><span data-stu-id="0a055-116">Example 1: Update the display name</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment' -Scope $ResourceGroup.ResourceId
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -DisplayName 'Do not allow VM creation'
```

<span data-ttu-id="0a055-117">第一個命令會使用 Get-AzResourceGroup Cmdlet 來取得名為 ResourceGroup11 的資源群組。</span><span class="sxs-lookup"><span data-stu-id="0a055-117">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="0a055-118">該命令會將該物件儲存在 $ResourceGroup 變數中。</span><span class="sxs-lookup"><span data-stu-id="0a055-118">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="0a055-119">第二個命令會使用 Get-AzPolicyAssignment Cmdlet 來取得名為 PolicyAssignment 的原則指派。</span><span class="sxs-lookup"><span data-stu-id="0a055-119">The second command gets the policy assignment named PolicyAssignment by using the Get-AzPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="0a055-120">該命令會將該物件儲存在 $PolicyAssignment 變數中。</span><span class="sxs-lookup"><span data-stu-id="0a055-120">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="0a055-121">最後一個命令會更新由 $ResourceGroup 的 **ResourceId** 屬性所識別之資源群組上的原則指派顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="0a055-121">The final command updates the display name on the policy assignment on the resource group identified by the **ResourceId** property of $ResourceGroup.</span></span>

### <span data-ttu-id="0a055-122">範例2：在原則指派中加入 managed 身分識別</span><span class="sxs-lookup"><span data-stu-id="0a055-122">Example 2: Add a managed identity to the policy assignment</span></span>
```
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment'
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -AssignIdentity -Location 'westus'
```

<span data-ttu-id="0a055-123">第一個命令會使用 Get-AzPolicyAssignment Cmdlet，從目前訂閱取得名為 PolicyAssignment 的原則指派。</span><span class="sxs-lookup"><span data-stu-id="0a055-123">The first command gets the policy assignment named PolicyAssignment from the current subscription by using the Get-AzPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="0a055-124">該命令會將該物件儲存在 $PolicyAssignment 變數中。</span><span class="sxs-lookup"><span data-stu-id="0a055-124">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="0a055-125">最終命令會為原則指派指派受管理的身分識別。</span><span class="sxs-lookup"><span data-stu-id="0a055-125">The final command assigns a managed identity to the policy assignment.</span></span>

### <span data-ttu-id="0a055-126">範例3：使用新的 policy 參數物件更新原則指派參數</span><span class="sxs-lookup"><span data-stu-id="0a055-126">Example 3: Update policy assignment parameters with new policy parameter object</span></span>
```
PS C:\> $Locations = Get-AzLocation | where {($_.displayname -like 'france*') -or ($_.displayname -like 'uk*')}
PS C:\> $AllowedLocations = @{'listOfAllowedLocations'=($Locations.location)}
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment'
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -PolicyParameterObject $AllowedLocations
```

<span data-ttu-id="0a055-127">第一個和第二個命令會建立一個物件，其中包含名稱以 "華北" 或 "uk" 開頭的所有 Azure 區域。</span><span class="sxs-lookup"><span data-stu-id="0a055-127">The first and second commands create an object containing all Azure regions whose names start with "france" or "uk".</span></span>
<span data-ttu-id="0a055-128">第二個命令會將該物件儲存在 $AllowedLocations 變數中。</span><span class="sxs-lookup"><span data-stu-id="0a055-128">The second command stores that object in the $AllowedLocations variable.</span></span>
<span data-ttu-id="0a055-129">第三個命令會取得名為「PolicyAssignment」的原則指派，命令會將該物件儲存在 $PolicyAssignment 變數中。</span><span class="sxs-lookup"><span data-stu-id="0a055-129">The third command gets the policy assignment named 'PolicyAssignment' The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="0a055-130">Final 命令會更新名為 PolicyAssignment 的原則指派上的參數值。</span><span class="sxs-lookup"><span data-stu-id="0a055-130">The final command updates the parameter values on the policy assignment named PolicyAssignment.</span></span>

### <span data-ttu-id="0a055-131">範例4：使用原則參數檔案更新原則指派參數</span><span class="sxs-lookup"><span data-stu-id="0a055-131">Example 4: Update policy assignment parameters with policy parameter file</span></span>
<span data-ttu-id="0a055-132">在本機工作目錄中，使用下列內容來建立名為 _AllowedLocations.js_ 的檔案。</span><span class="sxs-lookup"><span data-stu-id="0a055-132">Create a file called _AllowedLocations.json_ in the local working directory with the following content.</span></span>

```
{
    "listOfAllowedLocations":  {
      "value": [
        "uksouth",
        "ukwest",
        "francecentral",
        "francesouth"
      ]
    }
}
```

```
PS C:\> Set-AzPolicyAssignment -Name 'PolicyAssignment' -PolicyParameter .\AllowedLocations.json
```

<span data-ttu-id="0a055-133">這個命令會使用本機工作目錄中的原則 AllowedLocations.js參數檔案，更新名為「PolicyAssignment」的原則指派。</span><span class="sxs-lookup"><span data-stu-id="0a055-133">The command updates the policy assignment named 'PolicyAssignment' using the policy parameter file AllowedLocations.json from the local working directory.</span></span>

### <span data-ttu-id="0a055-134">範例5：更新 enforcementMode</span><span class="sxs-lookup"><span data-stu-id="0a055-134">Example 5: Update an enforcementMode</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment' -Scope $ResourceGroup.ResourceId
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -EnforcementMode Default
```

<span data-ttu-id="0a055-135">第一個命令會使用 Get-AzResourceGroup Cmdlet 來取得名為 ResourceGroup11 的資源群組。</span><span class="sxs-lookup"><span data-stu-id="0a055-135">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="0a055-136">該命令會將該物件儲存在 $ResourceGroup 變數中。</span><span class="sxs-lookup"><span data-stu-id="0a055-136">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="0a055-137">第二個命令會使用 Get-AzPolicyAssignment Cmdlet 來取得名為 PolicyAssignment 的原則指派。</span><span class="sxs-lookup"><span data-stu-id="0a055-137">The second command gets the policy assignment named PolicyAssignment by using the Get-AzPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="0a055-138">該命令會將該物件儲存在 $PolicyAssignment 變數中。</span><span class="sxs-lookup"><span data-stu-id="0a055-138">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="0a055-139">Final 命令會更新由 $ResourceGroup 的 **ResourceId** 屬性所識別之資源群組上的原則指派的 enforcementMode 屬性。</span><span class="sxs-lookup"><span data-stu-id="0a055-139">The final command updates the enforcementMode property on the policy assignment on the resource group identified by the **ResourceId** property of $ResourceGroup.</span></span>

## <span data-ttu-id="0a055-140">參數</span><span class="sxs-lookup"><span data-stu-id="0a055-140">PARAMETERS</span></span>

### <span data-ttu-id="0a055-141">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="0a055-141">-ApiVersion</span></span>
<span data-ttu-id="0a055-142">指定要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="0a055-142">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="0a055-143">如果您沒有指定版本，此 Cmdlet 會使用最新的可用版本。</span><span class="sxs-lookup"><span data-stu-id="0a055-143">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="0a055-144">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="0a055-144">-AssignIdentity</span></span>
<span data-ttu-id="0a055-145">針對此原則指派產生並指派 Azure Active Directory 身分識別。</span><span class="sxs-lookup"><span data-stu-id="0a055-145">Generate and assign an Azure Active Directory Identity for this policy assignment.</span></span> <span data-ttu-id="0a055-146">在執行「deployIfNotExists」原則的部署時，就會使用該身分識別。</span><span class="sxs-lookup"><span data-stu-id="0a055-146">The identity will be used when executing deployments for 'deployIfNotExists' policies.</span></span> <span data-ttu-id="0a055-147">指派身分識別時，位置是必要的。</span><span class="sxs-lookup"><span data-stu-id="0a055-147">Location is required when assigning an identity.</span></span>

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

### <span data-ttu-id="0a055-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a055-148">-DefaultProfile</span></span>
<span data-ttu-id="0a055-149">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="0a055-149">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0a055-150">-描述</span><span class="sxs-lookup"><span data-stu-id="0a055-150">-Description</span></span>
<span data-ttu-id="0a055-151">原則指派的描述</span><span class="sxs-lookup"><span data-stu-id="0a055-151">The description for policy assignment</span></span>

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

### <span data-ttu-id="0a055-152">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="0a055-152">-DisplayName</span></span>
<span data-ttu-id="0a055-153">指定原則指派的新顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="0a055-153">Specifies a new display name for the policy assignment.</span></span>

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

### <span data-ttu-id="0a055-154">-EnforcementMode</span><span class="sxs-lookup"><span data-stu-id="0a055-154">-EnforcementMode</span></span>
<span data-ttu-id="0a055-155">原則指派的強制模式。</span><span class="sxs-lookup"><span data-stu-id="0a055-155">The enforcement mode for policy assignment.</span></span> <span data-ttu-id="0a055-156">目前，有效值為預設值，DoNotEnforce。</span><span class="sxs-lookup"><span data-stu-id="0a055-156">Currently, valid values are Default, DoNotEnforce.</span></span>

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

### <span data-ttu-id="0a055-157">-識別碼</span><span class="sxs-lookup"><span data-stu-id="0a055-157">-Id</span></span>
<span data-ttu-id="0a055-158">指定此 Cmdlet 所修改之原則指派的完全限定資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="0a055-158">Specifies the fully qualified resource ID for the policy assignment that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet, PolicyParameterIdObjectParameterSet, PolicyParameterIdStringParameterSet
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a055-159">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0a055-159">-InputObject</span></span>
<span data-ttu-id="0a055-160">要從另一個 Cmdlet 輸出的 [要更新的原則指派] 物件。</span><span class="sxs-lookup"><span data-stu-id="0a055-160">The policy assignment object to update that was output from another cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.Policy.PsPolicyAssignment
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0a055-161">-位置</span><span class="sxs-lookup"><span data-stu-id="0a055-161">-Location</span></span>
<span data-ttu-id="0a055-162">原則指派資源身分識別的位置。</span><span class="sxs-lookup"><span data-stu-id="0a055-162">The location of the policy assignment's resource identity.</span></span> <span data-ttu-id="0a055-163">使用-AssignIdentity 切換時，這是必要的。</span><span class="sxs-lookup"><span data-stu-id="0a055-163">This is required when the -AssignIdentity switch is used.</span></span>

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

### <span data-ttu-id="0a055-164">-中繼資料</span><span class="sxs-lookup"><span data-stu-id="0a055-164">-Metadata</span></span>
<span data-ttu-id="0a055-165">原則指派的更新中繼資料。</span><span class="sxs-lookup"><span data-stu-id="0a055-165">The updated metadata for the policy assignment.</span></span> <span data-ttu-id="0a055-166">這可以是包含中繼資料之檔案名的路徑，或是中繼資料作為字串。</span><span class="sxs-lookup"><span data-stu-id="0a055-166">This can either be a path to a file name containing the metadata, or the metadata as a string.</span></span>

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

### <span data-ttu-id="0a055-167">-名稱</span><span class="sxs-lookup"><span data-stu-id="0a055-167">-Name</span></span>
<span data-ttu-id="0a055-168">指定此 Cmdlet 所修改之原則指派的名稱。</span><span class="sxs-lookup"><span data-stu-id="0a055-168">Specifies the name of the policy assignment that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet, PolicyParameterNameObjectParameterSet, PolicyParameterNameStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a055-169">-NotScope</span><span class="sxs-lookup"><span data-stu-id="0a055-169">-NotScope</span></span>
<span data-ttu-id="0a055-170">原則指派不是作用中的範圍。</span><span class="sxs-lookup"><span data-stu-id="0a055-170">The policy assignment not scopes.</span></span>

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

### <span data-ttu-id="0a055-171">-PolicyParameter</span><span class="sxs-lookup"><span data-stu-id="0a055-171">-PolicyParameter</span></span>
<span data-ttu-id="0a055-172">原則指派的新原則參數檔路徑或字串。</span><span class="sxs-lookup"><span data-stu-id="0a055-172">The new policy parameters file path or string for the policy assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyParameterNameStringParameterSet, PolicyParameterIdStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a055-173">-PolicyParameterObject</span><span class="sxs-lookup"><span data-stu-id="0a055-173">-PolicyParameterObject</span></span>
<span data-ttu-id="0a055-174">原則指派的新原則參數物件。</span><span class="sxs-lookup"><span data-stu-id="0a055-174">The new policy parameters object for the policy assignment.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: PolicyParameterNameObjectParameterSet, PolicyParameterIdObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a055-175">-預先</span><span class="sxs-lookup"><span data-stu-id="0a055-175">-Pre</span></span>
<span data-ttu-id="0a055-176">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="0a055-176">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="0a055-177">-範圍</span><span class="sxs-lookup"><span data-stu-id="0a055-177">-Scope</span></span>
<span data-ttu-id="0a055-178">指定應用原則的範圍。</span><span class="sxs-lookup"><span data-stu-id="0a055-178">Specifies the scope at which the policy is applied.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet, PolicyParameterNameObjectParameterSet, PolicyParameterNameStringParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a055-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a055-179">CommonParameters</span></span>
<span data-ttu-id="0a055-180">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0a055-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a055-181">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="0a055-181">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a055-182">輸入</span><span class="sxs-lookup"><span data-stu-id="0a055-182">INPUTS</span></span>

### <span data-ttu-id="0a055-183">System.object</span><span class="sxs-lookup"><span data-stu-id="0a055-183">System.String</span></span>

### <span data-ttu-id="0a055-184">System.object []</span><span class="sxs-lookup"><span data-stu-id="0a055-184">System.String[]</span></span>

## <span data-ttu-id="0a055-185">輸出</span><span class="sxs-lookup"><span data-stu-id="0a055-185">OUTPUTS</span></span>

### <span data-ttu-id="0a055-186">系統管理. PSObject</span><span class="sxs-lookup"><span data-stu-id="0a055-186">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="0a055-187">筆記</span><span class="sxs-lookup"><span data-stu-id="0a055-187">NOTES</span></span>

## <span data-ttu-id="0a055-188">相關連結</span><span class="sxs-lookup"><span data-stu-id="0a055-188">RELATED LINKS</span></span>

[<span data-ttu-id="0a055-189">AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="0a055-189">Get-AzPolicyAssignment</span></span>](./Get-AzPolicyAssignment.md)

[<span data-ttu-id="0a055-190">新-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="0a055-190">New-AzPolicyAssignment</span></span>](./New-AzPolicyAssignment.md)

[<span data-ttu-id="0a055-191">移除-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="0a055-191">Remove-AzPolicyAssignment</span></span>](./Remove-AzPolicyAssignment.md)


