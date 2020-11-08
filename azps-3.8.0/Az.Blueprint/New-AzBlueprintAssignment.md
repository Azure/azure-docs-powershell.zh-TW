---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/new-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprintAssignment.md
ms.openlocfilehash: 72c57f8310aaffdbe3c4afa38564c10132539749
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93956578"
---
# <span data-ttu-id="a750c-101">New-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="a750c-101">New-AzBlueprintAssignment</span></span>

## <span data-ttu-id="a750c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a750c-102">SYNOPSIS</span></span>
<span data-ttu-id="a750c-103">將藍圖定義指派給訂閱。</span><span class="sxs-lookup"><span data-stu-id="a750c-103">Assign a blueprint definition to a subscription.</span></span>

## <span data-ttu-id="a750c-104">句法</span><span class="sxs-lookup"><span data-stu-id="a750c-104">SYNTAX</span></span>

### <span data-ttu-id="a750c-105">CreateBlueprintAssignment (預設) </span><span class="sxs-lookup"><span data-stu-id="a750c-105">CreateBlueprintAssignment (Default)</span></span>
```
New-AzBlueprintAssignment -Name <String> -Blueprint <PSBlueprintBase> -Location <String>
 [-SystemAssignedIdentity] [-UserAssignedIdentity <String>] [-Lock <PSLockMode>]
 [-SecureStringParameter <Hashtable>] [-ResourceGroupParameter <Hashtable>] [-Parameter <Hashtable>]
 [-SubscriptionId <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a750c-106">CreateBlueprintAssignmentByFile</span><span class="sxs-lookup"><span data-stu-id="a750c-106">CreateBlueprintAssignmentByFile</span></span>
```
New-AzBlueprintAssignment -Name <String> -Blueprint <PSBlueprintBase> [-AssignmentFile <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a750c-107">說明</span><span class="sxs-lookup"><span data-stu-id="a750c-107">DESCRIPTION</span></span>
<span data-ttu-id="a750c-108">將藍圖定義指派給訂閱。</span><span class="sxs-lookup"><span data-stu-id="a750c-108">Assign a blueprint definition to a subscription.</span></span>

## <span data-ttu-id="a750c-109">示例</span><span class="sxs-lookup"><span data-stu-id="a750c-109">EXAMPLES</span></span>

### <span data-ttu-id="a750c-110">範例1</span><span class="sxs-lookup"><span data-stu-id="a750c-110">Example 1</span></span>
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

<span data-ttu-id="a750c-111">`$blueprintObject`使用已定義的參數和資源群組字典，在指定的訂閱中建立藍圖定義的新藍圖指派。</span><span class="sxs-lookup"><span data-stu-id="a750c-111">Create a new blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription using the defined parameter and resource group dictionary.</span></span> <span data-ttu-id="a750c-112">使用系統指派的身分識別。</span><span class="sxs-lookup"><span data-stu-id="a750c-112">Uses system-assigned identity.</span></span> <span data-ttu-id="a750c-113">位置定義建立受管理身分識別的區域。</span><span class="sxs-lookup"><span data-stu-id="a750c-113">The location defines the region for creating the managed identity.</span></span>

### <span data-ttu-id="a750c-114">範例2</span><span class="sxs-lookup"><span data-stu-id="a750c-114">Example 2</span></span>
```powershell
PS C:\> New-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId 00000000-1111-0000-1111-000000000000 -Location "West US" -Parameter @{P1="v1"; P2="v2"} -Lock AllResourcesReadOnly
```

<span data-ttu-id="a750c-115">`$blueprintObject`使用已定義的參數和資源群組字典，並將資源鎖定設定為 **AllResources** ，以在指定的訂閱中建立藍圖定義的新藍圖指派。</span><span class="sxs-lookup"><span data-stu-id="a750c-115">Create a new blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription using the defined parameter and resource group dictionary and configuring resource locking to **AllResources**.</span></span> <span data-ttu-id="a750c-116">預設為使用系統指派的身分識別。</span><span class="sxs-lookup"><span data-stu-id="a750c-116">Defaults to using system-assigned identity.</span></span>  <span data-ttu-id="a750c-117">位置定義建立受管理身分識別的區域。</span><span class="sxs-lookup"><span data-stu-id="a750c-117">The location defines the region for creating the managed identity.</span></span>

### <span data-ttu-id="a750c-118">範例3</span><span class="sxs-lookup"><span data-stu-id="a750c-118">Example 3</span></span>
```powershell
PS C:\> New-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId 00000000-1111-0000-1111-000000000000 -Location "West US" -Parameter @{P1="v1"; P2="v2"} -UserAssignedIdentity "/subscriptions/00000000-1111-0000-1111-000000000000/resourceGroups/my-resource-group/providers/Microsoft.ManagedIdentity/userAssignedIdentities/my-user-defined-identity"
```

<span data-ttu-id="a750c-119">`$blueprintObject`使用已定義的參數和資源群組字典，在指定的訂閱中使用指定的使用者指派身分識別識別碼來建立藍圖定義的新藍圖指派。</span><span class="sxs-lookup"><span data-stu-id="a750c-119">Create a new blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription using the defined parameter and resource group dictionary using the specified user-assigned identity id.</span></span>

### <span data-ttu-id="a750c-120">範例4</span><span class="sxs-lookup"><span data-stu-id="a750c-120">Example 4</span></span>
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

<span data-ttu-id="a750c-121">透過作業檔案建立藍圖作業。</span><span class="sxs-lookup"><span data-stu-id="a750c-121">Create a blueprint assignment through an assignment file.</span></span> <span data-ttu-id="a750c-122">您可以在 [要求/回應] 範例中找到作業檔的格式，網址如下： https://github.com/Azure/azure-rest-api-specs/tree/master/specification/blueprint/resource-manager/Microsoft.Blueprint/preview/2018-11-01-preview/examples</span><span class="sxs-lookup"><span data-stu-id="a750c-122">The format of the assignment file can be found in the request/response samples at: https://github.com/Azure/azure-rest-api-specs/tree/master/specification/blueprint/resource-manager/Microsoft.Blueprint/preview/2018-11-01-preview/examples</span></span>

## <span data-ttu-id="a750c-123">參數</span><span class="sxs-lookup"><span data-stu-id="a750c-123">PARAMETERS</span></span>

### <span data-ttu-id="a750c-124">-藍圖</span><span class="sxs-lookup"><span data-stu-id="a750c-124">-Blueprint</span></span>
<span data-ttu-id="a750c-125">藍圖定義物件。</span><span class="sxs-lookup"><span data-stu-id="a750c-125">Blueprint definition object.</span></span>

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

### <span data-ttu-id="a750c-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a750c-126">-DefaultProfile</span></span>
<span data-ttu-id="a750c-127">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a750c-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a750c-128">-位置</span><span class="sxs-lookup"><span data-stu-id="a750c-128">-Location</span></span>
<span data-ttu-id="a750c-129">要在其中建立受管理身分識別的地區。</span><span class="sxs-lookup"><span data-stu-id="a750c-129">Region for managed identity to be created in.</span></span>
<span data-ttu-id="a750c-130">深入瞭解 aka.ms/blueprintmsi</span><span class="sxs-lookup"><span data-stu-id="a750c-130">Learn more at aka.ms/blueprintmsi</span></span>

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

### <span data-ttu-id="a750c-131">鎖</span><span class="sxs-lookup"><span data-stu-id="a750c-131">-Lock</span></span>
<span data-ttu-id="a750c-132">鎖定資源。</span><span class="sxs-lookup"><span data-stu-id="a750c-132">Lock resources.</span></span>
<span data-ttu-id="a750c-133">深入瞭解 aka.ms/blueprintlocks</span><span class="sxs-lookup"><span data-stu-id="a750c-133">Learn more at aka.ms/blueprintlocks</span></span>

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

### <span data-ttu-id="a750c-134">-名稱</span><span class="sxs-lookup"><span data-stu-id="a750c-134">-Name</span></span>
<span data-ttu-id="a750c-135">藍圖作業名稱。</span><span class="sxs-lookup"><span data-stu-id="a750c-135">Blueprint assignment name.</span></span>

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

### <span data-ttu-id="a750c-136">-參數</span><span class="sxs-lookup"><span data-stu-id="a750c-136">-Parameter</span></span>
<span data-ttu-id="a750c-137">專案參數。</span><span class="sxs-lookup"><span data-stu-id="a750c-137">Artifact parameters.</span></span>

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

### <span data-ttu-id="a750c-138">-ResourceGroupParameter</span><span class="sxs-lookup"><span data-stu-id="a750c-138">-ResourceGroupParameter</span></span>
<span data-ttu-id="a750c-139">{{Fill ResourceGroupParameter 說明}}</span><span class="sxs-lookup"><span data-stu-id="a750c-139">{{Fill ResourceGroupParameter Description}}</span></span>

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

### <span data-ttu-id="a750c-140">-SecureStringParameter</span><span class="sxs-lookup"><span data-stu-id="a750c-140">-SecureStringParameter</span></span>
<span data-ttu-id="a750c-141">KeyVault 資源識別碼、名稱和版本的安全字串參數。</span><span class="sxs-lookup"><span data-stu-id="a750c-141">Secure string parameter for KeyVault resource id, name and version.</span></span>

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

### <span data-ttu-id="a750c-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a750c-142">-SubscriptionId</span></span>
<span data-ttu-id="a750c-143">[訂閱識別碼] 可指派藍圖定義。</span><span class="sxs-lookup"><span data-stu-id="a750c-143">Subscription Id to assign the blueprint definition.</span></span>
<span data-ttu-id="a750c-144">可以是以逗號分隔的 subscriptionId 字串清單。</span><span class="sxs-lookup"><span data-stu-id="a750c-144">Can be a comma delimited list of subscriptionId strings.</span></span>

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

### <span data-ttu-id="a750c-145">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="a750c-145">-SystemAssignedIdentity</span></span>
<span data-ttu-id="a750c-146">系統指派身分識別 (MSI) 來部署該專案。</span><span class="sxs-lookup"><span data-stu-id="a750c-146">System assigned identity(MSI) to deploy the artifacts.</span></span>

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

### <span data-ttu-id="a750c-147">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="a750c-147">-UserAssignedIdentity</span></span>
<span data-ttu-id="a750c-148">使用者指派身分識別 (MSI) 來部署該專案。</span><span class="sxs-lookup"><span data-stu-id="a750c-148">User assigned identity(MSI) to deploy the artifacts.</span></span>

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

### <span data-ttu-id="a750c-149">-確認</span><span class="sxs-lookup"><span data-stu-id="a750c-149">-Confirm</span></span>
<span data-ttu-id="a750c-150">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a750c-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a750c-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a750c-151">-WhatIf</span></span>
<span data-ttu-id="a750c-152">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a750c-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a750c-153">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a750c-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a750c-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a750c-154">CommonParameters</span></span>
<span data-ttu-id="a750c-155">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a750c-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a750c-156">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a750c-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a750c-157">輸入</span><span class="sxs-lookup"><span data-stu-id="a750c-157">INPUTS</span></span>

### <span data-ttu-id="a750c-158">System.object</span><span class="sxs-lookup"><span data-stu-id="a750c-158">System.String</span></span>

### <span data-ttu-id="a750c-159">PSBlueprintBase 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="a750c-159">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="a750c-160">System.object []</span><span class="sxs-lookup"><span data-stu-id="a750c-160">System.String[]</span></span>

### <span data-ttu-id="a750c-161">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="a750c-161">System.Collections.Hashtable</span></span>

## <span data-ttu-id="a750c-162">輸出</span><span class="sxs-lookup"><span data-stu-id="a750c-162">OUTPUTS</span></span>

### <span data-ttu-id="a750c-163">System.object</span><span class="sxs-lookup"><span data-stu-id="a750c-163">System.Object</span></span>
## <span data-ttu-id="a750c-164">筆記</span><span class="sxs-lookup"><span data-stu-id="a750c-164">NOTES</span></span>

## <span data-ttu-id="a750c-165">相關連結</span><span class="sxs-lookup"><span data-stu-id="a750c-165">RELATED LINKS</span></span>