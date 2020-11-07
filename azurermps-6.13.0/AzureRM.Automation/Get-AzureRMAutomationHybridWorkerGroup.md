---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 9B0BBBB4-A7A0-4243-9264-362A00F5B399
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationhybridworkergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationHybridWorkerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationHybridWorkerGroup.md
ms.openlocfilehash: 8fe4c554fd781d198af6bea784a433c141c2d41d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625365"
---
# <span data-ttu-id="c7acd-101">Get-AzureRmAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="c7acd-101">Get-AzureRmAutomationHybridWorkerGroup</span></span>

## <span data-ttu-id="c7acd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c7acd-102">SYNOPSIS</span></span>
<span data-ttu-id="c7acd-103">取得混合式 runbook 輔助角色群組。</span><span class="sxs-lookup"><span data-stu-id="c7acd-103">Gets hybrid runbook worker groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c7acd-104">句法</span><span class="sxs-lookup"><span data-stu-id="c7acd-104">SYNTAX</span></span>

### <span data-ttu-id="c7acd-105">ByAll (預設) </span><span class="sxs-lookup"><span data-stu-id="c7acd-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationHybridWorkerGroup [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c7acd-106">ByName</span><span class="sxs-lookup"><span data-stu-id="c7acd-106">ByName</span></span>
```
Get-AzureRmAutomationHybridWorkerGroup [[-Name] <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c7acd-107">說明</span><span class="sxs-lookup"><span data-stu-id="c7acd-107">DESCRIPTION</span></span>
<span data-ttu-id="c7acd-108">**AzureRmAutomationHybridWorkerGroup** Cmdlet 會取得 Azure 自動化混合式 runbook 輔助角色群組。</span><span class="sxs-lookup"><span data-stu-id="c7acd-108">The **Get-AzureRmAutomationHybridWorkerGroup** cmdlet gets Azure Automation hybrid runbook worker groups.</span></span>
<span data-ttu-id="c7acd-109">若要取得特定群組，請指定其名稱。</span><span class="sxs-lookup"><span data-stu-id="c7acd-109">To get a specific group, specify its name.</span></span>

## <span data-ttu-id="c7acd-110">示例</span><span class="sxs-lookup"><span data-stu-id="c7acd-110">EXAMPLES</span></span>

### <span data-ttu-id="c7acd-111">範例1：取得所有混合式 runbook 輔助角色群組</span><span class="sxs-lookup"><span data-stu-id="c7acd-111">Example 1: Get all hybrid runbook worker groups</span></span>
```
PS C:\>Get-AzureRMAutomationHybridWorkerGroup -ResourceGroupName "ResourceGroupName01" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="c7acd-112">這個命令會在自動化帳戶（名為 Contoso17）中取得所有混合式 runbook worker 群組。</span><span class="sxs-lookup"><span data-stu-id="c7acd-112">This command gets all hybrid runbook worker groups in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="c7acd-113">範例2：取得單一混合式 runbook 輔助角色群組</span><span class="sxs-lookup"><span data-stu-id="c7acd-113">Example 2: Get a single hybrid runbook worker group</span></span>
```
PS C:\>Get-AzureRMAutomationHybridWorkerGroup -ResourceGroupName "ResourceGroupName01" -AutomationAccountName "Contoso17" -Name "HybridRunbookWorkerGroup01"
```

<span data-ttu-id="c7acd-114">這個命令會在自動化帳戶（名為 Contoso17）中取得名為 HybridRunbookWorkerGroup01 的混合式 runbook worker 群組。</span><span class="sxs-lookup"><span data-stu-id="c7acd-114">This command gets the hybrid runbook worker group named HybridRunbookWorkerGroup01 in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="c7acd-115">範例3：在混合式 runbook worker 群組中取得工作人員</span><span class="sxs-lookup"><span data-stu-id="c7acd-115">Example 3: Get the workers in a hybrid runbook worker group</span></span>
```
PS C:\>(Get-AzureRMAutomationHybridWorker -ResourceGroupName ResourceGroupName01 -AutomationAccountName Contoso17 -Name "HybridRunbookWorkerGroup01" ).RunbookWorker
```

<span data-ttu-id="c7acd-116">這個命令會在自動化帳戶（名為 Contoso17）的混合式 runbook worker 群組中取得混合式 runbook 輔助角色。</span><span class="sxs-lookup"><span data-stu-id="c7acd-116">This command gets the hybrid runbook workers in the hybrid runbook worker group named HybridRunbookWorkerGroup01 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="c7acd-117">參數</span><span class="sxs-lookup"><span data-stu-id="c7acd-117">PARAMETERS</span></span>

### <span data-ttu-id="c7acd-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="c7acd-118">-AutomationAccountName</span></span>
<span data-ttu-id="c7acd-119">指定自動化帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="c7acd-119">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="c7acd-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7acd-120">-DefaultProfile</span></span>
<span data-ttu-id="c7acd-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="c7acd-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c7acd-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="c7acd-122">-Name</span></span>
<span data-ttu-id="c7acd-123">指定混合式 runbook worker 組名稱。</span><span class="sxs-lookup"><span data-stu-id="c7acd-123">Specifies the hybrid runbook worker group name.</span></span>

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

### <span data-ttu-id="c7acd-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7acd-124">-ResourceGroupName</span></span>
<span data-ttu-id="c7acd-125">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c7acd-125">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="c7acd-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7acd-126">CommonParameters</span></span>
<span data-ttu-id="c7acd-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c7acd-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7acd-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c7acd-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7acd-129">輸入</span><span class="sxs-lookup"><span data-stu-id="c7acd-129">INPUTS</span></span>

### <span data-ttu-id="c7acd-130">System.object</span><span class="sxs-lookup"><span data-stu-id="c7acd-130">System.String</span></span>
<span data-ttu-id="c7acd-131">參數： Name (ByValue) </span><span class="sxs-lookup"><span data-stu-id="c7acd-131">Parameters: Name (ByValue)</span></span>

## <span data-ttu-id="c7acd-132">輸出</span><span class="sxs-lookup"><span data-stu-id="c7acd-132">OUTPUTS</span></span>

### <span data-ttu-id="c7acd-133">HybridRunbookWorkerGroup 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="c7acd-133">Microsoft.Azure.Commands.Automation.Model.HybridRunbookWorkerGroup</span></span>

## <span data-ttu-id="c7acd-134">筆記</span><span class="sxs-lookup"><span data-stu-id="c7acd-134">NOTES</span></span>

## <span data-ttu-id="c7acd-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="c7acd-135">RELATED LINKS</span></span>