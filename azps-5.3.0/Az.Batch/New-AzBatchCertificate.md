---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: B423C1A1-1988-4721-81E7-3B7EC163B03A
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchCertificate.md
ms.openlocfilehash: b7b3dae97e5af4b7d31edabb215ef25a32be6caf
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98446912"
---
# <span data-ttu-id="9052f-101">New-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="9052f-101">New-AzBatchCertificate</span></span>

## <span data-ttu-id="9052f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9052f-102">SYNOPSIS</span></span>
<span data-ttu-id="9052f-103">將憑證新增到指定的批次帳戶。</span><span class="sxs-lookup"><span data-stu-id="9052f-103">Adds a certificate to the specified Batch account.</span></span>

## <span data-ttu-id="9052f-104">句法</span><span class="sxs-lookup"><span data-stu-id="9052f-104">SYNTAX</span></span>

### <span data-ttu-id="9052f-105">檔案 (預設) </span><span class="sxs-lookup"><span data-stu-id="9052f-105">File (Default)</span></span>
```
New-AzBatchCertificate [-FilePath] <String> [-Password <SecureString>] [-Kind <PSCertificateKind>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9052f-106">RawData</span><span class="sxs-lookup"><span data-stu-id="9052f-106">RawData</span></span>
```
New-AzBatchCertificate [-RawData] <Byte[]> [-Password <SecureString>] [-Kind <PSCertificateKind>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9052f-107">說明</span><span class="sxs-lookup"><span data-stu-id="9052f-107">DESCRIPTION</span></span>
<span data-ttu-id="9052f-108">**新的-AzBatchCertificate** Cmdlet 會將憑證新增到指定的 Azure Batch 帳戶。</span><span class="sxs-lookup"><span data-stu-id="9052f-108">The **New-AzBatchCertificate** cmdlet adds a certificate to the specified Azure Batch account.</span></span>

## <span data-ttu-id="9052f-109">示例</span><span class="sxs-lookup"><span data-stu-id="9052f-109">EXAMPLES</span></span>

### <span data-ttu-id="9052f-110">範例1：從檔案新增憑證</span><span class="sxs-lookup"><span data-stu-id="9052f-110">Example 1: Add a certificate from a file</span></span>
```
PS C:\>New-AzBatchCertificate -FilePath "E:\Certificates\MyCert.cer" -BatchContext $Context
```

<span data-ttu-id="9052f-111">這個命令會使用 [檔案 E:\Certificates\MyCert.cer.]，將憑證新增到指定的批次帳戶</span><span class="sxs-lookup"><span data-stu-id="9052f-111">This command adds a certificate to the specified Batch account by using the file E:\Certificates\MyCert.cer.</span></span>

### <span data-ttu-id="9052f-112">範例2：從原始資料新增憑證</span><span class="sxs-lookup"><span data-stu-id="9052f-112">Example 2: Add a certificate from raw data</span></span>
```
PS C:\>$RawData = [System.IO.File]::ReadAllBytes("E:\Certificates\MyCert.pfx")
PS C:\> New-AzBatchCertificate -RawData $RawData -Password "Password1234" -BatchContext $Context
```

<span data-ttu-id="9052f-113">第一個命令會將名為 MyCert 的檔案中的資料讀入 $RawData 變數中。</span><span class="sxs-lookup"><span data-stu-id="9052f-113">The first command reads the data from the file named MyCert.pfx into the $RawData variable.</span></span>
<span data-ttu-id="9052f-114">第二個命令會使用儲存在 $RawData 中的原始資料，將憑證新增到指定的批次帳戶。</span><span class="sxs-lookup"><span data-stu-id="9052f-114">The second command adds a certificate to the specified Batch account using the raw data stored in $RawData.</span></span>

## <span data-ttu-id="9052f-115">參數</span><span class="sxs-lookup"><span data-stu-id="9052f-115">PARAMETERS</span></span>

### <span data-ttu-id="9052f-116">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="9052f-116">-BatchContext</span></span>
<span data-ttu-id="9052f-117">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="9052f-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="9052f-118">如果您使用 Get-AzBatchAccount Cmdlet 來取得您的 BatchAccountCoNtext，則在與批次服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="9052f-118">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="9052f-119">若要改為使用共用金鑰驗證，請使用 Get-AzBatchAccountKey Cmdlet 來取得已填入其便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="9052f-119">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="9052f-120">使用共用金鑰驗證時，預設會使用主要便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="9052f-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="9052f-121">若要變更要使用的索引鍵，請設定 BatchAccountCoNtext 屬性。</span><span class="sxs-lookup"><span data-stu-id="9052f-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="9052f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9052f-122">-DefaultProfile</span></span>
<span data-ttu-id="9052f-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9052f-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9052f-124">-FilePath</span><span class="sxs-lookup"><span data-stu-id="9052f-124">-FilePath</span></span>
<span data-ttu-id="9052f-125">指定憑證檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="9052f-125">Specifies the path of the certificate file.</span></span>
<span data-ttu-id="9052f-126">憑證檔案必須是 .cer 或 .pfx 格式。</span><span class="sxs-lookup"><span data-stu-id="9052f-126">The certificate file must be in either .cer or .pfx format.</span></span>

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

### <span data-ttu-id="9052f-127">類型</span><span class="sxs-lookup"><span data-stu-id="9052f-127">-Kind</span></span>
<span data-ttu-id="9052f-128">要建立的憑證類型。</span><span class="sxs-lookup"><span data-stu-id="9052f-128">The kind of certificate to create.</span></span> <span data-ttu-id="9052f-129">如果未指定此專案，系統會假設所有沒有密碼的憑證都是 CER，且所有密碼都是 PFX 的憑證。</span><span class="sxs-lookup"><span data-stu-id="9052f-129">If this is not specified, it is assumed that all certificates without a password are CER and all certificates with password are PFX.</span></span>

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

### <span data-ttu-id="9052f-130">-Password</span><span class="sxs-lookup"><span data-stu-id="9052f-130">-Password</span></span>
<span data-ttu-id="9052f-131">指定用來存取證書私密金鑰的密碼。</span><span class="sxs-lookup"><span data-stu-id="9052f-131">Specifies the password to access the certificate private key.</span></span>
<span data-ttu-id="9052f-132">如果您指定的憑證是 .pfx 格式，您必須指定此參數。</span><span class="sxs-lookup"><span data-stu-id="9052f-132">You must specify this parameter if you specify a certificate in .pfx format.</span></span>

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

### <span data-ttu-id="9052f-133">-RawData</span><span class="sxs-lookup"><span data-stu-id="9052f-133">-RawData</span></span>
<span data-ttu-id="9052f-134">指定 .cer 或 .pfx 格式的原始憑證資料。</span><span class="sxs-lookup"><span data-stu-id="9052f-134">Specifies the raw certificate data in either .cer or .pfx format.</span></span>

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

### <span data-ttu-id="9052f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9052f-135">CommonParameters</span></span>
<span data-ttu-id="9052f-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9052f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9052f-137">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="9052f-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9052f-138">輸入</span><span class="sxs-lookup"><span data-stu-id="9052f-138">INPUTS</span></span>

### <span data-ttu-id="9052f-139">System.object []</span><span class="sxs-lookup"><span data-stu-id="9052f-139">System.Byte[]</span></span>

### <span data-ttu-id="9052f-140">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="9052f-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="9052f-141">輸出</span><span class="sxs-lookup"><span data-stu-id="9052f-141">OUTPUTS</span></span>

### <span data-ttu-id="9052f-142">System.void</span><span class="sxs-lookup"><span data-stu-id="9052f-142">System.Void</span></span>

## <span data-ttu-id="9052f-143">筆記</span><span class="sxs-lookup"><span data-stu-id="9052f-143">NOTES</span></span>

## <span data-ttu-id="9052f-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="9052f-144">RELATED LINKS</span></span>

[<span data-ttu-id="9052f-145">AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="9052f-145">Get-AzBatchCertificate</span></span>](./Get-AzBatchCertificate.md)

[<span data-ttu-id="9052f-146">AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="9052f-146">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="9052f-147">移除-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="9052f-147">Remove-AzBatchCertificate</span></span>](./Remove-AzBatchCertificate.md)

[<span data-ttu-id="9052f-148">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="9052f-148">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
