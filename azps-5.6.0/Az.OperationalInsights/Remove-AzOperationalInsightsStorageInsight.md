---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 92261663-CF50-4EBD-85D2-C2E254F39B41
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/remove-azoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsStorageInsight.md
ms.openlocfilehash: 7eece12130095889c5da574a4d0a3ec8d0b0bed2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911557"
---
# <span data-ttu-id="f3d1b-101">Remove-AzOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="f3d1b-101">Remove-AzOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="f3d1b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f3d1b-102">SYNOPSIS</span></span>
<span data-ttu-id="f3d1b-103">移除儲存深入資訊。</span><span class="sxs-lookup"><span data-stu-id="f3d1b-103">Removes a Storage Insight.</span></span>

## <span data-ttu-id="f3d1b-104">語法</span><span class="sxs-lookup"><span data-stu-id="f3d1b-104">SYNTAX</span></span>

### <span data-ttu-id="f3d1b-105">ByWorkspaceName (預設) </span><span class="sxs-lookup"><span data-stu-id="f3d1b-105">ByWorkspaceName (Default)</span></span>
```
Remove-AzOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3d1b-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="f3d1b-106">ByWorkspaceObject</span></span>
```
Remove-AzOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f3d1b-107">描述</span><span class="sxs-lookup"><span data-stu-id="f3d1b-107">DESCRIPTION</span></span>
<span data-ttu-id="f3d1b-108">**Remove-AzOperationalInsightsStorageInsight** Cmdlet 會從工作區刪除儲存深入資訊。</span><span class="sxs-lookup"><span data-stu-id="f3d1b-108">The **Remove-AzOperationalInsightsStorageInsight** cmdlet deletes a Storage Insight from a workspace.</span></span>

## <span data-ttu-id="f3d1b-109">例子</span><span class="sxs-lookup"><span data-stu-id="f3d1b-109">EXAMPLES</span></span>

### <span data-ttu-id="f3d1b-110">範例 1：移除儲存空間深入資訊</span><span class="sxs-lookup"><span data-stu-id="f3d1b-110">Example 1: Remove a Storage Insight by name</span></span>
```
PS C:\>Remove-AzOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -Name "MyStorageInsight"
```

<span data-ttu-id="f3d1b-111">此命令會從指定資源群組中名為 MyWorkspace 的工作區移除名為 MyStorageInsight 的儲存深入資訊。</span><span class="sxs-lookup"><span data-stu-id="f3d1b-111">This command removes the Storage Insight named MyStorageInsight from the workspace named MyWorkspace in the specified resource group.</span></span>
<span data-ttu-id="f3d1b-112">命令不會指定 *Force* 參數，因此會先提示您確認，然後再移除儲存深入資訊。</span><span class="sxs-lookup"><span data-stu-id="f3d1b-112">The command does not specify the *Force* parameter, so it prompts you for confirmation before removing the Storage Insight.</span></span>

### <span data-ttu-id="f3d1b-113">範例 2：移除儲存深入資訊而不確認</span><span class="sxs-lookup"><span data-stu-id="f3d1b-113">Example 2: Remove a Storage Insight without confirmation</span></span>
```
PS C:\>$Workspace = Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"

PS C:\>Remove-AzOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight" -Force
```

<span data-ttu-id="f3d1b-114">第一個命令使用 Get-AzOperationalInsightsWorkspace Cmdlet 取得名為 MyWorkspace 的工作區，然後將它儲存在 $Workspace 變數中。第二個命令會從 $Workspace移除名為 MyStorageInsight 的儲存深入資訊，而不會提示您確認。</span><span class="sxs-lookup"><span data-stu-id="f3d1b-114">The first command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then stores it in the $Workspace variable.The second command removes the storage insight named MyStorageInsight from $Workspace without prompting you for confirmation.</span></span>

## <span data-ttu-id="f3d1b-115">參數</span><span class="sxs-lookup"><span data-stu-id="f3d1b-115">PARAMETERS</span></span>

### <span data-ttu-id="f3d1b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3d1b-116">-DefaultProfile</span></span>
<span data-ttu-id="f3d1b-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="f3d1b-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f3d1b-118">-強制</span><span class="sxs-lookup"><span data-stu-id="f3d1b-118">-Force</span></span>
<span data-ttu-id="f3d1b-119">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="f3d1b-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f3d1b-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="f3d1b-120">-Name</span></span>
<span data-ttu-id="f3d1b-121">指定儲存深入資訊的名稱。</span><span class="sxs-lookup"><span data-stu-id="f3d1b-121">Specifies the name of the Storage Insight.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3d1b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3d1b-122">-ResourceGroupName</span></span>
<span data-ttu-id="f3d1b-123">指定 Azure 資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f3d1b-123">Specifies the name of an Azure resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3d1b-124">-工作區</span><span class="sxs-lookup"><span data-stu-id="f3d1b-124">-Workspace</span></span>
<span data-ttu-id="f3d1b-125">指定包含儲存深入資訊工作區。</span><span class="sxs-lookup"><span data-stu-id="f3d1b-125">Specifies the workspace that contains the Storage Insight.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f3d1b-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f3d1b-126">-WorkspaceName</span></span>
<span data-ttu-id="f3d1b-127">指定包含儲存深入資訊之工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="f3d1b-127">Specifies the name of the workspace that contains the Storage Insight.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3d1b-128">-確認</span><span class="sxs-lookup"><span data-stu-id="f3d1b-128">-Confirm</span></span>
<span data-ttu-id="f3d1b-129">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="f3d1b-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3d1b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3d1b-130">-WhatIf</span></span>
<span data-ttu-id="f3d1b-131">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f3d1b-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3d1b-132">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f3d1b-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3d1b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3d1b-133">CommonParameters</span></span>
<span data-ttu-id="f3d1b-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f3d1b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3d1b-135">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="f3d1b-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3d1b-136">輸入</span><span class="sxs-lookup"><span data-stu-id="f3d1b-136">INPUTS</span></span>

### <span data-ttu-id="f3d1b-137">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="f3d1b-137">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="f3d1b-138">System.String</span><span class="sxs-lookup"><span data-stu-id="f3d1b-138">System.String</span></span>

## <span data-ttu-id="f3d1b-139">輸出</span><span class="sxs-lookup"><span data-stu-id="f3d1b-139">OUTPUTS</span></span>

### <span data-ttu-id="f3d1b-140">System.Void</span><span class="sxs-lookup"><span data-stu-id="f3d1b-140">System.Void</span></span>

## <span data-ttu-id="f3d1b-141">筆記</span><span class="sxs-lookup"><span data-stu-id="f3d1b-141">NOTES</span></span>

## <span data-ttu-id="f3d1b-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="f3d1b-142">RELATED LINKS</span></span>

[<span data-ttu-id="f3d1b-143">Azure 營運深入資訊 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f3d1b-143">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="f3d1b-144">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="f3d1b-144">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


