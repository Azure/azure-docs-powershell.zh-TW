---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: BE1A9247-9F8E-45EA-9590-684A5A5662AC
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/stop-azautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Stop-AzAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Stop-AzAutomationJob.md
ms.openlocfilehash: 451457cf4483d9af6d8a7aca8731b95dc5c95859
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94286128"
---
# <span data-ttu-id="efd19-101">Stop-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="efd19-101">Stop-AzAutomationJob</span></span>

## <span data-ttu-id="efd19-102">摘要</span><span class="sxs-lookup"><span data-stu-id="efd19-102">SYNOPSIS</span></span>
<span data-ttu-id="efd19-103">停止自動化作業。</span><span class="sxs-lookup"><span data-stu-id="efd19-103">Stops an Automation job.</span></span>

## <span data-ttu-id="efd19-104">句法</span><span class="sxs-lookup"><span data-stu-id="efd19-104">SYNTAX</span></span>

```
Stop-AzAutomationJob [-Id] <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="efd19-105">說明</span><span class="sxs-lookup"><span data-stu-id="efd19-105">DESCRIPTION</span></span>
<span data-ttu-id="efd19-106">**AzAutomationJob** Cmdlet 會停止 Azure 自動化作業。</span><span class="sxs-lookup"><span data-stu-id="efd19-106">The **Stop-AzAutomationJob** cmdlet stops an Azure Automation job.</span></span>
<span data-ttu-id="efd19-107">指定執行自動化作業。</span><span class="sxs-lookup"><span data-stu-id="efd19-107">Specify a running Automation job.</span></span>

## <span data-ttu-id="efd19-108">示例</span><span class="sxs-lookup"><span data-stu-id="efd19-108">EXAMPLES</span></span>

### <span data-ttu-id="efd19-109">範例1：停止作業</span><span class="sxs-lookup"><span data-stu-id="efd19-109">Example 1: Stop a job</span></span>
```
PS C:\>Stop-AzAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="efd19-110">這個命令會停止具有指定識別碼的作業。</span><span class="sxs-lookup"><span data-stu-id="efd19-110">This command stops the job that has the specified ID.</span></span>

## <span data-ttu-id="efd19-111">參數</span><span class="sxs-lookup"><span data-stu-id="efd19-111">PARAMETERS</span></span>

### <span data-ttu-id="efd19-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="efd19-112">-AutomationAccountName</span></span>
<span data-ttu-id="efd19-113">指定此 Cmdlet 停止作業的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="efd19-113">Specifies the name of an Automation account in which this cmdlet stops a job.</span></span>

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

### <span data-ttu-id="efd19-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efd19-114">-DefaultProfile</span></span>
<span data-ttu-id="efd19-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="efd19-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="efd19-116">-識別碼</span><span class="sxs-lookup"><span data-stu-id="efd19-116">-Id</span></span>
<span data-ttu-id="efd19-117">指定此 Cmdlet 停止的作業識別碼。</span><span class="sxs-lookup"><span data-stu-id="efd19-117">Specifies the ID of a job that this cmdlet stops.</span></span>

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

### <span data-ttu-id="efd19-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="efd19-118">-ResourceGroupName</span></span>
<span data-ttu-id="efd19-119">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="efd19-119">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="efd19-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efd19-120">CommonParameters</span></span>
<span data-ttu-id="efd19-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="efd19-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efd19-122">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="efd19-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efd19-123">輸入</span><span class="sxs-lookup"><span data-stu-id="efd19-123">INPUTS</span></span>

### <span data-ttu-id="efd19-124">Guid.empty</span><span class="sxs-lookup"><span data-stu-id="efd19-124">System.Guid</span></span>

### <span data-ttu-id="efd19-125">System.object</span><span class="sxs-lookup"><span data-stu-id="efd19-125">System.String</span></span>

## <span data-ttu-id="efd19-126">輸出</span><span class="sxs-lookup"><span data-stu-id="efd19-126">OUTPUTS</span></span>

### <span data-ttu-id="efd19-127">System.void</span><span class="sxs-lookup"><span data-stu-id="efd19-127">System.Void</span></span>

## <span data-ttu-id="efd19-128">筆記</span><span class="sxs-lookup"><span data-stu-id="efd19-128">NOTES</span></span>

## <span data-ttu-id="efd19-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="efd19-129">RELATED LINKS</span></span>

[<span data-ttu-id="efd19-130">AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="efd19-130">Get-AzAutomationJob</span></span>](./Get-AzAutomationJob.md)

[<span data-ttu-id="efd19-131">AzAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="efd19-131">Get-AzAutomationJobOutput</span></span>](./Get-AzAutomationJobOutput.md)

[<span data-ttu-id="efd19-132">Resume-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="efd19-132">Resume-AzAutomationJob</span></span>](./Resume-AzAutomationJob.md)

[<span data-ttu-id="efd19-133">暫停-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="efd19-133">Suspend-AzAutomationJob</span></span>](./Suspend-AzAutomationJob.md)


