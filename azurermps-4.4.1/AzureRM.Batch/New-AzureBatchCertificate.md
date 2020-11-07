---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: B423C1A1-1988-4721-81E7-3B7EC163B03A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchCertificate.md
ms.openlocfilehash: d567c176580cba0659d6c88c919ffa34cad393ae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626512"
---
# <span data-ttu-id="2f880-101">New-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="2f880-101">New-AzureBatchCertificate</span></span>

## <span data-ttu-id="2f880-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2f880-102">SYNOPSIS</span></span>
<span data-ttu-id="2f880-103">將憑證新增到指定的批次帳戶。</span><span class="sxs-lookup"><span data-stu-id="2f880-103">Adds a certificate to the specified Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2f880-104">句法</span><span class="sxs-lookup"><span data-stu-id="2f880-104">SYNTAX</span></span>

### <span data-ttu-id="2f880-105">檔案 (預設) </span><span class="sxs-lookup"><span data-stu-id="2f880-105">File (Default)</span></span>
```
New-AzureBatchCertificate [-FilePath] <String> [-Password <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2f880-106">RawData</span><span class="sxs-lookup"><span data-stu-id="2f880-106">RawData</span></span>
```
New-AzureBatchCertificate [-RawData] <Byte[]> [-Password <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2f880-107">說明</span><span class="sxs-lookup"><span data-stu-id="2f880-107">DESCRIPTION</span></span>
<span data-ttu-id="2f880-108">**新的-AzureBatchCertificate** Cmdlet 會將憑證新增到指定的 Azure Batch 帳戶。</span><span class="sxs-lookup"><span data-stu-id="2f880-108">The **New-AzureBatchCertificate** cmdlet adds a certificate to the specified Azure Batch account.</span></span>

## <span data-ttu-id="2f880-109">示例</span><span class="sxs-lookup"><span data-stu-id="2f880-109">EXAMPLES</span></span>

### <span data-ttu-id="2f880-110">範例1：從檔案新增憑證</span><span class="sxs-lookup"><span data-stu-id="2f880-110">Example 1: Add a certificate from a file</span></span>
```
PS C:\>New-AzureBatchCertificate -FilePath "E:\Certificates\MyCert.cer" -BatchContext $Context
```

<span data-ttu-id="2f880-111">這個命令會使用 [檔案 E:\Certificates\MyCert.cer.]，將憑證新增到指定的批次帳戶</span><span class="sxs-lookup"><span data-stu-id="2f880-111">This command adds a certificate to the specified Batch account by using the file E:\Certificates\MyCert.cer.</span></span>

### <span data-ttu-id="2f880-112">範例2：從原始資料新增憑證</span><span class="sxs-lookup"><span data-stu-id="2f880-112">Example 2: Add a certificate from raw data</span></span>
```
PS C:\>$RawData = [System.IO.File]::ReadAllBytes("E:\Certificates\MyCert.pfx")
PS C:\> New-AzureBatchCertificate -RawData $RawData -Password "Password1234" -BatchContext $Context
```

<span data-ttu-id="2f880-113">第一個命令會將名為 MyCert 的檔案中的資料讀入 $RawData 變數中。</span><span class="sxs-lookup"><span data-stu-id="2f880-113">The first command reads the data from the file named MyCert.pfx into the $RawData variable.</span></span>

<span data-ttu-id="2f880-114">第二個命令會使用儲存在 $RawData 中的原始資料，將憑證新增到指定的批次帳戶。</span><span class="sxs-lookup"><span data-stu-id="2f880-114">The second command adds a certificate to the specified Batch account using the raw data stored in $RawData.</span></span>

## <span data-ttu-id="2f880-115">參數</span><span class="sxs-lookup"><span data-stu-id="2f880-115">PARAMETERS</span></span>

### <span data-ttu-id="2f880-116">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="2f880-116">-BatchContext</span></span>
<span data-ttu-id="2f880-117">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="2f880-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="2f880-118">若要取得包含您訂閱之便捷鍵的 **BatchAccountCoNtext** 物件，請使用 Get-AzureRmBatchAccountKeys Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2f880-118">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="2f880-119">-FilePath</span><span class="sxs-lookup"><span data-stu-id="2f880-119">-FilePath</span></span>
<span data-ttu-id="2f880-120">指定憑證檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="2f880-120">Specifies the path of the certificate file.</span></span>
<span data-ttu-id="2f880-121">憑證檔案必須是 .cer 或 .pfx 格式。</span><span class="sxs-lookup"><span data-stu-id="2f880-121">The certificate file must be in either .cer or .pfx format.</span></span>

```yaml
Type: System.String
Parameter Sets: File
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f880-122">-Password</span><span class="sxs-lookup"><span data-stu-id="2f880-122">-Password</span></span>
<span data-ttu-id="2f880-123">指定用來存取證書私密金鑰的密碼。</span><span class="sxs-lookup"><span data-stu-id="2f880-123">Specifies the password to access the certificate private key.</span></span>
<span data-ttu-id="2f880-124">如果您指定的憑證是 .pfx 格式，您必須指定此參數。</span><span class="sxs-lookup"><span data-stu-id="2f880-124">You must specify this parameter if you specify a certificate in .pfx format.</span></span>

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

### <span data-ttu-id="2f880-125">-RawData</span><span class="sxs-lookup"><span data-stu-id="2f880-125">-RawData</span></span>
<span data-ttu-id="2f880-126">指定 .cer 或 .pfx 格式的原始憑證資料。</span><span class="sxs-lookup"><span data-stu-id="2f880-126">Specifies the raw certificate data in either .cer or .pfx format.</span></span>

```yaml
Type: System.Byte[]
Parameter Sets: RawData
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2f880-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f880-127">-DefaultProfile</span></span>
<span data-ttu-id="2f880-128">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2f880-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2f880-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f880-129">CommonParameters</span></span>
<span data-ttu-id="2f880-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2f880-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f880-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2f880-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f880-132">輸入</span><span class="sxs-lookup"><span data-stu-id="2f880-132">INPUTS</span></span>

### <span data-ttu-id="2f880-133">BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="2f880-133">BatchAccountContext</span></span>
<span data-ttu-id="2f880-134">形參 "BatchCoNtext" 接受管線中 "BatchAccountCoNtext" 類型的值</span><span class="sxs-lookup"><span data-stu-id="2f880-134">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="2f880-135">Byte []</span><span class="sxs-lookup"><span data-stu-id="2f880-135">Byte[]</span></span>
<span data-ttu-id="2f880-136">形參 "RawData" 接受管線中 "Byte [] 類型的值</span><span class="sxs-lookup"><span data-stu-id="2f880-136">Parameter 'RawData' accepts value of type 'Byte[]' from the pipeline</span></span>

## <span data-ttu-id="2f880-137">輸出</span><span class="sxs-lookup"><span data-stu-id="2f880-137">OUTPUTS</span></span>

## <span data-ttu-id="2f880-138">筆記</span><span class="sxs-lookup"><span data-stu-id="2f880-138">NOTES</span></span>

## <span data-ttu-id="2f880-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="2f880-139">RELATED LINKS</span></span>

[<span data-ttu-id="2f880-140">AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="2f880-140">Get-AzureBatchCertificate</span></span>](./Get-AzureBatchCertificate.md)

[<span data-ttu-id="2f880-141">AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="2f880-141">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="2f880-142">移除-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="2f880-142">Remove-AzureBatchCertificate</span></span>](./Remove-AzureBatchCertificate.md)

[<span data-ttu-id="2f880-143">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="2f880-143">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


