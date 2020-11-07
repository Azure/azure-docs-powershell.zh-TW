---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7BEFA810-685C-4553-BED8-4CD6BCF8A5FE
online version: ''
schema: 2.0.0
ms.openlocfilehash: d88784e5d4fdd153700bd3879262198e5dd3807a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967802"
---
# <span data-ttu-id="8d9d1-101">Get-AzureCertificate</span><span class="sxs-lookup"><span data-stu-id="8d9d1-101">Get-AzureCertificate</span></span>

## <span data-ttu-id="8d9d1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8d9d1-102">SYNOPSIS</span></span>
<span data-ttu-id="8d9d1-103">從 Azure 服務取得憑證物件。</span><span class="sxs-lookup"><span data-stu-id="8d9d1-103">Gets a certificate object from an Azure service.</span></span>

## <span data-ttu-id="8d9d1-104">句法</span><span class="sxs-lookup"><span data-stu-id="8d9d1-104">SYNTAX</span></span>

```
Get-AzureCertificate [-ServiceName] <String> [-ThumbprintAlgorithm <String>] [-Thumbprint <String>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="8d9d1-105">說明</span><span class="sxs-lookup"><span data-stu-id="8d9d1-105">DESCRIPTION</span></span>
<span data-ttu-id="8d9d1-106">**AzureCertificate** Cmdlet 會從 Azure 服務取得證書物件。</span><span class="sxs-lookup"><span data-stu-id="8d9d1-106">The **Get-AzureCertificate** cmdlet gets a certificate object from an Azure service.</span></span>

## <span data-ttu-id="8d9d1-107">示例</span><span class="sxs-lookup"><span data-stu-id="8d9d1-107">EXAMPLES</span></span>

### <span data-ttu-id="8d9d1-108">範例1：從服務取得憑證</span><span class="sxs-lookup"><span data-stu-id="8d9d1-108">Example 1: Get certificates from a service</span></span>
```
PS C:\> $AzureCert = Get-AzureCertificate -ServiceName "ContosoService"
```

<span data-ttu-id="8d9d1-109">這個命令會從名為 ContosoService 的服務中取得證書物件，然後將它們儲存在 $AzureCert 變數中。</span><span class="sxs-lookup"><span data-stu-id="8d9d1-109">This command gets certificate objects from the service named ContosoService, and then stores them in the $AzureCert variable.</span></span>

### <span data-ttu-id="8d9d1-110">範例2：從服務取得憑證</span><span class="sxs-lookup"><span data-stu-id="8d9d1-110">Example 2: Get a certificate from a service</span></span>
```
PS C:\> $AzureCert = Get-AzureCertificate -ServiceName "ContosoService" -Thumbprint '5383CE0343CB6563281CA97C1D4D712209CFFA97'
```

<span data-ttu-id="8d9d1-111">這個命令會從名為 ContosoService 的服務中取得指定指紋所識別的憑證物件，然後將它儲存在 $AzureCert 變數中。</span><span class="sxs-lookup"><span data-stu-id="8d9d1-111">This command gets the certificate object identified by the specified thumbprint from the service named ContosoService, and then stores it in the $AzureCert variable.</span></span>

## <span data-ttu-id="8d9d1-112">參數</span><span class="sxs-lookup"><span data-stu-id="8d9d1-112">PARAMETERS</span></span>

### <span data-ttu-id="8d9d1-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="8d9d1-113">-InformationAction</span></span>
<span data-ttu-id="8d9d1-114">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="8d9d1-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="8d9d1-115">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="8d9d1-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8d9d1-116">持續</span><span class="sxs-lookup"><span data-stu-id="8d9d1-116">Continue</span></span>
- <span data-ttu-id="8d9d1-117">理會</span><span class="sxs-lookup"><span data-stu-id="8d9d1-117">Ignore</span></span>
- <span data-ttu-id="8d9d1-118">看</span><span class="sxs-lookup"><span data-stu-id="8d9d1-118">Inquire</span></span>
- <span data-ttu-id="8d9d1-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="8d9d1-119">SilentlyContinue</span></span>
- <span data-ttu-id="8d9d1-120">停止</span><span class="sxs-lookup"><span data-stu-id="8d9d1-120">Stop</span></span>
- <span data-ttu-id="8d9d1-121">封存</span><span class="sxs-lookup"><span data-stu-id="8d9d1-121">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d9d1-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="8d9d1-122">-InformationVariable</span></span>
<span data-ttu-id="8d9d1-123">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="8d9d1-123">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d9d1-124">-設定檔</span><span class="sxs-lookup"><span data-stu-id="8d9d1-124">-Profile</span></span>
<span data-ttu-id="8d9d1-125">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="8d9d1-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8d9d1-126">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="8d9d1-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d9d1-127">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="8d9d1-127">-ServiceName</span></span>
<span data-ttu-id="8d9d1-128">指定此 Cmdlet 取得憑證的 Azure 服務名稱。</span><span class="sxs-lookup"><span data-stu-id="8d9d1-128">Specifies the name of the Azure service from which this cmdlet gets a certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d9d1-129">-指紋</span><span class="sxs-lookup"><span data-stu-id="8d9d1-129">-Thumbprint</span></span>
<span data-ttu-id="8d9d1-130">指定此 Cmdlet 取得的憑證指紋。</span><span class="sxs-lookup"><span data-stu-id="8d9d1-130">Specifies the thumbprint of the certificate that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d9d1-131">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="8d9d1-131">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="8d9d1-132">指定用來建立憑證指紋的演算法。</span><span class="sxs-lookup"><span data-stu-id="8d9d1-132">Specifies the algorithm that is used to create the certificate thumbprint.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d9d1-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d9d1-133">CommonParameters</span></span>
<span data-ttu-id="8d9d1-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8d9d1-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d9d1-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8d9d1-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d9d1-136">輸入</span><span class="sxs-lookup"><span data-stu-id="8d9d1-136">INPUTS</span></span>

## <span data-ttu-id="8d9d1-137">輸出</span><span class="sxs-lookup"><span data-stu-id="8d9d1-137">OUTPUTS</span></span>

### <span data-ttu-id="8d9d1-138">CertificateCoNtext</span><span class="sxs-lookup"><span data-stu-id="8d9d1-138">CertificateContext</span></span>

## <span data-ttu-id="8d9d1-139">筆記</span><span class="sxs-lookup"><span data-stu-id="8d9d1-139">NOTES</span></span>

## <span data-ttu-id="8d9d1-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="8d9d1-140">RELATED LINKS</span></span>

[<span data-ttu-id="8d9d1-141">附加 AzureCertificate</span><span class="sxs-lookup"><span data-stu-id="8d9d1-141">Add-AzureCertificate</span></span>](./Add-AzureCertificate.md)

[<span data-ttu-id="8d9d1-142">新-AzureCertificateSetting</span><span class="sxs-lookup"><span data-stu-id="8d9d1-142">New-AzureCertificateSetting</span></span>](./New-AzureCertificateSetting.md)

[<span data-ttu-id="8d9d1-143">移除-AzureCertificate</span><span class="sxs-lookup"><span data-stu-id="8d9d1-143">Remove-AzureCertificate</span></span>](./Remove-AzureCertificate.md)


