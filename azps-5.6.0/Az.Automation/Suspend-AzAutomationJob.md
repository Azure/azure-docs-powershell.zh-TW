---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: FF44BCD2-AD8E-4F5C-AB10-BD6BD69E7F45
online version: https://docs.microsoft.com/powershell/module/az.automation/suspend-azautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Suspend-AzAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Suspend-AzAutomationJob.md
ms.openlocfilehash: 035cd77ab389b9c3cdce686620b3157b4b046c41
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909241"
---
# <span data-ttu-id="9fb15-101">Suspend-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="9fb15-101">Suspend-AzAutomationJob</span></span>

## <span data-ttu-id="9fb15-102">簡介</span><span class="sxs-lookup"><span data-stu-id="9fb15-102">SYNOPSIS</span></span>
<span data-ttu-id="9fb15-103">暫停自動化工作。</span><span class="sxs-lookup"><span data-stu-id="9fb15-103">Suspends an Automation job.</span></span>

## <span data-ttu-id="9fb15-104">語法</span><span class="sxs-lookup"><span data-stu-id="9fb15-104">SYNTAX</span></span>

```
Suspend-AzAutomationJob [-Id] <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9fb15-105">描述</span><span class="sxs-lookup"><span data-stu-id="9fb15-105">DESCRIPTION</span></span>
<span data-ttu-id="9fb15-106">**Suspend-AzAutomationJob** Cmdlet 會暫停 Azure 自動化工作。</span><span class="sxs-lookup"><span data-stu-id="9fb15-106">The **Suspend-AzAutomationJob** cmdlet suspends an Azure Automation job.</span></span>
<span data-ttu-id="9fb15-107">指定執行中自動化工作。</span><span class="sxs-lookup"><span data-stu-id="9fb15-107">Specify a running Automation job.</span></span>
<span data-ttu-id="9fb15-108">若要繼續暫停的工作，請使用 Resume-AzAutomationJob Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9fb15-108">To resume a suspended job, use the Resume-AzAutomationJob cmdlet.</span></span>

## <span data-ttu-id="9fb15-109">例子</span><span class="sxs-lookup"><span data-stu-id="9fb15-109">EXAMPLES</span></span>

### <span data-ttu-id="9fb15-110">範例 1：暫停工作</span><span class="sxs-lookup"><span data-stu-id="9fb15-110">Example 1: Suspend a job</span></span>
```
PS C:\>Suspend-AzAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="9fb15-111">此命令會暫停具有指定識別碼的工作。</span><span class="sxs-lookup"><span data-stu-id="9fb15-111">This command suspends the job that has the specified ID.</span></span>

## <span data-ttu-id="9fb15-112">參數</span><span class="sxs-lookup"><span data-stu-id="9fb15-112">PARAMETERS</span></span>

### <span data-ttu-id="9fb15-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="9fb15-113">-AutomationAccountName</span></span>
<span data-ttu-id="9fb15-114">指定此 Cmdlet 暫停工作的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="9fb15-114">Specifies the name of an Automation account in which this cmdlet suspends a job.</span></span>

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

### <span data-ttu-id="9fb15-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fb15-115">-DefaultProfile</span></span>
<span data-ttu-id="9fb15-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="9fb15-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9fb15-117">-Id</span><span class="sxs-lookup"><span data-stu-id="9fb15-117">-Id</span></span>
<span data-ttu-id="9fb15-118">指定此 Cmdlet 暫停的工作識別碼。</span><span class="sxs-lookup"><span data-stu-id="9fb15-118">Specifies the ID of a job that this cmdlet suspends.</span></span>

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

### <span data-ttu-id="9fb15-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9fb15-119">-ResourceGroupName</span></span>
<span data-ttu-id="9fb15-120">指定此 Cmdlet 暫停的工作識別碼。</span><span class="sxs-lookup"><span data-stu-id="9fb15-120">Specifies the ID of a job that this cmdlet suspends.</span></span>

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

### <span data-ttu-id="9fb15-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fb15-121">CommonParameters</span></span>
<span data-ttu-id="9fb15-122">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="9fb15-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fb15-123">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="9fb15-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fb15-124">輸入</span><span class="sxs-lookup"><span data-stu-id="9fb15-124">INPUTS</span></span>

### <span data-ttu-id="9fb15-125">System.Guid</span><span class="sxs-lookup"><span data-stu-id="9fb15-125">System.Guid</span></span>

### <span data-ttu-id="9fb15-126">System.String</span><span class="sxs-lookup"><span data-stu-id="9fb15-126">System.String</span></span>

## <span data-ttu-id="9fb15-127">輸出</span><span class="sxs-lookup"><span data-stu-id="9fb15-127">OUTPUTS</span></span>

### <span data-ttu-id="9fb15-128">System.Void</span><span class="sxs-lookup"><span data-stu-id="9fb15-128">System.Void</span></span>

## <span data-ttu-id="9fb15-129">筆記</span><span class="sxs-lookup"><span data-stu-id="9fb15-129">NOTES</span></span>

## <span data-ttu-id="9fb15-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="9fb15-130">RELATED LINKS</span></span>

[<span data-ttu-id="9fb15-131">Get-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="9fb15-131">Get-AzAutomationJob</span></span>](./Get-AzAutomationJob.md)

[<span data-ttu-id="9fb15-132">Get-AzAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="9fb15-132">Get-AzAutomationJobOutput</span></span>](./Get-AzAutomationJobOutput.md)

[<span data-ttu-id="9fb15-133">Resume-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="9fb15-133">Resume-AzAutomationJob</span></span>](./Resume-AzAutomationJob.md)

[<span data-ttu-id="9fb15-134">Stop-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="9fb15-134">Stop-AzAutomationJob</span></span>](./Stop-AzAutomationJob.md)


