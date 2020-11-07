---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: D077DB50-12BC-45AB-8EAC-57810DA83035
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchremotedesktopprotocolfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchRemoteDesktopProtocolFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchRemoteDesktopProtocolFile.md
ms.openlocfilehash: 812edce5ba6a9c1aa4582538c3fda510efdb7175
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624622"
---
# <span data-ttu-id="336a0-101">Get-AzureBatchRemoteDesktopProtocolFile</span><span class="sxs-lookup"><span data-stu-id="336a0-101">Get-AzureBatchRemoteDesktopProtocolFile</span></span>

## <span data-ttu-id="336a0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="336a0-102">SYNOPSIS</span></span>
<span data-ttu-id="336a0-103">從計算節點取得 RDP 檔案。</span><span class="sxs-lookup"><span data-stu-id="336a0-103">Gets an RDP file from a compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="336a0-104">句法</span><span class="sxs-lookup"><span data-stu-id="336a0-104">SYNTAX</span></span>

### <span data-ttu-id="336a0-105">Id_Path (預設) </span><span class="sxs-lookup"><span data-stu-id="336a0-105">Id_Path (Default)</span></span>
```
Get-AzureBatchRemoteDesktopProtocolFile [-PoolId] <String> [-ComputeNodeId] <String> -DestinationPath <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="336a0-106">Id_Stream</span><span class="sxs-lookup"><span data-stu-id="336a0-106">Id_Stream</span></span>
```
Get-AzureBatchRemoteDesktopProtocolFile [-PoolId] <String> [-ComputeNodeId] <String>
 -DestinationStream <Stream> -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="336a0-107">InputObject_Path</span><span class="sxs-lookup"><span data-stu-id="336a0-107">InputObject_Path</span></span>
```
Get-AzureBatchRemoteDesktopProtocolFile [[-ComputeNode] <PSComputeNode>] -DestinationPath <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="336a0-108">InputObject_Stream</span><span class="sxs-lookup"><span data-stu-id="336a0-108">InputObject_Stream</span></span>
```
Get-AzureBatchRemoteDesktopProtocolFile [[-ComputeNode] <PSComputeNode>] -DestinationStream <Stream>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="336a0-109">說明</span><span class="sxs-lookup"><span data-stu-id="336a0-109">DESCRIPTION</span></span>
<span data-ttu-id="336a0-110">**AzureBatchRemoteDesktopProtocolFile** Cmdlet 會從計算節點取得遠端桌面通訊協定 (RDP) 檔案，並將它儲存為檔案或使用者提供的資料流程。</span><span class="sxs-lookup"><span data-stu-id="336a0-110">The **Get-AzureBatchRemoteDesktopProtocolFile** cmdlet gets a Remote Desktop Protocol (RDP) file from a compute node and saves it as a file or to a user supplied stream.</span></span>

## <span data-ttu-id="336a0-111">示例</span><span class="sxs-lookup"><span data-stu-id="336a0-111">EXAMPLES</span></span>

### <span data-ttu-id="336a0-112">範例1：從指定的計算節點取得 RDP 檔案並儲存檔案</span><span class="sxs-lookup"><span data-stu-id="336a0-112">Example 1: Get an RDP file from a specified compute node and save the file</span></span>
```
PS C:\>Get-AzureBatchRemoteDesktopProtocolFile -PoolId "Pool06" -ComputeNodeId "ComputeNode01" -DestinationPath "C:\PowerShell\ComputeNode01.rdp" -BatchContext $Context
```

<span data-ttu-id="336a0-113">這個命令會從具有 ID Pool06 的 ComputeNode01 中的 [計算] 節點取得 RDP 檔案。</span><span class="sxs-lookup"><span data-stu-id="336a0-113">This command gets an RDP file from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool06.</span></span>
<span data-ttu-id="336a0-114">該命令會將 .rdp 檔案另存為 C:\PowerShell\MyComputeNode.rdp。</span><span class="sxs-lookup"><span data-stu-id="336a0-114">The command saves the .rdp file as C:\PowerShell\MyComputeNode.rdp.</span></span>
<span data-ttu-id="336a0-115">使用 Get-AzureRmBatchAccountKeys Cmdlet 將內容指派給 $CoNtext 變數。</span><span class="sxs-lookup"><span data-stu-id="336a0-115">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="336a0-116">範例2：從計算節點取得 RDP 檔案，並使用管線儲存檔案</span><span class="sxs-lookup"><span data-stu-id="336a0-116">Example 2: Get an RDP file from a compute node and save the file by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchComputeNode -PoolId "Pool06" -Id "ComputeNode02" -BatchContext $Context | Get-AzureBatchRemoteDesktopProtocolFile -DestinationPath "C:\PowerShell\MyComputeNode02.rdp" -BatchContext $Context
```

<span data-ttu-id="336a0-117">這個命令會在擁有 ID Pool06 的池中取得 ID 為 ComputeNode02 的 compute 節點。</span><span class="sxs-lookup"><span data-stu-id="336a0-117">This command gets the compute node that has the ID ComputeNode02 in the pool that has the ID Pool06.</span></span>
<span data-ttu-id="336a0-118">命令會使用管線運算子，將該計算節點傳到目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="336a0-118">The command passes that compute node to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="336a0-119">目前的 Cmdlet 會從 [計算] 節點取得 rpd 檔案，然後將內容另存為名為 C:\PowerShell\MyComputeNode02.rdp. 的檔案。</span><span class="sxs-lookup"><span data-stu-id="336a0-119">The current cmdlet gets an .rpd file from the compute node, and then saves the contents as a file that is named C:\PowerShell\MyComputeNode02.rdp.</span></span>

### <span data-ttu-id="336a0-120">範例3：從指定的計算節點取得 RDP 檔案，並將它引導至資料流程</span><span class="sxs-lookup"><span data-stu-id="336a0-120">Example 3: Get a RDP file from a specified compute node and direct it to a stream</span></span>
```
PS C:\>$Stream = New-Object -TypeName "System.IO.MemoryStream"
PS C:\> Get-AzureBatchRemoteDesktopProtocolFile "Pool06" -ComputeNodeId "ComputeNode03" -DestinationStream $Stream -BatchContext $Context
```

<span data-ttu-id="336a0-121">第一個命令會使用 New-Object Cmdlet 建立串流，然後將它儲存在 $Stream 變數中。</span><span class="sxs-lookup"><span data-stu-id="336a0-121">The first command creates a stream by using the New-Object cmdlet, and then stores it in the $Stream variable.</span></span>
<span data-ttu-id="336a0-122">第二個命令會從計算節點中取得一個 .rdp 檔案，並在擁有 ID Pool06 的池中包含 ID ComputeNode03。</span><span class="sxs-lookup"><span data-stu-id="336a0-122">The second command gets an .rdp file from the compute node that has the ID ComputeNode03 in the pool that has the ID Pool06.</span></span>
<span data-ttu-id="336a0-123">命令會將檔案內容定向至 $Stream 中的資料流程。</span><span class="sxs-lookup"><span data-stu-id="336a0-123">The command directs file contents to the stream in $Stream.</span></span>

## <span data-ttu-id="336a0-124">參數</span><span class="sxs-lookup"><span data-stu-id="336a0-124">PARAMETERS</span></span>

### <span data-ttu-id="336a0-125">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="336a0-125">-BatchContext</span></span>
<span data-ttu-id="336a0-126">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="336a0-126">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="336a0-127">如果您使用 Get-AzureRmBatchAccount Cmdlet 來取得您的 BatchAccountCoNtext，則在與批次服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="336a0-127">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="336a0-128">若要改為使用共用金鑰驗證，請使用 Get-AzureRmBatchAccountKeys Cmdlet 來取得已填入其便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="336a0-128">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="336a0-129">使用共用金鑰驗證時，預設會使用主要便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="336a0-129">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="336a0-130">若要變更要使用的索引鍵，請設定 BatchAccountCoNtext 屬性。</span><span class="sxs-lookup"><span data-stu-id="336a0-130">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="336a0-131">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="336a0-131">-ComputeNode</span></span>
<span data-ttu-id="336a0-132">將 .rdp 檔案指向的計算節點指定為 **PSComputeNode** 物件。</span><span class="sxs-lookup"><span data-stu-id="336a0-132">Specifies a compute node, as a **PSComputeNode** object, to which the .rdp file points.</span></span>
<span data-ttu-id="336a0-133">若要取得計算節點物件，請使用 Get-AzureBatchComputeNode Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="336a0-133">To obtain a compute node object, use the Get-AzureBatchComputeNode cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSComputeNode
Parameter Sets: InputObject_Path, InputObject_Stream
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="336a0-134">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="336a0-134">-ComputeNodeId</span></span>
<span data-ttu-id="336a0-135">指定 .rdp 檔案指向的計算節點 ID。</span><span class="sxs-lookup"><span data-stu-id="336a0-135">Specifies the ID of the compute node to which the .rdp file points.</span></span>

```yaml
Type: System.String
Parameter Sets: Id_Path, Id_Stream
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="336a0-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="336a0-136">-DefaultProfile</span></span>
<span data-ttu-id="336a0-137">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="336a0-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="336a0-138">-DestinationPath</span><span class="sxs-lookup"><span data-stu-id="336a0-138">-DestinationPath</span></span>
<span data-ttu-id="336a0-139">指定此 Cmdlet 儲存 .rdp 檔案的檔路徑。</span><span class="sxs-lookup"><span data-stu-id="336a0-139">Specifies the file path where this cmdlet saves the .rdp file.</span></span>

```yaml
Type: System.String
Parameter Sets: Id_Path, InputObject_Path
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="336a0-140">-DestinationStream</span><span class="sxs-lookup"><span data-stu-id="336a0-140">-DestinationStream</span></span>
<span data-ttu-id="336a0-141">指定此 Cmdlet 將 RDP 資料導向到哪個資料流程。</span><span class="sxs-lookup"><span data-stu-id="336a0-141">Specifies the stream into which this cmdlet directs the RDP data.</span></span>
<span data-ttu-id="336a0-142">這個 Cmdlet 不會關閉或倒帶此資料流程。</span><span class="sxs-lookup"><span data-stu-id="336a0-142">This cmdlet does not close or rewind this stream.</span></span>

```yaml
Type: System.IO.Stream
Parameter Sets: Id_Stream, InputObject_Stream
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="336a0-143">-PoolId</span><span class="sxs-lookup"><span data-stu-id="336a0-143">-PoolId</span></span>
<span data-ttu-id="336a0-144">指定包含 [計算] 節點（這個 Cmdlet 取得 .rdp 檔案）的池 ID。</span><span class="sxs-lookup"><span data-stu-id="336a0-144">Specifies the ID of the pool that contains the compute node from which this cmdlet gets an .rdp file.</span></span>

```yaml
Type: System.String
Parameter Sets: Id_Path, Id_Stream
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="336a0-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="336a0-145">CommonParameters</span></span>
<span data-ttu-id="336a0-146">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="336a0-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="336a0-147">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="336a0-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="336a0-148">輸入</span><span class="sxs-lookup"><span data-stu-id="336a0-148">INPUTS</span></span>

### <span data-ttu-id="336a0-149">System.object</span><span class="sxs-lookup"><span data-stu-id="336a0-149">System.String</span></span>

### <span data-ttu-id="336a0-150">Microsoft.Azure.Commands.Batch。PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="336a0-150">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>
<span data-ttu-id="336a0-151">參數： ComputeNode (ByValue) </span><span class="sxs-lookup"><span data-stu-id="336a0-151">Parameters: ComputeNode (ByValue)</span></span>

### <span data-ttu-id="336a0-152">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="336a0-152">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="336a0-153">參數： BatchCoNtext (ByValue) </span><span class="sxs-lookup"><span data-stu-id="336a0-153">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="336a0-154">輸出</span><span class="sxs-lookup"><span data-stu-id="336a0-154">OUTPUTS</span></span>

### <span data-ttu-id="336a0-155">System.void</span><span class="sxs-lookup"><span data-stu-id="336a0-155">System.Void</span></span>

## <span data-ttu-id="336a0-156">筆記</span><span class="sxs-lookup"><span data-stu-id="336a0-156">NOTES</span></span>

## <span data-ttu-id="336a0-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="336a0-157">RELATED LINKS</span></span>

[<span data-ttu-id="336a0-158">AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="336a0-158">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="336a0-159">AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="336a0-159">Get-AzureBatchComputeNode</span></span>](./Get-AzureBatchComputeNode.md)

[<span data-ttu-id="336a0-160">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="336a0-160">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


