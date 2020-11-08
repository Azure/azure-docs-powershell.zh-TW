---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: B423C1A1-1988-4721-81E7-3B7EC163B03A
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchCertificate.md
ms.openlocfilehash: 240da78c14b681b334d0793bfc15b2af4d97b5f3
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/13/2020
ms.locfileid: "93968706"
---
# <span data-ttu-id="6900e-101">New-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="6900e-101">New-AzBatchCertificate</span></span>

## <span data-ttu-id="6900e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6900e-102">SYNOPSIS</span></span>
<span data-ttu-id="6900e-103">將憑證新增到指定的批次帳戶。</span><span class="sxs-lookup"><span data-stu-id="6900e-103">Adds a certificate to the specified Batch account.</span></span>

## <span data-ttu-id="6900e-104">句法</span><span class="sxs-lookup"><span data-stu-id="6900e-104">SYNTAX</span></span>

### <span data-ttu-id="6900e-105">檔案 (預設) </span><span class="sxs-lookup"><span data-stu-id="6900e-105">File (Default)</span></span>
```
New-AzBatchCertificate [-FilePath] <String> [-Password <SecureString>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6900e-106">RawData</span><span class="sxs-lookup"><span data-stu-id="6900e-106">RawData</span></span>
```
New-AzBatchCertificate [-RawData] <Byte[]> [-Password <SecureString>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6900e-107">說明</span><span class="sxs-lookup"><span data-stu-id="6900e-107">DESCRIPTION</span></span>
<span data-ttu-id="6900e-108">**新的-AzBatchCertificate** Cmdlet 會將憑證新增到指定的 Azure Batch 帳戶。</span><span class="sxs-lookup"><span data-stu-id="6900e-108">The **New-AzBatchCertificate** cmdlet adds a certificate to the specified Azure Batch account.</span></span>

## <span data-ttu-id="6900e-109">示例</span><span class="sxs-lookup"><span data-stu-id="6900e-109">EXAMPLES</span></span>

### <span data-ttu-id="6900e-110">範例1：從檔案新增憑證</span><span class="sxs-lookup"><span data-stu-id="6900e-110">Example 1: Add a certificate from a file</span></span>
```
PS C:\>New-AzBatchCertificate -FilePath "E:\Certificates\MyCert.cer" -BatchContext $Context
```

<span data-ttu-id="6900e-111">這個命令會使用 [檔案 E:\Certificates\MyCert.cer.]，將憑證新增到指定的批次帳戶</span><span class="sxs-lookup"><span data-stu-id="6900e-111">This command adds a certificate to the specified Batch account by using the file E:\Certificates\MyCert.cer.</span></span>

### <span data-ttu-id="6900e-112">範例2：從原始資料新增憑證</span><span class="sxs-lookup"><span data-stu-id="6900e-112">Example 2: Add a certificate from raw data</span></span>
```
PS C:\>$RawData = [System.IO.File]::ReadAllBytes("E:\Certificates\MyCert.pfx")
PS C:\> New-AzBatchCertificate -RawData $RawData -Password "Password1234" -BatchContext $Context
```

<span data-ttu-id="6900e-113">第一個命令會將名為 MyCert 的檔案中的資料讀入 $RawData 變數中。</span><span class="sxs-lookup"><span data-stu-id="6900e-113">The first command reads the data from the file named MyCert.pfx into the $RawData variable.</span></span>
<span data-ttu-id="6900e-114">第二個命令會使用儲存在 $RawData 中的原始資料，將憑證新增到指定的批次帳戶。</span><span class="sxs-lookup"><span data-stu-id="6900e-114">The second command adds a certificate to the specified Batch account using the raw data stored in $RawData.</span></span>

## <span data-ttu-id="6900e-115">參數</span><span class="sxs-lookup"><span data-stu-id="6900e-115">PARAMETERS</span></span>

### <span data-ttu-id="6900e-116">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="6900e-116">-BatchContext</span></span>
<span data-ttu-id="6900e-117">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="6900e-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="6900e-118">如果您使用 Get-AzBatchAccount Cmdlet 來取得您的 BatchAccountCoNtext，則在與批次服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="6900e-118">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="6900e-119">若要改為使用共用金鑰驗證，請使用 Get-AzBatchAccountKey Cmdlet 來取得已填入其便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="6900e-119">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="6900e-120">使用共用金鑰驗證時，預設會使用主要便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="6900e-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="6900e-121">若要變更要使用的索引鍵，請設定 BatchAccountCoNtext 屬性。</span><span class="sxs-lookup"><span data-stu-id="6900e-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="6900e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6900e-122">-DefaultProfile</span></span>
<span data-ttu-id="6900e-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6900e-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6900e-124">-FilePath</span><span class="sxs-lookup"><span data-stu-id="6900e-124">-FilePath</span></span>
<span data-ttu-id="6900e-125">指定憑證檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="6900e-125">Specifies the path of the certificate file.</span></span>
<span data-ttu-id="6900e-126">憑證檔案必須是 .cer 或 .pfx 格式。</span><span class="sxs-lookup"><span data-stu-id="6900e-126">The certificate file must be in either .cer or .pfx format.</span></span>

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

### <span data-ttu-id="6900e-127">-Password</span><span class="sxs-lookup"><span data-stu-id="6900e-127">-Password</span></span>
<span data-ttu-id="6900e-128">指定用來存取證書私密金鑰的密碼。</span><span class="sxs-lookup"><span data-stu-id="6900e-128">Specifies the password to access the certificate private key.</span></span>
<span data-ttu-id="6900e-129">如果您指定的憑證是 .pfx 格式，您必須指定此參數。</span><span class="sxs-lookup"><span data-stu-id="6900e-129">You must specify this parameter if you specify a certificate in .pfx format.</span></span>

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

### <span data-ttu-id="6900e-130">-RawData</span><span class="sxs-lookup"><span data-stu-id="6900e-130">-RawData</span></span>
<span data-ttu-id="6900e-131">指定 .cer 或 .pfx 格式的原始憑證資料。</span><span class="sxs-lookup"><span data-stu-id="6900e-131">Specifies the raw certificate data in either .cer or .pfx format.</span></span>

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

### <span data-ttu-id="6900e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6900e-132">CommonParameters</span></span>
<span data-ttu-id="6900e-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6900e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6900e-134">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="6900e-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6900e-135">輸入</span><span class="sxs-lookup"><span data-stu-id="6900e-135">INPUTS</span></span>

### <span data-ttu-id="6900e-136">System.object []</span><span class="sxs-lookup"><span data-stu-id="6900e-136">System.Byte[]</span></span>

### <span data-ttu-id="6900e-137">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="6900e-137">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="6900e-138">輸出</span><span class="sxs-lookup"><span data-stu-id="6900e-138">OUTPUTS</span></span>

### <span data-ttu-id="6900e-139">System.void</span><span class="sxs-lookup"><span data-stu-id="6900e-139">System.Void</span></span>

## <span data-ttu-id="6900e-140">筆記</span><span class="sxs-lookup"><span data-stu-id="6900e-140">NOTES</span></span>

## <span data-ttu-id="6900e-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="6900e-141">RELATED LINKS</span></span>

[<span data-ttu-id="6900e-142">AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="6900e-142">Get-AzBatchCertificate</span></span>](./Get-AzBatchCertificate.md)

[<span data-ttu-id="6900e-143">AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="6900e-143">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="6900e-144">移除-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="6900e-144">Remove-AzBatchCertificate</span></span>](./Remove-AzBatchCertificate.md)

[<span data-ttu-id="6900e-145">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6900e-145">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)

