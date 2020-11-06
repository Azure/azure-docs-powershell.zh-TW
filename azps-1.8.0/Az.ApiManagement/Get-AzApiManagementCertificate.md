---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 6F7C6611-5C56-4F1D-AB98-CDD92D88821C
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementCertificate.md
ms.openlocfilehash: 52d40ed69adda157a8fdacd9d6c961f88508fbb9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93611628"
---
# <span data-ttu-id="4eb8a-101">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="4eb8a-101">Get-AzApiManagementCertificate</span></span>

## <span data-ttu-id="4eb8a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4eb8a-102">SYNOPSIS</span></span>
<span data-ttu-id="4eb8a-103">取得在服務中後端驗證所設定的 API 管理憑證。</span><span class="sxs-lookup"><span data-stu-id="4eb8a-103">Gets API Management certificates configured for Mutual Authentication with Backend in the service.</span></span>

## <span data-ttu-id="4eb8a-104">句法</span><span class="sxs-lookup"><span data-stu-id="4eb8a-104">SYNTAX</span></span>

### <span data-ttu-id="4eb8a-105">GetAllCertificates (預設) </span><span class="sxs-lookup"><span data-stu-id="4eb8a-105">GetAllCertificates (Default)</span></span>
```
Get-AzApiManagementCertificate -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4eb8a-106">GetByCertificateId</span><span class="sxs-lookup"><span data-stu-id="4eb8a-106">GetByCertificateId</span></span>
```
Get-AzApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4eb8a-107">說明</span><span class="sxs-lookup"><span data-stu-id="4eb8a-107">DESCRIPTION</span></span>
<span data-ttu-id="4eb8a-108">**AzApiManagementCertificate** Cmdlet 會取得您指定的所有 Azure API 管理憑證或憑證。</span><span class="sxs-lookup"><span data-stu-id="4eb8a-108">The **Get-AzApiManagementCertificate** cmdlet gets all Azure API Management certificates or certificates that you specify.</span></span>

## <span data-ttu-id="4eb8a-109">示例</span><span class="sxs-lookup"><span data-stu-id="4eb8a-109">EXAMPLES</span></span>

### <span data-ttu-id="4eb8a-110">範例1：取得所有憑證</span><span class="sxs-lookup"><span data-stu-id="4eb8a-110">Example 1: Get all certificates</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementCertificate -Context $ApiMgmtContext
```

<span data-ttu-id="4eb8a-111">這個命令會取得所有 API 管理憑證。</span><span class="sxs-lookup"><span data-stu-id="4eb8a-111">This command gets all API Management certificates.</span></span>

### <span data-ttu-id="4eb8a-112">範例2：根據其識別碼取得憑證</span><span class="sxs-lookup"><span data-stu-id="4eb8a-112">Example 2: Get a certificate by its ID</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementCertificate -Context $ApiMgmtContext -CertificateId "0123456789"
```

<span data-ttu-id="4eb8a-113">這個命令會取得具有指定識別碼的 API 管理憑證。</span><span class="sxs-lookup"><span data-stu-id="4eb8a-113">This command gets the API Management certificate with the specified ID.</span></span>

## <span data-ttu-id="4eb8a-114">參數</span><span class="sxs-lookup"><span data-stu-id="4eb8a-114">PARAMETERS</span></span>

### <span data-ttu-id="4eb8a-115">-CertificateId</span><span class="sxs-lookup"><span data-stu-id="4eb8a-115">-CertificateId</span></span>
<span data-ttu-id="4eb8a-116">指定要取得的憑證識別碼。</span><span class="sxs-lookup"><span data-stu-id="4eb8a-116">Specifies the ID of the certificate to get.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByCertificateId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4eb8a-117">-內容</span><span class="sxs-lookup"><span data-stu-id="4eb8a-117">-Context</span></span>
<span data-ttu-id="4eb8a-118">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="4eb8a-118">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="4eb8a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4eb8a-119">-DefaultProfile</span></span>
<span data-ttu-id="4eb8a-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4eb8a-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4eb8a-121">-確認</span><span class="sxs-lookup"><span data-stu-id="4eb8a-121">-Confirm</span></span>
<span data-ttu-id="4eb8a-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4eb8a-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4eb8a-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4eb8a-123">-WhatIf</span></span>
<span data-ttu-id="4eb8a-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4eb8a-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4eb8a-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4eb8a-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4eb8a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4eb8a-126">CommonParameters</span></span>
<span data-ttu-id="4eb8a-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4eb8a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4eb8a-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4eb8a-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4eb8a-129">輸入</span><span class="sxs-lookup"><span data-stu-id="4eb8a-129">INPUTS</span></span>

### <span data-ttu-id="4eb8a-130">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="4eb8a-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="4eb8a-131">System.object</span><span class="sxs-lookup"><span data-stu-id="4eb8a-131">System.String</span></span>

## <span data-ttu-id="4eb8a-132">輸出</span><span class="sxs-lookup"><span data-stu-id="4eb8a-132">OUTPUTS</span></span>

### <span data-ttu-id="4eb8a-133">ServiceManagement. PsApiManagementCertificate （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="4eb8a-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span></span>

## <span data-ttu-id="4eb8a-134">筆記</span><span class="sxs-lookup"><span data-stu-id="4eb8a-134">NOTES</span></span>

## <span data-ttu-id="4eb8a-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="4eb8a-135">RELATED LINKS</span></span>

[<span data-ttu-id="4eb8a-136">新-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="4eb8a-136">New-AzApiManagementCertificate</span></span>](./New-AzApiManagementCertificate.md)

[<span data-ttu-id="4eb8a-137">移除-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="4eb8a-137">Remove-AzApiManagementCertificate</span></span>](./Remove-AzApiManagementCertificate.md)

[<span data-ttu-id="4eb8a-138">Set-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="4eb8a-138">Set-AzApiManagementCertificate</span></span>](./Set-AzApiManagementCertificate.md)


