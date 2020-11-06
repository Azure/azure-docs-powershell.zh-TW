---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: D40BA2E2-50DF-4D51-A4D2-2D02AECBF20F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscCompilationJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscCompilationJobOutput.md
ms.openlocfilehash: d38971c15c46cbeaba6e9dda87ad0f3b7febbfd1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452607"
---
# <span data-ttu-id="ecfe7-101">Get-AzureRmAutomationDscCompilationJobOutput</span><span class="sxs-lookup"><span data-stu-id="ecfe7-101">Get-AzureRmAutomationDscCompilationJobOutput</span></span>

## <span data-ttu-id="ecfe7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ecfe7-102">SYNOPSIS</span></span>
<span data-ttu-id="ecfe7-103">取得自動化 DSC 編譯作業的記錄資料流程。</span><span class="sxs-lookup"><span data-stu-id="ecfe7-103">Gets the logging streams of an Automation DSC compilation job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ecfe7-104">句法</span><span class="sxs-lookup"><span data-stu-id="ecfe7-104">SYNTAX</span></span>

```
Get-AzureRmAutomationDscCompilationJobOutput [-Id] <Guid> [-Stream <CompilationJobStreamType>]
 [-StartTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ecfe7-105">說明</span><span class="sxs-lookup"><span data-stu-id="ecfe7-105">DESCRIPTION</span></span>
<span data-ttu-id="ecfe7-106">**AzureRmAutomationDscCompilationJobOutput** Cmdlet 會在 Azure 自動化中，以 (DSC) 編譯作業的方式，取得 Ap 所需狀態設定的資料流程記錄。</span><span class="sxs-lookup"><span data-stu-id="ecfe7-106">The **Get-AzureRmAutomationDscCompilationJobOutput** cmdlet gets the stream records of an APS Desired State Configuration (DSC) compilation job in Azure Automation.</span></span>

## <span data-ttu-id="ecfe7-107">示例</span><span class="sxs-lookup"><span data-stu-id="ecfe7-107">EXAMPLES</span></span>

### <span data-ttu-id="ecfe7-108">範例1：取得 DSC 編譯作業的記錄</span><span class="sxs-lookup"><span data-stu-id="ecfe7-108">Example 1: Get the logs for a DSC compilation job</span></span>
```
PS C:\>$Jobs = Get-AzureRmAutomationDscCompilationJob -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17"
PS C:\> $Jobs[0] | Get-AzureRmAutomationDscCompilationJobOutput -Stream "Any"
```

<span data-ttu-id="ecfe7-109">第一個命令會使用 Get-AzureRmAutomationDscCompilationJob Cmdlet，透過名為 Contoso17 的自動化帳戶中取得編譯作業。</span><span class="sxs-lookup"><span data-stu-id="ecfe7-109">The first command gets the compilation jobs in the Automation account named Contoso17 by using the Get-AzureRmAutomationDscCompilationJob cmdlet.</span></span>
<span data-ttu-id="ecfe7-110">該命令會將這些物件儲存在 $Jobs 變數中。</span><span class="sxs-lookup"><span data-stu-id="ecfe7-110">The command stores those objects in the $Jobs variable.</span></span>

<span data-ttu-id="ecfe7-111">第二個命令會針對 $Jobs 陣列的第一個成員，取得任何資料流程的編譯作業輸出。</span><span class="sxs-lookup"><span data-stu-id="ecfe7-111">The second command gets the compilation job output for any stream for the first member of the $Jobs array.</span></span>

## <span data-ttu-id="ecfe7-112">參數</span><span class="sxs-lookup"><span data-stu-id="ecfe7-112">PARAMETERS</span></span>

### <span data-ttu-id="ecfe7-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ecfe7-113">-AutomationAccountName</span></span>
<span data-ttu-id="ecfe7-114">指定包含 DSC 編譯作業之自動化帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="ecfe7-114">Specifies the name of the Automation account that contains the DSC compilation job.</span></span>

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

### <span data-ttu-id="ecfe7-115">-識別碼</span><span class="sxs-lookup"><span data-stu-id="ecfe7-115">-Id</span></span>
<span data-ttu-id="ecfe7-116">指定此 Cmdlet 取得輸出的 DSC 編譯作業的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="ecfe7-116">Specifies the unique ID of the DSC compilation job for which this cmdlet gets output.</span></span>

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

### <span data-ttu-id="ecfe7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ecfe7-117">-ResourceGroupName</span></span>
<span data-ttu-id="ecfe7-118">指定包含此 Cmdlet 取得串流記錄之 DSC 編譯作業之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ecfe7-118">Specifies the name of the resource group that contains the DSC compilation job for which this cmdlet gets stream records.</span></span>

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

### <span data-ttu-id="ecfe7-119">-StartTime</span><span class="sxs-lookup"><span data-stu-id="ecfe7-119">-StartTime</span></span>
<span data-ttu-id="ecfe7-120">指定開始時間。</span><span class="sxs-lookup"><span data-stu-id="ecfe7-120">Specifies a start time.</span></span>
<span data-ttu-id="ecfe7-121">這個 Cmdlet 會在此時間之後取得 DSC 編譯作業輸出的資料流程記錄。</span><span class="sxs-lookup"><span data-stu-id="ecfe7-121">This cmdlet gets stream records that the DSC compilation job outputs after this time.</span></span>

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

### <span data-ttu-id="ecfe7-122">資料流程</span><span class="sxs-lookup"><span data-stu-id="ecfe7-122">-Stream</span></span>
<span data-ttu-id="ecfe7-123">指定此 Cmdlet 取得之輸出的串流類型。</span><span class="sxs-lookup"><span data-stu-id="ecfe7-123">Specifies the type of stream for the output that this cmdlet gets.</span></span>
<span data-ttu-id="ecfe7-124">有效值為：</span><span class="sxs-lookup"><span data-stu-id="ecfe7-124">Valid values are:</span></span> 

- <span data-ttu-id="ecfe7-125">每</span><span class="sxs-lookup"><span data-stu-id="ecfe7-125">Any</span></span> 
- <span data-ttu-id="ecfe7-126">警告</span><span class="sxs-lookup"><span data-stu-id="ecfe7-126">Warning</span></span> 
- <span data-ttu-id="ecfe7-127">出錯</span><span class="sxs-lookup"><span data-stu-id="ecfe7-127">Error</span></span> 
- <span data-ttu-id="ecfe7-128">冗長</span><span class="sxs-lookup"><span data-stu-id="ecfe7-128">Verbose</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Common.CompilationJobStreamType
Parameter Sets: (All)
Aliases: 
Accepted values: Warning, Error, Verbose, Any

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecfe7-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecfe7-129">-DefaultProfile</span></span>
<span data-ttu-id="ecfe7-130">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ecfe7-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ecfe7-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecfe7-131">CommonParameters</span></span>
<span data-ttu-id="ecfe7-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ecfe7-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecfe7-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ecfe7-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecfe7-134">輸入</span><span class="sxs-lookup"><span data-stu-id="ecfe7-134">INPUTS</span></span>

## <span data-ttu-id="ecfe7-135">輸出</span><span class="sxs-lookup"><span data-stu-id="ecfe7-135">OUTPUTS</span></span>

### <span data-ttu-id="ecfe7-136">JobStream 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="ecfe7-136">Microsoft.Azure.Commands.Automation.Model.JobStream</span></span>

## <span data-ttu-id="ecfe7-137">筆記</span><span class="sxs-lookup"><span data-stu-id="ecfe7-137">NOTES</span></span>

## <span data-ttu-id="ecfe7-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="ecfe7-138">RELATED LINKS</span></span>

[<span data-ttu-id="ecfe7-139">AzureRmAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="ecfe7-139">Get-AzureRmAutomationDscCompilationJob</span></span>](./Get-AzureRmAutomationDscCompilationJob.md)

[<span data-ttu-id="ecfe7-140">開始-AzureRmAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="ecfe7-140">Start-AzureRmAutomationDscCompilationJob</span></span>](./Start-AzureRmAutomationDscCompilationJob.md)


