---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 87E7FA51-427E-4DB8-A6A2-D8638FD3DB8B
online version: https://docs.microsoft.com/powershell/module/az.batch/new-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchJobSchedule.md
ms.openlocfilehash: 63a8ba2d98bd81cbeca3286259920debc10723a6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910762"
---
# <span data-ttu-id="8e750-101">New-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="8e750-101">New-AzBatchJobSchedule</span></span>

## <span data-ttu-id="8e750-102">簡介</span><span class="sxs-lookup"><span data-stu-id="8e750-102">SYNOPSIS</span></span>
<span data-ttu-id="8e750-103">在批次處理服務中建立工作排程。</span><span class="sxs-lookup"><span data-stu-id="8e750-103">Creates a job schedule in the Batch service.</span></span>

## <span data-ttu-id="8e750-104">語法</span><span class="sxs-lookup"><span data-stu-id="8e750-104">SYNTAX</span></span>

```
New-AzBatchJobSchedule [-Id] <String> [-DisplayName <String>] -Schedule <PSSchedule>
 -JobSpecification <PSJobSpecification> [-Metadata <IDictionary>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8e750-105">描述</span><span class="sxs-lookup"><span data-stu-id="8e750-105">DESCRIPTION</span></span>
<span data-ttu-id="8e750-106">**New-AzBatchJobSchedule** Cmdlet 在 Azure 批次處理服務中建立工作排程。</span><span class="sxs-lookup"><span data-stu-id="8e750-106">The **New-AzBatchJobSchedule** cmdlet creates a job schedule in the Azure Batch service.</span></span>
<span data-ttu-id="8e750-107">*BatchAccountCoNtext* 參數會指定此 Cmdlet 建立排程的帳戶。</span><span class="sxs-lookup"><span data-stu-id="8e750-107">The *BatchAccountContext* parameter specifies the account in which this cmdlet creates the schedule.</span></span>

## <span data-ttu-id="8e750-108">例子</span><span class="sxs-lookup"><span data-stu-id="8e750-108">EXAMPLES</span></span>

### <span data-ttu-id="8e750-109">範例 1：建立工作排程</span><span class="sxs-lookup"><span data-stu-id="8e750-109">Example 1: Create a job schedule</span></span>
```
PS C:\>$Schedule = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSSchedule"
PS C:\> $Schedule.RecurrenceInterval = [TimeSpan]::FromDays(1)
PS C:\> $JobSpecification = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSJobSpecification"
PS C:\> $JobSpecification.PoolInformation = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSPoolInformation"
PS C:\> $JobSpecification.PoolInformation.PoolId = "ContosoPool06"
PS C:\> New-AzBatchJobSchedule -Id "JobSchedule17" -Schedule $Schedule -JobSpecification $JobSpecification -BatchContext $Context
```

<span data-ttu-id="8e750-110">此範例會建立工作排程。</span><span class="sxs-lookup"><span data-stu-id="8e750-110">This example creates a job schedule.</span></span>
<span data-ttu-id="8e750-111">前五個命令會建立及修改 **PSSchedule、PSJobS指定** 和 **PSPoolInformation** 物件。 </span><span class="sxs-lookup"><span data-stu-id="8e750-111">The first five commands create and modify **PSSchedule**, **PSJobSpecification**, and **PSPoolInformation** objects.</span></span>
<span data-ttu-id="8e750-112">命令會使用 New-Object Cmdlet 和標準 Azure PowerShell 語法。</span><span class="sxs-lookup"><span data-stu-id="8e750-112">The commands use the New-Object cmdlet and standard Azure PowerShell syntax.</span></span>
<span data-ttu-id="8e750-113">命令會儲存這些物件$Schedule$JobSpecification變數。</span><span class="sxs-lookup"><span data-stu-id="8e750-113">The commands store these objects in the $Schedule and $JobSpecification variables.</span></span>
<span data-ttu-id="8e750-114">最後一個命令會建立具有 ID JobSchedule17 的工作排程。</span><span class="sxs-lookup"><span data-stu-id="8e750-114">The final command creates a job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="8e750-115">此排程會建立週期間隔為一天的作業。</span><span class="sxs-lookup"><span data-stu-id="8e750-115">This schedule creates jobs with a recurrence interval of one day.</span></span>
<span data-ttu-id="8e750-116">工作在具有 ID ContosoPool06 的集中執行，如第五個命令所指定。</span><span class="sxs-lookup"><span data-stu-id="8e750-116">The jobs run on the pool that has the ID ContosoPool06, as specified in the fifth command.</span></span>
<span data-ttu-id="8e750-117">使用 **Get-AzBatchAccountKey** Cmdlet 將上下文指派給$CoNtext變數。</span><span class="sxs-lookup"><span data-stu-id="8e750-117">Use the **Get-AzBatchAccountKey** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="8e750-118">參數</span><span class="sxs-lookup"><span data-stu-id="8e750-118">PARAMETERS</span></span>

### <span data-ttu-id="8e750-119">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="8e750-119">-BatchContext</span></span>
<span data-ttu-id="8e750-120">指定此 Cmdlet 用來與批次處理服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="8e750-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="8e750-121">如果您使用 Get-AzBatchAccount Cmdlet 取得 BatchAccountCoNtext，則與批次處理服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="8e750-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="8e750-122">若要改為使用共用金鑰驗證，請使用 Get-AzBatchAccountKey Cmdlet 取得已填入便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="8e750-122">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="8e750-123">使用共用金鑰驗證時，預設會使用主便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="8e750-123">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="8e750-124">若要變更使用的金鑰，請設定 BatchAccountCoNtext.KeyInUse 屬性。</span><span class="sxs-lookup"><span data-stu-id="8e750-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8e750-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e750-125">-DefaultProfile</span></span>
<span data-ttu-id="8e750-126">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="8e750-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8e750-127">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="8e750-127">-DisplayName</span></span>
<span data-ttu-id="8e750-128">指定工作排程的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="8e750-128">Specifies a display name for the job schedule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e750-129">-Id</span><span class="sxs-lookup"><span data-stu-id="8e750-129">-Id</span></span>
<span data-ttu-id="8e750-130">指定此 Cmdlet 所建立的工作排程識別碼。</span><span class="sxs-lookup"><span data-stu-id="8e750-130">Specifies the ID of the job schedule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="8e750-131">-JobS指定</span><span class="sxs-lookup"><span data-stu-id="8e750-131">-JobSpecification</span></span>
<span data-ttu-id="8e750-132">指定此 Cmdlet 在工作排程中包含的工作詳細資料。</span><span class="sxs-lookup"><span data-stu-id="8e750-132">Specifies the details of the jobs that this cmdlet includes in the job schedule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSJobSpecification
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e750-133">-中繼資料</span><span class="sxs-lookup"><span data-stu-id="8e750-133">-Metadata</span></span>
<span data-ttu-id="8e750-134">指定要新增到工作排程的中繼資料，做為金鑰/值組。</span><span class="sxs-lookup"><span data-stu-id="8e750-134">Specifies metadata, as key/value pairs, to add to the job schedule.</span></span>
<span data-ttu-id="8e750-135">鍵是中繼資料名稱。</span><span class="sxs-lookup"><span data-stu-id="8e750-135">The key is the metadata name.</span></span>
<span data-ttu-id="8e750-136">該值是中繼資料值。</span><span class="sxs-lookup"><span data-stu-id="8e750-136">The value is the metadata value.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e750-137">-排程</span><span class="sxs-lookup"><span data-stu-id="8e750-137">-Schedule</span></span>
<span data-ttu-id="8e750-138">指定決定何時建立工作的排程。</span><span class="sxs-lookup"><span data-stu-id="8e750-138">Specifies the schedule that determines when to create jobs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSSchedule
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e750-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e750-139">CommonParameters</span></span>
<span data-ttu-id="8e750-140">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="8e750-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e750-141">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8e750-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e750-142">輸入</span><span class="sxs-lookup"><span data-stu-id="8e750-142">INPUTS</span></span>

### <span data-ttu-id="8e750-143">System.String</span><span class="sxs-lookup"><span data-stu-id="8e750-143">System.String</span></span>

### <span data-ttu-id="8e750-144">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="8e750-144">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="8e750-145">輸出</span><span class="sxs-lookup"><span data-stu-id="8e750-145">OUTPUTS</span></span>

### <span data-ttu-id="8e750-146">System.Void</span><span class="sxs-lookup"><span data-stu-id="8e750-146">System.Void</span></span>

## <span data-ttu-id="8e750-147">筆記</span><span class="sxs-lookup"><span data-stu-id="8e750-147">NOTES</span></span>

## <span data-ttu-id="8e750-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="8e750-148">RELATED LINKS</span></span>

[<span data-ttu-id="8e750-149">Disable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="8e750-149">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="8e750-150">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="8e750-150">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="8e750-151">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="8e750-151">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="8e750-152">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="8e750-152">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="8e750-153">Remove-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="8e750-153">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="8e750-154">Stop-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="8e750-154">Stop-AzBatchJobSchedule</span></span>](./Stop-AzBatchJobSchedule.md)

[<span data-ttu-id="8e750-155">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8e750-155">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
