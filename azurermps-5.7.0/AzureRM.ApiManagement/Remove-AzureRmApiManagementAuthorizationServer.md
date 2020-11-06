---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: C2CC10DE-1D36-4937-8A3E-9776BE80DF9A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementAuthorizationServer.md
ms.openlocfilehash: c9133c7a2924b4151afd01f257fe6b54a9eeb00d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456283"
---
# <span data-ttu-id="2546e-101">Remove-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="2546e-101">Remove-AzureRmApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="2546e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2546e-102">SYNOPSIS</span></span>
<span data-ttu-id="2546e-103">移除授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="2546e-103">Removes an authorization server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2546e-104">句法</span><span class="sxs-lookup"><span data-stu-id="2546e-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementAuthorizationServer -Context <PsApiManagementContext> -ServerId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2546e-105">說明</span><span class="sxs-lookup"><span data-stu-id="2546e-105">DESCRIPTION</span></span>
<span data-ttu-id="2546e-106">**AzureRmApiManagementAuthorizationServer** Cmdlet 會移除 Azure API 管理授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="2546e-106">The **Remove-AzureRmApiManagementAuthorizationServer** cmdlet removes an Azure API Management authorization server.</span></span>

## <span data-ttu-id="2546e-107">示例</span><span class="sxs-lookup"><span data-stu-id="2546e-107">EXAMPLES</span></span>

## <span data-ttu-id="2546e-108">參數</span><span class="sxs-lookup"><span data-stu-id="2546e-108">PARAMETERS</span></span>

### <span data-ttu-id="2546e-109">-內容</span><span class="sxs-lookup"><span data-stu-id="2546e-109">-Context</span></span>
<span data-ttu-id="2546e-110">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="2546e-110">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2546e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2546e-111">-DefaultProfile</span></span>
<span data-ttu-id="2546e-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2546e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2546e-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2546e-113">-PassThru</span></span>
<span data-ttu-id="2546e-114">passthru</span><span class="sxs-lookup"><span data-stu-id="2546e-114">passthru</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2546e-115">-ServerId</span><span class="sxs-lookup"><span data-stu-id="2546e-115">-ServerId</span></span>
<span data-ttu-id="2546e-116">指定要移除的授權伺服器識別碼。</span><span class="sxs-lookup"><span data-stu-id="2546e-116">Specifies the ID of the authorization server to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2546e-117">-確認</span><span class="sxs-lookup"><span data-stu-id="2546e-117">-Confirm</span></span>
<span data-ttu-id="2546e-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2546e-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2546e-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2546e-119">-WhatIf</span></span>
<span data-ttu-id="2546e-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2546e-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2546e-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2546e-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2546e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2546e-122">CommonParameters</span></span>
<span data-ttu-id="2546e-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2546e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2546e-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2546e-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2546e-125">輸入</span><span class="sxs-lookup"><span data-stu-id="2546e-125">INPUTS</span></span>

### <span data-ttu-id="2546e-126">所有</span><span class="sxs-lookup"><span data-stu-id="2546e-126">None</span></span>
<span data-ttu-id="2546e-127">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="2546e-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2546e-128">輸出</span><span class="sxs-lookup"><span data-stu-id="2546e-128">OUTPUTS</span></span>

### <span data-ttu-id="2546e-129">布林值</span><span class="sxs-lookup"><span data-stu-id="2546e-129">Boolean</span></span>

## <span data-ttu-id="2546e-130">筆記</span><span class="sxs-lookup"><span data-stu-id="2546e-130">NOTES</span></span>

## <span data-ttu-id="2546e-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="2546e-131">RELATED LINKS</span></span>

[<span data-ttu-id="2546e-132">AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="2546e-132">Get-AzureRmApiManagementAuthorizationServer</span></span>](./Get-AzureRmApiManagementAuthorizationServer.md)

[<span data-ttu-id="2546e-133">新-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="2546e-133">New-AzureRmApiManagementAuthorizationServer</span></span>](./New-AzureRmApiManagementAuthorizationServer.md)

[<span data-ttu-id="2546e-134">Set-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="2546e-134">Set-AzureRmApiManagementAuthorizationServer</span></span>](./Set-AzureRmApiManagementAuthorizationServer.md)


