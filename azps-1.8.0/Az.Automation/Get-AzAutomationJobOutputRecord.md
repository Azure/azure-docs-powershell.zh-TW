---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 38BB4F4E-B72B-460E-8DF2-2A7A9CACDB41
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationjoboutputrecord
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJobOutputRecord.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJobOutputRecord.md
ms.openlocfilehash: f5c6976ca1fa398c38f642cef757f0e7956f40c1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93623055"
---
# <span data-ttu-id="391a5-101">Get-AzAutomationJobOutputRecord</span><span class="sxs-lookup"><span data-stu-id="391a5-101">Get-AzAutomationJobOutputRecord</span></span>

## <span data-ttu-id="391a5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="391a5-102">SYNOPSIS</span></span>
<span data-ttu-id="391a5-103">取得自動化作業輸出記錄的完整輸出。</span><span class="sxs-lookup"><span data-stu-id="391a5-103">Gets the full output of an Automation job output record.</span></span>

## <span data-ttu-id="391a5-104">句法</span><span class="sxs-lookup"><span data-stu-id="391a5-104">SYNTAX</span></span>

```
Get-AzAutomationJobOutputRecord [-JobId] <Guid> [-Id] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="391a5-105">說明</span><span class="sxs-lookup"><span data-stu-id="391a5-105">DESCRIPTION</span></span>
<span data-ttu-id="391a5-106">**AzAutomationJobOutputRecord** Cmdlet 會取得自動化作業輸出記錄的完整輸出。</span><span class="sxs-lookup"><span data-stu-id="391a5-106">The **Get-AzAutomationJobOutputRecord** cmdlet gets the full output of an Automation job output record.</span></span>
<span data-ttu-id="391a5-107">雖然 **AzAutomationJobOutput** Cmdlet 會列出一或多個作業輸出記錄，但它只會傳回任何輸出記錄值的摘要（以字串形式）。</span><span class="sxs-lookup"><span data-stu-id="391a5-107">Although the **Get-AzAutomationJobOutput** cmdlet lists one or more job output records, it returns only a summary, as a string, of the value of any output record.</span></span>
<span data-ttu-id="391a5-108">它不會以原始類型傳回輸出記錄的輸出值的完整值。</span><span class="sxs-lookup"><span data-stu-id="391a5-108">It does not return the full value of an output record's outputted value in its original type.</span></span>
<span data-ttu-id="391a5-109">此外，摘要具有最大長度（此 Cmdlet 輸出可能會超過的完整值）。</span><span class="sxs-lookup"><span data-stu-id="391a5-109">In addition, the summary has a maximum length, which the full value that this cmdlet outputs may exceed.</span></span>
<span data-ttu-id="391a5-110">與 **AzAutomationJobOutput** 不同，此 Cmdlet 會針對任何輸出記錄的輸出值，傳回其原始輸出類型中的完整值。</span><span class="sxs-lookup"><span data-stu-id="391a5-110">Unlike **Get-AzAutomationJobOutput** , this cmdlet returns the full value in its originally outputted type, for any output record's outputted value.</span></span>

## <span data-ttu-id="391a5-111">示例</span><span class="sxs-lookup"><span data-stu-id="391a5-111">EXAMPLES</span></span>

### <span data-ttu-id="391a5-112">範例1：取得自動化工作的完整輸出</span><span class="sxs-lookup"><span data-stu-id="391a5-112">Example 1: Get the full output of an Automation job</span></span>
```
PS C:\>Get-AzAutomationJobOutput -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01" -Stream "Any" | Get-AzAutomationJobOutputRecord
```

<span data-ttu-id="391a5-113">這個命令會取得具有指定作業 ID 之作業的完整輸出。</span><span class="sxs-lookup"><span data-stu-id="391a5-113">This command gets the full output of the job that has the specified job ID.</span></span>

## <span data-ttu-id="391a5-114">參數</span><span class="sxs-lookup"><span data-stu-id="391a5-114">PARAMETERS</span></span>

### <span data-ttu-id="391a5-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="391a5-115">-AutomationAccountName</span></span>
<span data-ttu-id="391a5-116">指定此 Cmdlet 取得作業輸出記錄的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="391a5-116">Specifies the name of an Automation account for which this cmdlet gets a job output record.</span></span>

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

### <span data-ttu-id="391a5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="391a5-117">-DefaultProfile</span></span>
<span data-ttu-id="391a5-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="391a5-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="391a5-119">-識別碼</span><span class="sxs-lookup"><span data-stu-id="391a5-119">-Id</span></span>
<span data-ttu-id="391a5-120">指定此 Cmdlet 要檢索之作業輸出記錄的識別碼。</span><span class="sxs-lookup"><span data-stu-id="391a5-120">Specifies the ID of a job output record for this cmdlet to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StreamRecordId

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="391a5-121">-作業 Id</span><span class="sxs-lookup"><span data-stu-id="391a5-121">-JobId</span></span>
<span data-ttu-id="391a5-122">指定此 Cmdlet 取得輸出記錄的作業 ID。</span><span class="sxs-lookup"><span data-stu-id="391a5-122">Specifies the ID of a job for which this cmdlet gets an output record.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="391a5-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="391a5-123">-ResourceGroupName</span></span>
<span data-ttu-id="391a5-124">指定此 Cmdlet 取得作業輸出記錄的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="391a5-124">Specifies the name of a resource group for which this cmdlet gets a job output record.</span></span>

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

### <span data-ttu-id="391a5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="391a5-125">CommonParameters</span></span>
<span data-ttu-id="391a5-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="391a5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="391a5-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="391a5-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="391a5-128">輸入</span><span class="sxs-lookup"><span data-stu-id="391a5-128">INPUTS</span></span>

### <span data-ttu-id="391a5-129">Guid.empty</span><span class="sxs-lookup"><span data-stu-id="391a5-129">System.Guid</span></span>

### <span data-ttu-id="391a5-130">System.object</span><span class="sxs-lookup"><span data-stu-id="391a5-130">System.String</span></span>

## <span data-ttu-id="391a5-131">輸出</span><span class="sxs-lookup"><span data-stu-id="391a5-131">OUTPUTS</span></span>

### <span data-ttu-id="391a5-132">JobStreamRecord 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="391a5-132">Microsoft.Azure.Commands.Automation.Model.JobStreamRecord</span></span>

## <span data-ttu-id="391a5-133">筆記</span><span class="sxs-lookup"><span data-stu-id="391a5-133">NOTES</span></span>

## <span data-ttu-id="391a5-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="391a5-134">RELATED LINKS</span></span>

[<span data-ttu-id="391a5-135">AzAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="391a5-135">Get-AzAutomationJobOutput</span></span>](./Get-AzAutomationJobOutput.md)


