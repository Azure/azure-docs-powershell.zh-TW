---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/new-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprintAssignment.md
ms.openlocfilehash: 43689de5ae2431db8bc523369700f32dba0206bd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93788665"
---
# <span data-ttu-id="acff5-101">New-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="acff5-101">New-AzBlueprintAssignment</span></span>

## <span data-ttu-id="acff5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="acff5-102">SYNOPSIS</span></span>
<span data-ttu-id="acff5-103">將藍圖定義指派給訂閱。</span><span class="sxs-lookup"><span data-stu-id="acff5-103">Assign a blueprint definition to a subscription.</span></span>

## <span data-ttu-id="acff5-104">句法</span><span class="sxs-lookup"><span data-stu-id="acff5-104">SYNTAX</span></span>

```
New-AzBlueprintAssignment -Name <String> -Blueprint <PSBlueprintBase> [-SubscriptionId <String[]>]
 -Location <String> [-ResourceGroupParameter <Hashtable>] [-Parameter <Hashtable>] [-SystemAssignedIdentity]
 [-UserAssignedIdentity <String>] [-Lock <PSLockMode>] [-SecureStringParameter <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="acff5-105">說明</span><span class="sxs-lookup"><span data-stu-id="acff5-105">DESCRIPTION</span></span>
<span data-ttu-id="acff5-106">將藍圖定義指派給訂閱。</span><span class="sxs-lookup"><span data-stu-id="acff5-106">Assign a blueprint definition to a subscription.</span></span>

## <span data-ttu-id="acff5-107">示例</span><span class="sxs-lookup"><span data-stu-id="acff5-107">EXAMPLES</span></span>

### <span data-ttu-id="acff5-108">範例1</span><span class="sxs-lookup"><span data-stu-id="acff5-108">Example 1</span></span>
```powershell
PS C:\> $rg = @{ResourceGroup=@{name='storage_rg';location='eastus'}}
PS C:\> $params = @{applytaganditsdefaultvalue_tagName="Department_Cost_Center"; applytaganditsdefaultvalue_tagValue="Contoso/RnD/Dev/986754"}
PS C:\> $blueprintObject =  Get-AzBlueprint -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myBlueprintName"
PS C:\> $secureString = @{keyVaultId='/subscriptions/00000000-1111-0000-1111-000000000000/rsourcegroups/myResourceGroup/providers/Microsoft.Keyvault/Vaults/myKeyVault';secretName='mySecret';secretVersion='1.0'}
PS C:\> New-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId "00000000-1111-0000-1111-000000000000" -Location "West US" -ResourceGroupParameter $rg -Parameter $params -SecureStringParameters $secureString

Name              : myAssignment
Id                : /subscriptions/00000000-1111-0000-1111-000000000000/providers/Microsoft.Blueprint/blueprintAssignments/myAssignment
Scope             : /subscriptions/00000000-1111-0000-1111-000000000000
LastModified      : 2019-01-08
LockMode          : None
ProvisioningState : Creating
Parameters        : {applytaganditsdefaultvalue_tagName, applytaganditsdefaultvalue_tagValue}
ResourceGroups    : ResourceGroup
```

<span data-ttu-id="acff5-109">`$blueprintObject`使用已定義的參數和資源群組字典，在指定的訂閱中建立藍圖定義的新藍圖指派。</span><span class="sxs-lookup"><span data-stu-id="acff5-109">Create a new blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription using the defined parameter and resource group dictionary.</span></span> <span data-ttu-id="acff5-110">使用系統指派的身分識別。</span><span class="sxs-lookup"><span data-stu-id="acff5-110">Uses system-assigned identity.</span></span> <span data-ttu-id="acff5-111">位置定義建立受管理身分識別的區域。</span><span class="sxs-lookup"><span data-stu-id="acff5-111">The location defines the region for creating the managed identity.</span></span>

### <span data-ttu-id="acff5-112">範例2</span><span class="sxs-lookup"><span data-stu-id="acff5-112">Example 2</span></span>
```powershell
PS C:\> New-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId 00000000-1111-0000-1111-000000000000 -Location "West US" -Parameter @{P1="v1"; P2="v2"} -Lock AllResourcesReadOnly
```

<span data-ttu-id="acff5-113">`$blueprintObject`使用已定義的參數和資源群組字典，並將資源鎖定設定為 **AllResources** ，以在指定的訂閱中建立藍圖定義的新藍圖指派。</span><span class="sxs-lookup"><span data-stu-id="acff5-113">Create a new blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription using the defined parameter and resource group dictionary and configuring resource locking to **AllResources**.</span></span> <span data-ttu-id="acff5-114">預設為使用系統指派的身分識別。</span><span class="sxs-lookup"><span data-stu-id="acff5-114">Defaults to using system-assigned identity.</span></span>  <span data-ttu-id="acff5-115">位置定義建立受管理身分識別的區域。</span><span class="sxs-lookup"><span data-stu-id="acff5-115">The location defines the region for creating the managed identity.</span></span>

### <span data-ttu-id="acff5-116">範例3</span><span class="sxs-lookup"><span data-stu-id="acff5-116">Example 3</span></span>
```powershell
PS C:\> New-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId 00000000-1111-0000-1111-000000000000 -Location "West US" -Parameter @{P1="v1"; P2="v2"} -UserAssignedIdentity "/subscriptions/00000000-1111-0000-1111-000000000000/resourceGroups/my-resource-group/providers/Microsoft.ManagedIdentity/userAssignedIdentities/my-user-defined-identity"
```

<span data-ttu-id="acff5-117">`$blueprintObject`使用已定義的參數和資源群組字典，在指定的訂閱中使用指定的使用者指派身分識別識別碼來建立藍圖定義的新藍圖指派。</span><span class="sxs-lookup"><span data-stu-id="acff5-117">Create a new blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription using the defined parameter and resource group dictionary using the specified user-assigned identity id.</span></span>

## <span data-ttu-id="acff5-118">參數</span><span class="sxs-lookup"><span data-stu-id="acff5-118">PARAMETERS</span></span>

### <span data-ttu-id="acff5-119">-藍圖</span><span class="sxs-lookup"><span data-stu-id="acff5-119">-Blueprint</span></span>
<span data-ttu-id="acff5-120">藍圖定義物件。</span><span class="sxs-lookup"><span data-stu-id="acff5-120">Blueprint definition object.</span></span>

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

### <span data-ttu-id="acff5-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acff5-121">-DefaultProfile</span></span>
<span data-ttu-id="acff5-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="acff5-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="acff5-123">-位置</span><span class="sxs-lookup"><span data-stu-id="acff5-123">-Location</span></span>
<span data-ttu-id="acff5-124">要在其中建立受管理身分識別的地區。</span><span class="sxs-lookup"><span data-stu-id="acff5-124">Region for managed identity to be created in.</span></span>
<span data-ttu-id="acff5-125">深入瞭解 aka.ms/blueprintmsi</span><span class="sxs-lookup"><span data-stu-id="acff5-125">Learn more at aka.ms/blueprintmsi</span></span>

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

### <span data-ttu-id="acff5-126">鎖</span><span class="sxs-lookup"><span data-stu-id="acff5-126">-Lock</span></span>
<span data-ttu-id="acff5-127">鎖定資源。</span><span class="sxs-lookup"><span data-stu-id="acff5-127">Lock resources.</span></span>
<span data-ttu-id="acff5-128">深入瞭解 aka.ms/blueprintlocks</span><span class="sxs-lookup"><span data-stu-id="acff5-128">Learn more at aka.ms/blueprintlocks</span></span>

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

### <span data-ttu-id="acff5-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="acff5-129">-Name</span></span>
<span data-ttu-id="acff5-130">藍圖作業名稱。</span><span class="sxs-lookup"><span data-stu-id="acff5-130">Blueprint assignment name.</span></span>

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

### <span data-ttu-id="acff5-131">-參數</span><span class="sxs-lookup"><span data-stu-id="acff5-131">-Parameter</span></span>
<span data-ttu-id="acff5-132">專案參數。</span><span class="sxs-lookup"><span data-stu-id="acff5-132">Artifact parameters.</span></span>

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

### <span data-ttu-id="acff5-133">-ResourceGroupParameter</span><span class="sxs-lookup"><span data-stu-id="acff5-133">-ResourceGroupParameter</span></span>
<span data-ttu-id="acff5-134">{{Fill ResourceGroupParameter 說明}}</span><span class="sxs-lookup"><span data-stu-id="acff5-134">{{Fill ResourceGroupParameter Description}}</span></span>

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

### <span data-ttu-id="acff5-135">-SecureStringParameter</span><span class="sxs-lookup"><span data-stu-id="acff5-135">-SecureStringParameter</span></span>
<span data-ttu-id="acff5-136">KeyVault 資源識別碼、名稱和版本的安全字串參數。</span><span class="sxs-lookup"><span data-stu-id="acff5-136">Secure string parameter for KeyVault resource id, name and version.</span></span>

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

### <span data-ttu-id="acff5-137">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="acff5-137">-SubscriptionId</span></span>
<span data-ttu-id="acff5-138">[訂閱識別碼] 可指派藍圖定義。</span><span class="sxs-lookup"><span data-stu-id="acff5-138">Subscription Id to assign the blueprint definition.</span></span>
<span data-ttu-id="acff5-139">可以是以逗號分隔的 subscriptionId 字串清單。</span><span class="sxs-lookup"><span data-stu-id="acff5-139">Can be a comma delimited list of subscriptionId strings.</span></span>

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

### <span data-ttu-id="acff5-140">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="acff5-140">-SystemAssignedIdentity</span></span>
<span data-ttu-id="acff5-141">系統指派身分識別 (MSI) 來部署該專案。</span><span class="sxs-lookup"><span data-stu-id="acff5-141">System assigned identity(MSI) to deploy the artifacts.</span></span>

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

### <span data-ttu-id="acff5-142">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="acff5-142">-UserAssignedIdentity</span></span>
<span data-ttu-id="acff5-143">使用者指派身分識別 (MSI) 來部署該專案。</span><span class="sxs-lookup"><span data-stu-id="acff5-143">User assigned identity(MSI) to deploy the artifacts.</span></span>

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

### <span data-ttu-id="acff5-144">-確認</span><span class="sxs-lookup"><span data-stu-id="acff5-144">-Confirm</span></span>
<span data-ttu-id="acff5-145">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="acff5-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="acff5-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="acff5-146">-WhatIf</span></span>
<span data-ttu-id="acff5-147">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="acff5-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="acff5-148">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="acff5-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="acff5-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acff5-149">CommonParameters</span></span>
<span data-ttu-id="acff5-150">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="acff5-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acff5-151">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="acff5-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acff5-152">輸入</span><span class="sxs-lookup"><span data-stu-id="acff5-152">INPUTS</span></span>

### <span data-ttu-id="acff5-153">System.object</span><span class="sxs-lookup"><span data-stu-id="acff5-153">System.String</span></span>

### <span data-ttu-id="acff5-154">PSBlueprintBase 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="acff5-154">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="acff5-155">System.object []</span><span class="sxs-lookup"><span data-stu-id="acff5-155">System.String[]</span></span>

### <span data-ttu-id="acff5-156">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="acff5-156">System.Collections.Hashtable</span></span>

## <span data-ttu-id="acff5-157">輸出</span><span class="sxs-lookup"><span data-stu-id="acff5-157">OUTPUTS</span></span>

### <span data-ttu-id="acff5-158">System.object</span><span class="sxs-lookup"><span data-stu-id="acff5-158">System.Object</span></span>
## <span data-ttu-id="acff5-159">筆記</span><span class="sxs-lookup"><span data-stu-id="acff5-159">NOTES</span></span>

## <span data-ttu-id="acff5-160">相關連結</span><span class="sxs-lookup"><span data-stu-id="acff5-160">RELATED LINKS</span></span>
