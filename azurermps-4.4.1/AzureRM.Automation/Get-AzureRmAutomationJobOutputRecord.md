---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 38BB4F4E-B72B-460E-8DF2-2A7A9CACDB41
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationJobOutputRecord.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationJobOutputRecord.md
ms.openlocfilehash: d9ef76273d89f243f5a8d13543442aba16f7a9d9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450077"
---
# <span data-ttu-id="172b1-101">Get-AzureRmAutomationJobOutputRecord</span><span class="sxs-lookup"><span data-stu-id="172b1-101">Get-AzureRmAutomationJobOutputRecord</span></span>

## <span data-ttu-id="172b1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="172b1-102">SYNOPSIS</span></span>
<span data-ttu-id="172b1-103">取得自動化作業輸出記錄的完整輸出。</span><span class="sxs-lookup"><span data-stu-id="172b1-103">Gets the full output of an Automation job output record.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="172b1-104">句法</span><span class="sxs-lookup"><span data-stu-id="172b1-104">SYNTAX</span></span>

```
Get-AzureRmAutomationJobOutputRecord [-JobId] <Guid> [-Id] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="172b1-105">說明</span><span class="sxs-lookup"><span data-stu-id="172b1-105">DESCRIPTION</span></span>
<span data-ttu-id="172b1-106">**AzureRmAutomationJobOutputRecord** Cmdlet 會取得自動化作業輸出記錄的完整輸出。</span><span class="sxs-lookup"><span data-stu-id="172b1-106">The **Get-AzureRmAutomationJobOutputRecord** cmdlet gets the full output of an Automation job output record.</span></span>

<span data-ttu-id="172b1-107">雖然 **AzureRmAutomationJobOutput** Cmdlet 會列出一或多個作業輸出記錄，但它只會傳回任何輸出記錄值的摘要（以字串形式）。</span><span class="sxs-lookup"><span data-stu-id="172b1-107">Although the **Get-AzureRmAutomationJobOutput** cmdlet lists one or more job output records, it returns only a summary, as a string, of the value of any output record.</span></span>
<span data-ttu-id="172b1-108">它不會以原始類型傳回輸出記錄的輸出值的完整值。</span><span class="sxs-lookup"><span data-stu-id="172b1-108">It does not return the full value of an output record's outputted value in its original type.</span></span>
<span data-ttu-id="172b1-109">此外，摘要具有最大長度（此 Cmdlet 輸出可能會超過的完整值）。</span><span class="sxs-lookup"><span data-stu-id="172b1-109">In addition, the summary has a maximum length, which the full value that this cmdlet outputs may exceed.</span></span>
<span data-ttu-id="172b1-110">與 **AzureRmAutomationJobOutput** 不同，此 Cmdlet 會針對任何輸出記錄的輸出值，傳回其原始輸出類型中的完整值。</span><span class="sxs-lookup"><span data-stu-id="172b1-110">Unlike **Get-AzureRmAutomationJobOutput** , this cmdlet returns the full value in its originally outputted type, for any output record's outputted value.</span></span>

## <span data-ttu-id="172b1-111">示例</span><span class="sxs-lookup"><span data-stu-id="172b1-111">EXAMPLES</span></span>

### <span data-ttu-id="172b1-112">範例1：取得自動化工作的完整輸出</span><span class="sxs-lookup"><span data-stu-id="172b1-112">Example 1: Get the full output of an Automation job</span></span>
```
PS C:\>Get-AzureRmAutomationJobOutput -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01" -Stream "Any" | Get-AzureRmAutomationJobOutputRecord
```

<span data-ttu-id="172b1-113">這個命令會取得具有指定作業 ID 之作業的完整輸出。</span><span class="sxs-lookup"><span data-stu-id="172b1-113">This command gets the full output of the job that has the specified job ID.</span></span>

## <span data-ttu-id="172b1-114">參數</span><span class="sxs-lookup"><span data-stu-id="172b1-114">PARAMETERS</span></span>

### <span data-ttu-id="172b1-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="172b1-115">-AutomationAccountName</span></span>
<span data-ttu-id="172b1-116">指定此 Cmdlet 取得作業輸出記錄的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="172b1-116">Specifies the name of an Automation account for which this cmdlet gets a job output record.</span></span>

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

### <span data-ttu-id="172b1-117">-識別碼</span><span class="sxs-lookup"><span data-stu-id="172b1-117">-Id</span></span>
<span data-ttu-id="172b1-118">指定此 Cmdlet 要檢索之作業輸出記錄的識別碼。</span><span class="sxs-lookup"><span data-stu-id="172b1-118">Specifies the ID of a job output record for this cmdlet to retrieve.</span></span>

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

### <span data-ttu-id="172b1-119">-作業 Id</span><span class="sxs-lookup"><span data-stu-id="172b1-119">-JobId</span></span>
<span data-ttu-id="172b1-120">指定此 Cmdlet 取得輸出記錄的作業 ID。</span><span class="sxs-lookup"><span data-stu-id="172b1-120">Specifies the ID of a job for which this cmdlet gets an output record.</span></span>

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

### <span data-ttu-id="172b1-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="172b1-121">-ResourceGroupName</span></span>
<span data-ttu-id="172b1-122">指定此 Cmdlet 取得作業輸出記錄的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="172b1-122">Specifies the name of a resource group for which this cmdlet gets a job output record.</span></span>

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

### <span data-ttu-id="172b1-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="172b1-123">-DefaultProfile</span></span>
<span data-ttu-id="172b1-124">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="172b1-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="172b1-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="172b1-125">CommonParameters</span></span>
<span data-ttu-id="172b1-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="172b1-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="172b1-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="172b1-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="172b1-128">輸入</span><span class="sxs-lookup"><span data-stu-id="172b1-128">INPUTS</span></span>

## <span data-ttu-id="172b1-129">輸出</span><span class="sxs-lookup"><span data-stu-id="172b1-129">OUTPUTS</span></span>

### <span data-ttu-id="172b1-130">JobStreamRecord 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="172b1-130">Microsoft.Azure.Commands.Automation.Model.JobStreamRecord</span></span>

## <span data-ttu-id="172b1-131">筆記</span><span class="sxs-lookup"><span data-stu-id="172b1-131">NOTES</span></span>

## <span data-ttu-id="172b1-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="172b1-132">RELATED LINKS</span></span>

[<span data-ttu-id="172b1-133">AzureRmAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="172b1-133">Get-AzureRmAutomationJobOutput</span></span>](./Get-AzureRMAutomationJobOutput.md)


