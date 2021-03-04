---
external help file: Microsoft.Azure.PowerShell.Cmdlets.GuestConfiguration.dll-Help.xml
Module Name: Az.GuestConfiguration
online version: https://docs.microsoft.com/powershell/module/az.guestconfiguration/get-AzVMGuestPolicyStatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatus.md
ms.openlocfilehash: 3edb92ae8c46ab67e0e22ee808e38dad7101bfdf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911682"
---
# <span data-ttu-id="0b000-101">Get-AzVMGuestPolicyStatus</span><span class="sxs-lookup"><span data-stu-id="0b000-101">Get-AzVMGuestPolicyStatus</span></span>

## <span data-ttu-id="0b000-102">簡介</span><span class="sxs-lookup"><span data-stu-id="0b000-102">SYNOPSIS</span></span>
<span data-ttu-id="0b000-103">針對指派給 VM 的 (「來賓) 計畫，獲得來賓群組原則狀態的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="0b000-103">Gets guest configuration policy statuses (detailed) for an initiative of type "Guest Configuration" that is assigned to a VM.</span></span>
<span data-ttu-id="0b000-104">計畫是定義類型「計畫」的一項政策。</span><span class="sxs-lookup"><span data-stu-id="0b000-104">An initiative is a policy of definition type "Initiative".</span></span>

## <span data-ttu-id="0b000-105">語法</span><span class="sxs-lookup"><span data-stu-id="0b000-105">SYNTAX</span></span>

### <span data-ttu-id="0b000-106">VmScope (預設) </span><span class="sxs-lookup"><span data-stu-id="0b000-106">VmScope (Default)</span></span>
```
Get-AzVMGuestPolicyStatus [-ResourceGroupName] <String> [-VMName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0b000-107">InitiativeIdScope</span><span class="sxs-lookup"><span data-stu-id="0b000-107">InitiativeIdScope</span></span>
```
Get-AzVMGuestPolicyStatus [-ResourceGroupName] <String> [-VMName] <String> [-InitiativeId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0b000-108">InitiativeNameScope</span><span class="sxs-lookup"><span data-stu-id="0b000-108">InitiativeNameScope</span></span>
```
Get-AzVMGuestPolicyStatus [-ResourceGroupName] <String> [-VMName] <String> [-InitiativeName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0b000-109">ReportIdScope</span><span class="sxs-lookup"><span data-stu-id="0b000-109">ReportIdScope</span></span>
```
Get-AzVMGuestPolicyStatus [-ReportId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0b000-110">描述</span><span class="sxs-lookup"><span data-stu-id="0b000-110">DESCRIPTION</span></span>
<span data-ttu-id="0b000-111">Cmdlet Get-AzVMGuestPolicyStatus會針對指派給 VM 的「來賓群組原則」類型計畫，獲得來賓群組原則狀態。</span><span class="sxs-lookup"><span data-stu-id="0b000-111">The Get-AzVMGuestPolicyStatus cmdlet gets guest configuration policy statuses for an initiative of type "Guest Configuration" that is assigned to a VM.</span></span>
<span data-ttu-id="0b000-112">計畫是定義類型「計畫」的一項政策。</span><span class="sxs-lookup"><span data-stu-id="0b000-112">An initiative is a policy of definition type "Initiative".</span></span>
<span data-ttu-id="0b000-113">此 Cmdlet 會獲得 VM 的合規性狀態，以及該計畫中個別政策不符合規範的原因。</span><span class="sxs-lookup"><span data-stu-id="0b000-113">This cmdlet gets compliance statuses of the VM and reasons why it is non-compliant for the individual policies in the initiative.</span></span>

## <span data-ttu-id="0b000-114">例子</span><span class="sxs-lookup"><span data-stu-id="0b000-114">EXAMPLES</span></span>

### <span data-ttu-id="0b000-115">範例 1</span><span class="sxs-lookup"><span data-stu-id="0b000-115">Example 1</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName"
```

<span data-ttu-id="0b000-116">取得 VM 的所有最新來賓群組原則狀態。</span><span class="sxs-lookup"><span data-stu-id="0b000-116">Get all latest guest configuration policy statuses for a VM.</span></span>
<span data-ttu-id="0b000-117">狀態包含所有「來賓組配置」類型中每個計畫之每個策略的合規性狀態、合規性原因、合規性檢查的時間、已檢查合規性的資源資訊。</span><span class="sxs-lookup"><span data-stu-id="0b000-117">The status includes compliance status of the VM for each policy in all initiatives of type "Guest Configuration", compliance reasons, time of the compliance check, resource information which was checked for compliance.</span></span>
<span data-ttu-id="0b000-118">結果包含最新的狀態，不包含先前的歷史狀態。</span><span class="sxs-lookup"><span data-stu-id="0b000-118">The results include latest statuses, does not include previous historical statuses.</span></span>

### <span data-ttu-id="0b000-119">範例 2</span><span class="sxs-lookup"><span data-stu-id="0b000-119">Example 2</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeId "/providers/Microsoft.Authorization/policySetDefinitions/3fa7cbf5-c0a4-4a59-85a5-cca4d996d5af"
```

<span data-ttu-id="0b000-120">根據計畫識別碼取得最新的來賓群組原則狀態。狀態包括計畫中每個政策之 VM 的合規性狀態、合規性原因、合規性檢查的時間、已檢查合規性的資源資訊。</span><span class="sxs-lookup"><span data-stu-id="0b000-120">Get the latest guest configuration policy statuses by initiative Id. The status includes compliance status of the VM for each policy in the initiative, compliance reasons, time of the compliance check, resource information which was checked for compliance.</span></span>
<span data-ttu-id="0b000-121">結果不包含先前產生的狀態，它只包含計畫中每個政策的最新狀態。</span><span class="sxs-lookup"><span data-stu-id="0b000-121">The results does not include previous statuses generated, it just includes latest status for each policy in the initiative.</span></span>

### <span data-ttu-id="0b000-122">範例 3</span><span class="sxs-lookup"><span data-stu-id="0b000-122">Example 3</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeName "b5a822e0-ba98-4e54-9278-5d9833aa9b17"
```

<span data-ttu-id="0b000-123">根據計畫名稱取得最新的來賓群組原則狀態。</span><span class="sxs-lookup"><span data-stu-id="0b000-123">Get the latest guest configuration policy statuses by initiative name.</span></span>
<span data-ttu-id="0b000-124">狀態包括計畫中每個政策之 VM 的合規性狀態、合規性原因、合規性檢查的時間、已檢查合規性的資源資訊。</span><span class="sxs-lookup"><span data-stu-id="0b000-124">The status includes compliance status of the VM for each policy in the initiative, compliance reasons, time of the compliance check, resource information which was checked for compliance.</span></span>
<span data-ttu-id="0b000-125">結果不包含先前產生的狀態，它只包含計畫中每個政策的最新狀態。</span><span class="sxs-lookup"><span data-stu-id="0b000-125">The results does not include previous statuses generated, it just includes latest status for each policy in the initiative.</span></span>

### <span data-ttu-id="0b000-126">範例 4</span><span class="sxs-lookup"><span data-stu-id="0b000-126">Example 4</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ReportId "/subscriptions/4e6c6ed2-0bf6-41d7-9d21-a452c2cc7920/resourceGroups/MyResourceGroupName/providers/Microsoft.Compute/virtualMachines/MyVMName/providers/Microsoft.GuestConfiguration/guestConfigurationAssignments/MaximumPasswordAge/reports/c271f845-2c0a-4456-a441-e48fc332d0ac"
```

<span data-ttu-id="0b000-127">根據 ReportId 取得來賓群組原則狀態。</span><span class="sxs-lookup"><span data-stu-id="0b000-127">Get guest configuration policy status by ReportId.</span></span>
<span data-ttu-id="0b000-128">ReportId 是 ReportId 屬性，可在Get-AzVMGuestPolicyStatus id 或計畫名稱找到 (請參閱其他範例) </span><span class="sxs-lookup"><span data-stu-id="0b000-128">The ReportId is the ReportId property that can be found in the results of Get-AzVMGuestPolicyStatus by initiativeId or Initiative name (please refer other examples)</span></span>

## <span data-ttu-id="0b000-129">參數</span><span class="sxs-lookup"><span data-stu-id="0b000-129">PARAMETERS</span></span>

### <span data-ttu-id="0b000-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b000-130">-DefaultProfile</span></span>
<span data-ttu-id="0b000-131">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="0b000-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b000-132">-InitiativeId</span><span class="sxs-lookup"><span data-stu-id="0b000-132">-InitiativeId</span></span>
<span data-ttu-id="0b000-133">定義類型為計畫且類別為來賓群組原則的定義識別碼</span><span class="sxs-lookup"><span data-stu-id="0b000-133">Definition Id of a policy where definition type is Initiative and category is Guest Configuration</span></span>

```yaml
Type: System.String
Parameter Sets: InitiativeIdScope
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b000-134">-InitiativeName</span><span class="sxs-lookup"><span data-stu-id="0b000-134">-InitiativeName</span></span>
<span data-ttu-id="0b000-135">定義類型為計畫且類別為來賓群組原則之策略的名稱</span><span class="sxs-lookup"><span data-stu-id="0b000-135">Name of a policy where definition type is Initiative and category is Guest Configuration</span></span>

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

### <span data-ttu-id="0b000-136">-ReportId</span><span class="sxs-lookup"><span data-stu-id="0b000-136">-ReportId</span></span>
<span data-ttu-id="0b000-137">來賓群組原則狀態的識別碼。</span><span class="sxs-lookup"><span data-stu-id="0b000-137">Id of a Guest Configuration policy status.</span></span>
<span data-ttu-id="0b000-138">定義類型為計畫且類別為來賓群組原則時，必須指派給範圍以取得狀態。</span><span class="sxs-lookup"><span data-stu-id="0b000-138">A policy where definition type is Initiative and category is Guest Configuration must be assigned to a scope to get statuses.</span></span>

```yaml
Type: System.String
Parameter Sets: ReportIdScope
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b000-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b000-139">-ResourceGroupName</span></span>
<span data-ttu-id="0b000-140">資源組名。</span><span class="sxs-lookup"><span data-stu-id="0b000-140">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: VmScope, InitiativeIdScope, InitiativeNameScope
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b000-141">-VMName</span><span class="sxs-lookup"><span data-stu-id="0b000-141">-VMName</span></span>
<span data-ttu-id="0b000-142">VM 名稱。</span><span class="sxs-lookup"><span data-stu-id="0b000-142">VM name.</span></span>

```yaml
Type: System.String
Parameter Sets: VmScope, InitiativeIdScope, InitiativeNameScope
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b000-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b000-143">CommonParameters</span></span>
<span data-ttu-id="0b000-144">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="0b000-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b000-145">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="0b000-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b000-146">輸入</span><span class="sxs-lookup"><span data-stu-id="0b000-146">INPUTS</span></span>

### <span data-ttu-id="0b000-147">沒有</span><span class="sxs-lookup"><span data-stu-id="0b000-147">None</span></span>
## <span data-ttu-id="0b000-148">輸出</span><span class="sxs-lookup"><span data-stu-id="0b000-148">OUTPUTS</span></span>

### <span data-ttu-id="0b000-149">Microsoft.Azure.Commands.GuestConfiguration.models.PolicyStatusDetailed</span><span class="sxs-lookup"><span data-stu-id="0b000-149">Microsoft.Azure.Commands.GuestConfiguration.Models.PolicyStatusDetailed</span></span>
## <span data-ttu-id="0b000-150">筆記</span><span class="sxs-lookup"><span data-stu-id="0b000-150">NOTES</span></span>

## <span data-ttu-id="0b000-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="0b000-151">RELATED LINKS</span></span>
