---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 12FC21EB-0B4E-4275-88FB-7FF42730A6A0
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/set-azapimanagementcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementCertificate.md
ms.openlocfilehash: bb60ce1fc2cb20a24d1b445cf4a3729bf26747ce
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905282"
---
# <span data-ttu-id="4eab0-101">Set-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="4eab0-101">Set-AzApiManagementCertificate</span></span>

## <span data-ttu-id="4eab0-102">簡介</span><span class="sxs-lookup"><span data-stu-id="4eab0-102">SYNOPSIS</span></span>
<span data-ttu-id="4eab0-103">修改 API 管理憑證，此憑證已針對後端的相互驗證而進行。</span><span class="sxs-lookup"><span data-stu-id="4eab0-103">Modifies an API Management certificate which is configured for mutual authentication with backend.</span></span>

## <span data-ttu-id="4eab0-104">語法</span><span class="sxs-lookup"><span data-stu-id="4eab0-104">SYNTAX</span></span>

### <span data-ttu-id="4eab0-105">LoadFromFile (預設) </span><span class="sxs-lookup"><span data-stu-id="4eab0-105">LoadFromFile (Default)</span></span>
```
Set-AzApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String> -PfxFilePath <String>
 -PfxPassword <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4eab0-106">原始</span><span class="sxs-lookup"><span data-stu-id="4eab0-106">Raw</span></span>
```
Set-AzApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String> -PfxBytes <Byte[]>
 -PfxPassword <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4eab0-107">描述</span><span class="sxs-lookup"><span data-stu-id="4eab0-107">DESCRIPTION</span></span>
<span data-ttu-id="4eab0-108">**Set-AzApiManagementCertificate** Cmdlet 會修改 Azure API 管理憑證。</span><span class="sxs-lookup"><span data-stu-id="4eab0-108">The **Set-AzApiManagementCertificate** cmdlet modifies an Azure API Management certificate.</span></span>

## <span data-ttu-id="4eab0-109">例子</span><span class="sxs-lookup"><span data-stu-id="4eab0-109">EXAMPLES</span></span>

### <span data-ttu-id="4eab0-110">範例 1：修改憑證</span><span class="sxs-lookup"><span data-stu-id="4eab0-110">Example 1: Modify a certificate</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementCertificate -Context $ApiMgmtContext -CertificateId "0123456789" -PfxFilePath "C:\contoso\certificates\apimanagementnew.pfx" -PfxPassword "2222"
```

<span data-ttu-id="4eab0-111">此命令會修改指定的 API 管理憑證。</span><span class="sxs-lookup"><span data-stu-id="4eab0-111">This command modifies the specified API Management certificate.</span></span>

## <span data-ttu-id="4eab0-112">參數</span><span class="sxs-lookup"><span data-stu-id="4eab0-112">PARAMETERS</span></span>

### <span data-ttu-id="4eab0-113">-CertificateId</span><span class="sxs-lookup"><span data-stu-id="4eab0-113">-CertificateId</span></span>
<span data-ttu-id="4eab0-114">指定要修改的憑證識別碼。</span><span class="sxs-lookup"><span data-stu-id="4eab0-114">Specifies the ID of the certificate to modify.</span></span>

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

### <span data-ttu-id="4eab0-115">-內容</span><span class="sxs-lookup"><span data-stu-id="4eab0-115">-Context</span></span>
<span data-ttu-id="4eab0-116">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="4eab0-116">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4eab0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4eab0-117">-DefaultProfile</span></span>
<span data-ttu-id="4eab0-118">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="4eab0-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4eab0-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4eab0-119">-PassThru</span></span>
<span data-ttu-id="4eab0-120">Passthru</span><span class="sxs-lookup"><span data-stu-id="4eab0-120">passthru</span></span>

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

### <span data-ttu-id="4eab0-121">-PfxBytes</span><span class="sxs-lookup"><span data-stu-id="4eab0-121">-PfxBytes</span></span>
<span data-ttu-id="4eab0-122">以 .pfx 格式指定憑證檔案的位元組陣列。</span><span class="sxs-lookup"><span data-stu-id="4eab0-122">Specifies an array of bytes of the certificate file in .pfx format.</span></span>
<span data-ttu-id="4eab0-123">如果您未指定 *PfxFilePath* 參數，則此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="4eab0-123">This parameter is required if you do not specify the *PfxFilePath* parameter.</span></span>

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

### <span data-ttu-id="4eab0-124">-PfxFilePath</span><span class="sxs-lookup"><span data-stu-id="4eab0-124">-PfxFilePath</span></span>
<span data-ttu-id="4eab0-125">指定以 .pfx 格式建立和上傳的憑證檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="4eab0-125">Specifies the path to the certificate file in .pfx format to create and upload.</span></span>
<span data-ttu-id="4eab0-126">如果您沒有指定 *PfxBytes* 參數，則此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="4eab0-126">This parameter is required if you do not specify the *PfxBytes* parameter.</span></span>

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

### <span data-ttu-id="4eab0-127">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="4eab0-127">-PfxPassword</span></span>
<span data-ttu-id="4eab0-128">指定憑證的密碼。</span><span class="sxs-lookup"><span data-stu-id="4eab0-128">Specifies the password for the certificate.</span></span>

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

### <span data-ttu-id="4eab0-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4eab0-129">CommonParameters</span></span>
<span data-ttu-id="4eab0-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="4eab0-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4eab0-131">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4eab0-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4eab0-132">輸入</span><span class="sxs-lookup"><span data-stu-id="4eab0-132">INPUTS</span></span>

### <span data-ttu-id="4eab0-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementCoNtext</span><span class="sxs-lookup"><span data-stu-id="4eab0-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="4eab0-134">System.String</span><span class="sxs-lookup"><span data-stu-id="4eab0-134">System.String</span></span>

### <span data-ttu-id="4eab0-135">System.Byte[]</span><span class="sxs-lookup"><span data-stu-id="4eab0-135">System.Byte[]</span></span>

### <span data-ttu-id="4eab0-136">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="4eab0-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="4eab0-137">輸出</span><span class="sxs-lookup"><span data-stu-id="4eab0-137">OUTPUTS</span></span>

### <span data-ttu-id="4eab0-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="4eab0-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span></span>

## <span data-ttu-id="4eab0-139">筆記</span><span class="sxs-lookup"><span data-stu-id="4eab0-139">NOTES</span></span>

## <span data-ttu-id="4eab0-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="4eab0-140">RELATED LINKS</span></span>

[<span data-ttu-id="4eab0-141">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="4eab0-141">Get-AzApiManagementCertificate</span></span>](./Get-AzApiManagementCertificate.md)

[<span data-ttu-id="4eab0-142">New-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="4eab0-142">New-AzApiManagementCertificate</span></span>](./New-AzApiManagementCertificate.md)

[<span data-ttu-id="4eab0-143">Remove-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="4eab0-143">Remove-AzApiManagementCertificate</span></span>](./Remove-AzApiManagementCertificate.md)


