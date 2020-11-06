---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: FF44BCD2-AD8E-4F5C-AB10-BD6BD69E7F45
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/suspend-azurermautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Suspend-AzureRMAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Suspend-AzureRMAutomationJob.md
ms.openlocfilehash: 0820905ff8a4673c9abae56be2f7792912095e76
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448476"
---
# <span data-ttu-id="b0bff-101">Suspend-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="b0bff-101">Suspend-AzureRmAutomationJob</span></span>

## <span data-ttu-id="b0bff-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b0bff-102">SYNOPSIS</span></span>
<span data-ttu-id="b0bff-103">暫停自動化作業。</span><span class="sxs-lookup"><span data-stu-id="b0bff-103">Suspends an Automation job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b0bff-104">句法</span><span class="sxs-lookup"><span data-stu-id="b0bff-104">SYNTAX</span></span>

```
Suspend-AzureRmAutomationJob [-Id] <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b0bff-105">說明</span><span class="sxs-lookup"><span data-stu-id="b0bff-105">DESCRIPTION</span></span>
<span data-ttu-id="b0bff-106">**AzureRmAutomationJob** Cmdlet 會暫停 Azure 自動化作業。</span><span class="sxs-lookup"><span data-stu-id="b0bff-106">The **Suspend-AzureRmAutomationJob** cmdlet suspends an Azure Automation job.</span></span>
<span data-ttu-id="b0bff-107">指定執行自動化作業。</span><span class="sxs-lookup"><span data-stu-id="b0bff-107">Specify a running Automation job.</span></span>
<span data-ttu-id="b0bff-108">若要繼續暫停的作業，請使用 Resume-AzureRmAutomationJob Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b0bff-108">To resume a suspended job, use the Resume-AzureRmAutomationJob cmdlet.</span></span>

## <span data-ttu-id="b0bff-109">示例</span><span class="sxs-lookup"><span data-stu-id="b0bff-109">EXAMPLES</span></span>

### <span data-ttu-id="b0bff-110">範例1：暫停作業</span><span class="sxs-lookup"><span data-stu-id="b0bff-110">Example 1: Suspend a job</span></span>
```
PS C:\>Suspend-AzureRmAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="b0bff-111">這個命令會暫停具有指定識別碼的作業。</span><span class="sxs-lookup"><span data-stu-id="b0bff-111">This command suspends the job that has the specified ID.</span></span>

## <span data-ttu-id="b0bff-112">參數</span><span class="sxs-lookup"><span data-stu-id="b0bff-112">PARAMETERS</span></span>

### <span data-ttu-id="b0bff-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="b0bff-113">-AutomationAccountName</span></span>
<span data-ttu-id="b0bff-114">指定此 Cmdlet 暫停作業的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="b0bff-114">Specifies the name of an Automation account in which this cmdlet suspends a job.</span></span>

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

### <span data-ttu-id="b0bff-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0bff-115">-DefaultProfile</span></span>
<span data-ttu-id="b0bff-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="b0bff-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b0bff-117">-識別碼</span><span class="sxs-lookup"><span data-stu-id="b0bff-117">-Id</span></span>
<span data-ttu-id="b0bff-118">指定此 Cmdlet 暫停的作業識別碼。</span><span class="sxs-lookup"><span data-stu-id="b0bff-118">Specifies the ID of a job that this cmdlet suspends.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: JobId

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0bff-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0bff-119">-ResourceGroupName</span></span>
<span data-ttu-id="b0bff-120">指定此 Cmdlet 暫停的作業識別碼。</span><span class="sxs-lookup"><span data-stu-id="b0bff-120">Specifies the ID of a job that this cmdlet suspends.</span></span>

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

### <span data-ttu-id="b0bff-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0bff-121">CommonParameters</span></span>
<span data-ttu-id="b0bff-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b0bff-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0bff-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b0bff-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0bff-124">輸入</span><span class="sxs-lookup"><span data-stu-id="b0bff-124">INPUTS</span></span>

### <span data-ttu-id="b0bff-125">Guid.empty</span><span class="sxs-lookup"><span data-stu-id="b0bff-125">System.Guid</span></span>

### <span data-ttu-id="b0bff-126">System.object</span><span class="sxs-lookup"><span data-stu-id="b0bff-126">System.String</span></span>

## <span data-ttu-id="b0bff-127">輸出</span><span class="sxs-lookup"><span data-stu-id="b0bff-127">OUTPUTS</span></span>

### <span data-ttu-id="b0bff-128">System.void</span><span class="sxs-lookup"><span data-stu-id="b0bff-128">System.Void</span></span>

## <span data-ttu-id="b0bff-129">筆記</span><span class="sxs-lookup"><span data-stu-id="b0bff-129">NOTES</span></span>

## <span data-ttu-id="b0bff-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="b0bff-130">RELATED LINKS</span></span>

[<span data-ttu-id="b0bff-131">AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="b0bff-131">Get-AzureRmAutomationJob</span></span>](./Get-AzureRMAutomationJob.md)

[<span data-ttu-id="b0bff-132">AzureRmAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="b0bff-132">Get-AzureRmAutomationJobOutput</span></span>](./Get-AzureRMAutomationJobOutput.md)

[<span data-ttu-id="b0bff-133">Resume-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="b0bff-133">Resume-AzureRmAutomationJob</span></span>](./Resume-AzureRMAutomationJob.md)

[<span data-ttu-id="b0bff-134">停止 AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="b0bff-134">Stop-AzureRmAutomationJob</span></span>](./Stop-AzureRMAutomationJob.md)


