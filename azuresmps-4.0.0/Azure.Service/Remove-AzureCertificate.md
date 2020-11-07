---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 4E3D405D-69FB-42C2-8A5B-BDBD27B63088
online version: ''
schema: 2.0.0
ms.openlocfilehash: 503c2e0a076be3f31b6435a30dc658af9b45835a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967613"
---
# <span data-ttu-id="90447-101">Remove-AzureCertificate</span><span class="sxs-lookup"><span data-stu-id="90447-101">Remove-AzureCertificate</span></span>

## <span data-ttu-id="90447-102">摘要</span><span class="sxs-lookup"><span data-stu-id="90447-102">SYNOPSIS</span></span>
<span data-ttu-id="90447-103">從 Azure 服務移除憑證。</span><span class="sxs-lookup"><span data-stu-id="90447-103">Removes a certificate from an Azure service.</span></span>

## <span data-ttu-id="90447-104">句法</span><span class="sxs-lookup"><span data-stu-id="90447-104">SYNTAX</span></span>

```
Remove-AzureCertificate [-ServiceName] <String> [-ThumbprintAlgorithm] <String> [-Thumbprint] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="90447-105">說明</span><span class="sxs-lookup"><span data-stu-id="90447-105">DESCRIPTION</span></span>
<span data-ttu-id="90447-106">**AzureCertificate** Cmdlet 會從 Azure 服務中移除憑證。</span><span class="sxs-lookup"><span data-stu-id="90447-106">The **Remove-AzureCertificate** cmdlet removes a certificate from an Azure service.</span></span>

## <span data-ttu-id="90447-107">示例</span><span class="sxs-lookup"><span data-stu-id="90447-107">EXAMPLES</span></span>

### <span data-ttu-id="90447-108">範例1：從服務移除憑證</span><span class="sxs-lookup"><span data-stu-id="90447-108">Example 1: Remove a certificate from a service</span></span>
```
PS C:\> Remove-AzureCertificate -ServiceName "ContosoService" -Thumbprint '5383CE0343CB6563281CA97C1D4D712209CFFA97'
```

<span data-ttu-id="90447-109">這個命令會從雲端服務中移除具有指定指紋的憑證物件。</span><span class="sxs-lookup"><span data-stu-id="90447-109">This command removes the certificate object that has the specified thumbprint from the cloud service.</span></span>

### <span data-ttu-id="90447-110">範例2：從服務移除所有憑證</span><span class="sxs-lookup"><span data-stu-id="90447-110">Example 2: Remove all certificates from a service</span></span>
```
PS C:\> Get-AzureCertificate -ServiceName "ContosoService" | Remove-AzureCertificate
```

<span data-ttu-id="90447-111">這個命令會使用 **AzureCertificate** Cmdlet，從名為 ContosoService 的服務取得所有憑證。</span><span class="sxs-lookup"><span data-stu-id="90447-111">This command gets all the certificates from the service named ContosoService by using the **Get-AzureCertificate** cmdlet.</span></span>
<span data-ttu-id="90447-112">命令會使用管線運算子，將每個憑證傳到目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="90447-112">The command passes each certificate to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="90447-113">該 Cmdlet 會從雲端服務移除每個憑證。</span><span class="sxs-lookup"><span data-stu-id="90447-113">That cmdlet removes each certificate from the cloud service.</span></span>

### <span data-ttu-id="90447-114">範例3：從使用特定指紋演算法的服務中移除所有憑證</span><span class="sxs-lookup"><span data-stu-id="90447-114">Example 3: Remove all certificates from a service that use a specific thumbprint algorithm</span></span>
```
PS C:\> Get-AzureCertificate -ServiceName "ContosoService" -ThumbprintAlgorithm "sha1" | Remove-AzureCertificate
```

<span data-ttu-id="90447-115">這個命令會從名為 ContosoService 的服務中取得所有使用 sha1 指紋演算法的憑證。</span><span class="sxs-lookup"><span data-stu-id="90447-115">This command gets all the certificates from the service named ContosoService that use the sha1 thumbprint algorithm.</span></span>
<span data-ttu-id="90447-116">該命令會將每個憑證傳遞到目前的 Cmdlet，這會移除每個憑證。</span><span class="sxs-lookup"><span data-stu-id="90447-116">The command passes each certificate to the current cmdlet, which removes each certificate.</span></span>

## <span data-ttu-id="90447-117">參數</span><span class="sxs-lookup"><span data-stu-id="90447-117">PARAMETERS</span></span>

### <span data-ttu-id="90447-118">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="90447-118">-InformationAction</span></span>
<span data-ttu-id="90447-119">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="90447-119">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="90447-120">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="90447-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="90447-121">持續</span><span class="sxs-lookup"><span data-stu-id="90447-121">Continue</span></span>
- <span data-ttu-id="90447-122">理會</span><span class="sxs-lookup"><span data-stu-id="90447-122">Ignore</span></span>
- <span data-ttu-id="90447-123">看</span><span class="sxs-lookup"><span data-stu-id="90447-123">Inquire</span></span>
- <span data-ttu-id="90447-124">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="90447-124">SilentlyContinue</span></span>
- <span data-ttu-id="90447-125">停止</span><span class="sxs-lookup"><span data-stu-id="90447-125">Stop</span></span>
- <span data-ttu-id="90447-126">封存</span><span class="sxs-lookup"><span data-stu-id="90447-126">Suspend</span></span>

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

### <span data-ttu-id="90447-127">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="90447-127">-InformationVariable</span></span>
<span data-ttu-id="90447-128">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="90447-128">Specifies an information variable.</span></span>

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

### <span data-ttu-id="90447-129">-設定檔</span><span class="sxs-lookup"><span data-stu-id="90447-129">-Profile</span></span>
<span data-ttu-id="90447-130">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="90447-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="90447-131">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="90447-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="90447-132">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="90447-132">-ServiceName</span></span>
<span data-ttu-id="90447-133">指定此 Cmdlet 從中移除憑證的 Azure 服務名稱。</span><span class="sxs-lookup"><span data-stu-id="90447-133">Specifies the name of the Azure service from which this cmdlet removes a certificate.</span></span>

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

### <span data-ttu-id="90447-134">-指紋</span><span class="sxs-lookup"><span data-stu-id="90447-134">-Thumbprint</span></span>
<span data-ttu-id="90447-135">指定此 Cmdlet 移除之憑證的指紋。</span><span class="sxs-lookup"><span data-stu-id="90447-135">Specifies the thumbprint of the certificate that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90447-136">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="90447-136">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="90447-137">指定用來建立憑證指紋的演算法。</span><span class="sxs-lookup"><span data-stu-id="90447-137">Specifies the algorithm that is used to create the certificate thumbprint.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90447-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90447-138">CommonParameters</span></span>
<span data-ttu-id="90447-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="90447-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90447-140">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="90447-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90447-141">輸入</span><span class="sxs-lookup"><span data-stu-id="90447-141">INPUTS</span></span>

## <span data-ttu-id="90447-142">輸出</span><span class="sxs-lookup"><span data-stu-id="90447-142">OUTPUTS</span></span>

### <span data-ttu-id="90447-143">ManagementOperationCoNtext</span><span class="sxs-lookup"><span data-stu-id="90447-143">ManagementOperationContext</span></span>

## <span data-ttu-id="90447-144">筆記</span><span class="sxs-lookup"><span data-stu-id="90447-144">NOTES</span></span>

## <span data-ttu-id="90447-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="90447-145">RELATED LINKS</span></span>

[<span data-ttu-id="90447-146">附加 AzureCertificate</span><span class="sxs-lookup"><span data-stu-id="90447-146">Add-AzureCertificate</span></span>](./Add-AzureCertificate.md)

[<span data-ttu-id="90447-147">AzureCertificate</span><span class="sxs-lookup"><span data-stu-id="90447-147">Get-AzureCertificate</span></span>](./Get-AzureCertificate.md)

[<span data-ttu-id="90447-148">新-AzureCertificateSetting</span><span class="sxs-lookup"><span data-stu-id="90447-148">New-AzureCertificateSetting</span></span>](./New-AzureCertificateSetting.md)


