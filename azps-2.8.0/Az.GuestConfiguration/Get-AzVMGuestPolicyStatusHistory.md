---
external help file: Microsoft.Azure.PowerShell.Cmdlets.GuestConfiguration.dll-Help.xml
Module Name: Az.GuestConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.guestconfiguration/get-azvmguestpolicystatushistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatusHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatusHistory.md
ms.openlocfilehash: 2e2474b784d66c3c3c34bc9ea9abc2b0959ea500
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93612331"
---
# <span data-ttu-id="99d77-101">Get-AzVMGuestPolicyStatusHistory</span><span class="sxs-lookup"><span data-stu-id="99d77-101">Get-AzVMGuestPolicyStatusHistory</span></span>

## <span data-ttu-id="99d77-102">摘要</span><span class="sxs-lookup"><span data-stu-id="99d77-102">SYNOPSIS</span></span>
<span data-ttu-id="99d77-103">取得指派給 VM 之「來賓設定」類型之計畫的來賓設定原則合規性狀態歷程記錄。</span><span class="sxs-lookup"><span data-stu-id="99d77-103">Gets guest configuration policy compliance status history for an initiative of type "Guest Configuration" that is assigned to a VM.</span></span>
<span data-ttu-id="99d77-104">方案是「倡議」定義類型的原則。</span><span class="sxs-lookup"><span data-stu-id="99d77-104">An initiative is a policy of definition type "Initiative".</span></span>

## <span data-ttu-id="99d77-105">句法</span><span class="sxs-lookup"><span data-stu-id="99d77-105">SYNTAX</span></span>

### <span data-ttu-id="99d77-106">InitiativeNameScope (預設) </span><span class="sxs-lookup"><span data-stu-id="99d77-106">InitiativeNameScope (Default)</span></span>
```
Get-AzVMGuestPolicyStatusHistory [-ResourceGroupName] <String> [-VMName] <String> [-InitiativeName] <String>
 [-ShowOnlyChange] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="99d77-107">InitiativeIdScope</span><span class="sxs-lookup"><span data-stu-id="99d77-107">InitiativeIdScope</span></span>
```
Get-AzVMGuestPolicyStatusHistory [-ResourceGroupName] <String> [-VMName] <String> [[-InitiativeId] <String>]
 [-ShowOnlyChange] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="99d77-108">說明</span><span class="sxs-lookup"><span data-stu-id="99d77-108">DESCRIPTION</span></span>
<span data-ttu-id="99d77-109">Get-AzVMGuestPolicyStatusHistory Cmdlet 會取得指派給 VM 之「來賓設定」類型之計畫的來賓設定原則符合性狀態歷程記錄。</span><span class="sxs-lookup"><span data-stu-id="99d77-109">The Get-AzVMGuestPolicyStatusHistory cmdlet gets compliance status history of guest configuration policies for an initiative of type "Guest Configuration" that is assigned to a VM.</span></span>
<span data-ttu-id="99d77-110">方案是「倡議」定義類型的原則。</span><span class="sxs-lookup"><span data-stu-id="99d77-110">An initiative is a policy of definition type "Initiative".</span></span>
<span data-ttu-id="99d77-111">使用 Get-AzVMGuestPolicyStatus Cmdlet，以使用可在 Get-AzVMGuestPolicyStatusHistory Cmdlet 的輸出中找到的 ReportId，以取得單一合規性狀態的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="99d77-111">Use Get-AzVMGuestPolicyStatus cmdlet to get details of a single compliance status using ReportId that can be found in output of Get-AzVMGuestPolicyStatusHistory cmdlet.</span></span>

## <span data-ttu-id="99d77-112">示例</span><span class="sxs-lookup"><span data-stu-id="99d77-112">EXAMPLES</span></span>

### <span data-ttu-id="99d77-113">範例1</span><span class="sxs-lookup"><span data-stu-id="99d77-113">Example 1</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeId "/providers/Microsoft.Authorization/policySetDefinitions/3fa7cbf5-c0a4-4a59-85a5-cca4d996d5af" -ShowOnlyChange
```

<span data-ttu-id="99d77-114">根據倡議 Id 取得合規性狀態歷程記錄。 ShowOnlyChange 開關只會顯示歷史狀態變更。</span><span class="sxs-lookup"><span data-stu-id="99d77-114">Gets compliance status history by initiative Id. ShowOnlyChange switch shows only historical status changes.</span></span>
<span data-ttu-id="99d77-115">略過在兩個相容性檢查之間沒有變更的狀態。</span><span class="sxs-lookup"><span data-stu-id="99d77-115">Skips statuses that have not changed between two compliance checks.</span></span>

### <span data-ttu-id="99d77-116">範例2</span><span class="sxs-lookup"><span data-stu-id="99d77-116">Example 2</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeName "b5a822e0-ba98-4e54-9278-5d9833aa9b17" -ShowOnlyChange
```

<span data-ttu-id="99d77-117">依計畫名稱取得合規性狀態歷程記錄。</span><span class="sxs-lookup"><span data-stu-id="99d77-117">Gets compliance status history by initiative name.</span></span>
<span data-ttu-id="99d77-118">ShowOnlyChange 開關只會顯示歷史狀態變更。</span><span class="sxs-lookup"><span data-stu-id="99d77-118">ShowOnlyChange switch shows only historical status changes.</span></span>
<span data-ttu-id="99d77-119">略過在兩個相容性檢查之間沒有變更的狀態。</span><span class="sxs-lookup"><span data-stu-id="99d77-119">Skips statuses that have not changed between two compliance checks.</span></span>

### <span data-ttu-id="99d77-120">範例3</span><span class="sxs-lookup"><span data-stu-id="99d77-120">Example 3</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -ShowOnlyChange
```

<span data-ttu-id="99d77-121">取得指派給 VM 之所有來賓設定原則的合規性狀態歷程記錄。</span><span class="sxs-lookup"><span data-stu-id="99d77-121">Gets compliance status history for all guest configuration policies assigned to the VM.</span></span>
<span data-ttu-id="99d77-122">ShowOnlyChange 開關只會顯示歷史狀態變更。</span><span class="sxs-lookup"><span data-stu-id="99d77-122">ShowOnlyChange switch shows only historical status changes.</span></span>
<span data-ttu-id="99d77-123">略過在兩個相容性檢查之間沒有變更的狀態。</span><span class="sxs-lookup"><span data-stu-id="99d77-123">Skips statuses that have not changed between two compliance checks.</span></span>

### <span data-ttu-id="99d77-124">範例4</span><span class="sxs-lookup"><span data-stu-id="99d77-124">Example 4</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeId "/providers/Microsoft.Authorization/policySetDefinitions/3fa7cbf5-c0a4-4a59-85a5-cca4d996d5af"
```

<span data-ttu-id="99d77-125">依計畫識別碼取得合規性狀態歷程記錄。</span><span class="sxs-lookup"><span data-stu-id="99d77-125">Gets compliance status history by initiative Id.</span></span>

### <span data-ttu-id="99d77-126">範例5</span><span class="sxs-lookup"><span data-stu-id="99d77-126">Example 5</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeName "b5a822e0-ba98-4e54-9278-5d9833aa9b17"
```

<span data-ttu-id="99d77-127">依計畫名稱取得合規性狀態歷程記錄。</span><span class="sxs-lookup"><span data-stu-id="99d77-127">Gets compliance status history by initiative name.</span></span>

### <span data-ttu-id="99d77-128">範例6</span><span class="sxs-lookup"><span data-stu-id="99d77-128">Example 6</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName"
```
<span data-ttu-id="99d77-129">取得指派給 VM 之所有來賓設定原則的合規性狀態歷程記錄。</span><span class="sxs-lookup"><span data-stu-id="99d77-129">Gets compliance status history for all guest configuration policies assigned to the VM.</span></span>

### <span data-ttu-id="99d77-130">範例7</span><span class="sxs-lookup"><span data-stu-id="99d77-130">Example 7</span></span>
```powershell
PS C:\>$x = Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName"
PS C:\>$x[10].ReportId
/subscriptions/4e6c6ed2-0bf6-41d7-9d21-a452c2cc7920/resourceGroups/MyResourceGroupName/providers/Microsoft.Compute/virtualMachines/MyVMName/providers/Microsoft.GuestConfiguration/guestConfigurationAssignments/MaximumPasswordAge/reports/c271f845-2c0a-4456-a441-e48fc332d0ac
PS C:\> Get-AzVMGuestPolicyStatus -ReportId $x[10].ReportId
```

<span data-ttu-id="99d77-131">依 ReportId 取得來賓設定原則狀態。</span><span class="sxs-lookup"><span data-stu-id="99d77-131">Get guest configuration policy status by ReportId.</span></span>
<span data-ttu-id="99d77-132">ReportId 是 ReportId 屬性，可在取得 AzVMGuestPolicyStatusHistory 的結果中找到。</span><span class="sxs-lookup"><span data-stu-id="99d77-132">The ReportId is the ReportId property that can be found in the results of Get-AzVMGuestPolicyStatusHistory.</span></span> <span data-ttu-id="99d77-133"> (請參閱其他範例) </span><span class="sxs-lookup"><span data-stu-id="99d77-133">(please refer other examples)</span></span>

## <span data-ttu-id="99d77-134">參數</span><span class="sxs-lookup"><span data-stu-id="99d77-134">PARAMETERS</span></span>

### <span data-ttu-id="99d77-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99d77-135">-DefaultProfile</span></span>
<span data-ttu-id="99d77-136">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="99d77-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="99d77-137">-InitiativeId</span><span class="sxs-lookup"><span data-stu-id="99d77-137">-InitiativeId</span></span>
<span data-ttu-id="99d77-138">定義類型為 [倡議] 或 [類別 is 來賓設定] 之原則的定義識別碼</span><span class="sxs-lookup"><span data-stu-id="99d77-138">Definition Id of a policy where definition type is Initiative and category is Guest Configuration</span></span>

```yaml
Type: System.String
Parameter Sets: InitiativeIdScope
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99d77-139">-InitiativeName</span><span class="sxs-lookup"><span data-stu-id="99d77-139">-InitiativeName</span></span>
<span data-ttu-id="99d77-140">定義類型為 [倡議]，類別為 [來賓設定] 的原則名稱</span><span class="sxs-lookup"><span data-stu-id="99d77-140">Name of a policy where definition type is Initiative and category is Guest Configuration</span></span>

```yaml
Type: System.String
Parameter Sets: InitiativeNameScope
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99d77-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99d77-141">-ResourceGroupName</span></span>
<span data-ttu-id="99d77-142">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="99d77-142">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99d77-143">-ShowOnlyChange</span><span class="sxs-lookup"><span data-stu-id="99d77-143">-ShowOnlyChange</span></span>
<span data-ttu-id="99d77-144">僅顯示來賓設定原則的歷史狀態變更。</span><span class="sxs-lookup"><span data-stu-id="99d77-144">Shows historical status changes only for guest configuration policies.</span></span>
<span data-ttu-id="99d77-145">略過在兩個合規性狀態審核執行之間沒有變更的狀態。</span><span class="sxs-lookup"><span data-stu-id="99d77-145">Skips statuses that have not changed between two compliance status audit runs.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99d77-146">-VMName</span><span class="sxs-lookup"><span data-stu-id="99d77-146">-VMName</span></span>
<span data-ttu-id="99d77-147">VM 名稱。</span><span class="sxs-lookup"><span data-stu-id="99d77-147">VM name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99d77-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99d77-148">CommonParameters</span></span>
<span data-ttu-id="99d77-149">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="99d77-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99d77-150">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="99d77-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99d77-151">輸入</span><span class="sxs-lookup"><span data-stu-id="99d77-151">INPUTS</span></span>

### <span data-ttu-id="99d77-152">所有</span><span class="sxs-lookup"><span data-stu-id="99d77-152">None</span></span>
## <span data-ttu-id="99d77-153">輸出</span><span class="sxs-lookup"><span data-stu-id="99d77-153">OUTPUTS</span></span>

### <span data-ttu-id="99d77-154">PolicyStatus 中的 GuestConfiguration。</span><span class="sxs-lookup"><span data-stu-id="99d77-154">Microsoft.Azure.Commands.GuestConfiguration.Models.PolicyStatus</span></span>
## <span data-ttu-id="99d77-155">筆記</span><span class="sxs-lookup"><span data-stu-id="99d77-155">NOTES</span></span>

## <span data-ttu-id="99d77-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="99d77-156">RELATED LINKS</span></span>
