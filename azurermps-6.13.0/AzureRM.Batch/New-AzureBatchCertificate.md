---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: B423C1A1-1988-4721-81E7-3B7EC163B03A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/new-azurebatchcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchCertificate.md
ms.openlocfilehash: 7038f6c23273153a11aeccc8cbd12fdc6f629c28
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448462"
---
# <span data-ttu-id="861aa-101">New-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="861aa-101">New-AzureBatchCertificate</span></span>

## <span data-ttu-id="861aa-102">摘要</span><span class="sxs-lookup"><span data-stu-id="861aa-102">SYNOPSIS</span></span>
<span data-ttu-id="861aa-103">將憑證新增到指定的批次帳戶。</span><span class="sxs-lookup"><span data-stu-id="861aa-103">Adds a certificate to the specified Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="861aa-104">句法</span><span class="sxs-lookup"><span data-stu-id="861aa-104">SYNTAX</span></span>

### <span data-ttu-id="861aa-105">檔案 (預設) </span><span class="sxs-lookup"><span data-stu-id="861aa-105">File (Default)</span></span>
```
New-AzureBatchCertificate [-FilePath] <String> [-Password <SecureString>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="861aa-106">RawData</span><span class="sxs-lookup"><span data-stu-id="861aa-106">RawData</span></span>
```
New-AzureBatchCertificate [-RawData] <Byte[]> [-Password <SecureString>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="861aa-107">說明</span><span class="sxs-lookup"><span data-stu-id="861aa-107">DESCRIPTION</span></span>
<span data-ttu-id="861aa-108">**新的-AzureBatchCertificate** Cmdlet 會將憑證新增到指定的 Azure Batch 帳戶。</span><span class="sxs-lookup"><span data-stu-id="861aa-108">The **New-AzureBatchCertificate** cmdlet adds a certificate to the specified Azure Batch account.</span></span>

## <span data-ttu-id="861aa-109">示例</span><span class="sxs-lookup"><span data-stu-id="861aa-109">EXAMPLES</span></span>

### <span data-ttu-id="861aa-110">範例1：從檔案新增憑證</span><span class="sxs-lookup"><span data-stu-id="861aa-110">Example 1: Add a certificate from a file</span></span>
```
PS C:\>New-AzureBatchCertificate -FilePath "E:\Certificates\MyCert.cer" -BatchContext $Context
```

<span data-ttu-id="861aa-111">這個命令會使用 [檔案 E:\Certificates\MyCert.cer.]，將憑證新增到指定的批次帳戶</span><span class="sxs-lookup"><span data-stu-id="861aa-111">This command adds a certificate to the specified Batch account by using the file E:\Certificates\MyCert.cer.</span></span>

### <span data-ttu-id="861aa-112">範例2：從原始資料新增憑證</span><span class="sxs-lookup"><span data-stu-id="861aa-112">Example 2: Add a certificate from raw data</span></span>
```
PS C:\>$RawData = [System.IO.File]::ReadAllBytes("E:\Certificates\MyCert.pfx")
PS C:\> New-AzureBatchCertificate -RawData $RawData -Password "Password1234" -BatchContext $Context
```

<span data-ttu-id="861aa-113">第一個命令會將名為 MyCert 的檔案中的資料讀入 $RawData 變數中。</span><span class="sxs-lookup"><span data-stu-id="861aa-113">The first command reads the data from the file named MyCert.pfx into the $RawData variable.</span></span>
<span data-ttu-id="861aa-114">第二個命令會使用儲存在 $RawData 中的原始資料，將憑證新增到指定的批次帳戶。</span><span class="sxs-lookup"><span data-stu-id="861aa-114">The second command adds a certificate to the specified Batch account using the raw data stored in $RawData.</span></span>

## <span data-ttu-id="861aa-115">參數</span><span class="sxs-lookup"><span data-stu-id="861aa-115">PARAMETERS</span></span>

### <span data-ttu-id="861aa-116">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="861aa-116">-BatchContext</span></span>
<span data-ttu-id="861aa-117">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="861aa-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="861aa-118">如果您使用 Get-AzureRmBatchAccount Cmdlet 來取得您的 BatchAccountCoNtext，則在與批次服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="861aa-118">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="861aa-119">若要改為使用共用金鑰驗證，請使用 Get-AzureRmBatchAccountKeys Cmdlet 來取得已填入其便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="861aa-119">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="861aa-120">使用共用金鑰驗證時，預設會使用主要便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="861aa-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="861aa-121">若要變更要使用的索引鍵，請設定 BatchAccountCoNtext 屬性。</span><span class="sxs-lookup"><span data-stu-id="861aa-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="861aa-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="861aa-122">-DefaultProfile</span></span>
<span data-ttu-id="861aa-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="861aa-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="861aa-124">-FilePath</span><span class="sxs-lookup"><span data-stu-id="861aa-124">-FilePath</span></span>
<span data-ttu-id="861aa-125">指定憑證檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="861aa-125">Specifies the path of the certificate file.</span></span>
<span data-ttu-id="861aa-126">憑證檔案必須是 .cer 或 .pfx 格式。</span><span class="sxs-lookup"><span data-stu-id="861aa-126">The certificate file must be in either .cer or .pfx format.</span></span>

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

### <span data-ttu-id="861aa-127">-Password</span><span class="sxs-lookup"><span data-stu-id="861aa-127">-Password</span></span>
<span data-ttu-id="861aa-128">指定用來存取證書私密金鑰的密碼。</span><span class="sxs-lookup"><span data-stu-id="861aa-128">Specifies the password to access the certificate private key.</span></span>
<span data-ttu-id="861aa-129">如果您指定的憑證是 .pfx 格式，您必須指定此參數。</span><span class="sxs-lookup"><span data-stu-id="861aa-129">You must specify this parameter if you specify a certificate in .pfx format.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="861aa-130">-RawData</span><span class="sxs-lookup"><span data-stu-id="861aa-130">-RawData</span></span>
<span data-ttu-id="861aa-131">指定 .cer 或 .pfx 格式的原始憑證資料。</span><span class="sxs-lookup"><span data-stu-id="861aa-131">Specifies the raw certificate data in either .cer or .pfx format.</span></span>

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

### <span data-ttu-id="861aa-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="861aa-132">CommonParameters</span></span>
<span data-ttu-id="861aa-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="861aa-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="861aa-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="861aa-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="861aa-135">輸入</span><span class="sxs-lookup"><span data-stu-id="861aa-135">INPUTS</span></span>

### <span data-ttu-id="861aa-136">System.object []</span><span class="sxs-lookup"><span data-stu-id="861aa-136">System.Byte[]</span></span>

### <span data-ttu-id="861aa-137">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="861aa-137">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="861aa-138">參數： BatchCoNtext (ByValue) </span><span class="sxs-lookup"><span data-stu-id="861aa-138">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="861aa-139">輸出</span><span class="sxs-lookup"><span data-stu-id="861aa-139">OUTPUTS</span></span>

### <span data-ttu-id="861aa-140">System.void</span><span class="sxs-lookup"><span data-stu-id="861aa-140">System.Void</span></span>

## <span data-ttu-id="861aa-141">筆記</span><span class="sxs-lookup"><span data-stu-id="861aa-141">NOTES</span></span>

## <span data-ttu-id="861aa-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="861aa-142">RELATED LINKS</span></span>

[<span data-ttu-id="861aa-143">AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="861aa-143">Get-AzureBatchCertificate</span></span>](./Get-AzureBatchCertificate.md)

[<span data-ttu-id="861aa-144">AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="861aa-144">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="861aa-145">移除-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="861aa-145">Remove-AzureBatchCertificate</span></span>](./Remove-AzureBatchCertificate.md)

[<span data-ttu-id="861aa-146">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="861aa-146">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


