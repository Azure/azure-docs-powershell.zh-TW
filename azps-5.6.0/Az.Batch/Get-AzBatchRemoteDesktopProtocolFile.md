---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: D077DB50-12BC-45AB-8EAC-57810DA83035
online version: https://docs.microsoft.com/powershell/module/az.batch/get-azbatchremotedesktopprotocolfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchRemoteDesktopProtocolFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchRemoteDesktopProtocolFile.md
ms.openlocfilehash: 21e1848266f13fd44513ea0bce8c540b0387320a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910298"
---
# <span data-ttu-id="d8282-101">Get-AzBatchRemoteDesktopProtocolFile</span><span class="sxs-lookup"><span data-stu-id="d8282-101">Get-AzBatchRemoteDesktopProtocolFile</span></span>

## <span data-ttu-id="d8282-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d8282-102">SYNOPSIS</span></span>
<span data-ttu-id="d8282-103">從計算節點獲得 RDP 檔案。</span><span class="sxs-lookup"><span data-stu-id="d8282-103">Gets an RDP file from a compute node.</span></span>

## <span data-ttu-id="d8282-104">語法</span><span class="sxs-lookup"><span data-stu-id="d8282-104">SYNTAX</span></span>

### <span data-ttu-id="d8282-105">Id_Path (預設) </span><span class="sxs-lookup"><span data-stu-id="d8282-105">Id_Path (Default)</span></span>
```
Get-AzBatchRemoteDesktopProtocolFile [-PoolId] <String> [-ComputeNodeId] <String> -DestinationPath <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d8282-106">Id_Stream</span><span class="sxs-lookup"><span data-stu-id="d8282-106">Id_Stream</span></span>
```
Get-AzBatchRemoteDesktopProtocolFile [-PoolId] <String> [-ComputeNodeId] <String> -DestinationStream <Stream>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d8282-107">InputObject_Path</span><span class="sxs-lookup"><span data-stu-id="d8282-107">InputObject_Path</span></span>
```
Get-AzBatchRemoteDesktopProtocolFile [[-ComputeNode] <PSComputeNode>] -DestinationPath <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d8282-108">InputObject_Stream</span><span class="sxs-lookup"><span data-stu-id="d8282-108">InputObject_Stream</span></span>
```
Get-AzBatchRemoteDesktopProtocolFile [[-ComputeNode] <PSComputeNode>] -DestinationStream <Stream>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d8282-109">描述</span><span class="sxs-lookup"><span data-stu-id="d8282-109">DESCRIPTION</span></span>
<span data-ttu-id="d8282-110">**Get-AzBatchRemoteDesktopProtocolFile** Cmdlet 會從計算節點取得遠端桌面通訊協定 (RDP) 檔案，並另存為檔案或使用者提供的串流。</span><span class="sxs-lookup"><span data-stu-id="d8282-110">The **Get-AzBatchRemoteDesktopProtocolFile** cmdlet gets a Remote Desktop Protocol (RDP) file from a compute node and saves it as a file or to a user supplied stream.</span></span>

## <span data-ttu-id="d8282-111">例子</span><span class="sxs-lookup"><span data-stu-id="d8282-111">EXAMPLES</span></span>

### <span data-ttu-id="d8282-112">範例 1：從指定的計算節點取得 RDP 檔案並儲存該檔案</span><span class="sxs-lookup"><span data-stu-id="d8282-112">Example 1: Get an RDP file from a specified compute node and save the file</span></span>
```
PS C:\>Get-AzBatchRemoteDesktopProtocolFile -PoolId "Pool06" -ComputeNodeId "ComputeNode01" -DestinationPath "C:\PowerShell\ComputeNode01.rdp" -BatchContext $Context
```

<span data-ttu-id="d8282-113">此命令會從具有識別碼 Pool06 的集中具有 ID ComputeNode01 的計算節點中，獲得 RDP 檔案。</span><span class="sxs-lookup"><span data-stu-id="d8282-113">This command gets an RDP file from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool06.</span></span>
<span data-ttu-id="d8282-114">該命令會將 .rdp 檔案存為 C：\PowerShell\MyComputeNode.rdp。</span><span class="sxs-lookup"><span data-stu-id="d8282-114">The command saves the .rdp file as C:\PowerShell\MyComputeNode.rdp.</span></span>
<span data-ttu-id="d8282-115">使用 Get-AzBatchAccountKey Cmdlet 將上下文指派給$CoNtext變數。</span><span class="sxs-lookup"><span data-stu-id="d8282-115">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="d8282-116">範例 2：從計算節點取得 RDP 檔案，然後使用管線儲存該檔案</span><span class="sxs-lookup"><span data-stu-id="d8282-116">Example 2: Get an RDP file from a compute node and save the file by using the pipeline</span></span>
```
PS C:\>Get-AzBatchComputeNode -PoolId "Pool06" -Id "ComputeNode02" -BatchContext $Context | Get-AzBatchRemoteDesktopProtocolFile -DestinationPath "C:\PowerShell\MyComputeNode02.rdp" -BatchContext $Context
```

<span data-ttu-id="d8282-117">此命令會獲得具有識別碼 Pool06 的集中具有 ID ComputeNode02 的計算節點。</span><span class="sxs-lookup"><span data-stu-id="d8282-117">This command gets the compute node that has the ID ComputeNode02 in the pool that has the ID Pool06.</span></span>
<span data-ttu-id="d8282-118">該命令會使用管線運算子，將計算節點傳遞至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d8282-118">The command passes that compute node to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="d8282-119">目前的 Cmdlet 會從計算節點獲得 .rpd 檔案，然後將內容另存為 C：\PowerShell\MyComputeNode02.rdp 的檔案。</span><span class="sxs-lookup"><span data-stu-id="d8282-119">The current cmdlet gets an .rpd file from the compute node, and then saves the contents as a file that is named C:\PowerShell\MyComputeNode02.rdp.</span></span>

### <span data-ttu-id="d8282-120">範例 3：從指定的計算節點取得 RDP 檔案，並引導至資料流程</span><span class="sxs-lookup"><span data-stu-id="d8282-120">Example 3: Get a RDP file from a specified compute node and direct it to a stream</span></span>
```
PS C:\>$Stream = New-Object -TypeName "System.IO.MemoryStream"
PS C:\> Get-AzBatchRemoteDesktopProtocolFile "Pool06" -ComputeNodeId "ComputeNode03" -DestinationStream $Stream -BatchContext $Context
```

<span data-ttu-id="d8282-121">第一個命令會使用 New-Object Cmdlet 建立串流，然後將它儲存在 $Stream 變數中。</span><span class="sxs-lookup"><span data-stu-id="d8282-121">The first command creates a stream by using the New-Object cmdlet, and then stores it in the $Stream variable.</span></span>
<span data-ttu-id="d8282-122">第二個命令會從具有識別碼 Pool06 之計算節點的 ID ComputeNode03 中，獲得 .rdp 檔案。</span><span class="sxs-lookup"><span data-stu-id="d8282-122">The second command gets an .rdp file from the compute node that has the ID ComputeNode03 in the pool that has the ID Pool06.</span></span>
<span data-ttu-id="d8282-123">命令會以命令將檔案內容引導至 $Stream。</span><span class="sxs-lookup"><span data-stu-id="d8282-123">The command directs file contents to the stream in $Stream.</span></span>

## <span data-ttu-id="d8282-124">參數</span><span class="sxs-lookup"><span data-stu-id="d8282-124">PARAMETERS</span></span>

### <span data-ttu-id="d8282-125">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="d8282-125">-BatchContext</span></span>
<span data-ttu-id="d8282-126">指定此 Cmdlet 用來與批次處理服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="d8282-126">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="d8282-127">如果您使用 Get-AzBatchAccount Cmdlet 取得 BatchAccountCoNtext，則與批次處理服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="d8282-127">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="d8282-128">若要改為使用共用金鑰驗證，請使用 Get-AzBatchAccountKey Cmdlet 取得已填入便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="d8282-128">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="d8282-129">使用共用金鑰驗證時，預設會使用主便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="d8282-129">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="d8282-130">若要變更使用的金鑰，請設定 BatchAccountCoNtext.KeyInUse 屬性。</span><span class="sxs-lookup"><span data-stu-id="d8282-130">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="d8282-131">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="d8282-131">-ComputeNode</span></span>
<span data-ttu-id="d8282-132">指定計算節點 ，做為 **PSComputeNode** 物件，.rdp 檔案指向該物件。</span><span class="sxs-lookup"><span data-stu-id="d8282-132">Specifies a compute node, as a **PSComputeNode** object, to which the .rdp file points.</span></span>
<span data-ttu-id="d8282-133">若要取得計算節點物件，請使用 Get-AzBatchComputeNode Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d8282-133">To obtain a compute node object, use the Get-AzBatchComputeNode cmdlet.</span></span>

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

### <span data-ttu-id="d8282-134">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="d8282-134">-ComputeNodeId</span></span>
<span data-ttu-id="d8282-135">指定 .rdp 檔案指向之計算節點的識別碼。</span><span class="sxs-lookup"><span data-stu-id="d8282-135">Specifies the ID of the compute node to which the .rdp file points.</span></span>

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

### <span data-ttu-id="d8282-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8282-136">-DefaultProfile</span></span>
<span data-ttu-id="d8282-137">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="d8282-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d8282-138">-DestinationPath</span><span class="sxs-lookup"><span data-stu-id="d8282-138">-DestinationPath</span></span>
<span data-ttu-id="d8282-139">指定此 Cmdlet 將 .rdp 檔案存到何處的檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="d8282-139">Specifies the file path where this cmdlet saves the .rdp file.</span></span>

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

### <span data-ttu-id="d8282-140">-DestinationStream</span><span class="sxs-lookup"><span data-stu-id="d8282-140">-DestinationStream</span></span>
<span data-ttu-id="d8282-141">指定此 Cmdlet 會引導 RDP 資料的資料流程。</span><span class="sxs-lookup"><span data-stu-id="d8282-141">Specifies the stream into which this cmdlet directs the RDP data.</span></span>
<span data-ttu-id="d8282-142">此 Cmdlet 不會關閉或倒帶此串流。</span><span class="sxs-lookup"><span data-stu-id="d8282-142">This cmdlet does not close or rewind this stream.</span></span>

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

### <span data-ttu-id="d8282-143">-PoolId</span><span class="sxs-lookup"><span data-stu-id="d8282-143">-PoolId</span></span>
<span data-ttu-id="d8282-144">指定包含此 Cmdlet 從其中獲得 .rdp 檔案之計算節點的集區識別碼。</span><span class="sxs-lookup"><span data-stu-id="d8282-144">Specifies the ID of the pool that contains the compute node from which this cmdlet gets an .rdp file.</span></span>

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

### <span data-ttu-id="d8282-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8282-145">CommonParameters</span></span>
<span data-ttu-id="d8282-146">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d8282-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8282-147">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d8282-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8282-148">輸入</span><span class="sxs-lookup"><span data-stu-id="d8282-148">INPUTS</span></span>

### <span data-ttu-id="d8282-149">System.String</span><span class="sxs-lookup"><span data-stu-id="d8282-149">System.String</span></span>

### <span data-ttu-id="d8282-150">Microsoft.Azure.Commands.Batch。Models.PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="d8282-150">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="d8282-151">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="d8282-151">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="d8282-152">輸出</span><span class="sxs-lookup"><span data-stu-id="d8282-152">OUTPUTS</span></span>

### <span data-ttu-id="d8282-153">System.Void</span><span class="sxs-lookup"><span data-stu-id="d8282-153">System.Void</span></span>

## <span data-ttu-id="d8282-154">筆記</span><span class="sxs-lookup"><span data-stu-id="d8282-154">NOTES</span></span>

## <span data-ttu-id="d8282-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="d8282-155">RELATED LINKS</span></span>

[<span data-ttu-id="d8282-156">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="d8282-156">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="d8282-157">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="d8282-157">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="d8282-158">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="d8282-158">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
