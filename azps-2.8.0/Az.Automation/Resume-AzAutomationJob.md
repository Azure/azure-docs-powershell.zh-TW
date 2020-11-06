---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 9400E9EB-E927-44D5-8722-9706BDD92FD5
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/resume-azautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Resume-AzAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Resume-AzAutomationJob.md
ms.openlocfilehash: 6315ba9079729779a7db872a87237e1b664837c4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93613686"
---
# <span data-ttu-id="78b13-101">Resume-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="78b13-101">Resume-AzAutomationJob</span></span>

## <span data-ttu-id="78b13-102">摘要</span><span class="sxs-lookup"><span data-stu-id="78b13-102">SYNOPSIS</span></span>
<span data-ttu-id="78b13-103">繼續已暫停的自動作業。</span><span class="sxs-lookup"><span data-stu-id="78b13-103">Resumes a suspended Automation job.</span></span>

## <span data-ttu-id="78b13-104">句法</span><span class="sxs-lookup"><span data-stu-id="78b13-104">SYNTAX</span></span>

```
Resume-AzAutomationJob [-Id] <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="78b13-105">說明</span><span class="sxs-lookup"><span data-stu-id="78b13-105">DESCRIPTION</span></span>
<span data-ttu-id="78b13-106">**Resume AzAutomationJob** Cmdlet 會繼續執行暫停的 Azure 自動化作業。</span><span class="sxs-lookup"><span data-stu-id="78b13-106">The **Resume-AzAutomationJob** cmdlet resumes a suspended Azure Automation job.</span></span>
<span data-ttu-id="78b13-107">指定暫停的作業。</span><span class="sxs-lookup"><span data-stu-id="78b13-107">Specify the suspended job.</span></span>
<span data-ttu-id="78b13-108">若要暫停作業，請使用 Suspend-AzAutomationJob Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="78b13-108">To suspend a job, use the Suspend-AzAutomationJob cmdlet.</span></span>

## <span data-ttu-id="78b13-109">示例</span><span class="sxs-lookup"><span data-stu-id="78b13-109">EXAMPLES</span></span>

### <span data-ttu-id="78b13-110">範例1：繼續暫停的作業</span><span class="sxs-lookup"><span data-stu-id="78b13-110">Example 1: Resume a suspended job</span></span>
```
PS C:\>Resume-AzAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="78b13-111">這個命令會繼續執行具有指定識別碼的作業。</span><span class="sxs-lookup"><span data-stu-id="78b13-111">This command resumes the job that has the specified ID.</span></span>

## <span data-ttu-id="78b13-112">參數</span><span class="sxs-lookup"><span data-stu-id="78b13-112">PARAMETERS</span></span>

### <span data-ttu-id="78b13-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="78b13-113">-AutomationAccountName</span></span>
<span data-ttu-id="78b13-114">指定此 Cmdlet 繼續作業的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="78b13-114">Specifies the name of an Automation account in which this cmdlet resume a job.</span></span>

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

### <span data-ttu-id="78b13-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78b13-115">-DefaultProfile</span></span>
<span data-ttu-id="78b13-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="78b13-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="78b13-117">-識別碼</span><span class="sxs-lookup"><span data-stu-id="78b13-117">-Id</span></span>
<span data-ttu-id="78b13-118">指定此 Cmdlet 繼續的作業識別碼。</span><span class="sxs-lookup"><span data-stu-id="78b13-118">Specifies the ID of a job that this cmdlet resumes.</span></span>

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

### <span data-ttu-id="78b13-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78b13-119">-ResourceGroupName</span></span>
<span data-ttu-id="78b13-120">指定此 Cmdlet 繼續作業之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="78b13-120">Specifies the name of a resource group for which this cmdlet resumes a job.</span></span>

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

### <span data-ttu-id="78b13-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78b13-121">CommonParameters</span></span>
<span data-ttu-id="78b13-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="78b13-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78b13-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="78b13-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78b13-124">輸入</span><span class="sxs-lookup"><span data-stu-id="78b13-124">INPUTS</span></span>

### <span data-ttu-id="78b13-125">Guid.empty</span><span class="sxs-lookup"><span data-stu-id="78b13-125">System.Guid</span></span>

### <span data-ttu-id="78b13-126">System.object</span><span class="sxs-lookup"><span data-stu-id="78b13-126">System.String</span></span>

## <span data-ttu-id="78b13-127">輸出</span><span class="sxs-lookup"><span data-stu-id="78b13-127">OUTPUTS</span></span>

### <span data-ttu-id="78b13-128">System.void</span><span class="sxs-lookup"><span data-stu-id="78b13-128">System.Void</span></span>

## <span data-ttu-id="78b13-129">筆記</span><span class="sxs-lookup"><span data-stu-id="78b13-129">NOTES</span></span>

## <span data-ttu-id="78b13-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="78b13-130">RELATED LINKS</span></span>

[<span data-ttu-id="78b13-131">AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="78b13-131">Get-AzAutomationJob</span></span>](./Get-AzAutomationJob.md)

[<span data-ttu-id="78b13-132">AzAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="78b13-132">Get-AzAutomationJobOutput</span></span>](./Get-AzAutomationJobOutput.md)

[<span data-ttu-id="78b13-133">停止 AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="78b13-133">Stop-AzAutomationJob</span></span>](./Stop-AzAutomationJob.md)

[<span data-ttu-id="78b13-134">暫停-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="78b13-134">Suspend-AzAutomationJob</span></span>](./Suspend-AzAutomationJob.md)


