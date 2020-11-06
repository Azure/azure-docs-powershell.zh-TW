---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 9B0BBBB4-A7A0-4243-9264-362A00F5B399
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationHybridWorkerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationHybridWorkerGroup.md
ms.openlocfilehash: 1f2c82bc51cb5faba9f5b1dd0524e7aced2f0b84
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452620"
---
# <span data-ttu-id="f3a8e-101">Get-AzureRMAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="f3a8e-101">Get-AzureRMAutomationHybridWorkerGroup</span></span>

## <span data-ttu-id="f3a8e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f3a8e-102">SYNOPSIS</span></span>
<span data-ttu-id="f3a8e-103">取得混合式 runbook 輔助角色群組。</span><span class="sxs-lookup"><span data-stu-id="f3a8e-103">Gets hybrid runbook worker groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f3a8e-104">句法</span><span class="sxs-lookup"><span data-stu-id="f3a8e-104">SYNTAX</span></span>

### <span data-ttu-id="f3a8e-105">ByAll (預設) </span><span class="sxs-lookup"><span data-stu-id="f3a8e-105">ByAll (Default)</span></span>
```
Get-AzureRMAutomationHybridWorkerGroup [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3a8e-106">ByName</span><span class="sxs-lookup"><span data-stu-id="f3a8e-106">ByName</span></span>
```
Get-AzureRMAutomationHybridWorkerGroup [[-Name] <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f3a8e-107">說明</span><span class="sxs-lookup"><span data-stu-id="f3a8e-107">DESCRIPTION</span></span>
<span data-ttu-id="f3a8e-108">**AzureRmAutomationHybridWorkerGroup** Cmdlet 會取得 Azure 自動化混合式 runbook 輔助角色群組。</span><span class="sxs-lookup"><span data-stu-id="f3a8e-108">The **Get-AzureRmAutomationHybridWorkerGroup** cmdlet gets Azure Automation hybrid runbook worker groups.</span></span>
<span data-ttu-id="f3a8e-109">若要取得特定群組，請指定其名稱。</span><span class="sxs-lookup"><span data-stu-id="f3a8e-109">To get a specific group, specify its name.</span></span>

## <span data-ttu-id="f3a8e-110">示例</span><span class="sxs-lookup"><span data-stu-id="f3a8e-110">EXAMPLES</span></span>

### <span data-ttu-id="f3a8e-111">範例1：取得所有混合式 runbook 輔助角色群組</span><span class="sxs-lookup"><span data-stu-id="f3a8e-111">Example 1: Get all hybrid runbook worker groups</span></span>
```
PS C:\>Get-AzureRMAutomationHybridWorkerGroup -ResourceGroupName "ResourceGroupName01" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="f3a8e-112">這個命令會在自動化帳戶（名為 Contoso17）中取得所有混合式 runbook worker 群組。</span><span class="sxs-lookup"><span data-stu-id="f3a8e-112">This command gets all hybrid runbook worker groups in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="f3a8e-113">範例2：取得單一混合式 runbook 輔助角色群組</span><span class="sxs-lookup"><span data-stu-id="f3a8e-113">Example 2: Get a single hybrid runbook worker group</span></span>
```
PS C:\>Get-AzureRMAutomationHybridWorkerGroup -ResourceGroupName "ResourceGroupName01" -AutomationAccountName "Contoso17" -Name "HybridRunbookWorkerGroup01"
```

<span data-ttu-id="f3a8e-114">這個命令會在自動化帳戶（名為 Contoso17）中取得名為 HybridRunbookWorkerGroup01 的混合式 runbook worker 群組。</span><span class="sxs-lookup"><span data-stu-id="f3a8e-114">This command gets the hybrid runbook worker group named HybridRunbookWorkerGroup01 in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="f3a8e-115">範例3：在混合式 runbook worker 群組中取得工作人員</span><span class="sxs-lookup"><span data-stu-id="f3a8e-115">Example 3: Get the workers in a hybrid runbook worker group</span></span>
```
PS C:\>(Get-AzureRMAutomationHybridWorker -ResourceGroupName ResourceGroupName01 -AutomationAccountName Contoso17 -Name "HybridRunbookWorkerGroup01" ).RunbookWorker
```

<span data-ttu-id="f3a8e-116">這個命令會在自動化帳戶（名為 Contoso17）的混合式 runbook worker 群組中取得混合式 runbook 輔助角色。</span><span class="sxs-lookup"><span data-stu-id="f3a8e-116">This command gets the hybrid runbook workers in the hybrid runbook worker group named HybridRunbookWorkerGroup01 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="f3a8e-117">參數</span><span class="sxs-lookup"><span data-stu-id="f3a8e-117">PARAMETERS</span></span>

### <span data-ttu-id="f3a8e-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f3a8e-118">-AutomationAccountName</span></span>
<span data-ttu-id="f3a8e-119">指定自動化帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="f3a8e-119">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="f3a8e-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="f3a8e-120">-Name</span></span>
<span data-ttu-id="f3a8e-121">指定混合式 runbook worker 組名稱。</span><span class="sxs-lookup"><span data-stu-id="f3a8e-121">Specifies the hybrid runbook worker group name.</span></span>

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

### <span data-ttu-id="f3a8e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3a8e-122">-ResourceGroupName</span></span>
<span data-ttu-id="f3a8e-123">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f3a8e-123">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="f3a8e-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3a8e-124">-DefaultProfile</span></span>
<span data-ttu-id="f3a8e-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f3a8e-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f3a8e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3a8e-126">CommonParameters</span></span>
<span data-ttu-id="f3a8e-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f3a8e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3a8e-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f3a8e-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3a8e-129">輸入</span><span class="sxs-lookup"><span data-stu-id="f3a8e-129">INPUTS</span></span>

### <span data-ttu-id="f3a8e-130">字串</span><span class="sxs-lookup"><span data-stu-id="f3a8e-130">String</span></span>
<span data-ttu-id="f3a8e-131">形參 "Name" 接受管線中類型 "String" 的值</span><span class="sxs-lookup"><span data-stu-id="f3a8e-131">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="f3a8e-132">輸出</span><span class="sxs-lookup"><span data-stu-id="f3a8e-132">OUTPUTS</span></span>

### <span data-ttu-id="f3a8e-133">HybridRunbookWorker 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="f3a8e-133">Microsoft.Azure.Commands.Automation.Model.HybridRunbookWorker</span></span>

## <span data-ttu-id="f3a8e-134">筆記</span><span class="sxs-lookup"><span data-stu-id="f3a8e-134">NOTES</span></span>

## <span data-ttu-id="f3a8e-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="f3a8e-135">RELATED LINKS</span></span>
