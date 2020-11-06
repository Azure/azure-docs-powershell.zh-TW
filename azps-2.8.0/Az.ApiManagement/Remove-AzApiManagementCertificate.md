---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 9B261CD8-5209-4C14-A6F8-97D61B641642
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementCertificate.md
ms.openlocfilehash: fc22515fc1d1fc4c3975ee315ec9f7bf611e67c2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93613928"
---
# <span data-ttu-id="57adc-101">Remove-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="57adc-101">Remove-AzApiManagementCertificate</span></span>

## <span data-ttu-id="57adc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="57adc-102">SYNOPSIS</span></span>
<span data-ttu-id="57adc-103">移除 API 管理憑證。</span><span class="sxs-lookup"><span data-stu-id="57adc-103">Removes an API Management certificate.</span></span>

## <span data-ttu-id="57adc-104">句法</span><span class="sxs-lookup"><span data-stu-id="57adc-104">SYNTAX</span></span>

```
Remove-AzApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="57adc-105">說明</span><span class="sxs-lookup"><span data-stu-id="57adc-105">DESCRIPTION</span></span>
<span data-ttu-id="57adc-106">**AzApiManagementCertificate** Cmdlet 會移除 Azure API 管理憑證。</span><span class="sxs-lookup"><span data-stu-id="57adc-106">The **Remove-AzApiManagementCertificate** cmdlet removes an Azure API Management certificate.</span></span>

## <span data-ttu-id="57adc-107">示例</span><span class="sxs-lookup"><span data-stu-id="57adc-107">EXAMPLES</span></span>

### <span data-ttu-id="57adc-108">範例1：移除憑證</span><span class="sxs-lookup"><span data-stu-id="57adc-108">Example 1: Remove a certificate</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementCertificate -Context $ApiMgmtContext -CertificateId "0123456789" -Force
```

<span data-ttu-id="57adc-109">這個命令會移除指定的 API 管理憑證。</span><span class="sxs-lookup"><span data-stu-id="57adc-109">This command removes the specified API Management certificate.</span></span>
<span data-ttu-id="57adc-110">由於已指定 *Force* 參數，因此不需要確認。</span><span class="sxs-lookup"><span data-stu-id="57adc-110">Because the *Force* parameter is specified, no confirmation is required.</span></span>

## <span data-ttu-id="57adc-111">參數</span><span class="sxs-lookup"><span data-stu-id="57adc-111">PARAMETERS</span></span>

### <span data-ttu-id="57adc-112">-CertificateId</span><span class="sxs-lookup"><span data-stu-id="57adc-112">-CertificateId</span></span>
<span data-ttu-id="57adc-113">指定要移除的憑證識別碼。</span><span class="sxs-lookup"><span data-stu-id="57adc-113">Specifies the ID of the certificate to remove.</span></span>

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

### <span data-ttu-id="57adc-114">-內容</span><span class="sxs-lookup"><span data-stu-id="57adc-114">-Context</span></span>
<span data-ttu-id="57adc-115">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="57adc-115">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="57adc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57adc-116">-DefaultProfile</span></span>
<span data-ttu-id="57adc-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="57adc-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="57adc-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="57adc-118">-PassThru</span></span>
<span data-ttu-id="57adc-119">passthru</span><span class="sxs-lookup"><span data-stu-id="57adc-119">passthru</span></span>

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

### <span data-ttu-id="57adc-120">-確認</span><span class="sxs-lookup"><span data-stu-id="57adc-120">-Confirm</span></span>
<span data-ttu-id="57adc-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="57adc-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57adc-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57adc-122">-WhatIf</span></span>
<span data-ttu-id="57adc-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="57adc-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57adc-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="57adc-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57adc-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57adc-125">CommonParameters</span></span>
<span data-ttu-id="57adc-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="57adc-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57adc-127">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="57adc-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57adc-128">輸入</span><span class="sxs-lookup"><span data-stu-id="57adc-128">INPUTS</span></span>

### <span data-ttu-id="57adc-129">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="57adc-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="57adc-130">System.object</span><span class="sxs-lookup"><span data-stu-id="57adc-130">System.String</span></span>

### <span data-ttu-id="57adc-131">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="57adc-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="57adc-132">輸出</span><span class="sxs-lookup"><span data-stu-id="57adc-132">OUTPUTS</span></span>

### <span data-ttu-id="57adc-133">System.object</span><span class="sxs-lookup"><span data-stu-id="57adc-133">System.Boolean</span></span>

## <span data-ttu-id="57adc-134">筆記</span><span class="sxs-lookup"><span data-stu-id="57adc-134">NOTES</span></span>

## <span data-ttu-id="57adc-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="57adc-135">RELATED LINKS</span></span>

[<span data-ttu-id="57adc-136">AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="57adc-136">Get-AzApiManagementCertificate</span></span>](./Get-AzApiManagementCertificate.md)

[<span data-ttu-id="57adc-137">新-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="57adc-137">New-AzApiManagementCertificate</span></span>](./New-AzApiManagementCertificate.md)

[<span data-ttu-id="57adc-138">Set-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="57adc-138">Set-AzApiManagementCertificate</span></span>](./Set-AzApiManagementCertificate.md)

