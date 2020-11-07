---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 9A6D5C40-2532-4FD1-A74F-16725CAD8EDD
online version: ''
schema: 2.0.0
ms.openlocfilehash: 29d049dbdce93102411a875cfaef8e5fb9c719b6
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967841"
---
# <span data-ttu-id="03c5c-101">Add-AzureCertificate</span><span class="sxs-lookup"><span data-stu-id="03c5c-101">Add-AzureCertificate</span></span>

## <span data-ttu-id="03c5c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="03c5c-102">SYNOPSIS</span></span>
<span data-ttu-id="03c5c-103">將憑證上傳到 Azure 雲端服務。</span><span class="sxs-lookup"><span data-stu-id="03c5c-103">Uploads a certificate to an Azure cloud service.</span></span>

## <span data-ttu-id="03c5c-104">句法</span><span class="sxs-lookup"><span data-stu-id="03c5c-104">SYNTAX</span></span>

```
Add-AzureCertificate [-ServiceName] <String> [-CertToDeploy] <Object> [-Password <String>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="03c5c-105">說明</span><span class="sxs-lookup"><span data-stu-id="03c5c-105">DESCRIPTION</span></span>
<span data-ttu-id="03c5c-106">**AzureCertificate** Cmdlet 會上傳 Azure 服務的憑證。</span><span class="sxs-lookup"><span data-stu-id="03c5c-106">The **Add-AzureCertificate** cmdlet uploads a certificate for an Azure service.</span></span>

## <span data-ttu-id="03c5c-107">示例</span><span class="sxs-lookup"><span data-stu-id="03c5c-107">EXAMPLES</span></span>

### <span data-ttu-id="03c5c-108">範例1：上傳憑證和密碼</span><span class="sxs-lookup"><span data-stu-id="03c5c-108">Example 1: Upload a certificate and password</span></span>
```
PS C:\> Add-AzureCertificate -ServiceName "ContosoService" -CertToDeploy ContosoCertificate.pfx -Password "password"
```

<span data-ttu-id="03c5c-109">這個命令會將證書檔案 ContosoCertificate 上傳到雲端服務。</span><span class="sxs-lookup"><span data-stu-id="03c5c-109">This command uploads the certificate file ContosoCertificate.pfx to a cloud service.</span></span>
<span data-ttu-id="03c5c-110">此命令會指定憑證的密碼。</span><span class="sxs-lookup"><span data-stu-id="03c5c-110">The command specifies the password for the certificate.</span></span>

### <span data-ttu-id="03c5c-111">範例2：上傳憑證檔</span><span class="sxs-lookup"><span data-stu-id="03c5c-111">Example 2: Upload a certificate file</span></span>
```
PS C:\> Add-AzureCertificate -serviceName "MyService" -CertToDeploy ContosoCertificate.cer
```

<span data-ttu-id="03c5c-112">這個命令會將證書檔案 ContosoCertificate 上傳到雲端服務。</span><span class="sxs-lookup"><span data-stu-id="03c5c-112">This command uploads the certificate file ContosoCertificate.cer to a cloud service.</span></span>
<span data-ttu-id="03c5c-113">此命令會指定憑證的密碼。</span><span class="sxs-lookup"><span data-stu-id="03c5c-113">The command specifies the password for the certificate.</span></span>

### <span data-ttu-id="03c5c-114">範例3：上傳憑證物件</span><span class="sxs-lookup"><span data-stu-id="03c5c-114">Example 3: Upload a certificate object</span></span>
```
PS C:\> $Certificate = Get-Item cert:\PATTIFULLER\MY\1D6E34B526723E06C235BE8E5457784BF12C9F39
PS C:\> Add-AzureCertificate -ServiceName "ContosoService" -CertToDeploy $Certificate
```

<span data-ttu-id="03c5c-115">第一個命令會使用 Windows PowerShell 核心 **取得專案** Cmdlet，從使用者的 [我的存儲區] 中取得憑證。</span><span class="sxs-lookup"><span data-stu-id="03c5c-115">The first command gets a certificate from the MY store of a user by using the Windows PowerShell core **Get-Item** cmdlet.</span></span>
<span data-ttu-id="03c5c-116">該命令會將憑證儲存在 $Certificate 變數中。</span><span class="sxs-lookup"><span data-stu-id="03c5c-116">The command stores the certificate in the $Certificate variable.</span></span>

<span data-ttu-id="03c5c-117">第二個命令會將 $certificate 中的憑證上傳到雲端服務。</span><span class="sxs-lookup"><span data-stu-id="03c5c-117">The second command uploads the certificate in $certificate to a cloud service.</span></span>

## <span data-ttu-id="03c5c-118">參數</span><span class="sxs-lookup"><span data-stu-id="03c5c-118">PARAMETERS</span></span>

### <span data-ttu-id="03c5c-119">-CertToDeploy</span><span class="sxs-lookup"><span data-stu-id="03c5c-119">-CertToDeploy</span></span>
<span data-ttu-id="03c5c-120">指定要部署的憑證。</span><span class="sxs-lookup"><span data-stu-id="03c5c-120">Specifies the certificate to deploy.</span></span>
<span data-ttu-id="03c5c-121">您可以指定憑證檔案的完整路徑，例如包含 \* .cer 或 \* 的檔案。</span><span class="sxs-lookup"><span data-stu-id="03c5c-121">You can specify the full path of a certificate file, such as a file that has a \*.cer or \*.</span></span>
<span data-ttu-id="03c5c-122">pfx 檔案名副檔名或 x.509 憑證物件。</span><span class="sxs-lookup"><span data-stu-id="03c5c-122">pfx file name extension, or an X.509 Certificate object.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03c5c-123">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="03c5c-123">-InformationAction</span></span>
<span data-ttu-id="03c5c-124">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="03c5c-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="03c5c-125">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="03c5c-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="03c5c-126">持續</span><span class="sxs-lookup"><span data-stu-id="03c5c-126">Continue</span></span>
- <span data-ttu-id="03c5c-127">理會</span><span class="sxs-lookup"><span data-stu-id="03c5c-127">Ignore</span></span>
- <span data-ttu-id="03c5c-128">看</span><span class="sxs-lookup"><span data-stu-id="03c5c-128">Inquire</span></span>
- <span data-ttu-id="03c5c-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="03c5c-129">SilentlyContinue</span></span>
- <span data-ttu-id="03c5c-130">停止</span><span class="sxs-lookup"><span data-stu-id="03c5c-130">Stop</span></span>
- <span data-ttu-id="03c5c-131">封存</span><span class="sxs-lookup"><span data-stu-id="03c5c-131">Suspend</span></span>

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

### <span data-ttu-id="03c5c-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="03c5c-132">-InformationVariable</span></span>
<span data-ttu-id="03c5c-133">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="03c5c-133">Specifies an information variable.</span></span>

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

### <span data-ttu-id="03c5c-134">-Password</span><span class="sxs-lookup"><span data-stu-id="03c5c-134">-Password</span></span>
<span data-ttu-id="03c5c-135">指定憑證密碼。</span><span class="sxs-lookup"><span data-stu-id="03c5c-135">Specifies the certificate password.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03c5c-136">-設定檔</span><span class="sxs-lookup"><span data-stu-id="03c5c-136">-Profile</span></span>
<span data-ttu-id="03c5c-137">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="03c5c-137">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="03c5c-138">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="03c5c-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="03c5c-139">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="03c5c-139">-ServiceName</span></span>
<span data-ttu-id="03c5c-140">指定此 Cmdlet 新增憑證的 Azure 服務名稱。</span><span class="sxs-lookup"><span data-stu-id="03c5c-140">Specifies the name of the Azure service to which this cmdlet adds a certificate.</span></span>

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

### <span data-ttu-id="03c5c-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03c5c-141">CommonParameters</span></span>
<span data-ttu-id="03c5c-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="03c5c-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03c5c-143">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="03c5c-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03c5c-144">輸入</span><span class="sxs-lookup"><span data-stu-id="03c5c-144">INPUTS</span></span>

## <span data-ttu-id="03c5c-145">輸出</span><span class="sxs-lookup"><span data-stu-id="03c5c-145">OUTPUTS</span></span>

### <span data-ttu-id="03c5c-146">ManagementOperationCoNtext</span><span class="sxs-lookup"><span data-stu-id="03c5c-146">ManagementOperationContext</span></span>

## <span data-ttu-id="03c5c-147">筆記</span><span class="sxs-lookup"><span data-stu-id="03c5c-147">NOTES</span></span>

## <span data-ttu-id="03c5c-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="03c5c-148">RELATED LINKS</span></span>

[<span data-ttu-id="03c5c-149">AzureCertificate</span><span class="sxs-lookup"><span data-stu-id="03c5c-149">Get-AzureCertificate</span></span>](./Get-AzureCertificate.md)

[<span data-ttu-id="03c5c-150">新-AzureCertificateSetting</span><span class="sxs-lookup"><span data-stu-id="03c5c-150">New-AzureCertificateSetting</span></span>](./New-AzureCertificateSetting.md)

[<span data-ttu-id="03c5c-151">移除-AzureCertificate</span><span class="sxs-lookup"><span data-stu-id="03c5c-151">Remove-AzureCertificate</span></span>](./Remove-AzureCertificate.md)


