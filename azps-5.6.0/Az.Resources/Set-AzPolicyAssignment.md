---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C3B2C33F-8BD4-4E31-9450-EF6A3A6A5325
online version: https://docs.microsoft.com/powershell/module/az.resources/set-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyAssignment.md
ms.openlocfilehash: dcfc63c1dbf36cf7c592fe8fc7eb5afae09dc4e0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916897"
---
# <span data-ttu-id="c1a10-101">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="c1a10-101">Set-AzPolicyAssignment</span></span>

## <span data-ttu-id="c1a10-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c1a10-102">SYNOPSIS</span></span>
<span data-ttu-id="c1a10-103">修改策略指派。</span><span class="sxs-lookup"><span data-stu-id="c1a10-103">Modifies a policy assignment.</span></span>

## <span data-ttu-id="c1a10-104">語法</span><span class="sxs-lookup"><span data-stu-id="c1a10-104">SYNTAX</span></span>

### <span data-ttu-id="c1a10-105">NameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="c1a10-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Metadata <String>] [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c1a10-106">PolicyParameterNameObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c1a10-106">PolicyParameterNameObjectParameterSet</span></span>
```
Set-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Metadata <String>] -PolicyParameterObject <Hashtable> [-AssignIdentity]
 [-Location <String>] [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c1a10-107">PolicyParameterNameStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="c1a10-107">PolicyParameterNameStringParameterSet</span></span>
```
Set-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Metadata <String>] -PolicyParameter <String> [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c1a10-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c1a10-108">IdParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] -Id <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c1a10-109">PolicyParameterIdObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c1a10-109">PolicyParameterIdObjectParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] -Id <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] -PolicyParameterObject <Hashtable> [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c1a10-110">PolicyParameterIdStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="c1a10-110">PolicyParameterIdStringParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] -Id <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] -PolicyParameter <String> [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c1a10-111">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c1a10-111">InputObjectParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] -InputObject <PsPolicyAssignment> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c1a10-112">描述</span><span class="sxs-lookup"><span data-stu-id="c1a10-112">DESCRIPTION</span></span>
<span data-ttu-id="c1a10-113">**Set-AzPolicyAssignment Cmdlet** 會修改一個策略指派。</span><span class="sxs-lookup"><span data-stu-id="c1a10-113">The **Set-AzPolicyAssignment** cmdlet modifies a policy assignment.</span></span>
<span data-ttu-id="c1a10-114">根據識別碼或名稱和範圍指定作業。</span><span class="sxs-lookup"><span data-stu-id="c1a10-114">Specify an assignment by ID or by name and scope.</span></span>

## <span data-ttu-id="c1a10-115">例子</span><span class="sxs-lookup"><span data-stu-id="c1a10-115">EXAMPLES</span></span>

### <span data-ttu-id="c1a10-116">範例 1：更新顯示名稱</span><span class="sxs-lookup"><span data-stu-id="c1a10-116">Example 1: Update the display name</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment' -Scope $ResourceGroup.ResourceId
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -DisplayName 'Do not allow VM creation'
```

<span data-ttu-id="c1a10-117">第一個命令會使用 Get-AzResourceGroup Cmdlet，獲得一個名為 ResourceGroup11 的資源群組。</span><span class="sxs-lookup"><span data-stu-id="c1a10-117">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="c1a10-118">該命令將該物件儲存在$ResourceGroup變數中。</span><span class="sxs-lookup"><span data-stu-id="c1a10-118">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="c1a10-119">第二個命令會使用 Get-AzPolicyAssignment Cmdlet，獲得名為 PolicyAssignmentGet-AzPolicyAssignment指派。</span><span class="sxs-lookup"><span data-stu-id="c1a10-119">The second command gets the policy assignment named PolicyAssignment by using the Get-AzPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="c1a10-120">該命令將該物件儲存在$PolicyAssignment變數中。</span><span class="sxs-lookup"><span data-stu-id="c1a10-120">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="c1a10-121">最後一個命令會更新由 **resourceId** 屬性所識別之資源群組上的顯示名稱$ResourceGroup。</span><span class="sxs-lookup"><span data-stu-id="c1a10-121">The final command updates the display name on the policy assignment on the resource group identified by the **ResourceId** property of $ResourceGroup.</span></span>

### <span data-ttu-id="c1a10-122">範例 2：新增受管理的身分識別至策略指派</span><span class="sxs-lookup"><span data-stu-id="c1a10-122">Example 2: Add a managed identity to the policy assignment</span></span>
```
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment'
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -AssignIdentity -Location 'westus'
```

<span data-ttu-id="c1a10-123">第一個命令會使用 Get-AzPolicyAssignment Cmdlet，從目前的訂閱獲得名為 PolicyAssignmentGet-AzPolicyAssignment指派。</span><span class="sxs-lookup"><span data-stu-id="c1a10-123">The first command gets the policy assignment named PolicyAssignment from the current subscription by using the Get-AzPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="c1a10-124">該命令將該物件儲存在$PolicyAssignment變數中。</span><span class="sxs-lookup"><span data-stu-id="c1a10-124">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="c1a10-125">最後一個命令會指派受管理的身分識別給該策略指派。</span><span class="sxs-lookup"><span data-stu-id="c1a10-125">The final command assigns a managed identity to the policy assignment.</span></span>

### <span data-ttu-id="c1a10-126">範例 3：使用新的策略參數物件更新策略指派參數</span><span class="sxs-lookup"><span data-stu-id="c1a10-126">Example 3: Update policy assignment parameters with new policy parameter object</span></span>
```
PS C:\> $Locations = Get-AzLocation | where {($_.displayname -like 'france*') -or ($_.displayname -like 'uk*')}
PS C:\> $AllowedLocations = @{'listOfAllowedLocations'=($Locations.location)}
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment'
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -PolicyParameterObject $AllowedLocations
```

<span data-ttu-id="c1a10-127">第一個和第二個命令會建立一個物件，其中包含名稱以 "france" 或 "uk" 做為名字的所有 Azure 區域。</span><span class="sxs-lookup"><span data-stu-id="c1a10-127">The first and second commands create an object containing all Azure regions whose names start with "france" or "uk".</span></span>
<span data-ttu-id="c1a10-128">第二個命令將該物件儲存在$AllowedLocations變數中。</span><span class="sxs-lookup"><span data-stu-id="c1a10-128">The second command stores that object in the $AllowedLocations variable.</span></span>
<span data-ttu-id="c1a10-129">第三個命令會獲得名為'PolicyAssignment'的命令，該命令會儲存該物件$PolicyAssignment變數。</span><span class="sxs-lookup"><span data-stu-id="c1a10-129">The third command gets the policy assignment named 'PolicyAssignment' The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="c1a10-130">最後一個命令會更新名為 PolicyAssignment 之策略指派的參數值。</span><span class="sxs-lookup"><span data-stu-id="c1a10-130">The final command updates the parameter values on the policy assignment named PolicyAssignment.</span></span>

### <span data-ttu-id="c1a10-131">範例 4：使用策略參數檔案更新策略指派參數</span><span class="sxs-lookup"><span data-stu-id="c1a10-131">Example 4: Update policy assignment parameters with policy parameter file</span></span>
<span data-ttu-id="c1a10-132">在具有下列內容的 _AllowedLocations.js_ 建立名為AllowedLocations.js的檔案。</span><span class="sxs-lookup"><span data-stu-id="c1a10-132">Create a file called _AllowedLocations.json_ in the local working directory with the following content.</span></span>

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

<span data-ttu-id="c1a10-133">命令會使用來自本地工作目錄AllowedLocations.js參數檔案更新名為'PolicyAssignment」的策略指派。</span><span class="sxs-lookup"><span data-stu-id="c1a10-133">The command updates the policy assignment named 'PolicyAssignment' using the policy parameter file AllowedLocations.json from the local working directory.</span></span>

### <span data-ttu-id="c1a10-134">範例 5：更新強制執行Mode</span><span class="sxs-lookup"><span data-stu-id="c1a10-134">Example 5: Update an enforcementMode</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment' -Scope $ResourceGroup.ResourceId
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -EnforcementMode Default
```

<span data-ttu-id="c1a10-135">第一個命令會使用 Get-AzResourceGroup Cmdlet，獲得一個名為 ResourceGroup11 的資源群組。</span><span class="sxs-lookup"><span data-stu-id="c1a10-135">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="c1a10-136">該命令將該物件儲存在$ResourceGroup變數中。</span><span class="sxs-lookup"><span data-stu-id="c1a10-136">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="c1a10-137">第二個命令會使用 Get-AzPolicyAssignment Cmdlet，獲得名為 PolicyAssignmentGet-AzPolicyAssignment指派。</span><span class="sxs-lookup"><span data-stu-id="c1a10-137">The second command gets the policy assignment named PolicyAssignment by using the Get-AzPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="c1a10-138">該命令將該物件儲存在$PolicyAssignment變數中。</span><span class="sxs-lookup"><span data-stu-id="c1a10-138">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="c1a10-139">最後一個命令會更新由 **resourceId** 屬性識別之資源群組上的強制Mode屬性$ResourceGroup。</span><span class="sxs-lookup"><span data-stu-id="c1a10-139">The final command updates the enforcementMode property on the policy assignment on the resource group identified by the **ResourceId** property of $ResourceGroup.</span></span>

## <span data-ttu-id="c1a10-140">參數</span><span class="sxs-lookup"><span data-stu-id="c1a10-140">PARAMETERS</span></span>

### <span data-ttu-id="c1a10-141">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="c1a10-141">-ApiVersion</span></span>
<span data-ttu-id="c1a10-142">指定要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="c1a10-142">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="c1a10-143">如果您未指定版本，此 Cmdlet 會使用最新的可用版本。</span><span class="sxs-lookup"><span data-stu-id="c1a10-143">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="c1a10-144">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="c1a10-144">-AssignIdentity</span></span>
<span data-ttu-id="c1a10-145">產生並指派此策略指派的 Azure Active Directory 身分識別。</span><span class="sxs-lookup"><span data-stu-id="c1a10-145">Generate and assign an Azure Active Directory Identity for this policy assignment.</span></span> <span data-ttu-id="c1a10-146">身分識別將用於執行 'deployIfNotExists' 策略的部署。</span><span class="sxs-lookup"><span data-stu-id="c1a10-146">The identity will be used when executing deployments for 'deployIfNotExists' policies.</span></span> <span data-ttu-id="c1a10-147">指派身分識別時需要位置。</span><span class="sxs-lookup"><span data-stu-id="c1a10-147">Location is required when assigning an identity.</span></span>

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

### <span data-ttu-id="c1a10-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1a10-148">-DefaultProfile</span></span>
<span data-ttu-id="c1a10-149">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="c1a10-149">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c1a10-150">-描述</span><span class="sxs-lookup"><span data-stu-id="c1a10-150">-Description</span></span>
<span data-ttu-id="c1a10-151">政策指派的描述</span><span class="sxs-lookup"><span data-stu-id="c1a10-151">The description for policy assignment</span></span>

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

### <span data-ttu-id="c1a10-152">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="c1a10-152">-DisplayName</span></span>
<span data-ttu-id="c1a10-153">指定新的顯示名稱，以用於該工作分派。</span><span class="sxs-lookup"><span data-stu-id="c1a10-153">Specifies a new display name for the policy assignment.</span></span>

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

### <span data-ttu-id="c1a10-154">-EnforcementMode</span><span class="sxs-lookup"><span data-stu-id="c1a10-154">-EnforcementMode</span></span>
<span data-ttu-id="c1a10-155">策略指派的強制執行模式。</span><span class="sxs-lookup"><span data-stu-id="c1a10-155">The enforcement mode for policy assignment.</span></span> <span data-ttu-id="c1a10-156">目前，有效的值為 Default、DoNotEnforce。</span><span class="sxs-lookup"><span data-stu-id="c1a10-156">Currently, valid values are Default, DoNotEnforce.</span></span>

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

### <span data-ttu-id="c1a10-157">-Id</span><span class="sxs-lookup"><span data-stu-id="c1a10-157">-Id</span></span>
<span data-ttu-id="c1a10-158">指定此 Cmdlet 修改之策略工作分派的完全合格資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="c1a10-158">Specifies the fully qualified resource ID for the policy assignment that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="c1a10-159">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c1a10-159">-InputObject</span></span>
<span data-ttu-id="c1a10-160">這是要更新從另一個 Cmdlet 輸出的策略指派物件。</span><span class="sxs-lookup"><span data-stu-id="c1a10-160">The policy assignment object to update that was output from another cmdlet.</span></span>

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

### <span data-ttu-id="c1a10-161">-位置</span><span class="sxs-lookup"><span data-stu-id="c1a10-161">-Location</span></span>
<span data-ttu-id="c1a10-162">策略工作分派的資源身分識別位置。</span><span class="sxs-lookup"><span data-stu-id="c1a10-162">The location of the policy assignment's resource identity.</span></span> <span data-ttu-id="c1a10-163">使用 -AssignIdentity 切換時，這是必要的。</span><span class="sxs-lookup"><span data-stu-id="c1a10-163">This is required when the -AssignIdentity switch is used.</span></span>

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

### <span data-ttu-id="c1a10-164">-中繼資料</span><span class="sxs-lookup"><span data-stu-id="c1a10-164">-Metadata</span></span>
<span data-ttu-id="c1a10-165">已更新之策略指派的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="c1a10-165">The updated metadata for the policy assignment.</span></span> <span data-ttu-id="c1a10-166">這可以是包含中繼資料之檔案名的路徑，或以字串形式表示中繼資料。</span><span class="sxs-lookup"><span data-stu-id="c1a10-166">This can either be a path to a file name containing the metadata, or the metadata as a string.</span></span>

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

### <span data-ttu-id="c1a10-167">-名稱</span><span class="sxs-lookup"><span data-stu-id="c1a10-167">-Name</span></span>
<span data-ttu-id="c1a10-168">指定此 Cmdlet 修改之策略指派的名稱。</span><span class="sxs-lookup"><span data-stu-id="c1a10-168">Specifies the name of the policy assignment that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="c1a10-169">-NotScope</span><span class="sxs-lookup"><span data-stu-id="c1a10-169">-NotScope</span></span>
<span data-ttu-id="c1a10-170">非範圍之策略指派。</span><span class="sxs-lookup"><span data-stu-id="c1a10-170">The policy assignment not scopes.</span></span>

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

### <span data-ttu-id="c1a10-171">-PolicyParameter</span><span class="sxs-lookup"><span data-stu-id="c1a10-171">-PolicyParameter</span></span>
<span data-ttu-id="c1a10-172">新的策略參數檔案路徑或該策略指派的字串。</span><span class="sxs-lookup"><span data-stu-id="c1a10-172">The new policy parameters file path or string for the policy assignment.</span></span>

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

### <span data-ttu-id="c1a10-173">-PolicyParameterObject</span><span class="sxs-lookup"><span data-stu-id="c1a10-173">-PolicyParameterObject</span></span>
<span data-ttu-id="c1a10-174">新策略參數物件用於該策略指派。</span><span class="sxs-lookup"><span data-stu-id="c1a10-174">The new policy parameters object for the policy assignment.</span></span>

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

### <span data-ttu-id="c1a10-175">-Pre</span><span class="sxs-lookup"><span data-stu-id="c1a10-175">-Pre</span></span>
<span data-ttu-id="c1a10-176">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮測試版 API 版本。</span><span class="sxs-lookup"><span data-stu-id="c1a10-176">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="c1a10-177">-範圍</span><span class="sxs-lookup"><span data-stu-id="c1a10-177">-Scope</span></span>
<span data-ttu-id="c1a10-178">指定原則的適用範圍。</span><span class="sxs-lookup"><span data-stu-id="c1a10-178">Specifies the scope at which the policy is applied.</span></span>

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

### <span data-ttu-id="c1a10-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1a10-179">CommonParameters</span></span>
<span data-ttu-id="c1a10-180">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c1a10-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1a10-181">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c1a10-181">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1a10-182">輸入</span><span class="sxs-lookup"><span data-stu-id="c1a10-182">INPUTS</span></span>

### <span data-ttu-id="c1a10-183">System.String</span><span class="sxs-lookup"><span data-stu-id="c1a10-183">System.String</span></span>

### <span data-ttu-id="c1a10-184">System.String[]</span><span class="sxs-lookup"><span data-stu-id="c1a10-184">System.String[]</span></span>

## <span data-ttu-id="c1a10-185">輸出</span><span class="sxs-lookup"><span data-stu-id="c1a10-185">OUTPUTS</span></span>

### <span data-ttu-id="c1a10-186">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="c1a10-186">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="c1a10-187">筆記</span><span class="sxs-lookup"><span data-stu-id="c1a10-187">NOTES</span></span>

## <span data-ttu-id="c1a10-188">相關連結</span><span class="sxs-lookup"><span data-stu-id="c1a10-188">RELATED LINKS</span></span>

[<span data-ttu-id="c1a10-189">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="c1a10-189">Get-AzPolicyAssignment</span></span>](./Get-AzPolicyAssignment.md)

[<span data-ttu-id="c1a10-190">New-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="c1a10-190">New-AzPolicyAssignment</span></span>](./New-AzPolicyAssignment.md)

[<span data-ttu-id="c1a10-191">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="c1a10-191">Remove-AzPolicyAssignment</span></span>](./Remove-AzPolicyAssignment.md)


