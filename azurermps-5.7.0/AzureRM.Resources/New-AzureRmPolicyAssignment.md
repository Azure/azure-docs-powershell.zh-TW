---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: BA40BD11-8167-48D7-AC71-72B2FD9924F2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicyAssignment.md
ms.openlocfilehash: 364411d6b69c04d8b29c1c32e2809ec3c4789b09
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452064"
---
# <span data-ttu-id="5fd9c-101">New-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="5fd9c-101">New-AzureRmPolicyAssignment</span></span>

## <span data-ttu-id="5fd9c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5fd9c-102">SYNOPSIS</span></span>
<span data-ttu-id="5fd9c-103">建立原則指派。</span><span class="sxs-lookup"><span data-stu-id="5fd9c-103">Creates a policy assignment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5fd9c-104">句法</span><span class="sxs-lookup"><span data-stu-id="5fd9c-104">SYNTAX</span></span>

### <span data-ttu-id="5fd9c-105">CreateWithoutParameters (預設) </span><span class="sxs-lookup"><span data-stu-id="5fd9c-105">CreateWithoutParameters (Default)</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] [-PolicySetDefinition <PSObject>] [-Sku <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="5fd9c-106">CreateWithPolicyParameterObject</span><span class="sxs-lookup"><span data-stu-id="5fd9c-106">CreateWithPolicyParameterObject</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PSObject> [-PolicySetDefinition <PSObject>]
 -PolicyParameterObject <Hashtable> [-Sku <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="5fd9c-107">CreateWithPolicyParameterString</span><span class="sxs-lookup"><span data-stu-id="5fd9c-107">CreateWithPolicyParameterString</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PSObject> [-PolicySetDefinition <PSObject>]
 -PolicyParameter <String> [-Sku <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="5fd9c-108">CreateWithPolicySetParameterObject</span><span class="sxs-lookup"><span data-stu-id="5fd9c-108">CreateWithPolicySetParameterObject</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] -PolicySetDefinition <PSObject>
 -PolicyParameterObject <Hashtable> [-Sku <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="5fd9c-109">CreateWithPolicySetParameterString</span><span class="sxs-lookup"><span data-stu-id="5fd9c-109">CreateWithPolicySetParameterString</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] -PolicySetDefinition <PSObject>
 -PolicyParameter <String> [-Sku <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="5fd9c-110">說明</span><span class="sxs-lookup"><span data-stu-id="5fd9c-110">DESCRIPTION</span></span>
<span data-ttu-id="5fd9c-111">**新的-AzureRmPolicyAssignment** Cmdlet 會建立原則指派。</span><span class="sxs-lookup"><span data-stu-id="5fd9c-111">The **New-AzureRmPolicyAssignment** cmdlet creates a policy assignment.</span></span>
<span data-ttu-id="5fd9c-112">指定原則與範圍。</span><span class="sxs-lookup"><span data-stu-id="5fd9c-112">Specify a policy and scope.</span></span>

## <span data-ttu-id="5fd9c-113">示例</span><span class="sxs-lookup"><span data-stu-id="5fd9c-113">EXAMPLES</span></span>

### <span data-ttu-id="5fd9c-114">範例1：資源群組層級的原則指派</span><span class="sxs-lookup"><span data-stu-id="5fd9c-114">Example 1: Policy assignment at resource group level</span></span>
```
PS C:\>$ResourceGroup = Get-AzureRmResourceGroup -Name "ResourceGroup11"
PS C:\> $Policy = Get-AzureRmPolicyDefinition -Name "VirtualMachinePolicy"
PS C:\> New-AzureRmPolicyAssignment -Name "VirtualMachinePolicyAssignment" -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId
```

<span data-ttu-id="5fd9c-115">第一個命令會使用 Get-AzureRMResourceGroup Cmdlet 來取得名為 ResourceGroup11 的資源群組。</span><span class="sxs-lookup"><span data-stu-id="5fd9c-115">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="5fd9c-116">該命令會將該物件儲存在 $ResourceGroup 變數中。</span><span class="sxs-lookup"><span data-stu-id="5fd9c-116">The command stores that object in the $ResourceGroup variable.</span></span>

<span data-ttu-id="5fd9c-117">第二個命令會使用 Get-AzureRmPolicyDefinition Cmdlet 來取得名為 VirtualMachinePolicy 的原則定義。</span><span class="sxs-lookup"><span data-stu-id="5fd9c-117">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzureRmPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="5fd9c-118">該命令會將該物件儲存在 $Policy 變數中。</span><span class="sxs-lookup"><span data-stu-id="5fd9c-118">The command stores that object in the $Policy variable.</span></span>

<span data-ttu-id="5fd9c-119">最終命令會將原則指派給資源群組層級 $Policy。</span><span class="sxs-lookup"><span data-stu-id="5fd9c-119">The final command assigns the policy in $Policy at the level of a resource group.</span></span>
<span data-ttu-id="5fd9c-120">$ResourceGroup 的 **ResourceId** 屬性會識別資源群組。</span><span class="sxs-lookup"><span data-stu-id="5fd9c-120">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

### <span data-ttu-id="5fd9c-121">範例2：資源群組層級與 policy 參數物件的原則指派</span><span class="sxs-lookup"><span data-stu-id="5fd9c-121">Example 2: Policy assignment at resource group level with policy parameter object</span></span>
```
PS C:\>$ResourceGroup = Get-AzureRmResourceGroup -Name "ResourceGroup11"
PS C:\> $Policy = Get-AzureRmPolicyDefinition | Where-Object {$_.Properties.DisplayName -eq 'Allowed locations' -and $_.Properties.PolicyType -eq 'BuiltIn'}
PS C:\> $Locations = Get-AzureRmLocation | where displayname -like "*east*"
PS C:\> $AllowedLocations = @{"listOfAllowedLocations"=($Locations.location)}
PS C:\> New-AzureRmPolicyAssignment -Name "RestrictLocationPolicyAssignment" -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -PolicyParameterObject $AllowedLocations
```

<span data-ttu-id="5fd9c-122">第一個命令會使用 Get-AzureRMResourceGroup Cmdlet 來取得名為 ResourceGroup11 的資源群組。</span><span class="sxs-lookup"><span data-stu-id="5fd9c-122">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="5fd9c-123">該命令會將該物件儲存在 $ResourceGroup 變數中。</span><span class="sxs-lookup"><span data-stu-id="5fd9c-123">The command stores that object in the $ResourceGroup variable.</span></span>

<span data-ttu-id="5fd9c-124">第二個命令會使用 Get-AzureRmPolicyDefinition Cmdlet 來取得允許位置的內建原則定義。</span><span class="sxs-lookup"><span data-stu-id="5fd9c-124">The second command gets the built-in policy definition for allowed locations by using the Get-AzureRmPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="5fd9c-125">該命令會將該物件儲存在 $Policy 變數中。</span><span class="sxs-lookup"><span data-stu-id="5fd9c-125">The command stores that object in the $Policy variable.</span></span>

<span data-ttu-id="5fd9c-126">第三個和第四個命令會建立一個物件，其中包含名稱中含 "東" 的所有 Azure 區域。</span><span class="sxs-lookup"><span data-stu-id="5fd9c-126">The third and fourth commands create an object containing all Azure regions with "east" in the name.</span></span>
<span data-ttu-id="5fd9c-127">命令會將該物件儲存在 $AllowedLocations 變數中。</span><span class="sxs-lookup"><span data-stu-id="5fd9c-127">The commands store that object in the $AllowedLocations variable.</span></span>

<span data-ttu-id="5fd9c-128">Final 命令會在 $AllowedLocations 中使用 policy 參數物件的資源群組層次 $Policy 指派原則。</span><span class="sxs-lookup"><span data-stu-id="5fd9c-128">The final command assigns the policy in $Policy at the level of a resource group using the policy parameter object in $AllowedLocations.</span></span>
<span data-ttu-id="5fd9c-129">$ResourceGroup 的 **ResourceId** 屬性會識別資源群組。</span><span class="sxs-lookup"><span data-stu-id="5fd9c-129">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

### <span data-ttu-id="5fd9c-130">範例3：資源群組層級的原則指派（含原則參數檔案）</span><span class="sxs-lookup"><span data-stu-id="5fd9c-130">Example 3: Policy assignment at resource group level with policy parameter file</span></span>
<span data-ttu-id="5fd9c-131">在本機工作目錄中，使用下列內容來建立名為 _AllowedLocations.js_ 的檔案。</span><span class="sxs-lookup"><span data-stu-id="5fd9c-131">Create a file called _AllowedLocations.json_ in the local working directory with the following content.</span></span>
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
PS C:\>$ResourceGroup = Get-AzureRmResourceGroup -Name "ResourceGroup11"
PS C:\> $Policy = Get-AzureRmPolicyDefinition | Where-Object {$_.Properties.DisplayName -eq 'Allowed locations' -and $_.Properties.PolicyType -eq 'BuiltIn'}
PS C:\> New-AzureRmPolicyAssignment -Name "RestrictLocationPolicyAssignment" -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -PolicyParameter .\AllowedLocations.json
```

<span data-ttu-id="5fd9c-132">第一個命令會使用 Get-AzureRMResourceGroup Cmdlet 來取得名為 ResourceGroup11 的資源群組。</span><span class="sxs-lookup"><span data-stu-id="5fd9c-132">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="5fd9c-133">該命令會將該物件儲存在 $ResourceGroup 變數中。</span><span class="sxs-lookup"><span data-stu-id="5fd9c-133">The command stores that object in the $ResourceGroup variable.</span></span>

<span data-ttu-id="5fd9c-134">第二個命令會使用 Get-AzureRmPolicyDefinition Cmdlet 來取得允許位置的內建原則定義。</span><span class="sxs-lookup"><span data-stu-id="5fd9c-134">The second command gets the built-in policy definition for allowed locations by using the Get-AzureRmPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="5fd9c-135">該命令會將該物件儲存在 $Policy 變數中。</span><span class="sxs-lookup"><span data-stu-id="5fd9c-135">The command stores that object in the $Policy variable.</span></span>

<span data-ttu-id="5fd9c-136">Final 命令會使用本機工作目錄中的原則參數檔案 AllowedLocations.js，在 $Policy 的資源群組層級指派原則。</span><span class="sxs-lookup"><span data-stu-id="5fd9c-136">The final command assigns the policy in $Policy at the level of a resource group using the policy parameter file AllowedLocations.json from the local working directory.</span></span>
<span data-ttu-id="5fd9c-137">$ResourceGroup 的 **ResourceId** 屬性會識別資源群組。</span><span class="sxs-lookup"><span data-stu-id="5fd9c-137">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>


## <span data-ttu-id="5fd9c-138">參數</span><span class="sxs-lookup"><span data-stu-id="5fd9c-138">PARAMETERS</span></span>

### <span data-ttu-id="5fd9c-139">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="5fd9c-139">-ApiVersion</span></span>
<span data-ttu-id="5fd9c-140">指定要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="5fd9c-140">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="5fd9c-141">如果您沒有指定版本，此 Cmdlet 會使用最新的可用版本。</span><span class="sxs-lookup"><span data-stu-id="5fd9c-141">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fd9c-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fd9c-142">-DefaultProfile</span></span>
<span data-ttu-id="5fd9c-143">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="5fd9c-143">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fd9c-144">-描述</span><span class="sxs-lookup"><span data-stu-id="5fd9c-144">-Description</span></span>
<span data-ttu-id="5fd9c-145">原則指派的描述</span><span class="sxs-lookup"><span data-stu-id="5fd9c-145">The description for policy assignment</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fd9c-146">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="5fd9c-146">-DisplayName</span></span>
<span data-ttu-id="5fd9c-147">指定原則指派的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="5fd9c-147">Specifies a display name for the policy assignment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fd9c-148">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="5fd9c-148">-InformationAction</span></span>
<span data-ttu-id="5fd9c-149">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="5fd9c-149">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="5fd9c-150">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="5fd9c-150">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5fd9c-151">持續</span><span class="sxs-lookup"><span data-stu-id="5fd9c-151">Continue</span></span>
- <span data-ttu-id="5fd9c-152">理會</span><span class="sxs-lookup"><span data-stu-id="5fd9c-152">Ignore</span></span>
- <span data-ttu-id="5fd9c-153">看</span><span class="sxs-lookup"><span data-stu-id="5fd9c-153">Inquire</span></span>
- <span data-ttu-id="5fd9c-154">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="5fd9c-154">SilentlyContinue</span></span>
- <span data-ttu-id="5fd9c-155">停止</span><span class="sxs-lookup"><span data-stu-id="5fd9c-155">Stop</span></span>
- <span data-ttu-id="5fd9c-156">封存</span><span class="sxs-lookup"><span data-stu-id="5fd9c-156">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fd9c-157">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="5fd9c-157">-InformationVariable</span></span>
<span data-ttu-id="5fd9c-158">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="5fd9c-158">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fd9c-159">-名稱</span><span class="sxs-lookup"><span data-stu-id="5fd9c-159">-Name</span></span>
<span data-ttu-id="5fd9c-160">指定原則指派的名稱。</span><span class="sxs-lookup"><span data-stu-id="5fd9c-160">Specifies a name for the policy assignment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fd9c-161">-NotScope</span><span class="sxs-lookup"><span data-stu-id="5fd9c-161">-NotScope</span></span>
<span data-ttu-id="5fd9c-162">原則指派的 not 作用中。</span><span class="sxs-lookup"><span data-stu-id="5fd9c-162">The not scopes for policy assignment.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fd9c-163">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="5fd9c-163">-PolicyDefinition</span></span>
<span data-ttu-id="5fd9c-164">指定原則，做為包含原則規則的 **PSObject** 物件。</span><span class="sxs-lookup"><span data-stu-id="5fd9c-164">Specifies a policy, as a **PSObject** object that contains the policy rule.</span></span>

```yaml
Type: PSObject
Parameter Sets: CreateWithoutParameters, CreateWithPolicySetParameterObject, CreateWithPolicySetParameterString
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: PSObject
Parameter Sets: CreateWithPolicyParameterObject, CreateWithPolicyParameterString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fd9c-165">-PolicyParameter</span><span class="sxs-lookup"><span data-stu-id="5fd9c-165">-PolicyParameter</span></span>
<span data-ttu-id="5fd9c-166">原則參數檔案路徑或原則參數字串。</span><span class="sxs-lookup"><span data-stu-id="5fd9c-166">The policy parameter file path or policy parameter string.</span></span>

```yaml
Type: String
Parameter Sets: CreateWithPolicyParameterString, CreateWithPolicySetParameterString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fd9c-167">-PolicyParameterObject</span><span class="sxs-lookup"><span data-stu-id="5fd9c-167">-PolicyParameterObject</span></span>
<span data-ttu-id="5fd9c-168">原則參數物件。</span><span class="sxs-lookup"><span data-stu-id="5fd9c-168">The policy parameter object.</span></span>

```yaml
Type: Hashtable
Parameter Sets: CreateWithPolicyParameterObject, CreateWithPolicySetParameterObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fd9c-169">-PolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="5fd9c-169">-PolicySetDefinition</span></span>
<span data-ttu-id="5fd9c-170">原則集定義物件。</span><span class="sxs-lookup"><span data-stu-id="5fd9c-170">The policy set definition object.</span></span>

```yaml
Type: PSObject
Parameter Sets: CreateWithoutParameters, CreateWithPolicyParameterObject, CreateWithPolicyParameterString
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: PSObject
Parameter Sets: CreateWithPolicySetParameterObject, CreateWithPolicySetParameterString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fd9c-171">-預先</span><span class="sxs-lookup"><span data-stu-id="5fd9c-171">-Pre</span></span>
<span data-ttu-id="5fd9c-172">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="5fd9c-172">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fd9c-173">-範圍</span><span class="sxs-lookup"><span data-stu-id="5fd9c-173">-Scope</span></span>
<span data-ttu-id="5fd9c-174">指定指派原則的範圍。</span><span class="sxs-lookup"><span data-stu-id="5fd9c-174">Specifies the scope at which to assign the policy.</span></span>
<span data-ttu-id="5fd9c-175">例如，若要將原則指派給資源群組，請指定下列專案：</span><span class="sxs-lookup"><span data-stu-id="5fd9c-175">For instance, to assign a policy to a resource group, specify the following:</span></span>

<span data-ttu-id="5fd9c-176">`/subscriptions/`訂閱識別碼 `/resourcegroups/` 資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="5fd9c-176">`/subscriptions/`subscription ID`/resourcegroups/`resource group name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fd9c-177">-Sku</span><span class="sxs-lookup"><span data-stu-id="5fd9c-177">-Sku</span></span>
<span data-ttu-id="5fd9c-178">代表 sku 屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="5fd9c-178">A hash table which represents sku properties.</span></span> <span data-ttu-id="5fd9c-179">預設為免費 Sku： Name = A0，雙層 = Fre</span><span class="sxs-lookup"><span data-stu-id="5fd9c-179">Defaults to Free Sku: Name = A0, Tier = Fre</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: SkuObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fd9c-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fd9c-180">CommonParameters</span></span>
<span data-ttu-id="5fd9c-181">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5fd9c-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fd9c-182">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5fd9c-182">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fd9c-183">輸入</span><span class="sxs-lookup"><span data-stu-id="5fd9c-183">INPUTS</span></span>

### <span data-ttu-id="5fd9c-184">所有</span><span class="sxs-lookup"><span data-stu-id="5fd9c-184">None</span></span>
<span data-ttu-id="5fd9c-185">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="5fd9c-185">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5fd9c-186">輸出</span><span class="sxs-lookup"><span data-stu-id="5fd9c-186">OUTPUTS</span></span>

### <span data-ttu-id="5fd9c-187">系統管理. PSObject</span><span class="sxs-lookup"><span data-stu-id="5fd9c-187">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="5fd9c-188">筆記</span><span class="sxs-lookup"><span data-stu-id="5fd9c-188">NOTES</span></span>

## <span data-ttu-id="5fd9c-189">相關連結</span><span class="sxs-lookup"><span data-stu-id="5fd9c-189">RELATED LINKS</span></span>

[<span data-ttu-id="5fd9c-190">AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="5fd9c-190">Get-AzureRmPolicyDefinition</span></span>](./Get-AzureRmPolicyDefinition.md)

[<span data-ttu-id="5fd9c-191">AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="5fd9c-191">Get-AzureRmPolicyAssignment</span></span>](./Get-AzureRmPolicyAssignment.md)

[<span data-ttu-id="5fd9c-192">移除-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="5fd9c-192">Remove-AzureRmPolicyAssignment</span></span>](./Remove-AzureRmPolicyAssignment.md)

[<span data-ttu-id="5fd9c-193">Set-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="5fd9c-193">Set-AzureRmPolicyAssignment</span></span>](./Set-AzureRmPolicyAssignment.md)


