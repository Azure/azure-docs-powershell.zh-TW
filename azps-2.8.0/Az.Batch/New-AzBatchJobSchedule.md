---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 87E7FA51-427E-4DB8-A6A2-D8638FD3DB8B
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchJobSchedule.md
ms.openlocfilehash: 836ad4cda6d6631baf0885ac0ec380fdc401fde6
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/13/2020
ms.locfileid: "93799509"
---
# <span data-ttu-id="9265d-101">New-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="9265d-101">New-AzBatchJobSchedule</span></span>

## <span data-ttu-id="9265d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9265d-102">SYNOPSIS</span></span>
<span data-ttu-id="9265d-103">在批次服務中建立作業排程。</span><span class="sxs-lookup"><span data-stu-id="9265d-103">Creates a job schedule in the Batch service.</span></span>

## <span data-ttu-id="9265d-104">句法</span><span class="sxs-lookup"><span data-stu-id="9265d-104">SYNTAX</span></span>

```
New-AzBatchJobSchedule [-Id] <String> [-DisplayName <String>] -Schedule <PSSchedule>
 -JobSpecification <PSJobSpecification> [-Metadata <IDictionary>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9265d-105">說明</span><span class="sxs-lookup"><span data-stu-id="9265d-105">DESCRIPTION</span></span>
<span data-ttu-id="9265d-106">**新的-AzBatchJobSchedule** Cmdlet 會在 Azure Batch service 中建立作業排程。</span><span class="sxs-lookup"><span data-stu-id="9265d-106">The **New-AzBatchJobSchedule** cmdlet creates a job schedule in the Azure Batch service.</span></span>
<span data-ttu-id="9265d-107">*BatchAccountCoNtext* 參數會指定此 Cmdlet 建立排程的帳戶。</span><span class="sxs-lookup"><span data-stu-id="9265d-107">The *BatchAccountContext* parameter specifies the account in which this cmdlet creates the schedule.</span></span>

## <span data-ttu-id="9265d-108">示例</span><span class="sxs-lookup"><span data-stu-id="9265d-108">EXAMPLES</span></span>

### <span data-ttu-id="9265d-109">範例1：建立作業排程</span><span class="sxs-lookup"><span data-stu-id="9265d-109">Example 1: Create a job schedule</span></span>
```
PS C:\>$Schedule = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSSchedule"
PS C:\> $Schedule.RecurrenceInterval = [TimeSpan]::FromDays(1)
PS C:\> $JobSpecification = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSJobSpecification"
PS C:\> $JobSpecification.PoolInformation = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSPoolInformation"
PS C:\> $JobSpecification.PoolInformation.PoolId = "ContosoPool06"
PS C:\> New-AzBatchJobSchedule -Id "JobSchedule17" -Schedule $Schedule -JobSpecification $JobSpecification -BatchContext $Context
```

<span data-ttu-id="9265d-110">這個範例會建立作業排程。</span><span class="sxs-lookup"><span data-stu-id="9265d-110">This example creates a job schedule.</span></span>
<span data-ttu-id="9265d-111">前五個命令會建立及修改 **PSSchedule** 、 **PSJobSpecification** 和 **PSPoolInformation** 物件。</span><span class="sxs-lookup"><span data-stu-id="9265d-111">The first five commands create and modify **PSSchedule** , **PSJobSpecification** , and **PSPoolInformation** objects.</span></span>
<span data-ttu-id="9265d-112">這些命令會使用 New-Object Cmdlet 和標準的 Azure PowerShell 語法。</span><span class="sxs-lookup"><span data-stu-id="9265d-112">The commands use the New-Object cmdlet and standard Azure PowerShell syntax.</span></span>
<span data-ttu-id="9265d-113">這些命令會將這些物件儲存在 $Schedule 並 $JobSpecification 變數中。</span><span class="sxs-lookup"><span data-stu-id="9265d-113">The commands store these objects in the $Schedule and $JobSpecification variables.</span></span>
<span data-ttu-id="9265d-114">最後一個命令會建立具有識別碼 JobSchedule17 的作業排程。</span><span class="sxs-lookup"><span data-stu-id="9265d-114">The final command creates a job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="9265d-115">此排程會建立含一天的定期間隔的工作。</span><span class="sxs-lookup"><span data-stu-id="9265d-115">This schedule creates jobs with a recurrence interval of one day.</span></span>
<span data-ttu-id="9265d-116">作業會在擁有識別碼 ContosoPool06 的池中執行，如5個命令所指定。</span><span class="sxs-lookup"><span data-stu-id="9265d-116">The jobs run on the pool that has the ID ContosoPool06, as specified in the fifth command.</span></span>
<span data-ttu-id="9265d-117">使用 **AzBatchAccountKeys** Cmdlet，將內容指派給 $CoNtext 變數。</span><span class="sxs-lookup"><span data-stu-id="9265d-117">Use the **Get-AzBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="9265d-118">參數</span><span class="sxs-lookup"><span data-stu-id="9265d-118">PARAMETERS</span></span>

### <span data-ttu-id="9265d-119">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="9265d-119">-BatchContext</span></span>
<span data-ttu-id="9265d-120">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="9265d-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="9265d-121">如果您使用 Get-AzBatchAccount Cmdlet 來取得您的 BatchAccountCoNtext，則在與批次服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="9265d-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="9265d-122">若要改為使用共用金鑰驗證，請使用 Get-AzBatchAccountKeys Cmdlet 來取得已填入其便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="9265d-122">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="9265d-123">使用共用金鑰驗證時，預設會使用主要便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="9265d-123">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="9265d-124">若要變更要使用的索引鍵，請設定 BatchAccountCoNtext 屬性。</span><span class="sxs-lookup"><span data-stu-id="9265d-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="9265d-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9265d-125">-DefaultProfile</span></span>
<span data-ttu-id="9265d-126">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9265d-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9265d-127">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="9265d-127">-DisplayName</span></span>
<span data-ttu-id="9265d-128">指定作業排程的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="9265d-128">Specifies a display name for the job schedule.</span></span>

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

### <span data-ttu-id="9265d-129">-識別碼</span><span class="sxs-lookup"><span data-stu-id="9265d-129">-Id</span></span>
<span data-ttu-id="9265d-130">指定此 Cmdlet 建立之作業排程的識別碼。</span><span class="sxs-lookup"><span data-stu-id="9265d-130">Specifies the ID of the job schedule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="9265d-131">-JobSpecification</span><span class="sxs-lookup"><span data-stu-id="9265d-131">-JobSpecification</span></span>
<span data-ttu-id="9265d-132">指定此 Cmdlet 包含在作業排程中之作業的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="9265d-132">Specifies the details of the jobs that this cmdlet includes in the job schedule.</span></span>

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

### <span data-ttu-id="9265d-133">-中繼資料</span><span class="sxs-lookup"><span data-stu-id="9265d-133">-Metadata</span></span>
<span data-ttu-id="9265d-134">指定要新增至作業排程的中繼資料（做為索引鍵/值對）。</span><span class="sxs-lookup"><span data-stu-id="9265d-134">Specifies metadata, as key/value pairs, to add to the job schedule.</span></span>
<span data-ttu-id="9265d-135">金鑰就是中繼資料名稱。</span><span class="sxs-lookup"><span data-stu-id="9265d-135">The key is the metadata name.</span></span>
<span data-ttu-id="9265d-136">此值為中繼資料值。</span><span class="sxs-lookup"><span data-stu-id="9265d-136">The value is the metadata value.</span></span>

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

### <span data-ttu-id="9265d-137">-排程</span><span class="sxs-lookup"><span data-stu-id="9265d-137">-Schedule</span></span>
<span data-ttu-id="9265d-138">指定決定何時建立作業的排程。</span><span class="sxs-lookup"><span data-stu-id="9265d-138">Specifies the schedule that determines when to create jobs.</span></span>

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

### <span data-ttu-id="9265d-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9265d-139">CommonParameters</span></span>
<span data-ttu-id="9265d-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9265d-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9265d-141">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9265d-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9265d-142">輸入</span><span class="sxs-lookup"><span data-stu-id="9265d-142">INPUTS</span></span>

### <span data-ttu-id="9265d-143">System.object</span><span class="sxs-lookup"><span data-stu-id="9265d-143">System.String</span></span>

### <span data-ttu-id="9265d-144">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="9265d-144">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="9265d-145">輸出</span><span class="sxs-lookup"><span data-stu-id="9265d-145">OUTPUTS</span></span>

### <span data-ttu-id="9265d-146">System.void</span><span class="sxs-lookup"><span data-stu-id="9265d-146">System.Void</span></span>

## <span data-ttu-id="9265d-147">筆記</span><span class="sxs-lookup"><span data-stu-id="9265d-147">NOTES</span></span>

## <span data-ttu-id="9265d-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="9265d-148">RELATED LINKS</span></span>

[<span data-ttu-id="9265d-149">Disable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="9265d-149">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="9265d-150">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="9265d-150">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="9265d-151">AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="9265d-151">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="9265d-152">AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="9265d-152">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="9265d-153">移除-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="9265d-153">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="9265d-154">停止 AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="9265d-154">Stop-AzBatchJobSchedule</span></span>](./Stop-AzBatchJobSchedule.md)

[<span data-ttu-id="9265d-155">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="9265d-155">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


