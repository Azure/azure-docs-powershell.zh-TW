---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: C2CC10DE-1D36-4937-8A3E-9776BE80DF9A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementAuthorizationServer.md
ms.openlocfilehash: 2fc658f5bab9e6233e6b7279abc0ae80832bcc8a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93444140"
---
# <span data-ttu-id="0e905-101">Remove-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="0e905-101">Remove-AzureRmApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="0e905-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0e905-102">SYNOPSIS</span></span>
<span data-ttu-id="0e905-103">移除授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="0e905-103">Removes an authorization server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0e905-104">句法</span><span class="sxs-lookup"><span data-stu-id="0e905-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementAuthorizationServer -Context <PsApiManagementContext> -ServerId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e905-105">說明</span><span class="sxs-lookup"><span data-stu-id="0e905-105">DESCRIPTION</span></span>
<span data-ttu-id="0e905-106">**AzureRmApiManagementAuthorizationServer** Cmdlet 會移除 Azure API 管理授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="0e905-106">The **Remove-AzureRmApiManagementAuthorizationServer** cmdlet removes an Azure API Management authorization server.</span></span>

## <span data-ttu-id="0e905-107">示例</span><span class="sxs-lookup"><span data-stu-id="0e905-107">EXAMPLES</span></span>

## <span data-ttu-id="0e905-108">參數</span><span class="sxs-lookup"><span data-stu-id="0e905-108">PARAMETERS</span></span>

### <span data-ttu-id="0e905-109">-內容</span><span class="sxs-lookup"><span data-stu-id="0e905-109">-Context</span></span>
<span data-ttu-id="0e905-110">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="0e905-110">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="0e905-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e905-111">-DefaultProfile</span></span>
<span data-ttu-id="0e905-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0e905-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0e905-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0e905-113">-PassThru</span></span>
<span data-ttu-id="0e905-114">passthru</span><span class="sxs-lookup"><span data-stu-id="0e905-114">passthru</span></span>

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

### <span data-ttu-id="0e905-115">-ServerId</span><span class="sxs-lookup"><span data-stu-id="0e905-115">-ServerId</span></span>
<span data-ttu-id="0e905-116">指定要移除的授權伺服器識別碼。</span><span class="sxs-lookup"><span data-stu-id="0e905-116">Specifies the ID of the authorization server to remove.</span></span>

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

### <span data-ttu-id="0e905-117">-確認</span><span class="sxs-lookup"><span data-stu-id="0e905-117">-Confirm</span></span>
<span data-ttu-id="0e905-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="0e905-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e905-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e905-119">-WhatIf</span></span>
<span data-ttu-id="0e905-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0e905-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0e905-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0e905-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e905-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e905-122">CommonParameters</span></span>
<span data-ttu-id="0e905-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0e905-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e905-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0e905-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e905-125">輸入</span><span class="sxs-lookup"><span data-stu-id="0e905-125">INPUTS</span></span>

### <span data-ttu-id="0e905-126">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="0e905-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="0e905-127">System.object</span><span class="sxs-lookup"><span data-stu-id="0e905-127">System.String</span></span>

### <span data-ttu-id="0e905-128">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="0e905-128">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="0e905-129">輸出</span><span class="sxs-lookup"><span data-stu-id="0e905-129">OUTPUTS</span></span>

### <span data-ttu-id="0e905-130">System.object</span><span class="sxs-lookup"><span data-stu-id="0e905-130">System.Boolean</span></span>

## <span data-ttu-id="0e905-131">筆記</span><span class="sxs-lookup"><span data-stu-id="0e905-131">NOTES</span></span>

## <span data-ttu-id="0e905-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="0e905-132">RELATED LINKS</span></span>

[<span data-ttu-id="0e905-133">AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="0e905-133">Get-AzureRmApiManagementAuthorizationServer</span></span>](./Get-AzureRmApiManagementAuthorizationServer.md)

[<span data-ttu-id="0e905-134">新-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="0e905-134">New-AzureRmApiManagementAuthorizationServer</span></span>](./New-AzureRmApiManagementAuthorizationServer.md)

[<span data-ttu-id="0e905-135">Set-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="0e905-135">Set-AzureRmApiManagementAuthorizationServer</span></span>](./Set-AzureRmApiManagementAuthorizationServer.md)


