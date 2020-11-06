---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 92261663-CF50-4EBD-85D2-C2E254F39B41
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/remove-azurermoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Remove-AzureRmOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Remove-AzureRmOperationalInsightsStorageInsight.md
ms.openlocfilehash: 726386fb4a455b3daab314e5f61d33122592dcf8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448986"
---
# <span data-ttu-id="88394-101">Remove-AzureRmOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="88394-101">Remove-AzureRmOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="88394-102">摘要</span><span class="sxs-lookup"><span data-stu-id="88394-102">SYNOPSIS</span></span>
<span data-ttu-id="88394-103">移除儲存空間洞察力。</span><span class="sxs-lookup"><span data-stu-id="88394-103">Removes a Storage Insight.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="88394-104">句法</span><span class="sxs-lookup"><span data-stu-id="88394-104">SYNTAX</span></span>

### <span data-ttu-id="88394-105">ByWorkspaceName (預設) </span><span class="sxs-lookup"><span data-stu-id="88394-105">ByWorkspaceName (Default)</span></span>
```
Remove-AzureRmOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88394-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="88394-106">ByWorkspaceObject</span></span>
```
Remove-AzureRmOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88394-107">說明</span><span class="sxs-lookup"><span data-stu-id="88394-107">DESCRIPTION</span></span>
<span data-ttu-id="88394-108">**AzureRmOperationalInsightsStorageInsight** Cmdlet 會從工作區刪除儲存空間洞察力。</span><span class="sxs-lookup"><span data-stu-id="88394-108">The **Remove-AzureRmOperationalInsightsStorageInsight** cmdlet deletes a Storage Insight from a workspace.</span></span>

## <span data-ttu-id="88394-109">示例</span><span class="sxs-lookup"><span data-stu-id="88394-109">EXAMPLES</span></span>

### <span data-ttu-id="88394-110">範例1：移除依名稱的儲存空間洞察力</span><span class="sxs-lookup"><span data-stu-id="88394-110">Example 1: Remove a Storage Insight by name</span></span>
```
PS C:\>Remove-AzureRmOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -Name "MyStorageInsight"
```

<span data-ttu-id="88394-111">這個命令會從指定資源群組中名為 MyWorkspace 的工作區，移除名為 MyStorageInsight 的儲存空間洞察力。</span><span class="sxs-lookup"><span data-stu-id="88394-111">This command removes the Storage Insight named MyStorageInsight from the workspace named MyWorkspace in the specified resource group.</span></span>
<span data-ttu-id="88394-112">此命令不會指定 *Force* 參數，因此它會在您移除儲存空間洞察力之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="88394-112">The command does not specify the *Force* parameter, so it prompts you for confirmation before removing the Storage Insight.</span></span>

### <span data-ttu-id="88394-113">範例2：移除儲存空間洞察力而不需確認</span><span class="sxs-lookup"><span data-stu-id="88394-113">Example 2: Remove a Storage Insight without confirmation</span></span>
```
PS C:\>$Workspace = Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"

PS C:\>Remove-AzureRmOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight" -Force
```

<span data-ttu-id="88394-114">第一個命令使用 Get-AzureRmOperationalInsightsWorkspace Cmdlet 來取得名為 MyWorkspace 的工作區，然後將它儲存在 $Workspace 變數中。第二個命令會從 $Workspace 移除名為 MyStorageInsight 的儲存空間洞察力，而不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="88394-114">The first command uses the Get-AzureRmOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then stores it in the $Workspace variable.The second command removes the storage insight named MyStorageInsight from $Workspace without prompting you for confirmation.</span></span>

## <span data-ttu-id="88394-115">參數</span><span class="sxs-lookup"><span data-stu-id="88394-115">PARAMETERS</span></span>

### <span data-ttu-id="88394-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88394-116">-DefaultProfile</span></span>
<span data-ttu-id="88394-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="88394-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="88394-118">-Force</span><span class="sxs-lookup"><span data-stu-id="88394-118">-Force</span></span>
<span data-ttu-id="88394-119">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="88394-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="88394-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="88394-120">-Name</span></span>
<span data-ttu-id="88394-121">指定儲存空間洞察力的名稱。</span><span class="sxs-lookup"><span data-stu-id="88394-121">Specifies the name of the Storage Insight.</span></span>

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

### <span data-ttu-id="88394-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88394-122">-ResourceGroupName</span></span>
<span data-ttu-id="88394-123">指定 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="88394-123">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="88394-124">-工作區</span><span class="sxs-lookup"><span data-stu-id="88394-124">-Workspace</span></span>
<span data-ttu-id="88394-125">指定包含儲存空間洞察力的工作區。</span><span class="sxs-lookup"><span data-stu-id="88394-125">Specifies the workspace that contains the Storage Insight.</span></span>

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

### <span data-ttu-id="88394-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="88394-126">-WorkspaceName</span></span>
<span data-ttu-id="88394-127">指定包含儲存空間洞察力的工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="88394-127">Specifies the name of the workspace that contains the Storage Insight.</span></span>

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

### <span data-ttu-id="88394-128">-確認</span><span class="sxs-lookup"><span data-stu-id="88394-128">-Confirm</span></span>
<span data-ttu-id="88394-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="88394-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88394-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88394-130">-WhatIf</span></span>
<span data-ttu-id="88394-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="88394-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88394-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="88394-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88394-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88394-133">CommonParameters</span></span>
<span data-ttu-id="88394-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="88394-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88394-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="88394-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88394-136">輸入</span><span class="sxs-lookup"><span data-stu-id="88394-136">INPUTS</span></span>

### <span data-ttu-id="88394-137">PSWorkspace 中的 OperationalInsights。</span><span class="sxs-lookup"><span data-stu-id="88394-137">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>
<span data-ttu-id="88394-138">參數：工作區 (ByValue) </span><span class="sxs-lookup"><span data-stu-id="88394-138">Parameters: Workspace (ByValue)</span></span>

### <span data-ttu-id="88394-139">System.object</span><span class="sxs-lookup"><span data-stu-id="88394-139">System.String</span></span>

## <span data-ttu-id="88394-140">輸出</span><span class="sxs-lookup"><span data-stu-id="88394-140">OUTPUTS</span></span>

### <span data-ttu-id="88394-141">System.void</span><span class="sxs-lookup"><span data-stu-id="88394-141">System.Void</span></span>

## <span data-ttu-id="88394-142">筆記</span><span class="sxs-lookup"><span data-stu-id="88394-142">NOTES</span></span>

## <span data-ttu-id="88394-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="88394-143">RELATED LINKS</span></span>

[<span data-ttu-id="88394-144">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="88394-144">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="88394-145">AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="88394-145">Get-AzureRmOperationalInsightsWorkspace</span></span>](./Get-AzureRmOperationalInsightsWorkspace.md)


