---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationhybridworkergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationHybridWorkerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationHybridWorkerGroup.md
ms.openlocfilehash: 78674e3245da1b8a58e099948bff23df9159efec
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93966372"
---
# <span data-ttu-id="ba629-101">Remove-AzAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="ba629-101">Remove-AzAutomationHybridWorkerGroup</span></span>

## <span data-ttu-id="ba629-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ba629-102">SYNOPSIS</span></span>
<span data-ttu-id="ba629-103">從 [自動化] 移除混合式輔助角色群組。</span><span class="sxs-lookup"><span data-stu-id="ba629-103">Removes hybrid worker group from Automation.</span></span>

## <span data-ttu-id="ba629-104">句法</span><span class="sxs-lookup"><span data-stu-id="ba629-104">SYNTAX</span></span>

```
Remove-AzAutomationHybridWorkerGroup [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ba629-105">說明</span><span class="sxs-lookup"><span data-stu-id="ba629-105">DESCRIPTION</span></span>
<span data-ttu-id="ba629-106">Remove-AzAutomationHybridWorkerGroup Cmdlet 會將混合式輔助角色群組從 [自動化] 中移除。</span><span class="sxs-lookup"><span data-stu-id="ba629-106">The Remove-AzAutomationHybridWorkerGroup cmdlet removes a hybrid worker group from Automation.</span></span>

## <span data-ttu-id="ba629-107">示例</span><span class="sxs-lookup"><span data-stu-id="ba629-107">EXAMPLES</span></span>

### <span data-ttu-id="ba629-108">範例1</span><span class="sxs-lookup"><span data-stu-id="ba629-108">Example 1</span></span>
<span data-ttu-id="ba629-109">這個命令會依名稱移除混合式輔助角色。</span><span class="sxs-lookup"><span data-stu-id="ba629-109">This command removes a hybrid worker by name.</span></span>

```powershell
PS C:\> Remove-AzAutomationHybridWorkerGroup -ResourceGroupName "rg1" `
                                                  -AutomationAccountName "devAccount" `
                                                  -Name "GroupName" `
                                                  -Force
```

## <span data-ttu-id="ba629-110">參數</span><span class="sxs-lookup"><span data-stu-id="ba629-110">PARAMETERS</span></span>

### <span data-ttu-id="ba629-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ba629-111">-AutomationAccountName</span></span>
<span data-ttu-id="ba629-112">自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="ba629-112">The automation account name.</span></span>

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

### <span data-ttu-id="ba629-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba629-113">-DefaultProfile</span></span>
<span data-ttu-id="ba629-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ba629-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ba629-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="ba629-115">-Name</span></span>
<span data-ttu-id="ba629-116">混合式輔助角色組名稱。</span><span class="sxs-lookup"><span data-stu-id="ba629-116">The hybrid worker group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Group

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba629-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba629-117">-ResourceGroupName</span></span>
<span data-ttu-id="ba629-118">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ba629-118">The resource group name.</span></span>

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

### <span data-ttu-id="ba629-119">-確認</span><span class="sxs-lookup"><span data-stu-id="ba629-119">-Confirm</span></span>
<span data-ttu-id="ba629-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ba629-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba629-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba629-121">-WhatIf</span></span>
<span data-ttu-id="ba629-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ba629-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba629-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ba629-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba629-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba629-124">CommonParameters</span></span>
<span data-ttu-id="ba629-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ba629-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba629-126">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ba629-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba629-127">輸入</span><span class="sxs-lookup"><span data-stu-id="ba629-127">INPUTS</span></span>

### <span data-ttu-id="ba629-128">System.object</span><span class="sxs-lookup"><span data-stu-id="ba629-128">System.String</span></span>

## <span data-ttu-id="ba629-129">輸出</span><span class="sxs-lookup"><span data-stu-id="ba629-129">OUTPUTS</span></span>

### <span data-ttu-id="ba629-130">System.void</span><span class="sxs-lookup"><span data-stu-id="ba629-130">System.Void</span></span>

## <span data-ttu-id="ba629-131">筆記</span><span class="sxs-lookup"><span data-stu-id="ba629-131">NOTES</span></span>

## <span data-ttu-id="ba629-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="ba629-132">RELATED LINKS</span></span>
