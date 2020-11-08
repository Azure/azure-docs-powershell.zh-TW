---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 12FC21EB-0B4E-4275-88FB-7FF42730A6A0
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementCertificate.md
ms.openlocfilehash: 3c31da297b47c5d35c7d7b4eea5c55ca87d9521d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94137723"
---
# <span data-ttu-id="05305-101">Set-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="05305-101">Set-AzApiManagementCertificate</span></span>

## <span data-ttu-id="05305-102">摘要</span><span class="sxs-lookup"><span data-stu-id="05305-102">SYNOPSIS</span></span>
<span data-ttu-id="05305-103">修改以後端驗證所設定之共同驗證的 API 管理憑證。</span><span class="sxs-lookup"><span data-stu-id="05305-103">Modifies an API Management certificate which is configured for mutual authentication with backend.</span></span>

## <span data-ttu-id="05305-104">句法</span><span class="sxs-lookup"><span data-stu-id="05305-104">SYNTAX</span></span>

### <span data-ttu-id="05305-105">LoadFromFile (預設) </span><span class="sxs-lookup"><span data-stu-id="05305-105">LoadFromFile (Default)</span></span>
```
Set-AzApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String> -PfxFilePath <String>
 -PfxPassword <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="05305-106">未經</span><span class="sxs-lookup"><span data-stu-id="05305-106">Raw</span></span>
```
Set-AzApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String> -PfxBytes <Byte[]>
 -PfxPassword <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="05305-107">說明</span><span class="sxs-lookup"><span data-stu-id="05305-107">DESCRIPTION</span></span>
<span data-ttu-id="05305-108">**AzApiManagementCertificate** Cmdlet 會修改 Azure API 管理憑證。</span><span class="sxs-lookup"><span data-stu-id="05305-108">The **Set-AzApiManagementCertificate** cmdlet modifies an Azure API Management certificate.</span></span>

## <span data-ttu-id="05305-109">示例</span><span class="sxs-lookup"><span data-stu-id="05305-109">EXAMPLES</span></span>

### <span data-ttu-id="05305-110">範例1：修改憑證</span><span class="sxs-lookup"><span data-stu-id="05305-110">Example 1: Modify a certificate</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementCertificate -Context $ApiMgmtContext -CertificateId "0123456789" -PfxFilePath "C:\contoso\certificates\apimanagementnew.pfx" -PfxPassword "2222"
```

<span data-ttu-id="05305-111">這個命令會修改指定的 API 管理憑證。</span><span class="sxs-lookup"><span data-stu-id="05305-111">This command modifies the specified API Management certificate.</span></span>

## <span data-ttu-id="05305-112">參數</span><span class="sxs-lookup"><span data-stu-id="05305-112">PARAMETERS</span></span>

### <span data-ttu-id="05305-113">-CertificateId</span><span class="sxs-lookup"><span data-stu-id="05305-113">-CertificateId</span></span>
<span data-ttu-id="05305-114">指定要修改的憑證識別碼。</span><span class="sxs-lookup"><span data-stu-id="05305-114">Specifies the ID of the certificate to modify.</span></span>

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

### <span data-ttu-id="05305-115">-內容</span><span class="sxs-lookup"><span data-stu-id="05305-115">-Context</span></span>
<span data-ttu-id="05305-116">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="05305-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="05305-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05305-117">-DefaultProfile</span></span>
<span data-ttu-id="05305-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="05305-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="05305-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="05305-119">-PassThru</span></span>
<span data-ttu-id="05305-120">passthru</span><span class="sxs-lookup"><span data-stu-id="05305-120">passthru</span></span>

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

### <span data-ttu-id="05305-121">-PfxBytes</span><span class="sxs-lookup"><span data-stu-id="05305-121">-PfxBytes</span></span>
<span data-ttu-id="05305-122">以 .pfx 格式指定憑證檔的位元組陣列。</span><span class="sxs-lookup"><span data-stu-id="05305-122">Specifies an array of bytes of the certificate file in .pfx format.</span></span>
<span data-ttu-id="05305-123">如果您沒有指定 *PfxFilePath* 參數，則需要此參數。</span><span class="sxs-lookup"><span data-stu-id="05305-123">This parameter is required if you do not specify the *PfxFilePath* parameter.</span></span>

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

### <span data-ttu-id="05305-124">-PfxFilePath</span><span class="sxs-lookup"><span data-stu-id="05305-124">-PfxFilePath</span></span>
<span data-ttu-id="05305-125">指定要建立和上傳的憑證檔案的路徑（.pfx 格式）。</span><span class="sxs-lookup"><span data-stu-id="05305-125">Specifies the path to the certificate file in .pfx format to create and upload.</span></span>
<span data-ttu-id="05305-126">如果您沒有指定 *PfxBytes* 參數，則需要此參數。</span><span class="sxs-lookup"><span data-stu-id="05305-126">This parameter is required if you do not specify the *PfxBytes* parameter.</span></span>

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

### <span data-ttu-id="05305-127">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="05305-127">-PfxPassword</span></span>
<span data-ttu-id="05305-128">指定憑證的密碼。</span><span class="sxs-lookup"><span data-stu-id="05305-128">Specifies the password for the certificate.</span></span>

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

### <span data-ttu-id="05305-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05305-129">CommonParameters</span></span>
<span data-ttu-id="05305-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="05305-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05305-131">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="05305-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05305-132">輸入</span><span class="sxs-lookup"><span data-stu-id="05305-132">INPUTS</span></span>

### <span data-ttu-id="05305-133">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="05305-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="05305-134">System.object</span><span class="sxs-lookup"><span data-stu-id="05305-134">System.String</span></span>

### <span data-ttu-id="05305-135">System.object []</span><span class="sxs-lookup"><span data-stu-id="05305-135">System.Byte[]</span></span>

### <span data-ttu-id="05305-136">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="05305-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="05305-137">輸出</span><span class="sxs-lookup"><span data-stu-id="05305-137">OUTPUTS</span></span>

### <span data-ttu-id="05305-138">ServiceManagement. PsApiManagementCertificate （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="05305-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span></span>

## <span data-ttu-id="05305-139">筆記</span><span class="sxs-lookup"><span data-stu-id="05305-139">NOTES</span></span>

## <span data-ttu-id="05305-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="05305-140">RELATED LINKS</span></span>

[<span data-ttu-id="05305-141">AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="05305-141">Get-AzApiManagementCertificate</span></span>](./Get-AzApiManagementCertificate.md)

[<span data-ttu-id="05305-142">新-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="05305-142">New-AzApiManagementCertificate</span></span>](./New-AzApiManagementCertificate.md)

[<span data-ttu-id="05305-143">移除-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="05305-143">Remove-AzApiManagementCertificate</span></span>](./Remove-AzApiManagementCertificate.md)

