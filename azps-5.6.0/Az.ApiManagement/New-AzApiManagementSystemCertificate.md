---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/new-azapimanagementsystemcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSystemCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSystemCertificate.md
ms.openlocfilehash: cc3cc5d0e7ae617fc745c2f119f7da9df88417a3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903721"
---
# <span data-ttu-id="51b63-101">New-AzApiManagementSystemCertificate</span><span class="sxs-lookup"><span data-stu-id="51b63-101">New-AzApiManagementSystemCertificate</span></span>

## <span data-ttu-id="51b63-102">簡介</span><span class="sxs-lookup"><span data-stu-id="51b63-102">SYNOPSIS</span></span>
<span data-ttu-id="51b63-103">會建立一個 `PsApiManagementSystemCertificate` .</span><span class="sxs-lookup"><span data-stu-id="51b63-103">Creates an instance of `PsApiManagementSystemCertificate`.</span></span> <span data-ttu-id="51b63-104">憑證可以由私人 CA 發行，而且會安裝在 API 管理服務中或 `CertificateAuthority` 存放 `Root` 區。</span><span class="sxs-lookup"><span data-stu-id="51b63-104">The certificate can be issued by private CA's and will be installed on the API Management service into `CertificateAuthority` or `Root` store.</span></span>

## <span data-ttu-id="51b63-105">語法</span><span class="sxs-lookup"><span data-stu-id="51b63-105">SYNTAX</span></span>

```
New-AzApiManagementSystemCertificate -StoreName <String> -PfxPath <String> [-PfxPassword <SecureString>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="51b63-106">描述</span><span class="sxs-lookup"><span data-stu-id="51b63-106">DESCRIPTION</span></span>
<span data-ttu-id="51b63-107">**New-AzApiManagementSystemCertificate Cmdlet** 是建立 **PsApiManagementSystemCertificate** 實例的協助程式命令。</span><span class="sxs-lookup"><span data-stu-id="51b63-107">The **New-AzApiManagementSystemCertificate** cmdlet is a helper command that creates an instance of **PsApiManagementSystemCertificate**.</span></span>
<span data-ttu-id="51b63-108">此命令會與 New-AzApiManagement 和 Set-AzApiManagement 一起使用。</span><span class="sxs-lookup"><span data-stu-id="51b63-108">This command is used with the New-AzApiManagement and Set-AzApiManagement cmdlet.</span></span>

## <span data-ttu-id="51b63-109">例子</span><span class="sxs-lookup"><span data-stu-id="51b63-109">EXAMPLES</span></span>

### <span data-ttu-id="51b63-110">範例 1：使用檔案的 Ssl 憑證建立 PsApiManagementSystemCertificate 實例並初始化</span><span class="sxs-lookup"><span data-stu-id="51b63-110">Example 1: Create and initialize an instance of PsApiManagementSystemCertificate using an Ssl Certificate from file</span></span>
```powershell
PS C:\>$rootCa = New-AzApiManagementSystemCertificate -StoreName "Root" -PfxPath "C:\contoso\certificates\privateCa.cer"
PS C:\>$systemCert = @($rootCa)
PS C:\>New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -SystemCertificateConfiguration $systemCert
```

<span data-ttu-id="51b63-111">此命令會建立並初始化具有根 CA 憑證 **的 PsApiManagementSystemCertificate** 實例。</span><span class="sxs-lookup"><span data-stu-id="51b63-111">This command creates and initializes an instance of **PsApiManagementSystemCertificate** with a root CA certificate.</span></span> <span data-ttu-id="51b63-112">接著，它會建立 API 管理服務，將 CA 認證安裝到根存放區。</span><span class="sxs-lookup"><span data-stu-id="51b63-112">It then creates and API Management service which installs the CA cert to the Root store.</span></span>

## <span data-ttu-id="51b63-113">參數</span><span class="sxs-lookup"><span data-stu-id="51b63-113">PARAMETERS</span></span>

### <span data-ttu-id="51b63-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51b63-114">-DefaultProfile</span></span>
<span data-ttu-id="51b63-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="51b63-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="51b63-116">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="51b63-116">-PfxPassword</span></span>
<span data-ttu-id="51b63-117">.pfx 憑證檔案的密碼。</span><span class="sxs-lookup"><span data-stu-id="51b63-117">Password for the .pfx certificate file.</span></span>

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

### <span data-ttu-id="51b63-118">-PfxPath</span><span class="sxs-lookup"><span data-stu-id="51b63-118">-PfxPath</span></span>
<span data-ttu-id="51b63-119">.pfx 憑證檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="51b63-119">Path to a .pfx certificate file.</span></span>

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

### <span data-ttu-id="51b63-120">-StoreName</span><span class="sxs-lookup"><span data-stu-id="51b63-120">-StoreName</span></span>
<span data-ttu-id="51b63-121">Certificate StoreName</span><span class="sxs-lookup"><span data-stu-id="51b63-121">Certificate StoreName</span></span>

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

### <span data-ttu-id="51b63-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51b63-122">CommonParameters</span></span>
<span data-ttu-id="51b63-123">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="51b63-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51b63-124">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="51b63-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51b63-125">輸入</span><span class="sxs-lookup"><span data-stu-id="51b63-125">INPUTS</span></span>

### <span data-ttu-id="51b63-126">System.String</span><span class="sxs-lookup"><span data-stu-id="51b63-126">System.String</span></span>

### <span data-ttu-id="51b63-127">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="51b63-127">System.Security.SecureString</span></span>

## <span data-ttu-id="51b63-128">輸出</span><span class="sxs-lookup"><span data-stu-id="51b63-128">OUTPUTS</span></span>

### <span data-ttu-id="51b63-129">Microsoft.Azure.Commands.ApiManagement.models.PsApiManagementSystemCertificate</span><span class="sxs-lookup"><span data-stu-id="51b63-129">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSystemCertificate</span></span>

## <span data-ttu-id="51b63-130">筆記</span><span class="sxs-lookup"><span data-stu-id="51b63-130">NOTES</span></span>

## <span data-ttu-id="51b63-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="51b63-131">RELATED LINKS</span></span>

[<span data-ttu-id="51b63-132">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="51b63-132">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="51b63-133">Set-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="51b63-133">Set-AzApiManagement</span></span>](./Set-AzApiManagement.md)