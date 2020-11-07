---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/set-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintAssignment.md
ms.openlocfilehash: 795f1a7c4a002b7a8a141460b3b5e403ef8dc168
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93788669"
---
# <span data-ttu-id="e5d41-101">Set-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="e5d41-101">Set-AzBlueprintAssignment</span></span>

## <span data-ttu-id="e5d41-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e5d41-102">SYNOPSIS</span></span>
<span data-ttu-id="e5d41-103">更新現有的藍圖作業。</span><span class="sxs-lookup"><span data-stu-id="e5d41-103">Update an existing blueprint assignment.</span></span>

## <span data-ttu-id="e5d41-104">句法</span><span class="sxs-lookup"><span data-stu-id="e5d41-104">SYNTAX</span></span>

```
Set-AzBlueprintAssignment -Name <String> -Blueprint <PSBlueprintBase> [-SubscriptionId <String[]>]
 -Location <String> [-ResourceGroupParameter <Hashtable>] [-Parameter <Hashtable>] [-SystemAssignedIdentity]
 [-UserAssignedIdentity <String>] [-Lock <PSLockMode>] [-SecureStringParameter <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5d41-105">說明</span><span class="sxs-lookup"><span data-stu-id="e5d41-105">DESCRIPTION</span></span>
<span data-ttu-id="e5d41-106">更新現有的藍圖作業。</span><span class="sxs-lookup"><span data-stu-id="e5d41-106">Update an existing blueprint assignment.</span></span>

## <span data-ttu-id="e5d41-107">示例</span><span class="sxs-lookup"><span data-stu-id="e5d41-107">EXAMPLES</span></span>

### <span data-ttu-id="e5d41-108">範例1</span><span class="sxs-lookup"><span data-stu-id="e5d41-108">Example 1</span></span>
```powershell
PS C:\> $rg = @{ResourceGroup=@{name='storage_rg';location='eastus'}}
PS C:\> $params = @{applytaganditsdefaultvalue_tagName="Department_Cost_Center"; applytaganditsdefaultvalue_tagValue="Contoso/HR/Dev/0001"}
PS C:\> $blueprintObject =  Get-AzBlueprint -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myBlueprintName"
PS C:\> Set-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId "00000000-1111-0000-1111-000000000000" -Location "West US" -Parameter $params -ResourceGroupParameter $rg -SystemAssignedIdentity

Name              : myAssignment
Id                : /subscriptions/00000000-1111-0000-1111-000000000000/providers/Microsoft.Blueprint/blueprintAssignments/Assignment-PS-BlueprintDefinition
Scope             : /subscriptions/00000000-1111-0000-1111-000000000000
LastModified      : 2019-01-08
LockMode          : None
ProvisioningState : Creating
Parameters        : {applytaganditsdefaultvalue_tagName, applytaganditsdefaultvalue_tagValue}
ResourceGroups    : ResourceGroup
```

<span data-ttu-id="e5d41-109">在指定的訂閱中，更新藍圖定義的現有藍圖指派 `$blueprintObject` ，並更新參數。</span><span class="sxs-lookup"><span data-stu-id="e5d41-109">Update an existing blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription, updating the parameters.</span></span> <span data-ttu-id="e5d41-110">使用系統指派的身分識別。</span><span class="sxs-lookup"><span data-stu-id="e5d41-110">Uses system-assigned identity.</span></span> <span data-ttu-id="e5d41-111">位置定義建立受管理身分識別的區域。</span><span class="sxs-lookup"><span data-stu-id="e5d41-111">The location defines the region for creating the managed identity.</span></span>

## <span data-ttu-id="e5d41-112">參數</span><span class="sxs-lookup"><span data-stu-id="e5d41-112">PARAMETERS</span></span>

### <span data-ttu-id="e5d41-113">-藍圖</span><span class="sxs-lookup"><span data-stu-id="e5d41-113">-Blueprint</span></span>
<span data-ttu-id="e5d41-114">藍圖物件。</span><span class="sxs-lookup"><span data-stu-id="e5d41-114">Blueprint object.</span></span>

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

### <span data-ttu-id="e5d41-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5d41-115">-DefaultProfile</span></span>
<span data-ttu-id="e5d41-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e5d41-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5d41-117">-位置</span><span class="sxs-lookup"><span data-stu-id="e5d41-117">-Location</span></span>
<span data-ttu-id="e5d41-118">要在其中建立受管理身分識別的地區。</span><span class="sxs-lookup"><span data-stu-id="e5d41-118">Region for managed identity to be created in.</span></span>
<span data-ttu-id="e5d41-119">深入瞭解 aka.ms/blueprintmsi</span><span class="sxs-lookup"><span data-stu-id="e5d41-119">Learn more at aka.ms/blueprintmsi</span></span>

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

### <span data-ttu-id="e5d41-120">鎖</span><span class="sxs-lookup"><span data-stu-id="e5d41-120">-Lock</span></span>
<span data-ttu-id="e5d41-121">鎖定資源。</span><span class="sxs-lookup"><span data-stu-id="e5d41-121">Lock resources.</span></span>
<span data-ttu-id="e5d41-122">深入瞭解 aka.ms/blueprintlocks</span><span class="sxs-lookup"><span data-stu-id="e5d41-122">Learn more at aka.ms/blueprintlocks</span></span>

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

### <span data-ttu-id="e5d41-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="e5d41-123">-Name</span></span>
<span data-ttu-id="e5d41-124">藍圖作業名稱。</span><span class="sxs-lookup"><span data-stu-id="e5d41-124">Blueprint assignment name.</span></span>

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

### <span data-ttu-id="e5d41-125">-參數</span><span class="sxs-lookup"><span data-stu-id="e5d41-125">-Parameter</span></span>
<span data-ttu-id="e5d41-126">專案參數。</span><span class="sxs-lookup"><span data-stu-id="e5d41-126">Artifact parameter.</span></span>

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

### <span data-ttu-id="e5d41-127">-ResourceGroupParameter</span><span class="sxs-lookup"><span data-stu-id="e5d41-127">-ResourceGroupParameter</span></span>
<span data-ttu-id="e5d41-128">{{Fill ResourceGroupParameter 說明}}</span><span class="sxs-lookup"><span data-stu-id="e5d41-128">{{Fill ResourceGroupParameter Description}}</span></span>

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

### <span data-ttu-id="e5d41-129">-SecureStringParameter</span><span class="sxs-lookup"><span data-stu-id="e5d41-129">-SecureStringParameter</span></span>
<span data-ttu-id="e5d41-130">KeyVault 資源識別碼、名稱和版本的安全字串參數。</span><span class="sxs-lookup"><span data-stu-id="e5d41-130">Secure string parameter for KeyVault resource id, name and version.</span></span>

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

### <span data-ttu-id="e5d41-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e5d41-131">-SubscriptionId</span></span>
<span data-ttu-id="e5d41-132">[SubscriptionId] 可指派藍圖。</span><span class="sxs-lookup"><span data-stu-id="e5d41-132">SubscriptionId to assign the Blueprint.</span></span>
<span data-ttu-id="e5d41-133">可以是以逗號分隔的 subscriptionId 字串清單。</span><span class="sxs-lookup"><span data-stu-id="e5d41-133">Can be a comma delimited list of subscriptionId strings.</span></span>

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

### <span data-ttu-id="e5d41-134">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="e5d41-134">-SystemAssignedIdentity</span></span>
<span data-ttu-id="e5d41-135">系統指派身分識別 (MSI) 來部署該專案。</span><span class="sxs-lookup"><span data-stu-id="e5d41-135">System assigned identity(MSI) to deploy the artifacts.</span></span>

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

### <span data-ttu-id="e5d41-136">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="e5d41-136">-UserAssignedIdentity</span></span>
<span data-ttu-id="e5d41-137">使用者指派身分識別 (MSI) 來部署該專案。</span><span class="sxs-lookup"><span data-stu-id="e5d41-137">User assigned identity(MSI) to deploy the artifacts.</span></span>

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

### <span data-ttu-id="e5d41-138">-確認</span><span class="sxs-lookup"><span data-stu-id="e5d41-138">-Confirm</span></span>
<span data-ttu-id="e5d41-139">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e5d41-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5d41-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5d41-140">-WhatIf</span></span>
<span data-ttu-id="e5d41-141">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e5d41-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5d41-142">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e5d41-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5d41-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5d41-143">CommonParameters</span></span>
<span data-ttu-id="e5d41-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e5d41-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5d41-145">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e5d41-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5d41-146">輸入</span><span class="sxs-lookup"><span data-stu-id="e5d41-146">INPUTS</span></span>

### <span data-ttu-id="e5d41-147">System.object</span><span class="sxs-lookup"><span data-stu-id="e5d41-147">System.String</span></span>

### <span data-ttu-id="e5d41-148">PSBlueprintBase 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="e5d41-148">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="e5d41-149">System.object []</span><span class="sxs-lookup"><span data-stu-id="e5d41-149">System.String[]</span></span>

### <span data-ttu-id="e5d41-150">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="e5d41-150">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e5d41-151">輸出</span><span class="sxs-lookup"><span data-stu-id="e5d41-151">OUTPUTS</span></span>

### <span data-ttu-id="e5d41-152">System.object</span><span class="sxs-lookup"><span data-stu-id="e5d41-152">System.Object</span></span>
## <span data-ttu-id="e5d41-153">筆記</span><span class="sxs-lookup"><span data-stu-id="e5d41-153">NOTES</span></span>

## <span data-ttu-id="e5d41-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="e5d41-154">RELATED LINKS</span></span>
