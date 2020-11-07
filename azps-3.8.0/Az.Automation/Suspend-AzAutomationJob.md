---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: FF44BCD2-AD8E-4F5C-AB10-BD6BD69E7F45
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/suspend-azautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Suspend-AzAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Suspend-AzAutomationJob.md
ms.openlocfilehash: 3aecdb18579f46722a73e3de538f5f3c929b606f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93966100"
---
# <span data-ttu-id="03357-101">Suspend-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="03357-101">Suspend-AzAutomationJob</span></span>

## <span data-ttu-id="03357-102">摘要</span><span class="sxs-lookup"><span data-stu-id="03357-102">SYNOPSIS</span></span>
<span data-ttu-id="03357-103">暫停自動化作業。</span><span class="sxs-lookup"><span data-stu-id="03357-103">Suspends an Automation job.</span></span>

## <span data-ttu-id="03357-104">句法</span><span class="sxs-lookup"><span data-stu-id="03357-104">SYNTAX</span></span>

```
Suspend-AzAutomationJob [-Id] <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="03357-105">說明</span><span class="sxs-lookup"><span data-stu-id="03357-105">DESCRIPTION</span></span>
<span data-ttu-id="03357-106">**AzAutomationJob** Cmdlet 會暫停 Azure 自動化作業。</span><span class="sxs-lookup"><span data-stu-id="03357-106">The **Suspend-AzAutomationJob** cmdlet suspends an Azure Automation job.</span></span>
<span data-ttu-id="03357-107">指定執行自動化作業。</span><span class="sxs-lookup"><span data-stu-id="03357-107">Specify a running Automation job.</span></span>
<span data-ttu-id="03357-108">若要繼續暫停的作業，請使用 Resume-AzAutomationJob Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="03357-108">To resume a suspended job, use the Resume-AzAutomationJob cmdlet.</span></span>

## <span data-ttu-id="03357-109">示例</span><span class="sxs-lookup"><span data-stu-id="03357-109">EXAMPLES</span></span>

### <span data-ttu-id="03357-110">範例1：暫停作業</span><span class="sxs-lookup"><span data-stu-id="03357-110">Example 1: Suspend a job</span></span>
```
PS C:\>Suspend-AzAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="03357-111">這個命令會暫停具有指定識別碼的作業。</span><span class="sxs-lookup"><span data-stu-id="03357-111">This command suspends the job that has the specified ID.</span></span>

## <span data-ttu-id="03357-112">參數</span><span class="sxs-lookup"><span data-stu-id="03357-112">PARAMETERS</span></span>

### <span data-ttu-id="03357-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="03357-113">-AutomationAccountName</span></span>
<span data-ttu-id="03357-114">指定此 Cmdlet 暫停作業的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="03357-114">Specifies the name of an Automation account in which this cmdlet suspends a job.</span></span>

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

### <span data-ttu-id="03357-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03357-115">-DefaultProfile</span></span>
<span data-ttu-id="03357-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="03357-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="03357-117">-識別碼</span><span class="sxs-lookup"><span data-stu-id="03357-117">-Id</span></span>
<span data-ttu-id="03357-118">指定此 Cmdlet 暫停的作業識別碼。</span><span class="sxs-lookup"><span data-stu-id="03357-118">Specifies the ID of a job that this cmdlet suspends.</span></span>

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

### <span data-ttu-id="03357-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03357-119">-ResourceGroupName</span></span>
<span data-ttu-id="03357-120">指定此 Cmdlet 暫停的作業識別碼。</span><span class="sxs-lookup"><span data-stu-id="03357-120">Specifies the ID of a job that this cmdlet suspends.</span></span>

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

### <span data-ttu-id="03357-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03357-121">CommonParameters</span></span>
<span data-ttu-id="03357-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="03357-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03357-123">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="03357-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03357-124">輸入</span><span class="sxs-lookup"><span data-stu-id="03357-124">INPUTS</span></span>

### <span data-ttu-id="03357-125">Guid.empty</span><span class="sxs-lookup"><span data-stu-id="03357-125">System.Guid</span></span>

### <span data-ttu-id="03357-126">System.object</span><span class="sxs-lookup"><span data-stu-id="03357-126">System.String</span></span>

## <span data-ttu-id="03357-127">輸出</span><span class="sxs-lookup"><span data-stu-id="03357-127">OUTPUTS</span></span>

### <span data-ttu-id="03357-128">System.void</span><span class="sxs-lookup"><span data-stu-id="03357-128">System.Void</span></span>

## <span data-ttu-id="03357-129">筆記</span><span class="sxs-lookup"><span data-stu-id="03357-129">NOTES</span></span>

## <span data-ttu-id="03357-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="03357-130">RELATED LINKS</span></span>

[<span data-ttu-id="03357-131">AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="03357-131">Get-AzAutomationJob</span></span>](./Get-AzAutomationJob.md)

[<span data-ttu-id="03357-132">AzAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="03357-132">Get-AzAutomationJobOutput</span></span>](./Get-AzAutomationJobOutput.md)

[<span data-ttu-id="03357-133">Resume-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="03357-133">Resume-AzAutomationJob</span></span>](./Resume-AzAutomationJob.md)

[<span data-ttu-id="03357-134">停止 AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="03357-134">Stop-AzAutomationJob</span></span>](./Stop-AzAutomationJob.md)


