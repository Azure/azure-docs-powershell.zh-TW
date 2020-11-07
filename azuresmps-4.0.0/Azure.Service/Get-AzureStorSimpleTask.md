---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: CF3548F6-03FE-44D6-AA2C-1015611C657A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0423fe51a047385ef6395075dd116b4d4189c667
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93966998"
---
# <span data-ttu-id="749b1-101">Get-AzureStorSimpleTask</span><span class="sxs-lookup"><span data-stu-id="749b1-101">Get-AzureStorSimpleTask</span></span>

## <span data-ttu-id="749b1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="749b1-102">SYNOPSIS</span></span>
<span data-ttu-id="749b1-103">取得 StorSimple 裝置上任務的狀態。</span><span class="sxs-lookup"><span data-stu-id="749b1-103">Gets status of a task on a StorSimple device.</span></span>

## <span data-ttu-id="749b1-104">句法</span><span class="sxs-lookup"><span data-stu-id="749b1-104">SYNTAX</span></span>

```
Get-AzureStorSimpleTask -InstanceId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="749b1-105">說明</span><span class="sxs-lookup"><span data-stu-id="749b1-105">DESCRIPTION</span></span>
<span data-ttu-id="749b1-106">**AzureStorSimpleTask** Cmdlet 會檢索在 Azure StorSimple 裝置上以非同步方式執行的任務狀態。</span><span class="sxs-lookup"><span data-stu-id="749b1-106">The **Get-AzureStorSimpleTask** cmdlet retrieves the status of a task that runs asynchronously on an Azure StorSimple device.</span></span>

<span data-ttu-id="749b1-107">當您管理 StorSimple 裝置時，大部分的建立、讀取、更新及刪除動作都可以以非同步方式執行。</span><span class="sxs-lookup"><span data-stu-id="749b1-107">While you manage a StorSimple device, most create, read, update, and delete actions can run asynchronously.</span></span>
<span data-ttu-id="749b1-108">Windows PowerShell 會傳回 **TaskId** 。</span><span class="sxs-lookup"><span data-stu-id="749b1-108">Windows PowerShell returns a **TaskId**.</span></span>
<span data-ttu-id="749b1-109">使用識別碼來取得任務的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="749b1-109">Use the ID to get the current status of the task.</span></span>

## <span data-ttu-id="749b1-110">示例</span><span class="sxs-lookup"><span data-stu-id="749b1-110">EXAMPLES</span></span>

### <span data-ttu-id="749b1-111">範例1：取得任務的狀態</span><span class="sxs-lookup"><span data-stu-id="749b1-111">Example 1: Get the status of a task</span></span>
```
PS C:\>Get-AzureStorSimpleTask -TaskId "53816d8d-a8b5-4c1d-a177-e59007608d6d"
VERBOSE: ClientRequestId: d9c1e8a7-994f-4698-8b42-064600b45cad_PS
VERBOSE: ClientRequestId: aae17c82-6fd3-435e-a965-1c66b3c955fe_PS


AsyncTaskAggregatedResult : Succeeded
Error                     : Microsoft.WindowsAzure.Management.StorSimple.Models.ErrorDetails
Result                    : Succeeded
Status                    : Completed
TaskId                    : 53816d8d-a8b5-4c1d-a177-e59007608d6d
TaskSteps                 : {}
StatusCode                : OK
RequestId                 : e9174990825750bba69383748f23019c
```

<span data-ttu-id="749b1-112">這個命令會取得具有指定識別碼之任務的狀態。</span><span class="sxs-lookup"><span data-stu-id="749b1-112">This command gets the status of the task that has the specified ID.</span></span>
<span data-ttu-id="749b1-113">結果會顯示任務的狀態為 [已完成]，且結果為 [成功]。</span><span class="sxs-lookup"><span data-stu-id="749b1-113">The results show that the task has a status of completed and a result of successful.</span></span>

## <span data-ttu-id="749b1-114">參數</span><span class="sxs-lookup"><span data-stu-id="749b1-114">PARAMETERS</span></span>

### <span data-ttu-id="749b1-115">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="749b1-115">-InstanceId</span></span>
<span data-ttu-id="749b1-116">指定此 Cmdlet 追蹤狀態的任務識別碼。</span><span class="sxs-lookup"><span data-stu-id="749b1-116">Specifies the ID of the task for which this cmdlet tracks status.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: TaskId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="749b1-117">-設定檔</span><span class="sxs-lookup"><span data-stu-id="749b1-117">-Profile</span></span>
<span data-ttu-id="749b1-118">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="749b1-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="749b1-119">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="749b1-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="749b1-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="749b1-120">CommonParameters</span></span>
<span data-ttu-id="749b1-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="749b1-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="749b1-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="749b1-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="749b1-123">輸入</span><span class="sxs-lookup"><span data-stu-id="749b1-123">INPUTS</span></span>

### <span data-ttu-id="749b1-124">所有</span><span class="sxs-lookup"><span data-stu-id="749b1-124">None</span></span>

## <span data-ttu-id="749b1-125">輸出</span><span class="sxs-lookup"><span data-stu-id="749b1-125">OUTPUTS</span></span>

### <span data-ttu-id="749b1-126">JobStatusInfo</span><span class="sxs-lookup"><span data-stu-id="749b1-126">JobStatusInfo</span></span>
<span data-ttu-id="749b1-127">這個 Cmdlet 會傳回包含下欄欄位的 **TaskStatusInfo** 物件：</span><span class="sxs-lookup"><span data-stu-id="749b1-127">This cmdlet returns a **TaskStatusInfo** object which contains the following fields:</span></span> 

- <span data-ttu-id="749b1-128">**錯誤** 。</span><span class="sxs-lookup"><span data-stu-id="749b1-128">**Error**.</span></span>
<span data-ttu-id="749b1-129">**ErrorDetails** ，其中包含程式 **代碼** 和 **訊息** 。</span><span class="sxs-lookup"><span data-stu-id="749b1-129">**ErrorDetails** , which contains **Code** and **Message**.</span></span>
- <span data-ttu-id="749b1-130">**TaskId** 。</span><span class="sxs-lookup"><span data-stu-id="749b1-130">**TaskId**.</span></span>
<span data-ttu-id="749b1-131">**字串** 。</span><span class="sxs-lookup"><span data-stu-id="749b1-131">**String**.</span></span>
<span data-ttu-id="749b1-132">傳回其狀態的任務識別碼。</span><span class="sxs-lookup"><span data-stu-id="749b1-132">The ID of the task for which status is returned.</span></span>
- <span data-ttu-id="749b1-133">**TaskSteps** 。</span><span class="sxs-lookup"><span data-stu-id="749b1-133">**TaskSteps**.</span></span>
<span data-ttu-id="749b1-134">**IList \<TaskStep\>** 。</span><span class="sxs-lookup"><span data-stu-id="749b1-134">**IList\<TaskStep\>**.</span></span>
<span data-ttu-id="749b1-135">每個 **TaskStep** 物件都包含 **詳細資料** 、 **ErrorCode** 、 **訊息** 、 **結果** 和 **狀態** 。</span><span class="sxs-lookup"><span data-stu-id="749b1-135">Each **TaskStep** object contains **Detail** , **ErrorCode** , **Message** , **Result** , and **Status**.</span></span>
- <span data-ttu-id="749b1-136">**結果** 。</span><span class="sxs-lookup"><span data-stu-id="749b1-136">**Result**.</span></span>
<span data-ttu-id="749b1-137">[ **TaskResult** ]，其中包含任務的整體結果。</span><span class="sxs-lookup"><span data-stu-id="749b1-137">**TaskResult** , which contains the overall result of the task.</span></span>
<span data-ttu-id="749b1-138">有效值為：失敗、成功、PartialSuccess、已取消且無效。</span><span class="sxs-lookup"><span data-stu-id="749b1-138">Valid values are: Failed, Succeeded, PartialSuccess, Cancelled, and Invalid.</span></span>
- <span data-ttu-id="749b1-139">**狀態** 。</span><span class="sxs-lookup"><span data-stu-id="749b1-139">**Status**.</span></span>
<span data-ttu-id="749b1-140">[ **TaskStatus** ]，其中包含任務的整體執行狀態。</span><span class="sxs-lookup"><span data-stu-id="749b1-140">**TaskStatus** , which contains the overall running status of the task.</span></span>
<span data-ttu-id="749b1-141">有效值為： Inprogress、無效且已完成。</span><span class="sxs-lookup"><span data-stu-id="749b1-141">Valid values are: Inprogress, Invalid, and Completed.</span></span>
- <span data-ttu-id="749b1-142">**TaskResult** 。</span><span class="sxs-lookup"><span data-stu-id="749b1-142">**TaskResult**.</span></span>
<span data-ttu-id="749b1-143">**TaskResult** ，根據 **結果** 和 **狀態** 計算出的值。</span><span class="sxs-lookup"><span data-stu-id="749b1-143">**TaskResult** , a value computed based on **Result** and **Status**.</span></span>
<span data-ttu-id="749b1-144">有效值為：失敗、成功、InProgress、PartialSuccess、已取消且無效。</span><span class="sxs-lookup"><span data-stu-id="749b1-144">Valid values are: Failed, Succeeded, InProgress, PartialSuccess, Cancelled, and Invalid.</span></span>

## <span data-ttu-id="749b1-145">筆記</span><span class="sxs-lookup"><span data-stu-id="749b1-145">NOTES</span></span>

## <span data-ttu-id="749b1-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="749b1-146">RELATED LINKS</span></span>

