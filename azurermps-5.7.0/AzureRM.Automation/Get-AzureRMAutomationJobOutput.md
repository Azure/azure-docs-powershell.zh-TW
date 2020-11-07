---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B39C4D6B-392A-4C8D-A6FB-886DA1A2BA58
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationjoboutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationJobOutput.md
ms.openlocfilehash: d46dd2e314aa8064b305adb0501ae20480a34418
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623623"
---
# <span data-ttu-id="7cd6d-101">Get-AzureRmAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="7cd6d-101">Get-AzureRmAutomationJobOutput</span></span>

## <span data-ttu-id="7cd6d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7cd6d-102">SYNOPSIS</span></span>
<span data-ttu-id="7cd6d-103">取得自動化作業的輸出。</span><span class="sxs-lookup"><span data-stu-id="7cd6d-103">Gets the output of an Automation job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7cd6d-104">句法</span><span class="sxs-lookup"><span data-stu-id="7cd6d-104">SYNTAX</span></span>

```
Get-AzureRmAutomationJobOutput [-Id] <Guid> [-Stream <StreamType>] [-StartTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7cd6d-105">說明</span><span class="sxs-lookup"><span data-stu-id="7cd6d-105">DESCRIPTION</span></span>
<span data-ttu-id="7cd6d-106">**AzureRmAutomationJobOutput** Cmdlet 會取得 Azure 自動化作業的輸出。</span><span class="sxs-lookup"><span data-stu-id="7cd6d-106">The **Get-AzureRmAutomationJobOutput** cmdlet gets the output of an Azure Automation job.</span></span>

## <span data-ttu-id="7cd6d-107">示例</span><span class="sxs-lookup"><span data-stu-id="7cd6d-107">EXAMPLES</span></span>

### <span data-ttu-id="7cd6d-108">範例1：取得自動化作業的輸出</span><span class="sxs-lookup"><span data-stu-id="7cd6d-108">Example 1: Get the output of an Automation job</span></span>
```
PS C:\>Get-AzureRmAutomationJobOutput -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01" -Stream "Any"
```

<span data-ttu-id="7cd6d-109">這個命令會取得具有指定識別碼之作業的所有輸出。</span><span class="sxs-lookup"><span data-stu-id="7cd6d-109">This command gets all of the output of the job that has the specified ID.</span></span>

## <span data-ttu-id="7cd6d-110">參數</span><span class="sxs-lookup"><span data-stu-id="7cd6d-110">PARAMETERS</span></span>

### <span data-ttu-id="7cd6d-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="7cd6d-111">-AutomationAccountName</span></span>
<span data-ttu-id="7cd6d-112">指定此 Cmdlet 取得作業輸出的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="7cd6d-112">Specifies the name of an Automation account for which this cmdlet gets job output.</span></span>

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

### <span data-ttu-id="7cd6d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cd6d-113">-DefaultProfile</span></span>
<span data-ttu-id="7cd6d-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="7cd6d-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7cd6d-115">-識別碼</span><span class="sxs-lookup"><span data-stu-id="7cd6d-115">-Id</span></span>
<span data-ttu-id="7cd6d-116">指定此 Cmdlet 取得輸出的作業 ID。</span><span class="sxs-lookup"><span data-stu-id="7cd6d-116">Specifies the ID of a job for which this cmdlet gets output.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: JobId

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7cd6d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7cd6d-117">-ResourceGroupName</span></span>
<span data-ttu-id="7cd6d-118">指定此 Cmdlet 取得作業輸出的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="7cd6d-118">Specifies the name of a resource group for which this cmdlet gets job output.</span></span>

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

### <span data-ttu-id="7cd6d-119">-StartTime</span><span class="sxs-lookup"><span data-stu-id="7cd6d-119">-StartTime</span></span>
<span data-ttu-id="7cd6d-120">將開始時間指定為 **DateTimeOffset** 物件。</span><span class="sxs-lookup"><span data-stu-id="7cd6d-120">Specifies a start time as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="7cd6d-121">您可以指定可轉換成有效 **DateTimeOffset** 的字串。</span><span class="sxs-lookup"><span data-stu-id="7cd6d-121">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>
<span data-ttu-id="7cd6d-122">這個 Cmdlet 會檢索在這段時間之後建立的輸出。</span><span class="sxs-lookup"><span data-stu-id="7cd6d-122">The cmdlet retrieves output created after this time.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7cd6d-123">資料流程</span><span class="sxs-lookup"><span data-stu-id="7cd6d-123">-Stream</span></span>
<span data-ttu-id="7cd6d-124">指定輸出的類型。</span><span class="sxs-lookup"><span data-stu-id="7cd6d-124">Specifies the type of output.</span></span>
<span data-ttu-id="7cd6d-125">有效值為：</span><span class="sxs-lookup"><span data-stu-id="7cd6d-125">Valid values are:</span></span> 

- <span data-ttu-id="7cd6d-126">每</span><span class="sxs-lookup"><span data-stu-id="7cd6d-126">Any</span></span>
- <span data-ttu-id="7cd6d-127">Debug</span><span class="sxs-lookup"><span data-stu-id="7cd6d-127">Debug</span></span>
- <span data-ttu-id="7cd6d-128">出錯</span><span class="sxs-lookup"><span data-stu-id="7cd6d-128">Error</span></span>
- <span data-ttu-id="7cd6d-129">收</span><span class="sxs-lookup"><span data-stu-id="7cd6d-129">Output</span></span>
- <span data-ttu-id="7cd6d-130">處理</span><span class="sxs-lookup"><span data-stu-id="7cd6d-130">Progress</span></span>
- <span data-ttu-id="7cd6d-131">冗長</span><span class="sxs-lookup"><span data-stu-id="7cd6d-131">Verbose</span></span>
- <span data-ttu-id="7cd6d-132">警告</span><span class="sxs-lookup"><span data-stu-id="7cd6d-132">Warning</span></span>

```yaml
Type: StreamType
Parameter Sets: (All)
Aliases: 
Accepted values: Any, Progress, Output, Warning, Error, Debug, Verbose

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7cd6d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cd6d-133">CommonParameters</span></span>
<span data-ttu-id="7cd6d-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7cd6d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cd6d-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7cd6d-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cd6d-136">輸入</span><span class="sxs-lookup"><span data-stu-id="7cd6d-136">INPUTS</span></span>

### <span data-ttu-id="7cd6d-137">所有</span><span class="sxs-lookup"><span data-stu-id="7cd6d-137">None</span></span>
<span data-ttu-id="7cd6d-138">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="7cd6d-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7cd6d-139">輸出</span><span class="sxs-lookup"><span data-stu-id="7cd6d-139">OUTPUTS</span></span>

### <span data-ttu-id="7cd6d-140">JobStream 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="7cd6d-140">Microsoft.Azure.Commands.Automation.Model.JobStream</span></span>

## <span data-ttu-id="7cd6d-141">筆記</span><span class="sxs-lookup"><span data-stu-id="7cd6d-141">NOTES</span></span>

## <span data-ttu-id="7cd6d-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="7cd6d-142">RELATED LINKS</span></span>

[<span data-ttu-id="7cd6d-143">AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="7cd6d-143">Get-AzureRmAutomationJob</span></span>](./Get-AzureRMAutomationJob.md)

[<span data-ttu-id="7cd6d-144">Resume-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="7cd6d-144">Resume-AzureRmAutomationJob</span></span>](./Resume-AzureRMAutomationJob.md)

[<span data-ttu-id="7cd6d-145">停止 AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="7cd6d-145">Stop-AzureRmAutomationJob</span></span>](./Stop-AzureRMAutomationJob.md)

[<span data-ttu-id="7cd6d-146">暫停-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="7cd6d-146">Suspend-AzureRmAutomationJob</span></span>](./Suspend-AzureRMAutomationJob.md)


