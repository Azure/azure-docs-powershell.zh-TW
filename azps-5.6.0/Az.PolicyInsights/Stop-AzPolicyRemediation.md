---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/powershell/module/az.policyinsights/stop-azpolicyremediation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Stop-AzPolicyRemediation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Stop-AzPolicyRemediation.md
ms.openlocfilehash: 2eb9d5a11b160a1061bbd769f337cf053b6ad805
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911354"
---
# <span data-ttu-id="eca8e-101">Stop-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="eca8e-101">Stop-AzPolicyRemediation</span></span>

## <span data-ttu-id="eca8e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="eca8e-102">SYNOPSIS</span></span>
<span data-ttu-id="eca8e-103">取消進行中的策略補救。</span><span class="sxs-lookup"><span data-stu-id="eca8e-103">Cancels an in-progress policy remediation.</span></span>

## <span data-ttu-id="eca8e-104">語法</span><span class="sxs-lookup"><span data-stu-id="eca8e-104">SYNTAX</span></span>

### <span data-ttu-id="eca8e-105">ByName (預設) </span><span class="sxs-lookup"><span data-stu-id="eca8e-105">ByName (Default)</span></span>
```
Stop-AzPolicyRemediation -Name <String> [-Scope <String>] [-ManagementGroupName <String>]
 [-ResourceGroupName <String>] [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eca8e-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="eca8e-106">ByResourceId</span></span>
```
Stop-AzPolicyRemediation -ResourceId <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eca8e-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="eca8e-107">ByInputObject</span></span>
```
Stop-AzPolicyRemediation -InputObject <PSRemediation> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eca8e-108">描述</span><span class="sxs-lookup"><span data-stu-id="eca8e-108">DESCRIPTION</span></span>
<span data-ttu-id="eca8e-109">**Stop-AzPolicyRemediation** Cmdlet 會取消進行中的策略補救。</span><span class="sxs-lookup"><span data-stu-id="eca8e-109">The **Stop-AzPolicyRemediation** cmdlet cancels an in-progress policy remediation.</span></span> <span data-ttu-id="eca8e-110">活動部署將會取消，而且不會建立新的部署。</span><span class="sxs-lookup"><span data-stu-id="eca8e-110">Active deployments will be canceled and no new deployments will be created.</span></span>

## <span data-ttu-id="eca8e-111">例子</span><span class="sxs-lookup"><span data-stu-id="eca8e-111">EXAMPLES</span></span>

### <span data-ttu-id="eca8e-112">範例 1：取消資源群組範圍中的策略補救</span><span class="sxs-lookup"><span data-stu-id="eca8e-112">Example 1: Cancel a policy remediation at resource group scope</span></span>
```
PS C:\> Stop-AzPolicyRemediation -ResourceGroupName "myRG" -Name "remediation1"
```

<span data-ttu-id="eca8e-113">此命令會取消資源群組 "myRG" 中名為 "remediation1" 的補救。</span><span class="sxs-lookup"><span data-stu-id="eca8e-113">This command cancels the remediation named 'remediation1' in resource group 'myRG'.</span></span>

### <span data-ttu-id="eca8e-114">範例 2：透過管線取消管理群組補救</span><span class="sxs-lookup"><span data-stu-id="eca8e-114">Example 2: Cancel a management group remediation via piping</span></span>
```
PS C:\> $remediation = Get-AzPolicyRemediation -ManagementGroupName "mg1" -Name "remediation1"
PS C:\> $remediation | Stop-AzPolicyRemediation
```

<span data-ttu-id="eca8e-115">此命令會取消管理群組 "mg1" 中名為 "remediation1" 的補救。</span><span class="sxs-lookup"><span data-stu-id="eca8e-115">This command cancels the remediation named 'remediation1' in management group 'mg1'.</span></span>

## <span data-ttu-id="eca8e-116">參數</span><span class="sxs-lookup"><span data-stu-id="eca8e-116">PARAMETERS</span></span>

### <span data-ttu-id="eca8e-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="eca8e-117">-AsJob</span></span>
<span data-ttu-id="eca8e-118">在背景中執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="eca8e-118">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="eca8e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eca8e-119">-DefaultProfile</span></span>
<span data-ttu-id="eca8e-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="eca8e-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eca8e-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eca8e-121">-InputObject</span></span>
<span data-ttu-id="eca8e-122">修復物件。</span><span class="sxs-lookup"><span data-stu-id="eca8e-122">The Remediation object.</span></span>

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

### <span data-ttu-id="eca8e-123">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="eca8e-123">-ManagementGroupName</span></span>
<span data-ttu-id="eca8e-124">管理群組識別碼。</span><span class="sxs-lookup"><span data-stu-id="eca8e-124">Management group ID.</span></span>

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

### <span data-ttu-id="eca8e-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="eca8e-125">-Name</span></span>
<span data-ttu-id="eca8e-126">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="eca8e-126">Resource name.</span></span>

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

### <span data-ttu-id="eca8e-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="eca8e-127">-PassThru</span></span>
<span data-ttu-id="eca8e-128">如果命令成功完成，請返回 True。</span><span class="sxs-lookup"><span data-stu-id="eca8e-128">Return True if the command completes successfully.</span></span>

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

### <span data-ttu-id="eca8e-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eca8e-129">-ResourceGroupName</span></span>
<span data-ttu-id="eca8e-130">資源組名。</span><span class="sxs-lookup"><span data-stu-id="eca8e-130">Resource group name.</span></span>

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

### <span data-ttu-id="eca8e-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eca8e-131">-ResourceId</span></span>
<span data-ttu-id="eca8e-132">資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="eca8e-132">Resource ID.</span></span>

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

### <span data-ttu-id="eca8e-133">-範圍</span><span class="sxs-lookup"><span data-stu-id="eca8e-133">-Scope</span></span>
<span data-ttu-id="eca8e-134">資源的範圍。</span><span class="sxs-lookup"><span data-stu-id="eca8e-134">Scope of the resource.</span></span>
<span data-ttu-id="eca8e-135">例如</span><span class="sxs-lookup"><span data-stu-id="eca8e-135">E.g.</span></span>
<span data-ttu-id="eca8e-136">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'。</span><span class="sxs-lookup"><span data-stu-id="eca8e-136">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span></span>

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

### <span data-ttu-id="eca8e-137">-確認</span><span class="sxs-lookup"><span data-stu-id="eca8e-137">-Confirm</span></span>
<span data-ttu-id="eca8e-138">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="eca8e-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eca8e-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eca8e-139">-WhatIf</span></span>
<span data-ttu-id="eca8e-140">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="eca8e-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eca8e-141">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="eca8e-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eca8e-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eca8e-142">CommonParameters</span></span>
<span data-ttu-id="eca8e-143">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="eca8e-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eca8e-144">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="eca8e-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eca8e-145">輸入</span><span class="sxs-lookup"><span data-stu-id="eca8e-145">INPUTS</span></span>

### <span data-ttu-id="eca8e-146">System.String</span><span class="sxs-lookup"><span data-stu-id="eca8e-146">System.String</span></span>

### <span data-ttu-id="eca8e-147">Microsoft.Azure.Commands.PolicyInsights.models.Remediation.PSRemediation</span><span class="sxs-lookup"><span data-stu-id="eca8e-147">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span></span>

## <span data-ttu-id="eca8e-148">輸出</span><span class="sxs-lookup"><span data-stu-id="eca8e-148">OUTPUTS</span></span>

### <span data-ttu-id="eca8e-149">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="eca8e-149">System.Boolean</span></span>

## <span data-ttu-id="eca8e-150">筆記</span><span class="sxs-lookup"><span data-stu-id="eca8e-150">NOTES</span></span>

## <span data-ttu-id="eca8e-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="eca8e-151">RELATED LINKS</span></span>
