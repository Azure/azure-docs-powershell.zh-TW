---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/powershell/module/az.blueprint/set-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintAssignment.md
ms.openlocfilehash: 0e5c562d5b536e95d40bdbc1c08b2d778574fd41
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914921"
---
# <span data-ttu-id="c0c3a-101">Set-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="c0c3a-101">Set-AzBlueprintAssignment</span></span>

## <span data-ttu-id="c0c3a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c0c3a-102">SYNOPSIS</span></span>
<span data-ttu-id="c0c3a-103">更新現有的藍圖工作分派。</span><span class="sxs-lookup"><span data-stu-id="c0c3a-103">Update an existing blueprint assignment.</span></span>

## <span data-ttu-id="c0c3a-104">語法</span><span class="sxs-lookup"><span data-stu-id="c0c3a-104">SYNTAX</span></span>

### <span data-ttu-id="c0c3a-105">UpdateBlueprintAssignment (預設) </span><span class="sxs-lookup"><span data-stu-id="c0c3a-105">UpdateBlueprintAssignment (Default)</span></span>
```
Set-AzBlueprintAssignment -Name <String> -Blueprint <PSBlueprintBase> -Location <String>
 [-SystemAssignedIdentity] [-UserAssignedIdentity <String>] [-Lock <PSLockMode>]
 [-SecureStringParameter <Hashtable>] [-ResourceGroupParameter <Hashtable>] [-Parameter <Hashtable>]
 [-ManagementGroupId <String>] [-SubscriptionId <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0c3a-106">UpdateBlueprintAssignmentByFile</span><span class="sxs-lookup"><span data-stu-id="c0c3a-106">UpdateBlueprintAssignmentByFile</span></span>
```
Set-AzBlueprintAssignment -Name <String> [-Blueprint <PSBlueprintBase>] [-AssignmentFile <String>]
 [-ManagementGroupId <String>] [-SubscriptionId <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0c3a-107">描述</span><span class="sxs-lookup"><span data-stu-id="c0c3a-107">DESCRIPTION</span></span>
<span data-ttu-id="c0c3a-108">更新現有的藍圖工作分派。</span><span class="sxs-lookup"><span data-stu-id="c0c3a-108">Update an existing blueprint assignment.</span></span>

## <span data-ttu-id="c0c3a-109">例子</span><span class="sxs-lookup"><span data-stu-id="c0c3a-109">EXAMPLES</span></span>

### <span data-ttu-id="c0c3a-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="c0c3a-110">Example 1</span></span>
```powershell
PS C:\> $rg = @{ResourceGroup=@{name='storage_rg';location='eastus'}}
PS C:\> $params = @{applytaganditsdefaultvalue_tagName="Department_Cost_Center"; applytaganditsdefaultvalue_tagValue="Contoso/HR/Dev/0001"}
PS C:\> $blueprintObject =  Get-AzBlueprint -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myBlueprintName"
PS C:\> Set-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId "00000000-1111-0000-1111-000000000000" -Location "West US" -Parameter $params -ResourceGroupParameter $rg -SystemAssignedIdentity

Name              : myAssignment
Id                : /subscriptions/00000000-1111-0000-1111-000000000000/providers/Microsoft.Blueprint/blueprintAssignments/myAssignment
Scope             : /subscriptions/00000000-1111-0000-1111-000000000000
LastModified      : 2019-01-08
LockMode          : None
ProvisioningState : Creating
Parameters        : {applytaganditsdefaultvalue_tagName, applytaganditsdefaultvalue_tagValue}
ResourceGroups    : ResourceGroup
```

<span data-ttu-id="c0c3a-111">更新指定訂閱中藍圖定義的現有藍圖指派 `$blueprintObject` ，更新參數。</span><span class="sxs-lookup"><span data-stu-id="c0c3a-111">Update an existing blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription, updating the parameters.</span></span> <span data-ttu-id="c0c3a-112">使用系統指派的身分識別。</span><span class="sxs-lookup"><span data-stu-id="c0c3a-112">Uses system-assigned identity.</span></span> <span data-ttu-id="c0c3a-113">位置會定義建立受管理身分識別的區域。</span><span class="sxs-lookup"><span data-stu-id="c0c3a-113">The location defines the region for creating the managed identity.</span></span>

### <span data-ttu-id="c0c3a-114">範例 2</span><span class="sxs-lookup"><span data-stu-id="c0c3a-114">Example 2</span></span>
```powershell
PS C:\> $blueprintObject =  Get-AzBlueprint -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myBlueprintName"
PS C:\> Set-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId "00000000-1111-0000-1111-000000000000" -AssignmentFile C:\myAssignmentfile.json

Name              : myAssignment
Id                : /subscriptions/00000000-1111-0000-1111-000000000000/providers/Microsoft.Blueprint/blueprintAssignments/myAssignment
Scope             : /subscriptions/00000000-1111-0000-1111-000000000000
LastModified      : 2019-01-08
LockMode          : None
ProvisioningState : Creating
Parameters        : {applytaganditsdefaultvalue_tagName, applytaganditsdefaultvalue_tagValue}
ResourceGroups    : ResourceGroup
```

<span data-ttu-id="c0c3a-115">透過作業檔案更新現有的藍圖指派。</span><span class="sxs-lookup"><span data-stu-id="c0c3a-115">Update an existing blueprint assignment through an assignment file.</span></span> <span data-ttu-id="c0c3a-116">工作分派檔案格式可在要求/回應範例中找到： https://github.com/Azure/azure-rest-api-specs/tree/master/specification/blueprint/resource-manager/Microsoft.Blueprint/preview/2018-11-01-preview/examples</span><span class="sxs-lookup"><span data-stu-id="c0c3a-116">The format of the assignment file can be found in the request/response samples at: https://github.com/Azure/azure-rest-api-specs/tree/master/specification/blueprint/resource-manager/Microsoft.Blueprint/preview/2018-11-01-preview/examples</span></span>

### <span data-ttu-id="c0c3a-117">範例 3</span><span class="sxs-lookup"><span data-stu-id="c0c3a-117">Example 3</span></span>
```powershell
PS C:\> $blueprintObject =  Get-AzBlueprint -ManagementGroup "myManagementGroup" -Name "myBlueprintName"
PS C:\> Set-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -ManagementGroupId "myManagementGroup" -SubscriptionId 00000000-1111-0000-1111-000000000000 -Location "West US" -Parameter @{P1="v1"; P2="v2"}
```

<span data-ttu-id="c0c3a-118">使用已定義參數更新指定管理群組中指定訂閱的藍圖定義現有 `$blueprintObject` 藍圖指派。</span><span class="sxs-lookup"><span data-stu-id="c0c3a-118">Update an existing blueprint assignment of the blueprint definition `$blueprintObject` targeting the specified subscription within the specified management group using the defined parameter.</span></span>

## <span data-ttu-id="c0c3a-119">參數</span><span class="sxs-lookup"><span data-stu-id="c0c3a-119">PARAMETERS</span></span>

### <span data-ttu-id="c0c3a-120">-AssignmentFile</span><span class="sxs-lookup"><span data-stu-id="c0c3a-120">-AssignmentFile</span></span>
<span data-ttu-id="c0c3a-121">作業檔案在磁片上以 JSON 格式顯示的位置。</span><span class="sxs-lookup"><span data-stu-id="c0c3a-121">Location of the assignment file in JSON format on disk.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateBlueprintAssignmentByFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0c3a-122">-藍圖</span><span class="sxs-lookup"><span data-stu-id="c0c3a-122">-Blueprint</span></span>
<span data-ttu-id="c0c3a-123">藍圖物件。</span><span class="sxs-lookup"><span data-stu-id="c0c3a-123">Blueprint object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase
Parameter Sets: UpdateBlueprintAssignment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase
Parameter Sets: UpdateBlueprintAssignmentByFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c0c3a-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0c3a-124">-DefaultProfile</span></span>
<span data-ttu-id="c0c3a-125">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="c0c3a-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0c3a-126">-位置</span><span class="sxs-lookup"><span data-stu-id="c0c3a-126">-Location</span></span>
<span data-ttu-id="c0c3a-127">要建立受管理身分識別的區域。</span><span class="sxs-lookup"><span data-stu-id="c0c3a-127">Region for managed identity to be created in.</span></span>
<span data-ttu-id="c0c3a-128">若要深入瞭解，aka.ms/blueprintmsi</span><span class="sxs-lookup"><span data-stu-id="c0c3a-128">Learn more at aka.ms/blueprintmsi</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateBlueprintAssignment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0c3a-129">-鎖定</span><span class="sxs-lookup"><span data-stu-id="c0c3a-129">-Lock</span></span>
<span data-ttu-id="c0c3a-130">鎖定資源。</span><span class="sxs-lookup"><span data-stu-id="c0c3a-130">Lock resources.</span></span>
<span data-ttu-id="c0c3a-131">若要深入瞭解，請aka.ms/blueprintlocks</span><span class="sxs-lookup"><span data-stu-id="c0c3a-131">Learn more at aka.ms/blueprintlocks</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Blueprint.Models.PSLockMode]
Parameter Sets: UpdateBlueprintAssignment
Aliases:
Accepted values: None, AllResourcesReadOnly, AllResourcesDoNotDelete

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0c3a-132">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="c0c3a-132">-ManagementGroupId</span></span>
<span data-ttu-id="c0c3a-133">儲存藍圖工作分派 (管理) 識別碼。</span><span class="sxs-lookup"><span data-stu-id="c0c3a-133">The ID of the management group where the Blueprint assignment(s) will be saved.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: UpdateBlueprintAssignmentByFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0c3a-134">-名稱</span><span class="sxs-lookup"><span data-stu-id="c0c3a-134">-Name</span></span>
<span data-ttu-id="c0c3a-135">藍圖工作分派名稱。</span><span class="sxs-lookup"><span data-stu-id="c0c3a-135">Blueprint assignment name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateBlueprintAssignment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: UpdateBlueprintAssignmentByFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0c3a-136">-Parameter</span><span class="sxs-lookup"><span data-stu-id="c0c3a-136">-Parameter</span></span>
<span data-ttu-id="c0c3a-137">專案參數。</span><span class="sxs-lookup"><span data-stu-id="c0c3a-137">Artifact parameter.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0c3a-138">-ResourceGroupParameter</span><span class="sxs-lookup"><span data-stu-id="c0c3a-138">-ResourceGroupParameter</span></span>
<span data-ttu-id="c0c3a-139">要傳遞至資源群組產品的參數雜湊表。</span><span class="sxs-lookup"><span data-stu-id="c0c3a-139">Hashtable of parameters to pass to the resource group artifact.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0c3a-140">-SecureStringParameter</span><span class="sxs-lookup"><span data-stu-id="c0c3a-140">-SecureStringParameter</span></span>
<span data-ttu-id="c0c3a-141">KeyVault 資源識別碼、名稱和版本的安全字串參數。</span><span class="sxs-lookup"><span data-stu-id="c0c3a-141">Secure string parameter for KeyVault resource id, name and version.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0c3a-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c0c3a-142">-SubscriptionId</span></span>
<span data-ttu-id="c0c3a-143">SubscriptionId 以指派藍圖。</span><span class="sxs-lookup"><span data-stu-id="c0c3a-143">SubscriptionId to assign the Blueprint.</span></span>
<span data-ttu-id="c0c3a-144">可以是 subscriptionId 字串的逗號分隔清單。</span><span class="sxs-lookup"><span data-stu-id="c0c3a-144">Can be a comma delimited list of subscriptionId strings.</span></span>

```yaml
Type: System.String[]
Parameter Sets: UpdateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: UpdateBlueprintAssignmentByFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0c3a-145">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="c0c3a-145">-SystemAssignedIdentity</span></span>
<span data-ttu-id="c0c3a-146">系統指派的身分識別 (MSI) 部署產品。</span><span class="sxs-lookup"><span data-stu-id="c0c3a-146">System assigned identity(MSI) to deploy the artifacts.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UpdateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0c3a-147">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="c0c3a-147">-UserAssignedIdentity</span></span>
<span data-ttu-id="c0c3a-148">使用者指派的身分識別 (MSI) 部署產品。</span><span class="sxs-lookup"><span data-stu-id="c0c3a-148">User assigned identity(MSI) to deploy the artifacts.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0c3a-149">-確認</span><span class="sxs-lookup"><span data-stu-id="c0c3a-149">-Confirm</span></span>
<span data-ttu-id="c0c3a-150">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="c0c3a-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0c3a-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0c3a-151">-WhatIf</span></span>
<span data-ttu-id="c0c3a-152">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c0c3a-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0c3a-153">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c0c3a-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0c3a-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0c3a-154">CommonParameters</span></span>
<span data-ttu-id="c0c3a-155">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c0c3a-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0c3a-156">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c0c3a-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0c3a-157">輸入</span><span class="sxs-lookup"><span data-stu-id="c0c3a-157">INPUTS</span></span>

### <span data-ttu-id="c0c3a-158">System.String</span><span class="sxs-lookup"><span data-stu-id="c0c3a-158">System.String</span></span>

### <span data-ttu-id="c0c3a-159">Microsoft.Azure.Commands.藍圖.models.PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="c0c3a-159">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="c0c3a-160">System.String[]</span><span class="sxs-lookup"><span data-stu-id="c0c3a-160">System.String[]</span></span>

### <span data-ttu-id="c0c3a-161">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="c0c3a-161">System.Collections.Hashtable</span></span>

## <span data-ttu-id="c0c3a-162">輸出</span><span class="sxs-lookup"><span data-stu-id="c0c3a-162">OUTPUTS</span></span>

### <span data-ttu-id="c0c3a-163">System.Object</span><span class="sxs-lookup"><span data-stu-id="c0c3a-163">System.Object</span></span>
## <span data-ttu-id="c0c3a-164">筆記</span><span class="sxs-lookup"><span data-stu-id="c0c3a-164">NOTES</span></span>

## <span data-ttu-id="c0c3a-165">相關連結</span><span class="sxs-lookup"><span data-stu-id="c0c3a-165">RELATED LINKS</span></span>
