---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: BE1A9247-9F8E-45EA-9590-684A5A5662AC
online version: https://docs.microsoft.com/powershell/module/az.automation/stop-azautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Stop-AzAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Stop-AzAutomationJob.md
ms.openlocfilehash: c0169a799db59a66f0d44191e58dae3760ec4128
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911777"
---
# <span data-ttu-id="a1c51-101">Stop-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="a1c51-101">Stop-AzAutomationJob</span></span>

## <span data-ttu-id="a1c51-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a1c51-102">SYNOPSIS</span></span>
<span data-ttu-id="a1c51-103">停止自動化工作。</span><span class="sxs-lookup"><span data-stu-id="a1c51-103">Stops an Automation job.</span></span>

## <span data-ttu-id="a1c51-104">語法</span><span class="sxs-lookup"><span data-stu-id="a1c51-104">SYNTAX</span></span>

```
Stop-AzAutomationJob [-Id] <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a1c51-105">描述</span><span class="sxs-lookup"><span data-stu-id="a1c51-105">DESCRIPTION</span></span>
<span data-ttu-id="a1c51-106">**Stop-AzAutomationJob** Cmdlet 會停止 Azure 自動化工作。</span><span class="sxs-lookup"><span data-stu-id="a1c51-106">The **Stop-AzAutomationJob** cmdlet stops an Azure Automation job.</span></span>
<span data-ttu-id="a1c51-107">指定執行中自動化工作。</span><span class="sxs-lookup"><span data-stu-id="a1c51-107">Specify a running Automation job.</span></span>

## <span data-ttu-id="a1c51-108">例子</span><span class="sxs-lookup"><span data-stu-id="a1c51-108">EXAMPLES</span></span>

### <span data-ttu-id="a1c51-109">範例 1：停止工作</span><span class="sxs-lookup"><span data-stu-id="a1c51-109">Example 1: Stop a job</span></span>
```
PS C:\>Stop-AzAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="a1c51-110">此命令會停止具有指定識別碼的工作。</span><span class="sxs-lookup"><span data-stu-id="a1c51-110">This command stops the job that has the specified ID.</span></span>

## <span data-ttu-id="a1c51-111">參數</span><span class="sxs-lookup"><span data-stu-id="a1c51-111">PARAMETERS</span></span>

### <span data-ttu-id="a1c51-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a1c51-112">-AutomationAccountName</span></span>
<span data-ttu-id="a1c51-113">指定此 Cmdlet 停止工作的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="a1c51-113">Specifies the name of an Automation account in which this cmdlet stops a job.</span></span>

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

### <span data-ttu-id="a1c51-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1c51-114">-DefaultProfile</span></span>
<span data-ttu-id="a1c51-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="a1c51-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a1c51-116">-Id</span><span class="sxs-lookup"><span data-stu-id="a1c51-116">-Id</span></span>
<span data-ttu-id="a1c51-117">指定此 Cmdlet 停止的工作識別碼。</span><span class="sxs-lookup"><span data-stu-id="a1c51-117">Specifies the ID of a job that this cmdlet stops.</span></span>

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

### <span data-ttu-id="a1c51-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1c51-118">-ResourceGroupName</span></span>
<span data-ttu-id="a1c51-119">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a1c51-119">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="a1c51-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1c51-120">CommonParameters</span></span>
<span data-ttu-id="a1c51-121">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a1c51-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1c51-122">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="a1c51-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1c51-123">輸入</span><span class="sxs-lookup"><span data-stu-id="a1c51-123">INPUTS</span></span>

### <span data-ttu-id="a1c51-124">System.Guid</span><span class="sxs-lookup"><span data-stu-id="a1c51-124">System.Guid</span></span>

### <span data-ttu-id="a1c51-125">System.String</span><span class="sxs-lookup"><span data-stu-id="a1c51-125">System.String</span></span>

## <span data-ttu-id="a1c51-126">輸出</span><span class="sxs-lookup"><span data-stu-id="a1c51-126">OUTPUTS</span></span>

### <span data-ttu-id="a1c51-127">System.Void</span><span class="sxs-lookup"><span data-stu-id="a1c51-127">System.Void</span></span>

## <span data-ttu-id="a1c51-128">筆記</span><span class="sxs-lookup"><span data-stu-id="a1c51-128">NOTES</span></span>

## <span data-ttu-id="a1c51-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="a1c51-129">RELATED LINKS</span></span>

[<span data-ttu-id="a1c51-130">Get-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="a1c51-130">Get-AzAutomationJob</span></span>](./Get-AzAutomationJob.md)

[<span data-ttu-id="a1c51-131">Get-AzAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="a1c51-131">Get-AzAutomationJobOutput</span></span>](./Get-AzAutomationJobOutput.md)

[<span data-ttu-id="a1c51-132">Resume-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="a1c51-132">Resume-AzAutomationJob</span></span>](./Resume-AzAutomationJob.md)

[<span data-ttu-id="a1c51-133">Suspend-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="a1c51-133">Suspend-AzAutomationJob</span></span>](./Suspend-AzAutomationJob.md)


