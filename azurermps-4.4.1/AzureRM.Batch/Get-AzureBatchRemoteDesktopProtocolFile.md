---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: D077DB50-12BC-45AB-8EAC-57810DA83035
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchRemoteDesktopProtocolFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchRemoteDesktopProtocolFile.md
ms.openlocfilehash: 37d91dc6fd9d90291c7b619fdb9839d6d9af83b7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93457315"
---
# <span data-ttu-id="41c4d-101">Get-AzureBatchRemoteDesktopProtocolFile</span><span class="sxs-lookup"><span data-stu-id="41c4d-101">Get-AzureBatchRemoteDesktopProtocolFile</span></span>

## <span data-ttu-id="41c4d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="41c4d-102">SYNOPSIS</span></span>
<span data-ttu-id="41c4d-103">從計算節點取得 RDP 檔案。</span><span class="sxs-lookup"><span data-stu-id="41c4d-103">Gets an RDP file from a compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="41c4d-104">句法</span><span class="sxs-lookup"><span data-stu-id="41c4d-104">SYNTAX</span></span>

### <span data-ttu-id="41c4d-105">Id_Path (預設) </span><span class="sxs-lookup"><span data-stu-id="41c4d-105">Id_Path (Default)</span></span>
```
Get-AzureBatchRemoteDesktopProtocolFile [-PoolId] <String> [-ComputeNodeId] <String> -DestinationPath <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="41c4d-106">Id_Stream</span><span class="sxs-lookup"><span data-stu-id="41c4d-106">Id_Stream</span></span>
```
Get-AzureBatchRemoteDesktopProtocolFile [-PoolId] <String> [-ComputeNodeId] <String>
 -DestinationStream <Stream> -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="41c4d-107">InputObject_Path</span><span class="sxs-lookup"><span data-stu-id="41c4d-107">InputObject_Path</span></span>
```
Get-AzureBatchRemoteDesktopProtocolFile [[-ComputeNode] <PSComputeNode>] -DestinationPath <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="41c4d-108">InputObject_Stream</span><span class="sxs-lookup"><span data-stu-id="41c4d-108">InputObject_Stream</span></span>
```
Get-AzureBatchRemoteDesktopProtocolFile [[-ComputeNode] <PSComputeNode>] -DestinationStream <Stream>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="41c4d-109">說明</span><span class="sxs-lookup"><span data-stu-id="41c4d-109">DESCRIPTION</span></span>
<span data-ttu-id="41c4d-110">**AzureBatchRemoteDesktopProtocolFile** Cmdlet 會從計算節點取得遠端桌面通訊協定 (RDP) 檔案，並將它儲存為檔案或使用者提供的資料流程。</span><span class="sxs-lookup"><span data-stu-id="41c4d-110">The **Get-AzureBatchRemoteDesktopProtocolFile** cmdlet gets a Remote Desktop Protocol (RDP) file from a compute node and saves it as a file or to a user supplied stream.</span></span>

## <span data-ttu-id="41c4d-111">示例</span><span class="sxs-lookup"><span data-stu-id="41c4d-111">EXAMPLES</span></span>

### <span data-ttu-id="41c4d-112">範例1：從指定的計算節點取得 RDP 檔案並儲存檔案</span><span class="sxs-lookup"><span data-stu-id="41c4d-112">Example 1: Get an RDP file from a specified compute node and save the file</span></span>
```
PS C:\>Get-AzureBatchRemoteDesktopProtocolFile -PoolId "Pool06" -ComputeNodeId "ComputeNode01" -DestinationPath "C:\PowerShell\ComputeNode01.rdp" -BatchContext $Context
```

<span data-ttu-id="41c4d-113">這個命令會從具有 ID Pool06 的 ComputeNode01 中的 [計算] 節點取得 RDP 檔案。</span><span class="sxs-lookup"><span data-stu-id="41c4d-113">This command gets an RDP file from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool06.</span></span>
<span data-ttu-id="41c4d-114">該命令會將 .rdp 檔案另存為 C:\PowerShell\MyComputeNode.rdp。</span><span class="sxs-lookup"><span data-stu-id="41c4d-114">The command saves the .rdp file as C:\PowerShell\MyComputeNode.rdp.</span></span>
<span data-ttu-id="41c4d-115">使用 Get-AzureRmBatchAccountKeys Cmdlet 將內容指派給 $CoNtext 變數。</span><span class="sxs-lookup"><span data-stu-id="41c4d-115">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="41c4d-116">範例2：從計算節點取得 RDP 檔案，並使用管線儲存檔案</span><span class="sxs-lookup"><span data-stu-id="41c4d-116">Example 2: Get an RDP file from a compute node and save the file by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchComputeNode -PoolId "Pool06" -Id "ComputeNode02" -BatchContext $Context | Get-AzureBatchRemoteDesktopProtocolFile -DestinationPath "C:\PowerShell\MyComputeNode02.rdp" -BatchContext $Context
```

<span data-ttu-id="41c4d-117">這個命令會在擁有 ID Pool06 的池中取得 ID 為 ComputeNode02 的 compute 節點。</span><span class="sxs-lookup"><span data-stu-id="41c4d-117">This command gets the compute node that has the ID ComputeNode02 in the pool that has the ID Pool06.</span></span>
<span data-ttu-id="41c4d-118">命令會使用管線運算子，將該計算節點傳到目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="41c4d-118">The command passes that compute node to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="41c4d-119">目前的 Cmdlet 會從 [計算] 節點取得 rpd 檔案，然後將內容另存為名為 C:\PowerShell\MyComputeNode02.rdp. 的檔案。</span><span class="sxs-lookup"><span data-stu-id="41c4d-119">The current cmdlet gets an .rpd file from the compute node, and then saves the contents as a file that is named C:\PowerShell\MyComputeNode02.rdp.</span></span>

### <span data-ttu-id="41c4d-120">範例3：從指定的計算節點取得 RDP 檔案，並將它引導至資料流程</span><span class="sxs-lookup"><span data-stu-id="41c4d-120">Example 3: Get a RDP file from a specified compute node and direct it to a stream</span></span>
```
PS C:\>$Stream = New-Object -TypeName "System.IO.MemoryStream"
PS C:\> Get-AzureBatchRemoteDesktopProtocolFile "Pool06" -ComputeNodeId "ComputeNode03" -DestinationStream $Stream -BatchContext $Context
```

<span data-ttu-id="41c4d-121">第一個命令會使用 New-Object Cmdlet 建立串流，然後將它儲存在 $Stream 變數中。</span><span class="sxs-lookup"><span data-stu-id="41c4d-121">The first command creates a stream by using the New-Object cmdlet, and then stores it in the $Stream variable.</span></span>

<span data-ttu-id="41c4d-122">第二個命令會從計算節點中取得一個 .rdp 檔案，並在擁有 ID Pool06 的池中包含 ID ComputeNode03。</span><span class="sxs-lookup"><span data-stu-id="41c4d-122">The second command gets an .rdp file from the compute node that has the ID ComputeNode03 in the pool that has the ID Pool06.</span></span>
<span data-ttu-id="41c4d-123">命令會將檔案內容定向至 $Stream 中的資料流程。</span><span class="sxs-lookup"><span data-stu-id="41c4d-123">The command directs file contents to the stream in $Stream.</span></span>

## <span data-ttu-id="41c4d-124">參數</span><span class="sxs-lookup"><span data-stu-id="41c4d-124">PARAMETERS</span></span>

### <span data-ttu-id="41c4d-125">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="41c4d-125">-BatchContext</span></span>
<span data-ttu-id="41c4d-126">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="41c4d-126">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="41c4d-127">若要取得包含您訂閱之便捷鍵的 **BatchAccountCoNtext** 物件，請使用 Get-AzureRmBatchAccountKeys Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="41c4d-127">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="41c4d-128">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="41c4d-128">-ComputeNode</span></span>
<span data-ttu-id="41c4d-129">將 .rdp 檔案指向的計算節點指定為 **PSComputeNode** 物件。</span><span class="sxs-lookup"><span data-stu-id="41c4d-129">Specifies a compute node, as a **PSComputeNode** object, to which the .rdp file points.</span></span>
<span data-ttu-id="41c4d-130">若要取得計算節點物件，請使用 Get-AzureBatchComputeNode Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="41c4d-130">To obtain a compute node object, use the Get-AzureBatchComputeNode cmdlet.</span></span>

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

### <span data-ttu-id="41c4d-131">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="41c4d-131">-ComputeNodeId</span></span>
<span data-ttu-id="41c4d-132">指定 .rdp 檔案指向的計算節點 ID。</span><span class="sxs-lookup"><span data-stu-id="41c4d-132">Specifies the ID of the compute node to which the .rdp file points.</span></span>

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

### <span data-ttu-id="41c4d-133">-DestinationPath</span><span class="sxs-lookup"><span data-stu-id="41c4d-133">-DestinationPath</span></span>
<span data-ttu-id="41c4d-134">指定此 Cmdlet 儲存 .rdp 檔案的檔路徑。</span><span class="sxs-lookup"><span data-stu-id="41c4d-134">Specifies the file path where this cmdlet saves the .rdp file.</span></span>

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

### <span data-ttu-id="41c4d-135">-DestinationStream</span><span class="sxs-lookup"><span data-stu-id="41c4d-135">-DestinationStream</span></span>
<span data-ttu-id="41c4d-136">指定此 Cmdlet 將 RDP 資料導向到哪個資料流程。</span><span class="sxs-lookup"><span data-stu-id="41c4d-136">Specifies the stream into which this cmdlet directs the RDP data.</span></span>
<span data-ttu-id="41c4d-137">這個 Cmdlet 不會關閉或倒帶此資料流程。</span><span class="sxs-lookup"><span data-stu-id="41c4d-137">This cmdlet does not close or rewind this stream.</span></span>

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

### <span data-ttu-id="41c4d-138">-PoolId</span><span class="sxs-lookup"><span data-stu-id="41c4d-138">-PoolId</span></span>
<span data-ttu-id="41c4d-139">指定包含 [計算] 節點（這個 Cmdlet 取得 .rdp 檔案）的池 ID。</span><span class="sxs-lookup"><span data-stu-id="41c4d-139">Specifies the ID of the pool that contains the compute node from which this cmdlet gets an .rdp file.</span></span>

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

### <span data-ttu-id="41c4d-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41c4d-140">-DefaultProfile</span></span>
<span data-ttu-id="41c4d-141">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="41c4d-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="41c4d-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41c4d-142">CommonParameters</span></span>
<span data-ttu-id="41c4d-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="41c4d-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41c4d-144">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="41c4d-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41c4d-145">輸入</span><span class="sxs-lookup"><span data-stu-id="41c4d-145">INPUTS</span></span>

### <span data-ttu-id="41c4d-146">BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="41c4d-146">BatchAccountContext</span></span>
<span data-ttu-id="41c4d-147">形參 "BatchCoNtext" 接受管線中 "BatchAccountCoNtext" 類型的值</span><span class="sxs-lookup"><span data-stu-id="41c4d-147">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="41c4d-148">PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="41c4d-148">PSComputeNode</span></span>
<span data-ttu-id="41c4d-149">形參 "ComputeNode" 接受管線中 "PSComputeNode" 類型的值</span><span class="sxs-lookup"><span data-stu-id="41c4d-149">Parameter 'ComputeNode' accepts value of type 'PSComputeNode' from the pipeline</span></span>

## <span data-ttu-id="41c4d-150">輸出</span><span class="sxs-lookup"><span data-stu-id="41c4d-150">OUTPUTS</span></span>

## <span data-ttu-id="41c4d-151">筆記</span><span class="sxs-lookup"><span data-stu-id="41c4d-151">NOTES</span></span>

## <span data-ttu-id="41c4d-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="41c4d-152">RELATED LINKS</span></span>

[<span data-ttu-id="41c4d-153">AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="41c4d-153">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="41c4d-154">AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="41c4d-154">Get-AzureBatchComputeNode</span></span>](./Get-AzureBatchComputeNode.md)

[<span data-ttu-id="41c4d-155">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="41c4d-155">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


