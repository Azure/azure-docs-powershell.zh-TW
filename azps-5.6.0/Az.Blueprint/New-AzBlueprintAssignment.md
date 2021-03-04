---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/powershell/module/az.blueprint/new-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprintAssignment.md
ms.openlocfilehash: 8b17767f31683acb0228fbef52fd1de32d49ba6c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916440"
---
# <span data-ttu-id="ba130-101">New-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="ba130-101">New-AzBlueprintAssignment</span></span>

## <span data-ttu-id="ba130-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ba130-102">SYNOPSIS</span></span>
<span data-ttu-id="ba130-103">指派藍圖定義給訂閱或管理群組。</span><span class="sxs-lookup"><span data-stu-id="ba130-103">Assign a blueprint definition to a subscription or a management group.</span></span>

## <span data-ttu-id="ba130-104">語法</span><span class="sxs-lookup"><span data-stu-id="ba130-104">SYNTAX</span></span>

### <span data-ttu-id="ba130-105">CreateBlueprintAssignment (預設) </span><span class="sxs-lookup"><span data-stu-id="ba130-105">CreateBlueprintAssignment (Default)</span></span>
```
New-AzBlueprintAssignment -Name <String> -Blueprint <PSBlueprintBase> -Location <String>
 [-SystemAssignedIdentity] [-UserAssignedIdentity <String>] [-Lock <PSLockMode>]
 [-SecureStringParameter <Hashtable>] [-ResourceGroupParameter <Hashtable>] [-Parameter <Hashtable>]
 [-ManagementGroupId <String>] [-SubscriptionId <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba130-106">CreateBlueprintAssignmentByFile</span><span class="sxs-lookup"><span data-stu-id="ba130-106">CreateBlueprintAssignmentByFile</span></span>
```
New-AzBlueprintAssignment -Name <String> [-Blueprint <PSBlueprintBase>] [-AssignmentFile <String>]
 [-ManagementGroupId <String>] [-SubscriptionId <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba130-107">描述</span><span class="sxs-lookup"><span data-stu-id="ba130-107">DESCRIPTION</span></span>
<span data-ttu-id="ba130-108">指派藍圖定義給訂閱。</span><span class="sxs-lookup"><span data-stu-id="ba130-108">Assign a blueprint definition to a subscription.</span></span>

## <span data-ttu-id="ba130-109">例子</span><span class="sxs-lookup"><span data-stu-id="ba130-109">EXAMPLES</span></span>

### <span data-ttu-id="ba130-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="ba130-110">Example 1</span></span>
```powershell
PS C:\> $rg = @{ResourceGroup=@{name='storage_rg';location='eastus'}}
PS C:\> $params = @{applytaganditsdefaultvalue_tagName="Department_Cost_Center"; applytaganditsdefaultvalue_tagValue="Contoso/RnD/Dev/986754"}
PS C:\> $blueprintObject =  Get-AzBlueprint -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myBlueprintName"
PS C:\> $secureString = @{mySecureStringParam=@{keyVaultId='/subscriptions/00000000-1111-0000-1111-000000000000/rsourcegroups/myResourceGroup/providers/Microsoft.Keyvault/Vaults/myKeyVault';secretName='mySecret';secretVersion='1.0'}}
PS C:\> New-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId "00000000-1111-0000-1111-000000000000" -Location "West US" -ResourceGroupParameter $rg -Parameter $params -SecureStringParameter $secureString

Name              : myAssignment
Id                : /subscriptions/00000000-1111-0000-1111-000000000000/providers/Microsoft.Blueprint/blueprintAssignments/myAssignment
Scope             : /subscriptions/00000000-1111-0000-1111-000000000000
LastModified      : 2019-01-08
LockMode          : None
ProvisioningState : Creating
Parameters        : {applytaganditsdefaultvalue_tagName, applytaganditsdefaultvalue_tagValue}
ResourceGroups    : ResourceGroup
```

<span data-ttu-id="ba130-111">使用已定義參數和資源群組字典，在指定的訂閱中建立藍圖定義 `$blueprintObject` 的新藍圖指派。</span><span class="sxs-lookup"><span data-stu-id="ba130-111">Create a new blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription using the defined parameter and resource group dictionary.</span></span> <span data-ttu-id="ba130-112">使用系統指派的身分識別。</span><span class="sxs-lookup"><span data-stu-id="ba130-112">Uses system-assigned identity.</span></span> <span data-ttu-id="ba130-113">位置會定義建立受管理身分識別的區域。</span><span class="sxs-lookup"><span data-stu-id="ba130-113">The location defines the region for creating the managed identity.</span></span>

### <span data-ttu-id="ba130-114">範例 2</span><span class="sxs-lookup"><span data-stu-id="ba130-114">Example 2</span></span>
```powershell
PS C:\> New-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId 00000000-1111-0000-1111-000000000000 -Location "West US" -Parameter @{P1="v1"; P2="v2"} -Lock AllResourcesReadOnly
```

<span data-ttu-id="ba130-115">使用已定義參數和資源群組字典，並設定資源鎖定至 `$blueprintObject` **AllResources，** 來建立指定訂閱中藍圖定義的新藍圖指派。</span><span class="sxs-lookup"><span data-stu-id="ba130-115">Create a new blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription using the defined parameter and resource group dictionary and configuring resource locking to **AllResources**.</span></span> <span data-ttu-id="ba130-116">預設為使用系統指派的身分識別。</span><span class="sxs-lookup"><span data-stu-id="ba130-116">Defaults to using system-assigned identity.</span></span>  <span data-ttu-id="ba130-117">位置會定義建立受管理身分識別的區域。</span><span class="sxs-lookup"><span data-stu-id="ba130-117">The location defines the region for creating the managed identity.</span></span>

### <span data-ttu-id="ba130-118">範例 3</span><span class="sxs-lookup"><span data-stu-id="ba130-118">Example 3</span></span>
```powershell
PS C:\> New-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId 00000000-1111-0000-1111-000000000000 -Location "West US" -Parameter @{P1="v1"; P2="v2"} -UserAssignedIdentity "/subscriptions/00000000-1111-0000-1111-000000000000/resourceGroups/my-resource-group/providers/Microsoft.ManagedIdentity/userAssignedIdentities/my-user-defined-identity"
```

<span data-ttu-id="ba130-119">使用已定義參數和資源群組字典，使用指定的使用者指派身分識別識別碼，在指定的訂閱內建立藍圖定義 `$blueprintObject` 的新藍圖指派。</span><span class="sxs-lookup"><span data-stu-id="ba130-119">Create a new blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription using the defined parameter and resource group dictionary using the specified user-assigned identity id.</span></span>

### <span data-ttu-id="ba130-120">範例 4</span><span class="sxs-lookup"><span data-stu-id="ba130-120">Example 4</span></span>
```powershell
PS C:\> $blueprintObject =  Get-AzBlueprint -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myBlueprintName"
PS C:\> New-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId "00000000-1111-0000-1111-000000000000" -AssignmentFile C:\myAssignmentfile.json

Name              : myAssignment
Id                : /subscriptions/00000000-1111-0000-1111-000000000000/providers/Microsoft.Blueprint/blueprintAssignments/myAssignment
Scope             : /subscriptions/00000000-1111-0000-1111-000000000000
LastModified      : 2019-01-08
LockMode          : None
ProvisioningState : Creating
Parameters        : {applytaganditsdefaultvalue_tagName, applytaganditsdefaultvalue_tagValue}
ResourceGroups    : ResourceGroup
```

<span data-ttu-id="ba130-121">透過作業檔案建立藍圖作業。</span><span class="sxs-lookup"><span data-stu-id="ba130-121">Create a blueprint assignment through an assignment file.</span></span> <span data-ttu-id="ba130-122">工作分派檔案格式可在要求/回應範例中找到： https://github.com/Azure/azure-rest-api-specs/tree/master/specification/blueprint/resource-manager/Microsoft.Blueprint/preview/2018-11-01-preview/examples</span><span class="sxs-lookup"><span data-stu-id="ba130-122">The format of the assignment file can be found in the request/response samples at: https://github.com/Azure/azure-rest-api-specs/tree/master/specification/blueprint/resource-manager/Microsoft.Blueprint/preview/2018-11-01-preview/examples</span></span>

### <span data-ttu-id="ba130-123">範例 5</span><span class="sxs-lookup"><span data-stu-id="ba130-123">Example 5</span></span>
```powershell
PS C:\> $blueprintObject =  Get-AzBlueprint -SubscriptionId "myManagementGroup" -Name "myBlueprintName"
PS C:\> New-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -ManagementGroupId "myManagementGroup" -SubscriptionId 00000000-1111-0000-1111-000000000000 -Location "West US" -Parameter @{P1="v1"; P2="v2"}
```

<span data-ttu-id="ba130-124">使用已定義參數建立藍圖定義的新藍圖指派，以指定管理群組內的指定 `$blueprintObject` 訂閱為目標。</span><span class="sxs-lookup"><span data-stu-id="ba130-124">Create a new blueprint assignment of the blueprint definition `$blueprintObject` targeting the specified subscription within the specified management group using the defined parameter.</span></span>

## <span data-ttu-id="ba130-125">參數</span><span class="sxs-lookup"><span data-stu-id="ba130-125">PARAMETERS</span></span>

### <span data-ttu-id="ba130-126">-AssignmentFile</span><span class="sxs-lookup"><span data-stu-id="ba130-126">-AssignmentFile</span></span>
<span data-ttu-id="ba130-127">作業檔案在磁片上以 JSON 格式顯示的位置。</span><span class="sxs-lookup"><span data-stu-id="ba130-127">Location of the assignment file in JSON format on disk.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateBlueprintAssignmentByFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba130-128">-藍圖</span><span class="sxs-lookup"><span data-stu-id="ba130-128">-Blueprint</span></span>
<span data-ttu-id="ba130-129">藍圖定義物件。</span><span class="sxs-lookup"><span data-stu-id="ba130-129">Blueprint definition object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase
Parameter Sets: CreateBlueprintAssignment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase
Parameter Sets: CreateBlueprintAssignmentByFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ba130-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba130-130">-DefaultProfile</span></span>
<span data-ttu-id="ba130-131">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="ba130-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ba130-132">-位置</span><span class="sxs-lookup"><span data-stu-id="ba130-132">-Location</span></span>
<span data-ttu-id="ba130-133">要建立受管理身分識別的區域。</span><span class="sxs-lookup"><span data-stu-id="ba130-133">Region for managed identity to be created in.</span></span>
<span data-ttu-id="ba130-134">若要深入瞭解，aka.ms/blueprintmsi</span><span class="sxs-lookup"><span data-stu-id="ba130-134">Learn more at aka.ms/blueprintmsi</span></span>

```yaml
Type: System.String
Parameter Sets: CreateBlueprintAssignment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba130-135">-鎖定</span><span class="sxs-lookup"><span data-stu-id="ba130-135">-Lock</span></span>
<span data-ttu-id="ba130-136">鎖定資源。</span><span class="sxs-lookup"><span data-stu-id="ba130-136">Lock resources.</span></span>
<span data-ttu-id="ba130-137">若要深入瞭解，請aka.ms/blueprintlocks</span><span class="sxs-lookup"><span data-stu-id="ba130-137">Learn more at aka.ms/blueprintlocks</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Blueprint.Models.PSLockMode]
Parameter Sets: CreateBlueprintAssignment
Aliases:
Accepted values: None, AllResourcesReadOnly, AllResourcesDoNotDelete

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba130-138">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="ba130-138">-ManagementGroupId</span></span>
<span data-ttu-id="ba130-139">儲存藍圖工作分派 (管理) 識別碼。</span><span class="sxs-lookup"><span data-stu-id="ba130-139">The ID of the management group where the Blueprint assignment(s) will be saved.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: CreateBlueprintAssignmentByFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba130-140">-名稱</span><span class="sxs-lookup"><span data-stu-id="ba130-140">-Name</span></span>
<span data-ttu-id="ba130-141">藍圖工作分派名稱。</span><span class="sxs-lookup"><span data-stu-id="ba130-141">Blueprint assignment name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateBlueprintAssignment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: CreateBlueprintAssignmentByFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba130-142">-Parameter</span><span class="sxs-lookup"><span data-stu-id="ba130-142">-Parameter</span></span>
<span data-ttu-id="ba130-143">產品參數。</span><span class="sxs-lookup"><span data-stu-id="ba130-143">Artifact parameters.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba130-144">-ResourceGroupParameter</span><span class="sxs-lookup"><span data-stu-id="ba130-144">-ResourceGroupParameter</span></span>
<span data-ttu-id="ba130-145">要傳遞至資源群組產品的參數雜湊表。</span><span class="sxs-lookup"><span data-stu-id="ba130-145">Hashtable of parameters to pass to the resource group artifact.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba130-146">-SecureStringParameter</span><span class="sxs-lookup"><span data-stu-id="ba130-146">-SecureStringParameter</span></span>
<span data-ttu-id="ba130-147">KeyVault 資源識別碼、名稱和版本的安全字串參數。</span><span class="sxs-lookup"><span data-stu-id="ba130-147">Secure string parameter for KeyVault resource id, name and version.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba130-148">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ba130-148">-SubscriptionId</span></span>
<span data-ttu-id="ba130-149">指派藍圖定義的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="ba130-149">Subscription Id to assign the blueprint definition.</span></span>
<span data-ttu-id="ba130-150">可以是 subscriptionId 字串的逗號分隔清單。</span><span class="sxs-lookup"><span data-stu-id="ba130-150">Can be a comma delimited list of subscriptionId strings.</span></span>

```yaml
Type: System.String[]
Parameter Sets: CreateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: CreateBlueprintAssignmentByFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba130-151">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="ba130-151">-SystemAssignedIdentity</span></span>
<span data-ttu-id="ba130-152">系統指派的身分識別 (MSI) 部署產品。</span><span class="sxs-lookup"><span data-stu-id="ba130-152">System assigned identity(MSI) to deploy the artifacts.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CreateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba130-153">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="ba130-153">-UserAssignedIdentity</span></span>
<span data-ttu-id="ba130-154">使用者指派的身分識別 (MSI) 部署產品。</span><span class="sxs-lookup"><span data-stu-id="ba130-154">User assigned identity(MSI) to deploy the artifacts.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba130-155">-確認</span><span class="sxs-lookup"><span data-stu-id="ba130-155">-Confirm</span></span>
<span data-ttu-id="ba130-156">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="ba130-156">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba130-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba130-157">-WhatIf</span></span>
<span data-ttu-id="ba130-158">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ba130-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba130-159">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ba130-159">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba130-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba130-160">CommonParameters</span></span>
<span data-ttu-id="ba130-161">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ba130-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba130-162">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ba130-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba130-163">輸入</span><span class="sxs-lookup"><span data-stu-id="ba130-163">INPUTS</span></span>

### <span data-ttu-id="ba130-164">System.String</span><span class="sxs-lookup"><span data-stu-id="ba130-164">System.String</span></span>

### <span data-ttu-id="ba130-165">Microsoft.Azure.Commands.藍圖.models.PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="ba130-165">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="ba130-166">System.String[]</span><span class="sxs-lookup"><span data-stu-id="ba130-166">System.String[]</span></span>

### <span data-ttu-id="ba130-167">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="ba130-167">System.Collections.Hashtable</span></span>

## <span data-ttu-id="ba130-168">輸出</span><span class="sxs-lookup"><span data-stu-id="ba130-168">OUTPUTS</span></span>

### <span data-ttu-id="ba130-169">System.Object</span><span class="sxs-lookup"><span data-stu-id="ba130-169">System.Object</span></span>
## <span data-ttu-id="ba130-170">筆記</span><span class="sxs-lookup"><span data-stu-id="ba130-170">NOTES</span></span>

## <span data-ttu-id="ba130-171">相關連結</span><span class="sxs-lookup"><span data-stu-id="ba130-171">RELATED LINKS</span></span>
