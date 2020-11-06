---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: BA40BD11-8167-48D7-AC71-72B2FD9924F2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicyAssignment.md
ms.openlocfilehash: 616b75b4bdc5dab9f02bb1fc295effefc0e728be
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93443699"
---
# <span data-ttu-id="40de5-101">New-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="40de5-101">New-AzureRmPolicyAssignment</span></span>

## <span data-ttu-id="40de5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="40de5-102">SYNOPSIS</span></span>
<span data-ttu-id="40de5-103">建立原則指派。</span><span class="sxs-lookup"><span data-stu-id="40de5-103">Creates a policy assignment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="40de5-104">句法</span><span class="sxs-lookup"><span data-stu-id="40de5-104">SYNTAX</span></span>

### <span data-ttu-id="40de5-105">DefaultParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="40de5-105">DefaultParameterSet (Default)</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] [-PolicySetDefinition <PSObject>] [-Metadata <String>]
 [-Sku <Hashtable>] [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="40de5-106">PolicyParameterObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="40de5-106">PolicyParameterObjectParameterSet</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PSObject> [-PolicySetDefinition <PSObject>]
 -PolicyParameterObject <Hashtable> [-Metadata <String>] [-Sku <Hashtable>] [-AssignIdentity]
 [-Location <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="40de5-107">PolicyParameterStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="40de5-107">PolicyParameterStringParameterSet</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PSObject> [-PolicySetDefinition <PSObject>]
 -PolicyParameter <String> [-Metadata <String>] [-Sku <Hashtable>] [-AssignIdentity] [-Location <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="40de5-108">PolicySetParameterObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="40de5-108">PolicySetParameterObjectParameterSet</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] -PolicySetDefinition <PSObject>
 -PolicyParameterObject <Hashtable> [-Metadata <String>] [-Sku <Hashtable>] [-AssignIdentity]
 [-Location <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="40de5-109">PolicySetParameterStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="40de5-109">PolicySetParameterStringParameterSet</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] -PolicySetDefinition <PSObject>
 -PolicyParameter <String> [-Metadata <String>] [-Sku <Hashtable>] [-AssignIdentity] [-Location <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="40de5-110">說明</span><span class="sxs-lookup"><span data-stu-id="40de5-110">DESCRIPTION</span></span>
<span data-ttu-id="40de5-111">**新的-AzureRmPolicyAssignment** Cmdlet 會建立原則指派。</span><span class="sxs-lookup"><span data-stu-id="40de5-111">The **New-AzureRmPolicyAssignment** cmdlet creates a policy assignment.</span></span>
<span data-ttu-id="40de5-112">指定原則與範圍。</span><span class="sxs-lookup"><span data-stu-id="40de5-112">Specify a policy and scope.</span></span>

## <span data-ttu-id="40de5-113">示例</span><span class="sxs-lookup"><span data-stu-id="40de5-113">EXAMPLES</span></span>

### <span data-ttu-id="40de5-114">範例1：資源群組層級的原則指派</span><span class="sxs-lookup"><span data-stu-id="40de5-114">Example 1: Policy assignment at resource group level</span></span>
```
PS C:\> $ResourceGroup = Get-AzureRmResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzureRmPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzureRmPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId
```

<span data-ttu-id="40de5-115">第一個命令會使用 Get-AzureRMResourceGroup Cmdlet 來取得名為 ResourceGroup11 的資源群組，並將它儲存在 $ResourceGroup 變數中。</span><span class="sxs-lookup"><span data-stu-id="40de5-115">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="40de5-116">第二個命令會使用 Get-AzureRmPolicyDefinition Cmdlet 來取得名為 VirtualMachinePolicy 的原則定義，並將它儲存在 $Policy 變數中。</span><span class="sxs-lookup"><span data-stu-id="40de5-116">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzureRmPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="40de5-117">最後一個命令會將原則指派給 $Policy，該資源群組由 $ResourceGroup 的 **ResourceId** 屬性所識別。</span><span class="sxs-lookup"><span data-stu-id="40de5-117">The final command assigns the policy in $Policy at the level of the resource group identified by the **ResourceId** property of $ResourceGroup.</span></span>

### <span data-ttu-id="40de5-118">範例2：資源群組層級與 policy 參數物件的原則指派</span><span class="sxs-lookup"><span data-stu-id="40de5-118">Example 2: Policy assignment at resource group level with policy parameter object</span></span>
```
PS C:\> $ResourceGroup = Get-AzureRmResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzureRmPolicyDefinition -BuiltIn | Where-Object {$_.Properties.DisplayName -eq 'Allowed locations'}
PS C:\> $Locations = Get-AzureRmLocation | where displayname -like '*east*'
PS C:\> $AllowedLocations = @{'listOfAllowedLocations'=($Locations.location)}
PS C:\> New-AzureRmPolicyAssignment -Name 'RestrictLocationPolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -PolicyParameterObject $AllowedLocations
```

<span data-ttu-id="40de5-119">第一個命令會使用 Get-AzureRMResourceGroup Cmdlet 來取得名為 ResourceGroup11 的資源群組。</span><span class="sxs-lookup"><span data-stu-id="40de5-119">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="40de5-120">該命令會將該物件儲存在 $ResourceGroup 變數中。</span><span class="sxs-lookup"><span data-stu-id="40de5-120">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="40de5-121">第二個命令會使用 Get-AzureRmPolicyDefinition Cmdlet 來取得允許位置的內建原則定義。</span><span class="sxs-lookup"><span data-stu-id="40de5-121">The second command gets the built-in policy definition for allowed locations by using the Get-AzureRmPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="40de5-122">該命令會將該物件儲存在 $Policy 變數中。</span><span class="sxs-lookup"><span data-stu-id="40de5-122">The command stores that object in the $Policy variable.</span></span>
<span data-ttu-id="40de5-123">第三個和第四個命令會建立一個物件，其中包含名稱中含 "東" 的所有 Azure 區域。</span><span class="sxs-lookup"><span data-stu-id="40de5-123">The third and fourth commands create an object containing all Azure regions with "east" in the name.</span></span>
<span data-ttu-id="40de5-124">命令會將該物件儲存在 $AllowedLocations 變數中。</span><span class="sxs-lookup"><span data-stu-id="40de5-124">The commands store that object in the $AllowedLocations variable.</span></span>
<span data-ttu-id="40de5-125">Final 命令會在 $AllowedLocations 中使用 policy 參數物件的資源群組層次 $Policy 指派原則。</span><span class="sxs-lookup"><span data-stu-id="40de5-125">The final command assigns the policy in $Policy at the level of a resource group using the policy parameter object in $AllowedLocations.</span></span>
<span data-ttu-id="40de5-126">$ResourceGroup 的 **ResourceId** 屬性會識別資源群組。</span><span class="sxs-lookup"><span data-stu-id="40de5-126">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

### <span data-ttu-id="40de5-127">範例3：資源群組層級的原則指派（含原則參數檔案）</span><span class="sxs-lookup"><span data-stu-id="40de5-127">Example 3: Policy assignment at resource group level with policy parameter file</span></span>
<span data-ttu-id="40de5-128">在本機工作目錄中，使用下列內容來建立名為 _AllowedLocations.js_ 的檔案。</span><span class="sxs-lookup"><span data-stu-id="40de5-128">Create a file called _AllowedLocations.json_ in the local working directory with the following content.</span></span>

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
PS C:\> $ResourceGroup = Get-AzureRmResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzureRmPolicyDefinition -BuiltIn | Where-Object {$_.Properties.DisplayName -eq 'Allowed locations'}
PS C:\> New-AzureRmPolicyAssignment -Name 'RestrictLocationPolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -PolicyParameter .\AllowedLocations.json
```

<span data-ttu-id="40de5-129">第一個命令會使用 Get-AzureRMResourceGroup Cmdlet 來取得名為 ResourceGroup11 的資源群組，並將它儲存在 $ResourceGroup 變數中。</span><span class="sxs-lookup"><span data-stu-id="40de5-129">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="40de5-130">第二個命令會使用 Get-AzureRmPolicyDefinition Cmdlet 來取得允許位置的內建原則定義，並將它儲存在 $Policy 變數中。</span><span class="sxs-lookup"><span data-stu-id="40de5-130">The second command gets the built-in policy definition for allowed locations by using the Get-AzureRmPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="40de5-131">Final 命令會在 $Policy 的資源群組中，指派由 $ResourceGroup 的 **ResourceId** 屬性所識別的資源群組的原則，該資源組是從本機工作目錄 AllowedLocations.js。</span><span class="sxs-lookup"><span data-stu-id="40de5-131">The final command assigns the policy in $Policy at the resource group identified by the **ResourceId** property of $ResourceGroup using the policy parameter file AllowedLocations.json from the local working directory.</span></span>

### <span data-ttu-id="40de5-132">範例4：具有受管理身分識別的原則指派</span><span class="sxs-lookup"><span data-stu-id="40de5-132">Example 4: Policy assignment with a managed identity</span></span>
```
PS C:\> $ResourceGroup = Get-AzureRmResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzureRmPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzureRmPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -Location 'eastus' -AssignIdentity 
```

<span data-ttu-id="40de5-133">第一個命令會使用 Get-AzureRMResourceGroup Cmdlet 來取得名為 ResourceGroup11 的資源群組，並將它儲存在 $ResourceGroup 變數中。</span><span class="sxs-lookup"><span data-stu-id="40de5-133">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="40de5-134">第二個命令會使用 Get-AzureRmPolicyDefinition Cmdlet 來取得名為 VirtualMachinePolicy 的原則定義，並將它儲存在 $Policy 變數中。</span><span class="sxs-lookup"><span data-stu-id="40de5-134">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzureRmPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="40de5-135">最終命令會將 $Policy 的原則指派給資源群組。</span><span class="sxs-lookup"><span data-stu-id="40de5-135">The final command assigns the policy in $Policy to the resource group.</span></span> <span data-ttu-id="40de5-136">系統會自動建立受管理的身分識別，並指派給原則指派。</span><span class="sxs-lookup"><span data-stu-id="40de5-136">A managed identity is automatically created and assigned to the policy assignment.</span></span>

## <span data-ttu-id="40de5-137">參數</span><span class="sxs-lookup"><span data-stu-id="40de5-137">PARAMETERS</span></span>

### <span data-ttu-id="40de5-138">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="40de5-138">-ApiVersion</span></span>
<span data-ttu-id="40de5-139">指定要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="40de5-139">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="40de5-140">如果您沒有指定版本，此 Cmdlet 會使用最新的可用版本。</span><span class="sxs-lookup"><span data-stu-id="40de5-140">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="40de5-141">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="40de5-141">-AssignIdentity</span></span>
<span data-ttu-id="40de5-142">針對此原則指派產生並指派 Azure Active Directory 身分識別。</span><span class="sxs-lookup"><span data-stu-id="40de5-142">Generate and assign an Azure Active Directory Identity for this policy assignment.</span></span> <span data-ttu-id="40de5-143">在執行「deployIfNotExists」原則的部署時，就會使用該身分識別。</span><span class="sxs-lookup"><span data-stu-id="40de5-143">The identity will be used when executing deployments for 'deployIfNotExists' policies.</span></span> <span data-ttu-id="40de5-144">指派身分識別時，位置是必要的。</span><span class="sxs-lookup"><span data-stu-id="40de5-144">Location is required when assigning an identity.</span></span>

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

### <span data-ttu-id="40de5-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40de5-145">-DefaultProfile</span></span>
<span data-ttu-id="40de5-146">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="40de5-146">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="40de5-147">-描述</span><span class="sxs-lookup"><span data-stu-id="40de5-147">-Description</span></span>
<span data-ttu-id="40de5-148">原則指派的描述</span><span class="sxs-lookup"><span data-stu-id="40de5-148">The description for policy assignment</span></span>

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

### <span data-ttu-id="40de5-149">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="40de5-149">-DisplayName</span></span>
<span data-ttu-id="40de5-150">指定原則指派的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="40de5-150">Specifies a display name for the policy assignment.</span></span>

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

### <span data-ttu-id="40de5-151">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="40de5-151">-InformationAction</span></span>
<span data-ttu-id="40de5-152">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="40de5-152">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="40de5-153">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="40de5-153">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="40de5-154">持續</span><span class="sxs-lookup"><span data-stu-id="40de5-154">Continue</span></span>
- <span data-ttu-id="40de5-155">理會</span><span class="sxs-lookup"><span data-stu-id="40de5-155">Ignore</span></span>
- <span data-ttu-id="40de5-156">看</span><span class="sxs-lookup"><span data-stu-id="40de5-156">Inquire</span></span>
- <span data-ttu-id="40de5-157">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="40de5-157">SilentlyContinue</span></span>
- <span data-ttu-id="40de5-158">停止</span><span class="sxs-lookup"><span data-stu-id="40de5-158">Stop</span></span>
- <span data-ttu-id="40de5-159">封存</span><span class="sxs-lookup"><span data-stu-id="40de5-159">Suspend</span></span>

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

### <span data-ttu-id="40de5-160">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="40de5-160">-InformationVariable</span></span>
<span data-ttu-id="40de5-161">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="40de5-161">Specifies an information variable.</span></span>

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

### <span data-ttu-id="40de5-162">-位置</span><span class="sxs-lookup"><span data-stu-id="40de5-162">-Location</span></span>
<span data-ttu-id="40de5-163">原則指派資源身分識別的位置。</span><span class="sxs-lookup"><span data-stu-id="40de5-163">The location of the policy assignment's resource identity.</span></span> <span data-ttu-id="40de5-164">使用-AssignIdentity 切換時，這是必要的。</span><span class="sxs-lookup"><span data-stu-id="40de5-164">This is required when the -AssignIdentity switch is used.</span></span>

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

### <span data-ttu-id="40de5-165">-中繼資料</span><span class="sxs-lookup"><span data-stu-id="40de5-165">-Metadata</span></span>
<span data-ttu-id="40de5-166">新原則指派的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="40de5-166">The metadata for the new policy assignment.</span></span> <span data-ttu-id="40de5-167">這可以是包含中繼資料之檔案名的路徑，或是中繼資料作為字串。</span><span class="sxs-lookup"><span data-stu-id="40de5-167">This can either be a path to a file name containing the metadata, or the metadata as a string.</span></span>

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

### <span data-ttu-id="40de5-168">-名稱</span><span class="sxs-lookup"><span data-stu-id="40de5-168">-Name</span></span>
<span data-ttu-id="40de5-169">指定原則指派的名稱。</span><span class="sxs-lookup"><span data-stu-id="40de5-169">Specifies a name for the policy assignment.</span></span>

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

### <span data-ttu-id="40de5-170">-NotScope</span><span class="sxs-lookup"><span data-stu-id="40de5-170">-NotScope</span></span>
<span data-ttu-id="40de5-171">原則指派的 not 作用中。</span><span class="sxs-lookup"><span data-stu-id="40de5-171">The not scopes for policy assignment.</span></span>

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

### <span data-ttu-id="40de5-172">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="40de5-172">-PolicyDefinition</span></span>
<span data-ttu-id="40de5-173">指定原則，做為包含原則規則的 **PsPolicyDefinition** 物件。</span><span class="sxs-lookup"><span data-stu-id="40de5-173">Specifies a policy, as a **PsPolicyDefinition** object that contains the policy rule.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: PolicyParameterObjectParameterSet, PolicyParameterStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: PolicySetParameterObjectParameterSet, PolicySetParameterStringParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40de5-174">-PolicyParameter</span><span class="sxs-lookup"><span data-stu-id="40de5-174">-PolicyParameter</span></span>
<span data-ttu-id="40de5-175">原則參數檔案路徑或原則參數字串。</span><span class="sxs-lookup"><span data-stu-id="40de5-175">The policy parameter file path or policy parameter string.</span></span>

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

### <span data-ttu-id="40de5-176">-PolicyParameterObject</span><span class="sxs-lookup"><span data-stu-id="40de5-176">-PolicyParameterObject</span></span>
<span data-ttu-id="40de5-177">原則參數物件。</span><span class="sxs-lookup"><span data-stu-id="40de5-177">The policy parameter object.</span></span>

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

### <span data-ttu-id="40de5-178">-PolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="40de5-178">-PolicySetDefinition</span></span>
<span data-ttu-id="40de5-179">原則集定義物件。</span><span class="sxs-lookup"><span data-stu-id="40de5-179">The policy set definition object.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: PolicyParameterObjectParameterSet, PolicyParameterStringParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: PolicySetParameterObjectParameterSet, PolicySetParameterStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40de5-180">-預先</span><span class="sxs-lookup"><span data-stu-id="40de5-180">-Pre</span></span>
<span data-ttu-id="40de5-181">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="40de5-181">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="40de5-182">-範圍</span><span class="sxs-lookup"><span data-stu-id="40de5-182">-Scope</span></span>
<span data-ttu-id="40de5-183">指定指派原則的範圍。</span><span class="sxs-lookup"><span data-stu-id="40de5-183">Specifies the scope at which to assign the policy.</span></span>
<span data-ttu-id="40de5-184">例如，若要將原則指派給資源群組，請指定下列專案： `/subscriptions/` 訂閱識別碼 `/resourcegroups/` 資源組名稱</span><span class="sxs-lookup"><span data-stu-id="40de5-184">For instance, to assign a policy to a resource group, specify the following: `/subscriptions/`subscription ID`/resourcegroups/`resource group name</span></span>

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

### <span data-ttu-id="40de5-185">-Sku</span><span class="sxs-lookup"><span data-stu-id="40de5-185">-Sku</span></span>
<span data-ttu-id="40de5-186">代表 SKU 屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="40de5-186">A hash table which represents SKU properties.</span></span> <span data-ttu-id="40de5-187">預設為免費 SKU，其值為： `@{Name = 'A0'; Tier = 'Free'}` 。</span><span class="sxs-lookup"><span data-stu-id="40de5-187">Defaults to the Free SKU with the values: `@{Name = 'A0'; Tier = 'Free'}`.</span></span> <span data-ttu-id="40de5-188">若要使用標準 SKU，請使用以下值： `@{Name = 'A1'; Tier = 'Standard'}` 。</span><span class="sxs-lookup"><span data-stu-id="40de5-188">To use the Standard SKU, use the values: `@{Name = 'A1'; Tier = 'Standard'}`.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: SkuObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40de5-189">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40de5-189">CommonParameters</span></span>
<span data-ttu-id="40de5-190">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="40de5-190">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40de5-191">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="40de5-191">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40de5-192">輸入</span><span class="sxs-lookup"><span data-stu-id="40de5-192">INPUTS</span></span>

## <span data-ttu-id="40de5-193">輸出</span><span class="sxs-lookup"><span data-stu-id="40de5-193">OUTPUTS</span></span>

## <span data-ttu-id="40de5-194">筆記</span><span class="sxs-lookup"><span data-stu-id="40de5-194">NOTES</span></span>

## <span data-ttu-id="40de5-195">相關連結</span><span class="sxs-lookup"><span data-stu-id="40de5-195">RELATED LINKS</span></span>

[<span data-ttu-id="40de5-196">AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="40de5-196">Get-AzureRmPolicyDefinition</span></span>](./Get-AzureRmPolicyDefinition.md)

[<span data-ttu-id="40de5-197">AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="40de5-197">Get-AzureRmPolicyAssignment</span></span>](./Get-AzureRmPolicyAssignment.md)

[<span data-ttu-id="40de5-198">移除-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="40de5-198">Remove-AzureRmPolicyAssignment</span></span>](./Remove-AzureRmPolicyAssignment.md)

[<span data-ttu-id="40de5-199">Set-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="40de5-199">Set-AzureRmPolicyAssignment</span></span>](./Set-AzureRmPolicyAssignment.md)


