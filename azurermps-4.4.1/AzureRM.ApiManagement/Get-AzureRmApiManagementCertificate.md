---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 6F7C6611-5C56-4F1D-AB98-CDD92D88821C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementCertificate.md
ms.openlocfilehash: 167137cbb231bbd5093b118a22d33e2102159c67
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450138"
---
# <span data-ttu-id="fd8d3-101">Get-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="fd8d3-101">Get-AzureRmApiManagementCertificate</span></span>

## <span data-ttu-id="fd8d3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fd8d3-102">SYNOPSIS</span></span>
<span data-ttu-id="fd8d3-103">取得 API 管理憑證。</span><span class="sxs-lookup"><span data-stu-id="fd8d3-103">Gets API Management certificates.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fd8d3-104">句法</span><span class="sxs-lookup"><span data-stu-id="fd8d3-104">SYNTAX</span></span>

### <span data-ttu-id="fd8d3-105">取得所有憑證 (預設) </span><span class="sxs-lookup"><span data-stu-id="fd8d3-105">Get all certificates (Default)</span></span>
```
Get-AzureRmApiManagementCertificate -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd8d3-106">透過識別碼取得憑證</span><span class="sxs-lookup"><span data-stu-id="fd8d3-106">Get certificate by ID</span></span>
```
Get-AzureRmApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd8d3-107">說明</span><span class="sxs-lookup"><span data-stu-id="fd8d3-107">DESCRIPTION</span></span>
<span data-ttu-id="fd8d3-108">**AzureRmApiManagementCertificate** Cmdlet 會取得您指定的所有 Azure API 管理憑證或憑證。</span><span class="sxs-lookup"><span data-stu-id="fd8d3-108">The **Get-AzureRmApiManagementCertificate** cmdlet gets all Azure API Management certificates or certificates that you specify.</span></span>

## <span data-ttu-id="fd8d3-109">示例</span><span class="sxs-lookup"><span data-stu-id="fd8d3-109">EXAMPLES</span></span>

### <span data-ttu-id="fd8d3-110">範例1：取得所有憑證</span><span class="sxs-lookup"><span data-stu-id="fd8d3-110">Example 1: Get all certificates</span></span>
```
PS C:\>Get-AzureRmApiManagementCertificate -Context $ApiMgmtContext
```

<span data-ttu-id="fd8d3-111">這個命令會取得所有 API 管理憑證。</span><span class="sxs-lookup"><span data-stu-id="fd8d3-111">This command gets all API Management certificates.</span></span>

### <span data-ttu-id="fd8d3-112">範例2：根據其識別碼取得憑證</span><span class="sxs-lookup"><span data-stu-id="fd8d3-112">Example 2: Get a certificate by its ID</span></span>
```
PS C:\>Get-AzureRmApiManagementCertificate -Context $ApiMgmtContext -CertificateId "0123456789"
```

<span data-ttu-id="fd8d3-113">這個命令會取得具有指定識別碼的 API 管理憑證。</span><span class="sxs-lookup"><span data-stu-id="fd8d3-113">This command gets the API Management certificate with the specified ID.</span></span>

## <span data-ttu-id="fd8d3-114">參數</span><span class="sxs-lookup"><span data-stu-id="fd8d3-114">PARAMETERS</span></span>

### <span data-ttu-id="fd8d3-115">-CertificateId</span><span class="sxs-lookup"><span data-stu-id="fd8d3-115">-CertificateId</span></span>
<span data-ttu-id="fd8d3-116">指定要取得的憑證識別碼。</span><span class="sxs-lookup"><span data-stu-id="fd8d3-116">Specifies the ID of the certificate to get.</span></span>

```yaml
Type: System.String
Parameter Sets: Get certificate by ID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd8d3-117">-內容</span><span class="sxs-lookup"><span data-stu-id="fd8d3-117">-Context</span></span>
<span data-ttu-id="fd8d3-118">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="fd8d3-118">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="fd8d3-119">-確認</span><span class="sxs-lookup"><span data-stu-id="fd8d3-119">-Confirm</span></span>
<span data-ttu-id="fd8d3-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="fd8d3-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd8d3-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd8d3-121">-WhatIf</span></span>
<span data-ttu-id="fd8d3-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="fd8d3-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd8d3-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fd8d3-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd8d3-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd8d3-124">-DefaultProfile</span></span>
<span data-ttu-id="fd8d3-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="fd8d3-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fd8d3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd8d3-126">CommonParameters</span></span>
<span data-ttu-id="fd8d3-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fd8d3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd8d3-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="fd8d3-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd8d3-129">輸入</span><span class="sxs-lookup"><span data-stu-id="fd8d3-129">INPUTS</span></span>

## <span data-ttu-id="fd8d3-130">輸出</span><span class="sxs-lookup"><span data-stu-id="fd8d3-130">OUTPUTS</span></span>

### <span data-ttu-id="fd8d3-131">ServiceManagement. PsApiManagementCertificate （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="fd8d3-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span></span>

## <span data-ttu-id="fd8d3-132">筆記</span><span class="sxs-lookup"><span data-stu-id="fd8d3-132">NOTES</span></span>

## <span data-ttu-id="fd8d3-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="fd8d3-133">RELATED LINKS</span></span>

[<span data-ttu-id="fd8d3-134">新-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="fd8d3-134">New-AzureRmApiManagementCertificate</span></span>](./New-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="fd8d3-135">移除-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="fd8d3-135">Remove-AzureRmApiManagementCertificate</span></span>](./Remove-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="fd8d3-136">Set-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="fd8d3-136">Set-AzureRmApiManagementCertificate</span></span>](./Set-AzureRmApiManagementCertificate.md)


