---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/stop-azpolicyremediation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Stop-AzPolicyRemediation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Stop-AzPolicyRemediation.md
ms.openlocfilehash: 9dfb3ff2f50df7a858ab8194ec86fa312501dcff
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100140119"
---
# <span data-ttu-id="46c0d-101">Stop-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="46c0d-101">Stop-AzPolicyRemediation</span></span>

## <span data-ttu-id="46c0d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="46c0d-102">SYNOPSIS</span></span>
<span data-ttu-id="46c0d-103">取消進行中的原則修正。</span><span class="sxs-lookup"><span data-stu-id="46c0d-103">Cancels an in-progress policy remediation.</span></span>

## <span data-ttu-id="46c0d-104">句法</span><span class="sxs-lookup"><span data-stu-id="46c0d-104">SYNTAX</span></span>

### <span data-ttu-id="46c0d-105">ByName (預設) </span><span class="sxs-lookup"><span data-stu-id="46c0d-105">ByName (Default)</span></span>
```
Stop-AzPolicyRemediation -Name <String> [-Scope <String>] [-ManagementGroupName <String>]
 [-ResourceGroupName <String>] [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46c0d-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="46c0d-106">ByResourceId</span></span>
```
Stop-AzPolicyRemediation -ResourceId <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46c0d-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="46c0d-107">ByInputObject</span></span>
```
Stop-AzPolicyRemediation -InputObject <PSRemediation> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46c0d-108">說明</span><span class="sxs-lookup"><span data-stu-id="46c0d-108">DESCRIPTION</span></span>
<span data-ttu-id="46c0d-109">**AzPolicyRemediation** Cmdlet 會取消進行中原則修正。</span><span class="sxs-lookup"><span data-stu-id="46c0d-109">The **Stop-AzPolicyRemediation** cmdlet cancels an in-progress policy remediation.</span></span> <span data-ttu-id="46c0d-110">將會取消作用中的部署，而且不會建立新的部署。</span><span class="sxs-lookup"><span data-stu-id="46c0d-110">Active deployments will be canceled and no new deployments will be created.</span></span>

## <span data-ttu-id="46c0d-111">示例</span><span class="sxs-lookup"><span data-stu-id="46c0d-111">EXAMPLES</span></span>

### <span data-ttu-id="46c0d-112">範例1：取消資源群組作用中的原則修正</span><span class="sxs-lookup"><span data-stu-id="46c0d-112">Example 1: Cancel a policy remediation at resource group scope</span></span>
```
PS C:\> Stop-AzPolicyRemediation -ResourceGroupName "myRG" -Name "remediation1"
```

<span data-ttu-id="46c0d-113">這個命令會取消資源群組 ' myRG ' 中名為「remediation1」的修正。</span><span class="sxs-lookup"><span data-stu-id="46c0d-113">This command cancels the remediation named 'remediation1' in resource group 'myRG'.</span></span>

### <span data-ttu-id="46c0d-114">範例2：透過管道取消管理群組修正</span><span class="sxs-lookup"><span data-stu-id="46c0d-114">Example 2: Cancel a management group remediation via piping</span></span>
```
PS C:\> $remediation = Get-AzPolicyRemediation -ManagementGroupName "mg1" -Name "remediation1"
PS C:\> $remediation | Stop-AzPolicyRemediation
```

<span data-ttu-id="46c0d-115">這個命令會在管理群組 ' mg1」中取消名為「remediation1」的修正。</span><span class="sxs-lookup"><span data-stu-id="46c0d-115">This command cancels the remediation named 'remediation1' in management group 'mg1'.</span></span>

## <span data-ttu-id="46c0d-116">參數</span><span class="sxs-lookup"><span data-stu-id="46c0d-116">PARAMETERS</span></span>

### <span data-ttu-id="46c0d-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="46c0d-117">-AsJob</span></span>
<span data-ttu-id="46c0d-118">在背景中執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="46c0d-118">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="46c0d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46c0d-119">-DefaultProfile</span></span>
<span data-ttu-id="46c0d-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="46c0d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46c0d-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="46c0d-121">-InputObject</span></span>
<span data-ttu-id="46c0d-122">修正物件。</span><span class="sxs-lookup"><span data-stu-id="46c0d-122">The Remediation object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="46c0d-123">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="46c0d-123">-ManagementGroupName</span></span>
<span data-ttu-id="46c0d-124">管理群組識別碼。</span><span class="sxs-lookup"><span data-stu-id="46c0d-124">Management group ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46c0d-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="46c0d-125">-Name</span></span>
<span data-ttu-id="46c0d-126">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="46c0d-126">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46c0d-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="46c0d-127">-PassThru</span></span>
<span data-ttu-id="46c0d-128">如果命令順利完成，則傳回 True。</span><span class="sxs-lookup"><span data-stu-id="46c0d-128">Return True if the command completes successfully.</span></span>

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

### <span data-ttu-id="46c0d-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46c0d-129">-ResourceGroupName</span></span>
<span data-ttu-id="46c0d-130">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="46c0d-130">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46c0d-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="46c0d-131">-ResourceId</span></span>
<span data-ttu-id="46c0d-132">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="46c0d-132">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46c0d-133">-範圍</span><span class="sxs-lookup"><span data-stu-id="46c0d-133">-Scope</span></span>
<span data-ttu-id="46c0d-134">資源範圍。</span><span class="sxs-lookup"><span data-stu-id="46c0d-134">Scope of the resource.</span></span>
<span data-ttu-id="46c0d-135">例如.</span><span class="sxs-lookup"><span data-stu-id="46c0d-135">E.g.</span></span>
<span data-ttu-id="46c0d-136">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span><span class="sxs-lookup"><span data-stu-id="46c0d-136">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46c0d-137">-確認</span><span class="sxs-lookup"><span data-stu-id="46c0d-137">-Confirm</span></span>
<span data-ttu-id="46c0d-138">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="46c0d-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46c0d-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46c0d-139">-WhatIf</span></span>
<span data-ttu-id="46c0d-140">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="46c0d-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46c0d-141">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="46c0d-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46c0d-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46c0d-142">CommonParameters</span></span>
<span data-ttu-id="46c0d-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="46c0d-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46c0d-144">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="46c0d-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46c0d-145">輸入</span><span class="sxs-lookup"><span data-stu-id="46c0d-145">INPUTS</span></span>

### <span data-ttu-id="46c0d-146">System.object</span><span class="sxs-lookup"><span data-stu-id="46c0d-146">System.String</span></span>

### <span data-ttu-id="46c0d-147">PSRemediation 中的 PolicyInsights。</span><span class="sxs-lookup"><span data-stu-id="46c0d-147">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span></span>

## <span data-ttu-id="46c0d-148">輸出</span><span class="sxs-lookup"><span data-stu-id="46c0d-148">OUTPUTS</span></span>

### <span data-ttu-id="46c0d-149">System.object</span><span class="sxs-lookup"><span data-stu-id="46c0d-149">System.Boolean</span></span>

## <span data-ttu-id="46c0d-150">筆記</span><span class="sxs-lookup"><span data-stu-id="46c0d-150">NOTES</span></span>

## <span data-ttu-id="46c0d-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="46c0d-151">RELATED LINKS</span></span>
