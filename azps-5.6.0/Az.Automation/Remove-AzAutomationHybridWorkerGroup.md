---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/powershell/module/az.automation/remove-azautomationhybridworkergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationHybridWorkerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationHybridWorkerGroup.md
ms.openlocfilehash: 35ef4a5629726b33a8d9099da78134e6a0bac8b7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916668"
---
# <span data-ttu-id="41f29-101">Remove-AzAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="41f29-101">Remove-AzAutomationHybridWorkerGroup</span></span>

## <span data-ttu-id="41f29-102">簡介</span><span class="sxs-lookup"><span data-stu-id="41f29-102">SYNOPSIS</span></span>
<span data-ttu-id="41f29-103">從自動化移除混合式員工群組。</span><span class="sxs-lookup"><span data-stu-id="41f29-103">Removes hybrid worker group from Automation.</span></span>

## <span data-ttu-id="41f29-104">語法</span><span class="sxs-lookup"><span data-stu-id="41f29-104">SYNTAX</span></span>

```
Remove-AzAutomationHybridWorkerGroup [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="41f29-105">描述</span><span class="sxs-lookup"><span data-stu-id="41f29-105">DESCRIPTION</span></span>
<span data-ttu-id="41f29-106">Cmdlet Remove-AzAutomationHybridWorkerGroup從自動化移除混合式員工群組。</span><span class="sxs-lookup"><span data-stu-id="41f29-106">The Remove-AzAutomationHybridWorkerGroup cmdlet removes a hybrid worker group from Automation.</span></span>

## <span data-ttu-id="41f29-107">例子</span><span class="sxs-lookup"><span data-stu-id="41f29-107">EXAMPLES</span></span>

### <span data-ttu-id="41f29-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="41f29-108">Example 1</span></span>
<span data-ttu-id="41f29-109">此命令會按名稱移除混合式員工。</span><span class="sxs-lookup"><span data-stu-id="41f29-109">This command removes a hybrid worker by name.</span></span>

```powershell
PS C:\> Remove-AzAutomationHybridWorkerGroup -ResourceGroupName "rg1" `
                                                  -AutomationAccountName "devAccount" `
                                                  -Name "GroupName" `
                                                  -Force
```

## <span data-ttu-id="41f29-110">參數</span><span class="sxs-lookup"><span data-stu-id="41f29-110">PARAMETERS</span></span>

### <span data-ttu-id="41f29-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="41f29-111">-AutomationAccountName</span></span>
<span data-ttu-id="41f29-112">自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="41f29-112">The automation account name.</span></span>

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

### <span data-ttu-id="41f29-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41f29-113">-DefaultProfile</span></span>
<span data-ttu-id="41f29-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="41f29-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41f29-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="41f29-115">-Name</span></span>
<span data-ttu-id="41f29-116">混合式員工組名。</span><span class="sxs-lookup"><span data-stu-id="41f29-116">The hybrid worker group name.</span></span>

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

### <span data-ttu-id="41f29-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41f29-117">-ResourceGroupName</span></span>
<span data-ttu-id="41f29-118">資源組名。</span><span class="sxs-lookup"><span data-stu-id="41f29-118">The resource group name.</span></span>

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

### <span data-ttu-id="41f29-119">-確認</span><span class="sxs-lookup"><span data-stu-id="41f29-119">-Confirm</span></span>
<span data-ttu-id="41f29-120">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="41f29-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41f29-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41f29-121">-WhatIf</span></span>
<span data-ttu-id="41f29-122">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="41f29-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41f29-123">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="41f29-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41f29-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41f29-124">CommonParameters</span></span>
<span data-ttu-id="41f29-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="41f29-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41f29-126">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="41f29-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41f29-127">輸入</span><span class="sxs-lookup"><span data-stu-id="41f29-127">INPUTS</span></span>

### <span data-ttu-id="41f29-128">System.String</span><span class="sxs-lookup"><span data-stu-id="41f29-128">System.String</span></span>

## <span data-ttu-id="41f29-129">輸出</span><span class="sxs-lookup"><span data-stu-id="41f29-129">OUTPUTS</span></span>

### <span data-ttu-id="41f29-130">System.Void</span><span class="sxs-lookup"><span data-stu-id="41f29-130">System.Void</span></span>

## <span data-ttu-id="41f29-131">筆記</span><span class="sxs-lookup"><span data-stu-id="41f29-131">NOTES</span></span>

## <span data-ttu-id="41f29-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="41f29-132">RELATED LINKS</span></span>
