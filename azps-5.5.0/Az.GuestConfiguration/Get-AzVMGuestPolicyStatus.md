---
external help file: Microsoft.Azure.PowerShell.Cmdlets.GuestConfiguration.dll-Help.xml
Module Name: Az.GuestConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.guestconfiguration/get-AzVMGuestPolicyStatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatus.md
ms.openlocfilehash: 49148f1c62b71436e48b2b92a4591a7cdb36cccf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100132846"
---
# <span data-ttu-id="0c8e1-101">Get-AzVMGuestPolicyStatus</span><span class="sxs-lookup"><span data-stu-id="0c8e1-101">Get-AzVMGuestPolicyStatus</span></span>

## <span data-ttu-id="0c8e1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0c8e1-102">SYNOPSIS</span></span>
<span data-ttu-id="0c8e1-103">取得來賓設定原則狀態 (詳細) ，以取得指派給 VM 之「來賓設定」類型的計畫。</span><span class="sxs-lookup"><span data-stu-id="0c8e1-103">Gets guest configuration policy statuses (detailed) for an initiative of type "Guest Configuration" that is assigned to a VM.</span></span>
<span data-ttu-id="0c8e1-104">方案是「倡議」定義類型的原則。</span><span class="sxs-lookup"><span data-stu-id="0c8e1-104">An initiative is a policy of definition type "Initiative".</span></span>

## <span data-ttu-id="0c8e1-105">句法</span><span class="sxs-lookup"><span data-stu-id="0c8e1-105">SYNTAX</span></span>

### <span data-ttu-id="0c8e1-106">VmScope (預設) </span><span class="sxs-lookup"><span data-stu-id="0c8e1-106">VmScope (Default)</span></span>
```
Get-AzVMGuestPolicyStatus [-ResourceGroupName] <String> [-VMName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0c8e1-107">InitiativeIdScope</span><span class="sxs-lookup"><span data-stu-id="0c8e1-107">InitiativeIdScope</span></span>
```
Get-AzVMGuestPolicyStatus [-ResourceGroupName] <String> [-VMName] <String> [-InitiativeId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0c8e1-108">InitiativeNameScope</span><span class="sxs-lookup"><span data-stu-id="0c8e1-108">InitiativeNameScope</span></span>
```
Get-AzVMGuestPolicyStatus [-ResourceGroupName] <String> [-VMName] <String> [-InitiativeName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0c8e1-109">ReportIdScope</span><span class="sxs-lookup"><span data-stu-id="0c8e1-109">ReportIdScope</span></span>
```
Get-AzVMGuestPolicyStatus [-ReportId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0c8e1-110">說明</span><span class="sxs-lookup"><span data-stu-id="0c8e1-110">DESCRIPTION</span></span>
<span data-ttu-id="0c8e1-111">Get-AzVMGuestPolicyStatus Cmdlet 會取得指派給 VM 之「來賓配置」類型之計畫的來賓設定原則狀態。</span><span class="sxs-lookup"><span data-stu-id="0c8e1-111">The Get-AzVMGuestPolicyStatus cmdlet gets guest configuration policy statuses for an initiative of type "Guest Configuration" that is assigned to a VM.</span></span>
<span data-ttu-id="0c8e1-112">方案是「倡議」定義類型的原則。</span><span class="sxs-lookup"><span data-stu-id="0c8e1-112">An initiative is a policy of definition type "Initiative".</span></span>
<span data-ttu-id="0c8e1-113">這個 Cmdlet 會取得 VM 的相容性狀態，以及為什麼它不符合方案中個別原則的原因。</span><span class="sxs-lookup"><span data-stu-id="0c8e1-113">This cmdlet gets compliance statuses of the VM and reasons why it is non-compliant for the individual policies in the initiative.</span></span>

## <span data-ttu-id="0c8e1-114">示例</span><span class="sxs-lookup"><span data-stu-id="0c8e1-114">EXAMPLES</span></span>

### <span data-ttu-id="0c8e1-115">範例1</span><span class="sxs-lookup"><span data-stu-id="0c8e1-115">Example 1</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName"
```

<span data-ttu-id="0c8e1-116">取得 VM 所有最新的來賓設定原則狀態。</span><span class="sxs-lookup"><span data-stu-id="0c8e1-116">Get all latest guest configuration policy statuses for a VM.</span></span>
<span data-ttu-id="0c8e1-117">[狀態] 包含針對「來賓設定」類型的所有計劃中的每個原則的 VM 符合性狀態，遵從性原因，合規性檢查的時間，已針對合規性檢查的資源資訊。</span><span class="sxs-lookup"><span data-stu-id="0c8e1-117">The status includes compliance status of the VM for each policy in all initiatives of type "Guest Configuration", compliance reasons, time of the compliance check, resource information which was checked for compliance.</span></span>
<span data-ttu-id="0c8e1-118">結果包含最新狀態，不會包含先前的歷史狀態。</span><span class="sxs-lookup"><span data-stu-id="0c8e1-118">The results include latest statuses, does not include previous historical statuses.</span></span>

### <span data-ttu-id="0c8e1-119">範例2</span><span class="sxs-lookup"><span data-stu-id="0c8e1-119">Example 2</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeId "/providers/Microsoft.Authorization/policySetDefinitions/3fa7cbf5-c0a4-4a59-85a5-cca4d996d5af"
```

<span data-ttu-id="0c8e1-120">依計畫識別碼取得最新的來賓設定原則狀態。狀態會在計畫中包含每個原則的 VM 合規性狀態、遵從性原因、合規性檢查的時間，以及已針對合規性檢查的資源資訊。</span><span class="sxs-lookup"><span data-stu-id="0c8e1-120">Get the latest guest configuration policy statuses by initiative Id. The status includes compliance status of the VM for each policy in the initiative, compliance reasons, time of the compliance check, resource information which was checked for compliance.</span></span>
<span data-ttu-id="0c8e1-121">結果不包括先前產生的狀態，它只會包含方案中每個原則的最新狀態。</span><span class="sxs-lookup"><span data-stu-id="0c8e1-121">The results does not include previous statuses generated, it just includes latest status for each policy in the initiative.</span></span>

### <span data-ttu-id="0c8e1-122">範例3</span><span class="sxs-lookup"><span data-stu-id="0c8e1-122">Example 3</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeName "b5a822e0-ba98-4e54-9278-5d9833aa9b17"
```

<span data-ttu-id="0c8e1-123">依計畫名稱取得最新的來賓配置原則狀態。</span><span class="sxs-lookup"><span data-stu-id="0c8e1-123">Get the latest guest configuration policy statuses by initiative name.</span></span>
<span data-ttu-id="0c8e1-124">狀態會在計畫中包含每個原則的 VM 合規性狀態、遵從性原因、合規性檢查的時間，以及已針對合規性檢查的資源資訊。</span><span class="sxs-lookup"><span data-stu-id="0c8e1-124">The status includes compliance status of the VM for each policy in the initiative, compliance reasons, time of the compliance check, resource information which was checked for compliance.</span></span>
<span data-ttu-id="0c8e1-125">結果不包括先前產生的狀態，它只會包含方案中每個原則的最新狀態。</span><span class="sxs-lookup"><span data-stu-id="0c8e1-125">The results does not include previous statuses generated, it just includes latest status for each policy in the initiative.</span></span>

### <span data-ttu-id="0c8e1-126">範例4</span><span class="sxs-lookup"><span data-stu-id="0c8e1-126">Example 4</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ReportId "/subscriptions/4e6c6ed2-0bf6-41d7-9d21-a452c2cc7920/resourceGroups/MyResourceGroupName/providers/Microsoft.Compute/virtualMachines/MyVMName/providers/Microsoft.GuestConfiguration/guestConfigurationAssignments/MaximumPasswordAge/reports/c271f845-2c0a-4456-a441-e48fc332d0ac"
```

<span data-ttu-id="0c8e1-127">依 ReportId 取得來賓設定原則狀態。</span><span class="sxs-lookup"><span data-stu-id="0c8e1-127">Get guest configuration policy status by ReportId.</span></span>
<span data-ttu-id="0c8e1-128">ReportId 是 ReportId 屬性，可在 Get-AzVMGuestPolicyStatus 的結果中找到 initiativeId 或方案名稱 (請參閱其他範例) </span><span class="sxs-lookup"><span data-stu-id="0c8e1-128">The ReportId is the ReportId property that can be found in the results of Get-AzVMGuestPolicyStatus by initiativeId or Initiative name (please refer other examples)</span></span>

## <span data-ttu-id="0c8e1-129">參數</span><span class="sxs-lookup"><span data-stu-id="0c8e1-129">PARAMETERS</span></span>

### <span data-ttu-id="0c8e1-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c8e1-130">-DefaultProfile</span></span>
<span data-ttu-id="0c8e1-131">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0c8e1-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c8e1-132">-InitiativeId</span><span class="sxs-lookup"><span data-stu-id="0c8e1-132">-InitiativeId</span></span>
<span data-ttu-id="0c8e1-133">定義類型為 [倡議] 或 [類別 is 來賓設定] 之原則的定義識別碼</span><span class="sxs-lookup"><span data-stu-id="0c8e1-133">Definition Id of a policy where definition type is Initiative and category is Guest Configuration</span></span>

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

### <span data-ttu-id="0c8e1-134">-InitiativeName</span><span class="sxs-lookup"><span data-stu-id="0c8e1-134">-InitiativeName</span></span>
<span data-ttu-id="0c8e1-135">定義類型為 [倡議]，類別為 [來賓設定] 的原則名稱</span><span class="sxs-lookup"><span data-stu-id="0c8e1-135">Name of a policy where definition type is Initiative and category is Guest Configuration</span></span>

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

### <span data-ttu-id="0c8e1-136">-ReportId</span><span class="sxs-lookup"><span data-stu-id="0c8e1-136">-ReportId</span></span>
<span data-ttu-id="0c8e1-137">來賓配置原則狀態的 Id。</span><span class="sxs-lookup"><span data-stu-id="0c8e1-137">Id of a Guest Configuration policy status.</span></span>
<span data-ttu-id="0c8e1-138">定義類型為「方案」和「類別是來賓設定」的原則必須指派給範圍，才能取得狀態。</span><span class="sxs-lookup"><span data-stu-id="0c8e1-138">A policy where definition type is Initiative and category is Guest Configuration must be assigned to a scope to get statuses.</span></span>

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

### <span data-ttu-id="0c8e1-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c8e1-139">-ResourceGroupName</span></span>
<span data-ttu-id="0c8e1-140">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="0c8e1-140">Resource group name.</span></span>

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

### <span data-ttu-id="0c8e1-141">-VMName</span><span class="sxs-lookup"><span data-stu-id="0c8e1-141">-VMName</span></span>
<span data-ttu-id="0c8e1-142">VM 名稱。</span><span class="sxs-lookup"><span data-stu-id="0c8e1-142">VM name.</span></span>

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

### <span data-ttu-id="0c8e1-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c8e1-143">CommonParameters</span></span>
<span data-ttu-id="0c8e1-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0c8e1-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c8e1-145">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0c8e1-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c8e1-146">輸入</span><span class="sxs-lookup"><span data-stu-id="0c8e1-146">INPUTS</span></span>

### <span data-ttu-id="0c8e1-147">所有</span><span class="sxs-lookup"><span data-stu-id="0c8e1-147">None</span></span>
## <span data-ttu-id="0c8e1-148">輸出</span><span class="sxs-lookup"><span data-stu-id="0c8e1-148">OUTPUTS</span></span>

### <span data-ttu-id="0c8e1-149">PolicyStatusDetailed 中的 GuestConfiguration。</span><span class="sxs-lookup"><span data-stu-id="0c8e1-149">Microsoft.Azure.Commands.GuestConfiguration.Models.PolicyStatusDetailed</span></span>
## <span data-ttu-id="0c8e1-150">筆記</span><span class="sxs-lookup"><span data-stu-id="0c8e1-150">NOTES</span></span>

## <span data-ttu-id="0c8e1-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="0c8e1-151">RELATED LINKS</span></span>
