---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: BE1A9247-9F8E-45EA-9590-684A5A5662AC
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/stop-azautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Stop-AzAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Stop-AzAutomationJob.md
ms.openlocfilehash: 9559a599a6d0a50078dbec176ad937947facce7a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93613659"
---
# <span data-ttu-id="88dda-101">Stop-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="88dda-101">Stop-AzAutomationJob</span></span>

## <span data-ttu-id="88dda-102">摘要</span><span class="sxs-lookup"><span data-stu-id="88dda-102">SYNOPSIS</span></span>
<span data-ttu-id="88dda-103">停止自動化作業。</span><span class="sxs-lookup"><span data-stu-id="88dda-103">Stops an Automation job.</span></span>

## <span data-ttu-id="88dda-104">句法</span><span class="sxs-lookup"><span data-stu-id="88dda-104">SYNTAX</span></span>

```
Stop-AzAutomationJob [-Id] <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="88dda-105">說明</span><span class="sxs-lookup"><span data-stu-id="88dda-105">DESCRIPTION</span></span>
<span data-ttu-id="88dda-106">**AzAutomationJob** Cmdlet 會停止 Azure 自動化作業。</span><span class="sxs-lookup"><span data-stu-id="88dda-106">The **Stop-AzAutomationJob** cmdlet stops an Azure Automation job.</span></span>
<span data-ttu-id="88dda-107">指定執行自動化作業。</span><span class="sxs-lookup"><span data-stu-id="88dda-107">Specify a running Automation job.</span></span>

## <span data-ttu-id="88dda-108">示例</span><span class="sxs-lookup"><span data-stu-id="88dda-108">EXAMPLES</span></span>

### <span data-ttu-id="88dda-109">範例1：停止作業</span><span class="sxs-lookup"><span data-stu-id="88dda-109">Example 1: Stop a job</span></span>
```
PS C:\>Stop-AzAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="88dda-110">這個命令會停止具有指定識別碼的作業。</span><span class="sxs-lookup"><span data-stu-id="88dda-110">This command stops the job that has the specified ID.</span></span>

## <span data-ttu-id="88dda-111">參數</span><span class="sxs-lookup"><span data-stu-id="88dda-111">PARAMETERS</span></span>

### <span data-ttu-id="88dda-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="88dda-112">-AutomationAccountName</span></span>
<span data-ttu-id="88dda-113">指定此 Cmdlet 停止作業的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="88dda-113">Specifies the name of an Automation account in which this cmdlet stops a job.</span></span>

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

### <span data-ttu-id="88dda-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88dda-114">-DefaultProfile</span></span>
<span data-ttu-id="88dda-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="88dda-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="88dda-116">-識別碼</span><span class="sxs-lookup"><span data-stu-id="88dda-116">-Id</span></span>
<span data-ttu-id="88dda-117">指定此 Cmdlet 停止的作業識別碼。</span><span class="sxs-lookup"><span data-stu-id="88dda-117">Specifies the ID of a job that this cmdlet stops.</span></span>

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

### <span data-ttu-id="88dda-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88dda-118">-ResourceGroupName</span></span>
<span data-ttu-id="88dda-119">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="88dda-119">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="88dda-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88dda-120">CommonParameters</span></span>
<span data-ttu-id="88dda-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="88dda-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88dda-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="88dda-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88dda-123">輸入</span><span class="sxs-lookup"><span data-stu-id="88dda-123">INPUTS</span></span>

### <span data-ttu-id="88dda-124">Guid.empty</span><span class="sxs-lookup"><span data-stu-id="88dda-124">System.Guid</span></span>

### <span data-ttu-id="88dda-125">System.object</span><span class="sxs-lookup"><span data-stu-id="88dda-125">System.String</span></span>

## <span data-ttu-id="88dda-126">輸出</span><span class="sxs-lookup"><span data-stu-id="88dda-126">OUTPUTS</span></span>

### <span data-ttu-id="88dda-127">System.void</span><span class="sxs-lookup"><span data-stu-id="88dda-127">System.Void</span></span>

## <span data-ttu-id="88dda-128">筆記</span><span class="sxs-lookup"><span data-stu-id="88dda-128">NOTES</span></span>

## <span data-ttu-id="88dda-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="88dda-129">RELATED LINKS</span></span>

[<span data-ttu-id="88dda-130">AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="88dda-130">Get-AzAutomationJob</span></span>](./Get-AzAutomationJob.md)

[<span data-ttu-id="88dda-131">AzAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="88dda-131">Get-AzAutomationJobOutput</span></span>](./Get-AzAutomationJobOutput.md)

[<span data-ttu-id="88dda-132">Resume-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="88dda-132">Resume-AzAutomationJob</span></span>](./Resume-AzAutomationJob.md)

[<span data-ttu-id="88dda-133">暫停-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="88dda-133">Suspend-AzAutomationJob</span></span>](./Suspend-AzAutomationJob.md)


