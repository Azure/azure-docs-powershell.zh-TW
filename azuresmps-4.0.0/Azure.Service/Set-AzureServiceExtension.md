---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: D37920D3-AF6C-4CFC-B9A3-8ED931AEC0DC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 318683c26d05c624549363ff1afe4a2b963c1fe6
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93966893"
---
# <span data-ttu-id="42091-101">Set-AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="42091-101">Set-AzureServiceExtension</span></span>

## <span data-ttu-id="42091-102">摘要</span><span class="sxs-lookup"><span data-stu-id="42091-102">SYNOPSIS</span></span>
<span data-ttu-id="42091-103">在部署中加入雲端服務延伸。</span><span class="sxs-lookup"><span data-stu-id="42091-103">Adds a cloud service extension to a deployment.</span></span>

## <span data-ttu-id="42091-104">句法</span><span class="sxs-lookup"><span data-stu-id="42091-104">SYNTAX</span></span>

### <span data-ttu-id="42091-105">SetExtension (預設) </span><span class="sxs-lookup"><span data-stu-id="42091-105">SetExtension (Default)</span></span>
```
Set-AzureServiceExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [[-X509Certificate] <X509Certificate2>] [[-ThumbprintAlgorithm] <String>] [-ExtensionName] <String>
 [-ProviderNamespace] <String> [-PublicConfiguration] <String> [-PrivateConfiguration] <String>
 [-Version] <String> [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="42091-106">SetExtensionUsingThumbprint</span><span class="sxs-lookup"><span data-stu-id="42091-106">SetExtensionUsingThumbprint</span></span>
```
Set-AzureServiceExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [-CertificateThumbprint] <String> [[-ThumbprintAlgorithm] <String>] [-ExtensionName] <String>
 [-ProviderNamespace] <String> [-PublicConfiguration] <String> [-PrivateConfiguration] <String>
 [-Version] <String> [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="42091-107">說明</span><span class="sxs-lookup"><span data-stu-id="42091-107">DESCRIPTION</span></span>
<span data-ttu-id="42091-108">**AzureServiceExtension** Cmdlet 會將雲端服務延伸新增至部署。</span><span class="sxs-lookup"><span data-stu-id="42091-108">The **Set-AzureServiceExtension** cmdlet adds a cloud service extension to a deployment.</span></span>

## <span data-ttu-id="42091-109">示例</span><span class="sxs-lookup"><span data-stu-id="42091-109">EXAMPLES</span></span>

### <span data-ttu-id="42091-110">範例1：在部署中加入雲端服務</span><span class="sxs-lookup"><span data-stu-id="42091-110">Example 1: Add a cloud service to a deployment</span></span>
```
PS C:\> Set-AzureServiceExtension -Service $Svc -Slot "Production" -ExtensionName "RDP" -Version "1.0" -ProviderNamespace "Microsoft.Windows.Azure.Extensions" -PublicConfiguration $P1 -PrivateConfiguration $P2;
```

<span data-ttu-id="42091-111">這個命令會將雲端服務新增至部署。</span><span class="sxs-lookup"><span data-stu-id="42091-111">This command adds a cloud service to a deployment.</span></span>

### <span data-ttu-id="42091-112">範例2：將雲端服務新增至指定角色的部署</span><span class="sxs-lookup"><span data-stu-id="42091-112">Example 2: Add a cloud service to a deployment for a specified role</span></span>
```
PS C:\> Set-AzureServiceExtension -Service $Svc -Slot "Production" -Role "WebRole1" -ExtensionName "RDP" -ProviderNamespace "Microsoft.Windows.Azure.Extensions" -PublicConfiguration $P1 -PrivateConfiguration $P2;
```

<span data-ttu-id="42091-113">這個命令會將雲端服務新增至指定角色的部署。</span><span class="sxs-lookup"><span data-stu-id="42091-113">This command adds a cloud service to a deployment for a specified role.</span></span>

## <span data-ttu-id="42091-114">參數</span><span class="sxs-lookup"><span data-stu-id="42091-114">PARAMETERS</span></span>

### <span data-ttu-id="42091-115">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="42091-115">-CertificateThumbprint</span></span>
<span data-ttu-id="42091-116">指定要用來加密私人配置的憑證指紋。</span><span class="sxs-lookup"><span data-stu-id="42091-116">Specifies a certificate thumbprint to use to encrypt the private configuration.</span></span>
<span data-ttu-id="42091-117">此憑證必須已存在於憑證存放區中。</span><span class="sxs-lookup"><span data-stu-id="42091-117">This certificate has to already exist in the certificate store.</span></span>
<span data-ttu-id="42091-118">如果您沒有指定憑證，此 Cmdlet 會建立證書。</span><span class="sxs-lookup"><span data-stu-id="42091-118">If you do not specify a certificate, this cmdlet creates a certificate.</span></span>

```yaml
Type: String
Parameter Sets: SetExtensionUsingThumbprint
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42091-119">-ExtensionId</span><span class="sxs-lookup"><span data-stu-id="42091-119">-ExtensionId</span></span>
<span data-ttu-id="42091-120">指定延伸 ID。</span><span class="sxs-lookup"><span data-stu-id="42091-120">Specifies the extension ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42091-121">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="42091-121">-ExtensionName</span></span>
<span data-ttu-id="42091-122">指定副檔名。</span><span class="sxs-lookup"><span data-stu-id="42091-122">Specifies the extension name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42091-123">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="42091-123">-InformationAction</span></span>
<span data-ttu-id="42091-124">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="42091-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="42091-125">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="42091-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="42091-126">持續</span><span class="sxs-lookup"><span data-stu-id="42091-126">Continue</span></span>
- <span data-ttu-id="42091-127">理會</span><span class="sxs-lookup"><span data-stu-id="42091-127">Ignore</span></span>
- <span data-ttu-id="42091-128">看</span><span class="sxs-lookup"><span data-stu-id="42091-128">Inquire</span></span>
- <span data-ttu-id="42091-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="42091-129">SilentlyContinue</span></span>
- <span data-ttu-id="42091-130">停止</span><span class="sxs-lookup"><span data-stu-id="42091-130">Stop</span></span>
- <span data-ttu-id="42091-131">封存</span><span class="sxs-lookup"><span data-stu-id="42091-131">Suspend</span></span>

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

### <span data-ttu-id="42091-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="42091-132">-InformationVariable</span></span>
<span data-ttu-id="42091-133">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="42091-133">Specifies an information variable.</span></span>

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

### <span data-ttu-id="42091-134">-PrivateConfiguration</span><span class="sxs-lookup"><span data-stu-id="42091-134">-PrivateConfiguration</span></span>
<span data-ttu-id="42091-135">指定私人配置文字。</span><span class="sxs-lookup"><span data-stu-id="42091-135">Specifies the private configuration text.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42091-136">-設定檔</span><span class="sxs-lookup"><span data-stu-id="42091-136">-Profile</span></span>
<span data-ttu-id="42091-137">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="42091-137">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="42091-138">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="42091-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="42091-139">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="42091-139">-ProviderNamespace</span></span>
<span data-ttu-id="42091-140">指定延伸提供者命名空間。</span><span class="sxs-lookup"><span data-stu-id="42091-140">Specifies the extension provider namespace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42091-141">-PublicConfiguration</span><span class="sxs-lookup"><span data-stu-id="42091-141">-PublicConfiguration</span></span>
<span data-ttu-id="42091-142">指定公用配置文字。</span><span class="sxs-lookup"><span data-stu-id="42091-142">Specifies the public configuration text.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42091-143">-角色</span><span class="sxs-lookup"><span data-stu-id="42091-143">-Role</span></span>
<span data-ttu-id="42091-144">指定要指定其遠端桌面設定的選擇性角色陣列。</span><span class="sxs-lookup"><span data-stu-id="42091-144">Specifies an optional array of roles for which to specify the remote desktop configuration.</span></span>
<span data-ttu-id="42091-145">如果未指定此參數，則會將遠端桌面設定套用為所有角色的預設配置。</span><span class="sxs-lookup"><span data-stu-id="42091-145">If this parameter is not specified the remote desktop configuration is applied as the default configuration for all roles.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42091-146">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="42091-146">-ServiceName</span></span>
<span data-ttu-id="42091-147">指定部署的 Azure 服務名稱。</span><span class="sxs-lookup"><span data-stu-id="42091-147">Specifies the Azure service name of the deployment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42091-148">-槽</span><span class="sxs-lookup"><span data-stu-id="42091-148">-Slot</span></span>
<span data-ttu-id="42091-149">指定要修改的部署環境。</span><span class="sxs-lookup"><span data-stu-id="42091-149">Specifies the environment of the deployment to modify.</span></span>
<span data-ttu-id="42091-150">有效值為： [生產] 或 [轉移]。</span><span class="sxs-lookup"><span data-stu-id="42091-150">Valid values are: Production or Staging.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42091-151">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="42091-151">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="42091-152">指定與指紋搭配使用以識別憑證的指紋雜湊演算法。</span><span class="sxs-lookup"><span data-stu-id="42091-152">Specifies the thumbprint hashing algorithm which is used with the thumbprint to identify the certificate.</span></span>
<span data-ttu-id="42091-153">這個參數是選用的，預設值是 sha1。</span><span class="sxs-lookup"><span data-stu-id="42091-153">This parameter is optional and the default is sha1.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42091-154">-版本</span><span class="sxs-lookup"><span data-stu-id="42091-154">-Version</span></span>
<span data-ttu-id="42091-155">指定副檔名版本。</span><span class="sxs-lookup"><span data-stu-id="42091-155">Specifies the extension version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42091-156">-X509Certificate</span><span class="sxs-lookup"><span data-stu-id="42091-156">-X509Certificate</span></span>
<span data-ttu-id="42091-157">指定會自動上傳到雲端服務的 x.509 憑證，並用於加密延伸私人配置。</span><span class="sxs-lookup"><span data-stu-id="42091-157">Specifies an X.509 certificate that is automatically uploaded to the cloud service and used for encrypting the extension private configuration.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: SetExtension
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42091-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42091-158">CommonParameters</span></span>
<span data-ttu-id="42091-159">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="42091-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42091-160">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="42091-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42091-161">輸入</span><span class="sxs-lookup"><span data-stu-id="42091-161">INPUTS</span></span>

## <span data-ttu-id="42091-162">輸出</span><span class="sxs-lookup"><span data-stu-id="42091-162">OUTPUTS</span></span>

## <span data-ttu-id="42091-163">筆記</span><span class="sxs-lookup"><span data-stu-id="42091-163">NOTES</span></span>

## <span data-ttu-id="42091-164">相關連結</span><span class="sxs-lookup"><span data-stu-id="42091-164">RELATED LINKS</span></span>

[<span data-ttu-id="42091-165">AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="42091-165">Get-AzureServiceExtension</span></span>](./Get-AzureServiceExtension.md)

[<span data-ttu-id="42091-166">移除-AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="42091-166">Remove-AzureServiceExtension</span></span>](./Remove-AzureServiceExtension.md)


