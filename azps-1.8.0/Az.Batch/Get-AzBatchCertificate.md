---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: A9C98F8F-90F2-4BF4-A234-31966FBB975B
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchCertificate.md
ms.openlocfilehash: ed1b4baac3d22789fe08964e4b4d31b53eee7223
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/13/2020
ms.locfileid: "93623342"
---
# <span data-ttu-id="fe84e-101">Get-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="fe84e-101">Get-AzBatchCertificate</span></span>

## <span data-ttu-id="fe84e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fe84e-102">SYNOPSIS</span></span>
<span data-ttu-id="fe84e-103">取得批次帳戶中的憑證。</span><span class="sxs-lookup"><span data-stu-id="fe84e-103">Gets the certificates in a Batch account.</span></span>

## <span data-ttu-id="fe84e-104">句法</span><span class="sxs-lookup"><span data-stu-id="fe84e-104">SYNTAX</span></span>

### <span data-ttu-id="fe84e-105">ODataFilter (預設) </span><span class="sxs-lookup"><span data-stu-id="fe84e-105">ODataFilter (Default)</span></span>
```
Get-AzBatchCertificate [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fe84e-106">指紋</span><span class="sxs-lookup"><span data-stu-id="fe84e-106">Thumbprint</span></span>
```
Get-AzBatchCertificate [-ThumbprintAlgorithm] <String> [-Thumbprint] <String> [-Select <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fe84e-107">說明</span><span class="sxs-lookup"><span data-stu-id="fe84e-107">DESCRIPTION</span></span>
<span data-ttu-id="fe84e-108">**AzBatchCertificate** Cmdlet 會取得 Azure Batch 帳戶中 *BatchCoNtext* 參數指定的憑證。</span><span class="sxs-lookup"><span data-stu-id="fe84e-108">The **Get-AzBatchCertificate** cmdlet gets the certificates in the Azure Batch account that the *BatchContext* parameter specifies.</span></span>
<span data-ttu-id="fe84e-109">若要取得特定的憑證，請指定 *ThumbprintAlgorithm* 和 *指紋* 參數。</span><span class="sxs-lookup"><span data-stu-id="fe84e-109">To obtain a particular certificate, specify the *ThumbprintAlgorithm* and *Thumbprint* parameters.</span></span>
<span data-ttu-id="fe84e-110">指定 *篩選* 參數，以取得符合開放式資料通訊協定 (OData) 篩選的憑證。</span><span class="sxs-lookup"><span data-stu-id="fe84e-110">Specify the *Filter* parameter to get the certificates that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="fe84e-111">示例</span><span class="sxs-lookup"><span data-stu-id="fe84e-111">EXAMPLES</span></span>

### <span data-ttu-id="fe84e-112">範例1：透過指紋取得憑證</span><span class="sxs-lookup"><span data-stu-id="fe84e-112">Example 1: Get a certificate by thumbprint</span></span>
```
PS C:\>Get-AzBatchCertificate -ThumbprintAlgorithm "sha1" - Thumbprint "C1E494A415149C5F211C4778B52F2E834A07247C" -BatchContext $Context
Thumbprint                  : c1e494a415149c5f211c4778b52f2e834a07247c
ThumbprintAlgorithm         : sha1
Url                         : https://pstests.eastus.batch.azure.com/certificates(thumbprintAlgorithm=sha1,thumbprint=C1E494A415149C5F211C4778B52F2E834A07247
C) 
State                       : Active
StateTransitionTime         : 10/6/2015 6:21:16 PM
PreviousState               : 
PreviousStateTransitionTime : 
Data                        : 
CertificateFormat           : 
Password                    : 
PublicData                  : MIIB9DCCAWGgAwIBAgIQpUXhwCuAPJRDhl7kY/0PdTAJBgUrDgMCHQUAMBYxFDASBgNVBAMTC0JhdGNoVGVzdDAxMB4XDTE1MTAwMjE2MjkwNVoXDTM5MTIzMTIzNTk
1OVowFjEUMBIGA1UEAxMLQmF0Y2hUZXN0MDEwgZ8wDQYJKoZIhvcNAQEBBQADgY0AMIGJAoGBAM06unpRipn3BmHBM75d0s8w/Wwifci16PoJo4c2V68GwsCCFsNOn5
ypo7BBXo1fpBjrnso5w+koaE5LjxkBSVm+TkogwbKlW6WURTM0O5viRVbPnEEU/Y01Pj5cJElFuLEk9Uoe/r/lP8b5A607t1cPjSXkwhEZEYc3LkHDSo0ZAgMBAAGjS
zBJMEcGA1UdAQRAMD6AEFRsTAsrvF+FmPuICooZXaKhGDAWMRQwEgYDVQQDEwtCYXRjaFRlc3QwMYIQpUXhwCuAPJRDhl7kY/0PdTAJBgUrDgMCHQUAA4GBALt0F8Ep
+8XVE/M2aNtxzlku72gxiOiAo1HmpUaixXx3gl8kdP3xgoKMaq4JskqdLmbJJUnCQ3wmzsdPwjswsW2ycT12zuBddaiS+id98k8U/KYc6FxMgS+H70FYOxARLn7P4FS
SBf/QCyign+BherzezdZ5NBdfzbmWxIMP5iFJ
DeleteCertificateError      :
```

<span data-ttu-id="fe84e-113">這個命令會取得擁有指定指紋的單一憑證。</span><span class="sxs-lookup"><span data-stu-id="fe84e-113">This command gets a single certificate that has the specified thumbprint.</span></span>
<span data-ttu-id="fe84e-114">憑證指紋演算法是 sha1。</span><span class="sxs-lookup"><span data-stu-id="fe84e-114">The certificate thumbprint algorithm is sha1.</span></span>

### <span data-ttu-id="fe84e-115">範例2：取得篩選的憑證</span><span class="sxs-lookup"><span data-stu-id="fe84e-115">Example 2: Get filtered certificates</span></span>
```
PS C:\>Get-AzBatchCertificate -Filter "state eq 'active'" -BatchContext $Context
Thumbprint                  : 025b351b087a084c5067f5e71eff8591970323f9
ThumbprintAlgorithm         : sha1
Url                         : https://pstests.eastus.batch.azure.com/certificates(thumbprintAlgorithm=sha1,thumbprint=025b351b087a084c5067f5e71eff8591970323f9) 
State                       : Active
StateTransitionTime         : 10/6/2015 6:21:17 PM
PreviousState               : 
PreviousStateTransitionTime : 
Data                        : 
CertificateFormat           : 
Password                    : 
PublicData                  : MIIB9DCCAWGgAwIBAgIQy9W5y8iwhppGhtAG06dHKTAJBgUrDgMCHQUAMBYxFDASBgNVBAMTC0JhdGNoVGVzdDAyMB4XDTE1MTAwMjE2MjkxNFoXDTM5MTIzMTIzNTk
1OVowFjEUMBIGA1UEAxMLQmF0Y2hUZXN0MDIwgZ8wDQYJKoZIhvcNAQEBBQADgY0AMIGJAoGBAJxagvVrlnKfv6hfzSiFJUkdGkPjC3tFiKebK6IaeHzesFdFfupXUE
wT0xOWh9xwa3OVkPECEc/u1sw3iVX/J4AODiwzmOWutoVRpWjxGFpgw9+dPvXMjs/Ue7JL7ag3siHs5EcarW91qKbgtko6i/r4emaRyk60U93TrbWQAWJ9AgMBAAGjS
zBJMEcGA1UdAQRAMD6AEAdqsOpyeXF/uDe7ZGKeez+hGDAWMRQwEgYDVQQDEwtCYXRjaFRlc3QwMoIQy9W5y8iwhppGhtAG06dHKTAJBgUrDgMCHQUAA4GBAC0MaAem
6ByyURFvGnFZyjEepjXC5wcaGq+gguDFe8rG88ceig1ZqewdcmC1y4p05uBhbmETbYVWzJarNsHYq2LTihi4t2J4jt2YVYz/IRdUB82iaFFbJRSPrN+6xD3KM2lve5N
4OjtlZAdiXiSUYFf3I6ypberUsAdba3QQajCN
DeleteCertificateError      : 

Thumbprint                  : c1e494a415149c5f211c4778b52f2e834a07247c
ThumbprintAlgorithm         : sha1
Url                         : https://pstests.eastus.batch.azure.com/certificates(thumbprintAlgorithm=sha1,thumbprint=c1e494a415149c5f211c4778b52f2e834a07247c) 
State                       : Active
StateTransitionTime         : 10/6/2015 6:21:16 PM
PreviousState               : 
PreviousStateTransitionTime : 
Data                        : 
CertificateFormat           : 
Password                    : 
PublicData                  : MIIB9DCCAWGgAwIBAgIQpUXhwCuAPJRDhl7kY/0PdTAJBgUrDgMCHQUAMBYxFDASBgNVBAMTC0JhdGNoVGVzdDAxMB4XDTE1MTAwMjE2MjkwNVoXDTM5MTIzMTIzNTk
1OVowFjEUMBIGA1UEAxMLQmF0Y2hUZXN0MDEwgZ8wDQYJKoZIhvcNAQEBBQADgY0AMIGJAoGBAM06unpRipn3BmHBM75d0s8w/Wwifci16PoJo4c2V68GwsCCFsNOn5
ypo7BBXo1fpBjrnso5w+koaE5LjxkBSVm+TkogwbKlW6WURTM0O5viRVbPnEEU/Y01Pj5cJElFuLEk9Uoe/r/lP8b5A607t1cPjSXkwhEZEYc3LkHDSo0ZAgMBAAGjS
zBJMEcGA1UdAQRAMD6AEFRsTAsrvF+FmPuICooZXaKhGDAWMRQwEgYDVQQDEwtCYXRjaFRlc3QwMYIQpUXhwCuAPJRDhl7kY/0PdTAJBgUrDgMCHQUAA4GBALt0F8Ep
+8XVE/M2aNtxzlku72gxiOiAo1HmpUaixXx3gl8kdP3xgoKMaq4JskqdLmbJJUnCQ3wmzsdPwjswsW2ycT12zuBddaiS+id98k8U/KYc6FxMgS+H70FYOxARLn7P4FS
SBf/QCyign+BherzezdZ5NBdfzbmWxIMP5iFJ
DeleteCertificateError      :
```

<span data-ttu-id="fe84e-116">這個命令會從批次帳戶取得處於作用中狀態的所有憑證。</span><span class="sxs-lookup"><span data-stu-id="fe84e-116">This command gets all certificates in the active state from the Batch account.</span></span>
<span data-ttu-id="fe84e-117">*Filter* 參數會指定狀態。</span><span class="sxs-lookup"><span data-stu-id="fe84e-117">The *Filter* parameter specifies the state.</span></span>

## <span data-ttu-id="fe84e-118">參數</span><span class="sxs-lookup"><span data-stu-id="fe84e-118">PARAMETERS</span></span>

### <span data-ttu-id="fe84e-119">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="fe84e-119">-BatchContext</span></span>
<span data-ttu-id="fe84e-120">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="fe84e-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="fe84e-121">如果您使用 Get-AzBatchAccount Cmdlet 來取得您的 BatchAccountCoNtext，則在與批次服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="fe84e-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="fe84e-122">若要改為使用共用金鑰驗證，請使用 Get-AzBatchAccountKeys Cmdlet 來取得已填入其便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="fe84e-122">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="fe84e-123">使用共用金鑰驗證時，預設會使用主要便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="fe84e-123">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="fe84e-124">若要變更要使用的索引鍵，請設定 BatchAccountCoNtext 屬性。</span><span class="sxs-lookup"><span data-stu-id="fe84e-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="fe84e-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe84e-125">-DefaultProfile</span></span>
<span data-ttu-id="fe84e-126">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="fe84e-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fe84e-127">-篩選</span><span class="sxs-lookup"><span data-stu-id="fe84e-127">-Filter</span></span>
<span data-ttu-id="fe84e-128">指定 OData 篩選子句。</span><span class="sxs-lookup"><span data-stu-id="fe84e-128">Specifies an OData filter clause.</span></span>
<span data-ttu-id="fe84e-129">如果您指定此參數，此 Cmdlet 會取得符合篩選器的憑證。</span><span class="sxs-lookup"><span data-stu-id="fe84e-129">If you specify this parameter, this cmdlet gets the certificates that match the filter.</span></span>

```yaml
Type: System.String
Parameter Sets: ODataFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe84e-130">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="fe84e-130">-MaxCount</span></span>
<span data-ttu-id="fe84e-131">指定要傳回的憑證數目上限。</span><span class="sxs-lookup"><span data-stu-id="fe84e-131">Specifies the maximum number of certificates to return.</span></span>
<span data-ttu-id="fe84e-132">如果您指定的值為零 (0) 或更小，則 Cmdlet 不會使用上限。</span><span class="sxs-lookup"><span data-stu-id="fe84e-132">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="fe84e-133">預設值為1000。</span><span class="sxs-lookup"><span data-stu-id="fe84e-133">The default value is 1000.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ODataFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe84e-134">-選取</span><span class="sxs-lookup"><span data-stu-id="fe84e-134">-Select</span></span>
<span data-ttu-id="fe84e-135">指定 OData select 子句。</span><span class="sxs-lookup"><span data-stu-id="fe84e-135">Specifies an OData select clause.</span></span>
<span data-ttu-id="fe84e-136">指定此參數的值，以取得特定屬性，而不是所有物件屬性。</span><span class="sxs-lookup"><span data-stu-id="fe84e-136">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="fe84e-137">-指紋</span><span class="sxs-lookup"><span data-stu-id="fe84e-137">-Thumbprint</span></span>
<span data-ttu-id="fe84e-138">指定此 Cmdlet 取得的憑證指紋。</span><span class="sxs-lookup"><span data-stu-id="fe84e-138">Specifies the thumbprint of the certificate that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: Thumbprint
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe84e-139">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="fe84e-139">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="fe84e-140">指定用來衍生 *指紋* 參數的演算法。</span><span class="sxs-lookup"><span data-stu-id="fe84e-140">Specifies the algorithm used to derive the *Thumbprint* parameter.</span></span>
<span data-ttu-id="fe84e-141">目前，唯一有效的值是 sha1。</span><span class="sxs-lookup"><span data-stu-id="fe84e-141">Currently, the only valid value is sha1.</span></span>

```yaml
Type: System.String
Parameter Sets: Thumbprint
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe84e-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe84e-142">CommonParameters</span></span>
<span data-ttu-id="fe84e-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fe84e-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe84e-144">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="fe84e-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe84e-145">輸入</span><span class="sxs-lookup"><span data-stu-id="fe84e-145">INPUTS</span></span>

### <span data-ttu-id="fe84e-146">System.object</span><span class="sxs-lookup"><span data-stu-id="fe84e-146">System.String</span></span>

### <span data-ttu-id="fe84e-147">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="fe84e-147">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="fe84e-148">輸出</span><span class="sxs-lookup"><span data-stu-id="fe84e-148">OUTPUTS</span></span>

### <span data-ttu-id="fe84e-149">Microsoft.Azure.Commands.Batch。PSCertificate</span><span class="sxs-lookup"><span data-stu-id="fe84e-149">Microsoft.Azure.Commands.Batch.Models.PSCertificate</span></span>

## <span data-ttu-id="fe84e-150">筆記</span><span class="sxs-lookup"><span data-stu-id="fe84e-150">NOTES</span></span>

## <span data-ttu-id="fe84e-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="fe84e-151">RELATED LINKS</span></span>

[<span data-ttu-id="fe84e-152">AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="fe84e-152">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="fe84e-153">新-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="fe84e-153">New-AzBatchCertificate</span></span>](./New-AzBatchCertificate.md)

[<span data-ttu-id="fe84e-154">移除-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="fe84e-154">Remove-AzBatchCertificate</span></span>](./Remove-AzBatchCertificate.md)

[<span data-ttu-id="fe84e-155">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="fe84e-155">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


