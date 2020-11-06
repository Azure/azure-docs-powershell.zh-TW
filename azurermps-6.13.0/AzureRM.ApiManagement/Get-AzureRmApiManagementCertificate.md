---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 6F7C6611-5C56-4F1D-AB98-CDD92D88821C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementCertificate.md
ms.openlocfilehash: af187553ef8ea432299197cd06baefd585e73cd4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450354"
---
# <span data-ttu-id="8ed3d-101">Get-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="8ed3d-101">Get-AzureRmApiManagementCertificate</span></span>

## <span data-ttu-id="8ed3d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8ed3d-102">SYNOPSIS</span></span>
<span data-ttu-id="8ed3d-103">取得在服務中後端驗證所設定的 API 管理憑證。</span><span class="sxs-lookup"><span data-stu-id="8ed3d-103">Gets API Management certificates configured for Mutual Authentication with Backend in the service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8ed3d-104">句法</span><span class="sxs-lookup"><span data-stu-id="8ed3d-104">SYNTAX</span></span>

### <span data-ttu-id="8ed3d-105">GetAllCertificates (預設) </span><span class="sxs-lookup"><span data-stu-id="8ed3d-105">GetAllCertificates (Default)</span></span>
```
Get-AzureRmApiManagementCertificate -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ed3d-106">GetByCertificateId</span><span class="sxs-lookup"><span data-stu-id="8ed3d-106">GetByCertificateId</span></span>
```
Get-AzureRmApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8ed3d-107">說明</span><span class="sxs-lookup"><span data-stu-id="8ed3d-107">DESCRIPTION</span></span>
<span data-ttu-id="8ed3d-108">**AzureRmApiManagementCertificate** Cmdlet 會取得您指定的所有 Azure API 管理憑證或憑證。</span><span class="sxs-lookup"><span data-stu-id="8ed3d-108">The **Get-AzureRmApiManagementCertificate** cmdlet gets all Azure API Management certificates or certificates that you specify.</span></span>

## <span data-ttu-id="8ed3d-109">示例</span><span class="sxs-lookup"><span data-stu-id="8ed3d-109">EXAMPLES</span></span>

### <span data-ttu-id="8ed3d-110">範例1：取得所有憑證</span><span class="sxs-lookup"><span data-stu-id="8ed3d-110">Example 1: Get all certificates</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementCertificate -Context $ApiMgmtContext
```

<span data-ttu-id="8ed3d-111">這個命令會取得所有 API 管理憑證。</span><span class="sxs-lookup"><span data-stu-id="8ed3d-111">This command gets all API Management certificates.</span></span>

### <span data-ttu-id="8ed3d-112">範例2：根據其識別碼取得憑證</span><span class="sxs-lookup"><span data-stu-id="8ed3d-112">Example 2: Get a certificate by its ID</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementCertificate -Context $ApiMgmtContext -CertificateId "0123456789"
```

<span data-ttu-id="8ed3d-113">這個命令會取得具有指定識別碼的 API 管理憑證。</span><span class="sxs-lookup"><span data-stu-id="8ed3d-113">This command gets the API Management certificate with the specified ID.</span></span>

## <span data-ttu-id="8ed3d-114">參數</span><span class="sxs-lookup"><span data-stu-id="8ed3d-114">PARAMETERS</span></span>

### <span data-ttu-id="8ed3d-115">-CertificateId</span><span class="sxs-lookup"><span data-stu-id="8ed3d-115">-CertificateId</span></span>
<span data-ttu-id="8ed3d-116">指定要取得的憑證識別碼。</span><span class="sxs-lookup"><span data-stu-id="8ed3d-116">Specifies the ID of the certificate to get.</span></span>

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

### <span data-ttu-id="8ed3d-117">-內容</span><span class="sxs-lookup"><span data-stu-id="8ed3d-117">-Context</span></span>
<span data-ttu-id="8ed3d-118">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="8ed3d-118">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="8ed3d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ed3d-119">-DefaultProfile</span></span>
<span data-ttu-id="8ed3d-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8ed3d-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8ed3d-121">-確認</span><span class="sxs-lookup"><span data-stu-id="8ed3d-121">-Confirm</span></span>
<span data-ttu-id="8ed3d-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8ed3d-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ed3d-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ed3d-123">-WhatIf</span></span>
<span data-ttu-id="8ed3d-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8ed3d-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8ed3d-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8ed3d-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ed3d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ed3d-126">CommonParameters</span></span>
<span data-ttu-id="8ed3d-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8ed3d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ed3d-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8ed3d-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ed3d-129">輸入</span><span class="sxs-lookup"><span data-stu-id="8ed3d-129">INPUTS</span></span>

### <span data-ttu-id="8ed3d-130">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="8ed3d-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="8ed3d-131">System.object</span><span class="sxs-lookup"><span data-stu-id="8ed3d-131">System.String</span></span>

## <span data-ttu-id="8ed3d-132">輸出</span><span class="sxs-lookup"><span data-stu-id="8ed3d-132">OUTPUTS</span></span>

### <span data-ttu-id="8ed3d-133">ServiceManagement. PsApiManagementCertificate （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="8ed3d-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span></span>

## <span data-ttu-id="8ed3d-134">筆記</span><span class="sxs-lookup"><span data-stu-id="8ed3d-134">NOTES</span></span>

## <span data-ttu-id="8ed3d-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="8ed3d-135">RELATED LINKS</span></span>

[<span data-ttu-id="8ed3d-136">新-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="8ed3d-136">New-AzureRmApiManagementCertificate</span></span>](./New-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="8ed3d-137">移除-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="8ed3d-137">Remove-AzureRmApiManagementCertificate</span></span>](./Remove-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="8ed3d-138">Set-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="8ed3d-138">Set-AzureRmApiManagementCertificate</span></span>](./Set-AzureRmApiManagementCertificate.md)


