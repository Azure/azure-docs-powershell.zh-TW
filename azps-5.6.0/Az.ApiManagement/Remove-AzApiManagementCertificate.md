---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 9B261CD8-5209-4C14-A6F8-97D61B641642
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementCertificate.md
ms.openlocfilehash: 2a28464c735627e97551e845b1d463da9f324a5d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906985"
---
# <span data-ttu-id="b0685-101">Remove-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="b0685-101">Remove-AzApiManagementCertificate</span></span>

## <span data-ttu-id="b0685-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b0685-102">SYNOPSIS</span></span>
<span data-ttu-id="b0685-103">移除 API 管理憑證。</span><span class="sxs-lookup"><span data-stu-id="b0685-103">Removes an API Management certificate.</span></span>

## <span data-ttu-id="b0685-104">語法</span><span class="sxs-lookup"><span data-stu-id="b0685-104">SYNTAX</span></span>

```
Remove-AzApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b0685-105">描述</span><span class="sxs-lookup"><span data-stu-id="b0685-105">DESCRIPTION</span></span>
<span data-ttu-id="b0685-106">**Remove-AzApiManagementCertificate** Cmdlet 會移除 Azure API 管理憑證。</span><span class="sxs-lookup"><span data-stu-id="b0685-106">The **Remove-AzApiManagementCertificate** cmdlet removes an Azure API Management certificate.</span></span>

## <span data-ttu-id="b0685-107">例子</span><span class="sxs-lookup"><span data-stu-id="b0685-107">EXAMPLES</span></span>

### <span data-ttu-id="b0685-108">範例 1：移除憑證</span><span class="sxs-lookup"><span data-stu-id="b0685-108">Example 1: Remove a certificate</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementCertificate -Context $ApiMgmtContext -CertificateId "0123456789" -Force
```

<span data-ttu-id="b0685-109">此命令會移除指定的 API 管理憑證。</span><span class="sxs-lookup"><span data-stu-id="b0685-109">This command removes the specified API Management certificate.</span></span>
<span data-ttu-id="b0685-110">由於 *已指定 Force* 參數，因此不需要確認。</span><span class="sxs-lookup"><span data-stu-id="b0685-110">Because the *Force* parameter is specified, no confirmation is required.</span></span>

## <span data-ttu-id="b0685-111">參數</span><span class="sxs-lookup"><span data-stu-id="b0685-111">PARAMETERS</span></span>

### <span data-ttu-id="b0685-112">-CertificateId</span><span class="sxs-lookup"><span data-stu-id="b0685-112">-CertificateId</span></span>
<span data-ttu-id="b0685-113">指定要移除的憑證識別碼。</span><span class="sxs-lookup"><span data-stu-id="b0685-113">Specifies the ID of the certificate to remove.</span></span>

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

### <span data-ttu-id="b0685-114">-內容</span><span class="sxs-lookup"><span data-stu-id="b0685-114">-Context</span></span>
<span data-ttu-id="b0685-115">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="b0685-115">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="b0685-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0685-116">-DefaultProfile</span></span>
<span data-ttu-id="b0685-117">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b0685-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b0685-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b0685-118">-PassThru</span></span>
<span data-ttu-id="b0685-119">Passthru</span><span class="sxs-lookup"><span data-stu-id="b0685-119">passthru</span></span>

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

### <span data-ttu-id="b0685-120">-確認</span><span class="sxs-lookup"><span data-stu-id="b0685-120">-Confirm</span></span>
<span data-ttu-id="b0685-121">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="b0685-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0685-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0685-122">-WhatIf</span></span>
<span data-ttu-id="b0685-123">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b0685-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b0685-124">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b0685-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0685-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0685-125">CommonParameters</span></span>
<span data-ttu-id="b0685-126">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b0685-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0685-127">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b0685-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0685-128">輸入</span><span class="sxs-lookup"><span data-stu-id="b0685-128">INPUTS</span></span>

### <span data-ttu-id="b0685-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementCoNtext</span><span class="sxs-lookup"><span data-stu-id="b0685-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="b0685-130">System.String</span><span class="sxs-lookup"><span data-stu-id="b0685-130">System.String</span></span>

### <span data-ttu-id="b0685-131">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="b0685-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b0685-132">輸出</span><span class="sxs-lookup"><span data-stu-id="b0685-132">OUTPUTS</span></span>

### <span data-ttu-id="b0685-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b0685-133">System.Boolean</span></span>

## <span data-ttu-id="b0685-134">筆記</span><span class="sxs-lookup"><span data-stu-id="b0685-134">NOTES</span></span>

## <span data-ttu-id="b0685-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="b0685-135">RELATED LINKS</span></span>

[<span data-ttu-id="b0685-136">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="b0685-136">Get-AzApiManagementCertificate</span></span>](./Get-AzApiManagementCertificate.md)

[<span data-ttu-id="b0685-137">New-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="b0685-137">New-AzApiManagementCertificate</span></span>](./New-AzApiManagementCertificate.md)

[<span data-ttu-id="b0685-138">Set-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="b0685-138">Set-AzApiManagementCertificate</span></span>](./Set-AzApiManagementCertificate.md)


