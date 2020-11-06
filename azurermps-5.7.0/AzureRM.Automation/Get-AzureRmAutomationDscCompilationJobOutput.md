---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: D40BA2E2-50DF-4D51-A4D2-2D02AECBF20F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationdsccompilationjoboutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscCompilationJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscCompilationJobOutput.md
ms.openlocfilehash: e7093f04cfd7b51f00dcc5cbcd6ad3cb98f54bb1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93457488"
---
# <span data-ttu-id="b51ca-101">Get-AzureRmAutomationDscCompilationJobOutput</span><span class="sxs-lookup"><span data-stu-id="b51ca-101">Get-AzureRmAutomationDscCompilationJobOutput</span></span>

## <span data-ttu-id="b51ca-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b51ca-102">SYNOPSIS</span></span>
<span data-ttu-id="b51ca-103">取得自動化 DSC 編譯作業的記錄資料流程。</span><span class="sxs-lookup"><span data-stu-id="b51ca-103">Gets the logging streams of an Automation DSC compilation job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b51ca-104">句法</span><span class="sxs-lookup"><span data-stu-id="b51ca-104">SYNTAX</span></span>

```
Get-AzureRmAutomationDscCompilationJobOutput [-Id] <Guid> [-Stream <CompilationJobStreamType>]
 [-StartTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b51ca-105">說明</span><span class="sxs-lookup"><span data-stu-id="b51ca-105">DESCRIPTION</span></span>
<span data-ttu-id="b51ca-106">**AzureRmAutomationDscCompilationJobOutput** Cmdlet 會在 Azure 自動化中，以 (DSC) 編譯作業的方式，取得 Ap 所需狀態設定的資料流程記錄。</span><span class="sxs-lookup"><span data-stu-id="b51ca-106">The **Get-AzureRmAutomationDscCompilationJobOutput** cmdlet gets the stream records of an APS Desired State Configuration (DSC) compilation job in Azure Automation.</span></span>

## <span data-ttu-id="b51ca-107">示例</span><span class="sxs-lookup"><span data-stu-id="b51ca-107">EXAMPLES</span></span>

### <span data-ttu-id="b51ca-108">範例1：取得 DSC 編譯作業的記錄</span><span class="sxs-lookup"><span data-stu-id="b51ca-108">Example 1: Get the logs for a DSC compilation job</span></span>
```
PS C:\>$Jobs = Get-AzureRmAutomationDscCompilationJob -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17"
PS C:\> $Jobs[0] | Get-AzureRmAutomationDscCompilationJobOutput -Stream "Any"
```

<span data-ttu-id="b51ca-109">第一個命令會使用 Get-AzureRmAutomationDscCompilationJob Cmdlet，透過名為 Contoso17 的自動化帳戶中取得編譯作業。</span><span class="sxs-lookup"><span data-stu-id="b51ca-109">The first command gets the compilation jobs in the Automation account named Contoso17 by using the Get-AzureRmAutomationDscCompilationJob cmdlet.</span></span>
<span data-ttu-id="b51ca-110">該命令會將這些物件儲存在 $Jobs 變數中。</span><span class="sxs-lookup"><span data-stu-id="b51ca-110">The command stores those objects in the $Jobs variable.</span></span>

<span data-ttu-id="b51ca-111">第二個命令會針對 $Jobs 陣列的第一個成員，取得任何資料流程的編譯作業輸出。</span><span class="sxs-lookup"><span data-stu-id="b51ca-111">The second command gets the compilation job output for any stream for the first member of the $Jobs array.</span></span>

## <span data-ttu-id="b51ca-112">參數</span><span class="sxs-lookup"><span data-stu-id="b51ca-112">PARAMETERS</span></span>

### <span data-ttu-id="b51ca-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="b51ca-113">-AutomationAccountName</span></span>
<span data-ttu-id="b51ca-114">指定包含 DSC 編譯作業之自動化帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="b51ca-114">Specifies the name of the Automation account that contains the DSC compilation job.</span></span>

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

### <span data-ttu-id="b51ca-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b51ca-115">-DefaultProfile</span></span>
<span data-ttu-id="b51ca-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="b51ca-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b51ca-117">-識別碼</span><span class="sxs-lookup"><span data-stu-id="b51ca-117">-Id</span></span>
<span data-ttu-id="b51ca-118">指定此 Cmdlet 取得輸出的 DSC 編譯作業的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="b51ca-118">Specifies the unique ID of the DSC compilation job for which this cmdlet gets output.</span></span>

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

### <span data-ttu-id="b51ca-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b51ca-119">-ResourceGroupName</span></span>
<span data-ttu-id="b51ca-120">指定包含此 Cmdlet 取得串流記錄之 DSC 編譯作業之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b51ca-120">Specifies the name of the resource group that contains the DSC compilation job for which this cmdlet gets stream records.</span></span>

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

### <span data-ttu-id="b51ca-121">-StartTime</span><span class="sxs-lookup"><span data-stu-id="b51ca-121">-StartTime</span></span>
<span data-ttu-id="b51ca-122">指定開始時間。</span><span class="sxs-lookup"><span data-stu-id="b51ca-122">Specifies a start time.</span></span>
<span data-ttu-id="b51ca-123">這個 Cmdlet 會在此時間之後取得 DSC 編譯作業輸出的資料流程記錄。</span><span class="sxs-lookup"><span data-stu-id="b51ca-123">This cmdlet gets stream records that the DSC compilation job outputs after this time.</span></span>

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

### <span data-ttu-id="b51ca-124">資料流程</span><span class="sxs-lookup"><span data-stu-id="b51ca-124">-Stream</span></span>
<span data-ttu-id="b51ca-125">指定此 Cmdlet 取得之輸出的串流類型。</span><span class="sxs-lookup"><span data-stu-id="b51ca-125">Specifies the type of stream for the output that this cmdlet gets.</span></span>
<span data-ttu-id="b51ca-126">有效值為：</span><span class="sxs-lookup"><span data-stu-id="b51ca-126">Valid values are:</span></span> 

- <span data-ttu-id="b51ca-127">每</span><span class="sxs-lookup"><span data-stu-id="b51ca-127">Any</span></span> 
- <span data-ttu-id="b51ca-128">警告</span><span class="sxs-lookup"><span data-stu-id="b51ca-128">Warning</span></span> 
- <span data-ttu-id="b51ca-129">出錯</span><span class="sxs-lookup"><span data-stu-id="b51ca-129">Error</span></span> 
- <span data-ttu-id="b51ca-130">冗長</span><span class="sxs-lookup"><span data-stu-id="b51ca-130">Verbose</span></span>

```yaml
Type: CompilationJobStreamType
Parameter Sets: (All)
Aliases: 
Accepted values: Warning, Error, Verbose, Any

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b51ca-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b51ca-131">CommonParameters</span></span>
<span data-ttu-id="b51ca-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b51ca-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b51ca-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b51ca-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b51ca-134">輸入</span><span class="sxs-lookup"><span data-stu-id="b51ca-134">INPUTS</span></span>

### <span data-ttu-id="b51ca-135">所有</span><span class="sxs-lookup"><span data-stu-id="b51ca-135">None</span></span>
<span data-ttu-id="b51ca-136">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="b51ca-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b51ca-137">輸出</span><span class="sxs-lookup"><span data-stu-id="b51ca-137">OUTPUTS</span></span>

### <span data-ttu-id="b51ca-138">JobStream 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="b51ca-138">Microsoft.Azure.Commands.Automation.Model.JobStream</span></span>

## <span data-ttu-id="b51ca-139">筆記</span><span class="sxs-lookup"><span data-stu-id="b51ca-139">NOTES</span></span>

## <span data-ttu-id="b51ca-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="b51ca-140">RELATED LINKS</span></span>

[<span data-ttu-id="b51ca-141">AzureRmAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="b51ca-141">Get-AzureRmAutomationDscCompilationJob</span></span>](./Get-AzureRmAutomationDscCompilationJob.md)

[<span data-ttu-id="b51ca-142">開始-AzureRmAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="b51ca-142">Start-AzureRmAutomationDscCompilationJob</span></span>](./Start-AzureRmAutomationDscCompilationJob.md)


