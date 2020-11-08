---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/set-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintAssignment.md
ms.openlocfilehash: b8913ead9844a55190a6117f57f01d243e004fde
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94140668"
---
# <span data-ttu-id="0b2e5-101">Set-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="0b2e5-101">Set-AzBlueprintAssignment</span></span>

## <span data-ttu-id="0b2e5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0b2e5-102">SYNOPSIS</span></span>
<span data-ttu-id="0b2e5-103">更新現有的藍圖作業。</span><span class="sxs-lookup"><span data-stu-id="0b2e5-103">Update an existing blueprint assignment.</span></span>

## <span data-ttu-id="0b2e5-104">句法</span><span class="sxs-lookup"><span data-stu-id="0b2e5-104">SYNTAX</span></span>

### <span data-ttu-id="0b2e5-105">UpdateBlueprintAssignment (預設) </span><span class="sxs-lookup"><span data-stu-id="0b2e5-105">UpdateBlueprintAssignment (Default)</span></span>
```
Set-AzBlueprintAssignment -Name <String> -Blueprint <PSBlueprintBase> -Location <String>
 [-SystemAssignedIdentity] [-UserAssignedIdentity <String>] [-Lock <PSLockMode>]
 [-SecureStringParameter <Hashtable>] [-ResourceGroupParameter <Hashtable>] [-Parameter <Hashtable>]
 [-ManagementGroupId <String>] [-SubscriptionId <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b2e5-106">UpdateBlueprintAssignmentByFile</span><span class="sxs-lookup"><span data-stu-id="0b2e5-106">UpdateBlueprintAssignmentByFile</span></span>
```
Set-AzBlueprintAssignment -Name <String> [-Blueprint <PSBlueprintBase>] [-AssignmentFile <String>]
 [-ManagementGroupId <String>] [-SubscriptionId <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0b2e5-107">說明</span><span class="sxs-lookup"><span data-stu-id="0b2e5-107">DESCRIPTION</span></span>
<span data-ttu-id="0b2e5-108">更新現有的藍圖作業。</span><span class="sxs-lookup"><span data-stu-id="0b2e5-108">Update an existing blueprint assignment.</span></span>

## <span data-ttu-id="0b2e5-109">示例</span><span class="sxs-lookup"><span data-stu-id="0b2e5-109">EXAMPLES</span></span>

### <span data-ttu-id="0b2e5-110">範例1</span><span class="sxs-lookup"><span data-stu-id="0b2e5-110">Example 1</span></span>
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

<span data-ttu-id="0b2e5-111">在指定的訂閱中，更新藍圖定義的現有藍圖指派 `$blueprintObject` ，並更新參數。</span><span class="sxs-lookup"><span data-stu-id="0b2e5-111">Update an existing blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription, updating the parameters.</span></span> <span data-ttu-id="0b2e5-112">使用系統指派的身分識別。</span><span class="sxs-lookup"><span data-stu-id="0b2e5-112">Uses system-assigned identity.</span></span> <span data-ttu-id="0b2e5-113">位置定義建立受管理身分識別的區域。</span><span class="sxs-lookup"><span data-stu-id="0b2e5-113">The location defines the region for creating the managed identity.</span></span>

### <span data-ttu-id="0b2e5-114">範例2</span><span class="sxs-lookup"><span data-stu-id="0b2e5-114">Example 2</span></span>
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

<span data-ttu-id="0b2e5-115">透過作業檔案更新現有的藍圖作業。</span><span class="sxs-lookup"><span data-stu-id="0b2e5-115">Update an existing blueprint assignment through an assignment file.</span></span> <span data-ttu-id="0b2e5-116">您可以在 [要求/回應] 範例中找到作業檔的格式，網址如下： https://github.com/Azure/azure-rest-api-specs/tree/master/specification/blueprint/resource-manager/Microsoft.Blueprint/preview/2018-11-01-preview/examples</span><span class="sxs-lookup"><span data-stu-id="0b2e5-116">The format of the assignment file can be found in the request/response samples at: https://github.com/Azure/azure-rest-api-specs/tree/master/specification/blueprint/resource-manager/Microsoft.Blueprint/preview/2018-11-01-preview/examples</span></span>

### <span data-ttu-id="0b2e5-117">範例3</span><span class="sxs-lookup"><span data-stu-id="0b2e5-117">Example 3</span></span>
```powershell
PS C:\> $blueprintObject =  Get-AzBlueprint -ManagementGroup "myManagementGroup" -Name "myBlueprintName"
PS C:\> Set-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -ManagementGroupId "myManagementGroup" -SubscriptionId 00000000-1111-0000-1111-000000000000 -Location "West US" -Parameter @{P1="v1"; P2="v2"}
```

<span data-ttu-id="0b2e5-118">`$blueprintObject`使用已定義的參數，更新以指定的管理群組中指定訂閱為目標的藍圖定義的現有藍圖指派。</span><span class="sxs-lookup"><span data-stu-id="0b2e5-118">Update an existing blueprint assignment of the blueprint definition `$blueprintObject` targeting the specified subscription within the specified management group using the defined parameter.</span></span>

## <span data-ttu-id="0b2e5-119">參數</span><span class="sxs-lookup"><span data-stu-id="0b2e5-119">PARAMETERS</span></span>

### <span data-ttu-id="0b2e5-120">-AssignmentFile</span><span class="sxs-lookup"><span data-stu-id="0b2e5-120">-AssignmentFile</span></span>
<span data-ttu-id="0b2e5-121">在磁片上 JSON 格式的作業檔案位置。</span><span class="sxs-lookup"><span data-stu-id="0b2e5-121">Location of the assignment file in JSON format on disk.</span></span>

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

### <span data-ttu-id="0b2e5-122">-藍圖</span><span class="sxs-lookup"><span data-stu-id="0b2e5-122">-Blueprint</span></span>
<span data-ttu-id="0b2e5-123">藍圖物件。</span><span class="sxs-lookup"><span data-stu-id="0b2e5-123">Blueprint object.</span></span>

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

### <span data-ttu-id="0b2e5-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b2e5-124">-DefaultProfile</span></span>
<span data-ttu-id="0b2e5-125">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0b2e5-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b2e5-126">-位置</span><span class="sxs-lookup"><span data-stu-id="0b2e5-126">-Location</span></span>
<span data-ttu-id="0b2e5-127">要在其中建立受管理身分識別的地區。</span><span class="sxs-lookup"><span data-stu-id="0b2e5-127">Region for managed identity to be created in.</span></span>
<span data-ttu-id="0b2e5-128">深入瞭解 aka.ms/blueprintmsi</span><span class="sxs-lookup"><span data-stu-id="0b2e5-128">Learn more at aka.ms/blueprintmsi</span></span>

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

### <span data-ttu-id="0b2e5-129">鎖</span><span class="sxs-lookup"><span data-stu-id="0b2e5-129">-Lock</span></span>
<span data-ttu-id="0b2e5-130">鎖定資源。</span><span class="sxs-lookup"><span data-stu-id="0b2e5-130">Lock resources.</span></span>
<span data-ttu-id="0b2e5-131">深入瞭解 aka.ms/blueprintlocks</span><span class="sxs-lookup"><span data-stu-id="0b2e5-131">Learn more at aka.ms/blueprintlocks</span></span>

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

### <span data-ttu-id="0b2e5-132">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="0b2e5-132">-ManagementGroupId</span></span>
<span data-ttu-id="0b2e5-133">將儲存藍圖指派 (s) 之管理群組的識別碼。</span><span class="sxs-lookup"><span data-stu-id="0b2e5-133">The ID of the management group where the Blueprint assignment(s) will be saved.</span></span>

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

### <span data-ttu-id="0b2e5-134">-名稱</span><span class="sxs-lookup"><span data-stu-id="0b2e5-134">-Name</span></span>
<span data-ttu-id="0b2e5-135">藍圖作業名稱。</span><span class="sxs-lookup"><span data-stu-id="0b2e5-135">Blueprint assignment name.</span></span>

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

### <span data-ttu-id="0b2e5-136">-參數</span><span class="sxs-lookup"><span data-stu-id="0b2e5-136">-Parameter</span></span>
<span data-ttu-id="0b2e5-137">專案參數。</span><span class="sxs-lookup"><span data-stu-id="0b2e5-137">Artifact parameter.</span></span>

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

### <span data-ttu-id="0b2e5-138">-ResourceGroupParameter</span><span class="sxs-lookup"><span data-stu-id="0b2e5-138">-ResourceGroupParameter</span></span>
<span data-ttu-id="0b2e5-139">要傳遞給資源群組專案的參數雜湊值。</span><span class="sxs-lookup"><span data-stu-id="0b2e5-139">Hashtable of parameters to pass to the resource group artifact.</span></span>

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

### <span data-ttu-id="0b2e5-140">-SecureStringParameter</span><span class="sxs-lookup"><span data-stu-id="0b2e5-140">-SecureStringParameter</span></span>
<span data-ttu-id="0b2e5-141">KeyVault 資源識別碼、名稱和版本的安全字串參數。</span><span class="sxs-lookup"><span data-stu-id="0b2e5-141">Secure string parameter for KeyVault resource id, name and version.</span></span>

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

### <span data-ttu-id="0b2e5-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0b2e5-142">-SubscriptionId</span></span>
<span data-ttu-id="0b2e5-143">[SubscriptionId] 可指派藍圖。</span><span class="sxs-lookup"><span data-stu-id="0b2e5-143">SubscriptionId to assign the Blueprint.</span></span>
<span data-ttu-id="0b2e5-144">可以是以逗號分隔的 subscriptionId 字串清單。</span><span class="sxs-lookup"><span data-stu-id="0b2e5-144">Can be a comma delimited list of subscriptionId strings.</span></span>

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

### <span data-ttu-id="0b2e5-145">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="0b2e5-145">-SystemAssignedIdentity</span></span>
<span data-ttu-id="0b2e5-146">系統指派身分識別 (MSI) 來部署該專案。</span><span class="sxs-lookup"><span data-stu-id="0b2e5-146">System assigned identity(MSI) to deploy the artifacts.</span></span>

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

### <span data-ttu-id="0b2e5-147">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="0b2e5-147">-UserAssignedIdentity</span></span>
<span data-ttu-id="0b2e5-148">使用者指派身分識別 (MSI) 來部署該專案。</span><span class="sxs-lookup"><span data-stu-id="0b2e5-148">User assigned identity(MSI) to deploy the artifacts.</span></span>

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

### <span data-ttu-id="0b2e5-149">-確認</span><span class="sxs-lookup"><span data-stu-id="0b2e5-149">-Confirm</span></span>
<span data-ttu-id="0b2e5-150">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="0b2e5-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b2e5-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b2e5-151">-WhatIf</span></span>
<span data-ttu-id="0b2e5-152">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0b2e5-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0b2e5-153">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0b2e5-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b2e5-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b2e5-154">CommonParameters</span></span>
<span data-ttu-id="0b2e5-155">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0b2e5-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b2e5-156">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="0b2e5-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b2e5-157">輸入</span><span class="sxs-lookup"><span data-stu-id="0b2e5-157">INPUTS</span></span>

### <span data-ttu-id="0b2e5-158">System.object</span><span class="sxs-lookup"><span data-stu-id="0b2e5-158">System.String</span></span>

### <span data-ttu-id="0b2e5-159">PSBlueprintBase 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="0b2e5-159">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="0b2e5-160">System.object []</span><span class="sxs-lookup"><span data-stu-id="0b2e5-160">System.String[]</span></span>

### <span data-ttu-id="0b2e5-161">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="0b2e5-161">System.Collections.Hashtable</span></span>

## <span data-ttu-id="0b2e5-162">輸出</span><span class="sxs-lookup"><span data-stu-id="0b2e5-162">OUTPUTS</span></span>

### <span data-ttu-id="0b2e5-163">System.object</span><span class="sxs-lookup"><span data-stu-id="0b2e5-163">System.Object</span></span>
## <span data-ttu-id="0b2e5-164">筆記</span><span class="sxs-lookup"><span data-stu-id="0b2e5-164">NOTES</span></span>

## <span data-ttu-id="0b2e5-165">相關連結</span><span class="sxs-lookup"><span data-stu-id="0b2e5-165">RELATED LINKS</span></span>