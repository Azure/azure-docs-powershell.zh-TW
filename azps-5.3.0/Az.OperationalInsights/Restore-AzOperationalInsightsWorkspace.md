---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/restore-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Restore-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Restore-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: 01354106e3d6ad9fbe33c97f6bcd774c62be7ccf
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98436282"
---
# <span data-ttu-id="44027-101">Restore-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="44027-101">Restore-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="44027-102">摘要</span><span class="sxs-lookup"><span data-stu-id="44027-102">SYNOPSIS</span></span>
<span data-ttu-id="44027-103">還原已刪除的工作區。</span><span class="sxs-lookup"><span data-stu-id="44027-103">Restore a deleted workspace.</span></span>

## <span data-ttu-id="44027-104">句法</span><span class="sxs-lookup"><span data-stu-id="44027-104">SYNTAX</span></span>

```
Restore-AzOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="44027-105">說明</span><span class="sxs-lookup"><span data-stu-id="44027-105">DESCRIPTION</span></span>
<span data-ttu-id="44027-106">還原已刪除的工作區。</span><span class="sxs-lookup"><span data-stu-id="44027-106">Restore a deleted workspace.</span></span>

## <span data-ttu-id="44027-107">示例</span><span class="sxs-lookup"><span data-stu-id="44027-107">EXAMPLES</span></span>

### <span data-ttu-id="44027-108">範例1</span><span class="sxs-lookup"><span data-stu-id="44027-108">Example 1</span></span>
```powershell
PS C:\> $workspace = New-AzOperationalInsightsWorkspace -ResourceGroupName $rgname -Name $wsname -Location $wslocation
PS C:\> $workspace | Remove-AzOperationalInsightsWorkspace
PS C:\> $workspace = Restore-AzOperationalInsightsWorkspace -ResourceGroupName $rgname -Name $wsname -Location $wslocation
```

<span data-ttu-id="44027-109">還原已刪除的工作區。</span><span class="sxs-lookup"><span data-stu-id="44027-109">Restore deleted workspace.</span></span>

## <span data-ttu-id="44027-110">參數</span><span class="sxs-lookup"><span data-stu-id="44027-110">PARAMETERS</span></span>

### <span data-ttu-id="44027-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44027-111">-DefaultProfile</span></span>
<span data-ttu-id="44027-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="44027-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44027-113">-Force</span><span class="sxs-lookup"><span data-stu-id="44027-113">-Force</span></span>
<span data-ttu-id="44027-114">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="44027-114">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="44027-115">-位置</span><span class="sxs-lookup"><span data-stu-id="44027-115">-Location</span></span>
<span data-ttu-id="44027-116">要在其中建立工作區的地理區域。</span><span class="sxs-lookup"><span data-stu-id="44027-116">The geographic region that the workspace will be created in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44027-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="44027-117">-Name</span></span>
<span data-ttu-id="44027-118">工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="44027-118">The workspace name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44027-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44027-119">-ResourceGroupName</span></span>
<span data-ttu-id="44027-120">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="44027-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44027-121">-確認</span><span class="sxs-lookup"><span data-stu-id="44027-121">-Confirm</span></span>
<span data-ttu-id="44027-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="44027-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44027-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44027-123">-WhatIf</span></span>
<span data-ttu-id="44027-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="44027-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="44027-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="44027-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44027-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44027-126">CommonParameters</span></span>
<span data-ttu-id="44027-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="44027-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44027-128">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="44027-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44027-129">輸入</span><span class="sxs-lookup"><span data-stu-id="44027-129">INPUTS</span></span>

### <span data-ttu-id="44027-130">System.object</span><span class="sxs-lookup"><span data-stu-id="44027-130">System.String</span></span>

## <span data-ttu-id="44027-131">輸出</span><span class="sxs-lookup"><span data-stu-id="44027-131">OUTPUTS</span></span>

### <span data-ttu-id="44027-132">PSWorkspace 中的 OperationalInsights。</span><span class="sxs-lookup"><span data-stu-id="44027-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="44027-133">筆記</span><span class="sxs-lookup"><span data-stu-id="44027-133">NOTES</span></span>

## <span data-ttu-id="44027-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="44027-134">RELATED LINKS</span></span>
