---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B39C4D6B-392A-4C8D-A6FB-886DA1A2BA58
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationjoboutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJobOutput.md
ms.openlocfilehash: 53ae09ba82de2a96bc9db17ad7ca538c48b23a47
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98285396"
---
# <span data-ttu-id="141a2-101">Get-AzAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="141a2-101">Get-AzAutomationJobOutput</span></span>

## <span data-ttu-id="141a2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="141a2-102">SYNOPSIS</span></span>
<span data-ttu-id="141a2-103">取得自動化作業的輸出。</span><span class="sxs-lookup"><span data-stu-id="141a2-103">Gets the output of an Automation job.</span></span>

## <span data-ttu-id="141a2-104">句法</span><span class="sxs-lookup"><span data-stu-id="141a2-104">SYNTAX</span></span>

```
Get-AzAutomationJobOutput [-Id] <Guid> [-Stream <StreamType>] [-StartTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="141a2-105">說明</span><span class="sxs-lookup"><span data-stu-id="141a2-105">DESCRIPTION</span></span>
<span data-ttu-id="141a2-106">**AzAutomationJobOutput** Cmdlet 會取得 Azure 自動化作業的輸出。</span><span class="sxs-lookup"><span data-stu-id="141a2-106">The **Get-AzAutomationJobOutput** cmdlet gets the output of an Azure Automation job.</span></span>

## <span data-ttu-id="141a2-107">示例</span><span class="sxs-lookup"><span data-stu-id="141a2-107">EXAMPLES</span></span>

### <span data-ttu-id="141a2-108">範例1：取得自動化作業的輸出</span><span class="sxs-lookup"><span data-stu-id="141a2-108">Example 1: Get the output of an Automation job</span></span>
```
PS C:\>Get-AzAutomationJobOutput -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01" -Stream "Any"
```

<span data-ttu-id="141a2-109">這個命令會取得具有指定識別碼之作業的所有輸出。</span><span class="sxs-lookup"><span data-stu-id="141a2-109">This command gets all of the output of the job that has the specified ID.</span></span>

## <span data-ttu-id="141a2-110">參數</span><span class="sxs-lookup"><span data-stu-id="141a2-110">PARAMETERS</span></span>

### <span data-ttu-id="141a2-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="141a2-111">-AutomationAccountName</span></span>
<span data-ttu-id="141a2-112">指定此 Cmdlet 取得作業輸出的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="141a2-112">Specifies the name of an Automation account for which this cmdlet gets job output.</span></span>

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

### <span data-ttu-id="141a2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="141a2-113">-DefaultProfile</span></span>
<span data-ttu-id="141a2-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="141a2-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="141a2-115">-識別碼</span><span class="sxs-lookup"><span data-stu-id="141a2-115">-Id</span></span>
<span data-ttu-id="141a2-116">指定此 Cmdlet 取得輸出的作業 ID。</span><span class="sxs-lookup"><span data-stu-id="141a2-116">Specifies the ID of a job for which this cmdlet gets output.</span></span>

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

### <span data-ttu-id="141a2-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="141a2-117">-ResourceGroupName</span></span>
<span data-ttu-id="141a2-118">指定此 Cmdlet 取得作業輸出的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="141a2-118">Specifies the name of a resource group for which this cmdlet gets job output.</span></span>

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

### <span data-ttu-id="141a2-119">-StartTime</span><span class="sxs-lookup"><span data-stu-id="141a2-119">-StartTime</span></span>
<span data-ttu-id="141a2-120">將開始時間指定為 **DateTimeOffset** 物件。</span><span class="sxs-lookup"><span data-stu-id="141a2-120">Specifies a start time as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="141a2-121">您可以指定可轉換成有效 **DateTimeOffset** 的字串。</span><span class="sxs-lookup"><span data-stu-id="141a2-121">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>
<span data-ttu-id="141a2-122">這個 Cmdlet 會檢索在這段時間之後建立的輸出。</span><span class="sxs-lookup"><span data-stu-id="141a2-122">The cmdlet retrieves output created after this time.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="141a2-123">資料流程</span><span class="sxs-lookup"><span data-stu-id="141a2-123">-Stream</span></span>
<span data-ttu-id="141a2-124">指定輸出的類型。</span><span class="sxs-lookup"><span data-stu-id="141a2-124">Specifies the type of output.</span></span>
<span data-ttu-id="141a2-125">有效值為：</span><span class="sxs-lookup"><span data-stu-id="141a2-125">Valid values are:</span></span> 
- <span data-ttu-id="141a2-126">每</span><span class="sxs-lookup"><span data-stu-id="141a2-126">Any</span></span>
- <span data-ttu-id="141a2-127">Debug</span><span class="sxs-lookup"><span data-stu-id="141a2-127">Debug</span></span>
- <span data-ttu-id="141a2-128">出錯</span><span class="sxs-lookup"><span data-stu-id="141a2-128">Error</span></span>
- <span data-ttu-id="141a2-129">收</span><span class="sxs-lookup"><span data-stu-id="141a2-129">Output</span></span>
- <span data-ttu-id="141a2-130">處理</span><span class="sxs-lookup"><span data-stu-id="141a2-130">Progress</span></span>
- <span data-ttu-id="141a2-131">冗長</span><span class="sxs-lookup"><span data-stu-id="141a2-131">Verbose</span></span>
- <span data-ttu-id="141a2-132">警告</span><span class="sxs-lookup"><span data-stu-id="141a2-132">Warning</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Common.StreamType
Parameter Sets: (All)
Aliases:
Accepted values: Any, Progress, Output, Warning, Error, Verbose

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="141a2-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="141a2-133">CommonParameters</span></span>
<span data-ttu-id="141a2-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="141a2-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="141a2-135">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="141a2-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="141a2-136">輸入</span><span class="sxs-lookup"><span data-stu-id="141a2-136">INPUTS</span></span>

### <span data-ttu-id="141a2-137">Guid.empty</span><span class="sxs-lookup"><span data-stu-id="141a2-137">System.Guid</span></span>

### <span data-ttu-id="141a2-138">StreamType （自動化）。</span><span class="sxs-lookup"><span data-stu-id="141a2-138">Microsoft.Azure.Commands.Automation.Common.StreamType</span></span>

### <span data-ttu-id="141a2-139">"CoreLib" 1 [（System.object，System.object，，版本 = 4.0.0.0，Culture = 中立，</span><span class="sxs-lookup"><span data-stu-id="141a2-139">System.Nullable\`1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="141a2-140">System.object</span><span class="sxs-lookup"><span data-stu-id="141a2-140">System.String</span></span>

## <span data-ttu-id="141a2-141">輸出</span><span class="sxs-lookup"><span data-stu-id="141a2-141">OUTPUTS</span></span>

### <span data-ttu-id="141a2-142">JobStream 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="141a2-142">Microsoft.Azure.Commands.Automation.Model.JobStream</span></span>

## <span data-ttu-id="141a2-143">筆記</span><span class="sxs-lookup"><span data-stu-id="141a2-143">NOTES</span></span>

## <span data-ttu-id="141a2-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="141a2-144">RELATED LINKS</span></span>

[<span data-ttu-id="141a2-145">AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="141a2-145">Get-AzAutomationJob</span></span>](./Get-AzAutomationJob.md)

[<span data-ttu-id="141a2-146">Resume-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="141a2-146">Resume-AzAutomationJob</span></span>](./Resume-AzAutomationJob.md)

[<span data-ttu-id="141a2-147">停止 AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="141a2-147">Stop-AzAutomationJob</span></span>](./Stop-AzAutomationJob.md)

[<span data-ttu-id="141a2-148">暫停-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="141a2-148">Suspend-AzAutomationJob</span></span>](./Suspend-AzAutomationJob.md)


