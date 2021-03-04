---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 38BB4F4E-B72B-460E-8DF2-2A7A9CACDB41
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationjoboutputrecord
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJobOutputRecord.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJobOutputRecord.md
ms.openlocfilehash: 2f4fd8c81cadd890cd17f2dd8d6db77c0eef5283
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913606"
---
# <span data-ttu-id="bb58d-101">Get-AzAutomationJobOutputRecord</span><span class="sxs-lookup"><span data-stu-id="bb58d-101">Get-AzAutomationJobOutputRecord</span></span>

## <span data-ttu-id="bb58d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="bb58d-102">SYNOPSIS</span></span>
<span data-ttu-id="bb58d-103">獲得自動化工作輸出記錄的完整輸出。</span><span class="sxs-lookup"><span data-stu-id="bb58d-103">Gets the full output of an Automation job output record.</span></span>

## <span data-ttu-id="bb58d-104">語法</span><span class="sxs-lookup"><span data-stu-id="bb58d-104">SYNTAX</span></span>

```
Get-AzAutomationJobOutputRecord [-JobId] <Guid> [-Id] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bb58d-105">描述</span><span class="sxs-lookup"><span data-stu-id="bb58d-105">DESCRIPTION</span></span>
<span data-ttu-id="bb58d-106">**Get-AzAutomationJobOutputRecord** Cmdlet 會取得自動化工作輸出記錄的完整輸出。</span><span class="sxs-lookup"><span data-stu-id="bb58d-106">The **Get-AzAutomationJobOutputRecord** cmdlet gets the full output of an Automation job output record.</span></span>
<span data-ttu-id="bb58d-107">雖然 **Get-AzAutomationJobOutput** Cmdlet 會列出一或多個工作輸出記錄，但只會以字串形式，以任何輸出記錄的值摘要。</span><span class="sxs-lookup"><span data-stu-id="bb58d-107">Although the **Get-AzAutomationJobOutput** cmdlet lists one or more job output records, it returns only a summary, as a string, of the value of any output record.</span></span>
<span data-ttu-id="bb58d-108">它不會在輸出記錄的原始類型中，回回輸出記錄輸出值的完整值。</span><span class="sxs-lookup"><span data-stu-id="bb58d-108">It does not return the full value of an output record's outputted value in its original type.</span></span>
<span data-ttu-id="bb58d-109">此外，摘要有長度上限，此 Cmdlet 輸出可能會超過完整值。</span><span class="sxs-lookup"><span data-stu-id="bb58d-109">In addition, the summary has a maximum length, which the full value that this cmdlet outputs may exceed.</span></span>

## <span data-ttu-id="bb58d-110">例子</span><span class="sxs-lookup"><span data-stu-id="bb58d-110">EXAMPLES</span></span>

### <span data-ttu-id="bb58d-111">範例 1：取得自動化工作的完整輸出</span><span class="sxs-lookup"><span data-stu-id="bb58d-111">Example 1: Get the full output of an Automation job</span></span>
```
PS C:\>Get-AzAutomationJobOutput -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01" -Stream "Any" | Get-AzAutomationJobOutputRecord
```

<span data-ttu-id="bb58d-112">此命令會獲得具有指定工作識別碼之工作的完整輸出。</span><span class="sxs-lookup"><span data-stu-id="bb58d-112">This command gets the full output of the job that has the specified job ID.</span></span>

## <span data-ttu-id="bb58d-113">參數</span><span class="sxs-lookup"><span data-stu-id="bb58d-113">PARAMETERS</span></span>

### <span data-ttu-id="bb58d-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="bb58d-114">-AutomationAccountName</span></span>
<span data-ttu-id="bb58d-115">指定此 Cmdlet 會獲得工作輸出記錄的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="bb58d-115">Specifies the name of an Automation account for which this cmdlet gets a job output record.</span></span>

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

### <span data-ttu-id="bb58d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb58d-116">-DefaultProfile</span></span>
<span data-ttu-id="bb58d-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="bb58d-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bb58d-118">-Id</span><span class="sxs-lookup"><span data-stu-id="bb58d-118">-Id</span></span>
<span data-ttu-id="bb58d-119">指定要取回此 Cmdlet 的工作輸出記錄的識別碼。</span><span class="sxs-lookup"><span data-stu-id="bb58d-119">Specifies the ID of a job output record for this cmdlet to retrieve.</span></span>

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

### <span data-ttu-id="bb58d-120">-JobId</span><span class="sxs-lookup"><span data-stu-id="bb58d-120">-JobId</span></span>
<span data-ttu-id="bb58d-121">指定此 Cmdlet 會獲得輸出記錄的工作識別碼。</span><span class="sxs-lookup"><span data-stu-id="bb58d-121">Specifies the ID of a job for which this cmdlet gets an output record.</span></span>

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

### <span data-ttu-id="bb58d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb58d-122">-ResourceGroupName</span></span>
<span data-ttu-id="bb58d-123">指定此 Cmdlet 會獲得工作輸出記錄的資源組名。</span><span class="sxs-lookup"><span data-stu-id="bb58d-123">Specifies the name of a resource group for which this cmdlet gets a job output record.</span></span>

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

### <span data-ttu-id="bb58d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb58d-124">CommonParameters</span></span>
<span data-ttu-id="bb58d-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="bb58d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb58d-126">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="bb58d-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb58d-127">輸入</span><span class="sxs-lookup"><span data-stu-id="bb58d-127">INPUTS</span></span>

### <span data-ttu-id="bb58d-128">System.Guid</span><span class="sxs-lookup"><span data-stu-id="bb58d-128">System.Guid</span></span>

### <span data-ttu-id="bb58d-129">System.String</span><span class="sxs-lookup"><span data-stu-id="bb58d-129">System.String</span></span>

## <span data-ttu-id="bb58d-130">輸出</span><span class="sxs-lookup"><span data-stu-id="bb58d-130">OUTPUTS</span></span>

### <span data-ttu-id="bb58d-131">Microsoft.Azure.Commands.Automation.Model.JobStreamRecord</span><span class="sxs-lookup"><span data-stu-id="bb58d-131">Microsoft.Azure.Commands.Automation.Model.JobStreamRecord</span></span>

## <span data-ttu-id="bb58d-132">筆記</span><span class="sxs-lookup"><span data-stu-id="bb58d-132">NOTES</span></span>

## <span data-ttu-id="bb58d-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="bb58d-133">RELATED LINKS</span></span>

[<span data-ttu-id="bb58d-134">Get-AzAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="bb58d-134">Get-AzAutomationJobOutput</span></span>](./Get-AzAutomationJobOutput.md)


