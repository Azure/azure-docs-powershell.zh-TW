---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B39C4D6B-392A-4C8D-A6FB-886DA1A2BA58
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationjoboutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJobOutput.md
ms.openlocfilehash: f49c0bbf17ed87d782b03052d9caeb5aba51eeff
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913613"
---
# <span data-ttu-id="e7d83-101">Get-AzAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="e7d83-101">Get-AzAutomationJobOutput</span></span>

## <span data-ttu-id="e7d83-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e7d83-102">SYNOPSIS</span></span>
<span data-ttu-id="e7d83-103">獲得自動化工作的輸出結果。</span><span class="sxs-lookup"><span data-stu-id="e7d83-103">Gets the output of an Automation job.</span></span>

## <span data-ttu-id="e7d83-104">語法</span><span class="sxs-lookup"><span data-stu-id="e7d83-104">SYNTAX</span></span>

```
Get-AzAutomationJobOutput [-Id] <Guid> [-Stream <StreamType>] [-StartTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e7d83-105">描述</span><span class="sxs-lookup"><span data-stu-id="e7d83-105">DESCRIPTION</span></span>
<span data-ttu-id="e7d83-106">**Get-AzAutomationJobOutput** Cmdlet 會取得 Azure 自動化工作的輸出結果。</span><span class="sxs-lookup"><span data-stu-id="e7d83-106">The **Get-AzAutomationJobOutput** cmdlet gets the output of an Azure Automation job.</span></span>

## <span data-ttu-id="e7d83-107">例子</span><span class="sxs-lookup"><span data-stu-id="e7d83-107">EXAMPLES</span></span>

### <span data-ttu-id="e7d83-108">範例 1：取得自動化工作的輸出結果</span><span class="sxs-lookup"><span data-stu-id="e7d83-108">Example 1: Get the output of an Automation job</span></span>
```
PS C:\>Get-AzAutomationJobOutput -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01" -Stream "Any"
```

<span data-ttu-id="e7d83-109">此命令會獲得具有指定識別碼之工作的所有輸出。</span><span class="sxs-lookup"><span data-stu-id="e7d83-109">This command gets all of the output of the job that has the specified ID.</span></span>

## <span data-ttu-id="e7d83-110">參數</span><span class="sxs-lookup"><span data-stu-id="e7d83-110">PARAMETERS</span></span>

### <span data-ttu-id="e7d83-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="e7d83-111">-AutomationAccountName</span></span>
<span data-ttu-id="e7d83-112">指定此 Cmdlet 可輸出工作之自動化帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="e7d83-112">Specifies the name of an Automation account for which this cmdlet gets job output.</span></span>

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

### <span data-ttu-id="e7d83-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7d83-113">-DefaultProfile</span></span>
<span data-ttu-id="e7d83-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="e7d83-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e7d83-115">-Id</span><span class="sxs-lookup"><span data-stu-id="e7d83-115">-Id</span></span>
<span data-ttu-id="e7d83-116">指定此 Cmdlet 可輸出的工作識別碼。</span><span class="sxs-lookup"><span data-stu-id="e7d83-116">Specifies the ID of a job for which this cmdlet gets output.</span></span>

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

### <span data-ttu-id="e7d83-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7d83-117">-ResourceGroupName</span></span>
<span data-ttu-id="e7d83-118">指定此 Cmdlet 可輸出工作的資源組名。</span><span class="sxs-lookup"><span data-stu-id="e7d83-118">Specifies the name of a resource group for which this cmdlet gets job output.</span></span>

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

### <span data-ttu-id="e7d83-119">-StartTime</span><span class="sxs-lookup"><span data-stu-id="e7d83-119">-StartTime</span></span>
<span data-ttu-id="e7d83-120">將開始時間指定為 **DateTimeOffset** 物件。</span><span class="sxs-lookup"><span data-stu-id="e7d83-120">Specifies a start time as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="e7d83-121">您可以指定可以轉換成有效 **DateTimeOffset 的字串**。</span><span class="sxs-lookup"><span data-stu-id="e7d83-121">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>
<span data-ttu-id="e7d83-122">Cmdlet 會從這次之後所建立的輸出結果中，來取回。</span><span class="sxs-lookup"><span data-stu-id="e7d83-122">The cmdlet retrieves output created after this time.</span></span>

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

### <span data-ttu-id="e7d83-123">-Stream</span><span class="sxs-lookup"><span data-stu-id="e7d83-123">-Stream</span></span>
<span data-ttu-id="e7d83-124">指定輸出類型。</span><span class="sxs-lookup"><span data-stu-id="e7d83-124">Specifies the type of output.</span></span>
<span data-ttu-id="e7d83-125">有效的值為：</span><span class="sxs-lookup"><span data-stu-id="e7d83-125">Valid values are:</span></span> 
- <span data-ttu-id="e7d83-126">任何</span><span class="sxs-lookup"><span data-stu-id="e7d83-126">Any</span></span>
- <span data-ttu-id="e7d83-127">調試</span><span class="sxs-lookup"><span data-stu-id="e7d83-127">Debug</span></span>
- <span data-ttu-id="e7d83-128">錯誤</span><span class="sxs-lookup"><span data-stu-id="e7d83-128">Error</span></span>
- <span data-ttu-id="e7d83-129">輸出</span><span class="sxs-lookup"><span data-stu-id="e7d83-129">Output</span></span>
- <span data-ttu-id="e7d83-130">進展</span><span class="sxs-lookup"><span data-stu-id="e7d83-130">Progress</span></span>
- <span data-ttu-id="e7d83-131">詳細</span><span class="sxs-lookup"><span data-stu-id="e7d83-131">Verbose</span></span>
- <span data-ttu-id="e7d83-132">警告</span><span class="sxs-lookup"><span data-stu-id="e7d83-132">Warning</span></span>

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

### <span data-ttu-id="e7d83-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7d83-133">CommonParameters</span></span>
<span data-ttu-id="e7d83-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e7d83-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7d83-135">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="e7d83-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7d83-136">輸入</span><span class="sxs-lookup"><span data-stu-id="e7d83-136">INPUTS</span></span>

### <span data-ttu-id="e7d83-137">System.Guid</span><span class="sxs-lookup"><span data-stu-id="e7d83-137">System.Guid</span></span>

### <span data-ttu-id="e7d83-138">Microsoft.Azure.Commands.Automation.Common.StreamType</span><span class="sxs-lookup"><span data-stu-id="e7d83-138">Microsoft.Azure.Commands.Automation.Common.StreamType</span></span>

### <span data-ttu-id="e7d83-139">System.Nullable'1[[System.DateTimeOffset， System.Private.CoreLib， Version=4.0.0.0， Culture=neutral， PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="e7d83-139">System.Nullable\`1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="e7d83-140">System.String</span><span class="sxs-lookup"><span data-stu-id="e7d83-140">System.String</span></span>

## <span data-ttu-id="e7d83-141">輸出</span><span class="sxs-lookup"><span data-stu-id="e7d83-141">OUTPUTS</span></span>

### <span data-ttu-id="e7d83-142">Microsoft.Azure.Commands.Automation.Model.JobStream</span><span class="sxs-lookup"><span data-stu-id="e7d83-142">Microsoft.Azure.Commands.Automation.Model.JobStream</span></span>

## <span data-ttu-id="e7d83-143">筆記</span><span class="sxs-lookup"><span data-stu-id="e7d83-143">NOTES</span></span>

## <span data-ttu-id="e7d83-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="e7d83-144">RELATED LINKS</span></span>

[<span data-ttu-id="e7d83-145">Get-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="e7d83-145">Get-AzAutomationJob</span></span>](./Get-AzAutomationJob.md)

[<span data-ttu-id="e7d83-146">Resume-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="e7d83-146">Resume-AzAutomationJob</span></span>](./Resume-AzAutomationJob.md)

[<span data-ttu-id="e7d83-147">Stop-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="e7d83-147">Stop-AzAutomationJob</span></span>](./Stop-AzAutomationJob.md)

[<span data-ttu-id="e7d83-148">Suspend-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="e7d83-148">Suspend-AzAutomationJob</span></span>](./Suspend-AzAutomationJob.md)


