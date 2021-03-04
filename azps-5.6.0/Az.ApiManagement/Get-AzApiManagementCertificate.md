---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 6F7C6611-5C56-4F1D-AB98-CDD92D88821C
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementCertificate.md
ms.openlocfilehash: 1885f8b4f3c72ace4bad55b355e1d16013228611
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906989"
---
# <span data-ttu-id="30c46-101">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="30c46-101">Get-AzApiManagementCertificate</span></span>

## <span data-ttu-id="30c46-102">簡介</span><span class="sxs-lookup"><span data-stu-id="30c46-102">SYNOPSIS</span></span>
<span data-ttu-id="30c46-103">針對服務中的後端進行相互驗證，獲得 API 管理憑證。</span><span class="sxs-lookup"><span data-stu-id="30c46-103">Gets API Management certificates configured for Mutual Authentication with Backend in the service.</span></span>

## <span data-ttu-id="30c46-104">語法</span><span class="sxs-lookup"><span data-stu-id="30c46-104">SYNTAX</span></span>

### <span data-ttu-id="30c46-105">CoNtextParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="30c46-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementCertificate -Context <PsApiManagementContext> [-CertificateId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="30c46-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="30c46-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementCertificate [-CertificateId <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="30c46-107">描述</span><span class="sxs-lookup"><span data-stu-id="30c46-107">DESCRIPTION</span></span>
<span data-ttu-id="30c46-108">**Get-AzApiManagementCertificate Cmdlet** 會取得您指定的所有 Azure API 管理憑證或憑證。</span><span class="sxs-lookup"><span data-stu-id="30c46-108">The **Get-AzApiManagementCertificate** cmdlet gets all Azure API Management certificates or certificates that you specify.</span></span>

## <span data-ttu-id="30c46-109">例子</span><span class="sxs-lookup"><span data-stu-id="30c46-109">EXAMPLES</span></span>

### <span data-ttu-id="30c46-110">範例 1：取得所有憑證</span><span class="sxs-lookup"><span data-stu-id="30c46-110">Example 1: Get all certificates</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementCertificate -Context $ApiMgmtContext
```

<span data-ttu-id="30c46-111">此命令會獲得所有 API 管理憑證。</span><span class="sxs-lookup"><span data-stu-id="30c46-111">This command gets all API Management certificates.</span></span>

### <span data-ttu-id="30c46-112">範例 2：根據憑證識別碼取得憑證</span><span class="sxs-lookup"><span data-stu-id="30c46-112">Example 2: Get a certificate by its ID</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementCertificate -Context $ApiMgmtContext -CertificateId "0123456789"
```

<span data-ttu-id="30c46-113">此命令會獲得具有指定識別碼的 API 管理憑證。</span><span class="sxs-lookup"><span data-stu-id="30c46-113">This command gets the API Management certificate with the specified ID.</span></span>

## <span data-ttu-id="30c46-114">參數</span><span class="sxs-lookup"><span data-stu-id="30c46-114">PARAMETERS</span></span>

### <span data-ttu-id="30c46-115">-CertificateId</span><span class="sxs-lookup"><span data-stu-id="30c46-115">-CertificateId</span></span>
<span data-ttu-id="30c46-116">指定要取得之憑證的識別碼。</span><span class="sxs-lookup"><span data-stu-id="30c46-116">Specifies the ID of the certificate to get.</span></span>

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

### <span data-ttu-id="30c46-117">-內容</span><span class="sxs-lookup"><span data-stu-id="30c46-117">-Context</span></span>
<span data-ttu-id="30c46-118">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="30c46-118">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="30c46-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30c46-119">-DefaultProfile</span></span>
<span data-ttu-id="30c46-120">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="30c46-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="30c46-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="30c46-121">-ResourceId</span></span>
<span data-ttu-id="30c46-122">憑證的 Arm 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="30c46-122">Arm Resource Identifier of the Certificate.</span></span> <span data-ttu-id="30c46-123">如果指定，會嘗試根據識別碼尋找憑證。</span><span class="sxs-lookup"><span data-stu-id="30c46-123">If specified will try to find certificate by the identifier.</span></span> <span data-ttu-id="30c46-124">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="30c46-124">This parameter is required.</span></span>

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

### <span data-ttu-id="30c46-125">-確認</span><span class="sxs-lookup"><span data-stu-id="30c46-125">-Confirm</span></span>
<span data-ttu-id="30c46-126">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="30c46-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30c46-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30c46-127">-WhatIf</span></span>
<span data-ttu-id="30c46-128">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="30c46-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="30c46-129">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="30c46-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30c46-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30c46-130">CommonParameters</span></span>
<span data-ttu-id="30c46-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="30c46-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30c46-132">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="30c46-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30c46-133">輸入</span><span class="sxs-lookup"><span data-stu-id="30c46-133">INPUTS</span></span>

### <span data-ttu-id="30c46-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementCoNtext</span><span class="sxs-lookup"><span data-stu-id="30c46-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="30c46-135">System.String</span><span class="sxs-lookup"><span data-stu-id="30c46-135">System.String</span></span>

## <span data-ttu-id="30c46-136">輸出</span><span class="sxs-lookup"><span data-stu-id="30c46-136">OUTPUTS</span></span>

### <span data-ttu-id="30c46-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="30c46-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span></span>

## <span data-ttu-id="30c46-138">筆記</span><span class="sxs-lookup"><span data-stu-id="30c46-138">NOTES</span></span>

## <span data-ttu-id="30c46-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="30c46-139">RELATED LINKS</span></span>

[<span data-ttu-id="30c46-140">New-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="30c46-140">New-AzApiManagementCertificate</span></span>](./New-AzApiManagementCertificate.md)

[<span data-ttu-id="30c46-141">Remove-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="30c46-141">Remove-AzApiManagementCertificate</span></span>](./Remove-AzApiManagementCertificate.md)

[<span data-ttu-id="30c46-142">Set-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="30c46-142">Set-AzApiManagementCertificate</span></span>](./Set-AzApiManagementCertificate.md)


