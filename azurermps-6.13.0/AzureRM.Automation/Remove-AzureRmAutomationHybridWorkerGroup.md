---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationdscnodeconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationHybridWorkerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationHybridWorkerGroup.md
ms.openlocfilehash: b6f15bc55c2e9f9a05e60e7e6f2c139ddbb70454
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623770"
---
# <span data-ttu-id="a4a99-101">Remove-AzureRmAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="a4a99-101">Remove-AzureRmAutomationHybridWorkerGroup</span></span>

## <span data-ttu-id="a4a99-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a4a99-102">SYNOPSIS</span></span>
<span data-ttu-id="a4a99-103">從 [自動化] 移除混合式輔助角色群組。</span><span class="sxs-lookup"><span data-stu-id="a4a99-103">Removes hybrid worker group from Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a4a99-104">句法</span><span class="sxs-lookup"><span data-stu-id="a4a99-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationHybridWorkerGroup [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a4a99-105">說明</span><span class="sxs-lookup"><span data-stu-id="a4a99-105">DESCRIPTION</span></span>
<span data-ttu-id="a4a99-106">Remove-AzureRmAutomationHybridWorkerGroup Cmdlet 會將混合式輔助角色群組從 [自動化] 中移除。</span><span class="sxs-lookup"><span data-stu-id="a4a99-106">The Remove-AzureRmAutomationHybridWorkerGroup cmdlet removes a hybrid worker group from Automation.</span></span>

## <span data-ttu-id="a4a99-107">示例</span><span class="sxs-lookup"><span data-stu-id="a4a99-107">EXAMPLES</span></span>

### <span data-ttu-id="a4a99-108">範例1</span><span class="sxs-lookup"><span data-stu-id="a4a99-108">Example 1</span></span>
<span data-ttu-id="a4a99-109">這個命令會依名稱移除混合式輔助角色。</span><span class="sxs-lookup"><span data-stu-id="a4a99-109">This command removes a hybrid worker by name.</span></span>

```powershell
PS C:\> Remove-AzureRmAutomationHybridWorkerGroup -ResourceGroupName "rg1" `
                                                  -AutomationAccountName "devAccount" `
                                                  -Name "GroupName" `
                                                  -Force
```

## <span data-ttu-id="a4a99-110">參數</span><span class="sxs-lookup"><span data-stu-id="a4a99-110">PARAMETERS</span></span>

### <span data-ttu-id="a4a99-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a4a99-111">-AutomationAccountName</span></span>
<span data-ttu-id="a4a99-112">自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="a4a99-112">The automation account name.</span></span>

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

### <span data-ttu-id="a4a99-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4a99-113">-DefaultProfile</span></span>
<span data-ttu-id="a4a99-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a4a99-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4a99-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="a4a99-115">-Name</span></span>
<span data-ttu-id="a4a99-116">混合式輔助角色組名稱。</span><span class="sxs-lookup"><span data-stu-id="a4a99-116">The hybrid worker group name.</span></span>

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

### <span data-ttu-id="a4a99-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4a99-117">-ResourceGroupName</span></span>
<span data-ttu-id="a4a99-118">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a4a99-118">The resource group name.</span></span>

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

### <span data-ttu-id="a4a99-119">-確認</span><span class="sxs-lookup"><span data-stu-id="a4a99-119">-Confirm</span></span>
<span data-ttu-id="a4a99-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a4a99-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4a99-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4a99-121">-WhatIf</span></span>
<span data-ttu-id="a4a99-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a4a99-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4a99-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a4a99-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4a99-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4a99-124">CommonParameters</span></span>
<span data-ttu-id="a4a99-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a4a99-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4a99-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a4a99-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4a99-127">輸入</span><span class="sxs-lookup"><span data-stu-id="a4a99-127">INPUTS</span></span>

### <span data-ttu-id="a4a99-128">System.object</span><span class="sxs-lookup"><span data-stu-id="a4a99-128">System.String</span></span>

## <span data-ttu-id="a4a99-129">輸出</span><span class="sxs-lookup"><span data-stu-id="a4a99-129">OUTPUTS</span></span>

### <span data-ttu-id="a4a99-130">System.void</span><span class="sxs-lookup"><span data-stu-id="a4a99-130">System.Void</span></span>

## <span data-ttu-id="a4a99-131">筆記</span><span class="sxs-lookup"><span data-stu-id="a4a99-131">NOTES</span></span>

## <span data-ttu-id="a4a99-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="a4a99-132">RELATED LINKS</span></span>
