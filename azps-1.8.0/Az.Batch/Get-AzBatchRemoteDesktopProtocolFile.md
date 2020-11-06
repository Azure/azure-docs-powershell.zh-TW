---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: D077DB50-12BC-45AB-8EAC-57810DA83035
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchremotedesktopprotocolfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchRemoteDesktopProtocolFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchRemoteDesktopProtocolFile.md
ms.openlocfilehash: 491deaff0b609ce20de60299de71686ee2ece2a3
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/13/2020
ms.locfileid: "93623319"
---
# <span data-ttu-id="54e0f-101">Get-AzBatchRemoteDesktopProtocolFile</span><span class="sxs-lookup"><span data-stu-id="54e0f-101">Get-AzBatchRemoteDesktopProtocolFile</span></span>

## <span data-ttu-id="54e0f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="54e0f-102">SYNOPSIS</span></span>
<span data-ttu-id="54e0f-103">從計算節點取得 RDP 檔案。</span><span class="sxs-lookup"><span data-stu-id="54e0f-103">Gets an RDP file from a compute node.</span></span>

## <span data-ttu-id="54e0f-104">句法</span><span class="sxs-lookup"><span data-stu-id="54e0f-104">SYNTAX</span></span>

### <span data-ttu-id="54e0f-105">Id_Path (預設) </span><span class="sxs-lookup"><span data-stu-id="54e0f-105">Id_Path (Default)</span></span>
```
Get-AzBatchRemoteDesktopProtocolFile [-PoolId] <String> [-ComputeNodeId] <String> -DestinationPath <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="54e0f-106">Id_Stream</span><span class="sxs-lookup"><span data-stu-id="54e0f-106">Id_Stream</span></span>
```
Get-AzBatchRemoteDesktopProtocolFile [-PoolId] <String> [-ComputeNodeId] <String> -DestinationStream <Stream>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="54e0f-107">InputObject_Path</span><span class="sxs-lookup"><span data-stu-id="54e0f-107">InputObject_Path</span></span>
```
Get-AzBatchRemoteDesktopProtocolFile [[-ComputeNode] <PSComputeNode>] -DestinationPath <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="54e0f-108">InputObject_Stream</span><span class="sxs-lookup"><span data-stu-id="54e0f-108">InputObject_Stream</span></span>
```
Get-AzBatchRemoteDesktopProtocolFile [[-ComputeNode] <PSComputeNode>] -DestinationStream <Stream>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="54e0f-109">說明</span><span class="sxs-lookup"><span data-stu-id="54e0f-109">DESCRIPTION</span></span>
<span data-ttu-id="54e0f-110">**AzBatchRemoteDesktopProtocolFile** Cmdlet 會從計算節點取得遠端桌面通訊協定 (RDP) 檔案，並將它儲存為檔案或使用者提供的資料流程。</span><span class="sxs-lookup"><span data-stu-id="54e0f-110">The **Get-AzBatchRemoteDesktopProtocolFile** cmdlet gets a Remote Desktop Protocol (RDP) file from a compute node and saves it as a file or to a user supplied stream.</span></span>

## <span data-ttu-id="54e0f-111">示例</span><span class="sxs-lookup"><span data-stu-id="54e0f-111">EXAMPLES</span></span>

### <span data-ttu-id="54e0f-112">範例1：從指定的計算節點取得 RDP 檔案並儲存檔案</span><span class="sxs-lookup"><span data-stu-id="54e0f-112">Example 1: Get an RDP file from a specified compute node and save the file</span></span>
```
PS C:\>Get-AzBatchRemoteDesktopProtocolFile -PoolId "Pool06" -ComputeNodeId "ComputeNode01" -DestinationPath "C:\PowerShell\ComputeNode01.rdp" -BatchContext $Context
```

<span data-ttu-id="54e0f-113">這個命令會從具有 ID Pool06 的 ComputeNode01 中的 [計算] 節點取得 RDP 檔案。</span><span class="sxs-lookup"><span data-stu-id="54e0f-113">This command gets an RDP file from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool06.</span></span>
<span data-ttu-id="54e0f-114">該命令會將 .rdp 檔案另存為 C:\PowerShell\MyComputeNode.rdp。</span><span class="sxs-lookup"><span data-stu-id="54e0f-114">The command saves the .rdp file as C:\PowerShell\MyComputeNode.rdp.</span></span>
<span data-ttu-id="54e0f-115">使用 Get-AzBatchAccountKeys Cmdlet 將內容指派給 $CoNtext 變數。</span><span class="sxs-lookup"><span data-stu-id="54e0f-115">Use the Get-AzBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="54e0f-116">範例2：從計算節點取得 RDP 檔案，並使用管線儲存檔案</span><span class="sxs-lookup"><span data-stu-id="54e0f-116">Example 2: Get an RDP file from a compute node and save the file by using the pipeline</span></span>
```
PS C:\>Get-AzBatchComputeNode -PoolId "Pool06" -Id "ComputeNode02" -BatchContext $Context | Get-AzBatchRemoteDesktopProtocolFile -DestinationPath "C:\PowerShell\MyComputeNode02.rdp" -BatchContext $Context
```

<span data-ttu-id="54e0f-117">這個命令會在擁有 ID Pool06 的池中取得 ID 為 ComputeNode02 的 compute 節點。</span><span class="sxs-lookup"><span data-stu-id="54e0f-117">This command gets the compute node that has the ID ComputeNode02 in the pool that has the ID Pool06.</span></span>
<span data-ttu-id="54e0f-118">命令會使用管線運算子，將該計算節點傳到目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="54e0f-118">The command passes that compute node to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="54e0f-119">目前的 Cmdlet 會從 [計算] 節點取得 rpd 檔案，然後將內容另存為名為 C:\PowerShell\MyComputeNode02.rdp. 的檔案。</span><span class="sxs-lookup"><span data-stu-id="54e0f-119">The current cmdlet gets an .rpd file from the compute node, and then saves the contents as a file that is named C:\PowerShell\MyComputeNode02.rdp.</span></span>

### <span data-ttu-id="54e0f-120">範例3：從指定的計算節點取得 RDP 檔案，並將它引導至資料流程</span><span class="sxs-lookup"><span data-stu-id="54e0f-120">Example 3: Get a RDP file from a specified compute node and direct it to a stream</span></span>
```
PS C:\>$Stream = New-Object -TypeName "System.IO.MemoryStream"
PS C:\> Get-AzBatchRemoteDesktopProtocolFile "Pool06" -ComputeNodeId "ComputeNode03" -DestinationStream $Stream -BatchContext $Context
```

<span data-ttu-id="54e0f-121">第一個命令會使用 New-Object Cmdlet 建立串流，然後將它儲存在 $Stream 變數中。</span><span class="sxs-lookup"><span data-stu-id="54e0f-121">The first command creates a stream by using the New-Object cmdlet, and then stores it in the $Stream variable.</span></span>
<span data-ttu-id="54e0f-122">第二個命令會從計算節點中取得一個 .rdp 檔案，並在擁有 ID Pool06 的池中包含 ID ComputeNode03。</span><span class="sxs-lookup"><span data-stu-id="54e0f-122">The second command gets an .rdp file from the compute node that has the ID ComputeNode03 in the pool that has the ID Pool06.</span></span>
<span data-ttu-id="54e0f-123">命令會將檔案內容定向至 $Stream 中的資料流程。</span><span class="sxs-lookup"><span data-stu-id="54e0f-123">The command directs file contents to the stream in $Stream.</span></span>

## <span data-ttu-id="54e0f-124">參數</span><span class="sxs-lookup"><span data-stu-id="54e0f-124">PARAMETERS</span></span>

### <span data-ttu-id="54e0f-125">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="54e0f-125">-BatchContext</span></span>
<span data-ttu-id="54e0f-126">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="54e0f-126">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="54e0f-127">如果您使用 Get-AzBatchAccount Cmdlet 來取得您的 BatchAccountCoNtext，則在與批次服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="54e0f-127">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="54e0f-128">若要改為使用共用金鑰驗證，請使用 Get-AzBatchAccountKeys Cmdlet 來取得已填入其便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="54e0f-128">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="54e0f-129">使用共用金鑰驗證時，預設會使用主要便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="54e0f-129">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="54e0f-130">若要變更要使用的索引鍵，請設定 BatchAccountCoNtext 屬性。</span><span class="sxs-lookup"><span data-stu-id="54e0f-130">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="54e0f-131">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="54e0f-131">-ComputeNode</span></span>
<span data-ttu-id="54e0f-132">將 .rdp 檔案指向的計算節點指定為 **PSComputeNode** 物件。</span><span class="sxs-lookup"><span data-stu-id="54e0f-132">Specifies a compute node, as a **PSComputeNode** object, to which the .rdp file points.</span></span>
<span data-ttu-id="54e0f-133">若要取得計算節點物件，請使用 Get-AzBatchComputeNode Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="54e0f-133">To obtain a compute node object, use the Get-AzBatchComputeNode cmdlet.</span></span>

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

### <span data-ttu-id="54e0f-134">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="54e0f-134">-ComputeNodeId</span></span>
<span data-ttu-id="54e0f-135">指定 .rdp 檔案指向的計算節點 ID。</span><span class="sxs-lookup"><span data-stu-id="54e0f-135">Specifies the ID of the compute node to which the .rdp file points.</span></span>

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

### <span data-ttu-id="54e0f-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54e0f-136">-DefaultProfile</span></span>
<span data-ttu-id="54e0f-137">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="54e0f-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="54e0f-138">-DestinationPath</span><span class="sxs-lookup"><span data-stu-id="54e0f-138">-DestinationPath</span></span>
<span data-ttu-id="54e0f-139">指定此 Cmdlet 儲存 .rdp 檔案的檔路徑。</span><span class="sxs-lookup"><span data-stu-id="54e0f-139">Specifies the file path where this cmdlet saves the .rdp file.</span></span>

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

### <span data-ttu-id="54e0f-140">-DestinationStream</span><span class="sxs-lookup"><span data-stu-id="54e0f-140">-DestinationStream</span></span>
<span data-ttu-id="54e0f-141">指定此 Cmdlet 將 RDP 資料導向到哪個資料流程。</span><span class="sxs-lookup"><span data-stu-id="54e0f-141">Specifies the stream into which this cmdlet directs the RDP data.</span></span>
<span data-ttu-id="54e0f-142">這個 Cmdlet 不會關閉或倒帶此資料流程。</span><span class="sxs-lookup"><span data-stu-id="54e0f-142">This cmdlet does not close or rewind this stream.</span></span>

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

### <span data-ttu-id="54e0f-143">-PoolId</span><span class="sxs-lookup"><span data-stu-id="54e0f-143">-PoolId</span></span>
<span data-ttu-id="54e0f-144">指定包含 [計算] 節點（這個 Cmdlet 取得 .rdp 檔案）的池 ID。</span><span class="sxs-lookup"><span data-stu-id="54e0f-144">Specifies the ID of the pool that contains the compute node from which this cmdlet gets an .rdp file.</span></span>

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

### <span data-ttu-id="54e0f-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54e0f-145">CommonParameters</span></span>
<span data-ttu-id="54e0f-146">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="54e0f-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54e0f-147">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="54e0f-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54e0f-148">輸入</span><span class="sxs-lookup"><span data-stu-id="54e0f-148">INPUTS</span></span>

### <span data-ttu-id="54e0f-149">System.object</span><span class="sxs-lookup"><span data-stu-id="54e0f-149">System.String</span></span>

### <span data-ttu-id="54e0f-150">Microsoft.Azure.Commands.Batch。PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="54e0f-150">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="54e0f-151">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="54e0f-151">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="54e0f-152">輸出</span><span class="sxs-lookup"><span data-stu-id="54e0f-152">OUTPUTS</span></span>

### <span data-ttu-id="54e0f-153">System.void</span><span class="sxs-lookup"><span data-stu-id="54e0f-153">System.Void</span></span>

## <span data-ttu-id="54e0f-154">筆記</span><span class="sxs-lookup"><span data-stu-id="54e0f-154">NOTES</span></span>

## <span data-ttu-id="54e0f-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="54e0f-155">RELATED LINKS</span></span>

[<span data-ttu-id="54e0f-156">AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="54e0f-156">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="54e0f-157">AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="54e0f-157">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="54e0f-158">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="54e0f-158">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


