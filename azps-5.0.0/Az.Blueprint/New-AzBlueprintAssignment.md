---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/new-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprintAssignment.md
ms.openlocfilehash: 295e70d91af0c6c06ac913c10bfe5a9e265523c9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94137547"
---
# <span data-ttu-id="b60c2-101">New-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="b60c2-101">New-AzBlueprintAssignment</span></span>

## <span data-ttu-id="b60c2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b60c2-102">SYNOPSIS</span></span>
<span data-ttu-id="b60c2-103">將藍圖定義指派給訂閱或管理群組。</span><span class="sxs-lookup"><span data-stu-id="b60c2-103">Assign a blueprint definition to a subscription or a management group.</span></span>

## <span data-ttu-id="b60c2-104">句法</span><span class="sxs-lookup"><span data-stu-id="b60c2-104">SYNTAX</span></span>

### <span data-ttu-id="b60c2-105">CreateBlueprintAssignment (預設) </span><span class="sxs-lookup"><span data-stu-id="b60c2-105">CreateBlueprintAssignment (Default)</span></span>
```
New-AzBlueprintAssignment -Name <String> -Blueprint <PSBlueprintBase> -Location <String>
 [-SystemAssignedIdentity] [-UserAssignedIdentity <String>] [-Lock <PSLockMode>]
 [-SecureStringParameter <Hashtable>] [-ResourceGroupParameter <Hashtable>] [-Parameter <Hashtable>]
 [-ManagementGroupId <String>] [-SubscriptionId <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b60c2-106">CreateBlueprintAssignmentByFile</span><span class="sxs-lookup"><span data-stu-id="b60c2-106">CreateBlueprintAssignmentByFile</span></span>
```
New-AzBlueprintAssignment -Name <String> [-Blueprint <PSBlueprintBase>] [-AssignmentFile <String>]
 [-ManagementGroupId <String>] [-SubscriptionId <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b60c2-107">說明</span><span class="sxs-lookup"><span data-stu-id="b60c2-107">DESCRIPTION</span></span>
<span data-ttu-id="b60c2-108">將藍圖定義指派給訂閱。</span><span class="sxs-lookup"><span data-stu-id="b60c2-108">Assign a blueprint definition to a subscription.</span></span>

## <span data-ttu-id="b60c2-109">示例</span><span class="sxs-lookup"><span data-stu-id="b60c2-109">EXAMPLES</span></span>

### <span data-ttu-id="b60c2-110">範例1</span><span class="sxs-lookup"><span data-stu-id="b60c2-110">Example 1</span></span>
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

<span data-ttu-id="b60c2-111">`$blueprintObject`使用已定義的參數和資源群組字典，在指定的訂閱中建立藍圖定義的新藍圖指派。</span><span class="sxs-lookup"><span data-stu-id="b60c2-111">Create a new blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription using the defined parameter and resource group dictionary.</span></span> <span data-ttu-id="b60c2-112">使用系統指派的身分識別。</span><span class="sxs-lookup"><span data-stu-id="b60c2-112">Uses system-assigned identity.</span></span> <span data-ttu-id="b60c2-113">位置定義建立受管理身分識別的區域。</span><span class="sxs-lookup"><span data-stu-id="b60c2-113">The location defines the region for creating the managed identity.</span></span>

### <span data-ttu-id="b60c2-114">範例2</span><span class="sxs-lookup"><span data-stu-id="b60c2-114">Example 2</span></span>
```powershell
PS C:\> New-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId 00000000-1111-0000-1111-000000000000 -Location "West US" -Parameter @{P1="v1"; P2="v2"} -Lock AllResourcesReadOnly
```

<span data-ttu-id="b60c2-115">`$blueprintObject`使用已定義的參數和資源群組字典，並將資源鎖定設定為 **AllResources** ，以在指定的訂閱中建立藍圖定義的新藍圖指派。</span><span class="sxs-lookup"><span data-stu-id="b60c2-115">Create a new blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription using the defined parameter and resource group dictionary and configuring resource locking to **AllResources**.</span></span> <span data-ttu-id="b60c2-116">預設為使用系統指派的身分識別。</span><span class="sxs-lookup"><span data-stu-id="b60c2-116">Defaults to using system-assigned identity.</span></span>  <span data-ttu-id="b60c2-117">位置定義建立受管理身分識別的區域。</span><span class="sxs-lookup"><span data-stu-id="b60c2-117">The location defines the region for creating the managed identity.</span></span>

### <span data-ttu-id="b60c2-118">範例3</span><span class="sxs-lookup"><span data-stu-id="b60c2-118">Example 3</span></span>
```powershell
PS C:\> New-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId 00000000-1111-0000-1111-000000000000 -Location "West US" -Parameter @{P1="v1"; P2="v2"} -UserAssignedIdentity "/subscriptions/00000000-1111-0000-1111-000000000000/resourceGroups/my-resource-group/providers/Microsoft.ManagedIdentity/userAssignedIdentities/my-user-defined-identity"
```

<span data-ttu-id="b60c2-119">`$blueprintObject`使用已定義的參數和資源群組字典，在指定的訂閱中使用指定的使用者指派身分識別識別碼來建立藍圖定義的新藍圖指派。</span><span class="sxs-lookup"><span data-stu-id="b60c2-119">Create a new blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription using the defined parameter and resource group dictionary using the specified user-assigned identity id.</span></span>

### <span data-ttu-id="b60c2-120">範例4</span><span class="sxs-lookup"><span data-stu-id="b60c2-120">Example 4</span></span>
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

<span data-ttu-id="b60c2-121">透過作業檔案建立藍圖作業。</span><span class="sxs-lookup"><span data-stu-id="b60c2-121">Create a blueprint assignment through an assignment file.</span></span> <span data-ttu-id="b60c2-122">您可以在 [要求/回應] 範例中找到作業檔的格式，網址如下： https://github.com/Azure/azure-rest-api-specs/tree/master/specification/blueprint/resource-manager/Microsoft.Blueprint/preview/2018-11-01-preview/examples</span><span class="sxs-lookup"><span data-stu-id="b60c2-122">The format of the assignment file can be found in the request/response samples at: https://github.com/Azure/azure-rest-api-specs/tree/master/specification/blueprint/resource-manager/Microsoft.Blueprint/preview/2018-11-01-preview/examples</span></span>

### <span data-ttu-id="b60c2-123">範例5</span><span class="sxs-lookup"><span data-stu-id="b60c2-123">Example 5</span></span>
```powershell
PS C:\> $blueprintObject =  Get-AzBlueprint -SubscriptionId "myManagementGroup" -Name "myBlueprintName"
PS C:\> New-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -ManagementGroupId "myManagementGroup" -SubscriptionId 00000000-1111-0000-1111-000000000000 -Location "West US" -Parameter @{P1="v1"; P2="v2"}
```

<span data-ttu-id="b60c2-124">`$blueprintObject`使用已定義的參數，在指定的管理群組內，以指定的訂閱來建立藍圖定義的新藍圖指派。</span><span class="sxs-lookup"><span data-stu-id="b60c2-124">Create a new blueprint assignment of the blueprint definition `$blueprintObject` targeting the specified subscription within the specified management group using the defined parameter.</span></span>

## <span data-ttu-id="b60c2-125">參數</span><span class="sxs-lookup"><span data-stu-id="b60c2-125">PARAMETERS</span></span>

### <span data-ttu-id="b60c2-126">-AssignmentFile</span><span class="sxs-lookup"><span data-stu-id="b60c2-126">-AssignmentFile</span></span>
<span data-ttu-id="b60c2-127">在磁片上 JSON 格式的作業檔案位置。</span><span class="sxs-lookup"><span data-stu-id="b60c2-127">Location of the assignment file in JSON format on disk.</span></span>

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

### <span data-ttu-id="b60c2-128">-藍圖</span><span class="sxs-lookup"><span data-stu-id="b60c2-128">-Blueprint</span></span>
<span data-ttu-id="b60c2-129">藍圖定義物件。</span><span class="sxs-lookup"><span data-stu-id="b60c2-129">Blueprint definition object.</span></span>

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

### <span data-ttu-id="b60c2-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b60c2-130">-DefaultProfile</span></span>
<span data-ttu-id="b60c2-131">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b60c2-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b60c2-132">-位置</span><span class="sxs-lookup"><span data-stu-id="b60c2-132">-Location</span></span>
<span data-ttu-id="b60c2-133">要在其中建立受管理身分識別的地區。</span><span class="sxs-lookup"><span data-stu-id="b60c2-133">Region for managed identity to be created in.</span></span>
<span data-ttu-id="b60c2-134">深入瞭解 aka.ms/blueprintmsi</span><span class="sxs-lookup"><span data-stu-id="b60c2-134">Learn more at aka.ms/blueprintmsi</span></span>

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

### <span data-ttu-id="b60c2-135">鎖</span><span class="sxs-lookup"><span data-stu-id="b60c2-135">-Lock</span></span>
<span data-ttu-id="b60c2-136">鎖定資源。</span><span class="sxs-lookup"><span data-stu-id="b60c2-136">Lock resources.</span></span>
<span data-ttu-id="b60c2-137">深入瞭解 aka.ms/blueprintlocks</span><span class="sxs-lookup"><span data-stu-id="b60c2-137">Learn more at aka.ms/blueprintlocks</span></span>

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

### <span data-ttu-id="b60c2-138">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="b60c2-138">-ManagementGroupId</span></span>
<span data-ttu-id="b60c2-139">將儲存藍圖指派 (s) 之管理群組的識別碼。</span><span class="sxs-lookup"><span data-stu-id="b60c2-139">The ID of the management group where the Blueprint assignment(s) will be saved.</span></span>

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

### <span data-ttu-id="b60c2-140">-名稱</span><span class="sxs-lookup"><span data-stu-id="b60c2-140">-Name</span></span>
<span data-ttu-id="b60c2-141">藍圖作業名稱。</span><span class="sxs-lookup"><span data-stu-id="b60c2-141">Blueprint assignment name.</span></span>

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

### <span data-ttu-id="b60c2-142">-參數</span><span class="sxs-lookup"><span data-stu-id="b60c2-142">-Parameter</span></span>
<span data-ttu-id="b60c2-143">專案參數。</span><span class="sxs-lookup"><span data-stu-id="b60c2-143">Artifact parameters.</span></span>

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

### <span data-ttu-id="b60c2-144">-ResourceGroupParameter</span><span class="sxs-lookup"><span data-stu-id="b60c2-144">-ResourceGroupParameter</span></span>
<span data-ttu-id="b60c2-145">要傳遞給資源群組專案的參數雜湊值。</span><span class="sxs-lookup"><span data-stu-id="b60c2-145">Hashtable of parameters to pass to the resource group artifact.</span></span>

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

### <span data-ttu-id="b60c2-146">-SecureStringParameter</span><span class="sxs-lookup"><span data-stu-id="b60c2-146">-SecureStringParameter</span></span>
<span data-ttu-id="b60c2-147">KeyVault 資源識別碼、名稱和版本的安全字串參數。</span><span class="sxs-lookup"><span data-stu-id="b60c2-147">Secure string parameter for KeyVault resource id, name and version.</span></span>

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

### <span data-ttu-id="b60c2-148">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b60c2-148">-SubscriptionId</span></span>
<span data-ttu-id="b60c2-149">[訂閱識別碼] 可指派藍圖定義。</span><span class="sxs-lookup"><span data-stu-id="b60c2-149">Subscription Id to assign the blueprint definition.</span></span>
<span data-ttu-id="b60c2-150">可以是以逗號分隔的 subscriptionId 字串清單。</span><span class="sxs-lookup"><span data-stu-id="b60c2-150">Can be a comma delimited list of subscriptionId strings.</span></span>

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

### <span data-ttu-id="b60c2-151">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="b60c2-151">-SystemAssignedIdentity</span></span>
<span data-ttu-id="b60c2-152">系統指派身分識別 (MSI) 來部署該專案。</span><span class="sxs-lookup"><span data-stu-id="b60c2-152">System assigned identity(MSI) to deploy the artifacts.</span></span>

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

### <span data-ttu-id="b60c2-153">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="b60c2-153">-UserAssignedIdentity</span></span>
<span data-ttu-id="b60c2-154">使用者指派身分識別 (MSI) 來部署該專案。</span><span class="sxs-lookup"><span data-stu-id="b60c2-154">User assigned identity(MSI) to deploy the artifacts.</span></span>

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

### <span data-ttu-id="b60c2-155">-確認</span><span class="sxs-lookup"><span data-stu-id="b60c2-155">-Confirm</span></span>
<span data-ttu-id="b60c2-156">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b60c2-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b60c2-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b60c2-157">-WhatIf</span></span>
<span data-ttu-id="b60c2-158">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b60c2-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b60c2-159">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b60c2-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b60c2-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b60c2-160">CommonParameters</span></span>
<span data-ttu-id="b60c2-161">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b60c2-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b60c2-162">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b60c2-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b60c2-163">輸入</span><span class="sxs-lookup"><span data-stu-id="b60c2-163">INPUTS</span></span>

### <span data-ttu-id="b60c2-164">System.object</span><span class="sxs-lookup"><span data-stu-id="b60c2-164">System.String</span></span>

### <span data-ttu-id="b60c2-165">PSBlueprintBase 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="b60c2-165">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="b60c2-166">System.object []</span><span class="sxs-lookup"><span data-stu-id="b60c2-166">System.String[]</span></span>

### <span data-ttu-id="b60c2-167">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="b60c2-167">System.Collections.Hashtable</span></span>

## <span data-ttu-id="b60c2-168">輸出</span><span class="sxs-lookup"><span data-stu-id="b60c2-168">OUTPUTS</span></span>

### <span data-ttu-id="b60c2-169">System.object</span><span class="sxs-lookup"><span data-stu-id="b60c2-169">System.Object</span></span>
## <span data-ttu-id="b60c2-170">筆記</span><span class="sxs-lookup"><span data-stu-id="b60c2-170">NOTES</span></span>

## <span data-ttu-id="b60c2-171">相關連結</span><span class="sxs-lookup"><span data-stu-id="b60c2-171">RELATED LINKS</span></span>
