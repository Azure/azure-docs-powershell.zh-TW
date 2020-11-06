---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 12FC21EB-0B4E-4275-88FB-7FF42730A6A0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementCertificate.md
ms.openlocfilehash: f7712a7938617d979dad2feabf4d2b2126e20433
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93444103"
---
# <span data-ttu-id="334f7-101">Set-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="334f7-101">Set-AzureRmApiManagementCertificate</span></span>

## <span data-ttu-id="334f7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="334f7-102">SYNOPSIS</span></span>
<span data-ttu-id="334f7-103">修改以後端驗證所設定之共同驗證的 API 管理憑證。</span><span class="sxs-lookup"><span data-stu-id="334f7-103">Modifies an API Management certificate which is configured for mutual authentication with backend.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="334f7-104">句法</span><span class="sxs-lookup"><span data-stu-id="334f7-104">SYNTAX</span></span>

### <span data-ttu-id="334f7-105">LoadFromFile (預設) </span><span class="sxs-lookup"><span data-stu-id="334f7-105">LoadFromFile (Default)</span></span>
```
Set-AzureRmApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String>
 -PfxFilePath <String> -PfxPassword <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="334f7-106">未經</span><span class="sxs-lookup"><span data-stu-id="334f7-106">Raw</span></span>
```
Set-AzureRmApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String>
 -PfxBytes <Byte[]> -PfxPassword <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="334f7-107">說明</span><span class="sxs-lookup"><span data-stu-id="334f7-107">DESCRIPTION</span></span>
<span data-ttu-id="334f7-108">**AzureRmApiManagementCertificate** Cmdlet 會修改 Azure API 管理憑證。</span><span class="sxs-lookup"><span data-stu-id="334f7-108">The **Set-AzureRmApiManagementCertificate** cmdlet modifies an Azure API Management certificate.</span></span>

## <span data-ttu-id="334f7-109">示例</span><span class="sxs-lookup"><span data-stu-id="334f7-109">EXAMPLES</span></span>

### <span data-ttu-id="334f7-110">範例1：修改憑證</span><span class="sxs-lookup"><span data-stu-id="334f7-110">Example 1: Modify a certificate</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementCertificate -Context $ApiMgmtContext -CertificateId "0123456789" -PfxFilePath "C:\contoso\certificates\apimanagementnew.pfx" -PfxPassword "2222"
```

<span data-ttu-id="334f7-111">這個命令會修改指定的 API 管理憑證。</span><span class="sxs-lookup"><span data-stu-id="334f7-111">This command modifies the specified API Management certificate.</span></span>

## <span data-ttu-id="334f7-112">參數</span><span class="sxs-lookup"><span data-stu-id="334f7-112">PARAMETERS</span></span>

### <span data-ttu-id="334f7-113">-CertificateId</span><span class="sxs-lookup"><span data-stu-id="334f7-113">-CertificateId</span></span>
<span data-ttu-id="334f7-114">指定要修改的憑證識別碼。</span><span class="sxs-lookup"><span data-stu-id="334f7-114">Specifies the ID of the certificate to modify.</span></span>

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

### <span data-ttu-id="334f7-115">-內容</span><span class="sxs-lookup"><span data-stu-id="334f7-115">-Context</span></span>
<span data-ttu-id="334f7-116">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="334f7-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="334f7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="334f7-117">-DefaultProfile</span></span>
<span data-ttu-id="334f7-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="334f7-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="334f7-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="334f7-119">-PassThru</span></span>
<span data-ttu-id="334f7-120">passthru</span><span class="sxs-lookup"><span data-stu-id="334f7-120">passthru</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="334f7-121">-PfxBytes</span><span class="sxs-lookup"><span data-stu-id="334f7-121">-PfxBytes</span></span>
<span data-ttu-id="334f7-122">以 .pfx 格式指定憑證檔的位元組陣列。</span><span class="sxs-lookup"><span data-stu-id="334f7-122">Specifies an array of bytes of the certificate file in .pfx format.</span></span>
<span data-ttu-id="334f7-123">如果您沒有指定 *PfxFilePath* 參數，則需要此參數。</span><span class="sxs-lookup"><span data-stu-id="334f7-123">This parameter is required if you do not specify the *PfxFilePath* parameter.</span></span>

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

### <span data-ttu-id="334f7-124">-PfxFilePath</span><span class="sxs-lookup"><span data-stu-id="334f7-124">-PfxFilePath</span></span>
<span data-ttu-id="334f7-125">指定要建立和上傳的憑證檔案的路徑（.pfx 格式）。</span><span class="sxs-lookup"><span data-stu-id="334f7-125">Specifies the path to the certificate file in .pfx format to create and upload.</span></span>
<span data-ttu-id="334f7-126">如果您沒有指定 *PfxBytes* 參數，則需要此參數。</span><span class="sxs-lookup"><span data-stu-id="334f7-126">This parameter is required if you do not specify the *PfxBytes* parameter.</span></span>

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

### <span data-ttu-id="334f7-127">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="334f7-127">-PfxPassword</span></span>
<span data-ttu-id="334f7-128">指定憑證的密碼。</span><span class="sxs-lookup"><span data-stu-id="334f7-128">Specifies the password for the certificate.</span></span>

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

### <span data-ttu-id="334f7-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="334f7-129">CommonParameters</span></span>
<span data-ttu-id="334f7-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="334f7-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="334f7-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="334f7-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="334f7-132">輸入</span><span class="sxs-lookup"><span data-stu-id="334f7-132">INPUTS</span></span>

### <span data-ttu-id="334f7-133">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="334f7-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="334f7-134">System.object</span><span class="sxs-lookup"><span data-stu-id="334f7-134">System.String</span></span>

### <span data-ttu-id="334f7-135">System.object []</span><span class="sxs-lookup"><span data-stu-id="334f7-135">System.Byte[]</span></span>

### <span data-ttu-id="334f7-136">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="334f7-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="334f7-137">輸出</span><span class="sxs-lookup"><span data-stu-id="334f7-137">OUTPUTS</span></span>

### <span data-ttu-id="334f7-138">ServiceManagement. PsApiManagementCertificate （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="334f7-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span></span>

## <span data-ttu-id="334f7-139">筆記</span><span class="sxs-lookup"><span data-stu-id="334f7-139">NOTES</span></span>

## <span data-ttu-id="334f7-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="334f7-140">RELATED LINKS</span></span>

[<span data-ttu-id="334f7-141">AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="334f7-141">Get-AzureRmApiManagementCertificate</span></span>](./Get-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="334f7-142">新-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="334f7-142">New-AzureRmApiManagementCertificate</span></span>](./New-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="334f7-143">移除-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="334f7-143">Remove-AzureRmApiManagementCertificate</span></span>](./Remove-AzureRmApiManagementCertificate.md)


