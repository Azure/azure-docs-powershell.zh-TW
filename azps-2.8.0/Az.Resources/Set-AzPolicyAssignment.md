---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C3B2C33F-8BD4-4E31-9450-EF6A3A6A5325
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyAssignment.md
ms.openlocfilehash: 5d83266e341643adc45a2fc7af8eff1f9a5e0b3b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93792186"
---
# <span data-ttu-id="48722-101">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="48722-101">Set-AzPolicyAssignment</span></span>

## <span data-ttu-id="48722-102">摘要</span><span class="sxs-lookup"><span data-stu-id="48722-102">SYNOPSIS</span></span>
<span data-ttu-id="48722-103">修改原則分派。</span><span class="sxs-lookup"><span data-stu-id="48722-103">Modifies a policy assignment.</span></span>

## <span data-ttu-id="48722-104">句法</span><span class="sxs-lookup"><span data-stu-id="48722-104">SYNTAX</span></span>

### <span data-ttu-id="48722-105">NameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="48722-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Metadata <String>] [-AssignIdentity] [-Location <String>] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="48722-106">PolicyParameterNameObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="48722-106">PolicyParameterNameObjectParameterSet</span></span>
```
Set-AzPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Metadata <String>] -PolicyParameterObject <Hashtable> [-AssignIdentity]
 [-Location <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="48722-107">PolicyParameterNameStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="48722-107">PolicyParameterNameStringParameterSet</span></span>
```
Set-AzPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Metadata <String>] -PolicyParameter <String> [-AssignIdentity] [-Location <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="48722-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="48722-108">IdParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] -Id <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="48722-109">PolicyParameterIdObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="48722-109">PolicyParameterIdObjectParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] -Id <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] -PolicyParameterObject <Hashtable> [-AssignIdentity] [-Location <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="48722-110">PolicyParameterIdStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="48722-110">PolicyParameterIdStringParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] -Id <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] -PolicyParameter <String> [-AssignIdentity] [-Location <String>] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="48722-111">說明</span><span class="sxs-lookup"><span data-stu-id="48722-111">DESCRIPTION</span></span>
<span data-ttu-id="48722-112">**AzPolicyAssignment** Cmdlet 會修改原則指派。</span><span class="sxs-lookup"><span data-stu-id="48722-112">The **Set-AzPolicyAssignment** cmdlet modifies a policy assignment.</span></span>
<span data-ttu-id="48722-113">依識別碼或名稱和範圍指定作業。</span><span class="sxs-lookup"><span data-stu-id="48722-113">Specify an assignment by ID or by name and scope.</span></span>

## <span data-ttu-id="48722-114">示例</span><span class="sxs-lookup"><span data-stu-id="48722-114">EXAMPLES</span></span>

### <span data-ttu-id="48722-115">範例1：更新顯示名稱</span><span class="sxs-lookup"><span data-stu-id="48722-115">Example 1: Update the display name</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment' -Scope $ResourceGroup.ResourceId
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -DisplayName 'Do not allow VM creation'
```

<span data-ttu-id="48722-116">第一個命令會使用 Get-AzResourceGroup Cmdlet 來取得名為 ResourceGroup11 的資源群組。</span><span class="sxs-lookup"><span data-stu-id="48722-116">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="48722-117">該命令會將該物件儲存在 $ResourceGroup 變數中。</span><span class="sxs-lookup"><span data-stu-id="48722-117">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="48722-118">第二個命令會使用 Get-AzPolicyAssignment Cmdlet 來取得名為 PolicyAssignment 的原則指派。</span><span class="sxs-lookup"><span data-stu-id="48722-118">The second command gets the policy assignment named PolicyAssignment by using the Get-AzPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="48722-119">該命令會將該物件儲存在 $PolicyAssignment 變數中。</span><span class="sxs-lookup"><span data-stu-id="48722-119">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="48722-120">最後一個命令會更新由 $ResourceGroup 的 **ResourceId** 屬性所識別之資源群組上的原則指派顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="48722-120">The final command updates the display name on the policy assignment on the resource group identified by the **ResourceId** property of $ResourceGroup.</span></span>

### <span data-ttu-id="48722-121">範例2：在原則指派中加入 managed 身分識別</span><span class="sxs-lookup"><span data-stu-id="48722-121">Example 2: Add a managed identity to the policy assignment</span></span>
```
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment'
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -AssignIdentity -Location 'westus'
```

<span data-ttu-id="48722-122">第一個命令會使用 Get-AzPolicyAssignment Cmdlet，從目前訂閱取得名為 PolicyAssignment 的原則指派。</span><span class="sxs-lookup"><span data-stu-id="48722-122">The first command gets the policy assignment named PolicyAssignment from the current subscription by using the Get-AzPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="48722-123">該命令會將該物件儲存在 $PolicyAssignment 變數中。</span><span class="sxs-lookup"><span data-stu-id="48722-123">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="48722-124">最終命令會為原則指派指派受管理的身分識別。</span><span class="sxs-lookup"><span data-stu-id="48722-124">The final command assigns a managed identity to the policy assignment.</span></span>

### <span data-ttu-id="48722-125">範例3：使用新的 policy 參數物件更新原則指派參數</span><span class="sxs-lookup"><span data-stu-id="48722-125">Example 3: Update policy assignment parameters with new policy parameter object</span></span>
```
PS C:\> $Locations = Get-AzLocation | where {($_.displayname -like 'france*') -or ($_.displayname -like 'uk*')}
PS C:\> $AllowedLocations = @{'listOfAllowedLocations'=($Locations.location)}
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment'
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -PolicyParameterObject $AllowedLocations
```

<span data-ttu-id="48722-126">第一個和第二個命令會建立一個物件，其中包含名稱以 "華北" 或 "uk" 開頭的所有 Azure 區域。</span><span class="sxs-lookup"><span data-stu-id="48722-126">The first and second commands create an object containing all Azure regions whose names start with "france" or "uk".</span></span>
<span data-ttu-id="48722-127">第二個命令會將該物件儲存在 $AllowedLocations 變數中。</span><span class="sxs-lookup"><span data-stu-id="48722-127">The second command stores that object in the $AllowedLocations variable.</span></span>
<span data-ttu-id="48722-128">第三個命令會取得名為「PolicyAssignment」的原則指派，命令會將該物件儲存在 $PolicyAssignment 變數中。</span><span class="sxs-lookup"><span data-stu-id="48722-128">The third command gets the policy assignment named 'PolicyAssignment' The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="48722-129">Final 命令會更新名為 PolicyAssignment 的原則指派上的參數值。</span><span class="sxs-lookup"><span data-stu-id="48722-129">The final command updates the parameter values on the policy assignment named PolicyAssignment.</span></span>

### <span data-ttu-id="48722-130">範例4：使用原則參數檔案更新原則指派參數</span><span class="sxs-lookup"><span data-stu-id="48722-130">Example 4: Update policy assignment parameters with policy parameter file</span></span>
<span data-ttu-id="48722-131">在本機工作目錄中，使用下列內容來建立名為 _AllowedLocations.js_ 的檔案。</span><span class="sxs-lookup"><span data-stu-id="48722-131">Create a file called _AllowedLocations.json_ in the local working directory with the following content.</span></span>

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

<span data-ttu-id="48722-132">這個命令會使用本機工作目錄中的原則 AllowedLocations.js參數檔案，更新名為「PolicyAssignment」的原則指派。</span><span class="sxs-lookup"><span data-stu-id="48722-132">The command updates the policy assignment named 'PolicyAssignment' using the policy parameter file AllowedLocations.json from the local working directory.</span></span>

## <span data-ttu-id="48722-133">參數</span><span class="sxs-lookup"><span data-stu-id="48722-133">PARAMETERS</span></span>

### <span data-ttu-id="48722-134">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="48722-134">-ApiVersion</span></span>
<span data-ttu-id="48722-135">指定要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="48722-135">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="48722-136">如果您沒有指定版本，此 Cmdlet 會使用最新的可用版本。</span><span class="sxs-lookup"><span data-stu-id="48722-136">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="48722-137">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="48722-137">-AssignIdentity</span></span>
<span data-ttu-id="48722-138">針對此原則指派產生並指派 Azure Active Directory 身分識別。</span><span class="sxs-lookup"><span data-stu-id="48722-138">Generate and assign an Azure Active Directory Identity for this policy assignment.</span></span> <span data-ttu-id="48722-139">在執行「deployIfNotExists」原則的部署時，就會使用該身分識別。</span><span class="sxs-lookup"><span data-stu-id="48722-139">The identity will be used when executing deployments for 'deployIfNotExists' policies.</span></span> <span data-ttu-id="48722-140">指派身分識別時，位置是必要的。</span><span class="sxs-lookup"><span data-stu-id="48722-140">Location is required when assigning an identity.</span></span>

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

### <span data-ttu-id="48722-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48722-141">-DefaultProfile</span></span>
<span data-ttu-id="48722-142">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="48722-142">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="48722-143">-描述</span><span class="sxs-lookup"><span data-stu-id="48722-143">-Description</span></span>
<span data-ttu-id="48722-144">原則指派的描述</span><span class="sxs-lookup"><span data-stu-id="48722-144">The description for policy assignment</span></span>

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

### <span data-ttu-id="48722-145">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="48722-145">-DisplayName</span></span>
<span data-ttu-id="48722-146">指定原則指派的新顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="48722-146">Specifies a new display name for the policy assignment.</span></span>

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

### <span data-ttu-id="48722-147">-識別碼</span><span class="sxs-lookup"><span data-stu-id="48722-147">-Id</span></span>
<span data-ttu-id="48722-148">指定此 Cmdlet 所修改之原則指派的完全限定資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="48722-148">Specifies the fully qualified resource ID for the policy assignment that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="48722-149">-位置</span><span class="sxs-lookup"><span data-stu-id="48722-149">-Location</span></span>
<span data-ttu-id="48722-150">原則指派資源身分識別的位置。</span><span class="sxs-lookup"><span data-stu-id="48722-150">The location of the policy assignment's resource identity.</span></span> <span data-ttu-id="48722-151">使用-AssignIdentity 切換時，這是必要的。</span><span class="sxs-lookup"><span data-stu-id="48722-151">This is required when the -AssignIdentity switch is used.</span></span>

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

### <span data-ttu-id="48722-152">-中繼資料</span><span class="sxs-lookup"><span data-stu-id="48722-152">-Metadata</span></span>
<span data-ttu-id="48722-153">原則指派的更新中繼資料。</span><span class="sxs-lookup"><span data-stu-id="48722-153">The updated metadata for the policy assignment.</span></span> <span data-ttu-id="48722-154">這可以是包含中繼資料之檔案名的路徑，或是中繼資料作為字串。</span><span class="sxs-lookup"><span data-stu-id="48722-154">This can either be a path to a file name containing the metadata, or the metadata as a string.</span></span>

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

### <span data-ttu-id="48722-155">-名稱</span><span class="sxs-lookup"><span data-stu-id="48722-155">-Name</span></span>
<span data-ttu-id="48722-156">指定此 Cmdlet 所修改之原則指派的名稱。</span><span class="sxs-lookup"><span data-stu-id="48722-156">Specifies the name of the policy assignment that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="48722-157">-NotScope</span><span class="sxs-lookup"><span data-stu-id="48722-157">-NotScope</span></span>
<span data-ttu-id="48722-158">原則指派不是作用中的範圍。</span><span class="sxs-lookup"><span data-stu-id="48722-158">The policy assignment not scopes.</span></span>

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

### <span data-ttu-id="48722-159">-PolicyParameter</span><span class="sxs-lookup"><span data-stu-id="48722-159">-PolicyParameter</span></span>
<span data-ttu-id="48722-160">原則指派的新原則參數檔路徑或字串。</span><span class="sxs-lookup"><span data-stu-id="48722-160">The new policy parameters file path or string for the policy assignment.</span></span>

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

### <span data-ttu-id="48722-161">-PolicyParameterObject</span><span class="sxs-lookup"><span data-stu-id="48722-161">-PolicyParameterObject</span></span>
<span data-ttu-id="48722-162">原則指派的新原則參數物件。</span><span class="sxs-lookup"><span data-stu-id="48722-162">The new policy parameters object for the policy assignment.</span></span>

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

### <span data-ttu-id="48722-163">-預先</span><span class="sxs-lookup"><span data-stu-id="48722-163">-Pre</span></span>
<span data-ttu-id="48722-164">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="48722-164">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="48722-165">-範圍</span><span class="sxs-lookup"><span data-stu-id="48722-165">-Scope</span></span>
<span data-ttu-id="48722-166">指定應用原則的範圍。</span><span class="sxs-lookup"><span data-stu-id="48722-166">Specifies the scope at which the policy is applied.</span></span>

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

### <span data-ttu-id="48722-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48722-167">CommonParameters</span></span>
<span data-ttu-id="48722-168">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="48722-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48722-169">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="48722-169">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48722-170">輸入</span><span class="sxs-lookup"><span data-stu-id="48722-170">INPUTS</span></span>

### <span data-ttu-id="48722-171">System.object</span><span class="sxs-lookup"><span data-stu-id="48722-171">System.String</span></span>

### <span data-ttu-id="48722-172">System.object []</span><span class="sxs-lookup"><span data-stu-id="48722-172">System.String[]</span></span>

## <span data-ttu-id="48722-173">輸出</span><span class="sxs-lookup"><span data-stu-id="48722-173">OUTPUTS</span></span>

### <span data-ttu-id="48722-174">系統管理. PSObject</span><span class="sxs-lookup"><span data-stu-id="48722-174">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="48722-175">筆記</span><span class="sxs-lookup"><span data-stu-id="48722-175">NOTES</span></span>

## <span data-ttu-id="48722-176">相關連結</span><span class="sxs-lookup"><span data-stu-id="48722-176">RELATED LINKS</span></span>

[<span data-ttu-id="48722-177">AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="48722-177">Get-AzPolicyAssignment</span></span>](./Get-AzPolicyAssignment.md)

[<span data-ttu-id="48722-178">新-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="48722-178">New-AzPolicyAssignment</span></span>](./New-AzPolicyAssignment.md)

[<span data-ttu-id="48722-179">移除-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="48722-179">Remove-AzPolicyAssignment</span></span>](./Remove-AzPolicyAssignment.md)


