---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: D40BA2E2-50DF-4D51-A4D2-2D02AECBF20F
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationdsccompilationjoboutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscCompilationJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscCompilationJobOutput.md
ms.openlocfilehash: 1da8d90ca336d2886f7633e646583bc61529fcee
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912482"
---
# <span data-ttu-id="acf59-101">Get-AzAutomationDscCompilationJobOutput</span><span class="sxs-lookup"><span data-stu-id="acf59-101">Get-AzAutomationDscCompilationJobOutput</span></span>

## <span data-ttu-id="acf59-102">簡介</span><span class="sxs-lookup"><span data-stu-id="acf59-102">SYNOPSIS</span></span>
<span data-ttu-id="acf59-103">獲得自動化 DSC 編譯工作的記錄資料流程。</span><span class="sxs-lookup"><span data-stu-id="acf59-103">Gets the logging streams of an Automation DSC compilation job.</span></span>

## <span data-ttu-id="acf59-104">語法</span><span class="sxs-lookup"><span data-stu-id="acf59-104">SYNTAX</span></span>

```
Get-AzAutomationDscCompilationJobOutput [-Id] <Guid> [-Stream <CompilationJobStreamType>]
 [-StartTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="acf59-105">描述</span><span class="sxs-lookup"><span data-stu-id="acf59-105">DESCRIPTION</span></span>
<span data-ttu-id="acf59-106">**Get-AzAutomationDscCompilationJobOutput** Cmdlet 會取得 Azure Automation 中 APS 所需狀態組態 (DSC) 編譯工作的串流記錄。</span><span class="sxs-lookup"><span data-stu-id="acf59-106">The **Get-AzAutomationDscCompilationJobOutput** cmdlet gets the stream records of an APS Desired State Configuration (DSC) compilation job in Azure Automation.</span></span>

## <span data-ttu-id="acf59-107">例子</span><span class="sxs-lookup"><span data-stu-id="acf59-107">EXAMPLES</span></span>

### <span data-ttu-id="acf59-108">範例 1：取得 DSC 編譯工作的記錄</span><span class="sxs-lookup"><span data-stu-id="acf59-108">Example 1: Get the logs for a DSC compilation job</span></span>
```
PS C:\>$Jobs = Get-AzAutomationDscCompilationJob -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17"
PS C:\> $Jobs[0] | Get-AzAutomationDscCompilationJobOutput -Stream "Any"
```

<span data-ttu-id="acf59-109">第一個命令會使用 Get-AzAutomationDscCompilationJob Cmdlet，在名為 Contoso17 的自動化帳戶中Get-AzAutomationDscCompilationJob工作。</span><span class="sxs-lookup"><span data-stu-id="acf59-109">The first command gets the compilation jobs in the Automation account named Contoso17 by using the Get-AzAutomationDscCompilationJob cmdlet.</span></span>
<span data-ttu-id="acf59-110">命令會儲存這些物件$Jobs變數。</span><span class="sxs-lookup"><span data-stu-id="acf59-110">The command stores those objects in the $Jobs variable.</span></span>
<span data-ttu-id="acf59-111">第二個命令會針對陣列中第一個成員的任何串流，獲得編譯$Jobs輸出。</span><span class="sxs-lookup"><span data-stu-id="acf59-111">The second command gets the compilation job output for any stream for the first member of the $Jobs array.</span></span>

## <span data-ttu-id="acf59-112">參數</span><span class="sxs-lookup"><span data-stu-id="acf59-112">PARAMETERS</span></span>

### <span data-ttu-id="acf59-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="acf59-113">-AutomationAccountName</span></span>
<span data-ttu-id="acf59-114">指定包含 DSC 編譯工作的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="acf59-114">Specifies the name of the Automation account that contains the DSC compilation job.</span></span>

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

### <span data-ttu-id="acf59-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acf59-115">-DefaultProfile</span></span>
<span data-ttu-id="acf59-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="acf59-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="acf59-117">-Id</span><span class="sxs-lookup"><span data-stu-id="acf59-117">-Id</span></span>
<span data-ttu-id="acf59-118">指定此 Cmdlet 可輸出之 DSC 編譯工作的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="acf59-118">Specifies the unique ID of the DSC compilation job for which this cmdlet gets output.</span></span>

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

### <span data-ttu-id="acf59-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="acf59-119">-ResourceGroupName</span></span>
<span data-ttu-id="acf59-120">指定包含 DSC 編譯工作的資源組名，此 Cmdlet 會針對該工作獲得串流記錄。</span><span class="sxs-lookup"><span data-stu-id="acf59-120">Specifies the name of the resource group that contains the DSC compilation job for which this cmdlet gets stream records.</span></span>

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

### <span data-ttu-id="acf59-121">-StartTime</span><span class="sxs-lookup"><span data-stu-id="acf59-121">-StartTime</span></span>
<span data-ttu-id="acf59-122">指定開始時間。</span><span class="sxs-lookup"><span data-stu-id="acf59-122">Specifies a start time.</span></span>
<span data-ttu-id="acf59-123">此 Cmdlet 會獲得 DSC 編譯工作在此時間之後輸出的串流記錄。</span><span class="sxs-lookup"><span data-stu-id="acf59-123">This cmdlet gets stream records that the DSC compilation job outputs after this time.</span></span>

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

### <span data-ttu-id="acf59-124">-Stream</span><span class="sxs-lookup"><span data-stu-id="acf59-124">-Stream</span></span>
<span data-ttu-id="acf59-125">指定此 Cmdlet 獲得輸出的串流類型。</span><span class="sxs-lookup"><span data-stu-id="acf59-125">Specifies the type of stream for the output that this cmdlet gets.</span></span>
<span data-ttu-id="acf59-126">有效的值為：</span><span class="sxs-lookup"><span data-stu-id="acf59-126">Valid values are:</span></span> 
- <span data-ttu-id="acf59-127">任何</span><span class="sxs-lookup"><span data-stu-id="acf59-127">Any</span></span> 
- <span data-ttu-id="acf59-128">警告</span><span class="sxs-lookup"><span data-stu-id="acf59-128">Warning</span></span> 
- <span data-ttu-id="acf59-129">錯誤</span><span class="sxs-lookup"><span data-stu-id="acf59-129">Error</span></span> 
- <span data-ttu-id="acf59-130">詳細</span><span class="sxs-lookup"><span data-stu-id="acf59-130">Verbose</span></span>

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

### <span data-ttu-id="acf59-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acf59-131">CommonParameters</span></span>
<span data-ttu-id="acf59-132">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="acf59-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acf59-133">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="acf59-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acf59-134">輸入</span><span class="sxs-lookup"><span data-stu-id="acf59-134">INPUTS</span></span>

### <span data-ttu-id="acf59-135">System.Guid</span><span class="sxs-lookup"><span data-stu-id="acf59-135">System.Guid</span></span>

### <span data-ttu-id="acf59-136">Microsoft.Azure.Commands.Automation.Common.CompilationJobStreamType</span><span class="sxs-lookup"><span data-stu-id="acf59-136">Microsoft.Azure.Commands.Automation.Common.CompilationJobStreamType</span></span>

### <span data-ttu-id="acf59-137">System.Nullable'1[[System.DateTimeOffset， System.Private.CoreLib， Version=4.0.0.0， Culture=neutral， PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="acf59-137">System.Nullable\`1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="acf59-138">System.String</span><span class="sxs-lookup"><span data-stu-id="acf59-138">System.String</span></span>

## <span data-ttu-id="acf59-139">輸出</span><span class="sxs-lookup"><span data-stu-id="acf59-139">OUTPUTS</span></span>

### <span data-ttu-id="acf59-140">Microsoft.Azure.Commands.Automation.Model.JobStream</span><span class="sxs-lookup"><span data-stu-id="acf59-140">Microsoft.Azure.Commands.Automation.Model.JobStream</span></span>

## <span data-ttu-id="acf59-141">筆記</span><span class="sxs-lookup"><span data-stu-id="acf59-141">NOTES</span></span>

## <span data-ttu-id="acf59-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="acf59-142">RELATED LINKS</span></span>

[<span data-ttu-id="acf59-143">Get-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="acf59-143">Get-AzAutomationDscCompilationJob</span></span>](./Get-AzAutomationDscCompilationJob.md)

[<span data-ttu-id="acf59-144">Start-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="acf59-144">Start-AzAutomationDscCompilationJob</span></span>](./Start-AzAutomationDscCompilationJob.md)


