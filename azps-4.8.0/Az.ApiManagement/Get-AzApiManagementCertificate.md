---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 6F7C6611-5C56-4F1D-AB98-CDD92D88821C
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementCertificate.md
ms.openlocfilehash: 9826de76a65fe097d2daba106bd74df5e94a730e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94136094"
---
# <span data-ttu-id="f7246-101">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="f7246-101">Get-AzApiManagementCertificate</span></span>

## <span data-ttu-id="f7246-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f7246-102">SYNOPSIS</span></span>
<span data-ttu-id="f7246-103">取得在服務中後端驗證所設定的 API 管理憑證。</span><span class="sxs-lookup"><span data-stu-id="f7246-103">Gets API Management certificates configured for Mutual Authentication with Backend in the service.</span></span>

## <span data-ttu-id="f7246-104">句法</span><span class="sxs-lookup"><span data-stu-id="f7246-104">SYNTAX</span></span>

### <span data-ttu-id="f7246-105">CoNtextParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="f7246-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementCertificate -Context <PsApiManagementContext> [-CertificateId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7246-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f7246-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementCertificate [-CertificateId <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7246-107">說明</span><span class="sxs-lookup"><span data-stu-id="f7246-107">DESCRIPTION</span></span>
<span data-ttu-id="f7246-108">**AzApiManagementCertificate** Cmdlet 會取得您指定的所有 Azure API 管理憑證或憑證。</span><span class="sxs-lookup"><span data-stu-id="f7246-108">The **Get-AzApiManagementCertificate** cmdlet gets all Azure API Management certificates or certificates that you specify.</span></span>

## <span data-ttu-id="f7246-109">示例</span><span class="sxs-lookup"><span data-stu-id="f7246-109">EXAMPLES</span></span>

### <span data-ttu-id="f7246-110">範例1：取得所有憑證</span><span class="sxs-lookup"><span data-stu-id="f7246-110">Example 1: Get all certificates</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementCertificate -Context $ApiMgmtContext
```

<span data-ttu-id="f7246-111">這個命令會取得所有 API 管理憑證。</span><span class="sxs-lookup"><span data-stu-id="f7246-111">This command gets all API Management certificates.</span></span>

### <span data-ttu-id="f7246-112">範例2：根據其識別碼取得憑證</span><span class="sxs-lookup"><span data-stu-id="f7246-112">Example 2: Get a certificate by its ID</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementCertificate -Context $ApiMgmtContext -CertificateId "0123456789"
```

<span data-ttu-id="f7246-113">這個命令會取得具有指定識別碼的 API 管理憑證。</span><span class="sxs-lookup"><span data-stu-id="f7246-113">This command gets the API Management certificate with the specified ID.</span></span>

## <span data-ttu-id="f7246-114">參數</span><span class="sxs-lookup"><span data-stu-id="f7246-114">PARAMETERS</span></span>

### <span data-ttu-id="f7246-115">-CertificateId</span><span class="sxs-lookup"><span data-stu-id="f7246-115">-CertificateId</span></span>
<span data-ttu-id="f7246-116">指定要取得的憑證識別碼。</span><span class="sxs-lookup"><span data-stu-id="f7246-116">Specifies the ID of the certificate to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7246-117">-內容</span><span class="sxs-lookup"><span data-stu-id="f7246-117">-Context</span></span>
<span data-ttu-id="f7246-118">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="f7246-118">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f7246-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7246-119">-DefaultProfile</span></span>
<span data-ttu-id="f7246-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f7246-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f7246-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f7246-121">-ResourceId</span></span>
<span data-ttu-id="f7246-122">憑證的 Arm 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="f7246-122">Arm Resource Identifier of the Certificate.</span></span> <span data-ttu-id="f7246-123">如果已指定，將會嘗試依據識別碼尋找憑證。</span><span class="sxs-lookup"><span data-stu-id="f7246-123">If specified will try to find certificate by the identifier.</span></span> <span data-ttu-id="f7246-124">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="f7246-124">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7246-125">-確認</span><span class="sxs-lookup"><span data-stu-id="f7246-125">-Confirm</span></span>
<span data-ttu-id="f7246-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f7246-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7246-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7246-127">-WhatIf</span></span>
<span data-ttu-id="f7246-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f7246-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7246-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f7246-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7246-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7246-130">CommonParameters</span></span>
<span data-ttu-id="f7246-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f7246-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7246-132">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f7246-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7246-133">輸入</span><span class="sxs-lookup"><span data-stu-id="f7246-133">INPUTS</span></span>

### <span data-ttu-id="f7246-134">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="f7246-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="f7246-135">System.object</span><span class="sxs-lookup"><span data-stu-id="f7246-135">System.String</span></span>

## <span data-ttu-id="f7246-136">輸出</span><span class="sxs-lookup"><span data-stu-id="f7246-136">OUTPUTS</span></span>

### <span data-ttu-id="f7246-137">ServiceManagement. PsApiManagementCertificate （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="f7246-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span></span>

## <span data-ttu-id="f7246-138">筆記</span><span class="sxs-lookup"><span data-stu-id="f7246-138">NOTES</span></span>

## <span data-ttu-id="f7246-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="f7246-139">RELATED LINKS</span></span>

[<span data-ttu-id="f7246-140">新-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="f7246-140">New-AzApiManagementCertificate</span></span>](./New-AzApiManagementCertificate.md)

[<span data-ttu-id="f7246-141">移除-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="f7246-141">Remove-AzApiManagementCertificate</span></span>](./Remove-AzApiManagementCertificate.md)

[<span data-ttu-id="f7246-142">Set-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="f7246-142">Set-AzApiManagementCertificate</span></span>](./Set-AzApiManagementCertificate.md)


