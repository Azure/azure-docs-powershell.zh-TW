---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: B423C1A1-1988-4721-81E7-3B7EC163B03A
online version: https://docs.microsoft.com/powershell/module/az.batch/new-azbatchcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchCertificate.md
ms.openlocfilehash: 4ef75210204cddc8de2aa129f0997cb4f12269b4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906973"
---
# <span data-ttu-id="cde65-101">New-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="cde65-101">New-AzBatchCertificate</span></span>

## <span data-ttu-id="cde65-102">簡介</span><span class="sxs-lookup"><span data-stu-id="cde65-102">SYNOPSIS</span></span>
<span data-ttu-id="cde65-103">將憑證新增到指定的批次帳戶。</span><span class="sxs-lookup"><span data-stu-id="cde65-103">Adds a certificate to the specified Batch account.</span></span>

## <span data-ttu-id="cde65-104">語法</span><span class="sxs-lookup"><span data-stu-id="cde65-104">SYNTAX</span></span>

### <span data-ttu-id="cde65-105">檔案 (預設) </span><span class="sxs-lookup"><span data-stu-id="cde65-105">File (Default)</span></span>
```
New-AzBatchCertificate [-FilePath] <String> [-Password <SecureString>] [-Kind <PSCertificateKind>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cde65-106">RawData</span><span class="sxs-lookup"><span data-stu-id="cde65-106">RawData</span></span>
```
New-AzBatchCertificate [-RawData] <Byte[]> [-Password <SecureString>] [-Kind <PSCertificateKind>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cde65-107">描述</span><span class="sxs-lookup"><span data-stu-id="cde65-107">DESCRIPTION</span></span>
<span data-ttu-id="cde65-108">**New-AzBatchCertificate** Cmdlet 會新增憑證至指定的 Azure Batch 帳戶。</span><span class="sxs-lookup"><span data-stu-id="cde65-108">The **New-AzBatchCertificate** cmdlet adds a certificate to the specified Azure Batch account.</span></span>

## <span data-ttu-id="cde65-109">例子</span><span class="sxs-lookup"><span data-stu-id="cde65-109">EXAMPLES</span></span>

### <span data-ttu-id="cde65-110">範例 1：從檔案新增憑證</span><span class="sxs-lookup"><span data-stu-id="cde65-110">Example 1: Add a certificate from a file</span></span>
```
PS C:\>New-AzBatchCertificate -FilePath "E:\Certificates\MyCert.cer" -BatchContext $Context
```

<span data-ttu-id="cde65-111">此命令會使用檔案 E：\Certificate\MyCert.cer，將憑證新增到指定的批次處理帳戶。</span><span class="sxs-lookup"><span data-stu-id="cde65-111">This command adds a certificate to the specified Batch account by using the file E:\Certificates\MyCert.cer.</span></span>

### <span data-ttu-id="cde65-112">範例 2：從原始資料新增憑證</span><span class="sxs-lookup"><span data-stu-id="cde65-112">Example 2: Add a certificate from raw data</span></span>
```
PS C:\>$RawData = [System.IO.File]::ReadAllBytes("E:\Certificates\MyCert.pfx")
PS C:\> New-AzBatchCertificate -RawData $RawData -Password "Password1234" -BatchContext $Context
```

<span data-ttu-id="cde65-113">第一個命令會從名為 MyCert.pfx 的檔案讀取資料至$RawData變數。</span><span class="sxs-lookup"><span data-stu-id="cde65-113">The first command reads the data from the file named MyCert.pfx into the $RawData variable.</span></span>
<span data-ttu-id="cde65-114">第二個命令會使用儲存在 $RawData 中的原始資料，將憑證新增到指定的批次處理$RawData。</span><span class="sxs-lookup"><span data-stu-id="cde65-114">The second command adds a certificate to the specified Batch account using the raw data stored in $RawData.</span></span>

## <span data-ttu-id="cde65-115">參數</span><span class="sxs-lookup"><span data-stu-id="cde65-115">PARAMETERS</span></span>

### <span data-ttu-id="cde65-116">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="cde65-116">-BatchContext</span></span>
<span data-ttu-id="cde65-117">指定此 Cmdlet 用來與批次處理服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="cde65-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="cde65-118">如果您使用 Get-AzBatchAccount Cmdlet 取得 BatchAccountCoNtext，則與批次處理服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="cde65-118">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="cde65-119">若要改為使用共用金鑰驗證，請使用 Get-AzBatchAccountKey Cmdlet 取得已填入便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="cde65-119">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="cde65-120">使用共用金鑰驗證時，預設會使用主便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="cde65-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="cde65-121">若要變更使用的金鑰，請設定 BatchAccountCoNtext.KeyInUse 屬性。</span><span class="sxs-lookup"><span data-stu-id="cde65-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="cde65-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cde65-122">-DefaultProfile</span></span>
<span data-ttu-id="cde65-123">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="cde65-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cde65-124">-FilePath</span><span class="sxs-lookup"><span data-stu-id="cde65-124">-FilePath</span></span>
<span data-ttu-id="cde65-125">指定憑證檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="cde65-125">Specifies the path of the certificate file.</span></span>
<span data-ttu-id="cde65-126">憑證檔案必須採用 .cer 或 .pfx 格式。</span><span class="sxs-lookup"><span data-stu-id="cde65-126">The certificate file must be in either .cer or .pfx format.</span></span>

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

### <span data-ttu-id="cde65-127">-Kind</span><span class="sxs-lookup"><span data-stu-id="cde65-127">-Kind</span></span>
<span data-ttu-id="cde65-128">要建立之憑證種類。</span><span class="sxs-lookup"><span data-stu-id="cde65-128">The kind of certificate to create.</span></span> <span data-ttu-id="cde65-129">如果未指定，則假設所有沒有密碼的憑證都是 CER，而所有具有密碼的憑證都是 PFX。</span><span class="sxs-lookup"><span data-stu-id="cde65-129">If this is not specified, it is assumed that all certificates without a password are CER and all certificates with password are PFX.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCertificateKind
Parameter Sets: (All)
Aliases:
Accepted values: Cer, Pfx

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cde65-130">-密碼</span><span class="sxs-lookup"><span data-stu-id="cde65-130">-Password</span></span>
<span data-ttu-id="cde65-131">指定存取憑證私密金鑰的密碼。</span><span class="sxs-lookup"><span data-stu-id="cde65-131">Specifies the password to access the certificate private key.</span></span>
<span data-ttu-id="cde65-132">如果您以 .pfx 格式指定憑證，則必須指定此參數。</span><span class="sxs-lookup"><span data-stu-id="cde65-132">You must specify this parameter if you specify a certificate in .pfx format.</span></span>

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

### <span data-ttu-id="cde65-133">-RawData</span><span class="sxs-lookup"><span data-stu-id="cde65-133">-RawData</span></span>
<span data-ttu-id="cde65-134">指定 .cer 或 .pfx 格式的原始憑證資料。</span><span class="sxs-lookup"><span data-stu-id="cde65-134">Specifies the raw certificate data in either .cer or .pfx format.</span></span>

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

### <span data-ttu-id="cde65-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cde65-135">CommonParameters</span></span>
<span data-ttu-id="cde65-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="cde65-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cde65-137">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cde65-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cde65-138">輸入</span><span class="sxs-lookup"><span data-stu-id="cde65-138">INPUTS</span></span>

### <span data-ttu-id="cde65-139">System.Byte[]</span><span class="sxs-lookup"><span data-stu-id="cde65-139">System.Byte[]</span></span>

### <span data-ttu-id="cde65-140">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="cde65-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="cde65-141">輸出</span><span class="sxs-lookup"><span data-stu-id="cde65-141">OUTPUTS</span></span>

### <span data-ttu-id="cde65-142">System.Void</span><span class="sxs-lookup"><span data-stu-id="cde65-142">System.Void</span></span>

## <span data-ttu-id="cde65-143">筆記</span><span class="sxs-lookup"><span data-stu-id="cde65-143">NOTES</span></span>

## <span data-ttu-id="cde65-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="cde65-144">RELATED LINKS</span></span>

[<span data-ttu-id="cde65-145">Get-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="cde65-145">Get-AzBatchCertificate</span></span>](./Get-AzBatchCertificate.md)

[<span data-ttu-id="cde65-146">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="cde65-146">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="cde65-147">Remove-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="cde65-147">Remove-AzBatchCertificate</span></span>](./Remove-AzBatchCertificate.md)

[<span data-ttu-id="cde65-148">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cde65-148">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
