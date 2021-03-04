---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementapifromgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiFromGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiFromGateway.md
ms.openlocfilehash: 2b50ddb0186e1c7ca8bc0da237f3fca833cb7367
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903690"
---
# <span data-ttu-id="33c0c-101">Remove-AzApiManagementApiFromGateway</span><span class="sxs-lookup"><span data-stu-id="33c0c-101">Remove-AzApiManagementApiFromGateway</span></span>

## <span data-ttu-id="33c0c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="33c0c-102">SYNOPSIS</span></span>
<span data-ttu-id="33c0c-103">將 API 附加到閘道。</span><span class="sxs-lookup"><span data-stu-id="33c0c-103">Attaches an API to a gateway.</span></span>

## <span data-ttu-id="33c0c-104">語法</span><span class="sxs-lookup"><span data-stu-id="33c0c-104">SYNTAX</span></span>

```
Remove-AzApiManagementApiFromGateway -Context <PsApiManagementContext> -GatewayId <String> -ApiId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="33c0c-105">描述</span><span class="sxs-lookup"><span data-stu-id="33c0c-105">DESCRIPTION</span></span>
<span data-ttu-id="33c0c-106">**Remove-AzApiManagementApiFromGateway** Cmdlet 會將 API 附加到閘道。</span><span class="sxs-lookup"><span data-stu-id="33c0c-106">The **Remove-AzApiManagementApiFromGateway** cmdlet attaches an API to a gateway.</span></span>

## <span data-ttu-id="33c0c-107">例子</span><span class="sxs-lookup"><span data-stu-id="33c0c-107">EXAMPLES</span></span>

### <span data-ttu-id="33c0c-108">範例 1：從閘道移除 API</span><span class="sxs-lookup"><span data-stu-id="33c0c-108">Example 1: Remove an API from a gateway</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementApiFromGateway -Context $ApiMgmtContext -GatewayId "0123456789" -ApiId "0001" -PassThru
```

<span data-ttu-id="33c0c-109">此命令會從閘道移除指定的 API。</span><span class="sxs-lookup"><span data-stu-id="33c0c-109">This command removes the specified API from a gateway.</span></span>

## <span data-ttu-id="33c0c-110">參數</span><span class="sxs-lookup"><span data-stu-id="33c0c-110">PARAMETERS</span></span>

### <span data-ttu-id="33c0c-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="33c0c-111">-ApiId</span></span>
<span data-ttu-id="33c0c-112">要從閘道移除的現有 API 識別碼。</span><span class="sxs-lookup"><span data-stu-id="33c0c-112">Identifier of existing APIs to remove from the Gateway.</span></span>
<span data-ttu-id="33c0c-113">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="33c0c-113">This parameter is required.</span></span>

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

### <span data-ttu-id="33c0c-114">-內容</span><span class="sxs-lookup"><span data-stu-id="33c0c-114">-Context</span></span>
<span data-ttu-id="33c0c-115">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="33c0c-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="33c0c-116">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="33c0c-116">This parameter is required.</span></span>

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

### <span data-ttu-id="33c0c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33c0c-117">-DefaultProfile</span></span>
<span data-ttu-id="33c0c-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="33c0c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="33c0c-119">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="33c0c-119">-GatewayId</span></span>
<span data-ttu-id="33c0c-120">移除 API 之現有閘道的識別碼。</span><span class="sxs-lookup"><span data-stu-id="33c0c-120">Identifier of existing Gateway to remove API from.</span></span>
<span data-ttu-id="33c0c-121">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="33c0c-121">This parameter is required.</span></span>

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

### <span data-ttu-id="33c0c-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="33c0c-122">-PassThru</span></span>
<span data-ttu-id="33c0c-123">如果指定，如果作業成功，會寫入 True。</span><span class="sxs-lookup"><span data-stu-id="33c0c-123">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="33c0c-124">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="33c0c-124">This parameter is optional.</span></span>
<span data-ttu-id="33c0c-125">預設值為 False。</span><span class="sxs-lookup"><span data-stu-id="33c0c-125">Default value is false.</span></span>

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

### <span data-ttu-id="33c0c-126">-確認</span><span class="sxs-lookup"><span data-stu-id="33c0c-126">-Confirm</span></span>
<span data-ttu-id="33c0c-127">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="33c0c-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33c0c-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33c0c-128">-WhatIf</span></span>
<span data-ttu-id="33c0c-129">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="33c0c-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="33c0c-130">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="33c0c-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33c0c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33c0c-131">CommonParameters</span></span>
<span data-ttu-id="33c0c-132">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="33c0c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33c0c-133">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="33c0c-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33c0c-134">輸入</span><span class="sxs-lookup"><span data-stu-id="33c0c-134">INPUTS</span></span>

### <span data-ttu-id="33c0c-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementCoNtext</span><span class="sxs-lookup"><span data-stu-id="33c0c-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="33c0c-136">System.String</span><span class="sxs-lookup"><span data-stu-id="33c0c-136">System.String</span></span>

### <span data-ttu-id="33c0c-137">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="33c0c-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="33c0c-138">輸出</span><span class="sxs-lookup"><span data-stu-id="33c0c-138">OUTPUTS</span></span>

### <span data-ttu-id="33c0c-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="33c0c-139">System.Boolean</span></span>

## <span data-ttu-id="33c0c-140">筆記</span><span class="sxs-lookup"><span data-stu-id="33c0c-140">NOTES</span></span>

## <span data-ttu-id="33c0c-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="33c0c-141">RELATED LINKS</span></span>
