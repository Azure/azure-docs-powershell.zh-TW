---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 9B0BBBB4-A7A0-4243-9264-362A00F5B399
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationhybridworkergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationHybridWorkerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationHybridWorkerGroup.md
ms.openlocfilehash: 89c1b96744ce67765bed53f850e21a457ead4b6b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913617"
---
# <span data-ttu-id="6efc1-101">Get-AzAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="6efc1-101">Get-AzAutomationHybridWorkerGroup</span></span>

## <span data-ttu-id="6efc1-102">簡介</span><span class="sxs-lookup"><span data-stu-id="6efc1-102">SYNOPSIS</span></span>
<span data-ttu-id="6efc1-103">獲得混合式 runbook 員工群組。</span><span class="sxs-lookup"><span data-stu-id="6efc1-103">Gets hybrid runbook worker groups.</span></span>

## <span data-ttu-id="6efc1-104">語法</span><span class="sxs-lookup"><span data-stu-id="6efc1-104">SYNTAX</span></span>

### <span data-ttu-id="6efc1-105">根據預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="6efc1-105">ByAll (Default)</span></span>
```
Get-AzAutomationHybridWorkerGroup [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6efc1-106">ByName</span><span class="sxs-lookup"><span data-stu-id="6efc1-106">ByName</span></span>
```
Get-AzAutomationHybridWorkerGroup [[-Name] <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6efc1-107">描述</span><span class="sxs-lookup"><span data-stu-id="6efc1-107">DESCRIPTION</span></span>
<span data-ttu-id="6efc1-108">**Get-AzAutomationHybridWorkerGroup** Cmdlet 會取得 Azure Automation 混合式 runbook 工作群組。</span><span class="sxs-lookup"><span data-stu-id="6efc1-108">The **Get-AzAutomationHybridWorkerGroup** cmdlet gets Azure Automation hybrid runbook worker groups.</span></span>
<span data-ttu-id="6efc1-109">若要取得特定群組，請指定其名稱。</span><span class="sxs-lookup"><span data-stu-id="6efc1-109">To get a specific group, specify its name.</span></span>

## <span data-ttu-id="6efc1-110">例子</span><span class="sxs-lookup"><span data-stu-id="6efc1-110">EXAMPLES</span></span>

### <span data-ttu-id="6efc1-111">範例 1：取得所有混合式 runbook worker 群組</span><span class="sxs-lookup"><span data-stu-id="6efc1-111">Example 1: Get all hybrid runbook worker groups</span></span>
```
PS C:\>Get-AzAutomationHybridWorkerGroup -ResourceGroupName "ResourceGroupName01" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="6efc1-112">此命令會獲得自動化帳戶中名為 Contoso17 的所有混合式 runbook 員工群組。</span><span class="sxs-lookup"><span data-stu-id="6efc1-112">This command gets all hybrid runbook worker groups in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="6efc1-113">範例 2：取得單一混合式 runbook worker 群組</span><span class="sxs-lookup"><span data-stu-id="6efc1-113">Example 2: Get a single hybrid runbook worker group</span></span>
```
PS C:\>Get-AzAutomationHybridWorkerGroup -ResourceGroupName "ResourceGroupName01" -AutomationAccountName "Contoso17" -Name "HybridRunbookWorkerGroup01"
```

<span data-ttu-id="6efc1-114">此命令會獲得名為 Contoso17 的自動化帳戶中名為 HybridRunbookWorkerGroup01 的混合式 runbook 員工群組。</span><span class="sxs-lookup"><span data-stu-id="6efc1-114">This command gets the hybrid runbook worker group named HybridRunbookWorkerGroup01 in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="6efc1-115">範例 3：取得混合式 runbook worker 群組中的工作人員</span><span class="sxs-lookup"><span data-stu-id="6efc1-115">Example 3: Get the workers in a hybrid runbook worker group</span></span>
```
PS C:\>(Get-AzAutomationHybridWorker -ResourceGroupName ResourceGroupName01 -AutomationAccountName Contoso17 -Name "HybridRunbookWorkerGroup01" ).RunbookWorker
```

<span data-ttu-id="6efc1-116">此命令會獲得名為 Contoso17 之自動化帳戶中名為 HybridRunbookWorkerGroup01 的混合式 runbook 員工群組中的混合式 runbook 工作人員。</span><span class="sxs-lookup"><span data-stu-id="6efc1-116">This command gets the hybrid runbook workers in the hybrid runbook worker group named HybridRunbookWorkerGroup01 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="6efc1-117">參數</span><span class="sxs-lookup"><span data-stu-id="6efc1-117">PARAMETERS</span></span>

### <span data-ttu-id="6efc1-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="6efc1-118">-AutomationAccountName</span></span>
<span data-ttu-id="6efc1-119">指定自動化帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="6efc1-119">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="6efc1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6efc1-120">-DefaultProfile</span></span>
<span data-ttu-id="6efc1-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="6efc1-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6efc1-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="6efc1-122">-Name</span></span>
<span data-ttu-id="6efc1-123">指定混合式 runbook 員工組名。</span><span class="sxs-lookup"><span data-stu-id="6efc1-123">Specifies the hybrid runbook worker group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: Group

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6efc1-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6efc1-124">-ResourceGroupName</span></span>
<span data-ttu-id="6efc1-125">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6efc1-125">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="6efc1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6efc1-126">CommonParameters</span></span>
<span data-ttu-id="6efc1-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="6efc1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6efc1-128">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="6efc1-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6efc1-129">輸入</span><span class="sxs-lookup"><span data-stu-id="6efc1-129">INPUTS</span></span>

### <span data-ttu-id="6efc1-130">System.String</span><span class="sxs-lookup"><span data-stu-id="6efc1-130">System.String</span></span>

## <span data-ttu-id="6efc1-131">輸出</span><span class="sxs-lookup"><span data-stu-id="6efc1-131">OUTPUTS</span></span>

### <span data-ttu-id="6efc1-132">Microsoft.Azure.Commands.Automation.Model.HybridRunbookWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="6efc1-132">Microsoft.Azure.Commands.Automation.Model.HybridRunbookWorkerGroup</span></span>

## <span data-ttu-id="6efc1-133">筆記</span><span class="sxs-lookup"><span data-stu-id="6efc1-133">NOTES</span></span>

## <span data-ttu-id="6efc1-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="6efc1-134">RELATED LINKS</span></span>
