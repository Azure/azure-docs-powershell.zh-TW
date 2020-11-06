---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 5CBEDFF8-C441-44CC-B011-5F5AAFA2E5C6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementCertificate.md
ms.openlocfilehash: f97f6c59bc1888f511d84ed49e6d1d49a5d7f57f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447520"
---
# <span data-ttu-id="12626-101">New-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="12626-101">New-AzureRmApiManagementCertificate</span></span>

## <span data-ttu-id="12626-102">摘要</span><span class="sxs-lookup"><span data-stu-id="12626-102">SYNOPSIS</span></span>
<span data-ttu-id="12626-103">建立 API 管理憑證，以便在使用後端進行驗證時使用。</span><span class="sxs-lookup"><span data-stu-id="12626-103">Creates an API Management certificate to be used during Authentication with Backend.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="12626-104">句法</span><span class="sxs-lookup"><span data-stu-id="12626-104">SYNTAX</span></span>

### <span data-ttu-id="12626-105">LoadFromFile (預設) </span><span class="sxs-lookup"><span data-stu-id="12626-105">LoadFromFile (Default)</span></span>
```
New-AzureRmApiManagementCertificate -Context <PsApiManagementContext> [-CertificateId <String>]
 -PfxFilePath <String> -PfxPassword <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="12626-106">未經</span><span class="sxs-lookup"><span data-stu-id="12626-106">Raw</span></span>
```
New-AzureRmApiManagementCertificate -Context <PsApiManagementContext> [-CertificateId <String>]
 -PfxBytes <Byte[]> -PfxPassword <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="12626-107">說明</span><span class="sxs-lookup"><span data-stu-id="12626-107">DESCRIPTION</span></span>
<span data-ttu-id="12626-108">**新的-AzureRmApiManagementCertificate** Cmdlet 會建立 Azure API 管理憑證。</span><span class="sxs-lookup"><span data-stu-id="12626-108">The **New-AzureRmApiManagementCertificate** cmdlet creates an Azure API Management certificate.</span></span>

## <span data-ttu-id="12626-109">示例</span><span class="sxs-lookup"><span data-stu-id="12626-109">EXAMPLES</span></span>

### <span data-ttu-id="12626-110">範例1：建立並上傳憑證</span><span class="sxs-lookup"><span data-stu-id="12626-110">Example 1: Create and upload a certificate</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementCertificate -Context $ApiMgmtContext -PfxFilePath "C:\contoso\certificates\apimanagement.pfx" -PfxPassword "1111"
```

<span data-ttu-id="12626-111">這個命令會將憑證上傳到 Api 管理。</span><span class="sxs-lookup"><span data-stu-id="12626-111">This command uploads a certificate to Api Management.</span></span> <span data-ttu-id="12626-112">此憑證可以用來進行相互驗證，並使用原則進行。</span><span class="sxs-lookup"><span data-stu-id="12626-112">This certificate can be used for mutual authentication with backend using policies.</span></span>

## <span data-ttu-id="12626-113">參數</span><span class="sxs-lookup"><span data-stu-id="12626-113">PARAMETERS</span></span>

### <span data-ttu-id="12626-114">-CertificateId</span><span class="sxs-lookup"><span data-stu-id="12626-114">-CertificateId</span></span>
<span data-ttu-id="12626-115">指定要建立的憑證識別碼。</span><span class="sxs-lookup"><span data-stu-id="12626-115">Specifies the ID of the certificate to create.</span></span>
<span data-ttu-id="12626-116">如果您沒有指定此參數，系統會為您產生一個 ID。</span><span class="sxs-lookup"><span data-stu-id="12626-116">If you do not specify this parameter, an ID is generated for you.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12626-117">-內容</span><span class="sxs-lookup"><span data-stu-id="12626-117">-Context</span></span>
<span data-ttu-id="12626-118">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="12626-118">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12626-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12626-119">-DefaultProfile</span></span>
<span data-ttu-id="12626-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="12626-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="12626-121">-PfxBytes</span><span class="sxs-lookup"><span data-stu-id="12626-121">-PfxBytes</span></span>
<span data-ttu-id="12626-122">以 .pfx 格式指定憑證檔的位元組陣列。</span><span class="sxs-lookup"><span data-stu-id="12626-122">Specifies an array of bytes of the certificate file in .pfx format.</span></span>
<span data-ttu-id="12626-123">如果您沒有指定 *PfxFilePath* 參數，則需要此參數。</span><span class="sxs-lookup"><span data-stu-id="12626-123">This parameter is required if you do not specify the *PfxFilePath* parameter.</span></span>

```yaml
Type: System.Byte[]
Parameter Sets: Raw
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12626-124">-PfxFilePath</span><span class="sxs-lookup"><span data-stu-id="12626-124">-PfxFilePath</span></span>
<span data-ttu-id="12626-125">指定要建立和上傳的憑證檔案的路徑（.pfx 格式）。</span><span class="sxs-lookup"><span data-stu-id="12626-125">Specifies the path to the certificate file in .pfx format to create and upload.</span></span>
<span data-ttu-id="12626-126">如果您沒有指定 *PfxBytes* 參數，則需要此參數。</span><span class="sxs-lookup"><span data-stu-id="12626-126">This parameter is required if you do not specify the *PfxBytes* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: LoadFromFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12626-127">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="12626-127">-PfxPassword</span></span>
<span data-ttu-id="12626-128">指定憑證的密碼。</span><span class="sxs-lookup"><span data-stu-id="12626-128">Specifies the password for the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12626-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12626-129">CommonParameters</span></span>
<span data-ttu-id="12626-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="12626-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12626-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="12626-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12626-132">輸入</span><span class="sxs-lookup"><span data-stu-id="12626-132">INPUTS</span></span>

### <span data-ttu-id="12626-133">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="12626-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="12626-134">System.object</span><span class="sxs-lookup"><span data-stu-id="12626-134">System.String</span></span>

### <span data-ttu-id="12626-135">System.object []</span><span class="sxs-lookup"><span data-stu-id="12626-135">System.Byte[]</span></span>

## <span data-ttu-id="12626-136">輸出</span><span class="sxs-lookup"><span data-stu-id="12626-136">OUTPUTS</span></span>

### <span data-ttu-id="12626-137">ServiceManagement. PsApiManagementCertificate （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="12626-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span></span>

## <span data-ttu-id="12626-138">筆記</span><span class="sxs-lookup"><span data-stu-id="12626-138">NOTES</span></span>

## <span data-ttu-id="12626-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="12626-139">RELATED LINKS</span></span>

[<span data-ttu-id="12626-140">AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="12626-140">Get-AzureRmApiManagementCertificate</span></span>](./Get-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="12626-141">移除-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="12626-141">Remove-AzureRmApiManagementCertificate</span></span>](./Remove-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="12626-142">Set-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="12626-142">Set-AzureRmApiManagementCertificate</span></span>](./Set-AzureRmApiManagementCertificate.md)


