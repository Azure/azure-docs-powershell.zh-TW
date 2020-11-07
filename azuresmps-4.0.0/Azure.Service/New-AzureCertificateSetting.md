---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 11919623-9EDF-42A3-93FE-54E93D76D3D0
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7492dbdea0f924e364ac1acf5ce30476e34782d6
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967378"
---
# <span data-ttu-id="9e092-101">New-AzureCertificateSetting</span><span class="sxs-lookup"><span data-stu-id="9e092-101">New-AzureCertificateSetting</span></span>

## <span data-ttu-id="9e092-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9e092-102">SYNOPSIS</span></span>
<span data-ttu-id="9e092-103">為憑證建立憑證設定物件在服務中。</span><span class="sxs-lookup"><span data-stu-id="9e092-103">Creates a certificate setting object for a certificate is in a service.</span></span>

## <span data-ttu-id="9e092-104">句法</span><span class="sxs-lookup"><span data-stu-id="9e092-104">SYNTAX</span></span>

```
New-AzureCertificateSetting [[-StoreName] <String>] [-Thumbprint] <String>
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="9e092-105">說明</span><span class="sxs-lookup"><span data-stu-id="9e092-105">DESCRIPTION</span></span>
<span data-ttu-id="9e092-106">**新的-AzureCertificateSetting** Cmdlet 會針對 Azure 服務中的憑證建立憑證設定物件。</span><span class="sxs-lookup"><span data-stu-id="9e092-106">The **New-AzureCertificateSetting** cmdlet creates a certificate setting object for a certificate that is in an Azure service.</span></span>

<span data-ttu-id="9e092-107">您可以使用 [憑證設定] 物件，透過 **AzureProvisioningConfig** Cmdlet 來建立設定物件。</span><span class="sxs-lookup"><span data-stu-id="9e092-107">You can use a certificate setting object to create a configuration object by using the **Add-AzureProvisioningConfig** cmdlet.</span></span>
<span data-ttu-id="9e092-108">使用 configuration 物件，透過 **新的 add-azurevm** Cmdlet 來建立虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="9e092-108">Use a configuration object to create virtual machine by using the **New-AzureVM** cmdlet.</span></span>
<span data-ttu-id="9e092-109">您可以使用憑證設定物件，透過 **AzureQuickVM** Cmdlet 來建立虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="9e092-109">You can use a certificate setting object to create a virtual machine by using the **New-AzureQuickVM** cmdlet.</span></span>

## <span data-ttu-id="9e092-110">示例</span><span class="sxs-lookup"><span data-stu-id="9e092-110">EXAMPLES</span></span>

### <span data-ttu-id="9e092-111">範例1：建立憑證設定物件</span><span class="sxs-lookup"><span data-stu-id="9e092-111">Example 1: Create a certificate setting object</span></span>
```
PS C:\> New-AzureCertificateSetting -Thumbprint "D7BECD4D63EBAF86023BB41FA5FBF5C2C924902A" -StoreName "My"
```

<span data-ttu-id="9e092-112">這個命令會為現有的憑證建立憑證設定物件。</span><span class="sxs-lookup"><span data-stu-id="9e092-112">This command creates a certificate setting object for an existing certificate.</span></span>

### <span data-ttu-id="9e092-113">範例2：建立使用配置設定物件的虛擬機器</span><span class="sxs-lookup"><span data-stu-id="9e092-113">Example 2: Create a virtual machine that uses a configuration setting object</span></span>
```
PS C:\> Add-AzureCertificate -ServiceName "ContosoService" -CertToDeploy "C:\temp\ContosoCert.cer"
PS C:\> $CertificateSetting = New-AzureCertificateSetting -Thumbprint "D7BECD4D63EBAF86023BB41FA5FBF5C2C924902A" -StoreName "My" 
PS C:\> $Image = Get-AzureVMImage -ImageName "ContosoStandard"
PS C:\> New-AzureVMConfig -Name "VirtualMachine17" -InstanceSize Small -ImageName $Image | Add-AzureProvisioningConfig -Windows -Certificates $CertificateSetting -Password "password" | New-AzureVM -ServiceName "ContosoService"
```

<span data-ttu-id="9e092-114">第一個命令會使用 **Add-AzureCertificate** Cmdlet，將憑證 ContosoCert 新增到名為 ContosoService 的服務。</span><span class="sxs-lookup"><span data-stu-id="9e092-114">The first command adds the certificate ContosoCert.cer to the service named ContosoService by using the **Add-AzureCertificate** cmdlet.</span></span>

<span data-ttu-id="9e092-115">第二個命令會建立憑證設定物件，然後將它儲存在 $CertificateSetting 變數中。</span><span class="sxs-lookup"><span data-stu-id="9e092-115">The second command creates a certificate setting object, and then stores it in the $CertificateSetting variable.</span></span>

<span data-ttu-id="9e092-116">第三個命令會使用 **AzureVMImage** Cmdlet 從影像儲存庫中取得影像。</span><span class="sxs-lookup"><span data-stu-id="9e092-116">The third command gets an image from the image repository by using the **Get-AzureVMImage** cmdlet.</span></span>
<span data-ttu-id="9e092-117">這個命令會將圖像儲存在 $Image 變數中。</span><span class="sxs-lookup"><span data-stu-id="9e092-117">This command store the image in the $Image variable.</span></span>

<span data-ttu-id="9e092-118">最終命令會使用 **AzureVMConfig** Cmdlet，根據 $Image 中的影像建立虛擬機器設定物件。</span><span class="sxs-lookup"><span data-stu-id="9e092-118">The final command creates a virtual machine configuration object based on the image in $Image by using the **New-AzureVMConfig** cmdlet.</span></span>
<span data-ttu-id="9e092-119">命令會使用管線運算子，將該物件傳遞到 **AzureProvisioningConfig** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9e092-119">The command passes that object to the **Add-AzureProvisioningConfig** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="9e092-120">該 Cmdlet 會將提供資訊新增到設定。</span><span class="sxs-lookup"><span data-stu-id="9e092-120">That cmdlet add provisioning information to the configuration.</span></span>
<span data-ttu-id="9e092-121">該命令會將物件傳遞給 **新的 add-azurevm** Cmdlet，這會建立虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="9e092-121">The command passes the object to the **New-AzureVM** cmdlet, which creates the virtual machine.</span></span>

## <span data-ttu-id="9e092-122">參數</span><span class="sxs-lookup"><span data-stu-id="9e092-122">PARAMETERS</span></span>

### <span data-ttu-id="9e092-123">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="9e092-123">-InformationAction</span></span>
<span data-ttu-id="9e092-124">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="9e092-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="9e092-125">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="9e092-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9e092-126">持續</span><span class="sxs-lookup"><span data-stu-id="9e092-126">Continue</span></span>
- <span data-ttu-id="9e092-127">理會</span><span class="sxs-lookup"><span data-stu-id="9e092-127">Ignore</span></span>
- <span data-ttu-id="9e092-128">看</span><span class="sxs-lookup"><span data-stu-id="9e092-128">Inquire</span></span>
- <span data-ttu-id="9e092-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="9e092-129">SilentlyContinue</span></span>
- <span data-ttu-id="9e092-130">停止</span><span class="sxs-lookup"><span data-stu-id="9e092-130">Stop</span></span>
- <span data-ttu-id="9e092-131">封存</span><span class="sxs-lookup"><span data-stu-id="9e092-131">Suspend</span></span>

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

### <span data-ttu-id="9e092-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="9e092-132">-InformationVariable</span></span>
<span data-ttu-id="9e092-133">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="9e092-133">Specifies an information variable.</span></span>

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

### <span data-ttu-id="9e092-134">-StoreName</span><span class="sxs-lookup"><span data-stu-id="9e092-134">-StoreName</span></span>
<span data-ttu-id="9e092-135">指定要放入憑證的憑證存放區。</span><span class="sxs-lookup"><span data-stu-id="9e092-135">Specifies the certificate store in which to put the certificate.</span></span>
<span data-ttu-id="9e092-136">有效值為：</span><span class="sxs-lookup"><span data-stu-id="9e092-136">Valid values are:</span></span> 

- <span data-ttu-id="9e092-137">AddressBook</span><span class="sxs-lookup"><span data-stu-id="9e092-137">AddressBook</span></span>
- <span data-ttu-id="9e092-138">AuthRoot</span><span class="sxs-lookup"><span data-stu-id="9e092-138">AuthRoot</span></span>
- <span data-ttu-id="9e092-139">CertificateAuthority</span><span class="sxs-lookup"><span data-stu-id="9e092-139">CertificateAuthority</span></span>
- <span data-ttu-id="9e092-140">許可證</span><span class="sxs-lookup"><span data-stu-id="9e092-140">Disallowed</span></span>
- <span data-ttu-id="9e092-141">我的帳戶</span><span class="sxs-lookup"><span data-stu-id="9e092-141">My</span></span>
- <span data-ttu-id="9e092-142">根</span><span class="sxs-lookup"><span data-stu-id="9e092-142">Root</span></span>
- <span data-ttu-id="9e092-143">TrustedPeople</span><span class="sxs-lookup"><span data-stu-id="9e092-143">TrustedPeople</span></span>
- <span data-ttu-id="9e092-144">TrustedPublisher</span><span class="sxs-lookup"><span data-stu-id="9e092-144">TrustedPublisher</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e092-145">-指紋</span><span class="sxs-lookup"><span data-stu-id="9e092-145">-Thumbprint</span></span>
<span data-ttu-id="9e092-146">指定憑證的指紋。</span><span class="sxs-lookup"><span data-stu-id="9e092-146">Specifies the thumbprint of the certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e092-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e092-147">CommonParameters</span></span>
<span data-ttu-id="9e092-148">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9e092-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e092-149">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9e092-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e092-150">輸入</span><span class="sxs-lookup"><span data-stu-id="9e092-150">INPUTS</span></span>

## <span data-ttu-id="9e092-151">輸出</span><span class="sxs-lookup"><span data-stu-id="9e092-151">OUTPUTS</span></span>

## <span data-ttu-id="9e092-152">筆記</span><span class="sxs-lookup"><span data-stu-id="9e092-152">NOTES</span></span>

## <span data-ttu-id="9e092-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="9e092-153">RELATED LINKS</span></span>

[<span data-ttu-id="9e092-154">附加 AzureCertificate</span><span class="sxs-lookup"><span data-stu-id="9e092-154">Add-AzureCertificate</span></span>](./Add-AzureCertificate.md)

[<span data-ttu-id="9e092-155">附加 AzureProvisioningConfig</span><span class="sxs-lookup"><span data-stu-id="9e092-155">Add-AzureProvisioningConfig</span></span>](./Add-AzureProvisioningConfig.md)

[<span data-ttu-id="9e092-156">AzureCertificate</span><span class="sxs-lookup"><span data-stu-id="9e092-156">Get-AzureCertificate</span></span>](./Get-AzureCertificate.md)

[<span data-ttu-id="9e092-157">AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="9e092-157">Get-AzureVMImage</span></span>](./Get-AzureVMImage.md)

[<span data-ttu-id="9e092-158">新-AzureQuickVM</span><span class="sxs-lookup"><span data-stu-id="9e092-158">New-AzureQuickVM</span></span>](./New-AzureQuickVM.md)

[<span data-ttu-id="9e092-159">Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="9e092-159">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="9e092-160">移除-AzureCertificate</span><span class="sxs-lookup"><span data-stu-id="9e092-160">Remove-AzureCertificate</span></span>](./Remove-AzureCertificate.md)


