---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 38BB4F4E-B72B-460E-8DF2-2A7A9CACDB41
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationjoboutputrecord
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationJobOutputRecord.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationJobOutputRecord.md
ms.openlocfilehash: 18551d6d839991cf0eb9e020c62fa0a24207d1e7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449963"
---
# <span data-ttu-id="a2166-101">Get-AzureRmAutomationJobOutputRecord</span><span class="sxs-lookup"><span data-stu-id="a2166-101">Get-AzureRmAutomationJobOutputRecord</span></span>

## <span data-ttu-id="a2166-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a2166-102">SYNOPSIS</span></span>
<span data-ttu-id="a2166-103">取得自動化作業輸出記錄的完整輸出。</span><span class="sxs-lookup"><span data-stu-id="a2166-103">Gets the full output of an Automation job output record.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a2166-104">句法</span><span class="sxs-lookup"><span data-stu-id="a2166-104">SYNTAX</span></span>

```
Get-AzureRmAutomationJobOutputRecord [-JobId] <Guid> [-Id] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a2166-105">說明</span><span class="sxs-lookup"><span data-stu-id="a2166-105">DESCRIPTION</span></span>
<span data-ttu-id="a2166-106">**AzureRmAutomationJobOutputRecord** Cmdlet 會取得自動化作業輸出記錄的完整輸出。</span><span class="sxs-lookup"><span data-stu-id="a2166-106">The **Get-AzureRmAutomationJobOutputRecord** cmdlet gets the full output of an Automation job output record.</span></span>

<span data-ttu-id="a2166-107">雖然 **AzureRmAutomationJobOutput** Cmdlet 會列出一或多個作業輸出記錄，但它只會傳回任何輸出記錄值的摘要（以字串形式）。</span><span class="sxs-lookup"><span data-stu-id="a2166-107">Although the **Get-AzureRmAutomationJobOutput** cmdlet lists one or more job output records, it returns only a summary, as a string, of the value of any output record.</span></span>
<span data-ttu-id="a2166-108">它不會以原始類型傳回輸出記錄的輸出值的完整值。</span><span class="sxs-lookup"><span data-stu-id="a2166-108">It does not return the full value of an output record's outputted value in its original type.</span></span>
<span data-ttu-id="a2166-109">此外，摘要具有最大長度（此 Cmdlet 輸出可能會超過的完整值）。</span><span class="sxs-lookup"><span data-stu-id="a2166-109">In addition, the summary has a maximum length, which the full value that this cmdlet outputs may exceed.</span></span>
<span data-ttu-id="a2166-110">與 **AzureRmAutomationJobOutput** 不同，此 Cmdlet 會針對任何輸出記錄的輸出值，傳回其原始輸出類型中的完整值。</span><span class="sxs-lookup"><span data-stu-id="a2166-110">Unlike **Get-AzureRmAutomationJobOutput** , this cmdlet returns the full value in its originally outputted type, for any output record's outputted value.</span></span>

## <span data-ttu-id="a2166-111">示例</span><span class="sxs-lookup"><span data-stu-id="a2166-111">EXAMPLES</span></span>

### <span data-ttu-id="a2166-112">範例1：取得自動化工作的完整輸出</span><span class="sxs-lookup"><span data-stu-id="a2166-112">Example 1: Get the full output of an Automation job</span></span>
```
PS C:\>Get-AzureRmAutomationJobOutput -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01" -Stream "Any" | Get-AzureRmAutomationJobOutputRecord
```

<span data-ttu-id="a2166-113">這個命令會取得具有指定作業 ID 之作業的完整輸出。</span><span class="sxs-lookup"><span data-stu-id="a2166-113">This command gets the full output of the job that has the specified job ID.</span></span>

## <span data-ttu-id="a2166-114">參數</span><span class="sxs-lookup"><span data-stu-id="a2166-114">PARAMETERS</span></span>

### <span data-ttu-id="a2166-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a2166-115">-AutomationAccountName</span></span>
<span data-ttu-id="a2166-116">指定此 Cmdlet 取得作業輸出記錄的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="a2166-116">Specifies the name of an Automation account for which this cmdlet gets a job output record.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2166-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2166-117">-DefaultProfile</span></span>
<span data-ttu-id="a2166-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="a2166-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2166-119">-識別碼</span><span class="sxs-lookup"><span data-stu-id="a2166-119">-Id</span></span>
<span data-ttu-id="a2166-120">指定此 Cmdlet 要檢索之作業輸出記錄的識別碼。</span><span class="sxs-lookup"><span data-stu-id="a2166-120">Specifies the ID of a job output record for this cmdlet to retrieve.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StreamRecordId

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2166-121">-作業 Id</span><span class="sxs-lookup"><span data-stu-id="a2166-121">-JobId</span></span>
<span data-ttu-id="a2166-122">指定此 Cmdlet 取得輸出記錄的作業 ID。</span><span class="sxs-lookup"><span data-stu-id="a2166-122">Specifies the ID of a job for which this cmdlet gets an output record.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2166-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2166-123">-ResourceGroupName</span></span>
<span data-ttu-id="a2166-124">指定此 Cmdlet 取得作業輸出記錄的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a2166-124">Specifies the name of a resource group for which this cmdlet gets a job output record.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2166-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2166-125">CommonParameters</span></span>
<span data-ttu-id="a2166-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a2166-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2166-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a2166-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2166-128">輸入</span><span class="sxs-lookup"><span data-stu-id="a2166-128">INPUTS</span></span>

### <span data-ttu-id="a2166-129">所有</span><span class="sxs-lookup"><span data-stu-id="a2166-129">None</span></span>
<span data-ttu-id="a2166-130">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="a2166-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a2166-131">輸出</span><span class="sxs-lookup"><span data-stu-id="a2166-131">OUTPUTS</span></span>

### <span data-ttu-id="a2166-132">JobStreamRecord 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="a2166-132">Microsoft.Azure.Commands.Automation.Model.JobStreamRecord</span></span>

## <span data-ttu-id="a2166-133">筆記</span><span class="sxs-lookup"><span data-stu-id="a2166-133">NOTES</span></span>

## <span data-ttu-id="a2166-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="a2166-134">RELATED LINKS</span></span>

[<span data-ttu-id="a2166-135">AzureRmAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="a2166-135">Get-AzureRmAutomationJobOutput</span></span>](./Get-AzureRMAutomationJobOutput.md)


