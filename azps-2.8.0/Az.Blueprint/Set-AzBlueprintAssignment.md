---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/set-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintAssignment.md
ms.openlocfilehash: df1d25f2d5362a81bd33b74bad223bbfb952daa7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93613570"
---
# <span data-ttu-id="6d676-101">Set-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="6d676-101">Set-AzBlueprintAssignment</span></span>

## <span data-ttu-id="6d676-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6d676-102">SYNOPSIS</span></span>
<span data-ttu-id="6d676-103">更新現有的藍圖作業。</span><span class="sxs-lookup"><span data-stu-id="6d676-103">Update an existing blueprint assignment.</span></span>

## <span data-ttu-id="6d676-104">句法</span><span class="sxs-lookup"><span data-stu-id="6d676-104">SYNTAX</span></span>

### <span data-ttu-id="6d676-105">UpdateBlueprintAssignment (預設) </span><span class="sxs-lookup"><span data-stu-id="6d676-105">UpdateBlueprintAssignment (Default)</span></span>
```
Set-AzBlueprintAssignment -Name <String> -Blueprint <PSBlueprintBase> -Location <String>
 [-SystemAssignedIdentity] [-UserAssignedIdentity <String>] [-Lock <PSLockMode>]
 [-SecureStringParameter <Hashtable>] [-ResourceGroupParameter <Hashtable>] [-Parameter <Hashtable>]
 [-SubscriptionId <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6d676-106">UpdateBlueprintAssignmentByFile</span><span class="sxs-lookup"><span data-stu-id="6d676-106">UpdateBlueprintAssignmentByFile</span></span>
```
Set-AzBlueprintAssignment -Name <String> -Blueprint <PSBlueprintBase> [-AssignmentFile <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6d676-107">說明</span><span class="sxs-lookup"><span data-stu-id="6d676-107">DESCRIPTION</span></span>
<span data-ttu-id="6d676-108">更新現有的藍圖作業。</span><span class="sxs-lookup"><span data-stu-id="6d676-108">Update an existing blueprint assignment.</span></span>

## <span data-ttu-id="6d676-109">示例</span><span class="sxs-lookup"><span data-stu-id="6d676-109">EXAMPLES</span></span>

### <span data-ttu-id="6d676-110">範例1</span><span class="sxs-lookup"><span data-stu-id="6d676-110">Example 1</span></span>
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

<span data-ttu-id="6d676-111">在指定的訂閱中，更新藍圖定義的現有藍圖指派 `$blueprintObject` ，並更新參數。</span><span class="sxs-lookup"><span data-stu-id="6d676-111">Update an existing blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription, updating the parameters.</span></span> <span data-ttu-id="6d676-112">使用系統指派的身分識別。</span><span class="sxs-lookup"><span data-stu-id="6d676-112">Uses system-assigned identity.</span></span> <span data-ttu-id="6d676-113">位置定義建立受管理身分識別的區域。</span><span class="sxs-lookup"><span data-stu-id="6d676-113">The location defines the region for creating the managed identity.</span></span>

### <span data-ttu-id="6d676-114">範例2</span><span class="sxs-lookup"><span data-stu-id="6d676-114">Example 2</span></span>
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

<span data-ttu-id="6d676-115">透過作業檔案更新現有的藍圖作業。</span><span class="sxs-lookup"><span data-stu-id="6d676-115">Update an existing blueprint assignment through an assignment file.</span></span> <span data-ttu-id="6d676-116">您可以在 [要求/回應] 範例中找到作業檔的格式，網址如下： https://github.com/Azure/azure-rest-api-specs/tree/master/specification/blueprint/resource-manager/Microsoft.Blueprint/preview/2018-11-01-preview/examples</span><span class="sxs-lookup"><span data-stu-id="6d676-116">The format of the assignment file can be found in the request/response samples at: https://github.com/Azure/azure-rest-api-specs/tree/master/specification/blueprint/resource-manager/Microsoft.Blueprint/preview/2018-11-01-preview/examples</span></span>

## <span data-ttu-id="6d676-117">參數</span><span class="sxs-lookup"><span data-stu-id="6d676-117">PARAMETERS</span></span>

### <span data-ttu-id="6d676-118">-藍圖</span><span class="sxs-lookup"><span data-stu-id="6d676-118">-Blueprint</span></span>
<span data-ttu-id="6d676-119">藍圖物件。</span><span class="sxs-lookup"><span data-stu-id="6d676-119">Blueprint object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6d676-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d676-120">-DefaultProfile</span></span>
<span data-ttu-id="6d676-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6d676-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d676-122">-位置</span><span class="sxs-lookup"><span data-stu-id="6d676-122">-Location</span></span>
<span data-ttu-id="6d676-123">要在其中建立受管理身分識別的地區。</span><span class="sxs-lookup"><span data-stu-id="6d676-123">Region for managed identity to be created in.</span></span>
<span data-ttu-id="6d676-124">深入瞭解 aka.ms/blueprintmsi</span><span class="sxs-lookup"><span data-stu-id="6d676-124">Learn more at aka.ms/blueprintmsi</span></span>

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

### <span data-ttu-id="6d676-125">鎖</span><span class="sxs-lookup"><span data-stu-id="6d676-125">-Lock</span></span>
<span data-ttu-id="6d676-126">鎖定資源。</span><span class="sxs-lookup"><span data-stu-id="6d676-126">Lock resources.</span></span>
<span data-ttu-id="6d676-127">深入瞭解 aka.ms/blueprintlocks</span><span class="sxs-lookup"><span data-stu-id="6d676-127">Learn more at aka.ms/blueprintlocks</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Blueprint.Models.PSLockMode]
Parameter Sets: (All)
Aliases:
Accepted values: None, AllResourcesReadOnly, AllResourcesDoNotDelete

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d676-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="6d676-128">-Name</span></span>
<span data-ttu-id="6d676-129">藍圖作業名稱。</span><span class="sxs-lookup"><span data-stu-id="6d676-129">Blueprint assignment name.</span></span>

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

### <span data-ttu-id="6d676-130">-參數</span><span class="sxs-lookup"><span data-stu-id="6d676-130">-Parameter</span></span>
<span data-ttu-id="6d676-131">專案參數。</span><span class="sxs-lookup"><span data-stu-id="6d676-131">Artifact parameter.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d676-132">-ResourceGroupParameter</span><span class="sxs-lookup"><span data-stu-id="6d676-132">-ResourceGroupParameter</span></span>
<span data-ttu-id="6d676-133">{{Fill ResourceGroupParameter 說明}}</span><span class="sxs-lookup"><span data-stu-id="6d676-133">{{Fill ResourceGroupParameter Description}}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d676-134">-SecureStringParameter</span><span class="sxs-lookup"><span data-stu-id="6d676-134">-SecureStringParameter</span></span>
<span data-ttu-id="6d676-135">KeyVault 資源識別碼、名稱和版本的安全字串參數。</span><span class="sxs-lookup"><span data-stu-id="6d676-135">Secure string parameter for KeyVault resource id, name and version.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d676-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6d676-136">-SubscriptionId</span></span>
<span data-ttu-id="6d676-137">[SubscriptionId] 可指派藍圖。</span><span class="sxs-lookup"><span data-stu-id="6d676-137">SubscriptionId to assign the Blueprint.</span></span>
<span data-ttu-id="6d676-138">可以是以逗號分隔的 subscriptionId 字串清單。</span><span class="sxs-lookup"><span data-stu-id="6d676-138">Can be a comma delimited list of subscriptionId strings.</span></span>

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

### <span data-ttu-id="6d676-139">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="6d676-139">-SystemAssignedIdentity</span></span>
<span data-ttu-id="6d676-140">系統指派身分識別 (MSI) 來部署該專案。</span><span class="sxs-lookup"><span data-stu-id="6d676-140">System assigned identity(MSI) to deploy the artifacts.</span></span>

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

### <span data-ttu-id="6d676-141">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="6d676-141">-UserAssignedIdentity</span></span>
<span data-ttu-id="6d676-142">使用者指派身分識別 (MSI) 來部署該專案。</span><span class="sxs-lookup"><span data-stu-id="6d676-142">User assigned identity(MSI) to deploy the artifacts.</span></span>

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

### <span data-ttu-id="6d676-143">-確認</span><span class="sxs-lookup"><span data-stu-id="6d676-143">-Confirm</span></span>
<span data-ttu-id="6d676-144">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6d676-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d676-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d676-145">-WhatIf</span></span>
<span data-ttu-id="6d676-146">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6d676-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d676-147">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6d676-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d676-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d676-148">CommonParameters</span></span>
<span data-ttu-id="6d676-149">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6d676-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d676-150">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6d676-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d676-151">輸入</span><span class="sxs-lookup"><span data-stu-id="6d676-151">INPUTS</span></span>

### <span data-ttu-id="6d676-152">System.object</span><span class="sxs-lookup"><span data-stu-id="6d676-152">System.String</span></span>

### <span data-ttu-id="6d676-153">PSBlueprintBase 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="6d676-153">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="6d676-154">System.object []</span><span class="sxs-lookup"><span data-stu-id="6d676-154">System.String[]</span></span>

### <span data-ttu-id="6d676-155">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="6d676-155">System.Collections.Hashtable</span></span>

## <span data-ttu-id="6d676-156">輸出</span><span class="sxs-lookup"><span data-stu-id="6d676-156">OUTPUTS</span></span>

### <span data-ttu-id="6d676-157">System.object</span><span class="sxs-lookup"><span data-stu-id="6d676-157">System.Object</span></span>
## <span data-ttu-id="6d676-158">筆記</span><span class="sxs-lookup"><span data-stu-id="6d676-158">NOTES</span></span>

## <span data-ttu-id="6d676-159">相關連結</span><span class="sxs-lookup"><span data-stu-id="6d676-159">RELATED LINKS</span></span>