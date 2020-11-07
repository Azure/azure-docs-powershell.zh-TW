---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C3B2C33F-8BD4-4E31-9450-EF6A3A6A5325
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyAssignment.md
ms.openlocfilehash: ab0617b4012ca623bf67471a9a5bcc3ccf54d905
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93957678"
---
# <span data-ttu-id="4500b-101">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="4500b-101">Set-AzPolicyAssignment</span></span>

## <span data-ttu-id="4500b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4500b-102">SYNOPSIS</span></span>
<span data-ttu-id="4500b-103">修改原則分派。</span><span class="sxs-lookup"><span data-stu-id="4500b-103">Modifies a policy assignment.</span></span>

## <span data-ttu-id="4500b-104">句法</span><span class="sxs-lookup"><span data-stu-id="4500b-104">SYNTAX</span></span>

### <span data-ttu-id="4500b-105">NameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="4500b-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Metadata <String>] [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4500b-106">PolicyParameterNameObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4500b-106">PolicyParameterNameObjectParameterSet</span></span>
```
Set-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Metadata <String>] -PolicyParameterObject <Hashtable> [-AssignIdentity]
 [-Location <String>] [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4500b-107">PolicyParameterNameStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="4500b-107">PolicyParameterNameStringParameterSet</span></span>
```
Set-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Metadata <String>] -PolicyParameter <String> [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4500b-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4500b-108">IdParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] -Id <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4500b-109">PolicyParameterIdObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4500b-109">PolicyParameterIdObjectParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] -Id <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] -PolicyParameterObject <Hashtable> [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4500b-110">PolicyParameterIdStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="4500b-110">PolicyParameterIdStringParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] -Id <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] -PolicyParameter <String> [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4500b-111">說明</span><span class="sxs-lookup"><span data-stu-id="4500b-111">DESCRIPTION</span></span>
<span data-ttu-id="4500b-112">**AzPolicyAssignment** Cmdlet 會修改原則指派。</span><span class="sxs-lookup"><span data-stu-id="4500b-112">The **Set-AzPolicyAssignment** cmdlet modifies a policy assignment.</span></span>
<span data-ttu-id="4500b-113">依識別碼或名稱和範圍指定作業。</span><span class="sxs-lookup"><span data-stu-id="4500b-113">Specify an assignment by ID or by name and scope.</span></span>

## <span data-ttu-id="4500b-114">示例</span><span class="sxs-lookup"><span data-stu-id="4500b-114">EXAMPLES</span></span>

### <span data-ttu-id="4500b-115">範例1：更新顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4500b-115">Example 1: Update the display name</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment' -Scope $ResourceGroup.ResourceId
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -DisplayName 'Do not allow VM creation'
```

<span data-ttu-id="4500b-116">第一個命令會使用 Get-AzResourceGroup Cmdlet 來取得名為 ResourceGroup11 的資源群組。</span><span class="sxs-lookup"><span data-stu-id="4500b-116">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="4500b-117">該命令會將該物件儲存在 $ResourceGroup 變數中。</span><span class="sxs-lookup"><span data-stu-id="4500b-117">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="4500b-118">第二個命令會使用 Get-AzPolicyAssignment Cmdlet 來取得名為 PolicyAssignment 的原則指派。</span><span class="sxs-lookup"><span data-stu-id="4500b-118">The second command gets the policy assignment named PolicyAssignment by using the Get-AzPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="4500b-119">該命令會將該物件儲存在 $PolicyAssignment 變數中。</span><span class="sxs-lookup"><span data-stu-id="4500b-119">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="4500b-120">最後一個命令會更新由 $ResourceGroup 的 **ResourceId** 屬性所識別之資源群組上的原則指派顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="4500b-120">The final command updates the display name on the policy assignment on the resource group identified by the **ResourceId** property of $ResourceGroup.</span></span>

### <span data-ttu-id="4500b-121">範例2：在原則指派中加入 managed 身分識別</span><span class="sxs-lookup"><span data-stu-id="4500b-121">Example 2: Add a managed identity to the policy assignment</span></span>
```
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment'
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -AssignIdentity -Location 'westus'
```

<span data-ttu-id="4500b-122">第一個命令會使用 Get-AzPolicyAssignment Cmdlet，從目前訂閱取得名為 PolicyAssignment 的原則指派。</span><span class="sxs-lookup"><span data-stu-id="4500b-122">The first command gets the policy assignment named PolicyAssignment from the current subscription by using the Get-AzPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="4500b-123">該命令會將該物件儲存在 $PolicyAssignment 變數中。</span><span class="sxs-lookup"><span data-stu-id="4500b-123">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="4500b-124">最終命令會為原則指派指派受管理的身分識別。</span><span class="sxs-lookup"><span data-stu-id="4500b-124">The final command assigns a managed identity to the policy assignment.</span></span>

### <span data-ttu-id="4500b-125">範例3：使用新的 policy 參數物件更新原則指派參數</span><span class="sxs-lookup"><span data-stu-id="4500b-125">Example 3: Update policy assignment parameters with new policy parameter object</span></span>
```
PS C:\> $Locations = Get-AzLocation | where {($_.displayname -like 'france*') -or ($_.displayname -like 'uk*')}
PS C:\> $AllowedLocations = @{'listOfAllowedLocations'=($Locations.location)}
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment'
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -PolicyParameterObject $AllowedLocations
```

<span data-ttu-id="4500b-126">第一個和第二個命令會建立一個物件，其中包含名稱以 "華北" 或 "uk" 開頭的所有 Azure 區域。</span><span class="sxs-lookup"><span data-stu-id="4500b-126">The first and second commands create an object containing all Azure regions whose names start with "france" or "uk".</span></span>
<span data-ttu-id="4500b-127">第二個命令會將該物件儲存在 $AllowedLocations 變數中。</span><span class="sxs-lookup"><span data-stu-id="4500b-127">The second command stores that object in the $AllowedLocations variable.</span></span>
<span data-ttu-id="4500b-128">第三個命令會取得名為「PolicyAssignment」的原則指派，命令會將該物件儲存在 $PolicyAssignment 變數中。</span><span class="sxs-lookup"><span data-stu-id="4500b-128">The third command gets the policy assignment named 'PolicyAssignment' The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="4500b-129">Final 命令會更新名為 PolicyAssignment 的原則指派上的參數值。</span><span class="sxs-lookup"><span data-stu-id="4500b-129">The final command updates the parameter values on the policy assignment named PolicyAssignment.</span></span>

### <span data-ttu-id="4500b-130">範例4：使用原則參數檔案更新原則指派參數</span><span class="sxs-lookup"><span data-stu-id="4500b-130">Example 4: Update policy assignment parameters with policy parameter file</span></span>
<span data-ttu-id="4500b-131">在本機工作目錄中，使用下列內容來建立名為 _AllowedLocations.js_ 的檔案。</span><span class="sxs-lookup"><span data-stu-id="4500b-131">Create a file called _AllowedLocations.json_ in the local working directory with the following content.</span></span>

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

<span data-ttu-id="4500b-132">這個命令會使用本機工作目錄中的原則 AllowedLocations.js參數檔案，更新名為「PolicyAssignment」的原則指派。</span><span class="sxs-lookup"><span data-stu-id="4500b-132">The command updates the policy assignment named 'PolicyAssignment' using the policy parameter file AllowedLocations.json from the local working directory.</span></span>

### <span data-ttu-id="4500b-133">範例5：更新 enforcementMode</span><span class="sxs-lookup"><span data-stu-id="4500b-133">Example 5: Update an enforcementMode</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment' -Scope $ResourceGroup.ResourceId
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -EnforcementMode Default
```

<span data-ttu-id="4500b-134">第一個命令會使用 Get-AzResourceGroup Cmdlet 來取得名為 ResourceGroup11 的資源群組。</span><span class="sxs-lookup"><span data-stu-id="4500b-134">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="4500b-135">該命令會將該物件儲存在 $ResourceGroup 變數中。</span><span class="sxs-lookup"><span data-stu-id="4500b-135">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="4500b-136">第二個命令會使用 Get-AzPolicyAssignment Cmdlet 來取得名為 PolicyAssignment 的原則指派。</span><span class="sxs-lookup"><span data-stu-id="4500b-136">The second command gets the policy assignment named PolicyAssignment by using the Get-AzPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="4500b-137">該命令會將該物件儲存在 $PolicyAssignment 變數中。</span><span class="sxs-lookup"><span data-stu-id="4500b-137">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="4500b-138">Final 命令會更新由 $ResourceGroup 的 **ResourceId** 屬性所識別之資源群組上的原則指派的 enforcementMode 屬性。</span><span class="sxs-lookup"><span data-stu-id="4500b-138">The final command updates the enforcementMode property on the policy assignment on the resource group identified by the **ResourceId** property of $ResourceGroup.</span></span>

## <span data-ttu-id="4500b-139">參數</span><span class="sxs-lookup"><span data-stu-id="4500b-139">PARAMETERS</span></span>

### <span data-ttu-id="4500b-140">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="4500b-140">-ApiVersion</span></span>
<span data-ttu-id="4500b-141">指定要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="4500b-141">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="4500b-142">如果您沒有指定版本，此 Cmdlet 會使用最新的可用版本。</span><span class="sxs-lookup"><span data-stu-id="4500b-142">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="4500b-143">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="4500b-143">-AssignIdentity</span></span>
<span data-ttu-id="4500b-144">針對此原則指派產生並指派 Azure Active Directory 身分識別。</span><span class="sxs-lookup"><span data-stu-id="4500b-144">Generate and assign an Azure Active Directory Identity for this policy assignment.</span></span> <span data-ttu-id="4500b-145">在執行「deployIfNotExists」原則的部署時，就會使用該身分識別。</span><span class="sxs-lookup"><span data-stu-id="4500b-145">The identity will be used when executing deployments for 'deployIfNotExists' policies.</span></span> <span data-ttu-id="4500b-146">指派身分識別時，位置是必要的。</span><span class="sxs-lookup"><span data-stu-id="4500b-146">Location is required when assigning an identity.</span></span>

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

### <span data-ttu-id="4500b-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4500b-147">-DefaultProfile</span></span>
<span data-ttu-id="4500b-148">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="4500b-148">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4500b-149">-描述</span><span class="sxs-lookup"><span data-stu-id="4500b-149">-Description</span></span>
<span data-ttu-id="4500b-150">原則指派的描述</span><span class="sxs-lookup"><span data-stu-id="4500b-150">The description for policy assignment</span></span>

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

### <span data-ttu-id="4500b-151">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="4500b-151">-DisplayName</span></span>
<span data-ttu-id="4500b-152">指定原則指派的新顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="4500b-152">Specifies a new display name for the policy assignment.</span></span>

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

### <span data-ttu-id="4500b-153">-EnforcementMode</span><span class="sxs-lookup"><span data-stu-id="4500b-153">-EnforcementMode</span></span>
<span data-ttu-id="4500b-154">原則指派的強制模式。</span><span class="sxs-lookup"><span data-stu-id="4500b-154">The enforcement mode for policy assignment.</span></span> <span data-ttu-id="4500b-155">目前，有效值為預設值，DoNotEnforce。</span><span class="sxs-lookup"><span data-stu-id="4500b-155">Currently, valid values are Default, DoNotEnforce.</span></span>

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

### <span data-ttu-id="4500b-156">-識別碼</span><span class="sxs-lookup"><span data-stu-id="4500b-156">-Id</span></span>
<span data-ttu-id="4500b-157">指定此 Cmdlet 所修改之原則指派的完全限定資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="4500b-157">Specifies the fully qualified resource ID for the policy assignment that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="4500b-158">-位置</span><span class="sxs-lookup"><span data-stu-id="4500b-158">-Location</span></span>
<span data-ttu-id="4500b-159">原則指派資源身分識別的位置。</span><span class="sxs-lookup"><span data-stu-id="4500b-159">The location of the policy assignment's resource identity.</span></span> <span data-ttu-id="4500b-160">使用-AssignIdentity 切換時，這是必要的。</span><span class="sxs-lookup"><span data-stu-id="4500b-160">This is required when the -AssignIdentity switch is used.</span></span>

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

### <span data-ttu-id="4500b-161">-中繼資料</span><span class="sxs-lookup"><span data-stu-id="4500b-161">-Metadata</span></span>
<span data-ttu-id="4500b-162">原則指派的更新中繼資料。</span><span class="sxs-lookup"><span data-stu-id="4500b-162">The updated metadata for the policy assignment.</span></span> <span data-ttu-id="4500b-163">這可以是包含中繼資料之檔案名的路徑，或是中繼資料作為字串。</span><span class="sxs-lookup"><span data-stu-id="4500b-163">This can either be a path to a file name containing the metadata, or the metadata as a string.</span></span>

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

### <span data-ttu-id="4500b-164">-名稱</span><span class="sxs-lookup"><span data-stu-id="4500b-164">-Name</span></span>
<span data-ttu-id="4500b-165">指定此 Cmdlet 所修改之原則指派的名稱。</span><span class="sxs-lookup"><span data-stu-id="4500b-165">Specifies the name of the policy assignment that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="4500b-166">-NotScope</span><span class="sxs-lookup"><span data-stu-id="4500b-166">-NotScope</span></span>
<span data-ttu-id="4500b-167">原則指派不是作用中的範圍。</span><span class="sxs-lookup"><span data-stu-id="4500b-167">The policy assignment not scopes.</span></span>

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

### <span data-ttu-id="4500b-168">-PolicyParameter</span><span class="sxs-lookup"><span data-stu-id="4500b-168">-PolicyParameter</span></span>
<span data-ttu-id="4500b-169">原則指派的新原則參數檔路徑或字串。</span><span class="sxs-lookup"><span data-stu-id="4500b-169">The new policy parameters file path or string for the policy assignment.</span></span>

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

### <span data-ttu-id="4500b-170">-PolicyParameterObject</span><span class="sxs-lookup"><span data-stu-id="4500b-170">-PolicyParameterObject</span></span>
<span data-ttu-id="4500b-171">原則指派的新原則參數物件。</span><span class="sxs-lookup"><span data-stu-id="4500b-171">The new policy parameters object for the policy assignment.</span></span>

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

### <span data-ttu-id="4500b-172">-預先</span><span class="sxs-lookup"><span data-stu-id="4500b-172">-Pre</span></span>
<span data-ttu-id="4500b-173">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="4500b-173">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="4500b-174">-範圍</span><span class="sxs-lookup"><span data-stu-id="4500b-174">-Scope</span></span>
<span data-ttu-id="4500b-175">指定應用原則的範圍。</span><span class="sxs-lookup"><span data-stu-id="4500b-175">Specifies the scope at which the policy is applied.</span></span>

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

### <span data-ttu-id="4500b-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4500b-176">CommonParameters</span></span>
<span data-ttu-id="4500b-177">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4500b-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4500b-178">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="4500b-178">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4500b-179">輸入</span><span class="sxs-lookup"><span data-stu-id="4500b-179">INPUTS</span></span>

### <span data-ttu-id="4500b-180">System.object</span><span class="sxs-lookup"><span data-stu-id="4500b-180">System.String</span></span>

### <span data-ttu-id="4500b-181">System.object []</span><span class="sxs-lookup"><span data-stu-id="4500b-181">System.String[]</span></span>

## <span data-ttu-id="4500b-182">輸出</span><span class="sxs-lookup"><span data-stu-id="4500b-182">OUTPUTS</span></span>

### <span data-ttu-id="4500b-183">系統管理. PSObject</span><span class="sxs-lookup"><span data-stu-id="4500b-183">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="4500b-184">筆記</span><span class="sxs-lookup"><span data-stu-id="4500b-184">NOTES</span></span>

## <span data-ttu-id="4500b-185">相關連結</span><span class="sxs-lookup"><span data-stu-id="4500b-185">RELATED LINKS</span></span>

[<span data-ttu-id="4500b-186">AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="4500b-186">Get-AzPolicyAssignment</span></span>](./Get-AzPolicyAssignment.md)

[<span data-ttu-id="4500b-187">新-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="4500b-187">New-AzPolicyAssignment</span></span>](./New-AzPolicyAssignment.md)

[<span data-ttu-id="4500b-188">移除-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="4500b-188">Remove-AzPolicyAssignment</span></span>](./Remove-AzPolicyAssignment.md)


