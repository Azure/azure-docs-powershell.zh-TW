---
external help file: Microsoft.Azure.Commands.PolicyInsights.dll-Help.xml
Module Name: AzureRM.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.policyinsights/stop-azurermpolicyremediation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PolicyInsights/Commands.PolicyInsights/help/Stop-AzureRmPolicyRemediation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PolicyInsights/Commands.PolicyInsights/help/Stop-AzureRmPolicyRemediation.md
ms.openlocfilehash: 6e36b2ce8fb03173bfaab80b68c219873875526c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447299"
---
# <span data-ttu-id="e71c5-101">Stop-AzureRmPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="e71c5-101">Stop-AzureRmPolicyRemediation</span></span>

## <span data-ttu-id="e71c5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e71c5-102">SYNOPSIS</span></span>
<span data-ttu-id="e71c5-103">取消進行中的原則修正。</span><span class="sxs-lookup"><span data-stu-id="e71c5-103">Cancels an in-progress policy remediation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e71c5-104">句法</span><span class="sxs-lookup"><span data-stu-id="e71c5-104">SYNTAX</span></span>

### <span data-ttu-id="e71c5-105">ByName (預設) </span><span class="sxs-lookup"><span data-stu-id="e71c5-105">ByName (Default)</span></span>
```
Stop-AzureRmPolicyRemediation -Name <String> [-Scope <String>] [-ManagementGroupName <String>]
 [-ResourceGroupName <String>] [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e71c5-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e71c5-106">ByResourceId</span></span>
```
Stop-AzureRmPolicyRemediation -ResourceId <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e71c5-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="e71c5-107">ByInputObject</span></span>
```
Stop-AzureRmPolicyRemediation -InputObject <PSRemediation> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e71c5-108">說明</span><span class="sxs-lookup"><span data-stu-id="e71c5-108">DESCRIPTION</span></span>
<span data-ttu-id="e71c5-109">**AzureRmPolicyRemediation** Cmdlet 會取消進行中原則修正。</span><span class="sxs-lookup"><span data-stu-id="e71c5-109">The **Stop-AzureRmPolicyRemediation** cmdlet cancels an in-progress policy remediation.</span></span> <span data-ttu-id="e71c5-110">將會取消作用中的部署，而且不會建立新的部署。</span><span class="sxs-lookup"><span data-stu-id="e71c5-110">Active deployments will be canceled and no new deployments will be created.</span></span>

## <span data-ttu-id="e71c5-111">示例</span><span class="sxs-lookup"><span data-stu-id="e71c5-111">EXAMPLES</span></span>

### <span data-ttu-id="e71c5-112">範例1：取消資源群組作用中的原則修正</span><span class="sxs-lookup"><span data-stu-id="e71c5-112">Example 1: Cancel a policy remediation at resource group scope</span></span>
```
PS C:\> Stop-AzureRmPolicyRemediation -ResourceGroupName "myRG" -Name "remediation1"
```

<span data-ttu-id="e71c5-113">這個命令會取消資源群組 ' myRG ' 中名為「remediation1」的修正。</span><span class="sxs-lookup"><span data-stu-id="e71c5-113">This command cancels the remediation named 'remediation1' in resource group 'myRG'.</span></span>

### <span data-ttu-id="e71c5-114">範例2：透過管道取消管理群組修正</span><span class="sxs-lookup"><span data-stu-id="e71c5-114">Example 2: Cancel a management group remediation via piping</span></span>
```
PS C:\> $remediation = Get-AzureRmPolicyRemediation -ManagementGroupName "mg1" -Name "remediation1"
PS C:\> $remediation | Stop-AzureRmPolicyRemediation
```

<span data-ttu-id="e71c5-115">這個命令會在管理群組 ' mg1」中取消名為「remediation1」的修正。</span><span class="sxs-lookup"><span data-stu-id="e71c5-115">This command cancels the remediation named 'remediation1' in management group 'mg1'.</span></span>

## <span data-ttu-id="e71c5-116">參數</span><span class="sxs-lookup"><span data-stu-id="e71c5-116">PARAMETERS</span></span>

### <span data-ttu-id="e71c5-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e71c5-117">-AsJob</span></span>
<span data-ttu-id="e71c5-118">在背景中執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e71c5-118">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="e71c5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e71c5-119">-DefaultProfile</span></span>
<span data-ttu-id="e71c5-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e71c5-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e71c5-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e71c5-121">-InputObject</span></span>
<span data-ttu-id="e71c5-122">修正物件。</span><span class="sxs-lookup"><span data-stu-id="e71c5-122">The Remediation object.</span></span>

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

### <span data-ttu-id="e71c5-123">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="e71c5-123">-ManagementGroupName</span></span>
<span data-ttu-id="e71c5-124">管理群組識別碼。</span><span class="sxs-lookup"><span data-stu-id="e71c5-124">Management group ID.</span></span>

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

### <span data-ttu-id="e71c5-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="e71c5-125">-Name</span></span>
<span data-ttu-id="e71c5-126">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="e71c5-126">Resource name.</span></span>

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

### <span data-ttu-id="e71c5-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e71c5-127">-PassThru</span></span>
<span data-ttu-id="e71c5-128">如果命令順利完成，則傳回 True。</span><span class="sxs-lookup"><span data-stu-id="e71c5-128">Return True if the command completes successfully.</span></span>

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

### <span data-ttu-id="e71c5-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e71c5-129">-ResourceGroupName</span></span>
<span data-ttu-id="e71c5-130">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="e71c5-130">Resource group name.</span></span>

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

### <span data-ttu-id="e71c5-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e71c5-131">-ResourceId</span></span>
<span data-ttu-id="e71c5-132">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="e71c5-132">Resource ID.</span></span>

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

### <span data-ttu-id="e71c5-133">-範圍</span><span class="sxs-lookup"><span data-stu-id="e71c5-133">-Scope</span></span>
<span data-ttu-id="e71c5-134">資源範圍。</span><span class="sxs-lookup"><span data-stu-id="e71c5-134">Scope of the resource.</span></span>
<span data-ttu-id="e71c5-135">例如.</span><span class="sxs-lookup"><span data-stu-id="e71c5-135">E.g.</span></span>
<span data-ttu-id="e71c5-136">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span><span class="sxs-lookup"><span data-stu-id="e71c5-136">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span></span>

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

### <span data-ttu-id="e71c5-137">-確認</span><span class="sxs-lookup"><span data-stu-id="e71c5-137">-Confirm</span></span>
<span data-ttu-id="e71c5-138">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e71c5-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e71c5-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e71c5-139">-WhatIf</span></span>
<span data-ttu-id="e71c5-140">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e71c5-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e71c5-141">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e71c5-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e71c5-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e71c5-142">CommonParameters</span></span>
<span data-ttu-id="e71c5-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e71c5-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e71c5-144">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e71c5-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e71c5-145">輸入</span><span class="sxs-lookup"><span data-stu-id="e71c5-145">INPUTS</span></span>

### <span data-ttu-id="e71c5-146">System.object</span><span class="sxs-lookup"><span data-stu-id="e71c5-146">System.String</span></span>

### <span data-ttu-id="e71c5-147">PSRemediation 中的 PolicyInsights。</span><span class="sxs-lookup"><span data-stu-id="e71c5-147">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span></span>

## <span data-ttu-id="e71c5-148">輸出</span><span class="sxs-lookup"><span data-stu-id="e71c5-148">OUTPUTS</span></span>

### <span data-ttu-id="e71c5-149">System.object</span><span class="sxs-lookup"><span data-stu-id="e71c5-149">System.Boolean</span></span>

## <span data-ttu-id="e71c5-150">筆記</span><span class="sxs-lookup"><span data-stu-id="e71c5-150">NOTES</span></span>

## <span data-ttu-id="e71c5-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="e71c5-151">RELATED LINKS</span></span>
