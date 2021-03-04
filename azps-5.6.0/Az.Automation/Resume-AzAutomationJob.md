---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 9400E9EB-E927-44D5-8722-9706BDD92FD5
online version: https://docs.microsoft.com/powershell/module/az.automation/resume-azautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Resume-AzAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Resume-AzAutomationJob.md
ms.openlocfilehash: 68520eda43b3586e63930b6a96cec2fc6483c594
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903361"
---
# <span data-ttu-id="4a072-101">Resume-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="4a072-101">Resume-AzAutomationJob</span></span>

## <span data-ttu-id="4a072-102">簡介</span><span class="sxs-lookup"><span data-stu-id="4a072-102">SYNOPSIS</span></span>
<span data-ttu-id="4a072-103">繼續暫停的自動化工作。</span><span class="sxs-lookup"><span data-stu-id="4a072-103">Resumes a suspended Automation job.</span></span>

## <span data-ttu-id="4a072-104">語法</span><span class="sxs-lookup"><span data-stu-id="4a072-104">SYNTAX</span></span>

```
Resume-AzAutomationJob [-Id] <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4a072-105">描述</span><span class="sxs-lookup"><span data-stu-id="4a072-105">DESCRIPTION</span></span>
<span data-ttu-id="4a072-106">**Resume-AzAutomationJob** Cmdlet 繼續暫停的 Azure 自動化工作。</span><span class="sxs-lookup"><span data-stu-id="4a072-106">The **Resume-AzAutomationJob** cmdlet resumes a suspended Azure Automation job.</span></span>
<span data-ttu-id="4a072-107">指定暫停的工作。</span><span class="sxs-lookup"><span data-stu-id="4a072-107">Specify the suspended job.</span></span>
<span data-ttu-id="4a072-108">若要暫停工作，請使用 Suspend-AzAutomationJob Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4a072-108">To suspend a job, use the Suspend-AzAutomationJob cmdlet.</span></span>

## <span data-ttu-id="4a072-109">例子</span><span class="sxs-lookup"><span data-stu-id="4a072-109">EXAMPLES</span></span>

### <span data-ttu-id="4a072-110">範例 1：繼續暫停工作</span><span class="sxs-lookup"><span data-stu-id="4a072-110">Example 1: Resume a suspended job</span></span>
```
PS C:\>Resume-AzAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="4a072-111">此命令會繼續執行具有指定識別碼的工作。</span><span class="sxs-lookup"><span data-stu-id="4a072-111">This command resumes the job that has the specified ID.</span></span>

## <span data-ttu-id="4a072-112">參數</span><span class="sxs-lookup"><span data-stu-id="4a072-112">PARAMETERS</span></span>

### <span data-ttu-id="4a072-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="4a072-113">-AutomationAccountName</span></span>
<span data-ttu-id="4a072-114">指定此 Cmdlet 繼續工作的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="4a072-114">Specifies the name of an Automation account in which this cmdlet resume a job.</span></span>

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

### <span data-ttu-id="4a072-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a072-115">-DefaultProfile</span></span>
<span data-ttu-id="4a072-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="4a072-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4a072-117">-Id</span><span class="sxs-lookup"><span data-stu-id="4a072-117">-Id</span></span>
<span data-ttu-id="4a072-118">指定此 Cmdlet 繼續的工作識別碼。</span><span class="sxs-lookup"><span data-stu-id="4a072-118">Specifies the ID of a job that this cmdlet resumes.</span></span>

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

### <span data-ttu-id="4a072-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a072-119">-ResourceGroupName</span></span>
<span data-ttu-id="4a072-120">指定此 Cmdlet 繼續工作的資源組名。</span><span class="sxs-lookup"><span data-stu-id="4a072-120">Specifies the name of a resource group for which this cmdlet resumes a job.</span></span>

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

### <span data-ttu-id="4a072-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a072-121">CommonParameters</span></span>
<span data-ttu-id="4a072-122">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="4a072-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a072-123">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="4a072-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a072-124">輸入</span><span class="sxs-lookup"><span data-stu-id="4a072-124">INPUTS</span></span>

### <span data-ttu-id="4a072-125">System.Guid</span><span class="sxs-lookup"><span data-stu-id="4a072-125">System.Guid</span></span>

### <span data-ttu-id="4a072-126">System.String</span><span class="sxs-lookup"><span data-stu-id="4a072-126">System.String</span></span>

## <span data-ttu-id="4a072-127">輸出</span><span class="sxs-lookup"><span data-stu-id="4a072-127">OUTPUTS</span></span>

### <span data-ttu-id="4a072-128">System.Void</span><span class="sxs-lookup"><span data-stu-id="4a072-128">System.Void</span></span>

## <span data-ttu-id="4a072-129">筆記</span><span class="sxs-lookup"><span data-stu-id="4a072-129">NOTES</span></span>

## <span data-ttu-id="4a072-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="4a072-130">RELATED LINKS</span></span>

[<span data-ttu-id="4a072-131">Get-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="4a072-131">Get-AzAutomationJob</span></span>](./Get-AzAutomationJob.md)

[<span data-ttu-id="4a072-132">Get-AzAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="4a072-132">Get-AzAutomationJobOutput</span></span>](./Get-AzAutomationJobOutput.md)

[<span data-ttu-id="4a072-133">Stop-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="4a072-133">Stop-AzAutomationJob</span></span>](./Stop-AzAutomationJob.md)

[<span data-ttu-id="4a072-134">Suspend-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="4a072-134">Suspend-AzAutomationJob</span></span>](./Suspend-AzAutomationJob.md)


