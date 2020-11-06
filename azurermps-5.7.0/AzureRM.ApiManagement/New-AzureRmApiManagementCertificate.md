---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 5CBEDFF8-C441-44CC-B011-5F5AAFA2E5C6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementCertificate.md
ms.openlocfilehash: f7ddfb327931fc7ebb9eac76cdd6818521332483
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448791"
---
# <span data-ttu-id="1bd72-101">New-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="1bd72-101">New-AzureRmApiManagementCertificate</span></span>

## <span data-ttu-id="1bd72-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1bd72-102">SYNOPSIS</span></span>
<span data-ttu-id="1bd72-103">建立 API 管理憑證，以便在使用後端進行驗證時使用。</span><span class="sxs-lookup"><span data-stu-id="1bd72-103">Creates an API Management certificate to be used during Authentication with Backend.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1bd72-104">句法</span><span class="sxs-lookup"><span data-stu-id="1bd72-104">SYNTAX</span></span>

### <span data-ttu-id="1bd72-105">LoadFromFile (預設) </span><span class="sxs-lookup"><span data-stu-id="1bd72-105">LoadFromFile (Default)</span></span>
```
New-AzureRmApiManagementCertificate -Context <PsApiManagementContext> [-CertificateId <String>]
 -PfxFilePath <String> -PfxPassword <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1bd72-106">未經</span><span class="sxs-lookup"><span data-stu-id="1bd72-106">Raw</span></span>
```
New-AzureRmApiManagementCertificate -Context <PsApiManagementContext> [-CertificateId <String>]
 -PfxBytes <Byte[]> -PfxPassword <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1bd72-107">說明</span><span class="sxs-lookup"><span data-stu-id="1bd72-107">DESCRIPTION</span></span>
<span data-ttu-id="1bd72-108">**新的-AzureRmApiManagementCertificate** Cmdlet 會建立 Azure API 管理憑證。</span><span class="sxs-lookup"><span data-stu-id="1bd72-108">The **New-AzureRmApiManagementCertificate** cmdlet creates an Azure API Management certificate.</span></span>

## <span data-ttu-id="1bd72-109">示例</span><span class="sxs-lookup"><span data-stu-id="1bd72-109">EXAMPLES</span></span>

### <span data-ttu-id="1bd72-110">範例1：建立並上傳憑證</span><span class="sxs-lookup"><span data-stu-id="1bd72-110">Example 1: Create and upload a certificate</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementCertificate -Context $ApiMgmtContext -PfxFilePath "C:\contoso\certificates\apimanagement.pfx" -PfxPassword "1111"
```

<span data-ttu-id="1bd72-111">這個命令會將憑證上傳到 Api 管理。</span><span class="sxs-lookup"><span data-stu-id="1bd72-111">This command uploads a certificate to Api Management.</span></span> <span data-ttu-id="1bd72-112">此憑證可以用來進行相互驗證，並使用原則進行。</span><span class="sxs-lookup"><span data-stu-id="1bd72-112">This certificate can be used for mutual authentication with backend using policies.</span></span>

## <span data-ttu-id="1bd72-113">參數</span><span class="sxs-lookup"><span data-stu-id="1bd72-113">PARAMETERS</span></span>

### <span data-ttu-id="1bd72-114">-CertificateId</span><span class="sxs-lookup"><span data-stu-id="1bd72-114">-CertificateId</span></span>
<span data-ttu-id="1bd72-115">指定要建立的憑證識別碼。</span><span class="sxs-lookup"><span data-stu-id="1bd72-115">Specifies the ID of the certificate to create.</span></span>
<span data-ttu-id="1bd72-116">如果您沒有指定此參數，系統會為您產生一個 ID。</span><span class="sxs-lookup"><span data-stu-id="1bd72-116">If you do not specify this parameter, an ID is generated for you.</span></span>

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

### <span data-ttu-id="1bd72-117">-內容</span><span class="sxs-lookup"><span data-stu-id="1bd72-117">-Context</span></span>
<span data-ttu-id="1bd72-118">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="1bd72-118">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bd72-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1bd72-119">-DefaultProfile</span></span>
<span data-ttu-id="1bd72-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1bd72-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bd72-121">-PfxBytes</span><span class="sxs-lookup"><span data-stu-id="1bd72-121">-PfxBytes</span></span>
<span data-ttu-id="1bd72-122">以 .pfx 格式指定憑證檔的位元組陣列。</span><span class="sxs-lookup"><span data-stu-id="1bd72-122">Specifies an array of bytes of the certificate file in .pfx format.</span></span>
<span data-ttu-id="1bd72-123">如果您沒有指定 *PfxFilePath* 參數，則需要此參數。</span><span class="sxs-lookup"><span data-stu-id="1bd72-123">This parameter is required if you do not specify the *PfxFilePath* parameter.</span></span>

```yaml
Type: Byte[]
Parameter Sets: Raw
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bd72-124">-PfxFilePath</span><span class="sxs-lookup"><span data-stu-id="1bd72-124">-PfxFilePath</span></span>
<span data-ttu-id="1bd72-125">指定要建立和上傳的憑證檔案的路徑（.pfx 格式）。</span><span class="sxs-lookup"><span data-stu-id="1bd72-125">Specifies the path to the certificate file in .pfx format to create and upload.</span></span>
<span data-ttu-id="1bd72-126">如果您沒有指定 *PfxBytes* 參數，則需要此參數。</span><span class="sxs-lookup"><span data-stu-id="1bd72-126">This parameter is required if you do not specify the *PfxBytes* parameter.</span></span>

```yaml
Type: String
Parameter Sets: LoadFromFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bd72-127">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="1bd72-127">-PfxPassword</span></span>
<span data-ttu-id="1bd72-128">指定憑證的密碼。</span><span class="sxs-lookup"><span data-stu-id="1bd72-128">Specifies the password for the certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bd72-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bd72-129">CommonParameters</span></span>
<span data-ttu-id="1bd72-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1bd72-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bd72-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1bd72-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bd72-132">輸入</span><span class="sxs-lookup"><span data-stu-id="1bd72-132">INPUTS</span></span>

### <span data-ttu-id="1bd72-133">所有</span><span class="sxs-lookup"><span data-stu-id="1bd72-133">None</span></span>
<span data-ttu-id="1bd72-134">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="1bd72-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1bd72-135">輸出</span><span class="sxs-lookup"><span data-stu-id="1bd72-135">OUTPUTS</span></span>

### <span data-ttu-id="1bd72-136">ServiceManagement. PsApiManagementCertificate （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="1bd72-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span></span>

## <span data-ttu-id="1bd72-137">筆記</span><span class="sxs-lookup"><span data-stu-id="1bd72-137">NOTES</span></span>

## <span data-ttu-id="1bd72-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="1bd72-138">RELATED LINKS</span></span>

[<span data-ttu-id="1bd72-139">AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="1bd72-139">Get-AzureRmApiManagementCertificate</span></span>](./Get-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="1bd72-140">移除-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="1bd72-140">Remove-AzureRmApiManagementCertificate</span></span>](./Remove-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="1bd72-141">Set-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="1bd72-141">Set-AzureRmApiManagementCertificate</span></span>](./Set-AzureRmApiManagementCertificate.md)


