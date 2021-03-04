---
external help file: Microsoft.Azure.PowerShell.Cmdlets.GuestConfiguration.dll-Help.xml
Module Name: Az.GuestConfiguration
online version: https://docs.microsoft.com/powershell/module/az.guestconfiguration/get-azvmguestpolicystatushistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatusHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatusHistory.md
ms.openlocfilehash: 9161b3c9c55c1014b64419a3644bf7ec80af8648
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911681"
---
# <span data-ttu-id="ebc8d-101">Get-AzVMGuestPolicyStatusHistory</span><span class="sxs-lookup"><span data-stu-id="ebc8d-101">Get-AzVMGuestPolicyStatusHistory</span></span>

## <span data-ttu-id="ebc8d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ebc8d-102">SYNOPSIS</span></span>
<span data-ttu-id="ebc8d-103">針對指派給 VM 的「來賓群組原則」類型之計畫，獲得來賓群組原則合規性狀態歷程記錄。</span><span class="sxs-lookup"><span data-stu-id="ebc8d-103">Gets guest configuration policy compliance status history for an initiative of type "Guest Configuration" that is assigned to a VM.</span></span>
<span data-ttu-id="ebc8d-104">計畫是定義類型「計畫」的一項政策。</span><span class="sxs-lookup"><span data-stu-id="ebc8d-104">An initiative is a policy of definition type "Initiative".</span></span>

## <span data-ttu-id="ebc8d-105">語法</span><span class="sxs-lookup"><span data-stu-id="ebc8d-105">SYNTAX</span></span>

### <span data-ttu-id="ebc8d-106">InitiativeNameScope (預設) </span><span class="sxs-lookup"><span data-stu-id="ebc8d-106">InitiativeNameScope (Default)</span></span>
```
Get-AzVMGuestPolicyStatusHistory [-ResourceGroupName] <String> [-VMName] <String> [-InitiativeName] <String>
 [-ShowOnlyChange] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ebc8d-107">InitiativeIdScope</span><span class="sxs-lookup"><span data-stu-id="ebc8d-107">InitiativeIdScope</span></span>
```
Get-AzVMGuestPolicyStatusHistory [-ResourceGroupName] <String> [-VMName] <String> [[-InitiativeId] <String>]
 [-ShowOnlyChange] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ebc8d-108">描述</span><span class="sxs-lookup"><span data-stu-id="ebc8d-108">DESCRIPTION</span></span>
<span data-ttu-id="ebc8d-109">Cmdlet Get-AzVMGuestPolicyStatusHistory會針對指派給 VM 的「來賓組配置」類型之計畫，獲得來賓群組原則的合規性狀態歷程記錄。</span><span class="sxs-lookup"><span data-stu-id="ebc8d-109">The Get-AzVMGuestPolicyStatusHistory cmdlet gets compliance status history of guest configuration policies for an initiative of type "Guest Configuration" that is assigned to a VM.</span></span>
<span data-ttu-id="ebc8d-110">計畫是定義類型「計畫」的一項政策。</span><span class="sxs-lookup"><span data-stu-id="ebc8d-110">An initiative is a policy of definition type "Initiative".</span></span>
<span data-ttu-id="ebc8d-111">使用 Get-AzVMGuestPolicyStatus Cmdlet，使用 ReportId 取得單一合規性狀態的詳細資訊，可在 Get-AzVMGuestPolicyStatusHistory Cmdlet 的輸出中找到。</span><span class="sxs-lookup"><span data-stu-id="ebc8d-111">Use Get-AzVMGuestPolicyStatus cmdlet to get details of a single compliance status using ReportId that can be found in output of Get-AzVMGuestPolicyStatusHistory cmdlet.</span></span>

## <span data-ttu-id="ebc8d-112">例子</span><span class="sxs-lookup"><span data-stu-id="ebc8d-112">EXAMPLES</span></span>

### <span data-ttu-id="ebc8d-113">範例 1</span><span class="sxs-lookup"><span data-stu-id="ebc8d-113">Example 1</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeId "/providers/Microsoft.Authorization/policySetDefinitions/3fa7cbf5-c0a4-4a59-85a5-cca4d996d5af" -ShowOnlyChange
```

<span data-ttu-id="ebc8d-114">根據計畫識別碼來獲得合規性狀態歷程記錄。ShowOnlyChange 切換只會顯示歷程記錄狀態變更。</span><span class="sxs-lookup"><span data-stu-id="ebc8d-114">Gets compliance status history by initiative Id. ShowOnlyChange switch shows only historical status changes.</span></span>
<span data-ttu-id="ebc8d-115">略過未在兩個合規性檢查之間變更的狀態。</span><span class="sxs-lookup"><span data-stu-id="ebc8d-115">Skips statuses that have not changed between two compliance checks.</span></span>

### <span data-ttu-id="ebc8d-116">範例 2</span><span class="sxs-lookup"><span data-stu-id="ebc8d-116">Example 2</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeName "b5a822e0-ba98-4e54-9278-5d9833aa9b17" -ShowOnlyChange
```

<span data-ttu-id="ebc8d-117">根據計畫名稱來獲得合規性狀態歷程記錄。</span><span class="sxs-lookup"><span data-stu-id="ebc8d-117">Gets compliance status history by initiative name.</span></span>
<span data-ttu-id="ebc8d-118">ShowOnlyChange 切換只會顯示歷史狀態變更。</span><span class="sxs-lookup"><span data-stu-id="ebc8d-118">ShowOnlyChange switch shows only historical status changes.</span></span>
<span data-ttu-id="ebc8d-119">略過未在兩個合規性檢查之間變更的狀態。</span><span class="sxs-lookup"><span data-stu-id="ebc8d-119">Skips statuses that have not changed between two compliance checks.</span></span>

### <span data-ttu-id="ebc8d-120">範例 3</span><span class="sxs-lookup"><span data-stu-id="ebc8d-120">Example 3</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -ShowOnlyChange
```

<span data-ttu-id="ebc8d-121">為指派給 VM 的所有來賓群組原則，獲得合規性狀態歷程記錄。</span><span class="sxs-lookup"><span data-stu-id="ebc8d-121">Gets compliance status history for all guest configuration policies assigned to the VM.</span></span>
<span data-ttu-id="ebc8d-122">ShowOnlyChange 切換只會顯示歷史狀態變更。</span><span class="sxs-lookup"><span data-stu-id="ebc8d-122">ShowOnlyChange switch shows only historical status changes.</span></span>
<span data-ttu-id="ebc8d-123">略過未在兩個合規性檢查之間變更的狀態。</span><span class="sxs-lookup"><span data-stu-id="ebc8d-123">Skips statuses that have not changed between two compliance checks.</span></span>

### <span data-ttu-id="ebc8d-124">範例 4</span><span class="sxs-lookup"><span data-stu-id="ebc8d-124">Example 4</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeId "/providers/Microsoft.Authorization/policySetDefinitions/3fa7cbf5-c0a4-4a59-85a5-cca4d996d5af"
```

<span data-ttu-id="ebc8d-125">根據計畫識別碼來獲得合規性狀態歷程記錄。</span><span class="sxs-lookup"><span data-stu-id="ebc8d-125">Gets compliance status history by initiative Id.</span></span>

### <span data-ttu-id="ebc8d-126">範例 5</span><span class="sxs-lookup"><span data-stu-id="ebc8d-126">Example 5</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeName "b5a822e0-ba98-4e54-9278-5d9833aa9b17"
```

<span data-ttu-id="ebc8d-127">根據計畫名稱來獲得合規性狀態歷程記錄。</span><span class="sxs-lookup"><span data-stu-id="ebc8d-127">Gets compliance status history by initiative name.</span></span>

### <span data-ttu-id="ebc8d-128">範例 6</span><span class="sxs-lookup"><span data-stu-id="ebc8d-128">Example 6</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName"
```
<span data-ttu-id="ebc8d-129">為指派給 VM 的所有來賓群組原則，獲得合規性狀態歷程記錄。</span><span class="sxs-lookup"><span data-stu-id="ebc8d-129">Gets compliance status history for all guest configuration policies assigned to the VM.</span></span>

### <span data-ttu-id="ebc8d-130">範例 7</span><span class="sxs-lookup"><span data-stu-id="ebc8d-130">Example 7</span></span>
```powershell
PS C:\>$x = Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName"
PS C:\>$x[10].ReportId
/subscriptions/4e6c6ed2-0bf6-41d7-9d21-a452c2cc7920/resourceGroups/MyResourceGroupName/providers/Microsoft.Compute/virtualMachines/MyVMName/providers/Microsoft.GuestConfiguration/guestConfigurationAssignments/MaximumPasswordAge/reports/c271f845-2c0a-4456-a441-e48fc332d0ac
PS C:\> Get-AzVMGuestPolicyStatus -ReportId $x[10].ReportId
```

<span data-ttu-id="ebc8d-131">根據 ReportId 取得來賓群組原則狀態。</span><span class="sxs-lookup"><span data-stu-id="ebc8d-131">Get guest configuration policy status by ReportId.</span></span>
<span data-ttu-id="ebc8d-132">ReportId 是 ReportId 屬性，可在 Get-AzEVGuestPolicyStatusHistory 結果中找到。</span><span class="sxs-lookup"><span data-stu-id="ebc8d-132">The ReportId is the ReportId property that can be found in the results of Get-AzVMGuestPolicyStatusHistory.</span></span> <span data-ttu-id="ebc8d-133"> (請參閱其他範例) </span><span class="sxs-lookup"><span data-stu-id="ebc8d-133">(please refer other examples)</span></span>

## <span data-ttu-id="ebc8d-134">參數</span><span class="sxs-lookup"><span data-stu-id="ebc8d-134">PARAMETERS</span></span>

### <span data-ttu-id="ebc8d-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebc8d-135">-DefaultProfile</span></span>
<span data-ttu-id="ebc8d-136">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="ebc8d-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ebc8d-137">-InitiativeId</span><span class="sxs-lookup"><span data-stu-id="ebc8d-137">-InitiativeId</span></span>
<span data-ttu-id="ebc8d-138">定義類型為計畫且類別為來賓群組原則的定義識別碼</span><span class="sxs-lookup"><span data-stu-id="ebc8d-138">Definition Id of a policy where definition type is Initiative and category is Guest Configuration</span></span>

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

### <span data-ttu-id="ebc8d-139">-InitiativeName</span><span class="sxs-lookup"><span data-stu-id="ebc8d-139">-InitiativeName</span></span>
<span data-ttu-id="ebc8d-140">定義類型為計畫且類別為來賓群組原則之策略的名稱</span><span class="sxs-lookup"><span data-stu-id="ebc8d-140">Name of a policy where definition type is Initiative and category is Guest Configuration</span></span>

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

### <span data-ttu-id="ebc8d-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ebc8d-141">-ResourceGroupName</span></span>
<span data-ttu-id="ebc8d-142">資源組名。</span><span class="sxs-lookup"><span data-stu-id="ebc8d-142">Resource group name.</span></span>

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

### <span data-ttu-id="ebc8d-143">-ShowOnlyChange</span><span class="sxs-lookup"><span data-stu-id="ebc8d-143">-ShowOnlyChange</span></span>
<span data-ttu-id="ebc8d-144">只顯示來賓群組原則的歷史記錄狀態變更。</span><span class="sxs-lookup"><span data-stu-id="ebc8d-144">Shows historical status changes only for guest configuration policies.</span></span>
<span data-ttu-id="ebc8d-145">略過在兩個合規性狀態稽核執行之間未變更的狀態。</span><span class="sxs-lookup"><span data-stu-id="ebc8d-145">Skips statuses that have not changed between two compliance status audit runs.</span></span>

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

### <span data-ttu-id="ebc8d-146">-VMName</span><span class="sxs-lookup"><span data-stu-id="ebc8d-146">-VMName</span></span>
<span data-ttu-id="ebc8d-147">VM 名稱。</span><span class="sxs-lookup"><span data-stu-id="ebc8d-147">VM name.</span></span>

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

### <span data-ttu-id="ebc8d-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebc8d-148">CommonParameters</span></span>
<span data-ttu-id="ebc8d-149">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ebc8d-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebc8d-150">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="ebc8d-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebc8d-151">輸入</span><span class="sxs-lookup"><span data-stu-id="ebc8d-151">INPUTS</span></span>

### <span data-ttu-id="ebc8d-152">沒有</span><span class="sxs-lookup"><span data-stu-id="ebc8d-152">None</span></span>
## <span data-ttu-id="ebc8d-153">輸出</span><span class="sxs-lookup"><span data-stu-id="ebc8d-153">OUTPUTS</span></span>

### <span data-ttu-id="ebc8d-154">Microsoft.Azure.Commands.GuestConfiguration.models.PolicyStatus</span><span class="sxs-lookup"><span data-stu-id="ebc8d-154">Microsoft.Azure.Commands.GuestConfiguration.Models.PolicyStatus</span></span>
## <span data-ttu-id="ebc8d-155">筆記</span><span class="sxs-lookup"><span data-stu-id="ebc8d-155">NOTES</span></span>

## <span data-ttu-id="ebc8d-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="ebc8d-156">RELATED LINKS</span></span>
