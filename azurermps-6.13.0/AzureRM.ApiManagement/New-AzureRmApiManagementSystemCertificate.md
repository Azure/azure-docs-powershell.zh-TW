---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementsystemcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementSystemCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementSystemCertificate.md
ms.openlocfilehash: fa64e9bade3a6cd8ec4edc8e04956c97306328ea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93444151"
---
# <span data-ttu-id="bba0c-101">New-AzureRmApiManagementSystemCertificate</span><span class="sxs-lookup"><span data-stu-id="bba0c-101">New-AzureRmApiManagementSystemCertificate</span></span>

## <span data-ttu-id="bba0c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bba0c-102">SYNOPSIS</span></span>
<span data-ttu-id="bba0c-103">建立的實例 `PsApiManagementSystemCertificate` 。</span><span class="sxs-lookup"><span data-stu-id="bba0c-103">Creates an instance of `PsApiManagementSystemCertificate`.</span></span> <span data-ttu-id="bba0c-104">證書可以由私人 CA 發行，並將在 API 管理服務上安裝到 `CertificateAuthority` 或 `Root` 儲存。</span><span class="sxs-lookup"><span data-stu-id="bba0c-104">The certificate can be issued by private CA's and will be installed on the API Management service into `CertificateAuthority` or `Root` store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bba0c-105">句法</span><span class="sxs-lookup"><span data-stu-id="bba0c-105">SYNTAX</span></span>

```
New-AzureRmApiManagementSystemCertificate -StoreName <String> -PfxPath <String> [-PfxPassword <SecureString>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bba0c-106">說明</span><span class="sxs-lookup"><span data-stu-id="bba0c-106">DESCRIPTION</span></span>
<span data-ttu-id="bba0c-107">**新的 AzureRmApiManagementSystemCertificate** Cmdlet 是一個協助程式命令，可建立 **PsApiManagementSystemCertificate** 的實例。</span><span class="sxs-lookup"><span data-stu-id="bba0c-107">The **New-AzureRmApiManagementSystemCertificate** cmdlet is a helper command that creates an instance of **PsApiManagementSystemCertificate**.</span></span>
<span data-ttu-id="bba0c-108">此命令與 New-AzureRmApiManagement 和 Set-AzureRmApiManagement Cmdlet 搭配使用。</span><span class="sxs-lookup"><span data-stu-id="bba0c-108">This command is used with the New-AzureRmApiManagement and Set-AzureRmApiManagement cmdlet.</span></span>

## <span data-ttu-id="bba0c-109">示例</span><span class="sxs-lookup"><span data-stu-id="bba0c-109">EXAMPLES</span></span>

### <span data-ttu-id="bba0c-110">範例1：使用來自檔案的 Ssl 憑證來建立和初始化 PsApiManagementSystemCertificate 的實例</span><span class="sxs-lookup"><span data-stu-id="bba0c-110">Example 1: Create and initialize an instance of PsApiManagementSystemCertificate using an Ssl Certificate from file</span></span>
```powershell
PS C:\>$rootCa = New-AzureRmApiManagementSystemCertificate -StoreName "Root" -PfxPath "C:\contoso\certificates\privateCa.cer"
PS C:\>$systemCert = @($rootCa)
PS C:\>New-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -SystemCertificateConfiguration $systemCert
```

<span data-ttu-id="bba0c-111">這個命令會透過根 CA 憑證來建立和初始化 **PsApiManagementSystemCertificate** 的實例。</span><span class="sxs-lookup"><span data-stu-id="bba0c-111">This command creates and initializes an instance of **PsApiManagementSystemCertificate** with a root CA certificate.</span></span> <span data-ttu-id="bba0c-112">接著，它會建立和 API 管理服務，將 CA 憑證安裝到根存放區。</span><span class="sxs-lookup"><span data-stu-id="bba0c-112">It then creates and API Management service which installs the CA cert to the Root store.</span></span>

## <span data-ttu-id="bba0c-113">參數</span><span class="sxs-lookup"><span data-stu-id="bba0c-113">PARAMETERS</span></span>

### <span data-ttu-id="bba0c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bba0c-114">-DefaultProfile</span></span>
<span data-ttu-id="bba0c-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="bba0c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bba0c-116">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="bba0c-116">-PfxPassword</span></span>
<span data-ttu-id="bba0c-117">.Pfx 憑證檔案的密碼。</span><span class="sxs-lookup"><span data-stu-id="bba0c-117">Password for the .pfx certificate file.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bba0c-118">-PfxPath</span><span class="sxs-lookup"><span data-stu-id="bba0c-118">-PfxPath</span></span>
<span data-ttu-id="bba0c-119">.Pfx 憑證檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="bba0c-119">Path to a .pfx certificate file.</span></span>

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

### <span data-ttu-id="bba0c-120">-StoreName</span><span class="sxs-lookup"><span data-stu-id="bba0c-120">-StoreName</span></span>
<span data-ttu-id="bba0c-121">憑證 StoreName</span><span class="sxs-lookup"><span data-stu-id="bba0c-121">Certificate StoreName</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: CertificateAuthority, Root

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bba0c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bba0c-122">CommonParameters</span></span>
<span data-ttu-id="bba0c-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bba0c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bba0c-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="bba0c-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bba0c-125">輸入</span><span class="sxs-lookup"><span data-stu-id="bba0c-125">INPUTS</span></span>

### <span data-ttu-id="bba0c-126">System.object</span><span class="sxs-lookup"><span data-stu-id="bba0c-126">System.String</span></span>

### <span data-ttu-id="bba0c-127">SecureString</span><span class="sxs-lookup"><span data-stu-id="bba0c-127">System.Security.SecureString</span></span>

## <span data-ttu-id="bba0c-128">輸出</span><span class="sxs-lookup"><span data-stu-id="bba0c-128">OUTPUTS</span></span>

### <span data-ttu-id="bba0c-129">PsApiManagementSystemCertificate 中的 ApiManagement。</span><span class="sxs-lookup"><span data-stu-id="bba0c-129">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSystemCertificate</span></span>

## <span data-ttu-id="bba0c-130">筆記</span><span class="sxs-lookup"><span data-stu-id="bba0c-130">NOTES</span></span>

## <span data-ttu-id="bba0c-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="bba0c-131">RELATED LINKS</span></span>

[<span data-ttu-id="bba0c-132">新-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="bba0c-132">New-AzureRmApiManagement</span></span>](./New-AzureRmApiManagement.md)

[<span data-ttu-id="bba0c-133">Set-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="bba0c-133">Set-AzureRmApiManagement</span></span>](./Set-AzureRmApiManagement.md)
