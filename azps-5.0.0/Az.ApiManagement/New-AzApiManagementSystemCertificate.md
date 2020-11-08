---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementsystemcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSystemCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSystemCertificate.md
ms.openlocfilehash: 657a1b729bfa5de8b62c58ed590b5cbf2cf7dca8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94139316"
---
# <span data-ttu-id="8374e-101">New-AzApiManagementSystemCertificate</span><span class="sxs-lookup"><span data-stu-id="8374e-101">New-AzApiManagementSystemCertificate</span></span>

## <span data-ttu-id="8374e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8374e-102">SYNOPSIS</span></span>
<span data-ttu-id="8374e-103">建立的實例 `PsApiManagementSystemCertificate` 。</span><span class="sxs-lookup"><span data-stu-id="8374e-103">Creates an instance of `PsApiManagementSystemCertificate`.</span></span> <span data-ttu-id="8374e-104">證書可以由私人 CA 發行，並將在 API 管理服務上安裝到 `CertificateAuthority` 或 `Root` 儲存。</span><span class="sxs-lookup"><span data-stu-id="8374e-104">The certificate can be issued by private CA's and will be installed on the API Management service into `CertificateAuthority` or `Root` store.</span></span>

## <span data-ttu-id="8374e-105">句法</span><span class="sxs-lookup"><span data-stu-id="8374e-105">SYNTAX</span></span>

```
New-AzApiManagementSystemCertificate -StoreName <String> -PfxPath <String> [-PfxPassword <SecureString>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8374e-106">說明</span><span class="sxs-lookup"><span data-stu-id="8374e-106">DESCRIPTION</span></span>
<span data-ttu-id="8374e-107">**新的 AzApiManagementSystemCertificate** Cmdlet 是一個協助程式命令，可建立 **PsApiManagementSystemCertificate** 的實例。</span><span class="sxs-lookup"><span data-stu-id="8374e-107">The **New-AzApiManagementSystemCertificate** cmdlet is a helper command that creates an instance of **PsApiManagementSystemCertificate**.</span></span>
<span data-ttu-id="8374e-108">此命令與 New-AzApiManagement 和 Set-AzApiManagement Cmdlet 搭配使用。</span><span class="sxs-lookup"><span data-stu-id="8374e-108">This command is used with the New-AzApiManagement and Set-AzApiManagement cmdlet.</span></span>

## <span data-ttu-id="8374e-109">示例</span><span class="sxs-lookup"><span data-stu-id="8374e-109">EXAMPLES</span></span>

### <span data-ttu-id="8374e-110">範例1：使用來自檔案的 Ssl 憑證來建立和初始化 PsApiManagementSystemCertificate 的實例</span><span class="sxs-lookup"><span data-stu-id="8374e-110">Example 1: Create and initialize an instance of PsApiManagementSystemCertificate using an Ssl Certificate from file</span></span>
```powershell
PS C:\>$rootCa = New-AzApiManagementSystemCertificate -StoreName "Root" -PfxPath "C:\contoso\certificates\privateCa.cer"
PS C:\>$systemCert = @($rootCa)
PS C:\>New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -SystemCertificateConfiguration $systemCert
```

<span data-ttu-id="8374e-111">這個命令會透過根 CA 憑證來建立和初始化 **PsApiManagementSystemCertificate** 的實例。</span><span class="sxs-lookup"><span data-stu-id="8374e-111">This command creates and initializes an instance of **PsApiManagementSystemCertificate** with a root CA certificate.</span></span> <span data-ttu-id="8374e-112">接著，它會建立和 API 管理服務，將 CA 憑證安裝到根存放區。</span><span class="sxs-lookup"><span data-stu-id="8374e-112">It then creates and API Management service which installs the CA cert to the Root store.</span></span>

## <span data-ttu-id="8374e-113">參數</span><span class="sxs-lookup"><span data-stu-id="8374e-113">PARAMETERS</span></span>

### <span data-ttu-id="8374e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8374e-114">-DefaultProfile</span></span>
<span data-ttu-id="8374e-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8374e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8374e-116">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="8374e-116">-PfxPassword</span></span>
<span data-ttu-id="8374e-117">.Pfx 憑證檔案的密碼。</span><span class="sxs-lookup"><span data-stu-id="8374e-117">Password for the .pfx certificate file.</span></span>

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

### <span data-ttu-id="8374e-118">-PfxPath</span><span class="sxs-lookup"><span data-stu-id="8374e-118">-PfxPath</span></span>
<span data-ttu-id="8374e-119">.Pfx 憑證檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="8374e-119">Path to a .pfx certificate file.</span></span>

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

### <span data-ttu-id="8374e-120">-StoreName</span><span class="sxs-lookup"><span data-stu-id="8374e-120">-StoreName</span></span>
<span data-ttu-id="8374e-121">憑證 StoreName</span><span class="sxs-lookup"><span data-stu-id="8374e-121">Certificate StoreName</span></span>

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

### <span data-ttu-id="8374e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8374e-122">CommonParameters</span></span>
<span data-ttu-id="8374e-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8374e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8374e-124">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="8374e-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8374e-125">輸入</span><span class="sxs-lookup"><span data-stu-id="8374e-125">INPUTS</span></span>

### <span data-ttu-id="8374e-126">System.object</span><span class="sxs-lookup"><span data-stu-id="8374e-126">System.String</span></span>

### <span data-ttu-id="8374e-127">SecureString</span><span class="sxs-lookup"><span data-stu-id="8374e-127">System.Security.SecureString</span></span>

## <span data-ttu-id="8374e-128">輸出</span><span class="sxs-lookup"><span data-stu-id="8374e-128">OUTPUTS</span></span>

### <span data-ttu-id="8374e-129">PsApiManagementSystemCertificate 中的 ApiManagement。</span><span class="sxs-lookup"><span data-stu-id="8374e-129">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSystemCertificate</span></span>

## <span data-ttu-id="8374e-130">筆記</span><span class="sxs-lookup"><span data-stu-id="8374e-130">NOTES</span></span>

## <span data-ttu-id="8374e-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="8374e-131">RELATED LINKS</span></span>

[<span data-ttu-id="8374e-132">新-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="8374e-132">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="8374e-133">Set-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="8374e-133">Set-AzApiManagement</span></span>](./Set-AzApiManagement.md)